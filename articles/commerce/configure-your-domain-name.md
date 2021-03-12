---
title: 配置域名
description: 此主题介绍如何为 Microsoft Dynamics 365 电子商务站点配置域名。
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3df563b62b40970509340802a09bb36dda14777
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000992"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="9dca2-103">配置域名</span><span class="sxs-lookup"><span data-stu-id="9dca2-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9dca2-104">此主题介绍如何为 Microsoft Dynamics 365 电子商务站点配置域名。</span><span class="sxs-lookup"><span data-stu-id="9dca2-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="9dca2-105">在电子商务初始化期间添加域</span><span class="sxs-lookup"><span data-stu-id="9dca2-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="9dca2-106">若要将域与 Dynamics 365 Commerce 电子商务环境关联，请按照[部署新电子商务租户](deploy-ecommerce-site.md)中的说明初始化电子商务。</span><span class="sxs-lookup"><span data-stu-id="9dca2-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="9dca2-107">在初始化期间，系统将要求您提供将用于预配电子商务环境的信息。</span><span class="sxs-lookup"><span data-stu-id="9dca2-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="9dca2-108">在 **支持的主机名** 字段中，添加计划用于此环境的所有域。</span><span class="sxs-lookup"><span data-stu-id="9dca2-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="9dca2-109">应该使用分号分隔多个域。</span><span class="sxs-lookup"><span data-stu-id="9dca2-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="9dca2-110">这样，将在所有必需电子商务组件中配置域，并且在您从内容交付网络 (CDN) 或 Web 服务器切换流量并将其指向电子商务前端时，可以使用这些域。</span><span class="sxs-lookup"><span data-stu-id="9dca2-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="9dca2-111">在电子商务初始化后添加域</span><span class="sxs-lookup"><span data-stu-id="9dca2-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="9dca2-112">若要在电子商务初始化之后将新域与电子商务环境关联，您必须提交服务请求。</span><span class="sxs-lookup"><span data-stu-id="9dca2-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9dca2-113">其他资源</span><span class="sxs-lookup"><span data-stu-id="9dca2-113">Additional resources</span></span>

[<span data-ttu-id="9dca2-114">部署新的电子商务租户</span><span class="sxs-lookup"><span data-stu-id="9dca2-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="9dca2-115">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="9dca2-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9dca2-116">将 Dynamics 365 Commerce 站点与在线渠道相关联</span><span class="sxs-lookup"><span data-stu-id="9dca2-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9dca2-117">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="9dca2-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="9dca2-118">批量上传 URL 重定向</span><span class="sxs-lookup"><span data-stu-id="9dca2-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="9dca2-119">在 Commerce 中设置 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="9dca2-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="9dca2-120">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="9dca2-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9dca2-121">在 Commerce 环境中配置多个 B2C 租户</span><span class="sxs-lookup"><span data-stu-id="9dca2-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="9dca2-122">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="9dca2-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9dca2-123">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="9dca2-123">Enable location-based store detection</span></span>](enable-store-detection.md)
