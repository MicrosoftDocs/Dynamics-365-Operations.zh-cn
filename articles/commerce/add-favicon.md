---
title: 添加收藏夹图标
description: 此主题介绍如何向站点添加收藏夹图标。
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696983"
---
# <a name="add-a-favicon"></a><span data-ttu-id="4a3f4-103">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="4a3f4-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4a3f4-104">此主题介绍如何向站点添加收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="4a3f4-105">概览</span><span class="sxs-lookup"><span data-stu-id="4a3f4-105">Overview</span></span>

<span data-ttu-id="4a3f4-106">收藏夹图标是在 Web 浏览器标签页上、地址栏中、浏览历史记录中和书签或收藏夹中及其他位置内显示的小图形文件。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="4a3f4-107">建议向站点添加收藏夹图标，因为这样可以展示和强化您的品牌形象，帮助您的站点从客户访问的其他站点中脱颖而出。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="4a3f4-108">虽然可以向站点添加各种大小和文件类型的多个收藏夹图标，此主题介绍如何添加一个收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="4a3f4-109">但是，可使用相同流程和位置添加更多收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="4a3f4-110">将收藏夹图标上传到站点的资产集中</span><span class="sxs-lookup"><span data-stu-id="4a3f4-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="4a3f4-111">若要将收藏夹图标上传到站点的资产集中，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="4a3f4-112">转到**资产 \> 上传 \> 上传资产**。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="4a3f4-113">在本地文件系统中找到并选择收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="4a3f4-114">输入标题，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="4a3f4-115">在右侧的属性窗格中，复制收藏夹图标的公共 URL。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="4a3f4-116">如果不选择**上传后发布资产**选项，必须回到**资产**页，以后再发布该收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="4a3f4-117">为收藏夹图标创建 HTML</span><span class="sxs-lookup"><span data-stu-id="4a3f4-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="4a3f4-118">若要为收藏夹图标创建 HTML，请使用以下 HTML 片段。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="4a3f4-119">对于 **href** 属性，将 **"Public\_URL\_for\_your\_favicon"** 替换为您前面复制的公共 URL。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="4a3f4-120">将收藏夹图标的 HTML 添加到页面的 \<head\> 元素中。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="4a3f4-121">若要向站点添加收藏夹图标，请使用向站点页的 **\<head\>** 元素添加任何类型的 HTML 或脚本所用相同过程。</span><span class="sxs-lookup"><span data-stu-id="4a3f4-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a3f4-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="4a3f4-122">Additional resources</span></span>

[<span data-ttu-id="4a3f4-123">添加徽标</span><span class="sxs-lookup"><span data-stu-id="4a3f4-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="4a3f4-124">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="4a3f4-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="4a3f4-125">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="4a3f4-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="4a3f4-126">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="4a3f4-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="4a3f4-127">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="4a3f4-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="4a3f4-128">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="4a3f4-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

