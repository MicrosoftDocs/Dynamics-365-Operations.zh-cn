---
title: 为 Commerce 预览环境配置可选功能
description: 本主题说明如何为 Microsoft Dynamics 365 Commerce 预览环境配置可选功能。
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2c4872cdebc414eaa865af025237bd9e1d14bfd2
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906108"
---
# <a name="configure-optional-features-for-a-commerce-preview-environment"></a><span data-ttu-id="afee2-103">为 Commerce 预览环境配置可选功能</span><span class="sxs-lookup"><span data-stu-id="afee2-103">Configure optional features for a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="afee2-104">本主题说明如何为 Microsoft Dynamics 365 Commerce 预览环境配置可选功能。</span><span class="sxs-lookup"><span data-stu-id="afee2-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="afee2-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="afee2-105">Prerequisites</span></span>

<span data-ttu-id="afee2-106">如果要评估交易电子邮件功能，必须满足以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="afee2-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="afee2-107">您有可用的电子邮件服务器（简单邮件传输协议 \[SMTP\] 服务器），可从 Microsoft Azure 订阅（在其中预配了预览环境）使用该服务器。</span><span class="sxs-lookup"><span data-stu-id="afee2-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="afee2-108">您有该服务器的完全限定域名 (FQDN)/IP 地址、SMTP 端口号和身份验证详细信息。</span><span class="sxs-lookup"><span data-stu-id="afee2-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="afee2-109">如果要通过摄取新的全渠道图像来评估数字资产管理功能，您必须具有可用的内容管理系统 (CMS) 租户的名称。</span><span class="sxs-lookup"><span data-stu-id="afee2-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="afee2-110">本主题后面将提供了查找此名称的说明。</span><span class="sxs-lookup"><span data-stu-id="afee2-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="afee2-111">>>>（问：哪里有说明？）</span><span class="sxs-lookup"><span data-stu-id="afee2-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="afee2-112">配置图像后端</span><span class="sxs-lookup"><span data-stu-id="afee2-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="afee2-113">查找您的媒体基 URL</span><span class="sxs-lookup"><span data-stu-id="afee2-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="afee2-114">您必须先完成[在 Commerce 中设置您的站点](cpe-post-provisioning.md#set-up-your-site-in-commerce)中的步骤，然后才能完成此过程。</span><span class="sxs-lookup"><span data-stu-id="afee2-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="afee2-115">使用您在预配期间初始化电子商务时记下的 URL 登录 Commerce 站点管理工具（请参阅[初始化电子商务](provisioning-guide.md#initialize-e-commerce)）。</span><span class="sxs-lookup"><span data-stu-id="afee2-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="afee2-116">打开 **Fabrikam** 站点。</span><span class="sxs-lookup"><span data-stu-id="afee2-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="afee2-117">在左侧菜单中，选择**资产**。</span><span class="sxs-lookup"><span data-stu-id="afee2-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="afee2-118">选择任何单个图像资产。</span><span class="sxs-lookup"><span data-stu-id="afee2-118">Select any single image asset.</span></span>
1. <span data-ttu-id="afee2-119">在右侧的属性检查器中，找到**公共 URL** 属性。</span><span class="sxs-lookup"><span data-stu-id="afee2-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="afee2-120">此值是一个 URL。</span><span class="sxs-lookup"><span data-stu-id="afee2-120">The value is a URL.</span></span> <span data-ttu-id="afee2-121">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="afee2-121">Here is an example:</span></span>

    <span data-ttu-id="afee2-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`。</span><span class="sxs-lookup"><span data-stu-id="afee2-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="afee2-123">将 URL 中的最后一个标识符（前面示例中为 **MA1nQC**）替换为字符串 **search?fileName=**。</span><span class="sxs-lookup"><span data-stu-id="afee2-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="afee2-124">进行此更改后，示例 URL 如下所示：</span><span class="sxs-lookup"><span data-stu-id="afee2-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="afee2-125">此 URL 是您的媒体基 URL。</span><span class="sxs-lookup"><span data-stu-id="afee2-125">This URL is your media base URL.</span></span> <span data-ttu-id="afee2-126">请记下它。</span><span class="sxs-lookup"><span data-stu-id="afee2-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="afee2-127">更新媒体基 URL</span><span class="sxs-lookup"><span data-stu-id="afee2-127">Update the media base URL</span></span>

1. <span data-ttu-id="afee2-128">登录 Dynamics 365 Retail。</span><span class="sxs-lookup"><span data-stu-id="afee2-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="afee2-129">使用左侧菜单转到**模块 \> Retail \> 渠道设置 \> 渠道配置文件**。</span><span class="sxs-lookup"><span data-stu-id="afee2-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="afee2-130">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="afee2-130">Select **Edit**.</span></span>
1. <span data-ttu-id="afee2-131">在**配置文件属性**下，将**媒体服务器基 URL** 属性的值替换为您前面创建的媒体基 URL。</span><span class="sxs-lookup"><span data-stu-id="afee2-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="afee2-132">在左侧列表中，在**默认**渠道下，选择另一个渠道。</span><span class="sxs-lookup"><span data-stu-id="afee2-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="afee2-133">在**配置文件属性**下，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="afee2-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="afee2-134">对于添加的属性，选择**媒体服务器基 URL** 作为属性键。</span><span class="sxs-lookup"><span data-stu-id="afee2-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="afee2-135">作为属性值，输入您先前创建的媒体基 URL。</span><span class="sxs-lookup"><span data-stu-id="afee2-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="afee2-136">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="afee2-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="afee2-137">配置电子邮件服务器</span><span class="sxs-lookup"><span data-stu-id="afee2-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="afee2-138">必须可从您用于环境的 Azure 订阅访问您在此处输入的 SMTP 服务器或电子邮件服务。</span><span class="sxs-lookup"><span data-stu-id="afee2-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="afee2-139">登录 Retail。</span><span class="sxs-lookup"><span data-stu-id="afee2-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="afee2-140">使用左侧菜单转到**模块 \> 系统管理 \> 设置 \> 电子邮件 \> 电子邮件参数**。</span><span class="sxs-lookup"><span data-stu-id="afee2-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="afee2-141">在 **SMTP 设置**选项卡上，在**出站邮件服务器**字段中，输入您的 SMTP 服务器或电子邮件服务的 FQDN 或 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="afee2-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="afee2-142">在 **SMTP 端口号**字段中，输入端口号。</span><span class="sxs-lookup"><span data-stu-id="afee2-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="afee2-143">（如果您使用的不是安全套接字层 \[SSL\]，默认端口号是 **25**。）</span><span class="sxs-lookup"><span data-stu-id="afee2-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="afee2-144">如果需要验证，请在**用户名**和**密码**字段中输入值。</span><span class="sxs-lookup"><span data-stu-id="afee2-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="afee2-145">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="afee2-145">Select **Save**.</span></span>
1. <span data-ttu-id="afee2-146">选择**刷新**。</span><span class="sxs-lookup"><span data-stu-id="afee2-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="afee2-147">在**测试电子邮件**选项卡上，在**电子邮件提供程序**字段中，选择 **SMTP**。</span><span class="sxs-lookup"><span data-stu-id="afee2-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="afee2-148">在**发送到**字段中，输入要测试电子邮件应发送到的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="afee2-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="afee2-149">选择**发送测试电子邮件**。</span><span class="sxs-lookup"><span data-stu-id="afee2-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="afee2-150">配置电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="afee2-150">Configure email templates</span></span>

<span data-ttu-id="afee2-151">对于要为其发送电子邮件的每个交易事件，必须使用有效的发件人电子邮件地址更新电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="afee2-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="afee2-152">登录 Retail。</span><span class="sxs-lookup"><span data-stu-id="afee2-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="afee2-153">使用左侧菜单转到**模块 \> 组织管理 \> 设置 \> 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="afee2-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="afee2-154">选择**显示列表**。</span><span class="sxs-lookup"><span data-stu-id="afee2-154">Select **Show list**.</span></span>
1. <span data-ttu-id="afee2-155">对于列表中的每个模板，请执行这些步骤：</span><span class="sxs-lookup"><span data-stu-id="afee2-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="afee2-156">在**发件人电子邮件**字段中，输入发件人电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="afee2-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="afee2-157">可选：在**发件人名称**字段中，输入应用作发件人名称的名称。</span><span class="sxs-lookup"><span data-stu-id="afee2-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="afee2-158">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="afee2-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="afee2-159">自定义电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="afee2-159">Customize email templates</span></span>

<span data-ttu-id="afee2-160">您可能希望自定义电子邮件模板，让它们使用不同的图像。</span><span class="sxs-lookup"><span data-stu-id="afee2-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="afee2-161">或者，您可能想要更新模板中的链接，使其转到您的预览环境。</span><span class="sxs-lookup"><span data-stu-id="afee2-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="afee2-162">此过程说明如何下载默认模板，自定义默认模板和更新系统中的模板。</span><span class="sxs-lookup"><span data-stu-id="afee2-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="afee2-163">在 Web 浏览器中，将 [Microsoft Dynamics 365 Commerce 预览默认电子邮件模板 .zip 文件](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip)下载到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="afee2-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="afee2-164">此文件包含以下 HTML 文档：</span><span class="sxs-lookup"><span data-stu-id="afee2-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="afee2-165">订单确认模板</span><span class="sxs-lookup"><span data-stu-id="afee2-165">Order confirmation template</span></span>
    - <span data-ttu-id="afee2-166">颁发礼品卡模板</span><span class="sxs-lookup"><span data-stu-id="afee2-166">Issue gift card template</span></span>
    - <span data-ttu-id="afee2-167">新订单模板</span><span class="sxs-lookup"><span data-stu-id="afee2-167">New order template</span></span>
    - <span data-ttu-id="afee2-168">打包订单模板</span><span class="sxs-lookup"><span data-stu-id="afee2-168">Pack order template</span></span>
    - <span data-ttu-id="afee2-169">选择订单模板</span><span class="sxs-lookup"><span data-stu-id="afee2-169">Pick order template</span></span>

1. <span data-ttu-id="afee2-170">使用文本编辑器或 HTML 编辑器自定义模板。</span><span class="sxs-lookup"><span data-stu-id="afee2-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="afee2-171">请参阅本主题后面的[支持的标志](#supported-tokens-in-the-email-template)列表。</span><span class="sxs-lookup"><span data-stu-id="afee2-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="afee2-172">登录 Retail。</span><span class="sxs-lookup"><span data-stu-id="afee2-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="afee2-173">使用左侧菜单转到**模块 \> 组织管理 \> 设置 \> 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="afee2-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="afee2-174">展开左侧列表查看所有模板。</span><span class="sxs-lookup"><span data-stu-id="afee2-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="afee2-175">对于您要自定义的每个模板，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="afee2-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="afee2-176">在列表中选择模板。</span><span class="sxs-lookup"><span data-stu-id="afee2-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="afee2-177">在**电子邮件内容**下，在列表中选择相应语言版本。</span><span class="sxs-lookup"><span data-stu-id="afee2-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="afee2-178">（默认语言为 **en-us**。）</span><span class="sxs-lookup"><span data-stu-id="afee2-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="afee2-179">在**电子邮件内容**下，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="afee2-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="afee2-180">**上载电子邮件模板**窗格将出现。</span><span class="sxs-lookup"><span data-stu-id="afee2-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="afee2-181">选择**浏览**，找到具有自定义内容的 HTML 文件。</span><span class="sxs-lookup"><span data-stu-id="afee2-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="afee2-182">选择**上载**。</span><span class="sxs-lookup"><span data-stu-id="afee2-182">Select **Upload**.</span></span> <span data-ttu-id="afee2-183">您的模板将上载到系统，并显示预览。</span><span class="sxs-lookup"><span data-stu-id="afee2-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="afee2-184">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="afee2-184">Select **OK**.</span></span>
    1. <span data-ttu-id="afee2-185">可选：自定义模板的**主题**属性。</span><span class="sxs-lookup"><span data-stu-id="afee2-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="afee2-186">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="afee2-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="afee2-187">电子邮件模板中支持的令牌</span><span class="sxs-lookup"><span data-stu-id="afee2-187">Supported tokens in the email template</span></span>

<span data-ttu-id="afee2-188">呈现电子邮件时，这些标志将替换为应用于客户和客户订单的实际值。</span><span class="sxs-lookup"><span data-stu-id="afee2-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="afee2-189">销售订单</span><span class="sxs-lookup"><span data-stu-id="afee2-189">Sales order</span></span>

<span data-ttu-id="afee2-190">以下标志应用于整个销售订单。</span><span class="sxs-lookup"><span data-stu-id="afee2-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="afee2-191">令牌的名称</span><span class="sxs-lookup"><span data-stu-id="afee2-191">Name of the token</span></span> | <span data-ttu-id="afee2-192">标志</span><span class="sxs-lookup"><span data-stu-id="afee2-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="afee2-193">转移单编号</span><span class="sxs-lookup"><span data-stu-id="afee2-193">Order number</span></span>      | <span data-ttu-id="afee2-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="afee2-194">%salesid%</span></span> |
| <span data-ttu-id="afee2-195">客户名称</span><span class="sxs-lookup"><span data-stu-id="afee2-195">Customer's name</span></span>   | <span data-ttu-id="afee2-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="afee2-196">%customername%</span></span> |
| <span data-ttu-id="afee2-197">交货地址</span><span class="sxs-lookup"><span data-stu-id="afee2-197">Delivery address</span></span>  | <span data-ttu-id="afee2-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="afee2-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="afee2-199">帐单地址</span><span class="sxs-lookup"><span data-stu-id="afee2-199">Billing address</span></span>   | <span data-ttu-id="afee2-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="afee2-200">%customeraddress%</span></span> |
| <span data-ttu-id="afee2-201">订货日期</span><span class="sxs-lookup"><span data-stu-id="afee2-201">Order date</span></span>        | <span data-ttu-id="afee2-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="afee2-202">%shipdate%</span></span> |
| <span data-ttu-id="afee2-203">传递模式</span><span class="sxs-lookup"><span data-stu-id="afee2-203">Delivery mode</span></span>     | <span data-ttu-id="afee2-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="afee2-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="afee2-205">折扣</span><span class="sxs-lookup"><span data-stu-id="afee2-205">Discount</span></span>          | <span data-ttu-id="afee2-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="afee2-206">%discount%</span></span> |
| <span data-ttu-id="afee2-207">销售税</span><span class="sxs-lookup"><span data-stu-id="afee2-207">Sales tax</span></span>         | <span data-ttu-id="afee2-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="afee2-208">%tax%</span></span> |
| <span data-ttu-id="afee2-209">订单合计</span><span class="sxs-lookup"><span data-stu-id="afee2-209">Order total</span></span>       | <span data-ttu-id="afee2-210">%total%</span><span class="sxs-lookup"><span data-stu-id="afee2-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="afee2-211">销售行</span><span class="sxs-lookup"><span data-stu-id="afee2-211">Sales line</span></span>

<span data-ttu-id="afee2-212">以下标志由订单中每个产品的值替换。</span><span class="sxs-lookup"><span data-stu-id="afee2-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="afee2-213">将**产品列表 - 开始**标志放在对每个产品重复的 HTML 块的开头，并将**产品列表 - 结束**标志放在块的末尾。</span><span class="sxs-lookup"><span data-stu-id="afee2-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="afee2-214">令牌的名称</span><span class="sxs-lookup"><span data-stu-id="afee2-214">Name of the token</span></span>      | <span data-ttu-id="afee2-215">标志</span><span class="sxs-lookup"><span data-stu-id="afee2-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="afee2-216">产品列表 - 开始</span><span class="sxs-lookup"><span data-stu-id="afee2-216">Product list - start</span></span>   | <span data-ttu-id="afee2-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="afee2-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="afee2-218">产品列表 - 结束</span><span class="sxs-lookup"><span data-stu-id="afee2-218">Product list - end</span></span>     | <span data-ttu-id="afee2-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="afee2-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="afee2-220">产品名称</span><span class="sxs-lookup"><span data-stu-id="afee2-220">Product name</span></span>           | <span data-ttu-id="afee2-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="afee2-221">%lineproductname%</span></span> |
| <span data-ttu-id="afee2-222">说明</span><span class="sxs-lookup"><span data-stu-id="afee2-222">Description</span></span>            | <span data-ttu-id="afee2-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="afee2-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="afee2-224">数量</span><span class="sxs-lookup"><span data-stu-id="afee2-224">Quantity</span></span>               | <span data-ttu-id="afee2-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="afee2-225">%linequantity%</span></span> |
| <span data-ttu-id="afee2-226">行单价</span><span class="sxs-lookup"><span data-stu-id="afee2-226">Line unit price</span></span>        | <span data-ttu-id="afee2-227">%lineprice%（验证）</span><span class="sxs-lookup"><span data-stu-id="afee2-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="afee2-228">行项总数</span><span class="sxs-lookup"><span data-stu-id="afee2-228">line item total</span></span>        | <span data-ttu-id="afee2-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="afee2-229">%linenetamount%</span></span> |
| <span data-ttu-id="afee2-230">行折扣</span><span class="sxs-lookup"><span data-stu-id="afee2-230">line discount</span></span>          | <span data-ttu-id="afee2-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="afee2-231">%linediscount%</span></span> |
| <span data-ttu-id="afee2-232">装运日期</span><span class="sxs-lookup"><span data-stu-id="afee2-232">Ship date</span></span>              | <span data-ttu-id="afee2-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="afee2-233">%lineshipdate%</span></span> |
| <span data-ttu-id="afee2-234">采购方法</span><span class="sxs-lookup"><span data-stu-id="afee2-234">Procurement method</span></span>     | <span data-ttu-id="afee2-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="afee2-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="afee2-236">delivery address / 交货地址</span><span class="sxs-lookup"><span data-stu-id="afee2-236">delivery address</span></span>       | <span data-ttu-id="afee2-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="afee2-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="afee2-238">行的销售单位</span><span class="sxs-lookup"><span data-stu-id="afee2-238">Sales unit of the line</span></span> | <span data-ttu-id="afee2-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="afee2-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="afee2-240">其他资源</span><span class="sxs-lookup"><span data-stu-id="afee2-240">Additional resources</span></span>

[<span data-ttu-id="afee2-241">Commerce 预览环境概述</span><span class="sxs-lookup"><span data-stu-id="afee2-241">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="afee2-242">预配 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="afee2-242">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="afee2-243">配置 Commerce 预览环境</span><span class="sxs-lookup"><span data-stu-id="afee2-243">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="afee2-244">Commerce 预览环境常见问题</span><span class="sxs-lookup"><span data-stu-id="afee2-244">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="afee2-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="afee2-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="afee2-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="afee2-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="afee2-247">Microsoft Azure 门户</span><span class="sxs-lookup"><span data-stu-id="afee2-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="afee2-248">Dynamics 365 Commerce 网站</span><span class="sxs-lookup"><span data-stu-id="afee2-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="afee2-249">Dynamics 365 Retail 的帮助资源</span><span class="sxs-lookup"><span data-stu-id="afee2-249">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
