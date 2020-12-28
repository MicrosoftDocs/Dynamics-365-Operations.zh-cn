---
title: 运输管理杂项费用
description: 此主题说明运输产生的费用为何必须与费用代码关联。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2020
ms.locfileid: "4423468"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="1a048-103">运输管理杂项费用</span><span class="sxs-lookup"><span data-stu-id="1a048-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a048-104">与所有杂项费用一样，运输产生的费用必须与费用代码关联。</span><span class="sxs-lookup"><span data-stu-id="1a048-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="1a048-105">否则，它们将不会作为杂项费用添加回订单中。</span><span class="sxs-lookup"><span data-stu-id="1a048-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="1a048-106">**费用代码** 确定对于添加费用的订单和订单行费用如何计算。</span><span class="sxs-lookup"><span data-stu-id="1a048-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="1a048-107">转到 **运输管理 > 设置 > 评级 > 杂项费用** 定义确定特定 **费用代码** 何时应用于费用的合格条件。</span><span class="sxs-lookup"><span data-stu-id="1a048-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="1a048-108">每个 **费用模块** 设置（*客户* 和 *供应商*）至少应有一个将 **杂项费用类型** 设置为 *无* 的设置。</span><span class="sxs-lookup"><span data-stu-id="1a048-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="1a048-109">如果缺少此设置，杂项费用 *不* 会被添加到订单中。</span><span class="sxs-lookup"><span data-stu-id="1a048-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>
