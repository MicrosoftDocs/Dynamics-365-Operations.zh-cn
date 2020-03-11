---
title: 选择使用评分和评价
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点中选择使用评分和评价。
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057502"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="c3664-103">选择使用评分和评价</span><span class="sxs-lookup"><span data-stu-id="c3664-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3664-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 站点中选择使用评分和评价。</span><span class="sxs-lookup"><span data-stu-id="c3664-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="c3664-105">概览</span><span class="sxs-lookup"><span data-stu-id="c3664-105">Overview</span></span>

<span data-ttu-id="c3664-106">评分和评价解决方案是可通过使用 Microsoft Dynamics Lifecycle Services (LCS) 在 Dynamics 365 Commerce 中启用的全渠道解决方案。</span><span class="sxs-lookup"><span data-stu-id="c3664-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c3664-107">LCS 是零售商用于管理环境（从预配到停用）的管理门户。</span><span class="sxs-lookup"><span data-stu-id="c3664-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="c3664-108">如果要在 Commerce 网站中使用评分和评价解决方案，您必须在 Dynamics 365 Commerce 上部署电子商务站点期间选择使用评分和评价。</span><span class="sxs-lookup"><span data-stu-id="c3664-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="c3664-109">选择使用评分和评价</span><span class="sxs-lookup"><span data-stu-id="c3664-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="c3664-110">若要在站点中选择使用评分和评价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c3664-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="c3664-111">执行[部署新电子商务站点](deploy-ecommerce-site.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="c3664-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="c3664-112">还在 LCS 中时，转到 **Retail 部署设置 \> 其他设置**。</span><span class="sxs-lookup"><span data-stu-id="c3664-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="c3664-113">将**启用评分和评价服务**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="c3664-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="c3664-114">在**评分和评价审查者的 AAD 安全组(安全组对象 ID)** 字段中，输入其中包含评分和评价审查者的 Microsoft Azure Active Directory (Azure AD) 安全组的 ID。</span><span class="sxs-lookup"><span data-stu-id="c3664-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![选择使用评分和评价](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="c3664-116">完成电子商务初始化流程。</span><span class="sxs-lookup"><span data-stu-id="c3664-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="c3664-117">如果您是现有的 Dynamics 365 Commerce 客户，已经部署了电子商务站点而未选择使用评分和评价，但现在想要使用 Dynamics 365 Commerce 包中的评分和评价，请提交服务请求。</span><span class="sxs-lookup"><span data-stu-id="c3664-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="c3664-118">有关如何提交服务请求的信息，请参阅[提交服务请求流程](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="c3664-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="c3664-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="c3664-119">Additional resources</span></span>

[<span data-ttu-id="c3664-120">评分和评价概览</span><span class="sxs-lookup"><span data-stu-id="c3664-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="c3664-121">管理评分和评价</span><span class="sxs-lookup"><span data-stu-id="c3664-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="c3664-122">配置评分和评价</span><span class="sxs-lookup"><span data-stu-id="c3664-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="c3664-123">在 Dynamics 365 Commerce 中同步产品评分</span><span class="sxs-lookup"><span data-stu-id="c3664-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


