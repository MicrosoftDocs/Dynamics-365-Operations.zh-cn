---
title: 客户会员卡和奖励积分
description: 本主题介绍有关双写入中的客户会员卡和奖励积分的数据的集成。
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747979"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="be078-103">客户会员卡和奖励积分</span><span class="sxs-lookup"><span data-stu-id="be078-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="be078-104">企业根据客户的购物和消费模式对客户进行分类并提供完善的服务。</span><span class="sxs-lookup"><span data-stu-id="be078-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="be078-105">例如，Dynamics 365 Commerce 具有推进和处理客户会员卡、奖励积分、基于会员制的定价和基于奖励的购物体验的基础结构和功能。</span><span class="sxs-lookup"><span data-stu-id="be078-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="be078-106">当有关 Commerce 中客户会员卡和奖励积分的数据同步到 Dataverse 时，客户参与应用可以使用该数据。</span><span class="sxs-lookup"><span data-stu-id="be078-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="be078-107">例如，Dynamics 365 Customer Service 用户可以使用数据通过帮助台提供相同的完善服务。</span><span class="sxs-lookup"><span data-stu-id="be078-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="be078-108">模板</span><span class="sxs-lookup"><span data-stu-id="be078-108">Templates</span></span>

| <span data-ttu-id="be078-109">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="be078-109">Finance and Operations apps</span></span> | <span data-ttu-id="be078-110">Dynamics 365 中的模型驱动应用</span><span class="sxs-lookup"><span data-stu-id="be078-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="be078-111">说明</span><span class="sxs-lookup"><span data-stu-id="be078-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="be078-112">会员卡</span><span class="sxs-lookup"><span data-stu-id="be078-112">Loyalty card</span></span>                | <span data-ttu-id="be078-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="be078-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="be078-114">此模板同步有关客户会员卡的信息。</span><span class="sxs-lookup"><span data-stu-id="be078-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="be078-115">会员奖励分</span><span class="sxs-lookup"><span data-stu-id="be078-115">Loyalty reward points</span></span>       | <span data-ttu-id="be078-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="be078-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="be078-117">此模板同步有关客户奖励积分的信息。</span><span class="sxs-lookup"><span data-stu-id="be078-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]