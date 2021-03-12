---
title: 包括实际成本
description: 您使用“物料模型组”页的“库存模型”选项卡上的“包括实际成本”复选框来指定在为物料计算移动平均成本价时是否考虑了实际更新的交易记录。
author: AndersGirke
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5685fd384e240c1bc6236dbddf678c8d6d9c8c66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005494"
---
# <a name="include-physical-value"></a><span data-ttu-id="31cfe-103">包括实际成本</span><span class="sxs-lookup"><span data-stu-id="31cfe-103">Include physical value</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31cfe-104">您使用“物料模型组”页的“库存模型”选项卡上的“包括实际成本”复选框来指定在为物料计算移动平均成本价时是否考虑了实际更新的交易记录。</span><span class="sxs-lookup"><span data-stu-id="31cfe-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="31cfe-105">**包括实际成本** 复选框具有以下值。</span><span class="sxs-lookup"><span data-stu-id="31cfe-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="31cfe-106">值</span><span class="sxs-lookup"><span data-stu-id="31cfe-106">Value</span></span>    | <span data-ttu-id="31cfe-107">结果</span><span class="sxs-lookup"><span data-stu-id="31cfe-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31cfe-108">已选择</span><span class="sxs-lookup"><span data-stu-id="31cfe-108">Selected</span></span> | <span data-ttu-id="31cfe-109">实际更新的交易记录和财务更新的交易记录都用于计算移动平均成本价。</span><span class="sxs-lookup"><span data-stu-id="31cfe-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="31cfe-110">清除</span><span class="sxs-lookup"><span data-stu-id="31cfe-110">Cleared</span></span>  | <span data-ttu-id="31cfe-111">只有财务更新交易记录用于计算移动平均成本价。</span><span class="sxs-lookup"><span data-stu-id="31cfe-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="31cfe-112">根据您使用的库存模型，此复选框具有略微不同的效果。</span><span class="sxs-lookup"><span data-stu-id="31cfe-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="31cfe-113">如果您在使用 FIFO（先进先出）、LIFO（后进先出）或 LIFO 日期库存模型时选择了 **包括实际成本** 复选框，则库存结转也将对实际更新的交易记录做出调整。</span><span class="sxs-lookup"><span data-stu-id="31cfe-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="31cfe-114">如果在您使用这些库存模型时没有选择 **包括实际成本** 复选框，则库存结转只对财务更新交易记录进行结算。</span><span class="sxs-lookup"><span data-stu-id="31cfe-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="31cfe-115">当您使用了加权平均或加权平均日期库存模型时，不管您是否选择了 **包括实际成本** 复选框，库存结转都只结算财务更新的交易记录。</span><span class="sxs-lookup"><span data-stu-id="31cfe-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="31cfe-116">**示例 1** 您选中 **包括实际成本** 复选框并收到以下采购订单：</span><span class="sxs-lookup"><span data-stu-id="31cfe-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="31cfe-117">数量为 2 且成本价为 USD 10.00 的采购订单已更新装箱单。</span><span class="sxs-lookup"><span data-stu-id="31cfe-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated.</span></span>
-   <span data-ttu-id="31cfe-118">数量为 3 且成本价为 USD 12.00 的采购订单已更新发票。</span><span class="sxs-lookup"><span data-stu-id="31cfe-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated.</span></span>

<span data-ttu-id="31cfe-119">在此示例中，移动平均成本价将是 USD 11.20 = (2x10+3x12)/(2+3)，因为物理更新的交易记录和财务更新的交易记录都用于计算该成本价。</span><span class="sxs-lookup"><span data-stu-id="31cfe-119">In this case, the running average cost price will be USD 11.20 = (2x10+3x12)/(2+3), because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> 

<span data-ttu-id="31cfe-120">**示例 2** 您未选中 **包括实际成本** 复选框，物料设置的成本价是 USD 10.00。</span><span class="sxs-lookup"><span data-stu-id="31cfe-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> 

-   <span data-ttu-id="31cfe-121">您收到已更新装箱单的数量为 20 且成本价为 USD 12.00 的采购订单。</span><span class="sxs-lookup"><span data-stu-id="31cfe-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span>

<span data-ttu-id="31cfe-122">当过账销售订单时，过账的成本金额为 USD 10.00，因为移动平均成本价将不包括实际过账的交易记录。</span><span class="sxs-lookup"><span data-stu-id="31cfe-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> 

> [!NOTE]
> <span data-ttu-id="31cfe-123">对于比较，如果为此物料选中 **包括实际成本** 复选框，在过帐某一销售订单时，过帐的成本金额将是 USD 12.00。</span><span class="sxs-lookup"><span data-stu-id="31cfe-123">For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>
