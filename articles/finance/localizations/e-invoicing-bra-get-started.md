---
title: 开始使用适用于巴西的电子开票附加产品
description: 本主题提供的信息将帮助您开始使用 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中适用于巴西的电子开票附加产品。
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: fb3ec2d60875d7a0747d64b397aafaa0a3d26348
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039861"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="346a1-103">开始使用适用于巴西的电子开票附加产品</span><span class="sxs-lookup"><span data-stu-id="346a1-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="346a1-104">适用于巴西的电子开票附加产品当前不支持 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中内置的会计单据集成中提供的所有功能。</span><span class="sxs-lookup"><span data-stu-id="346a1-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="346a1-105">本主题提供的信息将帮助您开始使用适用于巴西的电子开票附加产品。</span><span class="sxs-lookup"><span data-stu-id="346a1-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="346a1-106">指导您完成 Regulatory Configuration Services (RCS) 以及 Finance 和 Supply Chain Management 中与国家/地区相关的配置步骤。</span><span class="sxs-lookup"><span data-stu-id="346a1-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="346a1-107">另外还指导您完成通过服务提交 NF-e 会计单据（电子会计单据模型 55）的流程，并说明如何查看处理结果和会计单据的状态。</span><span class="sxs-lookup"><span data-stu-id="346a1-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="346a1-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="346a1-108">Prerequisites</span></span>

<span data-ttu-id="346a1-109">在完成本主题中的步骤之前，您必须[开始使用电子开票附加产品](e-invoicing-get-started.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="346a1-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="346a1-110">RCS 设置</span><span class="sxs-lookup"><span data-stu-id="346a1-110">RCS setup</span></span>

<span data-ttu-id="346a1-111">在 RCS 设置期间，您将完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="346a1-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="346a1-112">导入 NF-e 会计单据的电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="346a1-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="346a1-113">查看提交 NF-e 会计单据以进行授权所需的文件格式。</span><span class="sxs-lookup"><span data-stu-id="346a1-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="346a1-114">查看请求取消批准的 NF-e 所需的文件格式。</span><span class="sxs-lookup"><span data-stu-id="346a1-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="346a1-115">配置提交 NF-e 会计单据以进行授权所需的事件。</span><span class="sxs-lookup"><span data-stu-id="346a1-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="346a1-116">配置请求取消批准的 NF-e 所需的事件。</span><span class="sxs-lookup"><span data-stu-id="346a1-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="346a1-117">将电子开票功能分配到电子开票附加产品环境。</span><span class="sxs-lookup"><span data-stu-id="346a1-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="346a1-118">发布电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="346a1-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="346a1-119">“电子开票功能”是配置和发布以使用电子开票附加产品服务器的资源的通用名称。</span><span class="sxs-lookup"><span data-stu-id="346a1-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="346a1-120">电子开票功能的设置将使用电子报告 (ER) 配置格式来创建可配置的导出和导入文件，与使用操作和操作流来支持创建可配置规则以发送请求、导入响应和分析响应内容，以及另外一些设置相结合。</span><span class="sxs-lookup"><span data-stu-id="346a1-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="346a1-121">导入电子开票功能</span><span class="sxs-lookup"><span data-stu-id="346a1-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="346a1-122">登录您的 RCS 帐户</span><span class="sxs-lookup"><span data-stu-id="346a1-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="346a1-123">在 **全球化功能** 工作区中，在 **功能** 部分，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="346a1-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="346a1-124">在 **电子开票功能** 页上，选择 **导入** 从全局存储库中导入 NF-e 会计单据电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="346a1-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![“导入”按钮](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="346a1-126">选择 NF-e 会计单据功能，然后选择 **导入** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![导入 NF-e 功能](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="346a1-128">创建新版本的 NF-e 会计单据功能</span><span class="sxs-lookup"><span data-stu-id="346a1-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="346a1-129">在 **电子开票功能** 页上的 **版本** 选项卡上，选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![添加新的电子开票功能版本](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="346a1-131">更新配置版本</span><span class="sxs-lookup"><span data-stu-id="346a1-131">Update the configuration version</span></span>

1. <span data-ttu-id="346a1-132">在 **电子开票功能** 页上的 **配置** 选项卡上，选择 **添加** 或 **删除** 管理配置版本（ER 文件格式配置）。</span><span class="sxs-lookup"><span data-stu-id="346a1-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![管理电子开票功能配置](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="346a1-134">当您创建新版本的 NF-e 会计单据功能时，所有配置版本（ER 文件格式）都将从最新版本继承。</span><span class="sxs-lookup"><span data-stu-id="346a1-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="346a1-135">要提交 NF-e 会计单据以进行授权，需要以下配置版本：</span><span class="sxs-lookup"><span data-stu-id="346a1-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="346a1-136">NFe 提交导出格式</span><span class="sxs-lookup"><span data-stu-id="346a1-136">NFe submit export format</span></span>
        - <span data-ttu-id="346a1-137">NFe 响应消息导入</span><span class="sxs-lookup"><span data-stu-id="346a1-137">NFe response message import</span></span>
        - <span data-ttu-id="346a1-138">NFe 错误日志导入</span><span class="sxs-lookup"><span data-stu-id="346a1-138">NFe error log import</span></span>

    - <span data-ttu-id="346a1-139">要提交 NF-e 取消，需要以下配置版本：</span><span class="sxs-lookup"><span data-stu-id="346a1-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="346a1-140">NFe 取消导出格式</span><span class="sxs-lookup"><span data-stu-id="346a1-140">NFe cancel export format</span></span>

2. <span data-ttu-id="346a1-141">在列表中，选择配置版本，然后选择 **编辑** 或 **查看** 打开 **格式设计器** 页，您可以在其中编辑或查看配置。</span><span class="sxs-lookup"><span data-stu-id="346a1-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![打开“格式设计器”页](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="346a1-143">使用 **格式设计器** 页编辑或查看 ER 格式文件配置。</span><span class="sxs-lookup"><span data-stu-id="346a1-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="346a1-144">有关详细信息，请参阅[创建电子单据配置](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration)。</span><span class="sxs-lookup"><span data-stu-id="346a1-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![“格式设计器”页面](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="346a1-146">管理电子开票功能设置</span><span class="sxs-lookup"><span data-stu-id="346a1-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="346a1-147">在 **电子开票功能** 页上的 **设置** 选项卡上，选择 **添加** 或 **删除** 管理电子开票功能设置（即 NF-e 事件）。</span><span class="sxs-lookup"><span data-stu-id="346a1-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![管理电子开票功能设置](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="346a1-149">当您创建从另一个电子开票功能派生的 NF-e 会计单据功能的新版本时，所有功能设置（NF-e 事件）均从最新版本继承。</span><span class="sxs-lookup"><span data-stu-id="346a1-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="346a1-150">要提交 NF-e 会计单据以进行授权，需要进行 **提交** 功能设置。</span><span class="sxs-lookup"><span data-stu-id="346a1-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="346a1-151">要提交 NF-e 取消，需要进行 **取消** 功能设置。</span><span class="sxs-lookup"><span data-stu-id="346a1-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="346a1-152">配置“提交”功能设置</span><span class="sxs-lookup"><span data-stu-id="346a1-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="346a1-153">在 **电子开票功能** 页上的 **设置** 选项卡上，在 **功能设置** 列中，选择 **提交** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="346a1-154">选择 **编辑** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-154">Select **Edit**.</span></span>

    ![编辑电子开票功能设置](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="346a1-156">在 **功能版本设置** 页上，选择 **操作** 选项卡管理操作列表。</span><span class="sxs-lookup"><span data-stu-id="346a1-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![“操作”选项卡](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="346a1-158">查看提交 NF-e 进行授权所需的操作。</span><span class="sxs-lookup"><span data-stu-id="346a1-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="346a1-159">行动 ID</span><span class="sxs-lookup"><span data-stu-id="346a1-159">Action ID</span></span> | <span data-ttu-id="346a1-160">操作名称</span><span class="sxs-lookup"><span data-stu-id="346a1-160">Action name</span></span>                  | <span data-ttu-id="346a1-161">操作描述</span><span class="sxs-lookup"><span data-stu-id="346a1-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="346a1-162">1</span><span class="sxs-lookup"><span data-stu-id="346a1-162">1</span></span>         | <span data-ttu-id="346a1-163">转换文档</span><span class="sxs-lookup"><span data-stu-id="346a1-163">Transform document</span></span>           | <span data-ttu-id="346a1-164">创建要提交的 NF-e XML 文件。</span><span class="sxs-lookup"><span data-stu-id="346a1-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="346a1-165">2</span><span class="sxs-lookup"><span data-stu-id="346a1-165">2</span></span>         | <span data-ttu-id="346a1-166">对文档签名</span><span class="sxs-lookup"><span data-stu-id="346a1-166">Sign document</span></span>                | <span data-ttu-id="346a1-167">将数字证书应用于 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="346a1-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="346a1-168">3</span><span class="sxs-lookup"><span data-stu-id="346a1-168">3</span></span>         | <span data-ttu-id="346a1-169">调用巴西 SEFAZ 服务</span><span class="sxs-lookup"><span data-stu-id="346a1-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="346a1-170">将签名的 XML 文件提交到 Web 服务以进行授权。</span><span class="sxs-lookup"><span data-stu-id="346a1-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="346a1-171">4</span><span class="sxs-lookup"><span data-stu-id="346a1-171">4</span></span>         | <span data-ttu-id="346a1-172">处理响应</span><span class="sxs-lookup"><span data-stu-id="346a1-172">Process response</span></span>             | <span data-ttu-id="346a1-173">获取 Web 服务响应。</span><span class="sxs-lookup"><span data-stu-id="346a1-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="346a1-174">5</span><span class="sxs-lookup"><span data-stu-id="346a1-174">5</span></span>         | <span data-ttu-id="346a1-175">转换文档</span><span class="sxs-lookup"><span data-stu-id="346a1-175">Transform document</span></span>           | <span data-ttu-id="346a1-176">分析作为响应接收的文件的内容。</span><span class="sxs-lookup"><span data-stu-id="346a1-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="346a1-177">6</span><span class="sxs-lookup"><span data-stu-id="346a1-177">6</span></span>         | <span data-ttu-id="346a1-178">转换文档</span><span class="sxs-lookup"><span data-stu-id="346a1-178">Transform document</span></span>           | <span data-ttu-id="346a1-179">创建 XML 文件来查询提交的状态。</span><span class="sxs-lookup"><span data-stu-id="346a1-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="346a1-180">7</span><span class="sxs-lookup"><span data-stu-id="346a1-180">7</span></span>         | <span data-ttu-id="346a1-181">调用巴西 SEFAZ 服务</span><span class="sxs-lookup"><span data-stu-id="346a1-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="346a1-182">提交请求提交状态的 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="346a1-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="346a1-183">8</span><span class="sxs-lookup"><span data-stu-id="346a1-183">8</span></span>         | <span data-ttu-id="346a1-184">处理响应</span><span class="sxs-lookup"><span data-stu-id="346a1-184">Process response</span></span>             | <span data-ttu-id="346a1-185">获取 Web 服务响应。</span><span class="sxs-lookup"><span data-stu-id="346a1-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="346a1-186">为 SEFAZ Web 服务设置 URL</span><span class="sxs-lookup"><span data-stu-id="346a1-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="346a1-187">在 **功能版本设置** 页上的 **操作** 选项卡上，在 **操作** 快速选项卡上，选择 **调用巴西 SEFAZ 服务** （操作 ID **3** ）。</span><span class="sxs-lookup"><span data-stu-id="346a1-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3** ).</span></span>
2. <span data-ttu-id="346a1-188">在 **参数** 快速选项卡的 **URL 地址参数** 字段中，输入用于 NF-e 提交的 SEFAZ Web 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="346a1-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="346a1-189">在 **操作** 快速选项卡上，选择 **调用巴西 SEFAZ 服务** （操作 ID **7** ）。</span><span class="sxs-lookup"><span data-stu-id="346a1-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7** ).</span></span>
4. <span data-ttu-id="346a1-190">在 **参数** 快速选项卡的 **URL 地址参数** 字段中，输入用于 NF-e 提交的 SEFAZ Web 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="346a1-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="346a1-191">配置“取消”功能设置</span><span class="sxs-lookup"><span data-stu-id="346a1-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="346a1-192">在 **电子开票功能** 页上的 **设置** 选项卡上，在 **功能设置** 列中，选择 **取消** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="346a1-193">选择 **编辑** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-193">Select **Edit**.</span></span>
3. <span data-ttu-id="346a1-194">在 **功能版本设置** 页上，选择 **操作** 选项卡管理操作列表。</span><span class="sxs-lookup"><span data-stu-id="346a1-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="346a1-195">查看请求取消批准的 NF-e 所需的操作。</span><span class="sxs-lookup"><span data-stu-id="346a1-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="346a1-196">行动 ID</span><span class="sxs-lookup"><span data-stu-id="346a1-196">Action ID</span></span> | <span data-ttu-id="346a1-197">操作名称</span><span class="sxs-lookup"><span data-stu-id="346a1-197">Action name</span></span>                  | <span data-ttu-id="346a1-198">操作描述</span><span class="sxs-lookup"><span data-stu-id="346a1-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="346a1-199">1</span><span class="sxs-lookup"><span data-stu-id="346a1-199">1</span></span>         | <span data-ttu-id="346a1-200">转换文档</span><span class="sxs-lookup"><span data-stu-id="346a1-200">Transform document</span></span>           | <span data-ttu-id="346a1-201">创建要提交的 NF-e 取消 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="346a1-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="346a1-202">2</span><span class="sxs-lookup"><span data-stu-id="346a1-202">2</span></span>         | <span data-ttu-id="346a1-203">对文档签名</span><span class="sxs-lookup"><span data-stu-id="346a1-203">Sign document</span></span>                | <span data-ttu-id="346a1-204">将数字证书应用于 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="346a1-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="346a1-205">3</span><span class="sxs-lookup"><span data-stu-id="346a1-205">3</span></span>         | <span data-ttu-id="346a1-206">调用巴西 SEFAZ 服务</span><span class="sxs-lookup"><span data-stu-id="346a1-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="346a1-207">将签名的 XML 文件提交到 Web 服务以取消。</span><span class="sxs-lookup"><span data-stu-id="346a1-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="346a1-208">4</span><span class="sxs-lookup"><span data-stu-id="346a1-208">4</span></span>         | <span data-ttu-id="346a1-209">处理响应</span><span class="sxs-lookup"><span data-stu-id="346a1-209">Process response</span></span>             | <span data-ttu-id="346a1-210">获取 Web 服务响应。</span><span class="sxs-lookup"><span data-stu-id="346a1-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="346a1-211">为 SEFAZ Web 服务设置 URL</span><span class="sxs-lookup"><span data-stu-id="346a1-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="346a1-212">在 **功能版本设置** 页上的 **操作** 选项卡上，在 **操作** 快速选项卡上，选择 **调用巴西 SEFAZ 服务** （操作 ID **3** ）。</span><span class="sxs-lookup"><span data-stu-id="346a1-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3** ).</span></span>
2. <span data-ttu-id="346a1-213">在 **参数** 快速选项卡的 **URL 地址参数** 字段中，输入用于取消批准的 NF-e 的 SEFAZ Web 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="346a1-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="346a1-214">使电子开票环境可用和分配草稿版本</span><span class="sxs-lookup"><span data-stu-id="346a1-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="346a1-215">在 **电子开票功能** 页上的 **环境** 选项卡上，选择 **启用** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="346a1-216">在 **环境** 字段中，选择环境。</span><span class="sxs-lookup"><span data-stu-id="346a1-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="346a1-217">在 **生效开始日期** 字段中，选择环境应该生效的日期。</span><span class="sxs-lookup"><span data-stu-id="346a1-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="346a1-218">选择 **启用** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-218">Select **Enable**.</span></span>

![启用电子开票环境](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="346a1-220">将状态更改为“已完成”</span><span class="sxs-lookup"><span data-stu-id="346a1-220">Change the status to Completed</span></span>

1. <span data-ttu-id="346a1-221">在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **草稿** 的电子开票功能的版本。</span><span class="sxs-lookup"><span data-stu-id="346a1-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="346a1-222">选择 **更改状态 \> 完成** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="346a1-223">将状态更改为“发布”</span><span class="sxs-lookup"><span data-stu-id="346a1-223">Change the status to Publish</span></span>

1. <span data-ttu-id="346a1-224">在 **电子开票功能** 页的 **版本** 选项卡上，选择状态为 **已完成** 的电子开票功能的版本。</span><span class="sxs-lookup"><span data-stu-id="346a1-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="346a1-225">选择 **更改状态 \> 发布** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-225">Select **Change status \> Publish**.</span></span>

![发布电子开票功能](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="346a1-227">在 Finance 或 Supply Chain Management 中设置电子开票附加产品集成</span><span class="sxs-lookup"><span data-stu-id="346a1-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="346a1-228">在设置期间，您将完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="346a1-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="346a1-229">打开适用于巴西的 NF-e 联邦功能。</span><span class="sxs-lookup"><span data-stu-id="346a1-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="346a1-230">导入特定的 ER 数据模型、数据模型映射以及 NF-e 会计单据所需的格式。</span><span class="sxs-lookup"><span data-stu-id="346a1-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="346a1-231">导入 ER 配置，并设置返回提交流程后更新会计单据的状态所需的响应类型。</span><span class="sxs-lookup"><span data-stu-id="346a1-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="346a1-232">打开适用于巴西的 NF-e 联邦功能</span><span class="sxs-lookup"><span data-stu-id="346a1-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="346a1-233">转到 **组织管理 \> 设置 \> 电子单据参数** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="346a1-234">在 **功能** 选项卡上，选中功能引用 **BR00053** 的行中的 **启用** 复选框。</span><span class="sxs-lookup"><span data-stu-id="346a1-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="346a1-235">导入 NF-e 会计单据所需的 ER 数据模型映射</span><span class="sxs-lookup"><span data-stu-id="346a1-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="346a1-236">登录 Finance。</span><span class="sxs-lookup"><span data-stu-id="346a1-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="346a1-237">在 **电子报告** 工作区的 **配置提供程序** 部分，选择 **Microsoft** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="346a1-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="346a1-238">确保此配置提供程序设置为 **有效** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="346a1-239">有关如何将提供程序设置为 **有效** 的信息，请参阅[创建配置提供程序并将其标记为有效](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)。</span><span class="sxs-lookup"><span data-stu-id="346a1-239">For information about how to set a provider to **Active** , see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="346a1-240">选择 **存储库** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="346a1-241">选择 **全局资源 \> 打开** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="346a1-242">导入 **会计单据映射** 配置。</span><span class="sxs-lookup"><span data-stu-id="346a1-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="346a1-243">导入 ER 配置并设置会计单据的响应类型</span><span class="sxs-lookup"><span data-stu-id="346a1-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="346a1-244">在 **电子报告** 工作区的 **配置提供程序** 部分，选择 **Microsoft** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="346a1-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="346a1-245">选择 **存储库** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="346a1-246">选择 **全局资源 \> 打开** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="346a1-247">导入 **NF-e 错误日志导入 (BR)** 、 **NF-e 响应数据导入格式 (BR)** 和 **NF-e 响应消息导入 (BR)** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-247">Import **NF-e error log import (BR)** , **NF-e response data import format (BR)** , and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="346a1-248">转到 **组织管理 \> 设置 \> 电子单据参数** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="346a1-249">在 **电子单据** 选项卡上，选择 **添加** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="346a1-250">在 **表名称** 字段中，输入 **会计单据标题** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="346a1-251">在 **单据上下文** 字段中，选择 **客户发票上下文模型 – 会计单据上下文** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="346a1-252">选择 **响应类型** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-252">Select **Response types**.</span></span>
9. <span data-ttu-id="346a1-253">选择 **新建** ，然后在 **响应类型** 字段中选择 **Response** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-253">Select **New** , and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="346a1-254">在 **提交状态** 字段中，选择 **待处理** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="346a1-255">在 **模型映射** 字段中，选择 **响应消息导入格式 – 来自响应消息的模型映射** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="346a1-256">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-256">Select **Save**.</span></span>
13. <span data-ttu-id="346a1-257">选择 **新建** ，然后在 **响应类型** 字段中输入 **ResponseData** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-257">Select **New** , and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="346a1-258">在 **提交状态** 字段中，选择 **待处理** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="346a1-259">在 **模型映射** 字段中，选择 **NFe 响应数据导入格式 – 响应数据导入** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="346a1-260">选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="346a1-261">电子发票处理</span><span class="sxs-lookup"><span data-stu-id="346a1-261">Electronic invoice processing</span></span>

<span data-ttu-id="346a1-262">在 Finance 中进行处理期间，您将完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="346a1-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="346a1-263">通过电子开票附加产品提交会计单据。</span><span class="sxs-lookup"><span data-stu-id="346a1-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="346a1-264">查看提交执行日志和处理结果。</span><span class="sxs-lookup"><span data-stu-id="346a1-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="346a1-265">通过电子开票附加产品提交会计单据的取消。</span><span class="sxs-lookup"><span data-stu-id="346a1-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="346a1-266">提交 NF-e 会计单据以进行 SEFAZ 授权</span><span class="sxs-lookup"><span data-stu-id="346a1-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="346a1-267">打开 **可配置电子开票附加产品集成** 功能后，将不再使用提交 NF-e 会计单据进行授权的旧流程（ **导出/导入 NF-e 流程** ）。</span><span class="sxs-lookup"><span data-stu-id="346a1-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization ( **Export/Import NF-e process** ) can no longer be used.</span></span> <span data-ttu-id="346a1-268">取而代之的是一个名为 **提交电子单据** 的新流程。</span><span class="sxs-lookup"><span data-stu-id="346a1-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="346a1-269">在继续之前，请确保您有由客户的财务设施签发的一个或多个客户会计单据模型 55。</span><span class="sxs-lookup"><span data-stu-id="346a1-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="346a1-270">这些会计单据的方向必须设置为 **传出** ，状态必须为 **已创建** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-270">The direction for these fiscal documents must be set to **Outgoing** , and the status must be **Created**.</span></span> <span data-ttu-id="346a1-271">有关详细信息，请参阅[签发客户会计单据（巴西）](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document)。</span><span class="sxs-lookup"><span data-stu-id="346a1-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="346a1-272">转到 **组织管理 \> 定期 \> 电子单据 \> 提交电子单据** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="346a1-273">对于任何文档的首次提交，请始终将 **重新提交文档** 选项设置为 **否** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="346a1-274">如果必须通过服务重新提交文档，请将此选项设置为 **是** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="346a1-275">在 **要包括的记录** 快速选项卡上，选择 **筛选** 打开 **查询** 对话框，您可以在其中构建查询来选择要提交的文档。</span><span class="sxs-lookup"><span data-stu-id="346a1-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="346a1-276">在 **范围** 选项卡上，选择 **添加** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="346a1-277">在 **表** 字段中，选择 **会计单据标题** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="346a1-278">在 **派生表** 字段中，选择 **会计单据标题** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="346a1-279">在 **字段** 字段中，选择 **编号** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="346a1-280">在 **条件** 字段中，输入应提交的会计单据的编号。</span><span class="sxs-lookup"><span data-stu-id="346a1-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="346a1-281">单击 **确定** 以关闭 **查询** 对话框。</span><span class="sxs-lookup"><span data-stu-id="346a1-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="346a1-282">选择 **确定** 提交所选文档。</span><span class="sxs-lookup"><span data-stu-id="346a1-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="346a1-283">在首次尝试通过服务提交文档时，系统会提示您确认与电子开票附加产品的连接。</span><span class="sxs-lookup"><span data-stu-id="346a1-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="346a1-284">选择 **单击此处连接到电子单据提交服务** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="346a1-285">查看所有提交日志</span><span class="sxs-lookup"><span data-stu-id="346a1-285">View all submission logs</span></span>

<span data-ttu-id="346a1-286">打开 **可配置电子开票附加产品集成** 功能后，将出现一个新页面，可让您跟进文档提交过程。</span><span class="sxs-lookup"><span data-stu-id="346a1-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="346a1-287">您可以使用此页面查看所有已提交文档的提交日志。</span><span class="sxs-lookup"><span data-stu-id="346a1-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="346a1-288">转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="346a1-289">在 **文档类型** 字段中，选择 **会计单据标题** 仅筛选出会计单据。</span><span class="sxs-lookup"><span data-stu-id="346a1-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="346a1-290">在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。</span><span class="sxs-lookup"><span data-stu-id="346a1-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![查看提交日志详细信息](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="346a1-292">对于 NF-e 会计单据， **错误代码** 列显示 SEFAZ Web 服务返回的返回代码。</span><span class="sxs-lookup"><span data-stu-id="346a1-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="346a1-293">通过会计单据页查看提交日志</span><span class="sxs-lookup"><span data-stu-id="346a1-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="346a1-294">打开 **可配置电子开票附加产品集成** 功能后，您还可以通过会计单据页查看提交日志。</span><span class="sxs-lookup"><span data-stu-id="346a1-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="346a1-295">转到 **总帐 \> 查询和报表 \> 会计单据 \> 所有会计单据** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="346a1-296">选择以前通过电子开票附加产品提交的会计单据。</span><span class="sxs-lookup"><span data-stu-id="346a1-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="346a1-297">在操作窗格上的 **NF-e 联邦** 选项卡中，选择 **电子单据日志** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![从会计单据页查看提交日志](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="346a1-299">提交批准的 NF-e 会计单据以取消 SEFAZ</span><span class="sxs-lookup"><span data-stu-id="346a1-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="346a1-300">打开 **可配置电子开票附加产品集成** 功能后，不能再使用旧的取消 NF-e 会计单据的流程。</span><span class="sxs-lookup"><span data-stu-id="346a1-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="346a1-301">取而代之的是嵌入在 **电子单据提交日志** 页上的新取消流程。</span><span class="sxs-lookup"><span data-stu-id="346a1-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="346a1-302">确保已为批准的 NF-e 会计单据运行了客户会计单据取消。</span><span class="sxs-lookup"><span data-stu-id="346a1-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="346a1-303">有关详细信息，请参阅[取消客户会计单据（巴西）](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents)。</span><span class="sxs-lookup"><span data-stu-id="346a1-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="346a1-304">转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="346a1-305">选择会计单据，然后选择 **功能 \> 发送相关提交** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="346a1-306">为相关提交输入描述，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="346a1-307">查看取消提交日志</span><span class="sxs-lookup"><span data-stu-id="346a1-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="346a1-308">转到 **组织管理 \> 定期 \> 电子单据 \> 电子单据提交日志** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="346a1-309">在 **文档类型** 字段中，选择 **会计单据标题** 仅筛选出会计单据。</span><span class="sxs-lookup"><span data-stu-id="346a1-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="346a1-310">选择会计单据，然后在操作窗格上，选择 **查询 \> 相关提交** 。</span><span class="sxs-lookup"><span data-stu-id="346a1-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="346a1-311">相关提交是与首先进行的主要提交相关的提交。</span><span class="sxs-lookup"><span data-stu-id="346a1-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="346a1-312">例如，授权特定 NF-e 的提交是主要提交。</span><span class="sxs-lookup"><span data-stu-id="346a1-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="346a1-313">请求取消 SEFAZ 中同一个 NF-e 的提交是相关提交。</span><span class="sxs-lookup"><span data-stu-id="346a1-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="346a1-314">此提交之所以存在，只是因为它要请求取消通过另一个提交执行的作业。</span><span class="sxs-lookup"><span data-stu-id="346a1-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="346a1-315">**相关提交** 页显示给定会计单据的所有相关提交及其提交状态。</span><span class="sxs-lookup"><span data-stu-id="346a1-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="346a1-316">在下图中，第一行表示请求审批会计单据的提交。</span><span class="sxs-lookup"><span data-stu-id="346a1-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="346a1-317">第二行表示取消该会计单据的提交。</span><span class="sxs-lookup"><span data-stu-id="346a1-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![查看取消提交日志](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="346a1-319">在操作窗格上，选择 **查询 \> 提交详细信息** 查看提交执行日志的详细信息。</span><span class="sxs-lookup"><span data-stu-id="346a1-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![查看取消提交日志详细信息](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="346a1-321">隐私声明</span><span class="sxs-lookup"><span data-stu-id="346a1-321">Privacy notice</span></span>
<span data-ttu-id="346a1-322">启用 BR-00053（NF-e 联邦）功能可能需要发送有限的数据，其中包括组织税务登记 ID。</span><span class="sxs-lookup"><span data-stu-id="346a1-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="346a1-323">这将被传输到税务机构授权的第三方机构，以便以与政府的 Web 服务集成所需的预定义格式向该税务机构发送电子发票。</span><span class="sxs-lookup"><span data-stu-id="346a1-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="346a1-324">管理员可以通过导航到 **组织管理 \> 设置 \> 电子单据参数** 来启用和禁用 BR-00053（NF-e 联邦）功能。</span><span class="sxs-lookup"><span data-stu-id="346a1-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="346a1-325">选择 **功能** 选项卡，选择包含 BR-00053 功能的行，然后进行适当的选择。</span><span class="sxs-lookup"><span data-stu-id="346a1-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="346a1-326">从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。</span><span class="sxs-lookup"><span data-stu-id="346a1-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="346a1-327">有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。</span><span class="sxs-lookup"><span data-stu-id="346a1-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="346a1-328">其他资源</span><span class="sxs-lookup"><span data-stu-id="346a1-328">Additional resources</span></span>

- [<span data-ttu-id="346a1-329">电子开票附加产品概述</span><span class="sxs-lookup"><span data-stu-id="346a1-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="346a1-330">开始使用电子开票附加产品</span><span class="sxs-lookup"><span data-stu-id="346a1-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="346a1-331">设置电子开票附加产品</span><span class="sxs-lookup"><span data-stu-id="346a1-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
