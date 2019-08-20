---
title: 创建牌照合并的移动设备菜单项
description: 此过程显示如何为牌照合并工作创建移动设备菜单项。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc610a16f4b0e574b5d5e7f8fc9ecf1e12534645
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847295"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="e4a34-103">创建牌照合并的移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="e4a34-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4a34-104">此过程显示如何为牌照合并工作创建移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="e4a34-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="e4a34-105">这样仓库工作人员就可以将一个牌照的物料与同一个库位中的另一个牌照合并合。</span><span class="sxs-lookup"><span data-stu-id="e4a34-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="e4a34-106">例如，如果后续暂存步骤在两个工作订单中均相同，可能使用此过程，以便只需要为合并的物料执行一次工作。</span><span class="sxs-lookup"><span data-stu-id="e4a34-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="e4a34-107">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="e4a34-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="e4a34-108">此任务通常由仓库管理员完成。</span><span class="sxs-lookup"><span data-stu-id="e4a34-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="e4a34-109">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="e4a34-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="e4a34-110">转到“仓库管理”>“设置”>“移动设备”>“移动设备菜单项”。</span><span class="sxs-lookup"><span data-stu-id="e4a34-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="e4a34-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="e4a34-111">Click New.</span></span>
3. <span data-ttu-id="e4a34-112">在“菜单项名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e4a34-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="e4a34-113">在“标题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="e4a34-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="e4a34-114">在“模式”字段中，选择“间接”。</span><span class="sxs-lookup"><span data-stu-id="e4a34-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="e4a34-115">在“活动代码”字段中，选择“合并牌照”。</span><span class="sxs-lookup"><span data-stu-id="e4a34-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

