---
title: 为 Dynamics 365 Commerce 评估环境配置可选功能
description: 本主题说明如何为 Microsoft Dynamics 365 Commerce 评估环境配置可选功能。
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6639de250557ce9a25fc2cde3807abf64b0ddc18
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993442"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="8ef6a-103">为 Dynamics 365 Commerce 评估环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="8ef6a-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ef6a-104">本主题说明如何为 Microsoft Dynamics 365 Commerce 评估环境配置可选功能。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8ef6a-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="8ef6a-105">Prerequisites</span></span>

<span data-ttu-id="8ef6a-106">如果要评估交易电子邮件功能，必须满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="8ef6a-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="8ef6a-107">您有可用的电子邮件服务器（简单邮件传输协议 \[SMTP\] 服务器），可从 Microsoft Azure 订阅（在其中预配了评估环境）使用该服务器。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="8ef6a-108">您有该服务器的完全限定域名 (FQDN)/IP 地址、SMTP 端口号和身份验证详细信息。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="8ef6a-109">配置图像后端</span><span class="sxs-lookup"><span data-stu-id="8ef6a-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="8ef6a-110">查找您的媒体基 URL</span><span class="sxs-lookup"><span data-stu-id="8ef6a-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="8ef6a-111">您必须先完成[在 Commerce 中设置您的站点](cpe-post-provisioning.md#set-up-your-site-in-commerce)中的步骤，然后才能完成此过程。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="8ef6a-112">使用您在预配期间初始化电子商务时记下的 URL 登录 Commerce 站点构建器（请参阅[初始化电子商务](provisioning-guide.md#initialize-e-commerce)）。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="8ef6a-113">打开 **Fabrikam** 站点。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="8ef6a-114">在左侧菜单中，选择 **媒体库**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="8ef6a-115">选择任何单个图像资产。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-115">Select any single image asset.</span></span>
1. <span data-ttu-id="8ef6a-116">在右侧的属性检查器中，找到 **公共 URL** 属性。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="8ef6a-117">此值是一个 URL。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-117">The value is a URL.</span></span> <span data-ttu-id="8ef6a-118">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="8ef6a-118">Here is an example:</span></span>

    <span data-ttu-id="8ef6a-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="8ef6a-120">将 URL 中的最后一个标识符（前面示例中为 **MA1nQC**）替换为字符串 **search?fileName=**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="8ef6a-121">进行此更改后，示例 URL 如下所示：</span><span class="sxs-lookup"><span data-stu-id="8ef6a-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="8ef6a-122">此 URL 是您的媒体基 URL。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-122">This URL is your media base URL.</span></span> <span data-ttu-id="8ef6a-123">请记下它。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="8ef6a-124">更新媒体基 URL</span><span class="sxs-lookup"><span data-stu-id="8ef6a-124">Update the media base URL</span></span>

1. <span data-ttu-id="8ef6a-125">登录 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="8ef6a-126">使用左侧菜单转到 **模块 \> Retail 和 Commerce \> 渠道设置 \> 渠道配置文件**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="8ef6a-127">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-127">Select **Edit**.</span></span>
1. <span data-ttu-id="8ef6a-128">在 **配置文件属性** 下，将 **媒体服务器基 URL** 属性的值替换为您前面创建的媒体基 URL。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="8ef6a-129">选择名为 **scXXXXXXXXX** 的渠道。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="8ef6a-130">在 **配置文件属性** 下，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="8ef6a-131">对于添加的属性，选择 **媒体服务器基 URL** 作为属性键。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="8ef6a-132">作为属性值，输入您先前创建的媒体基 URL。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="8ef6a-133">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="8ef6a-134">配置和测试电子邮件服务器</span><span class="sxs-lookup"><span data-stu-id="8ef6a-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="8ef6a-135">必须可从您用于环境的 Azure 订阅访问您在此处输入的 SMTP 服务器或电子邮件服务。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="8ef6a-136">登录 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="8ef6a-137">使用左侧菜单转到 **模块 \> Retail 和 Commerce \> Headquarters 设置 \> 参数 \> 电子邮件参数**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="8ef6a-138">在 **SMTP 设置** 选项卡上，在 **出站邮件服务器** 字段中，输入您的 SMTP 服务器或电子邮件服务的 FQDN 或 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="8ef6a-139">在 **SMTP 端口号** 字段中，输入端口号。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="8ef6a-140">（如果您使用的不是安全套接字层 \[SSL\]，默认端口号是 **25**。）</span><span class="sxs-lookup"><span data-stu-id="8ef6a-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="8ef6a-141">如果需要验证，请在 **用户名** 和 **密码** 字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="8ef6a-142">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-142">Select **Save**.</span></span>
1. <span data-ttu-id="8ef6a-143">选择 **刷新**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="8ef6a-144">在 **测试电子邮件** 选项卡上，在 **电子邮件提供程序** 字段中，选择 **SMTP**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="8ef6a-145">在 **发送到** 字段中，输入要测试电子邮件应发送到的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="8ef6a-146">选择 **发送测试电子邮件**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="8ef6a-147">配置电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="8ef6a-147">Configure email templates</span></span>

<span data-ttu-id="8ef6a-148">对于要为其发送电子邮件的每个交易事件，必须使用有效的发件人电子邮件地址更新电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="8ef6a-149">登录 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="8ef6a-150">使用左侧菜单转到 **模块 \> Retail 和 Commerce \> Headquarters 设置 \> 参数 \> 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="8ef6a-151">选择 **显示列表**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-151">Select **Show list**.</span></span>
1. <span data-ttu-id="8ef6a-152">对于列表中的每个模板，请执行这些步骤：</span><span class="sxs-lookup"><span data-stu-id="8ef6a-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="8ef6a-153">在 **发件人电子邮件** 字段中，输入发件人电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="8ef6a-154">可选：在 **发件人名称** 字段中，输入应用作发件人名称的名称。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="8ef6a-155">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="8ef6a-156">自定义电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="8ef6a-156">Customize email templates</span></span>

<span data-ttu-id="8ef6a-157">您可能希望自定义电子邮件模板，让它们使用不同的图像。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="8ef6a-158">或者，您可能想要更新模板中的链接，使其转到您的评估环境。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="8ef6a-159">此过程说明如何下载默认模板，自定义默认模板和更新系统中的模板。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="8ef6a-160">在 Web 浏览器中，将 [Microsoft Dynamics 365 Commerce 评估默认电子邮件模板 .zip 文件](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip)下载到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="8ef6a-161">此文件包含以下 HTML 文档：</span><span class="sxs-lookup"><span data-stu-id="8ef6a-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="8ef6a-162">订单确认模板</span><span class="sxs-lookup"><span data-stu-id="8ef6a-162">Order confirmation template</span></span>
    - <span data-ttu-id="8ef6a-163">颁发礼品卡模板</span><span class="sxs-lookup"><span data-stu-id="8ef6a-163">Issue gift card template</span></span>
    - <span data-ttu-id="8ef6a-164">新订单模板</span><span class="sxs-lookup"><span data-stu-id="8ef6a-164">New order template</span></span>
    - <span data-ttu-id="8ef6a-165">打包订单模板</span><span class="sxs-lookup"><span data-stu-id="8ef6a-165">Pack order template</span></span>
    - <span data-ttu-id="8ef6a-166">选择订单模板</span><span class="sxs-lookup"><span data-stu-id="8ef6a-166">Pick order template</span></span>

1. <span data-ttu-id="8ef6a-167">使用文本编辑器或 HTML 编辑器自定义模板。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="8ef6a-168">请参阅本主题后面的[支持的标志](#supported-tokens-in-the-email-template)列表。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="8ef6a-169">登录 Commerce。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="8ef6a-170">使用左侧菜单转到 **模块 \> 组织管理 \> 设置 \> 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="8ef6a-171">展开左侧列表查看所有模板。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="8ef6a-172">对于您要自定义的每个模板，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="8ef6a-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="8ef6a-173">在列表中选择模板。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="8ef6a-174">在 **电子邮件内容** 下，在列表中选择相应语言版本。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="8ef6a-175">（默认语言为 **en-us**。）</span><span class="sxs-lookup"><span data-stu-id="8ef6a-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="8ef6a-176">在 **电子邮件内容** 下，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="8ef6a-177">**上载电子邮件模板** 窗格将出现。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="8ef6a-178">选择 **浏览**，找到具有自定义内容的 HTML 文件。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="8ef6a-179">选择 **上载**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-179">Select **Upload**.</span></span> <span data-ttu-id="8ef6a-180">您的模板将上载到系统，并显示预览。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="8ef6a-181">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-181">Select **OK**.</span></span>
    1. <span data-ttu-id="8ef6a-182">可选：自定义模板的 **主题** 属性。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="8ef6a-183">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="8ef6a-184">电子邮件模板中支持的令牌</span><span class="sxs-lookup"><span data-stu-id="8ef6a-184">Supported tokens in the email template</span></span>

<span data-ttu-id="8ef6a-185">呈现电子邮件时，这些标志将替换为应用于客户和客户订单的实际值。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="8ef6a-186">销售订单</span><span class="sxs-lookup"><span data-stu-id="8ef6a-186">Sales order</span></span>

<span data-ttu-id="8ef6a-187">以下标志应用于整个销售订单。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="8ef6a-188">令牌的名称</span><span class="sxs-lookup"><span data-stu-id="8ef6a-188">Name of the token</span></span> | <span data-ttu-id="8ef6a-189">标志</span><span class="sxs-lookup"><span data-stu-id="8ef6a-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="8ef6a-190">转移单编号</span><span class="sxs-lookup"><span data-stu-id="8ef6a-190">Order number</span></span>      | <span data-ttu-id="8ef6a-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-191">%salesid%</span></span> |
| <span data-ttu-id="8ef6a-192">客户名称</span><span class="sxs-lookup"><span data-stu-id="8ef6a-192">Customer's name</span></span>   | <span data-ttu-id="8ef6a-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-193">%customername%</span></span> |
| <span data-ttu-id="8ef6a-194">交货地址</span><span class="sxs-lookup"><span data-stu-id="8ef6a-194">Delivery address</span></span>  | <span data-ttu-id="8ef6a-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="8ef6a-196">帐单地址</span><span class="sxs-lookup"><span data-stu-id="8ef6a-196">Billing address</span></span>   | <span data-ttu-id="8ef6a-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-197">%customeraddress%</span></span> |
| <span data-ttu-id="8ef6a-198">订货日期</span><span class="sxs-lookup"><span data-stu-id="8ef6a-198">Order date</span></span>        | <span data-ttu-id="8ef6a-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-199">%shipdate%</span></span> |
| <span data-ttu-id="8ef6a-200">传递模式</span><span class="sxs-lookup"><span data-stu-id="8ef6a-200">Delivery mode</span></span>     | <span data-ttu-id="8ef6a-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="8ef6a-202">折扣</span><span class="sxs-lookup"><span data-stu-id="8ef6a-202">Discount</span></span>          | <span data-ttu-id="8ef6a-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-203">%discount%</span></span> |
| <span data-ttu-id="8ef6a-204">销售税</span><span class="sxs-lookup"><span data-stu-id="8ef6a-204">Sales tax</span></span>         | <span data-ttu-id="8ef6a-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-205">%tax%</span></span> |
| <span data-ttu-id="8ef6a-206">订单合计</span><span class="sxs-lookup"><span data-stu-id="8ef6a-206">Order total</span></span>       | <span data-ttu-id="8ef6a-207">%total%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="8ef6a-208">销售行</span><span class="sxs-lookup"><span data-stu-id="8ef6a-208">Sales line</span></span>

<span data-ttu-id="8ef6a-209">以下标志由订单中每个产品的值替换。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="8ef6a-210">将 **产品列表 - 开始** 标志放在对每个产品重复的 HTML 块的开头，并将 **产品列表 - 结束** 标志放在块的末尾。</span><span class="sxs-lookup"><span data-stu-id="8ef6a-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="8ef6a-211">令牌的名称</span><span class="sxs-lookup"><span data-stu-id="8ef6a-211">Name of the token</span></span>      | <span data-ttu-id="8ef6a-212">标志</span><span class="sxs-lookup"><span data-stu-id="8ef6a-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="8ef6a-213">产品列表 - 开始</span><span class="sxs-lookup"><span data-stu-id="8ef6a-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="8ef6a-214">产品列表 - 结束</span><span class="sxs-lookup"><span data-stu-id="8ef6a-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="8ef6a-215">产品名称</span><span class="sxs-lookup"><span data-stu-id="8ef6a-215">Product name</span></span>           | <span data-ttu-id="8ef6a-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-216">%lineproductname%</span></span> |
| <span data-ttu-id="8ef6a-217">说明</span><span class="sxs-lookup"><span data-stu-id="8ef6a-217">Description</span></span>            | <span data-ttu-id="8ef6a-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="8ef6a-219">数量</span><span class="sxs-lookup"><span data-stu-id="8ef6a-219">Quantity</span></span>               | <span data-ttu-id="8ef6a-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-220">%linequantity%</span></span> |
| <span data-ttu-id="8ef6a-221">行单价</span><span class="sxs-lookup"><span data-stu-id="8ef6a-221">Line unit price</span></span>        | <span data-ttu-id="8ef6a-222">%lineprice%（验证）</span><span class="sxs-lookup"><span data-stu-id="8ef6a-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="8ef6a-223">行项总数</span><span class="sxs-lookup"><span data-stu-id="8ef6a-223">line item total</span></span>        | <span data-ttu-id="8ef6a-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-224">%linenetamount%</span></span> |
| <span data-ttu-id="8ef6a-225">行折扣</span><span class="sxs-lookup"><span data-stu-id="8ef6a-225">line discount</span></span>          | <span data-ttu-id="8ef6a-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-226">%linediscount%</span></span> |
| <span data-ttu-id="8ef6a-227">装运日期</span><span class="sxs-lookup"><span data-stu-id="8ef6a-227">Ship date</span></span>              | <span data-ttu-id="8ef6a-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-228">%lineshipdate%</span></span> |
| <span data-ttu-id="8ef6a-229">采购方法</span><span class="sxs-lookup"><span data-stu-id="8ef6a-229">Procurement method</span></span>     | <span data-ttu-id="8ef6a-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="8ef6a-231">delivery address / 交货地址</span><span class="sxs-lookup"><span data-stu-id="8ef6a-231">delivery address</span></span>       | <span data-ttu-id="8ef6a-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="8ef6a-233">行的销售单位</span><span class="sxs-lookup"><span data-stu-id="8ef6a-233">Sales unit of the line</span></span> | <span data-ttu-id="8ef6a-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="8ef6a-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="8ef6a-235">其他资源</span><span class="sxs-lookup"><span data-stu-id="8ef6a-235">Additional resources</span></span>

[<span data-ttu-id="8ef6a-236">Dynamics 365 Commerce 评估环境概览</span><span class="sxs-lookup"><span data-stu-id="8ef6a-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="8ef6a-237">预配 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="8ef6a-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="8ef6a-238">配置 Dynamics 365 Commerce 评估环境</span><span class="sxs-lookup"><span data-stu-id="8ef6a-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="8ef6a-239">在 Dynamics 365 Commerce 评估环境中配置 BOPIS</span><span class="sxs-lookup"><span data-stu-id="8ef6a-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="8ef6a-240">Dynamics 365 Commerce 评估环境常见问题</span><span class="sxs-lookup"><span data-stu-id="8ef6a-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="8ef6a-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8ef6a-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="8ef6a-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="8ef6a-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="8ef6a-243">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="8ef6a-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="8ef6a-244">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="8ef6a-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
