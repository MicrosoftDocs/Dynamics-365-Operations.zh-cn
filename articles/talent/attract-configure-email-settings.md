---
title: 在 Attract 中配置电子邮件设置
description: 本主题介绍如何为 Microsoft Dynamcis 365 Talent - Attract 发送的电子邮件配置设置。
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c1ebfaeb2e9bc2836bb70e87afa93484c829b6cb
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833107"
---
# <a name="configure-email-settings-in-attract"></a><span data-ttu-id="36f21-103">在 Attract 中配置电子邮件设置</span><span class="sxs-lookup"><span data-stu-id="36f21-103">Configure email settings in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="36f21-104">甚至在应聘者申请您的职位之前，您的品牌就已经树立了信誉，并可以帮助您建立与应聘者之间的关系。</span><span class="sxs-lookup"><span data-stu-id="36f21-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="36f21-105">品牌正面形象会吸引最优秀的人才，并且会提高现有员工的忠诚。</span><span class="sxs-lookup"><span data-stu-id="36f21-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="36f21-106">Microsoft Dynamics 365 Talent: Attract 允许您配置电子邮件，使其体现贵公司的品牌。</span><span class="sxs-lookup"><span data-stu-id="36f21-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="36f21-107">因此，可以为工作应聘者在经历申请流程时提供一致的体验。</span><span class="sxs-lookup"><span data-stu-id="36f21-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="36f21-108">可使用 Attract 执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="36f21-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="36f21-109">配置电子邮件设置，以便使用贵公司的 Microsoft Exchange 电子邮件服务帐户。</span><span class="sxs-lookup"><span data-stu-id="36f21-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="36f21-110">这样，应聘者就会知道电子邮件来自贵公司。</span><span class="sxs-lookup"><span data-stu-id="36f21-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="36f21-111">例如，可配置您的设置，使应聘者收到的电子邮件就会来自 `recruiting@contoso.com`，而不是来自 `contoso@microsoft.com`。</span><span class="sxs-lookup"><span data-stu-id="36f21-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="36f21-112">通过为电子邮件模板设置全局页眉和页脚，为所有电子邮件通信创建一致的品牌。</span><span class="sxs-lookup"><span data-stu-id="36f21-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="36f21-113">要将 Attract 配置为使用贵公司的电子邮件服务帐户发送电子邮件，需要综合招聘加载项。</span><span class="sxs-lookup"><span data-stu-id="36f21-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="36f21-114">连接电子邮件服务帐户</span><span class="sxs-lookup"><span data-stu-id="36f21-114">Connect an email service account</span></span>

<span data-ttu-id="36f21-115">通过连接贵公司的电子邮件服务帐户，可为工作应聘者创建品牌化电子邮件体验。</span><span class="sxs-lookup"><span data-stu-id="36f21-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="36f21-116">如果不连接贵公司帐户，Attract 将使用基于 Microsoft 的默认电子邮件服务帐户。</span><span class="sxs-lookup"><span data-stu-id="36f21-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="36f21-117">选择**设置**（右上角的齿轮符号），然后选择**管理中心**。</span><span class="sxs-lookup"><span data-stu-id="36f21-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="36f21-118">在**发送电子邮件设置**选项卡上**电子邮件服务帐户**下，选择**连接公司帐户**。</span><span class="sxs-lookup"><span data-stu-id="36f21-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![在 Attract 中连接贵公司的电子邮件服务帐户](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="36f21-120">有关如何创建共享电子邮件帐户的详细信息，请参阅[Exchange Online 中的共享邮箱](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes)。</span><span class="sxs-lookup"><span data-stu-id="36f21-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="36f21-121">在 Microsoft 登录窗口中，使用您的企业凭证登录。</span><span class="sxs-lookup"><span data-stu-id="36f21-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="36f21-122">如果尚未设置电子邮件服务帐户，或者如果要添加新的，请选择**添加新的服务帐户**，然后输入您的电子邮件信息。</span><span class="sxs-lookup"><span data-stu-id="36f21-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="36f21-123">如果您已设置了要使用的电子邮件帐户，请选择该帐户。</span><span class="sxs-lookup"><span data-stu-id="36f21-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="36f21-124">成功配置电子邮件服务帐户之后，会发现**电子邮件服务帐户**下列出了该帐户。</span><span class="sxs-lookup"><span data-stu-id="36f21-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="36f21-125">断开电子邮件服务帐户</span><span class="sxs-lookup"><span data-stu-id="36f21-125">Disconnect an email service account</span></span>

<span data-ttu-id="36f21-126">如果要通过 Attract 停止电子邮件通信中使用贵公司的域，可断开电子邮件服务帐户。</span><span class="sxs-lookup"><span data-stu-id="36f21-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="36f21-127">选择**设置**（右上角的齿轮符号），然后选择**管理中心**。</span><span class="sxs-lookup"><span data-stu-id="36f21-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="36f21-128">在**电子邮件设置**选项卡上**电子邮件服务帐户**下，选择要断开的电子邮件服务帐户旁边的**更多**按钮（具有三个直点）。</span><span class="sxs-lookup"><span data-stu-id="36f21-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="36f21-129">选择**断开电子邮件帐户**。</span><span class="sxs-lookup"><span data-stu-id="36f21-129">Select **Disconnect email account**.</span></span>

    ![断开贵公司的电子邮件服务帐户](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="36f21-131">提示确认操作时，选择**断开**。</span><span class="sxs-lookup"><span data-stu-id="36f21-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![确认断开贵公司的电子邮件服务帐户](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="36f21-133">如果不连接其他电子邮件服务帐户，则从 Attract 发送的电子邮件将使用 Microsoft 品牌的默认电子邮件服务帐户。</span><span class="sxs-lookup"><span data-stu-id="36f21-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="36f21-134">配置电子邮件模板设置</span><span class="sxs-lookup"><span data-stu-id="36f21-134">Configure email template settings</span></span>

<span data-ttu-id="36f21-135">可将贵公司的徽标图像和其他信息作为带品牌的电子邮件页眉发送。</span><span class="sxs-lookup"><span data-stu-id="36f21-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="36f21-136">也可以在电子邮件页脚中提供您的隐私政策和使用条款的连接。</span><span class="sxs-lookup"><span data-stu-id="36f21-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="36f21-137">您必须遵守您的国家或地区及管辖电子邮件收件人的国家或地区的所有适用法律。</span><span class="sxs-lookup"><span data-stu-id="36f21-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="36f21-138">这些法律包括反垃圾邮件法规。</span><span class="sxs-lookup"><span data-stu-id="36f21-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="36f21-139">选择**设置**（右上角的齿轮符号），然后选择**管理中心**。</span><span class="sxs-lookup"><span data-stu-id="36f21-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="36f21-140">在**电子邮件设置**选项卡上**电子邮件模板设置**下，将要用作电子邮件页眉的图像拖到图像框，或在图像框中单击以浏览文件。</span><span class="sxs-lookup"><span data-stu-id="36f21-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="36f21-141">若要替换现有图像，必须首先选择其旁边的**移除**。</span><span class="sxs-lookup"><span data-stu-id="36f21-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="36f21-142">此图像必须是 JPEG、JPG、PNG 或 SVG 文件。</span><span class="sxs-lookup"><span data-stu-id="36f21-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="36f21-143">建议的图像大小为宽度为 25 与 800 像素之间，高度为 25 与 150 像素之间。</span><span class="sxs-lookup"><span data-stu-id="36f21-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="36f21-144">页眉的最大文件大小为 1 兆字节 (MB)。</span><span class="sxs-lookup"><span data-stu-id="36f21-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![添加贵公司电子邮件页眉的图像](./media/attract-admin-email-header.png)

3. <span data-ttu-id="36f21-146">在**你的通信隐私政策**下，提供贵公司隐私政策的链接。</span><span class="sxs-lookup"><span data-stu-id="36f21-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="36f21-147">在**你的通信条款和条件**下，提供贵公司使用条款的链接。</span><span class="sxs-lookup"><span data-stu-id="36f21-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![为电子邮件页眉添加贵公司隐私政策和使用条款的链接](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="36f21-149">选择**保存**保存您的电子邮件模板设置。</span><span class="sxs-lookup"><span data-stu-id="36f21-149">Select **Save** to save your email template settings.</span></span>
