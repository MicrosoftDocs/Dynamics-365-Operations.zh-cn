---
title: 管理 robots.txt 文件
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理 robots.txt 文件。
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: e472f3612bd6860e7262bb128035f2aed3b39372
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945974"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="5ad40-103">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="5ad40-103">Manage robots.txt files</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5ad40-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5ad40-105">概览</span><span class="sxs-lookup"><span data-stu-id="5ad40-105">Overview</span></span>

<span data-ttu-id="5ad40-106">机器人排除标准或 robots.txt 是网站用于与 Web 机器人通信的标准。</span><span class="sxs-lookup"><span data-stu-id="5ad40-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="5ad40-107">它通知 Web 机器人有关网站上不应访问的区域的信息。</span><span class="sxs-lookup"><span data-stu-id="5ad40-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="5ad40-108">机器人经常被搜索引擎用来为网站建立索引。</span><span class="sxs-lookup"><span data-stu-id="5ad40-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="5ad40-109">要从服务器中排除机器人，请在服务器上创建一个文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="5ad40-110">在此文件中，指定机器人的访问策略。</span><span class="sxs-lookup"><span data-stu-id="5ad40-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="5ad40-111">此文件必须可以通过 HTTP 在本地 URL **/robots.txt** 访问。</span><span class="sxs-lookup"><span data-stu-id="5ad40-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="5ad40-112">robots.txt 文件可帮助搜索引擎将您站点上的内容编入索引。</span><span class="sxs-lookup"><span data-stu-id="5ad40-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="5ad40-113">Dynamics 365 Commerce 可让您为您的域上载 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="5ad40-114">对于您的 Commerce 环境中的每个域，您可以上载一个 robots.txt 文件并将其与该域相关联。</span><span class="sxs-lookup"><span data-stu-id="5ad40-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="5ad40-115">有关 robots.txt 文件的详细信息，请访问 [Web 机器人页面](https://www.robotstxt.org/)。</span><span class="sxs-lookup"><span data-stu-id="5ad40-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="5ad40-116">上载 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="5ad40-116">Upload a robots.txt file</span></span>

<span data-ttu-id="5ad40-117">根据[机器人排除标准](https://www.robotstxt.org/orig.html)创建并编辑 robots.txt 文件后，请确保可以在要使用 Commerce 创作工具的计算机上访问该文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="5ad40-118">文件必须命名为 **robots.txt**。</span><span class="sxs-lookup"><span data-stu-id="5ad40-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="5ad40-119">为了获得最佳结果，必须采用标准中注明的格式。</span><span class="sxs-lookup"><span data-stu-id="5ad40-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="5ad40-120">每个 Commerce 客户负责验证和维护其 robots.txt 文件的内容。</span><span class="sxs-lookup"><span data-stu-id="5ad40-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="5ad40-121">要上载 robots.txt 文件，您必须以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="5ad40-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="5ad40-122">要在 Commerce 中上载 robots.txt 文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5ad40-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5ad40-123">以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="5ad40-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5ad40-124">在左侧导航窗格中，选择**租户设置**（在齿轮符号旁边）将其展开。</span><span class="sxs-lookup"><span data-stu-id="5ad40-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5ad40-125">在**租户设置**下，选择 **Robots.txt**。</span><span class="sxs-lookup"><span data-stu-id="5ad40-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5ad40-126">与您的环境关联的所有域的列表将显示在窗口的主要部分。</span><span class="sxs-lookup"><span data-stu-id="5ad40-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5ad40-127">选择**管理**为您环境中的域上载 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5ad40-128">在右侧菜单上，选择与 robots.txt 文件关联的域旁边的**上载**按钮（向上箭头）。</span><span class="sxs-lookup"><span data-stu-id="5ad40-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5ad40-129">将出现一个文件浏览器对话框。</span><span class="sxs-lookup"><span data-stu-id="5ad40-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="5ad40-130">在对话框中，浏览并选择要为关联的域上载的 robots.txt 文件，然后选择**打开**完成上载。</span><span class="sxs-lookup"><span data-stu-id="5ad40-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="5ad40-131">在上载期间，Commerce 会验证该文件是否是文本文件，但不会验证文件的内容。</span><span class="sxs-lookup"><span data-stu-id="5ad40-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="5ad40-132">下载 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="5ad40-132">Download a robots.txt file</span></span>

<span data-ttu-id="5ad40-133">要在 Commerce 中下载 robots.txt 文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5ad40-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5ad40-134">以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="5ad40-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5ad40-135">在左侧导航窗格中，选择**租户设置**（在齿轮符号旁边）将其展开。</span><span class="sxs-lookup"><span data-stu-id="5ad40-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5ad40-136">在**租户设置**下，选择 **Robots.txt**。</span><span class="sxs-lookup"><span data-stu-id="5ad40-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5ad40-137">与您的环境关联的所有域的列表将显示在窗口的主要部分。</span><span class="sxs-lookup"><span data-stu-id="5ad40-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5ad40-138">选择**管理**为您环境中的域下载 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5ad40-139">在右侧菜单上，选择与 robots.txt 文件关联的域旁边的**下载**按钮（向下箭头）。</span><span class="sxs-lookup"><span data-stu-id="5ad40-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5ad40-140">将出现一个文件浏览器对话框。</span><span class="sxs-lookup"><span data-stu-id="5ad40-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="5ad40-141">在对话框中，转到本地驱动器上的所需位置，确认或输入文件名，然后选择**保存**完成下载。</span><span class="sxs-lookup"><span data-stu-id="5ad40-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="5ad40-142">此过程只能用于下载以前通过 Commerce 创作工具上载的 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="5ad40-143">删除 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="5ad40-143">Delete a robots.txt file</span></span>

<span data-ttu-id="5ad40-144">要在 Commerce 中删除 robots.txt 文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="5ad40-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5ad40-145">以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="5ad40-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5ad40-146">在左侧导航窗格中，选择**租户设置**（在齿轮符号旁边）将其展开。</span><span class="sxs-lookup"><span data-stu-id="5ad40-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5ad40-147">在**租户设置**下，选择 **Robots.txt**。</span><span class="sxs-lookup"><span data-stu-id="5ad40-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5ad40-148">与您的环境关联的所有域的列表将显示在窗口的主要部分。</span><span class="sxs-lookup"><span data-stu-id="5ad40-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5ad40-149">选择**管理**为您环境中的域删除 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5ad40-150">在右侧菜单上，选择与 robots.txt 文件关联的域旁边的**删除**按钮（垃圾桶符号）。</span><span class="sxs-lookup"><span data-stu-id="5ad40-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5ad40-151">将出现一个文件浏览器窗口。</span><span class="sxs-lookup"><span data-stu-id="5ad40-151">A file browser window appears.</span></span>
6. <span data-ttu-id="5ad40-152">在文件浏览器窗口中，浏览并选择要为域删除的 robots.txt 文件，然后选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="5ad40-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="5ad40-153">将出现警告消息框。</span><span class="sxs-lookup"><span data-stu-id="5ad40-153">A warning message box appears.</span></span>
7. <span data-ttu-id="5ad40-154">在消息框中，选择**删除**确认删除 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="5ad40-155">此过程只能用于删除以前通过 Commerce 创作工具上载的 robots.txt 文件。</span><span class="sxs-lookup"><span data-stu-id="5ad40-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ad40-156">其他资源</span><span class="sxs-lookup"><span data-stu-id="5ad40-156">Additional resources</span></span>

[<span data-ttu-id="5ad40-157">配置域名</span><span class="sxs-lookup"><span data-stu-id="5ad40-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5ad40-158">部署新的电子商务站点</span><span class="sxs-lookup"><span data-stu-id="5ad40-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="5ad40-159">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="5ad40-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="5ad40-160">将在线站点与渠道关联</span><span class="sxs-lookup"><span data-stu-id="5ad40-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="5ad40-161">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="5ad40-161">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="5ad40-162">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="5ad40-162">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="5ad40-163">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="5ad40-163">Enable location-based store detection</span></span>](enable-store-detection.md)
