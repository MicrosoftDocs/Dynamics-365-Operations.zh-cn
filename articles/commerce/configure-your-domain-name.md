---
title: 配置域名
description: 此主题介绍如何为 Microsoft Dynamics 365 电子商务站点配置域名。
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4db774783dba4b1cea9552da3cff29a9528bd496
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002166"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="94440-103">配置域名</span><span class="sxs-lookup"><span data-stu-id="94440-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="94440-104">此主题介绍如何为 Microsoft Dynamics 365 电子商务站点配置域名。</span><span class="sxs-lookup"><span data-stu-id="94440-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="94440-105">电子商务初始化期间添加域</span><span class="sxs-lookup"><span data-stu-id="94440-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="94440-106">若要将域与电子商务环境关联，请按照[部署新电子商务站点](deploy-ecommerce-site.md)中的说明初始化电子商务。</span><span class="sxs-lookup"><span data-stu-id="94440-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="94440-107">初始化期间，将请您提供将用于预配电子商务环境的信息。</span><span class="sxs-lookup"><span data-stu-id="94440-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="94440-108">在**支持的主机名**字段中，添加计划用于此环境的所有域。</span><span class="sxs-lookup"><span data-stu-id="94440-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="94440-109">应该使用分号分隔多个域。</span><span class="sxs-lookup"><span data-stu-id="94440-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="94440-110">这样，将在所有必需电子商务组件中配置域，并且在您从内容交付网络 (CDN) 或 Web 服务器切换流量并将其指向电子商务前端时，可以使用这些域。</span><span class="sxs-lookup"><span data-stu-id="94440-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="94440-111">电子商务初始化后添加域</span><span class="sxs-lookup"><span data-stu-id="94440-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="94440-112">若要在电子商务初始化之后将新域与电子商务环境关联，必须提交服务请求。</span><span class="sxs-lookup"><span data-stu-id="94440-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94440-113">其他资源</span><span class="sxs-lookup"><span data-stu-id="94440-113">Additional resources</span></span>

[<span data-ttu-id="94440-114">部署新的电子商务站点</span><span class="sxs-lookup"><span data-stu-id="94440-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="94440-115">创建电子商务站点</span><span class="sxs-lookup"><span data-stu-id="94440-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="94440-116">将在线站点与渠道关联</span><span class="sxs-lookup"><span data-stu-id="94440-116">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="94440-117">管理 robots.txt 文件</span><span class="sxs-lookup"><span data-stu-id="94440-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="94440-118">设置用户登录自定义页面</span><span class="sxs-lookup"><span data-stu-id="94440-118">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="94440-119">添加对内容交付网络 (CDN) 的支持</span><span class="sxs-lookup"><span data-stu-id="94440-119">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="94440-120">启用基于位置的商店检测</span><span class="sxs-lookup"><span data-stu-id="94440-120">Enable location-based store detection</span></span>](enable-store-detection.md)
