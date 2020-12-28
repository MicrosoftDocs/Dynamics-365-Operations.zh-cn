---
title: 创建电子商务站点
description: 本主题介绍在 Dynamics 365 Commerce 站点构建器中创建新电子商务站点所需的步骤和信息。
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
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
ms.openlocfilehash: 7d552f29fd8f52b512a7c21b36b0a814cac50646
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517176"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="ba5f7-103">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="ba5f7-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba5f7-104">本主题介绍在 Dynamics 365 Commerce 站点构建器中创建新电子商务站点所需的步骤和信息。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="ba5f7-105">在许可 Dynamics 365 Commerce 功能时，将为站点构建器预配可用作您自己站点的基础的入门站点。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="ba5f7-106">但是，如果要从头开始或要建立第二个站点，则需要在站点创作环境中建立一个新站点。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="ba5f7-107">设置站点</span><span class="sxs-lookup"><span data-stu-id="ba5f7-107">Set up your site</span></span>

<span data-ttu-id="ba5f7-108">若要设置站点，请执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="ba5f7-109">打开站点构建器环境。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-109">Open the site builder environment.</span></span> <span data-ttu-id="ba5f7-110">您可以在 Commerce 环境功能页面内的 Microsoft Lifecycle Services (LCS) 中查找指向站点构建器的链接。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="ba5f7-111">在站点创作环境的主页中，选择 **新建站点**。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="ba5f7-112">在 **新站点** 对话框中，提供以下信息。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="ba5f7-113">字段</span><span class="sxs-lookup"><span data-stu-id="ba5f7-113">Field</span></span>                               | <span data-ttu-id="ba5f7-114">说明</span><span class="sxs-lookup"><span data-stu-id="ba5f7-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="ba5f7-115">站点名称</span><span class="sxs-lookup"><span data-stu-id="ba5f7-115">Site name</span></span>                           | <span data-ttu-id="ba5f7-116">输入应该在站点创作环境中用于站点的显示名称。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="ba5f7-117">此名称仅在创作环境中显示，不对客户显示。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="ba5f7-118">站点管理员的安全组</span><span class="sxs-lookup"><span data-stu-id="ba5f7-118">Site administrator's security group</span></span> | <span data-ttu-id="ba5f7-119">指定用于管理在此站点中具有站点管理员角色的用户的 Microsoft Azure Active Directory (Azure AD) 安全组。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="ba5f7-120">默认渠道(运营单位编号)</span><span class="sxs-lookup"><span data-stu-id="ba5f7-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="ba5f7-121">选择此站点将充当其 Web 店面的在线商店。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="ba5f7-122">如果您希望电子商务站点支持多个在线商店，必须在设置站点后在 **站点设置** 中将商店与站点关联。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="ba5f7-123">默认语言</span><span class="sxs-lookup"><span data-stu-id="ba5f7-123">Default language</span></span>                            | <span data-ttu-id="ba5f7-124">指定此在线商店和市场的默认语言。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="ba5f7-125">在线商店可支持多种语言。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-125">An online store can support multiple languages.</span></span> <span data-ttu-id="ba5f7-126">如果希望此在线商店或其他在线商店支持多种语言，可在设置站点后在 **站点设置** 中配置此项支持。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="ba5f7-127">域</span><span class="sxs-lookup"><span data-stu-id="ba5f7-127">Domain</span></span>                              | <span data-ttu-id="ba5f7-128">选择将充当此在线商店的域的域名。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="ba5f7-129">如果尚未在 LCS 中配置任何域，可将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="ba5f7-130">在 LCS 中配置域之后，必须在 **站点设置** 中将其添加到您的在线商店。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="ba5f7-131">路径</span><span class="sxs-lookup"><span data-stu-id="ba5f7-131">Path</span></span>                              | <span data-ttu-id="ba5f7-132">如果您的站点支持对给定域名使用多种语言，请使用路径字段为该域和语言的组合创建唯一站点。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="ba5f7-133">如果在 **默认语言** 中指定的语言是此域将支持的唯一语言，或将在将站点本地化为更多语言后继续充当默认语言，建议您将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="ba5f7-134">创建站点之后，可通过选择 **产品** 选项卡将其与在线商店关联。应该可以查看已经分配给在线商店的产品的分类。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="ba5f7-135">还可以使用页面左上角的下拉菜单按类别访问分配的产品。</span><span class="sxs-lookup"><span data-stu-id="ba5f7-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba5f7-136">其他资源</span><span class="sxs-lookup"><span data-stu-id="ba5f7-136">Additional resources</span></span>

[<span data-ttu-id="ba5f7-137">配置域名</span><span class="sxs-lookup"><span data-stu-id="ba5f7-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ba5f7-138">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="ba5f7-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ba5f7-139">将 Dynamics 365 Commerce 站点与在线渠道相关联</span><span class="sxs-lookup"><span data-stu-id="ba5f7-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ba5f7-140">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="ba5f7-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="ba5f7-141">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="ba5f7-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="ba5f7-142">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="ba5f7-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="ba5f7-143">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="ba5f7-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="ba5f7-144">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="ba5f7-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="ba5f7-145">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="ba5f7-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ba5f7-146">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="ba5f7-146">Enable location-based store detection</span></span>](enable-store-detection.md)
