---
title: "批次和牌照确认"
description: "此主题描述如何从移动设备设置和应用批次和牌照确认。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6454335989fe03a7332b6fb956667850896ffaf4
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="dbc1a-103">批次和牌照确认</span><span class="sxs-lookup"><span data-stu-id="dbc1a-103">Batch and license plate confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dbc1a-104">批次确认允许您从移动设备确认正领取正确的批次。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="dbc1a-105">在仅物料上方批次的初始领料工作上，上方批次表示高于搜索层次结构中的库位的批次范围，您必须验证领取的批次与工作行上的批次匹配。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="dbc1a-106">牌照确认允许您从移动设备确认正领取正确的牌照。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="dbc1a-107">从暂存位置执行领料工作时，您必须核实已领取的牌照与该工作关联的牌照匹配。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="dbc1a-108">如果通过扫描牌照启动该工作，将跳过此确认步骤。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="dbc1a-109">适用情况</span><span class="sxs-lookup"><span data-stu-id="dbc1a-109">Where it applies</span></span>
<span data-ttu-id="dbc1a-110">确认在以下情况下适用：</span><span class="sxs-lookup"><span data-stu-id="dbc1a-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="dbc1a-111">批次确认适用于物料上方批次的初始领料工作。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="dbc1a-112">确认牌照适用于从暂存位置领料。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="dbc1a-113">设置批次和牌照确认</span><span class="sxs-lookup"><span data-stu-id="dbc1a-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="dbc1a-114">您可以从移动设备菜单项配置批次和牌照确认。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="dbc1a-115">从移动设备菜单项输入工作确认设置。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="dbc1a-116">为批次或牌照确认选择选项。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="dbc1a-117">两个选项对未启用自动确认的工作类型领料均可用。</span><span class="sxs-lookup"><span data-stu-id="dbc1a-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  
