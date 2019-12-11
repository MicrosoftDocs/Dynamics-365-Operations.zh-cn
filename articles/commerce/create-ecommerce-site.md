---
title: 创建电子商务站点
description: 此主题介绍与在 Dynamics 365 Commerce 中创建新电子商务站点关联的任务。
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697121"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="6588b-103">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="6588b-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6588b-104">此主题介绍与在 Dynamics 365 Commerce 中创建新电子商务站点关联的任务。</span><span class="sxs-lookup"><span data-stu-id="6588b-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6588b-105">概览</span><span class="sxs-lookup"><span data-stu-id="6588b-105">Overview</span></span>

<span data-ttu-id="6588b-106">若要开始开发电子商务站点，必须先在站点创作环境中建立新站点。</span><span class="sxs-lookup"><span data-stu-id="6588b-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="6588b-107">必须至少现在 Dynamics 365 Retail 中创建一个在线商店，才能创建新站点。</span><span class="sxs-lookup"><span data-stu-id="6588b-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="6588b-108">设置站点</span><span class="sxs-lookup"><span data-stu-id="6588b-108">Set up your site</span></span>

<span data-ttu-id="6588b-109">若要设置站点，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="6588b-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="6588b-110">在 Microsoft Lifecycle Services (LCS) 中，选择站点创作环境的链接。</span><span class="sxs-lookup"><span data-stu-id="6588b-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="6588b-111">在站点创作环境的主页中，选择**新建站点**。</span><span class="sxs-lookup"><span data-stu-id="6588b-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="6588b-112">在**新站点**对话框中，提供以下信息。</span><span class="sxs-lookup"><span data-stu-id="6588b-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="6588b-113">字段</span><span class="sxs-lookup"><span data-stu-id="6588b-113">Field</span></span>                               | <span data-ttu-id="6588b-114">说明</span><span class="sxs-lookup"><span data-stu-id="6588b-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="6588b-115">站点名称</span><span class="sxs-lookup"><span data-stu-id="6588b-115">Site name</span></span>                           | <span data-ttu-id="6588b-116">输入应该在站点创作环境中用于站点的显示名称。</span><span class="sxs-lookup"><span data-stu-id="6588b-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="6588b-117">此名称仅在创作环境中显示，不对客户显示。</span><span class="sxs-lookup"><span data-stu-id="6588b-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="6588b-118">站点管理员的安全组</span><span class="sxs-lookup"><span data-stu-id="6588b-118">Site administrator's security group</span></span> | <span data-ttu-id="6588b-119">指定用于管理在此站点中具有站点管理员角色的用户的 Microsoft Azure Active Directory (Azure AD) 安全组。</span><span class="sxs-lookup"><span data-stu-id="6588b-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="6588b-120">默认渠道(运营单位编号)</span><span class="sxs-lookup"><span data-stu-id="6588b-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="6588b-121">选择此站点将充当其 Web 店面的在线商店。</span><span class="sxs-lookup"><span data-stu-id="6588b-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="6588b-122">如果希望电子商务站点支持多个在线商店，必须在设置站点后在**站点设置**中将商店与站点关联。</span><span class="sxs-lookup"><span data-stu-id="6588b-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="6588b-123">默认语言</span><span class="sxs-lookup"><span data-stu-id="6588b-123">Default language</span></span>                            | <span data-ttu-id="6588b-124">指定此在线商店和市场的默认语言。</span><span class="sxs-lookup"><span data-stu-id="6588b-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="6588b-125">在线商店可支持多种语言。</span><span class="sxs-lookup"><span data-stu-id="6588b-125">An online store can support multiple languages.</span></span> <span data-ttu-id="6588b-126">如果希望此在线商店或其他在线商店支持多种语言，可在设置站点后在**站点设置**中配置此项支持。</span><span class="sxs-lookup"><span data-stu-id="6588b-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="6588b-127">域</span><span class="sxs-lookup"><span data-stu-id="6588b-127">Domain</span></span>                              | <span data-ttu-id="6588b-128">选择将充当此在线商店的域的域名。</span><span class="sxs-lookup"><span data-stu-id="6588b-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="6588b-129">如果尚未在 LCS 中配置任何域，可将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="6588b-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="6588b-130">在 LCS 中配置域之后，必须在**站点设置**中将其添加到您的在线商店。</span><span class="sxs-lookup"><span data-stu-id="6588b-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="6588b-131">路径</span><span class="sxs-lookup"><span data-stu-id="6588b-131">Path</span></span>                              | <span data-ttu-id="6588b-132">如果您的站点支持对给定域名使用多种语言，请使用路径字段为该域和语言的组合创建唯一站点。</span><span class="sxs-lookup"><span data-stu-id="6588b-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="6588b-133">如果在**默认语言**中指定的语言是此域将支持的唯一语言，或将在将站点本地化为更多语言后继续充当默认语言，建议您将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="6588b-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="6588b-134">创建站点之后，可通过选择**产品**选项卡将其与在线商店关联。应该可以查看已经分配给在线商店的产品的分类。</span><span class="sxs-lookup"><span data-stu-id="6588b-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="6588b-135">还可以使用页面左上角的下拉菜单按类别访问分配的产品。</span><span class="sxs-lookup"><span data-stu-id="6588b-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6588b-136">其他资源</span><span class="sxs-lookup"><span data-stu-id="6588b-136">Additional resources</span></span>

[<span data-ttu-id="6588b-137">在线商店概览</span><span class="sxs-lookup"><span data-stu-id="6588b-137">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="6588b-138">部署新的电子商务站点</span><span class="sxs-lookup"><span data-stu-id="6588b-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6588b-139">将在线站点与渠道关联</span><span class="sxs-lookup"><span data-stu-id="6588b-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6588b-140">配置域名</span><span class="sxs-lookup"><span data-stu-id="6588b-140">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6588b-141">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="6588b-141">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6588b-142">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="6588b-142">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="6588b-143">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="6588b-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6588b-144">创作主页概览</span><span class="sxs-lookup"><span data-stu-id="6588b-144">Authoring home page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="6588b-145">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="6588b-145">Add a new site page</span></span>](add-new-page.md)
