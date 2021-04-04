---
title: 管理 robots.txt 文件
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理 robots.txt 文件。
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477700"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="af062-103">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="af062-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="af062-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="af062-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="af062-105">机器人排除标准或 robots.txt 是网站用于与 Web 机器人通信的标准。</span><span class="sxs-lookup"><span data-stu-id="af062-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="af062-106">它通知 Web 机器人有关网站上不应访问的区域的信息。</span><span class="sxs-lookup"><span data-stu-id="af062-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="af062-107">机器人经常被搜索引擎用来为网站建立索引。</span><span class="sxs-lookup"><span data-stu-id="af062-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="af062-108">要从服务器中排除机器人，请在服务器上创建一个文件。</span><span class="sxs-lookup"><span data-stu-id="af062-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="af062-109">在此文件中，指定机器人的访问策略。</span><span class="sxs-lookup"><span data-stu-id="af062-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="af062-110">此文件必须可以通过 HTTP 在本地 URL **/robots.txt** 访问。</span><span class="sxs-lookup"><span data-stu-id="af062-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="af062-111">robots.txt 文件可帮助搜索引擎将您站点上的内容编入索引。</span><span class="sxs-lookup"><span data-stu-id="af062-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="af062-112">Dynamics 365 Commerce 可让您为您的域上载 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="af062-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="af062-113">对于您的 Commerce 环境中的每个域，您可以上载一个 robots.txt 文件并将其与该域相关联。</span><span class="sxs-lookup"><span data-stu-id="af062-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="af062-114">有关 robots.txt 文件的详细信息，请访问 [Web 机器人页面](https://www.robotstxt.org/)。</span><span class="sxs-lookup"><span data-stu-id="af062-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="af062-115">上载 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="af062-115">Upload a robots.txt file</span></span>

<span data-ttu-id="af062-116">根据[机器人排除标准](https://www.robotstxt.org/orig.html)创建并编辑 robots.txt 文件后，请确保可以在要使用 Commerce 创作工具的计算机上访问该文件。</span><span class="sxs-lookup"><span data-stu-id="af062-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="af062-117">文件必须命名为 **robots.txt**。</span><span class="sxs-lookup"><span data-stu-id="af062-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="af062-118">为了获得最佳结果，必须采用标准中注明的格式。</span><span class="sxs-lookup"><span data-stu-id="af062-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="af062-119">每个 Commerce 客户负责验证和维护其 robots.txt 文件的内容。</span><span class="sxs-lookup"><span data-stu-id="af062-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="af062-120">要上载 robots.txt 文件，您必须以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="af062-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="af062-121">要在 Commerce 中上载 robots.txt 文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="af062-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="af062-122">以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="af062-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="af062-123">在左侧导航窗格中，选择 **租户设置**（在齿轮符号旁边）将其展开。</span><span class="sxs-lookup"><span data-stu-id="af062-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="af062-124">在 **租户设置** 下，选择 **Robots.txt**。</span><span class="sxs-lookup"><span data-stu-id="af062-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="af062-125">与您的环境关联的所有域的列表将显示在窗口的主要部分。</span><span class="sxs-lookup"><span data-stu-id="af062-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="af062-126">选择 **管理** 为您环境中的域上载 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="af062-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="af062-127">在右侧菜单上，选择与 robots.txt 文件关联的域旁边的 **上载** 按钮（向上箭头）。</span><span class="sxs-lookup"><span data-stu-id="af062-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="af062-128">将出现一个文件浏览器对话框。</span><span class="sxs-lookup"><span data-stu-id="af062-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="af062-129">在对话框中，浏览并选择要为关联的域上载的 robots.txt 文件，然后选择 **打开** 完成上载。</span><span class="sxs-lookup"><span data-stu-id="af062-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="af062-130">在上载期间，Commerce 会验证该文件是否是文本文件，但不会验证文件的内容。</span><span class="sxs-lookup"><span data-stu-id="af062-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="af062-131">下载 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="af062-131">Download a robots.txt file</span></span>

<span data-ttu-id="af062-132">要在 Commerce 中下载 robots.txt 文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="af062-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="af062-133">以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="af062-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="af062-134">在左侧导航窗格中，选择 **租户设置**（在齿轮符号旁边）将其展开。</span><span class="sxs-lookup"><span data-stu-id="af062-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="af062-135">在 **租户设置** 下，选择 **Robots.txt**。</span><span class="sxs-lookup"><span data-stu-id="af062-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="af062-136">与您的环境关联的所有域的列表将显示在窗口的主要部分。</span><span class="sxs-lookup"><span data-stu-id="af062-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="af062-137">选择 **管理** 为您环境中的域下载 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="af062-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="af062-138">在右侧菜单上，选择与 robots.txt 文件关联的域旁边的 **下载** 按钮（向下箭头）。</span><span class="sxs-lookup"><span data-stu-id="af062-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="af062-139">将出现一个文件浏览器对话框。</span><span class="sxs-lookup"><span data-stu-id="af062-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="af062-140">在对话框中，转到本地驱动器上的所需位置，确认或输入文件名，然后选择 **保存** 完成下载。</span><span class="sxs-lookup"><span data-stu-id="af062-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="af062-141">此过程只能用于下载以前通过 Commerce 创作工具上载的 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="af062-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="af062-142">删除 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="af062-142">Delete a robots.txt file</span></span>

<span data-ttu-id="af062-143">要在 Commerce 中删除 robots.txt 文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="af062-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="af062-144">以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="af062-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="af062-145">在左侧导航窗格中，选择 **租户设置**（在齿轮符号旁边）将其展开。</span><span class="sxs-lookup"><span data-stu-id="af062-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="af062-146">在 **租户设置** 下，选择 **Robots.txt**。</span><span class="sxs-lookup"><span data-stu-id="af062-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="af062-147">与您的环境关联的所有域的列表将显示在窗口的主要部分。</span><span class="sxs-lookup"><span data-stu-id="af062-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="af062-148">选择 **管理** 为您环境中的域删除 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="af062-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="af062-149">在右侧菜单上，选择与 robots.txt 文件关联的域旁边的 **删除** 按钮（垃圾桶符号）。</span><span class="sxs-lookup"><span data-stu-id="af062-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="af062-150">将出现一个文件浏览器窗口。</span><span class="sxs-lookup"><span data-stu-id="af062-150">A file browser window appears.</span></span>
6. <span data-ttu-id="af062-151">在文件浏览器窗口中，浏览并选择要为域删除的 robots.txt 文件，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="af062-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="af062-152">将出现警告消息框。</span><span class="sxs-lookup"><span data-stu-id="af062-152">A warning message box appears.</span></span>
7. <span data-ttu-id="af062-153">在消息框中，选择 **删除** 确认删除 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="af062-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="af062-154">此过程只能用于删除以前通过 Commerce 创作工具上载的 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="af062-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af062-155">其他资源</span><span class="sxs-lookup"><span data-stu-id="af062-155">Additional resources</span></span>

[<span data-ttu-id="af062-156">配置域名</span><span class="sxs-lookup"><span data-stu-id="af062-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="af062-157">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="af062-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="af062-158">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="af062-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="af062-159">将 Dynamics 365 Commerce 站点与在线渠道相关联</span><span class="sxs-lookup"><span data-stu-id="af062-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="af062-160">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="af062-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="af062-161">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="af062-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="af062-162">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="af062-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="af062-163">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="af062-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="af062-164">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="af062-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="af062-165">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="af062-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
