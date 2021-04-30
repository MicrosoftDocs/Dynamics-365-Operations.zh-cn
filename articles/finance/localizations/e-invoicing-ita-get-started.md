---
title: 开始使用适用于意大利的电子开票
description: 本主题提供的信息将帮助您开始使用适用于意大利的电子开票。
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 140977a6eac145f35870d3516a4b0d0c794afe4b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894769"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a><span data-ttu-id="0aec1-103">开始使用适用于意大利的电子开票</span><span class="sxs-lookup"><span data-stu-id="0aec1-103">Get started with Electronic invoicing for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="0aec1-104">适用于意大利的电子开票当前可能不支持 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中可用于电子发票的所有功能。</span><span class="sxs-lookup"><span data-stu-id="0aec1-104">Electronic invoicing for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="0aec1-105">本主题提供的信息将帮助您开始使用适用于意大利的电子开票。</span><span class="sxs-lookup"><span data-stu-id="0aec1-105">This topic provides information that will help you get started with Electronic invoicing for Italy.</span></span> <span data-ttu-id="0aec1-106">指导您完成 Regulatory Configuration Services (RCS) 和 Finance 中与国家/地区相关的配置步骤。</span><span class="sxs-lookup"><span data-stu-id="0aec1-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="0aec1-107">还会指导您完成通过服务提交以意大利特定的 **FatturaPA** 格式生成的电子发票的流程，并说明如何查看处理结果。</span><span class="sxs-lookup"><span data-stu-id="0aec1-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0aec1-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="0aec1-108">Prerequisites</span></span>

<span data-ttu-id="0aec1-109">在完成本主题中的步骤之前，您必须完成[开始使用电子开票](e-invoicing-get-started.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="0aec1-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="0aec1-110">RCS 设置</span><span class="sxs-lookup"><span data-stu-id="0aec1-110">RCS setup</span></span>

<span data-ttu-id="0aec1-111">在 RCS 设置期间，您将完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="0aec1-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="0aec1-112">导入可以 **FatturaPA** 格式导出客户电子发票的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="0aec1-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="0aec1-113">查看生成、提交和接收有关电子发票的响应所需的格式配置。</span><span class="sxs-lookup"><span data-stu-id="0aec1-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="0aec1-114">配置支持电子发票提交方案的事件。</span><span class="sxs-lookup"><span data-stu-id="0aec1-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="0aec1-115">发布电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="0aec1-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="0aec1-116">“电子开票功能”是配置和发布以使用电子开票服务器的资源的通用名称。</span><span class="sxs-lookup"><span data-stu-id="0aec1-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="0aec1-117">在这种情况下，导出客户电子发票是您将要设置的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="0aec1-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="0aec1-118">导入电子开票功能</span><span class="sxs-lookup"><span data-stu-id="0aec1-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="0aec1-119">登录您的 RCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="0aec1-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0aec1-120">在 **全球化功能** 工作区中，在 **功能** 部分，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="0aec1-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="0aec1-121">在 **电子开票功能** 页上，选择 **导入** 从全局存储库中导入电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="0aec1-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0aec1-122">如果看不到可用功能列表，请选择 **同步**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="0aec1-123">选择 **电子发票导出 (IT)** 功能，然后选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![导入电子发票导出 (IT) 功能](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="0aec1-125">从全局存储库导入 **电子发票导出 (IT)** 功能时，还将导入接下来几节中所述的所有设置。</span><span class="sxs-lookup"><span data-stu-id="0aec1-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="0aec1-126">创建新版本的电子发票导出 (IT) 功能</span><span class="sxs-lookup"><span data-stu-id="0aec1-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="0aec1-127">在 **电子开票功能** 页上的 **版本** 选项卡上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![添加新的电子开票功能版本](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="0aec1-129">接下来，您将配置与电子开票功能关联的电子报告 (ER) 格式。</span><span class="sxs-lookup"><span data-stu-id="0aec1-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="0aec1-130">在 **配置** 选项卡上，选择 **添加** 管理配置版本。</span><span class="sxs-lookup"><span data-stu-id="0aec1-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![管理电子开票功能配置版本](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="0aec1-132">在此步骤中，您将添加和配置用于导出意大利电子发票的不同文件的 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="0aec1-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="0aec1-133">对于意大利 FatturaPA 电子发票，请使用以下标准配置或用于电子开票的实际的自定义配置：</span><span class="sxs-lookup"><span data-stu-id="0aec1-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="0aec1-134">销售发票 (IT)</span><span class="sxs-lookup"><span data-stu-id="0aec1-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="0aec1-135">项目发票 (IT)</span><span class="sxs-lookup"><span data-stu-id="0aec1-135">Project invoice (IT)</span></span>

    <span data-ttu-id="0aec1-136">当您创建从另一个电子开票功能派生的电子开票功能时，所有 ER 格式都将从原始功能继承。</span><span class="sxs-lookup"><span data-stu-id="0aec1-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="0aec1-137">选择特定的 ER 格式文件配置。</span><span class="sxs-lookup"><span data-stu-id="0aec1-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="0aec1-138">选择 **编辑** 或 **查看** 打开 **格式设计器** 页。</span><span class="sxs-lookup"><span data-stu-id="0aec1-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![打开“格式设计器”页](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="0aec1-140">使用 **格式设计器** 页编辑和查看 ER 格式文件配置。</span><span class="sxs-lookup"><span data-stu-id="0aec1-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![“格式设计器”页面](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="0aec1-142">管理电子开票功能设置</span><span class="sxs-lookup"><span data-stu-id="0aec1-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="0aec1-143">在 **电子开票功能** 页上的 **设置** 选项卡上，选择 **添加**、**删除** 或 **编辑** 管理电子开票功能设置。</span><span class="sxs-lookup"><span data-stu-id="0aec1-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![管理电子开票功能设置](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="0aec1-145">在此步骤中，您将配置适用于电子发票的事件，包括生成 **FatturaPA** 格式的 XML 输出文件和数字签名（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="0aec1-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="0aec1-146">配置“销售发票”功能设置</span><span class="sxs-lookup"><span data-stu-id="0aec1-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="0aec1-147">在 **电子开票功能** 页上的 **设置** 选项卡上，在 **功能设置** 列中，选择 **销售发票**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="0aec1-148">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-148">Select **Edit**.</span></span>
3. <span data-ttu-id="0aec1-149">在 **功能版本设置** 页上，选择 **操作** 选项卡管理操作列表。</span><span class="sxs-lookup"><span data-stu-id="0aec1-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="0aec1-150">操作定义必须按顺序运行以完成事件的完全执行的操作的列表。</span><span class="sxs-lookup"><span data-stu-id="0aec1-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![“操作”选项卡](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="0aec1-152">行动 ID</span><span class="sxs-lookup"><span data-stu-id="0aec1-152">Action ID</span></span> | <span data-ttu-id="0aec1-153">操作名称</span><span class="sxs-lookup"><span data-stu-id="0aec1-153">Action name</span></span>        | <span data-ttu-id="0aec1-154">操作描述</span><span class="sxs-lookup"><span data-stu-id="0aec1-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="0aec1-155">1</span><span class="sxs-lookup"><span data-stu-id="0aec1-155">1</span></span>         | <span data-ttu-id="0aec1-156">转换文档</span><span class="sxs-lookup"><span data-stu-id="0aec1-156">Transform document</span></span> | <span data-ttu-id="0aec1-157">以 **FatturaPA** 格式创建电子发票 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="0aec1-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="0aec1-158">2</span><span class="sxs-lookup"><span data-stu-id="0aec1-158">2</span></span>         | <span data-ttu-id="0aec1-159">对文档签名</span><span class="sxs-lookup"><span data-stu-id="0aec1-159">Sign document</span></span>      | <span data-ttu-id="0aec1-160">将数字签名应用于 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="0aec1-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="0aec1-161">选择 **适用性规则** 选项卡查看和维护适用性规则。</span><span class="sxs-lookup"><span data-stu-id="0aec1-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="0aec1-162">适用性规则定义操作将在其中运行的上下文。</span><span class="sxs-lookup"><span data-stu-id="0aec1-162">Applicability rules define the context where the action will be run.</span></span>

    ![“适用性规则”选项卡](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="0aec1-164">选择 **变量** 选项卡查看和维护变量。</span><span class="sxs-lookup"><span data-stu-id="0aec1-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![“变量”选项卡](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="0aec1-166">定义运行操作所需的公共变量。</span><span class="sxs-lookup"><span data-stu-id="0aec1-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="0aec1-167">配置“项目发票”功能设置</span><span class="sxs-lookup"><span data-stu-id="0aec1-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="0aec1-168">配置 **项目发票** 功能设置所需的步骤和设置与 **销售发票** 功能设置的步骤和设置非常相似。</span><span class="sxs-lookup"><span data-stu-id="0aec1-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="0aec1-169">处理项目发票时，请参阅销售发票的过程。</span><span class="sxs-lookup"><span data-stu-id="0aec1-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="0aec1-170">将电子开票功能分配到环境</span><span class="sxs-lookup"><span data-stu-id="0aec1-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="0aec1-171">在 **电子开票功能** 页上的 **环境** 选项卡上，选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="0aec1-172">在 **环境** 字段中，选择环境。</span><span class="sxs-lookup"><span data-stu-id="0aec1-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="0aec1-173">在 **生效开始日期** 字段中，选择环境应该生效的日期。</span><span class="sxs-lookup"><span data-stu-id="0aec1-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="0aec1-174">选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-174">Select **Enable**.</span></span> 

![启用电子开票环境](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="0aec1-176">发布电子开票功能</span><span class="sxs-lookup"><span data-stu-id="0aec1-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="0aec1-177">您可以通过将版本状态更改为 **已完成** 或 **已发布** 来发布电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="0aec1-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="0aec1-178">将版本状态更改为“已完成”</span><span class="sxs-lookup"><span data-stu-id="0aec1-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="0aec1-179">在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **草稿** 的电子开票功能的版本。</span><span class="sxs-lookup"><span data-stu-id="0aec1-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="0aec1-180">选择 **更改状态 \> 完成**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="0aec1-181">将版本状态更改为“已发布”</span><span class="sxs-lookup"><span data-stu-id="0aec1-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="0aec1-182">在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **已完成** 的电子开票功能的版本。</span><span class="sxs-lookup"><span data-stu-id="0aec1-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="0aec1-183">选择 **更改状态 \> 发布**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-183">Select **Change status \> Publish**.</span></span>

![更改电子开票功能的状态](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a><span data-ttu-id="0aec1-185">在 Finance 中设置电子开票集成</span><span class="sxs-lookup"><span data-stu-id="0aec1-185">Set up Electronic invoicing integration in Finance</span></span>

<span data-ttu-id="0aec1-186">在 Finance 设置期间，您将完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="0aec1-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="0aec1-187">导入 FatturaPA 电子发票的 ER 数据模型、ER 数据模型映射和上下文配置。</span><span class="sxs-lookup"><span data-stu-id="0aec1-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="0aec1-188">配置对意大利电子发票进行数字签名所需的证书。</span><span class="sxs-lookup"><span data-stu-id="0aec1-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="0aec1-189">导入 ER 数据模型、数据模型映射和格式</span><span class="sxs-lookup"><span data-stu-id="0aec1-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="0aec1-190">在 **电子报告** 工作区中，确认 **业务文档服务** 配置提供程序设置为 **活动**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="0aec1-191">选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="0aec1-192">选择 **全局资源 \> 打开**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="0aec1-193">导入 **发票模型**、**发票模型映射** 和 **客户发票上下文模型**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="0aec1-194">打开导出意大利客户电子发票的功能</span><span class="sxs-lookup"><span data-stu-id="0aec1-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="0aec1-195">转到 **组织管理 \> 设置 \> 电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="0aec1-196">在 **功能** 选项卡上，选中功能引用 **IT00036** 的行中的 **已启用** 复选框。</span><span class="sxs-lookup"><span data-stu-id="0aec1-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![打开 FatturaPA 功能](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="0aec1-198">配置电子单据</span><span class="sxs-lookup"><span data-stu-id="0aec1-198">Configure electronic documents</span></span>

1. <span data-ttu-id="0aec1-199">转到 **组织管理 \> 设置 \> 电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="0aec1-200">在 **电子单据** 选项卡，选择 **添加**，输入生成意大利电子发票所需的表：</span><span class="sxs-lookup"><span data-stu-id="0aec1-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="0aec1-201">**表名称：** 客户发票日记帐</span><span class="sxs-lookup"><span data-stu-id="0aec1-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="0aec1-202">**表名称：** 项目发票</span><span class="sxs-lookup"><span data-stu-id="0aec1-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="0aec1-203">为每个表定义一个相关的文档上下文：</span><span class="sxs-lookup"><span data-stu-id="0aec1-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="0aec1-204">对于 **客户发票日记帐**，选择 **客户发票上下文**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="0aec1-205">对于 **项目发票**，选择 **项目发票上下文**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-205">For **Project invoice**, select **Project invoice context**.</span></span>

![设置响应类型](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="0aec1-207">电子发票处理</span><span class="sxs-lookup"><span data-stu-id="0aec1-207">Electronic invoice processing</span></span>

<span data-ttu-id="0aec1-208">在 Finance 中进行处理期间，您将完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="0aec1-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="0aec1-209">通过电子开票生成意大利电子发票</span><span class="sxs-lookup"><span data-stu-id="0aec1-209">Generate Italian e-invoices through Electronic invoicing</span></span>
2. <span data-ttu-id="0aec1-210">查看执行日志和处理结果</span><span class="sxs-lookup"><span data-stu-id="0aec1-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="0aec1-211">生成电子发票</span><span class="sxs-lookup"><span data-stu-id="0aec1-211">Generate electronic invoices</span></span>

<span data-ttu-id="0aec1-212">打开 **可配置电子开票集成** 功能并激活 **IT00036** 功能后，将不再使用生成意大利电子发票的旧 Finance 流程。</span><span class="sxs-lookup"><span data-stu-id="0aec1-212">After you turn on the **Configurable Electronic invoicing integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="0aec1-213">取而代之的是一个名为 **提交电子单据** 的新流程。</span><span class="sxs-lookup"><span data-stu-id="0aec1-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="0aec1-214">您可以根据对电子发票单据的要求手动提交单据。</span><span class="sxs-lookup"><span data-stu-id="0aec1-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="0aec1-215">在继续之前，请验证意大利电子发票所需的设置已完成。</span><span class="sxs-lookup"><span data-stu-id="0aec1-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="0aec1-216">有关详细信息，请参阅[客户电子发票](./emea-ita-e-invoices.md)。</span><span class="sxs-lookup"><span data-stu-id="0aec1-216">For more information, see [Customer electronic invoices](./emea-ita-e-invoices.md).</span></span> <span data-ttu-id="0aec1-217">请注意，该主题中所述的某些设置步骤可能由于电子开票激活不可用。</span><span class="sxs-lookup"><span data-stu-id="0aec1-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing activation.</span></span>

1. <span data-ttu-id="0aec1-218">转到 **组织管理 \> 定期 \> 电子单据 \> 提交电子单据**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="0aec1-219">对于任何文档的首次提交，请将 **重新提交文档** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="0aec1-220">如果必须通过服务重新提交文档，请将此选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="0aec1-221">在 **要包括的记录** 快速选项卡上，选择 **筛选** 打开 **查询** 对话框，您可以在其中构建查询来选择要提交的文档。</span><span class="sxs-lookup"><span data-stu-id="0aec1-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![“提交电子单据”对话框](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="0aec1-223">筛选器查询</span><span class="sxs-lookup"><span data-stu-id="0aec1-223">Filter query</span></span>

1. <span data-ttu-id="0aec1-224">在 **查询** 对话框中，配置销售发票和项目发票的筛选条件，或将条件留空以包括所有未提交的发票。</span><span class="sxs-lookup"><span data-stu-id="0aec1-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![设置提交筛选条件](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="0aec1-226">单击 **确定** 以关闭 **查询** 对话框。</span><span class="sxs-lookup"><span data-stu-id="0aec1-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="0aec1-227">选择 **确定** 提交所选文档。</span><span class="sxs-lookup"><span data-stu-id="0aec1-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="0aec1-228">![注意] 在首次尝试通过服务提交单据时，系统会提示您确认与电子开票的连接。</span><span class="sxs-lookup"><span data-stu-id="0aec1-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="0aec1-229">选择 **单击此处连接到电子单据提交服务**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="0aec1-230">查看提交日志</span><span class="sxs-lookup"><span data-stu-id="0aec1-230">View submission logs</span></span>

<span data-ttu-id="0aec1-231">您可以查看所有已提交文档的提交日志。</span><span class="sxs-lookup"><span data-stu-id="0aec1-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="0aec1-232">转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。</span><span class="sxs-lookup"><span data-stu-id="0aec1-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="0aec1-233">在 **文档类型** 字段中，选择 **客户发票日记帐** 或 **项目发票** 筛选所需的电子单据。</span><span class="sxs-lookup"><span data-stu-id="0aec1-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![选择文档类型以查看提交日志](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="0aec1-235">**提交状态** 列中显示的值表示提交流程的状态。</span><span class="sxs-lookup"><span data-stu-id="0aec1-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="0aec1-236">指示流程是否按配置运行，以及是否需要其他操作。</span><span class="sxs-lookup"><span data-stu-id="0aec1-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="0aec1-237">在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。</span><span class="sxs-lookup"><span data-stu-id="0aec1-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![查看提交日志详细信息](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="0aec1-239">在 **处理操作** 快速选项卡上，您可以查看在 RCS 中设置的功能版本中配置的操作的执行日志。</span><span class="sxs-lookup"><span data-stu-id="0aec1-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="0aec1-240">**状态** 列显示操作是否成功运行。</span><span class="sxs-lookup"><span data-stu-id="0aec1-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="0aec1-241">在 **操作文件** 快速选项卡上，您可以查看在执行操作期间生成的中间文件。</span><span class="sxs-lookup"><span data-stu-id="0aec1-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="0aec1-242">您可以选择 **查看** 以 **FatturaPA** 格式下载输出 XML 文件并查看其内容。</span><span class="sxs-lookup"><span data-stu-id="0aec1-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aec1-243">相关主题</span><span class="sxs-lookup"><span data-stu-id="0aec1-243">Related topics</span></span>

- [<span data-ttu-id="0aec1-244">电子开票概览</span><span class="sxs-lookup"><span data-stu-id="0aec1-244">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="0aec1-245">开始使用电子开票</span><span class="sxs-lookup"><span data-stu-id="0aec1-245">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="0aec1-246">设置电子开票</span><span class="sxs-lookup"><span data-stu-id="0aec1-246">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]