---
title: 创建牌照合并的移动设备菜单项
description: 此过程显示如何为牌照合并工作创建移动设备菜单项。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1dfb0bb2db5690a966d70f96a3bba2d60833abd4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830994"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="7ed14-103">创建牌照合并的移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="7ed14-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ed14-104">此过程显示如何为牌照合并工作创建移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="7ed14-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="7ed14-105">这样仓库工作人员就可以将一个牌照的物料与同一个库位中的另一个牌照合并合。</span><span class="sxs-lookup"><span data-stu-id="7ed14-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="7ed14-106">例如，如果后续暂存步骤在两个工作订单中均相同，可能使用此过程，以便只需要为合并的物料执行一次工作。</span><span class="sxs-lookup"><span data-stu-id="7ed14-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="7ed14-107">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="7ed14-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="7ed14-108">此任务通常由仓库管理员完成。</span><span class="sxs-lookup"><span data-stu-id="7ed14-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="7ed14-109">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="7ed14-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="7ed14-110">转到“仓库管理”>“设置”>“移动设备”>“移动设备菜单项”。</span><span class="sxs-lookup"><span data-stu-id="7ed14-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="7ed14-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7ed14-111">Click New.</span></span>
3. <span data-ttu-id="7ed14-112">在“菜单项名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7ed14-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="7ed14-113">在“标题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7ed14-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="7ed14-114">在“模式”字段中，选择“间接”。</span><span class="sxs-lookup"><span data-stu-id="7ed14-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="7ed14-115">在“活动代码”字段中，选择“合并牌照”。</span><span class="sxs-lookup"><span data-stu-id="7ed14-115">In the Activity code field, select 'Consolidate license plates'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]