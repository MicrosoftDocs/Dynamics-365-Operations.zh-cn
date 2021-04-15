---
title: 将 Dynamics 365 Commerce 站点与在线渠道关联
description: 此主题介绍如何将 Microsoft Dynamics 365 Commerce 站点绑定到一个或多个在线商店。
author: bicyclingfool
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7ceef55bac11ae8a1f7d9dafbddc45d67b836504
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797297"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="12f1d-103">将 Dynamics 365 Commerce 站点与在线渠道关联</span><span class="sxs-lookup"><span data-stu-id="12f1d-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12f1d-104">此主题介绍如何将 Microsoft Dynamics 365 Commerce 站点绑定到一个或多个在线商店。</span><span class="sxs-lookup"><span data-stu-id="12f1d-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="12f1d-105">在使用 Microsoft Dynamics Lifecycle Services (LCS) 门户预配 Dynamics 365 Commerce 电子商务环境之后，即可建立您的第一个电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="12f1d-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="12f1d-106">创建初始站点时，将站点与之前创建的在线商店关联。</span><span class="sxs-lookup"><span data-stu-id="12f1d-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="12f1d-107">此步骤将站点绑定到在线渠道，让站点显示导航层次结构、产品、类别、价格、装运选项和您在在线商店中定义的其他所有项。</span><span class="sxs-lookup"><span data-stu-id="12f1d-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="12f1d-108">若要建立新站点和将在线商店与其关联，请在 LCS 中选择站点制作环境的链接。</span><span class="sxs-lookup"><span data-stu-id="12f1d-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="12f1d-109">然后，在站点制作环境的页面中，选择 **新建站点**。</span><span class="sxs-lookup"><span data-stu-id="12f1d-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="12f1d-110">在 **新站点** 对话框中，必须提供有关站点的一些基本信息。</span><span class="sxs-lookup"><span data-stu-id="12f1d-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="12f1d-111">有关必须提供的信息的完整说明，请参阅[创建新电子商务站点](create-ecommerce-site.md)。</span><span class="sxs-lookup"><span data-stu-id="12f1d-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="12f1d-112">创建站点之后，可通过选择 **产品** 选项卡将其与在线商店关联。应该可以查看已经分配给在线商店的产品的分类。</span><span class="sxs-lookup"><span data-stu-id="12f1d-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="12f1d-113">还可以使用页面左上角的下拉字段按类别访问产品。</span><span class="sxs-lookup"><span data-stu-id="12f1d-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12f1d-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="12f1d-114">Additional resources</span></span>

[<span data-ttu-id="12f1d-115">配置域名</span><span class="sxs-lookup"><span data-stu-id="12f1d-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="12f1d-116">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="12f1d-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="12f1d-117">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="12f1d-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="12f1d-118">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="12f1d-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="12f1d-119">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="12f1d-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="12f1d-120">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="12f1d-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="12f1d-121">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="12f1d-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="12f1d-122">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="12f1d-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="12f1d-123">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="12f1d-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="12f1d-124">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="12f1d-124">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]