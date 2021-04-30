---
title: 开始使用适用于墨西哥的电子开票
description: 本主题提供的信息将帮助您开始使用适用于墨西哥的电子开票。
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
ms.openlocfilehash: c1112ba8394afb3aa9c9b4f68249524498bd8b32
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894875"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a><span data-ttu-id="35823-103">开始使用适用于墨西哥的电子开票</span><span class="sxs-lookup"><span data-stu-id="35823-103">Get started with Electronic invoicing for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="35823-104">适用于墨西哥的电子开票当前可能不支持 Comprobante Fiscal Digital por Internet (CFDI) 单据以及 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 中内置的相关集成中提供的所有功能。</span><span class="sxs-lookup"><span data-stu-id="35823-104">Electronic invoicing for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="35823-105">本主题提供的信息将帮助您开始使用适用于墨西哥的电子开票。</span><span class="sxs-lookup"><span data-stu-id="35823-105">This topic provides information that will help you get started with Electronic invoicing for Mexico.</span></span> <span data-ttu-id="35823-106">指导您完成 Regulatory Configuration Services (RCS) 和 Finance 中与国家/地区相关的配置步骤。</span><span class="sxs-lookup"><span data-stu-id="35823-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="35823-107">还将指导您完成 Finance 中通过服务提交 CFDI 发票所必须遵循的步骤，并说明如何查看处理结果和 CFDI 发票的状态。</span><span class="sxs-lookup"><span data-stu-id="35823-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="35823-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="35823-108">Prerequisites</span></span>

<span data-ttu-id="35823-109">在完成本主题中的步骤之前，您必须完成[开始使用电子开票](e-invoicing-get-started.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="35823-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="35823-110">RCS 设置</span><span class="sxs-lookup"><span data-stu-id="35823-110">RCS setup</span></span>

<span data-ttu-id="35823-111">在 RCS 设置期间，您将完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="35823-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="35823-112">导入电子开票功能来处理 CFDI 发票。</span><span class="sxs-lookup"><span data-stu-id="35823-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="35823-113">查看生成、提交和接收有关 CFDI 发票的响应以及提交和接收有关取消的响应所需的格式配置。</span><span class="sxs-lookup"><span data-stu-id="35823-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="35823-114">配置支持 CFDI 发票提交方案的事件。</span><span class="sxs-lookup"><span data-stu-id="35823-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="35823-115">发布 CFDI 发票的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="35823-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="35823-116">“电子开票功能”是配置和发布以使用电子开票服务器的资源的通用名称。</span><span class="sxs-lookup"><span data-stu-id="35823-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="35823-117">在这种情况下，CFDI 发票 (MX) 是您将要设置的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="35823-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="35823-118">导入电子开票功能</span><span class="sxs-lookup"><span data-stu-id="35823-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="35823-119">登录您的 RCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="35823-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="35823-120">在 **全球化功能** 工作区中，在 **功能** 部分，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="35823-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="35823-121">在 **电子开票功能** 页上，选择 **导入** 从全局存储库中导入 **CFDI 发票 (MX)** 功能。</span><span class="sxs-lookup"><span data-stu-id="35823-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="35823-122">如果您没有在列表中看到此功能，请选择 **同步**，然后重复步骤 3。</span><span class="sxs-lookup"><span data-stu-id="35823-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![导入 CFDI 发票 (MX) 功能](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="35823-124">从全局存储库导入 **CFDI 发票 (MX)** 能时，还将导入所有功能设置，包括配置和操作。</span><span class="sxs-lookup"><span data-stu-id="35823-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="35823-125">创建新版本的 CFDI 发票 (MX) 功能</span><span class="sxs-lookup"><span data-stu-id="35823-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="35823-126">例如，如果必须更新 URL，您可以创建新版本。</span><span class="sxs-lookup"><span data-stu-id="35823-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="35823-127">有关详细信息，请参阅[电子开票 CFDI](tasks/mx-00010-e-invoicing-cfdi.md)。</span><span class="sxs-lookup"><span data-stu-id="35823-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="35823-128">在 **电子开票功能** 页上的 **版本** 选项卡上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="35823-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![添加新的电子开票功能版本](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="35823-130">更新配置版本</span><span class="sxs-lookup"><span data-stu-id="35823-130">Update the configuration version</span></span>

1. <span data-ttu-id="35823-131">在 **电子开票功能** 页上的 **配置** 选项卡上，选择 **添加** 或 **删除** 管理配置版本（ER 文件格式配置）。</span><span class="sxs-lookup"><span data-stu-id="35823-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![管理电子开票功能配置](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="35823-133">创建新版本时，所有配置都将从上次发布的版本继承。</span><span class="sxs-lookup"><span data-stu-id="35823-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="35823-134">要处理 CFDI 发票，需要以下配置：</span><span class="sxs-lookup"><span data-stu-id="35823-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="35823-135">CFDI 发票 (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="35823-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="35823-136">CFDI 响应消息导入</span><span class="sxs-lookup"><span data-stu-id="35823-136">CFDI response message import</span></span>
    - <span data-ttu-id="35823-137">CFDI 错误日志导入</span><span class="sxs-lookup"><span data-stu-id="35823-137">CFDI error log import</span></span>
    - <span data-ttu-id="35823-138">CFDI 取消请求 (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="35823-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="35823-139">CFDI 发票 (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="35823-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="35823-140">在列表中，选择配置版本，然后选择 **编辑** 或 **查看** 打开 **格式设计器** 页，您可以在其中编辑或查看配置。</span><span class="sxs-lookup"><span data-stu-id="35823-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![打开“格式设计器”页](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="35823-142">使用 **格式设计器** 页编辑和查看 ER 格式文件配置。</span><span class="sxs-lookup"><span data-stu-id="35823-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="35823-143">有关详细信息，请参阅[创建电子单据配置](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md)。</span><span class="sxs-lookup"><span data-stu-id="35823-143">For more information, see [Create electronic document configurations](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![“格式设计器”页面](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="35823-145">管理电子开票功能设置</span><span class="sxs-lookup"><span data-stu-id="35823-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="35823-146">在 **电子开票功能** 页上的 **设置** 选项卡上，选择 **添加**、**删除** 或 **编辑** 管理电子开票功能设置。</span><span class="sxs-lookup"><span data-stu-id="35823-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![管理电子开票功能设置](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="35823-148">要提交 CFDI 发票进行授权（生成 XML 文件、提交 XML 文件和处理响应），需要 **销售发票** 功能设置。</span><span class="sxs-lookup"><span data-stu-id="35823-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="35823-149">要提交 CFDI 发票取消，需要 **取消** 和 **取消** 功能设置。</span><span class="sxs-lookup"><span data-stu-id="35823-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="35823-150">配置“销售发票”功能设置</span><span class="sxs-lookup"><span data-stu-id="35823-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="35823-151">在 **电子开票功能** 页上的 **设置** 选项卡上，在 **功能设置** 列中，选择 **销售发票**。</span><span class="sxs-lookup"><span data-stu-id="35823-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="35823-152">选择 **编辑** 配置操作、适用性规则和变量。</span><span class="sxs-lookup"><span data-stu-id="35823-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![编辑电子开票功能设置](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="35823-154">在 **功能版本设置** 页上，选择 **操作** 选项卡管理操作列表。</span><span class="sxs-lookup"><span data-stu-id="35823-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="35823-155">操作定义必须按顺序运行以完成事件的完全执行的操作的列表。</span><span class="sxs-lookup"><span data-stu-id="35823-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![“操作”选项卡](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="35823-157">行动 ID</span><span class="sxs-lookup"><span data-stu-id="35823-157">Action ID</span></span> | <span data-ttu-id="35823-158">行动</span><span class="sxs-lookup"><span data-stu-id="35823-158">Action</span></span>                   | <span data-ttu-id="35823-159">操作名称</span><span class="sxs-lookup"><span data-stu-id="35823-159">Action name</span></span>                                  | <span data-ttu-id="35823-160">操作描述</span><span class="sxs-lookup"><span data-stu-id="35823-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="35823-161">1</span><span class="sxs-lookup"><span data-stu-id="35823-161">1</span></span>         | <span data-ttu-id="35823-162">转换文档</span><span class="sxs-lookup"><span data-stu-id="35823-162">Transform document</span></span>       | <span data-ttu-id="35823-163">生成没有数字签名的 CFDI 电子发票</span><span class="sxs-lookup"><span data-stu-id="35823-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="35823-164">生成 CFDI 电子发票。</span><span class="sxs-lookup"><span data-stu-id="35823-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="35823-165">2</span><span class="sxs-lookup"><span data-stu-id="35823-165">2</span></span>         | <span data-ttu-id="35823-166">对文档签名</span><span class="sxs-lookup"><span data-stu-id="35823-166">Sign document</span></span>            | <span data-ttu-id="35823-167">数字签名</span><span class="sxs-lookup"><span data-stu-id="35823-167">Digital sign</span></span>                                 | <span data-ttu-id="35823-168">对电子发票进行数字签名以进行提交。</span><span class="sxs-lookup"><span data-stu-id="35823-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="35823-169">3</span><span class="sxs-lookup"><span data-stu-id="35823-169">3</span></span>         | <span data-ttu-id="35823-170">调用墨西哥 PAC 服务</span><span class="sxs-lookup"><span data-stu-id="35823-170">Call Mexican PAC service</span></span> | <span data-ttu-id="35823-171">提交 CFDI 电子发票</span><span class="sxs-lookup"><span data-stu-id="35823-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="35823-172">Windows Communication Foundation (WCF) 客户端提交 CFDI 电子发票。</span><span class="sxs-lookup"><span data-stu-id="35823-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="35823-173">4</span><span class="sxs-lookup"><span data-stu-id="35823-173">4</span></span>         | <span data-ttu-id="35823-174">处理响应</span><span class="sxs-lookup"><span data-stu-id="35823-174">Process response</span></span>         | <span data-ttu-id="35823-175">分析 Web 服务响应</span><span class="sxs-lookup"><span data-stu-id="35823-175">Analyze web service response</span></span>                 | <span data-ttu-id="35823-176">分析 Web 服务响应，并返回错误日志。</span><span class="sxs-lookup"><span data-stu-id="35823-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="35823-177">为墨西哥 PAC Web 服务设置 URL</span><span class="sxs-lookup"><span data-stu-id="35823-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="35823-178">在 **功能版本设置** 页上的 **操作** 选项卡上，在 **操作** 快速选项卡上，选择 **调用墨西哥 PAC 服务**。</span><span class="sxs-lookup"><span data-stu-id="35823-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="35823-179">在 **参数** 快速选项卡的 **URL 地址** 字段中，输入用于提交 CFDI 发票的 Web 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="35823-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="35823-180">使用相同的步骤为 **取消** 和 **取消请求** 功能设置更新 **调用墨西哥 PAC 服务** 操作的 URL。</span><span class="sxs-lookup"><span data-stu-id="35823-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="35823-181">将草稿版本分配给电子开票环境</span><span class="sxs-lookup"><span data-stu-id="35823-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="35823-182">在 **电子开票功能** 页上的 **环境** 选项卡上，选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="35823-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="35823-183">在 **环境** 字段中，选择环境。</span><span class="sxs-lookup"><span data-stu-id="35823-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="35823-184">在 **生效开始日期** 字段中，选择环境应该生效的日期。</span><span class="sxs-lookup"><span data-stu-id="35823-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="35823-185">选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="35823-185">Select **Enable**.</span></span>

![启用电子开票环境](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="35823-187">将版本状态更改为“已完成”</span><span class="sxs-lookup"><span data-stu-id="35823-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="35823-188">在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **草稿** 的电子开票功能的版本。</span><span class="sxs-lookup"><span data-stu-id="35823-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="35823-189">选择 **更改状态 \> 完成**。</span><span class="sxs-lookup"><span data-stu-id="35823-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="35823-190">将版本状态更改为“已发布”</span><span class="sxs-lookup"><span data-stu-id="35823-190">Change the version status to Published</span></span>

- <span data-ttu-id="35823-191">在 **电子开票功能** 页上的 **版本** 选项卡上，选择 **更改状态 \> 发布**。</span><span class="sxs-lookup"><span data-stu-id="35823-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="35823-192">发布电子开票功能</span><span class="sxs-lookup"><span data-stu-id="35823-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="35823-193">在 **电子开票功能** 页上，选择 **版本** 选项卡管理 **CFDI 发票 (MX)** 功能的状态。</span><span class="sxs-lookup"><span data-stu-id="35823-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="35823-194">选择 **更改状态** 更改功能的状态。</span><span class="sxs-lookup"><span data-stu-id="35823-194">Select **Change status** to change the status of the feature.</span></span>

![更改电子开票功能的状态](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a><span data-ttu-id="35823-196">在 Finance 中设置电子开票集成</span><span class="sxs-lookup"><span data-stu-id="35823-196">Set up Electronic invoicing  integration in Finance</span></span>

<span data-ttu-id="35823-197">若要在 Finance 中设置电子开票，您将完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="35823-197">To set up Electronic invoicing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="35823-198">导入 ER 数据模型、ER 数据模型映射以及 CFDI 发票所需的格式。</span><span class="sxs-lookup"><span data-stu-id="35823-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="35823-199">配置更新 CFDI 发票的响应类型。</span><span class="sxs-lookup"><span data-stu-id="35823-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="35823-200">这些响应类型用于来自授权认证提供程序 (PAC) 服务器的响应。</span><span class="sxs-lookup"><span data-stu-id="35823-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="35823-201">导入 CFDI 发票的 ER 数据模型、ER 数据模型映射和上下文配置</span><span class="sxs-lookup"><span data-stu-id="35823-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="35823-202">登录 Finance。</span><span class="sxs-lookup"><span data-stu-id="35823-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="35823-203">在 **电子报告** 工作区的 **配置提供程序** 部分，选择 **Microsoft** 标题。</span><span class="sxs-lookup"><span data-stu-id="35823-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="35823-204">确保此配置提供程序设置为 **有效**。</span><span class="sxs-lookup"><span data-stu-id="35823-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="35823-205">有关如何将提供程序设置为 **有效** 的信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="35823-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="35823-206">选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="35823-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="35823-207">选择 **全局资源 \> 打开**。</span><span class="sxs-lookup"><span data-stu-id="35823-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="35823-208">导入 **发票模型**、**发票模型映射**、**CFDI 发票格式 (MX)**、**CFDI 发票取消请求格式 (MX)** 和 **CFDI 发票取消格式 (MX)**。</span><span class="sxs-lookup"><span data-stu-id="35823-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="35823-209">打开处理 CFDI 发票的功能</span><span class="sxs-lookup"><span data-stu-id="35823-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="35823-210">转到 **组织管理 \> 设置 \> 电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="35823-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="35823-211">在 **功能** 选项卡上，选中功能引用 **MX-00010** 和 **MX-00016** 的行中的 **启用** 复选框。</span><span class="sxs-lookup"><span data-stu-id="35823-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![打开处理 CFDI 发票的功能](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="35823-213">导入 ER 配置并设置更新 CFDI 发票的响应类型</span><span class="sxs-lookup"><span data-stu-id="35823-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="35823-214">导入 ER 配置</span><span class="sxs-lookup"><span data-stu-id="35823-214">Import ER configurations</span></span>

1. <span data-ttu-id="35823-215">在 **电子报告** 工作区的 **配置提供程序** 部分，选择 **Microsoft** 标题。</span><span class="sxs-lookup"><span data-stu-id="35823-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="35823-216">选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="35823-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="35823-217">选择 **全局资源 \> 打开**。</span><span class="sxs-lookup"><span data-stu-id="35823-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="35823-218">导入 **响应消息模型**、**CFDI 错误日志导入 (MX)** 和 **CFDI 响应消息导入 (MX)**。</span><span class="sxs-lookup"><span data-stu-id="35823-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="35823-219">设置响应类型</span><span class="sxs-lookup"><span data-stu-id="35823-219">Set up the response types</span></span>

1. <span data-ttu-id="35823-220">转到 **组织管理 \> 设置 \> 电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="35823-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="35823-221">在 **电子单据** 选项卡上，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="35823-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="35823-222">输入客户发票日记帐，然后在 **表名称** 字段中，选择项目发票。</span><span class="sxs-lookup"><span data-stu-id="35823-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="35823-223">为每个表定义一个相关的文档上下文：</span><span class="sxs-lookup"><span data-stu-id="35823-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="35823-224">对于 **客户发票日记帐**，输入 **客户发票上下文**。</span><span class="sxs-lookup"><span data-stu-id="35823-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="35823-225">对于 **项目发票**，输入 **项目发票上下文**。</span><span class="sxs-lookup"><span data-stu-id="35823-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="35823-226">选择 **响应类型** 配置可以从电子开票返回并包含在客户发票日记帐或项目发票中的响应类型。</span><span class="sxs-lookup"><span data-stu-id="35823-226">Select **Response types** to configure the response types that can be returned from Electronic invoicing and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="35823-227">选择 **新建**，然后在 **响应类型** 字段中选择 **Response**。</span><span class="sxs-lookup"><span data-stu-id="35823-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="35823-228">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="35823-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="35823-229">在 **模型映射** 字段中，选择 **响应消息导入格式 – 来自响应消息的模型映射**。</span><span class="sxs-lookup"><span data-stu-id="35823-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="35823-230">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="35823-230">Select **Save**.</span></span>
9. <span data-ttu-id="35823-231">选择 **新建**，然后在 **响应类型** 字段中选择 **ResponseData**。</span><span class="sxs-lookup"><span data-stu-id="35823-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="35823-232">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="35823-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="35823-233">在 **模型映射** 字段中，选择 **CFDI 响应数据导入格式(详细信息) – 响应数据导入**。</span><span class="sxs-lookup"><span data-stu-id="35823-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="35823-234">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="35823-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="35823-235">在 Finance 中处理电子发票</span><span class="sxs-lookup"><span data-stu-id="35823-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="35823-236">在通过电子开票在 Finance 中处理 CFDI 发票期间，您可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="35823-236">During the processing of CFDI invoices in Finance through Electronic invoicing, you can perform the following tasks:</span></span>

- <span data-ttu-id="35823-237">提交 CFDI 发票。</span><span class="sxs-lookup"><span data-stu-id="35823-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="35823-238">查看提交执行日志。</span><span class="sxs-lookup"><span data-stu-id="35823-238">View the submission execution logs.</span></span>
- <span data-ttu-id="35823-239">提交 CFDI 发票的取消。</span><span class="sxs-lookup"><span data-stu-id="35823-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="35823-240">提交 CFDI 发票</span><span class="sxs-lookup"><span data-stu-id="35823-240">Submit CFDI invoices</span></span>

<span data-ttu-id="35823-241">打开 **可配置电子开票集成** 功能后，将不再使用用于提交 CFDI 发票的 **导出/导入电子发票** 流程（**应收帐款 \> 发票 \> 电子发票**）。</span><span class="sxs-lookup"><span data-stu-id="35823-241">After you turn on the **Configurable Electronic invoicing integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="35823-242">取而代之的是一个名为 **提交电子单据** 的新流程。</span><span class="sxs-lookup"><span data-stu-id="35823-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="35823-243">在使用新的 **提交电子单据** 流程前，请验证墨西哥电子发票所需的设置已完成。</span><span class="sxs-lookup"><span data-stu-id="35823-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="35823-244">有关详细信息，请参阅 [CFDI 布局版本 3.3](./latam-mex-cfdi-3-3.md)。</span><span class="sxs-lookup"><span data-stu-id="35823-244">For more information, see [CFDI layout version 3.3](./latam-mex-cfdi-3-3.md).</span></span>

1. <span data-ttu-id="35823-245">转到 **组织管理 \> 定期 \> 电子单据 \> 提交电子单据**。</span><span class="sxs-lookup"><span data-stu-id="35823-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="35823-246">对于任何文档的首次提交，请始终将 **重新提交文档** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="35823-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="35823-247">如果必须通过服务重新提交文档，请将此选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="35823-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="35823-248">在 **要包括的记录** 快速选项卡上，选择 **筛选** 打开 **查询** 对话框，您可以在其中构建查询来选择要提交的文档。</span><span class="sxs-lookup"><span data-stu-id="35823-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![提交 CFDI 文档](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="35823-250">在首次尝试通过服务提交单据时，系统会提示您确认与电子开票的连接。</span><span class="sxs-lookup"><span data-stu-id="35823-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="35823-251">选择 **单击此处连接到电子单据提交服务**。</span><span class="sxs-lookup"><span data-stu-id="35823-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="35823-252">查看提交日志</span><span class="sxs-lookup"><span data-stu-id="35823-252">View submission logs</span></span>

<span data-ttu-id="35823-253">您可以查看所有已提交文档或仅一个已提交文档的提交日志。</span><span class="sxs-lookup"><span data-stu-id="35823-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="35823-254">查看所有提交日志</span><span class="sxs-lookup"><span data-stu-id="35823-254">View all submission logs</span></span>

<span data-ttu-id="35823-255">打开 **可配置电子开票集成** 功能后，将出现一个新页面，可让您跟进单据提交流程。</span><span class="sxs-lookup"><span data-stu-id="35823-255">After you turn on the **Configurable Electronic invoicing integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="35823-256">您可以使用此页面查看所有已提交文档的提交日志。</span><span class="sxs-lookup"><span data-stu-id="35823-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="35823-257">转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。</span><span class="sxs-lookup"><span data-stu-id="35823-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="35823-258">在 **文档类型** 字段中，选择 **客户发票日记帐** 筛选所需的电子单据。</span><span class="sxs-lookup"><span data-stu-id="35823-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![选择文档类型以查看提交日志](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="35823-260">在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。</span><span class="sxs-lookup"><span data-stu-id="35823-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![查看提交日志详细信息](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="35823-262">提交日志中的信息划分到三个快速选项卡：</span><span class="sxs-lookup"><span data-stu-id="35823-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="35823-263">**处理操作** – 此快速选项卡显示在 RCS 中设置的功能版本中配置的操作的执行日志。</span><span class="sxs-lookup"><span data-stu-id="35823-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="35823-264">**状态** 列显示操作是否成功运行。</span><span class="sxs-lookup"><span data-stu-id="35823-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="35823-265">**操作文件** – 此快速选项卡显示在执行操作期间生成的中间文件。</span><span class="sxs-lookup"><span data-stu-id="35823-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="35823-266">您可以选择 **查看** 下载和查看文件。</span><span class="sxs-lookup"><span data-stu-id="35823-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="35823-267">**处理操作日志** – 此快速选项卡显示电子开票与目标 Web 服务之间的通信结果。</span><span class="sxs-lookup"><span data-stu-id="35823-267">**Processing action log** – This FastTab shows the results of the communication between Electronic invoicing and the target web service.</span></span> <span data-ttu-id="35823-268">另外还显示 Web 服务的处理返回的内容。</span><span class="sxs-lookup"><span data-stu-id="35823-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="35823-269">**错误代码** 列显示授权 Web 服务返回的返回代码。</span><span class="sxs-lookup"><span data-stu-id="35823-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="35823-270">授权所提交的 CFDI 发票后，其状态将更新为 **已批准**。</span><span class="sxs-lookup"><span data-stu-id="35823-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="35823-271">查看 CFDI 发票的提交日志</span><span class="sxs-lookup"><span data-stu-id="35823-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="35823-272">打开 **可配置电子开票集成** 功能后，您还可以查看 CFDI 发票的提交日志。</span><span class="sxs-lookup"><span data-stu-id="35823-272">After you turn on the **ConfigurableElectronic invoicing integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="35823-273">转到 **应收帐款 \> 查询与报表 \> CFDI（电子发票）**。</span><span class="sxs-lookup"><span data-stu-id="35823-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="35823-274">选择打开 **可配置电子开票集成** 功能后提交的 CFDI 发票。</span><span class="sxs-lookup"><span data-stu-id="35823-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>
3. <span data-ttu-id="35823-275">在操作窗格上的 **历史记录** 选项卡中，选择 **电子单据日志**。</span><span class="sxs-lookup"><span data-stu-id="35823-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![查看 CFDI 发票的提交日志](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="35823-277">对于在打开 **可配置电子开票集成** 功能之前提交的 CFDI 发票，**历史记录** 按钮可用。</span><span class="sxs-lookup"><span data-stu-id="35823-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="35823-278">对于在打开 **可配置电子开票集成** 功能之后提交的 CFDI 发票，**历史记录** 按钮不可用。</span><span class="sxs-lookup"><span data-stu-id="35823-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="35823-279">提交 CFDI 发票的取消</span><span class="sxs-lookup"><span data-stu-id="35823-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="35823-280">打开 **可配置电子开票集成** 功能后，不再使用旧的取消 CFDI 发票流程。</span><span class="sxs-lookup"><span data-stu-id="35823-280">After you turn on the **Configurable Electronic invoicing integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="35823-281">取而代之的是嵌入在 **电子单据提交日志** 页上的新取消流程。</span><span class="sxs-lookup"><span data-stu-id="35823-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="35823-282">转到 **应收帐款 \> 查询与报表 \> CFDI（电子发票）**。</span><span class="sxs-lookup"><span data-stu-id="35823-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="35823-283">如果 CFDI 发票的状态为 **已批准**，选择 **功能 \> 取消 CFDI**。</span><span class="sxs-lookup"><span data-stu-id="35823-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="35823-284">转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。</span><span class="sxs-lookup"><span data-stu-id="35823-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="35823-285">选择 CFDI 发票，然后选择 **功能 \> 发送相关提交**。</span><span class="sxs-lookup"><span data-stu-id="35823-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="35823-286">为相关提交输入描述，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="35823-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="35823-287">查看取消提交日志</span><span class="sxs-lookup"><span data-stu-id="35823-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="35823-288">转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志**。</span><span class="sxs-lookup"><span data-stu-id="35823-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="35823-289">在 **文档类型** 字段中，选择 **客户发票日记帐** 仅筛选出客户发票日记帐单据。</span><span class="sxs-lookup"><span data-stu-id="35823-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="35823-290">选择 CFDI 发票，然后在操作窗格上，选择 **查询 \> 相关提交**。</span><span class="sxs-lookup"><span data-stu-id="35823-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="35823-291">**相关提交** 页显示给定 CFDI 发票的所有相关提交及其提交状态。</span><span class="sxs-lookup"><span data-stu-id="35823-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="35823-292">在下图中，第一行表示请求审批 CFDI 发票的提交。</span><span class="sxs-lookup"><span data-stu-id="35823-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="35823-293">第二行表示取消该 CFDI 发票的提交。</span><span class="sxs-lookup"><span data-stu-id="35823-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![查看取消提交日志](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="35823-295">在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。</span><span class="sxs-lookup"><span data-stu-id="35823-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![查看取消提交日志详细信息](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="35823-297">隐私声明</span><span class="sxs-lookup"><span data-stu-id="35823-297">Privacy notice</span></span>
<span data-ttu-id="35823-298">启用 **CFDI 墨西哥电子发票 (MX)** 功能可能需要发送有限的数据，其中包括组织税务登记 ID。</span><span class="sxs-lookup"><span data-stu-id="35823-298">Enabling the **CFDI Mexican electronic invoice (MX)** feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="35823-299">这将被传输到税务机构授权的第三方机构，以便以与政府的 Web 服务集成所需的预定义格式向该税务机构发送电子发票。</span><span class="sxs-lookup"><span data-stu-id="35823-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="35823-300">管理员可以通过导航到 **组织管理 \> 设置 \> 电子单据参数** 来启用和禁用 **CFDI 墨西哥电子发票 (MX)** 功能。</span><span class="sxs-lookup"><span data-stu-id="35823-300">An administrator can enable and disable the **CFDI Mexican electronic invoice (MX)** feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="35823-301">选择 **功能** 选项卡，选择包含 **CFDI 墨西哥电子发票 (MX)** 功能的行，然后进行适当的选择。</span><span class="sxs-lookup"><span data-stu-id="35823-301">Select the **Features** tab, select the rows containing the **CFDI Mexican electronic invoice (MX)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="35823-302">从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。</span><span class="sxs-lookup"><span data-stu-id="35823-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="35823-303">有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。</span><span class="sxs-lookup"><span data-stu-id="35823-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35823-304">其他资源</span><span class="sxs-lookup"><span data-stu-id="35823-304">Additional resources</span></span>

- [<span data-ttu-id="35823-305">电子开票概览</span><span class="sxs-lookup"><span data-stu-id="35823-305">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="35823-306">开始使用电子开票</span><span class="sxs-lookup"><span data-stu-id="35823-306">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="35823-307">设置电子开票</span><span class="sxs-lookup"><span data-stu-id="35823-307">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]