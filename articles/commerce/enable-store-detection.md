---
title: 启用基于位置的商店检测
description: 此主题介绍如何为 Dynamics 365 Commerce 站点开启基于位置的商店检测。
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3f7e9a3acde508f405ce85f125db552c3ae3656b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000713"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="30bc2-103">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="30bc2-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="30bc2-104">此主题介绍如何为 Dynamics 365 Commerce 站点开启基于位置的商店检测。</span><span class="sxs-lookup"><span data-stu-id="30bc2-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="30bc2-105">概览</span><span class="sxs-lookup"><span data-stu-id="30bc2-105">Overview</span></span>

<span data-ttu-id="30bc2-106">可通过 Commerce 中基于位置的商店检测基于客户的位置向客户提供相关站点内容。</span><span class="sxs-lookup"><span data-stu-id="30bc2-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="30bc2-107">开启基于位置的商店检测之后，Commerce 呈现服务使用客户 Web 浏览器 IP 地址的国家/区域信息将客户重定向到可用的最佳地理站点配置。</span><span class="sxs-lookup"><span data-stu-id="30bc2-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="30bc2-108">隐私声明</span><span class="sxs-lookup"><span data-stu-id="30bc2-108">Privacy notice</span></span>

<span data-ttu-id="30bc2-109">如果开启基于位置的商店检测功能，将把客户浏览器的信息发送到 Microsoft 位置服务。</span><span class="sxs-lookup"><span data-stu-id="30bc2-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="30bc2-110">然后使用此信息提供与其位置有关的客户内容。</span><span class="sxs-lookup"><span data-stu-id="30bc2-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="30bc2-111">从客户浏览器发送的信息和返回给客户的基于位置的信息应遵守隐私和 cookie 合规性政策。</span><span class="sxs-lookup"><span data-stu-id="30bc2-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="30bc2-112">开启基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="30bc2-112">Turn on location-based store detection</span></span>

<span data-ttu-id="30bc2-113">若要在 Commerce 中开启基于位置的商店检测，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="30bc2-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="30bc2-114">在创作工具中，转到您的站点。</span><span class="sxs-lookup"><span data-stu-id="30bc2-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="30bc2-115">在左侧的导航窗格中，选择 **站点管理**。</span><span class="sxs-lookup"><span data-stu-id="30bc2-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="30bc2-116">选择 **站点设置**。</span><span class="sxs-lookup"><span data-stu-id="30bc2-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="30bc2-117">将 **启用基于位置的商店检测** 选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="30bc2-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30bc2-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="30bc2-118">Additional resources</span></span>

[<span data-ttu-id="30bc2-119">配置域名</span><span class="sxs-lookup"><span data-stu-id="30bc2-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="30bc2-120">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="30bc2-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="30bc2-121">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="30bc2-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="30bc2-122">将 Dynamics 365 Commerce 站点与在线渠道相关联</span><span class="sxs-lookup"><span data-stu-id="30bc2-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="30bc2-123">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="30bc2-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="30bc2-124">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="30bc2-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="30bc2-125">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="30bc2-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="30bc2-126">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="30bc2-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="30bc2-127">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="30bc2-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="30bc2-128">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="30bc2-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
