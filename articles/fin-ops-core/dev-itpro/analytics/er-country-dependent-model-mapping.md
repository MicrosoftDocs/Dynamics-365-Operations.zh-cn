---
title: 配置依赖于国家/地区上下文的 ER 模型映射
description: 本主题说明如何设置 ER 模型映射，以使其依赖于控制其使用的法人的国家/地区上下文。
author: NickSelin
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 83cd99350f58a56d121d694393edc4eb98af728a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753760"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a><span data-ttu-id="eba13-103">配置依赖于国家/地区上下文的 ER 模型映射</span><span class="sxs-lookup"><span data-stu-id="eba13-103">Configure country context dependent ER model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="eba13-104">您可以配置电子报告 (ER) 模型映射，以便它们实现通用的 ER 数据模型，但特定于 Dynamics 365 Finance。</span><span class="sxs-lookup"><span data-stu-id="eba13-104">You can configure Electronic reporting (ER) model mappings so that they implement a generic ER data model but are specific to Dynamics 365 Finance.</span></span> <span data-ttu-id="eba13-105">本主题说明如何为 ER 数据模型设计多个 ER 模型映射，以控制来自具有不同国家/地区上下文的公司的相应 ER 格式如何使用它们。</span><span class="sxs-lookup"><span data-stu-id="eba13-105">This topic explains how to design multiple ER model mappings for an ER data model to control how they are used by corresponding ER formats that are run from companies that have different country/region contexts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eba13-106">先决条件</span><span class="sxs-lookup"><span data-stu-id="eba13-106">Prerequisites</span></span>

<span data-ttu-id="eba13-107">要完成本主题中的示例，您必须具有以下访问权限：</span><span class="sxs-lookup"><span data-stu-id="eba13-107">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="eba13-108">访问 Finance 的以下其中一个角色：</span><span class="sxs-lookup"><span data-stu-id="eba13-108">Access to Finance for one of the following roles:</span></span>
    - <span data-ttu-id="eba13-109">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="eba13-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="eba13-110">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="eba13-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="eba13-111">系统管理员</span><span class="sxs-lookup"><span data-stu-id="eba13-111">System administrator</span></span>

- <span data-ttu-id="eba13-112">对于下列角色之一，已为与 Finance 相同的租户配置的 Regulatory Configuration Services (RCS) 的实例：</span><span class="sxs-lookup"><span data-stu-id="eba13-112">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>
    - <span data-ttu-id="eba13-113">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="eba13-113">Electronic reporting developer</span></span>
    - <span data-ttu-id="eba13-114">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="eba13-114">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="eba13-115">系统管理员</span><span class="sxs-lookup"><span data-stu-id="eba13-115">System administrator</span></span>

<span data-ttu-id="eba13-116">本主题中的某些步骤需要执行 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-116">Some steps in this topic require execution of an ER format.</span></span> <span data-ttu-id="eba13-117">在某些情况下，ER 格式的执行会受到您当前登录的公司所在的国家地区上下文的影响。</span><span class="sxs-lookup"><span data-stu-id="eba13-117">In some cases, execution of an ER format is affected by the country/region context of the company that you're currently signed in to.</span></span> <span data-ttu-id="eba13-118">如果具有所需国家/地区上下文的公司在 RCS 中可用，则可以在当前 RCS 实例中运行 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-118">You can run an ER format in the current RCS instance if the company that has the required country/region context is available in RCS.</span></span> <span data-ttu-id="eba13-119">否则，您必须将使用 ER 数据模型的 ER 模型映射和 ER 格式配置的已完成版本上载到 Finance 实例，然后在该 Finance 实例中运行 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-119">Otherwise, you must upload a completed version of the ER model mapping and ER format configurations that use the ER data model to your Finance instance, and then run the ER format in that Finance instance.</span></span> <span data-ttu-id="eba13-120">有关如何将 RCS 中驻留的配置导入到 Finance 实例中的信息，请参阅[从 RCS 导入配置](rcs-download-configurations.md)。</span><span class="sxs-lookup"><span data-stu-id="eba13-120">For information about how to import configurations that reside in RCS into a Finance instance, see [Import configurations from RCS](rcs-download-configurations.md).</span></span>

## <a name="single-model-mapping-case"></a><span data-ttu-id="eba13-121">单个模型映射案例</span><span class="sxs-lookup"><span data-stu-id="eba13-121">Single model mapping case</span></span>

<span data-ttu-id="eba13-122">请按照本主题的[附录 1](#appendix1) 中的步骤设计所需的 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="eba13-122">Follow the steps in [Appendix 1](#appendix1) of this topic to design the required ER components.</span></span> <span data-ttu-id="eba13-123">现在，您具有 **映射(一般)** 模型映射配置，其中包含 **入口点 1** 定义的模型映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-123">You now have the **Mapping (General)** model mapping configuration that contains the model mapping for the **Entry point 1** definition.</span></span>

![ER 配置页](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="eba13-125">运行配置的格式</span><span class="sxs-lookup"><span data-stu-id="eba13-125">Run the configured format</span></span>

1.  <span data-ttu-id="eba13-126">在 **配置页** 的 **版本** 快速选项卡上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="eba13-126">On the **Configurations page**, on the **Versions** FastTab, select **Run**.</span></span>
2.  <span data-ttu-id="eba13-127">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-127">Select **OK**.</span></span>

<span data-ttu-id="eba13-128">请注意，Web 浏览器提供了下载由执行的 ER 格式生成的文本文件的功能。</span><span class="sxs-lookup"><span data-stu-id="eba13-128">Notice that the web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="eba13-129">因为此格式已配置为使用 **入口点 1** 定义，并且当前仅单个模型映射可用于包含此定义的映射的基本模型，所以执行的 ER 格式使用 **映射(一般)** 配置的 **映射(一般)** 模型映射作为数据源。</span><span class="sxs-lookup"><span data-stu-id="eba13-129">Because this format was configured to use the **Entry point 1** definition, and only a single model mapping is currently available for the base model that contains a mapping for this definition, the executed ER format used the **Mapping (General)** model mapping of the **Mapping (General)** configuration as a data source.</span></span> <span data-ttu-id="eba13-130">因此，下载的文件包含 **通用功能 1** 文本。</span><span class="sxs-lookup"><span data-stu-id="eba13-130">Therefore, the downloaded file contains the **Generic functionality 1** text.</span></span>

## <a name="multiple-shared-model-mappings-case"></a><span data-ttu-id="eba13-131">多个共享模型映射案例</span><span class="sxs-lookup"><span data-stu-id="eba13-131">Multiple shared model mappings case</span></span>

<span data-ttu-id="eba13-132">请按照本主题的[附录 2](#appendix2) 中的步骤设计所需的 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="eba13-132">Follow the steps in [Appendix 2](#appendix2) of this topic to design the required ER components.</span></span> <span data-ttu-id="eba13-133">现在，您具有 **映射(一般)** 和 **映射(一般)自定义** 模型映射配置，每个配置都包含 **入口点 1** 定义的模型映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-133">You now have **Mapping (General)** and **Mapping (General) custom** model mapping configurations, each of which contains the model mapping for the **Entry point 1** definition.</span></span>

![ER 配置页](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="eba13-135">运行配置的格式</span><span class="sxs-lookup"><span data-stu-id="eba13-135">Run the configured format</span></span>

1.  <span data-ttu-id="eba13-136">在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。</span><span class="sxs-lookup"><span data-stu-id="eba13-136">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="eba13-137">在 **版本** 快速选项卡上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="eba13-137">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="eba13-138">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-138">Select **OK**.</span></span>

<span data-ttu-id="eba13-139">请注意，所选 ER 格式的执行将不成功。</span><span class="sxs-lookup"><span data-stu-id="eba13-139">Notice that execution of the selected ER format is unsuccessful.</span></span> <span data-ttu-id="eba13-140">一条错误消息通知您，**映射(一般)** 和 **映射(一般)自定义** 模型映射配置中的 **用于了解映射的模型** 模型和 **入口点 1** 定义存在多个模型映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-140">An error message informs you that more than one model mapping exists for the **Model to learn mappings** model and the **Entry point 1** definition in the **Mapping (General)** and **Mapping (General) custom** model mapping configurations.</span></span> <span data-ttu-id="eba13-141">此消息还建议您选择这些配置之一作为默认配置。</span><span class="sxs-lookup"><span data-stu-id="eba13-141">The message also recommends that you select one of those configurations as the default configuration.</span></span>

![ER 配置页](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a><span data-ttu-id="eba13-143">定义默认映射配置</span><span class="sxs-lookup"><span data-stu-id="eba13-143">Define a default mapping configuration</span></span>

<span data-ttu-id="eba13-144">请按照以下步骤将 **映射(一般)自定义** 模型映射配置定义为默认配置，以便其映射可用作 **用于了解映射的格式** ER 格式的数据源。</span><span class="sxs-lookup"><span data-stu-id="eba13-144">Follow these steps to define the **Mapping (General) custom** model mapping configuration as the default configuration, so that its mappings can be used as data sources for the **Format to learn mappings** ER format.</span></span>

1.  <span data-ttu-id="eba13-145">在 **配置** 页上的配置树中，选择 **映射(一般)自定义**。</span><span class="sxs-lookup"><span data-stu-id="eba13-145">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="eba13-146">根据需要，选择 **编辑** 以使当前页面可供编辑。</span><span class="sxs-lookup"><span data-stu-id="eba13-146">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="eba13-147">将 **模型映射的默认值** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="eba13-147">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="eba13-148">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-148">Select **Save**.</span></span>

![ER 配置页](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="eba13-150">运行配置的格式</span><span class="sxs-lookup"><span data-stu-id="eba13-150">Run the configured format</span></span>

1.  <span data-ttu-id="eba13-151">在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。</span><span class="sxs-lookup"><span data-stu-id="eba13-151">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="eba13-152">在 **版本** 快速选项卡上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="eba13-152">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="eba13-153">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-153">Select **OK**.</span></span>

<span data-ttu-id="eba13-154">请注意，所选 ER 格式的执行将成功。</span><span class="sxs-lookup"><span data-stu-id="eba13-154">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="eba13-155">Web 浏览器提供了下载由执行的 ER 格式生成的文本文件的功能。</span><span class="sxs-lookup"><span data-stu-id="eba13-155">The web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="eba13-156">由于此格式已配置为使用 **入口点 1** 定义，并且选择了 **映射(一般)自定义** 模型映射配置作为默认配置，因此执行的 ER 格式使用了 **映射(一般)自定义** 配置的 **映射(一般)复制** 模型映射作为数据源。</span><span class="sxs-lookup"><span data-stu-id="eba13-156">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="eba13-157">因此，下载的文件包含 **通用功能 1 自定义** 文本。</span><span class="sxs-lookup"><span data-stu-id="eba13-157">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

> [!NOTE]
> <span data-ttu-id="eba13-158">如果您更改当前登录的公司并再次运行此 ER 格式，则在生成的文件中将获得相同的内容，因为默认的 ER 模型映射配置不包含任何依赖于公司的限制。</span><span class="sxs-lookup"><span data-stu-id="eba13-158">If you change the company that you're currently signed in to and run this ER format again, you get the same content in the generated file, because the default ER model mapping configuration doesn't contain any company-dependent restrictions.</span></span>

## <a name="multiple-mixed-model-mappings-case"></a><span data-ttu-id="eba13-159">多个混合模型映射案例</span><span class="sxs-lookup"><span data-stu-id="eba13-159">Multiple mixed model mappings case</span></span>

<span data-ttu-id="eba13-160">请按照本主题的[附录 3](#appendix3) 中的步骤设计所需的 ER 组件。</span><span class="sxs-lookup"><span data-stu-id="eba13-160">Follow the steps in [Appendix 3](#appendix3) of this topic to design the required ER components.</span></span> <span data-ttu-id="eba13-161">您现在具有 **映射(一般)**、**映射(一般)自定义** 和 **映射(FR)模型映射** 配置，其包含 **入口点 1** 定义的模型映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-161">You now have **Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR) model mapping** configurations that contain the model mapping for the **Entry point 1** definition.</span></span>

<span data-ttu-id="eba13-162">请注意，已配置 **映射(FR)** 模型映射配置的版本 1，使其仅应用于在具有法国国家/地区上下文的 Finance 公司中运行的 **用于了解映射的模型** 模型的格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-162">Notice that version 1 of the **Mapping (FR)** model mapping configuration is configured so that it applies only to ER formats of the **Model to learn mappings** model that are run in Finance companies that have French country/region context.</span></span>

![ER 配置页](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="eba13-164">运行配置的格式</span><span class="sxs-lookup"><span data-stu-id="eba13-164">Run the configured format</span></span>

1.  <span data-ttu-id="eba13-165">将公司更改为 **FRSI**。</span><span class="sxs-lookup"><span data-stu-id="eba13-165">Change the company to **FRSI**.</span></span>
2.  <span data-ttu-id="eba13-166">在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。</span><span class="sxs-lookup"><span data-stu-id="eba13-166">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
3.  <span data-ttu-id="eba13-167">在 **版本** 快速选项卡上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="eba13-167">On the **Versions** FastTab, select **Run**.</span></span>
4.  <span data-ttu-id="eba13-168">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-168">Select **OK**.</span></span>

<span data-ttu-id="eba13-169">请注意，所选 ER 格式的执行将成功。</span><span class="sxs-lookup"><span data-stu-id="eba13-169">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="eba13-170">Web 浏览器提供了下载由执行的 ER 格式生成的文本文件的功能。</span><span class="sxs-lookup"><span data-stu-id="eba13-170">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="eba13-171">由于此格式已配置为使用 **入口点 1** 定义，并且选择了 **映射(一般)自定义** 模型映射配置作为默认配置，因此执行的 ER 格式使用了 **映射(一般)自定义** 配置的 **映射(一般)复制** 模型映射作为数据源。</span><span class="sxs-lookup"><span data-stu-id="eba13-171">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="eba13-172">因此，下载的文件包含 **通用功能 1 自定义** 文本。</span><span class="sxs-lookup"><span data-stu-id="eba13-172">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a><span data-ttu-id="eba13-173">将特定于法国的映射配置定义为默认配置</span><span class="sxs-lookup"><span data-stu-id="eba13-173">Define the France-specific mapping configuration as the default configuration</span></span>

<span data-ttu-id="eba13-174">请按照以下步骤将自定义 **映射(FR)** 模型映射配置定义为默认配置。</span><span class="sxs-lookup"><span data-stu-id="eba13-174">Follow these steps to define the custom **Mapping (FR)** model mapping configuration as the default configuration.</span></span> <span data-ttu-id="eba13-175">请注意，由于此映射特定于法国，因此将被视为所有在 **ISO 国家/地区代码** 字段中指定了 **FR** 国家/地区代码的模型映射配置之间的默认映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-175">Note that, because this mapping is specific to France, it will be considered the default mapping between all model mapping configurations that have the **FR** country code specified in the **ISO country/region codes** field.</span></span>

1.  <span data-ttu-id="eba13-176">在 **配置** 页上的配置树中，选择 **映射(FR)**。</span><span class="sxs-lookup"><span data-stu-id="eba13-176">On the **Configurations** page, in the configurations tree, select **Mapping (FR)**.</span></span>
2.  <span data-ttu-id="eba13-177">根据需要，选择 **编辑** 以使当前页面可供编辑。</span><span class="sxs-lookup"><span data-stu-id="eba13-177">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="eba13-178">将 **模型映射的默认值** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="eba13-178">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="eba13-179">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-179">Select **Save**.</span></span>

![ER 配置页](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="eba13-181">运行配置的格式</span><span class="sxs-lookup"><span data-stu-id="eba13-181">Run the configured format</span></span>

1.  <span data-ttu-id="eba13-182">在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。</span><span class="sxs-lookup"><span data-stu-id="eba13-182">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="eba13-183">在 **版本** 快速选项卡上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="eba13-183">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="eba13-184">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-184">Select **OK**.</span></span>

<span data-ttu-id="eba13-185">请注意，所选 ER 格式的执行将成功。</span><span class="sxs-lookup"><span data-stu-id="eba13-185">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="eba13-186">Web 浏览器提供了下载由执行的 ER 格式生成的文本文件的功能。</span><span class="sxs-lookup"><span data-stu-id="eba13-186">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="eba13-187">由于此格式已配置为使用 **入口点 1** 定义，并且选择了 **映射(FR)** 模型映射配置作为默认配置，因此执行的 ER 格式使用了 **映射(FR)** 配置的 **映射(FR)** 模型映射作为数据源。</span><span class="sxs-lookup"><span data-stu-id="eba13-187">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (FR)** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (FR)** model mapping of the **Mapping (FR)** configuration as a data source.</span></span> <span data-ttu-id="eba13-188">因此，下载的文件包含 **FR 功能 1** 文本。</span><span class="sxs-lookup"><span data-stu-id="eba13-188">Therefore, the downloaded file contains the **FR functionality 1** text.</span></span>

> [!NOTE]
> <span data-ttu-id="eba13-189">如果您更改当前登录的公司并再次运行此 ER 格式，则输出将依赖于所选公司的国家/地区上下文。</span><span class="sxs-lookup"><span data-stu-id="eba13-189">If you change the company that you're currently signed in to and run this ER format again, the output will depend on the country/region context of the selected company.</span></span>

## <a name="other-model-mapping-cases"></a><span data-ttu-id="eba13-190">其他模型映射案例</span><span class="sxs-lookup"><span data-stu-id="eba13-190">Other model mapping cases</span></span>

<span data-ttu-id="eba13-191">如您所见，选择用于执行 ER 格式的模型映射的工作方式如下：</span><span class="sxs-lookup"><span data-stu-id="eba13-191">As you've seen, the selection of a model mapping for the execution of an ER format works in the following way:</span></span>

- <span data-ttu-id="eba13-192">指定 ER 格式使用的模型映射定义（本主题示例中的 **入口点 1**）。</span><span class="sxs-lookup"><span data-stu-id="eba13-192">The model mapping definition that an ER format uses is specified (**Entry point 1** in the examples in this topic).</span></span>
- <span data-ttu-id="eba13-193">包含具有指定定义的映射并且满足已配置的任何国家/地区上下文限制的所有映射配置，都可能能够用于运行 ER 格式（本主题示例中的 **映射(一般)**、**映射(一般)自定义** 和 **映射(FR)**）。</span><span class="sxs-lookup"><span data-stu-id="eba13-193">All mapping configurations that contain a mapping that has the specified definition, and that satisfy any country/region context restrictions that are configured, can potentially be used to run the ER format (**Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="eba13-194">具有国家/地区上下文限制的任何默认模型映射都具有最高的选择优先级（本主题示例中的 **映射(FR)**）。</span><span class="sxs-lookup"><span data-stu-id="eba13-194">Any default model mapping that has country/region context restrictions has the highest priority for selection (**Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="eba13-195">没有国家/地区上下文限制的任何默认模型映射都具有更高的选择优先级（本主题示例中的 **映射(一般)自定义**）。</span><span class="sxs-lookup"><span data-stu-id="eba13-195">Any default model mapping that doesn't have country/region context restrictions has the next higher priority for selection  (**Mapping (General) custom** in the examples in this topic).</span></span>
- <span data-ttu-id="eba13-196">具有国家/地区上下文限制的任何模型映射都比没有国家/地区上下文限制的模型映射具有更高的选择优先级。</span><span class="sxs-lookup"><span data-stu-id="eba13-196">Any model mapping that has country/region context restrictions has higher priority for selection than a model mapping that doesn't have country/region context restrictions.</span></span>

<span data-ttu-id="eba13-197">下表提供了有关模型映射设置的所有可能案例的模型映射选择结果的信息：</span><span class="sxs-lookup"><span data-stu-id="eba13-197">The following table provides information about the results of model mapping selection for all possible cases for model mapping settings:</span></span>

- <span data-ttu-id="eba13-198">第 1 列指示是否显示没有国家/地区上下文限制的第一个模型映射（例如，共享的 **映射(一般)** 映射），如果显示，则指示其 **模型映射的默认值** 选项是否设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="eba13-198">Column 1 indicates whether the first model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="eba13-199">第 2 列指示是否显示没有国家/地区上下文限制的第二个模型映射（例如，共享的 **映射(一般)自定义** 映射），如果显示，则指示其 **模型映射的默认值** 选项是否设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="eba13-199">Column 2 indicates whether the second model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General) custom** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="eba13-200">第 3 列指示是否显示具有国家/地区 A 上下文限制的第一个模型映射（例如，特定于法国的 **映射(FR)** 映射），如果显示，则指示其 **模型映射的默认值** 选项是否设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="eba13-200">Column 3 indicates whether the first model mapping that has country/region A context restrictions (for example, the France-specific **Mapping (FR)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="eba13-201">第 4 列指示是否显示具有国家/地区 A 上下文限制的第二个模型映射，如果显示，则指示其 **模型映射的默认值** 选项是否设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="eba13-201">Column 4 indicates whether the second model mapping that has country/region A context restrictions is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="eba13-202">第 5 列显示在具有国家/地区 A 上下文的公司的控制下执行 ER 格式的模型映射选择的结果。</span><span class="sxs-lookup"><span data-stu-id="eba13-202">Column 5 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region A context.</span></span>
- <span data-ttu-id="eba13-203">第 6 列显示在具有国家/地区 B 上下文的公司的控制下执行 ER 格式的模型映射选择的结果。</span><span class="sxs-lookup"><span data-stu-id="eba13-203">Column 6 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region B context.</span></span>

<span data-ttu-id="eba13-204">在表中，加号 (+) 表示用于运行 ER 格式（Finance 或 RCS）的 Microsoft Azure 服务的当前实例中是否存在模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="eba13-204">In the table, a plus sign (+) indicates the presence of a model mapping configuration in the current instance of the Microsoft Azure service that is used to run an ER format (either Finance or RCS).</span></span>

| <span data-ttu-id="eba13-205">包装箱</span><span class="sxs-lookup"><span data-stu-id="eba13-205">Case</span></span> | <span data-ttu-id="eba13-206">没有国家/地区上下文的模型映射 1 (MM1)</span><span class="sxs-lookup"><span data-stu-id="eba13-206">Model mapping 1 without country/region context (MM1)</span></span> | <span data-ttu-id="eba13-207">没有国家/地区上下文的模型映射 2 (MM2)</span><span class="sxs-lookup"><span data-stu-id="eba13-207">Model mapping 2 without country/region context (MM2)</span></span> | <span data-ttu-id="eba13-208">具有国家/地区 A 上下文的模型映射 1 (MM1A)</span><span class="sxs-lookup"><span data-stu-id="eba13-208">Model mapping 1 with country/region A context (MM1A)</span></span> | <span data-ttu-id="eba13-209">具有国家/地区 A 上下文的模型映射 2 (MM2A)</span><span class="sxs-lookup"><span data-stu-id="eba13-209">Model mapping 2 with country/region A context (MM2A)</span></span> | <span data-ttu-id="eba13-210">在具有国家/地区 A 上下文的公司的控制下运行</span><span class="sxs-lookup"><span data-stu-id="eba13-210">Run under control of a company that has country/region A context</span></span> | <span data-ttu-id="eba13-211">在具有国家/地区 B 上下文的公司的控制下运行</span><span class="sxs-lookup"><span data-stu-id="eba13-211">Run under the control of a company that has country/region B context</span></span> |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     <span data-ttu-id="eba13-212">1</span><span class="sxs-lookup"><span data-stu-id="eba13-212">1</span></span>   |     <span data-ttu-id="eba13-213">2</span><span class="sxs-lookup"><span data-stu-id="eba13-213">2</span></span>   |    <span data-ttu-id="eba13-214">3</span><span class="sxs-lookup"><span data-stu-id="eba13-214">3</span></span>    |    <span data-ttu-id="eba13-215">4</span><span class="sxs-lookup"><span data-stu-id="eba13-215">4</span></span>    |           <span data-ttu-id="eba13-216">5</span><span class="sxs-lookup"><span data-stu-id="eba13-216">5</span></span>               |            <span data-ttu-id="eba13-217">6</span><span class="sxs-lookup"><span data-stu-id="eba13-217">6</span></span>               |
|     <span data-ttu-id="eba13-218">1</span><span class="sxs-lookup"><span data-stu-id="eba13-218">1</span></span>   |         |         |         |         | <span data-ttu-id="eba13-219">错误（缺少映射）</span><span class="sxs-lookup"><span data-stu-id="eba13-219">Error (missing mapping)</span></span>   | <span data-ttu-id="eba13-220">错误（缺少映射）</span><span class="sxs-lookup"><span data-stu-id="eba13-220">Error (missing mapping)</span></span>    |
|     <span data-ttu-id="eba13-221">2</span><span class="sxs-lookup"><span data-stu-id="eba13-221">2</span></span>   |     +   |         |         |         | <span data-ttu-id="eba13-222">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-222">MM1</span></span>                       | <span data-ttu-id="eba13-223">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-223">MM1</span></span>                        |
|     <span data-ttu-id="eba13-224">3</span><span class="sxs-lookup"><span data-stu-id="eba13-224">3</span></span>   |     +   |     +   |         |         | <span data-ttu-id="eba13-225">错误（多个映射）</span><span class="sxs-lookup"><span data-stu-id="eba13-225">Error (multiple mappings)</span></span> | <span data-ttu-id="eba13-226">错误（多个映射）</span><span class="sxs-lookup"><span data-stu-id="eba13-226">Error (multiple mappings)</span></span>  |
|     <span data-ttu-id="eba13-227">4</span><span class="sxs-lookup"><span data-stu-id="eba13-227">4</span></span>   |     +   |         |    +    |         | <span data-ttu-id="eba13-228">MM1A</span><span class="sxs-lookup"><span data-stu-id="eba13-228">MM1A</span></span>                      | <span data-ttu-id="eba13-229">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-229">MM1</span></span>                        |
|     <span data-ttu-id="eba13-230">5</span><span class="sxs-lookup"><span data-stu-id="eba13-230">5</span></span>   |     +   |         |    +    |    +    | <span data-ttu-id="eba13-231">错误（多个映射）</span><span class="sxs-lookup"><span data-stu-id="eba13-231">Error (multiple mappings)</span></span> | <span data-ttu-id="eba13-232">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-232">MM1</span></span>                        |
|     <span data-ttu-id="eba13-233">6</span><span class="sxs-lookup"><span data-stu-id="eba13-233">6</span></span>   |     +   | <span data-ttu-id="eba13-234">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-234">default</span></span> |    +    |    +    | <span data-ttu-id="eba13-235">MM2</span><span class="sxs-lookup"><span data-stu-id="eba13-235">MM2</span></span>                       | <span data-ttu-id="eba13-236">MM2</span><span class="sxs-lookup"><span data-stu-id="eba13-236">MM2</span></span>                        |
|     <span data-ttu-id="eba13-237">7</span><span class="sxs-lookup"><span data-stu-id="eba13-237">7</span></span>   |     +   |         | <span data-ttu-id="eba13-238">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-238">default</span></span> |         | <span data-ttu-id="eba13-239">MM1A</span><span class="sxs-lookup"><span data-stu-id="eba13-239">MM1A</span></span>                      | <span data-ttu-id="eba13-240">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-240">MM1</span></span>                        |
|     <span data-ttu-id="eba13-241">8</span><span class="sxs-lookup"><span data-stu-id="eba13-241">8</span></span>   |     +   |         | <span data-ttu-id="eba13-242">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-242">default</span></span> |    +    | <span data-ttu-id="eba13-243">MM1A</span><span class="sxs-lookup"><span data-stu-id="eba13-243">MM1A</span></span>                      | <span data-ttu-id="eba13-244">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-244">MM1</span></span>                        |
|     <span data-ttu-id="eba13-245">9</span><span class="sxs-lookup"><span data-stu-id="eba13-245">9</span></span>   |     +   |         | <span data-ttu-id="eba13-246">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-246">default</span></span> | <span data-ttu-id="eba13-247">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-247">default</span></span> | <span data-ttu-id="eba13-248">错误（多个映射）</span><span class="sxs-lookup"><span data-stu-id="eba13-248">Error (multiple mappings)</span></span> | <span data-ttu-id="eba13-249">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-249">MM1</span></span>                        |
|    <span data-ttu-id="eba13-250">10</span><span class="sxs-lookup"><span data-stu-id="eba13-250">10</span></span>   | <span data-ttu-id="eba13-251">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-251">default</span></span> |         |         |         | <span data-ttu-id="eba13-252">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-252">MM1</span></span>                       | <span data-ttu-id="eba13-253">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-253">MM1</span></span>                        |
|    <span data-ttu-id="eba13-254">11</span><span class="sxs-lookup"><span data-stu-id="eba13-254">11</span></span>   | <span data-ttu-id="eba13-255">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-255">default</span></span> |    +    |         |         | <span data-ttu-id="eba13-256">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-256">MM1</span></span>                       | <span data-ttu-id="eba13-257">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-257">MM1</span></span>                        |
|    <span data-ttu-id="eba13-258">12</span><span class="sxs-lookup"><span data-stu-id="eba13-258">12</span></span>   | <span data-ttu-id="eba13-259">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-259">default</span></span> |         |    +    |         | <span data-ttu-id="eba13-260">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-260">MM1</span></span>                       | <span data-ttu-id="eba13-261">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-261">MM1</span></span>                        |
|    <span data-ttu-id="eba13-262">13</span><span class="sxs-lookup"><span data-stu-id="eba13-262">13</span></span>   | <span data-ttu-id="eba13-263">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-263">default</span></span> | <span data-ttu-id="eba13-264">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-264">default</span></span> |         |         | <span data-ttu-id="eba13-265">错误（多个映射）</span><span class="sxs-lookup"><span data-stu-id="eba13-265">Error (multiple mappings)</span></span> | <span data-ttu-id="eba13-266">错误（多个映射）</span><span class="sxs-lookup"><span data-stu-id="eba13-266">Error (multiple mappings)</span></span>  |
|    <span data-ttu-id="eba13-267">14</span><span class="sxs-lookup"><span data-stu-id="eba13-267">14</span></span>   | <span data-ttu-id="eba13-268">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-268">default</span></span> |         | <span data-ttu-id="eba13-269">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-269">default</span></span> |         | <span data-ttu-id="eba13-270">MM1A</span><span class="sxs-lookup"><span data-stu-id="eba13-270">MM1A</span></span>                      | <span data-ttu-id="eba13-271">MM1</span><span class="sxs-lookup"><span data-stu-id="eba13-271">MM1</span></span>                        |
|    <span data-ttu-id="eba13-272">15</span><span class="sxs-lookup"><span data-stu-id="eba13-272">15</span></span>   | <span data-ttu-id="eba13-273">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-273">default</span></span> |         | <span data-ttu-id="eba13-274">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-274">default</span></span> | <span data-ttu-id="eba13-275">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-275">default</span></span> | <span data-ttu-id="eba13-276">MM1A</span><span class="sxs-lookup"><span data-stu-id="eba13-276">MM1A</span></span>                      | <span data-ttu-id="eba13-277">MM2A</span><span class="sxs-lookup"><span data-stu-id="eba13-277">MM2A</span></span>                       |
|    <span data-ttu-id="eba13-278">16</span><span class="sxs-lookup"><span data-stu-id="eba13-278">16</span></span>   |         |         |    +    |    +    | <span data-ttu-id="eba13-279">MM1A</span><span class="sxs-lookup"><span data-stu-id="eba13-279">MM1A</span></span>                      | <span data-ttu-id="eba13-280">MM2A</span><span class="sxs-lookup"><span data-stu-id="eba13-280">MM2A</span></span>                       |
|    <span data-ttu-id="eba13-281">17</span><span class="sxs-lookup"><span data-stu-id="eba13-281">17</span></span>   |         |         | <span data-ttu-id="eba13-282">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-282">default</span></span> | <span data-ttu-id="eba13-283">默认</span><span class="sxs-lookup"><span data-stu-id="eba13-283">default</span></span> | <span data-ttu-id="eba13-284">MM1A</span><span class="sxs-lookup"><span data-stu-id="eba13-284">MM1A</span></span>                      | <span data-ttu-id="eba13-285">MM2A</span><span class="sxs-lookup"><span data-stu-id="eba13-285">MM2A</span></span>                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a><span data-ttu-id="eba13-286">了解在执行 ER 格式时使用了什么映射</span><span class="sxs-lookup"><span data-stu-id="eba13-286">Learn what mapping was used in the execution of an ER format</span></span>

### <a name="configure-er-user-parameters"></a><span data-ttu-id="eba13-287">配置 ER 用户参数</span><span class="sxs-lookup"><span data-stu-id="eba13-287">Configure ER user parameters</span></span>

1.  <span data-ttu-id="eba13-288">在 **配置** 页操作窗格中的 **配置** 选项卡上，选择 **用户参数**。</span><span class="sxs-lookup"><span data-stu-id="eba13-288">On the **Configurations** page, on the Action Pane, on the **CONFIGURATIONS** tab, select **User parameters**.</span></span>
2.  <span data-ttu-id="eba13-289">将 **以调试模式运行** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="eba13-289">Set the **Run in debug mode** option to **Yes**.</span></span>
4.  <span data-ttu-id="eba13-290">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-290">Select **Ok**.</span></span>

### <a name="run-the-configured-format"></a><span data-ttu-id="eba13-291">运行配置的格式</span><span class="sxs-lookup"><span data-stu-id="eba13-291">Run the configured format</span></span>

1.  <span data-ttu-id="eba13-292">在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。</span><span class="sxs-lookup"><span data-stu-id="eba13-292">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="eba13-293">在 **版本** 快速选项卡上，选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="eba13-293">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="eba13-294">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-294">Select **Ok**.</span></span>

### <a name="review-the-er-debug-log"></a><span data-ttu-id="eba13-295">查看 ER 调试日志</span><span class="sxs-lookup"><span data-stu-id="eba13-295">Review the ER debug log</span></span>

1.  <span data-ttu-id="eba13-296">在导航窗格中，转到 **模块 \> 组织管理 \> 电子报告 \> 配置调试日志**。</span><span class="sxs-lookup"><span data-stu-id="eba13-296">In the navigation pane, go to **Modules \> Organization administration \> Electronic reporting \> Configuration debug log**.</span></span>
2.  <span data-ttu-id="eba13-297">选择 **重新加载此页面** 按钮。</span><span class="sxs-lookup"><span data-stu-id="eba13-297">Select the **Reload this page** button.</span></span>

![ER 运行日志页](./media/RCS-Context-specific-mapping-DebugLog.PNG)

<span data-ttu-id="eba13-299">请注意，已为执行的 ER 格式将新记录添加到 ER 调试日志中。</span><span class="sxs-lookup"><span data-stu-id="eba13-299">Notice that a new record has been added to the ER debug log for the executed ER format.</span></span> <span data-ttu-id="eba13-300">由于此记录的 **级别** 字段设置为 **信息**，因此此记录是信息性的。</span><span class="sxs-lookup"><span data-stu-id="eba13-300">Because the **Level** field of this record is set to **Info**, the record is informational.</span></span> <span data-ttu-id="eba13-301">由于格式组件字段设置为 **映射配置**，因此记录会通知您有关执行 **用于了解映射的格式** ER 格式（已在 **配置名称** 字段中选择）期间使用的模型映射的信息。</span><span class="sxs-lookup"><span data-stu-id="eba13-301">Because the Format component field is set to **Mapping configuration**, the record informs you about a model mapping that was used during execution of the **Format to learn mappings** ER format (selected in the **Configuration name** field).</span></span> <span data-ttu-id="eba13-302">**生成的文本** 字段的内容会通知您，位于 **映射(FR)** 配置中的 **映射(FR)** 映射组件已用于运行此报表。</span><span class="sxs-lookup"><span data-stu-id="eba13-302">The content of the **Generated text** field informs you that the **Mapping (FR)** mapping component that resides in the **Mapping (FR)** configuration has been used to run this report.</span></span>

## <a name="appendix-1"></a><a name="appendix1"></a> <span data-ttu-id="eba13-303">附录 1</span><span class="sxs-lookup"><span data-stu-id="eba13-303">Appendix 1</span></span>

### <a name="configure-a-sample-data-model"></a><span data-ttu-id="eba13-304">配置示例数据模型</span><span class="sxs-lookup"><span data-stu-id="eba13-304">Configure a sample data model</span></span>

<span data-ttu-id="eba13-305">登录您的 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="eba13-305">Sign in to your RCS instance.</span></span>

<span data-ttu-id="eba13-306">在此示例中，将为示例公司 Litware 公司创建一个配置。要完成这些步骤，您必须首先在 RCS 中完成[创建一个配置提供程序，并标记其为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="eba13-306">In this example, you will create a configuration for sample company, Litware, Inc. To complete these steps, you must first complete, in RCS, the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

#### <a name="create-an-er-data-model-configuration"></a><span data-ttu-id="eba13-307">创建 ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="eba13-307">Create an ER data model configuration</span></span>

1.  <span data-ttu-id="eba13-308">在默认仪表板中，选择 **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="eba13-308">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="eba13-309">选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="eba13-309">Select the **Reporting configurations** tile.</span></span>
3.  <span data-ttu-id="eba13-310">在 **配置** 页上，选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-310">On the **Configurations** page, select **Create configuration**.</span></span>
4.  <span data-ttu-id="eba13-311">在下拉对话框的 **名称** 字段中，输入 **用于了解映射的模型**。</span><span class="sxs-lookup"><span data-stu-id="eba13-311">In the drop-down dialog box, in the **Name** field, enter **Model to learn mappings**.</span></span>
5.  <span data-ttu-id="eba13-312">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-312">Select **Create configuration**.</span></span>
6.  <span data-ttu-id="eba13-313">选择 **配置组件** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="eba13-313">Select the **Configuration components** FastTab.</span></span>

<span data-ttu-id="eba13-314">请注意，此 ER 配置的草稿版本 1 已可以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="eba13-314">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="eba13-315">此版本包含数据模型组件。</span><span class="sxs-lookup"><span data-stu-id="eba13-315">This version contains the data model component.</span></span>

#### <a name="design-a-sample-data-model"></a><span data-ttu-id="eba13-316">设计示例数据模型</span><span class="sxs-lookup"><span data-stu-id="eba13-316">Design a sample data model</span></span>

1.  <span data-ttu-id="eba13-317">在 **配置页** 上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-317">On the **Configurations page**, select **Designer**.</span></span>
2.  <span data-ttu-id="eba13-318">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="eba13-318">Select **New**.</span></span>
3.  <span data-ttu-id="eba13-319">在下拉对话框的 **名称** 字段中，输入 **入口点 1**。</span><span class="sxs-lookup"><span data-stu-id="eba13-319">In the drop-down dialog box, in the **Name** field, enter **Entry point 1**.</span></span>
4.  <span data-ttu-id="eba13-320">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="eba13-320">Select **Add**.</span></span>
5.  <span data-ttu-id="eba13-321">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="eba13-321">Select **New**.</span></span>
6.  <span data-ttu-id="eba13-322">在下拉对话框的 **名称** 字段中，输入 **功能描述**。</span><span class="sxs-lookup"><span data-stu-id="eba13-322">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
7.  <span data-ttu-id="eba13-323">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="eba13-323">Select **Add**.</span></span>
8.  <span data-ttu-id="eba13-324">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="eba13-324">Select **New**.</span></span>
9.  <span data-ttu-id="eba13-325">在下拉对话框的 **新建节点** 字段组中，选择 **模型根**。</span><span class="sxs-lookup"><span data-stu-id="eba13-325">In the drop-down dialog box, in the **New node** field group, select **Model root**.</span></span>
10. <span data-ttu-id="eba13-326">在 **名称** 字段中，输入 **入口点 2**。</span><span class="sxs-lookup"><span data-stu-id="eba13-326">In the **Name** field, enter **Entry point 2**.</span></span>
11. <span data-ttu-id="eba13-327">选择 **入口点 2**。</span><span class="sxs-lookup"><span data-stu-id="eba13-327">Select **Entry point 2**.</span></span>
12. <span data-ttu-id="eba13-328">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="eba13-328">Select **Add**.</span></span>
13. <span data-ttu-id="eba13-329">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="eba13-329">Select **New**.</span></span>
14. <span data-ttu-id="eba13-330">在下拉对话框的 **名称** 字段中，输入 **功能描述**。</span><span class="sxs-lookup"><span data-stu-id="eba13-330">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
15. <span data-ttu-id="eba13-331">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="eba13-331">Select **Add**.</span></span>

    ![ER 数据模型设计器页面](./media/RCS-Context-specific-mapping-Model.PNG)

16. <span data-ttu-id="eba13-333">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-333">Select **Save**.</span></span>
17. <span data-ttu-id="eba13-334">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-334">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-configuration"></a><span data-ttu-id="eba13-335">完成修改后的模型配置版本</span><span class="sxs-lookup"><span data-stu-id="eba13-335">Complete the modified version of the model configuration</span></span>

1.  <span data-ttu-id="eba13-336">在 **配置** 页的 **版本** 快速选项卡上，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="eba13-336">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="eba13-337">将设计的模型配置的状态从 **草稿** 更改为 **已完成**，以便可以将其用于设计所需的模型映射和格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-337">Change the status of designed model configuration from **Draft** to **Completed**, so that it can be used to design the required model mappings and formats.</span></span>

2.  <span data-ttu-id="eba13-338">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="eba13-338">Select **Complete**.</span></span>
3.  <span data-ttu-id="eba13-339">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-339">Select **OK**.</span></span>

<span data-ttu-id="eba13-340">请注意已创建的配置保存为已完成版本 1。</span><span class="sxs-lookup"><span data-stu-id="eba13-340">Notice that the configuration that you created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-model-mapping"></a><span data-ttu-id="eba13-341">配置示例模型映射</span><span class="sxs-lookup"><span data-stu-id="eba13-341">Configure a sample model mapping</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="eba13-342">创建 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="eba13-342">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="eba13-343">在 **配置** 页上，选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-343">On the **Configurations** page, select **Create configuration**.</span></span>
2.  <span data-ttu-id="eba13-344">在下拉对话框中的 **新建** 字段组中，选择 **用于了解映射的基于数据模型的模型映射**。</span><span class="sxs-lookup"><span data-stu-id="eba13-344">In the drop-down dialog box, in the **New** field group, select **Model mapping based on data model Model to learn mappings**.</span></span>
3.  <span data-ttu-id="eba13-345">在 **名称** 字段中，输入 **映射(一般)**。</span><span class="sxs-lookup"><span data-stu-id="eba13-345">In the **Name** field, enter **Mapping (General)**.</span></span>
4.  <span data-ttu-id="eba13-346">在 **数据模型定义** 字段中，选择 **入口点 1**。</span><span class="sxs-lookup"><span data-stu-id="eba13-346">In the **Data model definition** field, select **Entry point 1**.</span></span>
5.  <span data-ttu-id="eba13-347">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-347">Select **Create configuration**.</span></span>

<span data-ttu-id="eba13-348">请注意，此 ER 配置的草稿版本 1 已可以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="eba13-348">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="eba13-349">此版本包含模型映射组件。</span><span class="sxs-lookup"><span data-stu-id="eba13-349">This version contains the model mapping component.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="eba13-350">设计示例模型映射</span><span class="sxs-lookup"><span data-stu-id="eba13-350">Design a sample model mapping</span></span>

1.  <span data-ttu-id="eba13-351">在 **配置** 页上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-351">On the **Configurations** page, select **Designer**.</span></span>

    <span data-ttu-id="eba13-352">请注意，对于 **入口点 1** 定义，**目标模型** 方向类型的模型映射已自动添加到此组件。</span><span class="sxs-lookup"><span data-stu-id="eba13-352">Notice that the model mapping of the **To model** direction type has been automatically added to this component for the **Entry point 1** definition.</span></span>
    
2.  <span data-ttu-id="eba13-353">选择 **设计器** 开始编辑添加的模型映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-353">Select **Designer** to start editing the added model mapping.</span></span>
3.  <span data-ttu-id="eba13-354">在 **数据模型** 部分，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="eba13-354">In the **Data model** section, select **Edit**.</span></span>
4.  <span data-ttu-id="eba13-355">在 **公式** 字段中，输入 **通用功能 1**。</span><span class="sxs-lookup"><span data-stu-id="eba13-355">In the **Formula** field, enter **"Generic functionality 1"**.</span></span>
5.  <span data-ttu-id="eba13-356">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-356">Select **Save**.</span></span>
6.  <span data-ttu-id="eba13-357">关闭 **公式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="eba13-357">Close the **Formula designer** page.</span></span>

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  <span data-ttu-id="eba13-359">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-359">Select **Save**.</span></span>
8.  <span data-ttu-id="eba13-360">关闭 **模型映射设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="eba13-360">Close the **Model mapping designer** page.</span></span>
9.  <span data-ttu-id="eba13-361">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="eba13-361">Select **New**.</span></span>
10. <span data-ttu-id="eba13-362">在 **定义** 字段中，选择 **入口点 2**。</span><span class="sxs-lookup"><span data-stu-id="eba13-362">In the **Definition** field, select **Entry point 2**.</span></span>
11. <span data-ttu-id="eba13-363">在 **名称** 字段中，输入 **映射(一般) 2**。</span><span class="sxs-lookup"><span data-stu-id="eba13-363">In the **Name** field, enter **Mapping (General) 2**.</span></span>
12. <span data-ttu-id="eba13-364">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-364">Select **Designer**.</span></span>
13. <span data-ttu-id="eba13-365">在 **数据模型** 部分，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="eba13-365">In the **Data model** section, select **Edit**.</span></span>
14. <span data-ttu-id="eba13-366">在 **公式** 字段中，输入 **通用功能 2**。</span><span class="sxs-lookup"><span data-stu-id="eba13-366">In the **Formula** field, enter **"Generic functionality 2"**.</span></span>
15. <span data-ttu-id="eba13-367">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-367">Select **Save**.</span></span>
16. <span data-ttu-id="eba13-368">关闭 **公式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="eba13-368">Close the **Formula designer** page.</span></span>

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. <span data-ttu-id="eba13-370">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-370">Select **Save**.</span></span>
18. <span data-ttu-id="eba13-371">关闭 **模型映射设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="eba13-371">Close the **Model mapping designer** page.</span></span>

    ![ER 模型映射页](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. <span data-ttu-id="eba13-373">关闭 **模型映射** 页。</span><span class="sxs-lookup"><span data-stu-id="eba13-373">Close the **Model mappings** page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="eba13-374">完成修改后的模型映射配置版本</span><span class="sxs-lookup"><span data-stu-id="eba13-374">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="eba13-375">在 **配置页** 的 **版本** 快速选项卡上，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="eba13-375">On the **Configurations page**, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="eba13-376">将设计的模型映射配置的状态从 **草稿** 更改为 **已完成**，以便可以将其用于 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-376">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="eba13-377">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="eba13-377">Select **Complete**.</span></span>
3.  <span data-ttu-id="eba13-378">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-378">Select **OK**.</span></span>

<span data-ttu-id="eba13-379">请注意已创建的配置保存为已完成版本 1。</span><span class="sxs-lookup"><span data-stu-id="eba13-379">Notice that the configuration that is created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-format"></a><span data-ttu-id="eba13-380">配置示例格式</span><span class="sxs-lookup"><span data-stu-id="eba13-380">Configure a sample format</span></span>

#### <a name="create-an-er-format-configuration"></a><span data-ttu-id="eba13-381">创建 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="eba13-381">Create an ER format configuration</span></span>

1.  <span data-ttu-id="eba13-382">在 **配置** 页上的配置树中，选择 **用于了解映射的模型**。</span><span class="sxs-lookup"><span data-stu-id="eba13-382">On the **Configurations** page, in the configurations tree, select **Model to learn mappings**.</span></span>
2.  <span data-ttu-id="eba13-383">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-383">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="eba13-384">在下拉对话框中的 **新建** 字段组中，选择 **用于了解映射的基于数据模型的格式**。</span><span class="sxs-lookup"><span data-stu-id="eba13-384">In the drop-down dialog box, in the **New** field group, select **Format based on data model Model to learn mappings**.</span></span>
4.  <span data-ttu-id="eba13-385">在 **名称** 字段中，输入 **用于了解映射的格式**。</span><span class="sxs-lookup"><span data-stu-id="eba13-385">In the **Name** field, enter **Format to learn mappings**.</span></span>
5.  <span data-ttu-id="eba13-386">在 **数据模型定义** 字段中，选择 **入口点 1**。</span><span class="sxs-lookup"><span data-stu-id="eba13-386">In the **Data model definition** field, select **Entry point 1**.</span></span>
6.  <span data-ttu-id="eba13-387">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-387">Select **Create configuration**.</span></span>

<span data-ttu-id="eba13-388">请注意，此 ER 配置的草稿版本 1 已可以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="eba13-388">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="eba13-389">此版本包含格式组件。</span><span class="sxs-lookup"><span data-stu-id="eba13-389">This version contains the format component.</span></span>

#### <a name="design-a-sample-format"></a><span data-ttu-id="eba13-390">设计示例格式</span><span class="sxs-lookup"><span data-stu-id="eba13-390">Design a sample format</span></span>

1.  <span data-ttu-id="eba13-391">在 **配置** 页上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-391">On the **Configurations** page, select **Designer**.</span></span>
2.  <span data-ttu-id="eba13-392">选择 **添加根**。</span><span class="sxs-lookup"><span data-stu-id="eba13-392">Select **Add root**.</span></span>
3.  <span data-ttu-id="eba13-393">在 **文本** 组中，选择 **字符串** 项。</span><span class="sxs-lookup"><span data-stu-id="eba13-393">In the **Text** group, select the **String** item.</span></span>
4.  <span data-ttu-id="eba13-394">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-394">Select **OK**.</span></span>

#### <a name="bind-format-elements-to-a-data-source"></a><span data-ttu-id="eba13-395">将格式元素绑定到数据源</span><span class="sxs-lookup"><span data-stu-id="eba13-395">Bind format elements to a data source</span></span>

1.  <span data-ttu-id="eba13-396">在 **格式设计器** 页上的 **映射** 选项卡上，展开模型数据源。</span><span class="sxs-lookup"><span data-stu-id="eba13-396">On the **Format designer** page, on the **Mapping** tab, expand the model data source.</span></span>
2.  <span data-ttu-id="eba13-397">选择 **功能描述** 字段。</span><span class="sxs-lookup"><span data-stu-id="eba13-397">Select the **Functionality description** field.</span></span>
3.  <span data-ttu-id="eba13-398">选择 **绑定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-398">Select **Bind**.</span></span>

    ![ER 格式设计器页面](./media/RCS-Context-specific-mapping-Format.PNG)

4.  <span data-ttu-id="eba13-400">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-400">Select **Save**.</span></span>
5.  <span data-ttu-id="eba13-401">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-401">Close the page.</span></span>

## <a name="appendix-2"></a><a name="appendix2"></a> <span data-ttu-id="eba13-402">附录 2</span><span class="sxs-lookup"><span data-stu-id="eba13-402">Appendix 2</span></span>

### <a name="configure-a-sample-model-mapping-for-general-customization"></a><span data-ttu-id="eba13-403">配置示例模型映射以进行一般自定义</span><span class="sxs-lookup"><span data-stu-id="eba13-403">Configure a sample model mapping for general customization</span></span>

<span data-ttu-id="eba13-404">您可能想要自定义配置提供商（合作伙伴）提供给您的模型映射，然后将自定义版本用作 ER 格式的数据源。</span><span class="sxs-lookup"><span data-stu-id="eba13-404">You might want to customize a model mapping that a configuration provider (partner) provided to you, and then use the customized version as a data source for your ER formats.</span></span> <span data-ttu-id="eba13-405">在这种情况下，您必须创建自定义 ER 模型映射配置，以在现有模型映射中进行所需的更改。</span><span class="sxs-lookup"><span data-stu-id="eba13-405">In this case, you must create a custom ER model mapping configuration to make the required changes in existing model mappings.</span></span> <span data-ttu-id="eba13-406">此附录中的过程以 **映射(一般)** 模型映射为例。</span><span class="sxs-lookup"><span data-stu-id="eba13-406">The procedures in this appendix use the **Mapping (General)** model mapping as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="eba13-407">创建 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="eba13-407">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="eba13-408">在 **配置** 页上的配置树中，选择 **映射(一般)**。</span><span class="sxs-lookup"><span data-stu-id="eba13-408">On the **Configurations** page, in the configurations tree, select **Mapping (General)**.</span></span>
2.  <span data-ttu-id="eba13-409">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-409">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="eba13-410">在下拉对话框的 **新建** 字段组中，选择 **从以下名称派生: 映射(一般)，Litware, Inc.**。</span><span class="sxs-lookup"><span data-stu-id="eba13-410">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General), Litware, Inc.**.</span></span>
4.  <span data-ttu-id="eba13-411">在 **名称** 字段中，输入 **映射(一般)自定义**。</span><span class="sxs-lookup"><span data-stu-id="eba13-411">In the **Name** field, enter **Mapping (General) custom**.</span></span>
5.  <span data-ttu-id="eba13-412">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-412">Select **Create configuration**.</span></span>

<span data-ttu-id="eba13-413">请注意，此 ER 配置的草稿版本 1 已可以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="eba13-413">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="eba13-414">设计示例模型映射</span><span class="sxs-lookup"><span data-stu-id="eba13-414">Design a sample model mapping</span></span>

1.  <span data-ttu-id="eba13-415">在 **配置** 页上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-415">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="eba13-416">请注意，基本配置的模型映射已自动复制到此配置。</span><span class="sxs-lookup"><span data-stu-id="eba13-416">Notice that the model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="eba13-417">选择 **映射(一般)复制** 映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-417">Select the **Mapping (General) Copy** mapping.</span></span>
3.  <span data-ttu-id="eba13-418">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-418">Select **Designer**.</span></span>
4.  <span data-ttu-id="eba13-419">在 **数据模型** 部分，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="eba13-419">In the **Data model** section, select **Edit**.</span></span>
5.  <span data-ttu-id="eba13-420">在 **公式** 字段中，输入 **通用功能 1 自定义**。</span><span class="sxs-lookup"><span data-stu-id="eba13-420">In the **Formula** field, enter **"Generic functionality 1 custom"**.</span></span>
6.  <span data-ttu-id="eba13-421">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-421">Select **Save**.</span></span>
7.  <span data-ttu-id="eba13-422">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-422">Close the page.</span></span>

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  <span data-ttu-id="eba13-424">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-424">Select **Save**.</span></span>
9.  <span data-ttu-id="eba13-425">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-425">Close the page.</span></span>
10. <span data-ttu-id="eba13-426">选择 **映射(一般) 2 复制** 映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-426">Select the **Mapping (General) 2 Copy** mapping.</span></span>
11. <span data-ttu-id="eba13-427">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-427">Select **Designer**.</span></span>
12. <span data-ttu-id="eba13-428">在 **数据模型** 部分，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="eba13-428">In the **Data model** section, select **Edit**.</span></span>
13. <span data-ttu-id="eba13-429">在 **公式** 字段中，输入 **通用功能 2 自定义**。</span><span class="sxs-lookup"><span data-stu-id="eba13-429">In the **Formula** field, enter **"Generic functionality 2 custom"**.</span></span>
14. <span data-ttu-id="eba13-430">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-430">Select **Save**.</span></span>
15. <span data-ttu-id="eba13-431">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-431">Close the page.</span></span>

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. <span data-ttu-id="eba13-433">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-433">Select **Save**.</span></span>
17. <span data-ttu-id="eba13-434">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-434">Close the page.</span></span>

    ![ER 模型映射页](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. <span data-ttu-id="eba13-436">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-436">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="eba13-437">完成修改后的模型映射配置版本</span><span class="sxs-lookup"><span data-stu-id="eba13-437">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="eba13-438">在 **配置** 页的 **版本** 快速选项卡上，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="eba13-438">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="eba13-439">将设计的模型映射配置的状态从 **草稿** 更改为 **已完成**，以便可以将其用于 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-439">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="eba13-440">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="eba13-440">Select **Complete**.</span></span>
3.  <span data-ttu-id="eba13-441">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-441">Select **OK**.</span></span>

<span data-ttu-id="eba13-442">请注意已创建的配置保存为已完成版本 1。</span><span class="sxs-lookup"><span data-stu-id="eba13-442">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="appendix-3"></a><a name="appendix3"></a> <span data-ttu-id="eba13-443">附录 3</span><span class="sxs-lookup"><span data-stu-id="eba13-443">Appendix 3</span></span>

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a><span data-ttu-id="eba13-444">配置示例模型映射以进行国家/地区特定自定义</span><span class="sxs-lookup"><span data-stu-id="eba13-444">Configure a sample model mapping for country/region-specific customization</span></span>

<span data-ttu-id="eba13-445">对于某些 ER 格式，可能需要针对国家/地区进行数据准备。</span><span class="sxs-lookup"><span data-stu-id="eba13-445">For some ER formats, there might be country/region-specific requirements for data preparation.</span></span> <span data-ttu-id="eba13-446">在这种情况下，您可以管理单独的 ER 模型映射配置，并将这些特定于国家/地区要求的实现与常规实现隔离开来。</span><span class="sxs-lookup"><span data-stu-id="eba13-446">In this case, you can manage a separate ER model mapping configuration and isolate the implementation of these country/region-specific requirements from the general implementation.</span></span> <span data-ttu-id="eba13-447">此附录中的过程以 **用于了解映射的格式** ER 格式和特定于法国的要求为例。</span><span class="sxs-lookup"><span data-stu-id="eba13-447">The procedures in this appendix use the **Format to learn mappings** ER format and French-specific requirements as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="eba13-448">创建 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="eba13-448">Create an ER model mapping configuration</span></span>

<span data-ttu-id="eba13-449">首先，创建新的 ER 模型映射配置，以实现国家/地区的特定要求。</span><span class="sxs-lookup"><span data-stu-id="eba13-449">First, create a new ER model mapping configuration to implement the country/region-specific requirements.</span></span> <span data-ttu-id="eba13-450">使用您的自定义 ER 模型映射配置作为基础。</span><span class="sxs-lookup"><span data-stu-id="eba13-450">Use your custom ER model mapping configuration as a base.</span></span>

1.  <span data-ttu-id="eba13-451">在 **配置** 页上的配置树中，选择 **映射(一般)自定义**。</span><span class="sxs-lookup"><span data-stu-id="eba13-451">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="eba13-452">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-452">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="eba13-453">在下拉对话框的 **新建** 字段组中，选择 **从以下名称派生: 映射(一般)自定义，Litware, Inc.**。</span><span class="sxs-lookup"><span data-stu-id="eba13-453">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General) custom, Litware, Inc**.</span></span>
4.  <span data-ttu-id="eba13-454">在 **名称** 字段中，输入 **映射(FR)**。</span><span class="sxs-lookup"><span data-stu-id="eba13-454">In the **Name** field, enter **Mapping (FR)**.</span></span>
5.  <span data-ttu-id="eba13-455">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="eba13-455">Select **Create configuration**.</span></span>

<span data-ttu-id="eba13-456">请注意，此 ER 配置的草稿版本 1 已可以进行编辑。</span><span class="sxs-lookup"><span data-stu-id="eba13-456">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="eba13-457">设计示例模型映射</span><span class="sxs-lookup"><span data-stu-id="eba13-457">Design a sample model mapping</span></span>

1.  <span data-ttu-id="eba13-458">在 **配置** 页上，选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-458">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="eba13-459">请注意，基本配置的模型映射已自动复制到此配置。</span><span class="sxs-lookup"><span data-stu-id="eba13-459">Notice that model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="eba13-460">选择 **映射(一般)复制** 映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-460">Select the **Mapping (General) Copy Copy** mapping.</span></span>
3.  <span data-ttu-id="eba13-461">将其重命名为 **映射(FR)**。</span><span class="sxs-lookup"><span data-stu-id="eba13-461">Rename it **Mapping (FR)**.</span></span>
4.  <span data-ttu-id="eba13-462">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-462">Select **Designer**.</span></span>
5.  <span data-ttu-id="eba13-463">在 **数据模型** 部分，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="eba13-463">In the **Data model** section, select **Edit**.</span></span>
6.  <span data-ttu-id="eba13-464">在 **公式** 字段中，输入 **FR 功能 1**。</span><span class="sxs-lookup"><span data-stu-id="eba13-464">In the **Formula** field, enter **"FR functionality 1"**.</span></span>
7.  <span data-ttu-id="eba13-465">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-465">Select **Save**.</span></span>
8.  <span data-ttu-id="eba13-466">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-466">Close the page.</span></span>

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  <span data-ttu-id="eba13-468">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-468">Select **Save**.</span></span>
10. <span data-ttu-id="eba13-469">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-469">Close the page.</span></span>
11. <span data-ttu-id="eba13-470">选择 **映射(一般) 2 复制** 映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-470">Select the **Mapping (General) 2 Copy Copy** mapping.</span></span>
12. <span data-ttu-id="eba13-471">将其重命名为 **映射(FR) 2**。</span><span class="sxs-lookup"><span data-stu-id="eba13-471">Rename it **Mapping (FR) 2**.</span></span>
13. <span data-ttu-id="eba13-472">选择 **设计器**。</span><span class="sxs-lookup"><span data-stu-id="eba13-472">Select **Designer**.</span></span>
14. <span data-ttu-id="eba13-473">在 **数据模型** 部分，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="eba13-473">In the **Data model** section, select **Edit**.</span></span>
15. <span data-ttu-id="eba13-474">在 **公式** 字段中，输入 **FR 功能 2**。</span><span class="sxs-lookup"><span data-stu-id="eba13-474">In the **Formula** field, enter **"FR functionality 2"**.</span></span>
16. <span data-ttu-id="eba13-475">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-475">Select **Save**.</span></span>
17. <span data-ttu-id="eba13-476">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-476">Close the page.</span></span>

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. <span data-ttu-id="eba13-478">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-478">Select **Save**.</span></span>
19. <span data-ttu-id="eba13-479">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-479">Close the page.</span></span>

    ![ER 模型映射页](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. <span data-ttu-id="eba13-481">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="eba13-481">Close the page.</span></span>

#### <a name="specify-countryregion-context-restrictions-for-use"></a><span data-ttu-id="eba13-482">指定要使用的国家/地区上下文限制</span><span class="sxs-lookup"><span data-stu-id="eba13-482">Specify country/region context restrictions for use</span></span>

1.  <span data-ttu-id="eba13-483">在 **配置** 页的 **ISO 国家/地区代码** 快速选项卡上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="eba13-483">On the **Configurations** page, on the **ISO Country/region codes** FastTab, select **New**.</span></span>
2.  <span data-ttu-id="eba13-484">在 **ISO** 字段中，选择 **FR**。</span><span class="sxs-lookup"><span data-stu-id="eba13-484">In the **ISO** field, select **FR**.</span></span>
3.  <span data-ttu-id="eba13-485">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="eba13-485">Select **Save**.</span></span>

<span data-ttu-id="eba13-486">请注意，您必须登录 Finance 中的特定公司才能运行 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-486">Note that you must sign in to a specific company in Finance to run an ER format.</span></span> <span data-ttu-id="eba13-487">因此，此公司可以被视为同时控制基本 ER 数据模型的 ER 格式执行和正确 ER 模型映射选择的一方。</span><span class="sxs-lookup"><span data-stu-id="eba13-487">Therefore, this company can be considered a party that controls both ER format execution and selection of the correct ER model mapping of the base ER data model.</span></span> <span data-ttu-id="eba13-488">通过添加 **FR** 国家/地区代码，您可以指定仅当在具有法国国家/地区上下文的公司的控制下运行基本数据模型的 ER 格式时，此模型映射才可供选择。</span><span class="sxs-lookup"><span data-stu-id="eba13-488">By adding the **FR** country code, you specify that this model mapping is available for selection by an ER format of the base data model only when that format is run under the control of a company that has French country/region context.</span></span>

<span data-ttu-id="eba13-489">您可以为单个版本的 ER 模型映射配置添加多个国家/地区代码。</span><span class="sxs-lookup"><span data-stu-id="eba13-489">You can add multiple country/region codes for a single version of an ER model mapping configuration.</span></span> <span data-ttu-id="eba13-490">这样，可以将驻留在该模型映射配置中的模型映射用于在具有不同国家/地区上下文的公司控制下运行的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-490">In this way, model mappings that reside in that model mapping configuration can be used for an ER format that is run under the control of companies that have a different country/region context.</span></span>

<span data-ttu-id="eba13-491">请注意，国家/地区代码列表是为 ER 模型映射配置的每个版本指定的，可能因版本而异。</span><span class="sxs-lookup"><span data-stu-id="eba13-491">Note that the list of country/region codes is specified for each version of an ER model mapping configuration and can vary from version to version.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="eba13-492">完成修改后的模型映射配置版本</span><span class="sxs-lookup"><span data-stu-id="eba13-492">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="eba13-493">在 **配置** 页的 **版本** 快速选项卡上，选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="eba13-493">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="eba13-494">将设计的模型映射配置的状态从 **草稿** 更改为 **已完成**，以便可以将其用于 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="eba13-494">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="eba13-495">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="eba13-495">Select **Complete**.</span></span>
3.  <span data-ttu-id="eba13-496">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="eba13-496">Select **OK**.</span></span>

<span data-ttu-id="eba13-497">请注意已创建的配置保存为已完成版本 1。</span><span class="sxs-lookup"><span data-stu-id="eba13-497">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eba13-498">其他资源</span><span class="sxs-lookup"><span data-stu-id="eba13-498">Additional resources</span></span>

[<span data-ttu-id="eba13-499">电子申报 (ER) 概览</span><span class="sxs-lookup"><span data-stu-id="eba13-499">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="eba13-500">管理单独电子报告配置中的电子报告模型映射</span><span class="sxs-lookup"><span data-stu-id="eba13-500">Manage ER model mapping in separate ER configurations</span></span>](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[<span data-ttu-id="eba13-501">应用国家/地区上下文</span><span class="sxs-lookup"><span data-stu-id="eba13-501">Apply country/region context</span></span>](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="eba13-502">常见问题</span><span class="sxs-lookup"><span data-stu-id="eba13-502">Frequently asked questions</span></span>

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a><span data-ttu-id="eba13-503">我在 RCS 中配置了两个共享 ER 模型映射配置，并将其中一个标记为默认模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="eba13-503">I configured two shared ER model mapping configurations in RCS and marked one of them as the default model mapping configuration.</span></span> <span data-ttu-id="eba13-504">我成功运行了为相同的基本 ER 数据模型配置创建的 ER 格式，以测试模型映射。</span><span class="sxs-lookup"><span data-stu-id="eba13-504">I successfully ran an ER format that was created for the same base ER data model configuration, to test model mappings.</span></span> <span data-ttu-id="eba13-505">然后，我将整个 ER 解决方案（ER 数据模型、两个 ER 模型映射配置和 ER 格式配置）导入了 Finance。</span><span class="sxs-lookup"><span data-stu-id="eba13-505">I then imported the whole ER solution (ER data model, two ER model mapping configurations, and ER format configuration) into Finance.</span></span> <span data-ttu-id="eba13-506">当我尝试在 Finance 中运行相同的 ER 格式时，为什么会收到错误消息？</span><span class="sxs-lookup"><span data-stu-id="eba13-506">Why do I receive an error message when I try to run the same ER format in Finance?</span></span>
<span data-ttu-id="eba13-507">默认的模型映射设置是特定于环境的。</span><span class="sxs-lookup"><span data-stu-id="eba13-507">The default model mapping setting is environment-specific.</span></span> <span data-ttu-id="eba13-508">它是在 RCS 中配置的，但没有导出到 Finance。</span><span class="sxs-lookup"><span data-stu-id="eba13-508">It's configured in RCS but isn't exported to Finance.</span></span> <span data-ttu-id="eba13-509">要成功运行此 ER 格式，您还必须在 Finance 中将其中一个 ER 模型映射配置标记为默认模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="eba13-509">To successfully run this ER format, you must mark one of ER model mapping configurations as the default model mapping configuration in Finance too.</span></span>

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a><span data-ttu-id="eba13-510">我将一个模型映射配置为共享模型映射，并完成了其草稿版本。</span><span class="sxs-lookup"><span data-stu-id="eba13-510">I configured one model mapping as a shared model mapping and completed the draft version of it.</span></span> <span data-ttu-id="eba13-511">然后，我为相同的数据模型添加了新的模型映射配置，并将其配置为特定于法国。</span><span class="sxs-lookup"><span data-stu-id="eba13-511">I then added a new model mapping configuration for same data model and configured it as French-specific.</span></span> <span data-ttu-id="eba13-512">为什么即使我运行的 ER 格式使用正确的根定义并且在具有法国国家/地区上下文的公司控制下进行执行，在运行此 ER 格式时仍然选择了共享模型映射？</span><span class="sxs-lookup"><span data-stu-id="eba13-512">Why is the shared model mapping selected when I run an ER format, even though this ER format uses the correct root definition and execution is done under the control of the company that has French country/region context?</span></span>
<span data-ttu-id="eba13-513">请确保未将共享模型映射配置标记为默认模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="eba13-513">Make sure that the shared model mapping configuration isn't marked as the default model mapping configuration.</span></span> <span data-ttu-id="eba13-514">否则，它将在映射选择期间具有更高的优先级。</span><span class="sxs-lookup"><span data-stu-id="eba13-514">Otherwise, it will have higher priority during mapping selection.</span></span> <span data-ttu-id="eba13-515">另外，在 ER 格式执行期间选择映射时，还请确保考虑了特定于法国的模型映射配置。</span><span class="sxs-lookup"><span data-stu-id="eba13-515">Also make sure that the French-specific model mapping configuration is considered when a mapping is selected during ER format execution.</span></span> <span data-ttu-id="eba13-516">仅当满足以下条件中的至少一项时，才可以选择 ER 模型映射配置：</span><span class="sxs-lookup"><span data-stu-id="eba13-516">An ER model mapping configuration is available for selection only if at least one of the following conditions is met:</span></span>
- <span data-ttu-id="eba13-517">至少一个版本的 ER 模型映射配置具有 **已完成** 或 **共享** 状态。</span><span class="sxs-lookup"><span data-stu-id="eba13-517">At least one version of the ER model mapping configuration has either **Completed** or **Shared** status.</span></span> <span data-ttu-id="eba13-518">在这种情况下，具有最高版本号的版本将用于 ER 格式执行。</span><span class="sxs-lookup"><span data-stu-id="eba13-518">In this case, the version that has the highest version number will be used for ER format execution.</span></span>
- <span data-ttu-id="eba13-519">ER 模型映射配置的 **运行草稿** 选项已打开。</span><span class="sxs-lookup"><span data-stu-id="eba13-519">The **Run draft** option for the ER model mapping configuration is turned on.</span></span> <span data-ttu-id="eba13-520">在这种情况下，**草稿** 状态的版本将用于 ER 格式执行。</span><span class="sxs-lookup"><span data-stu-id="eba13-520">In this case, the version that has **Draft** status will be used for ER format execution.</span></span>
> <span data-ttu-id="eba13-521">打开 **运行设置** ER 用户参数后，每个 ER 模型映射配置的 **运行草稿** 选项在 **配置** 页面上将可用。</span><span class="sxs-lookup"><span data-stu-id="eba13-521">The **Run draft** option becomes available on the **Configurations** page for each ER model mapping configuration when the **Run setting** ER user parameter is turned on.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]