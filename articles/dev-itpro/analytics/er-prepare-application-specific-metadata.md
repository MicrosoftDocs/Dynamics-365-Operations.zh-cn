---
title: 为 RCS 和 ER 准备应用程序特定的元数据
description: 本主题介绍如何为 Regulatory Configuration Service (RCS) 和电子申报 (ER) 准备应用程序特定的元数据。
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 289f901501a68319c9d85e993d8dfbfc3838a8eb
ms.sourcegitcommit: d940c7892b6caa6141b3bda8abf1c56e9df4687a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726424"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a><span data-ttu-id="9fdf6-103">为 RCS 准备应用程序特定的元数据</span><span class="sxs-lookup"><span data-stu-id="9fdf6-103">Prepare application-specific metadata for RCS</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9fdf6-104">本主题引导您学习以下任务的示例：</span><span class="sxs-lookup"><span data-stu-id="9fdf6-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="9fdf6-105">准备可在 RCS 中使用的应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="9fdf6-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="9fdf6-106">通过使用 ER 配置访问应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="9fdf6-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="9fdf6-107">通过使用相连应用程序访问应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="9fdf6-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="9fdf6-108">准备可在 RCS 中使用的应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="9fdf6-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="9fdf6-109">以下过程显示具有**系统管理员**或**电子申报开发人员**角色的 Finance and Operations 用户如何创建其中包含 Microsoft Dynamics 365 for Finance and Operations 应用程序的元数据，并用于在 Regulatory Configuration Service (RCS) 中设计 ER 模型映射配置的电子申报 (ER) 配置。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-109">The following procedure shows how a user of Finance and Operations who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the Microsoft Dynamics 365 for Finance and Operations application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="9fdf6-110">此示例中创建的示例 ER 模型映射配置将用于访问外贸交易。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="9fdf6-111">对于此示例，您要使用 RCS 为 Finance and Operations 设计 ER 解决方案，用于生成其中包含来自外贸业务域的信息的电子单据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-111">For this example, you want to use RCS to design an ER solution for Finance and Operations that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="9fdf6-112">若要 ER 数据模型与所需数据源之间的映射，必须可以在 RCS 中访问 Finance and Operations 的应用程序元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata for Finance and Operations in RCS.</span></span> <span data-ttu-id="9fdf6-113">因此，在 ER 解决方案的设计过程中，必须新建一个 ER 元数据配置，其中包含为所选业务域生成 ER 报表当前所需全部元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="9fdf6-114">在此示例中，您将创建示例公司 Litware 公司的配置。这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="9fdf6-115">转到**组织管理 \> 工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="9fdf6-116">确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="9fdf6-117">如果没有看到此配置提供程序，请完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-117">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="9fdf6-118">选择**元数据配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="9fdf6-119">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="9fdf6-120">在下拉对话框的**名称**字段中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="9fdf6-121">对于此示例，请输入**外贸元数据**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="9fdf6-122">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="9fdf6-123">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-123">Select **Designer**.</span></span>
8. <span data-ttu-id="9fdf6-124">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fdf6-125">可为整个应用程序，或所选模型或模块选择所有元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="9fdf6-126">在这两种情况下，请注意，将自动添加以下元数据：记录表、枚举和扩展数据类型 (EDT)。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="9fdf6-127">如果需要更多元数据类型，则必须手动添加。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-127">When additional types of metadata are required, they must be manually added.</span></span>

<span data-ttu-id="9fdf6-128">必须添加一些与外贸交易有关的元数据，并手动选择元数据项。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="9fdf6-129">选择**添加数据源 \> 表记录**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="9fdf6-130">筛选**名称**字段中的**内部统计**值。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="9fdf6-131">选择**内部统计**表记录。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="9fdf6-132">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-132">Select **OK**.</span></span>

<span data-ttu-id="9fdf6-133">必须添加有关“内部统计”记录表的元数据信息。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="9fdf6-134">在树中，选择**表记录‘内部统计’ \> \>关系 \> IntrastatCommodity（表记录 EcoResCategory）**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="9fdf6-135">选择**添加元数据**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fdf6-136">必须手动添加有关所选记录表的所需关系的元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="9fdf6-137">选择**添加数据源**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="9fdf6-138">选择**枚举**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="9fdf6-139">筛选**名称**字段中的 **IntrastatDirection** 值。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="9fdf6-140">选择 **IntrastatDirection** 枚举记录。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="9fdf6-141">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-141">Select **OK**.</span></span>
20. <span data-ttu-id="9fdf6-142">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-142">Select **Save**.</span></span>
21. <span data-ttu-id="9fdf6-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-143">Close the page.</span></span>
22. <span data-ttu-id="9fdf6-144">完成元数据配置的草稿版本。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="9fdf6-145">选择**更改状态 \> 完成**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="9fdf6-146">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-146">Select **OK**.</span></span>
    3. <span data-ttu-id="9fdf6-147">选择已完成版本 1。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="9fdf6-148">将元数据配置的已完成版本作为 XML 文件从应用程序导出：</span><span class="sxs-lookup"><span data-stu-id="9fdf6-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="9fdf6-149">选择**交还 \> 导出为 XML 文件**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="9fdf6-150">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-150">Select **OK**.</span></span>

<span data-ttu-id="9fdf6-151">将把创建的 ER 元数据配置另存为 **Foreign trade metadata.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="9fdf6-152">现在可将其导入到 RCS 中，以便在 Finance and Operations 中将其用作外贸业务域的元数据源。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain in Finance and Operations.</span></span> <span data-ttu-id="9fdf6-153">可根据此信息指定应用程序元数据与 ER 数据模型之间的映射。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="9fdf6-154">通过使用 ER 配置访问应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="9fdf6-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="9fdf6-155">以下过程显示具有**系统管理员**或**电子申报开发人员**角色的 RCS 用户如何使用来自 Finance and Operations 应用程序的元数据设计新的 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the Finance and Operations application.</span></span> <span data-ttu-id="9fdf6-156">可访问应用程序元数据，方法是使用其中包含一组示例元数据的 ER 配置访问外贸交易。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="9fdf6-157">必须首先完成以下过程，才能完成此过程：</span><span class="sxs-lookup"><span data-stu-id="9fdf6-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="9fdf6-158">创建一个配置提供程序，并标记其为当前运行的</span><span class="sxs-lookup"><span data-stu-id="9fdf6-158">Create a configuration provider and mark it as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="9fdf6-159">准备可在 RCS 中使用的应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="9fdf6-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="9fdf6-160">转到**所有工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="9fdf6-161">确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="9fdf6-162">如果没有看到此配置提供程序，请完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-162">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="9fdf6-163">导入包含 Finance and Operations 应用程序的元数据且为了生成外贸业务域所用电子单据而配置的元数据的 ER 元数据配置。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-163">Import the ER metadata configuration that contains metadata for the Finance and Operations application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="9fdf6-164">您已在本主题前面的[准备可在 RCS 中使用的应用程序元数据](#prepare-application-metadata-that-can-be-used-in-rcs)过程中创建了此 ER 元数据配置并将其导出为 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="9fdf6-165">选择**元数据配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="9fdf6-166">选择**交换**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="9fdf6-167">选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="9fdf6-168">浏览到并选择 **Foreign trade metadata.xml** 文件。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="9fdf6-169">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-169">Select **OK**.</span></span>
    6. <span data-ttu-id="9fdf6-170">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-170">Close the page.</span></span>

4. <span data-ttu-id="9fdf6-171">创建数据模型配置：</span><span class="sxs-lookup"><span data-stu-id="9fdf6-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="9fdf6-172">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="9fdf6-173">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="9fdf6-174">在下拉对话框的**名称**字段中，输入**外贸模型**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="9fdf6-175">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="9fdf6-176">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="9fdf6-177">选择**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="9fdf6-178">在**名称**字段中，键入**根**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="9fdf6-179">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="9fdf6-180">选择**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="9fdf6-181">在**名称**字段中，键入**交易**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="9fdf6-182">在**物料类型**字段中，选择**记录列表**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="9fdf6-183">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="9fdf6-184">选择**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="9fdf6-185">在**名称**字段中，键入**商品代码**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="9fdf6-186">在**物料类型**字段中，选择**字符串**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="9fdf6-187">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-187">Select **Add**.</span></span>

    9. <span data-ttu-id="9fdf6-188">选择**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="9fdf6-189">在“名称”字段中，键入**开票金额**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="9fdf6-190">在**物料类型**字段中，选择**实际**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="9fdf6-191">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-191">Select **Add**.</span></span>

    10. <span data-ttu-id="9fdf6-192">选择**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="9fdf6-193">在**名称**字段中，键入**日期**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="9fdf6-194">在**物料类型**字段中，选择**日期**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="9fdf6-195">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="9fdf6-196">选择**添加 \> 根引用**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="9fdf6-197">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-197">Select **OK**.</span></span>
    13. <span data-ttu-id="9fdf6-198">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-198">Select **Save**.</span></span>
    14. <span data-ttu-id="9fdf6-199">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-199">Close the page.</span></span>
    15. <span data-ttu-id="9fdf6-200">选择**更改状态 \> 完成**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="9fdf6-201">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-201">Select **OK**.</span></span>

5. <span data-ttu-id="9fdf6-202">创建模型映射配置：</span><span class="sxs-lookup"><span data-stu-id="9fdf6-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="9fdf6-203">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="9fdf6-204">在下拉对话框的**新建**字段中，输入**基于数据模型‘外贸模型’的模型映射**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="9fdf6-205">在**名称**字段中输入**外贸映射**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="9fdf6-206">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="9fdf6-207">在**先决条件**快速选项卡中，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="9fdf6-208">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-208">Select **New**.</span></span>
    7. <span data-ttu-id="9fdf6-209">在**先决条件组件类型**字段中，选择**配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="9fdf6-210">选择**外贸元数据**配置。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="9fdf6-211">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-211">Select **Save**.</span></span> <span data-ttu-id="9fdf6-212">请注意，将向**外贸元数据**配置版本 1 添加引用。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="9fdf6-213">设计模型映射时，将提供来自此配置的应用程序元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="9fdf6-214">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-214">Close the page.</span></span>
    11. <span data-ttu-id="9fdf6-215">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="9fdf6-216">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="9fdf6-217">在树中，选择 **Dynamics 365 for Operations \> 表记录**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="9fdf6-218">选择**添加根**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="9fdf6-219">在**名称**字段中，输入**内部统计**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="9fdf6-220">选择**内部统计**表记录。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="9fdf6-221">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="9fdf6-222">仅提供了两个表，因为仅向当前使用的元数据集添加了两个表。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="9fdf6-223">选择**绑定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="9fdf6-224">在树中，选择**内部统计 \> AmountMST**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="9fdf6-225">在树中，选择**交易 = 内部统计 \> 开票金额**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="9fdf6-226">选择**绑定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="9fdf6-227">在树中，选择**内部统计 \> TransDate**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="9fdf6-228">在树中，选择**交易 = 内部统计 \> 日期**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="9fdf6-229">选择**绑定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="9fdf6-230">在树中，选择**内部统计 \> \>关系 \> IntrastatCommodity \> 代码**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="9fdf6-231">在树中，选择**交易 = 内部统计 \> 商品代码**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="9fdf6-232">选择**绑定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="9fdf6-233">选择**验证**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="9fdf6-234">完成验证之后，我们已使用来自引用的 ER 元数据配置的应用程序元数据详细信息将数据模型的元素成功绑定到了介绍的数据源项。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="9fdf6-235">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-235">Select **Save**.</span></span>

<span data-ttu-id="9fdf6-236">如果需要，可以扩展 Finance and Operations 中的现有元数据集。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-236">As you require, you can extend the existing set of metadata in Finance and Operations.</span></span> <span data-ttu-id="9fdf6-237">然后就可以从 Finance and Operations 中导出新的 ER 元数据配置已完成版本，导入到 RCS 中，然后更新引用新的所导入元数据配置版本的所配置模型映射配置的必备条件。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-237">You can then export the new completed version of the ER metadata configuration from Finance and Operations, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="9fdf6-238">本地部署的应用程序（即在对 Finance and Operations 使用本地业务数据 \[LBD\] 或本地部署的部署模型）只能使用这种方法获取有关应用程序元数据的信息。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for Finance and Operations).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="9fdf6-239">通过使用相连应用程序访问应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="9fdf6-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="9fdf6-240">以下过程显示具有**系统管理员**或**电子申报开发人员**角色的 RCS 用户如何使用 Finance and Operations 应用程序的元数据设计新的 ER 模型映射。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the Finance and Operations application.</span></span> <span data-ttu-id="9fdf6-241">将使用与 RCS 相连的应用程序联机访问应用程序元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="9fdf6-242">将配置示例 ER 模型映射以访问外贸交易。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="9fdf6-243">为了完成此过程，您必须首先在 RCS 中完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-243">To complete this procedure, you must first complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="9fdf6-244">如果尚未完成本主题中前面的[使用 ER 配置访问应用程序元数据](#access-application-metadata-by-using-an-er-configuration)过程，请转至[Dynamics 365 for Finance and Operations 8.1 电子申报任务指南](https://go.microsoft.com/fwlink/?linkid=2082739)页提前下载以下 ER 配置文件并在本地保存：**Foreign trade metadata.xml**、**Foreign trade model.xml** 和 **Foreign trade mapping.xml**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="9fdf6-245">获取所需的 ER 配置</span><span class="sxs-lookup"><span data-stu-id="9fdf6-245">Get required ER configurations</span></span>

<span data-ttu-id="9fdf6-246">如果已经完成了本主题前面的[使用 ER 配置访问应用程序元数据](#access-application-metadata-by-using-an-er-configuration)过程，则当前 RCS 实例中已经拥有了所有必需的 ER 配置（外贸元数据、模型和映射配置）。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="9fdf6-247">在这种情况下，您可以跳过此过程。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="9fdf6-248">转到**所有工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="9fdf6-249">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="9fdf6-250">加载 **Foreign trade metadata.xml**、**Foreign trade model.xml** 和 **Foreign trade mapping.xml** 配置文件，并对这些文件每一个重复执行下面的一系列步骤：</span><span class="sxs-lookup"><span data-stu-id="9fdf6-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="9fdf6-251">选择**交换**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="9fdf6-252">选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="9fdf6-253">选择**浏览**，然后选择文件。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="9fdf6-254">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-finance-and-operations"></a><span data-ttu-id="9fdf6-255">在 Finance and Operations 中注册连接</span><span class="sxs-lookup"><span data-stu-id="9fdf6-255">Register the connection with Finance and Operations</span></span>

1. <span data-ttu-id="9fdf6-256">转到**所有工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="9fdf6-257">选择**相连应用程序**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="9fdf6-258">确保配置的应用程序基于 Microsoft Azure，并且通常可供 RCS 用户访问。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="9fdf6-259">当前 RCS 用户必须可访问所配置应用程序，已注册为此应用程序的用户，并且其角色有权访问此应用程序的元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="9fdf6-260">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-260">Select **New**.</span></span>
5. <span data-ttu-id="9fdf6-261">在**名称**字段，输入 **MyConnectedApp** 作为相连应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="9fdf6-262">在**应用程序**字段中，指定应用程序的 URL。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="9fdf6-263">在**租户**字段中，指定应用程序的提供程序。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="9fdf6-264">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-264">Select **Save**.</span></span> 
9. <span data-ttu-id="9fdf6-265">检查与配置的应用程序之间的连接时，请在**连接到远程应用程序**页中选择**选择此处连接到所选远程应用程序**链接。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="9fdf6-266">选择**检查连接**以验证所配置应用程序的访问权限。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="9fdf6-267">选择**关闭**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-267">Select **Close**.</span></span>

<span data-ttu-id="9fdf6-268">完成此过程且连接验证成功后，将在当前网格中更新所配置应用程序的版本和租户详细信息。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="9fdf6-269">检查现有模型映射配置</span><span class="sxs-lookup"><span data-stu-id="9fdf6-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="9fdf6-270">转到**所有工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="9fdf6-271">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="9fdf6-272">在树中，选择**外贸模型 \> 外贸映射**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="9fdf6-273">选择**先决条件**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fdf6-274">此映射当前引用元数据配置。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="9fdf6-275">设计此模型映射时，将提供来自此配置的应用程序元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="9fdf6-276">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-276">Select **Designer**.</span></span>
5. <span data-ttu-id="9fdf6-277">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-277">Select **Designer**.</span></span>
6. <span data-ttu-id="9fdf6-278">在树中，选择 **Dynamics 365 for Operations \> 表记录**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="9fdf6-279">选择**添加根**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-279">Select **Add root**.</span></span>
8. <span data-ttu-id="9fdf6-280">在**表格**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fdf6-281">此映射当前引用元数据配置。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="9fdf6-282">设计此模型映射时，将提供来自此配置的应用程序元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="9fdf6-283">选择**取消**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="9fdf6-284">将相连应用程序分配给模型映射</span><span class="sxs-lookup"><span data-stu-id="9fdf6-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="9fdf6-285">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-285">Select **Edit**.</span></span>
2. <span data-ttu-id="9fdf6-286">在**相连应用程序**字段中，选择 **MyConnectedApp** 应用程序。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fdf6-287">此映射引用所选相连应用程序的元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="9fdf6-288">如果映射同时引用元数据配置和相连应用程序时，将使用相连应用程序的元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="9fdf6-289">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-289">Select **Designer**.</span></span>
4. <span data-ttu-id="9fdf6-290">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-290">Select **Designer**.</span></span>
5. <span data-ttu-id="9fdf6-291">在树中，选择 **Dynamics 365 for Operations \> 表记录**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="9fdf6-292">选择**添加根**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-292">Select **Add root**.</span></span>
7. <span data-ttu-id="9fdf6-293">在**表格**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fdf6-294">此时提供了两个以上的应用程序表，因为此映射使用已经为其分配的相连应用程序的所有元数据。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="9fdf6-295">选择**取消**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="9fdf6-296">选择**验证**。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-296">Select **Validate**.</span></span>

<span data-ttu-id="9fdf6-297">现在已使用已为此映射分配的相连应用程序的元数据详细信息将数据模型的元素绑定到了介绍的数据源项。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="9fdf6-298">如果必须使用另一个版本应用程序的元数据评估此模型映射，请再注册一个相连应用程序，将其分配给此模型映射，然后使用新元数据再次验证。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9fdf6-299">其他资源</span><span class="sxs-lookup"><span data-stu-id="9fdf6-299">Additional resources</span></span>

<span data-ttu-id="9fdf6-300">也可以播放 Finance and Operationsas 中的**准备可在 RCS 中使用的应用程序元数据**任务指南，以及 RCS 中的**通过使用 ER 配置访问应用程序元数据**和**通过使用相连应用程序访问应用程序元数据**任务指南。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in Finance and Operationsas as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="9fdf6-301">可以从 [Dynamics 365 for Finance and Operations 8.1 电子申报任务指南](https://go.microsoft.com/fwlink/?linkid=2082739)页下载这些任务指南。</span><span class="sxs-lookup"><span data-stu-id="9fdf6-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
