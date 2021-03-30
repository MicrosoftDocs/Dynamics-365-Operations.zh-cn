---
title: 生产过帐
description: 本文提供有关生产流程中不同过帐类型的信息。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fa5040e1923a1ff7135f1311a260f65c75b8ead
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245267"
---
# <a name="production-posting"></a><span data-ttu-id="8f90f-103">生产过帐</span><span class="sxs-lookup"><span data-stu-id="8f90f-103">Production posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f90f-104">本文提供有关生产流程中不同过帐类型的信息。</span><span class="sxs-lookup"><span data-stu-id="8f90f-104">This article provides information about different types of postings in the production process.</span></span>

<span data-ttu-id="8f90f-105">生产过帐活动遵循以下各节中描述的生产流程。</span><span class="sxs-lookup"><span data-stu-id="8f90f-105">Production posting activities follow production processes that are described in the sections below.</span></span>

## <a name="material-consumption"></a><span data-ttu-id="8f90f-106">物料消耗量</span><span class="sxs-lookup"><span data-stu-id="8f90f-106">Material consumption</span></span>
<span data-ttu-id="8f90f-107">在过帐生产领料单日记帐时，将物料登记为在生产中被消耗。</span><span class="sxs-lookup"><span data-stu-id="8f90f-107">Materials are registered as consumed during production when the production picking list journal is posted.</span></span> <span data-ttu-id="8f90f-108">此流程生成扣减现有库存量的发货交易记录。</span><span class="sxs-lookup"><span data-stu-id="8f90f-108">This process generates issue transactions that deduct the on-hand inventory.</span></span> <span data-ttu-id="8f90f-109">在生产参数中，您可以指定是否应在分类帐中过帐生产中的原材料（在制品 \[WIP\]）的值。</span><span class="sxs-lookup"><span data-stu-id="8f90f-109">In the production parameters, you can specify whether the value of raw materials that are in progress (work in process \[WIP\]) should be posted in the ledger.</span></span> <span data-ttu-id="8f90f-110">随后，生产中的原材料 (WIP) 的值将过帐到专用领料单帐户和专用领料单对方科目。</span><span class="sxs-lookup"><span data-stu-id="8f90f-110">The value of raw materials that are in progress (WIP) is then posted to a dedicated Picking list account and a dedicated Picking list offset account.</span></span>

## <a name="time-consumption"></a><span data-ttu-id="8f90f-111">时间消耗量</span><span class="sxs-lookup"><span data-stu-id="8f90f-111">Time consumption</span></span>
<span data-ttu-id="8f90f-112">工作人员在生产作业上花费的时间将记录在工艺卡日记帐或作业卡日记帐中。</span><span class="sxs-lookup"><span data-stu-id="8f90f-112">The time that workers spend on production jobs is recorded in the Route card journal or the Job card journal.</span></span> <span data-ttu-id="8f90f-113">在过帐这些日记帐时，将处理过帐到生产中 (WIP) 的资源的专用帐户的分类帐。</span><span class="sxs-lookup"><span data-stu-id="8f90f-113">When these journals are posted, ledger posting to a dedicated account for resources that are in progress (WIP) is processed.</span></span> <span data-ttu-id="8f90f-114">此过帐表示在生产订单上花费的时间的值。</span><span class="sxs-lookup"><span data-stu-id="8f90f-114">This posting represents the value of the time that is spent on the production order.</span></span> <span data-ttu-id="8f90f-115">在将生产订单登记为已结束后，将结算 WIP 帐户。</span><span class="sxs-lookup"><span data-stu-id="8f90f-115">After the production order is registered as ended, the WIP accounts are settled.</span></span>

## <a name="reporting-finished-goods-and-error-quantities"></a><span data-ttu-id="8f90f-116">报告成品和残次数量</span><span class="sxs-lookup"><span data-stu-id="8f90f-116">Reporting finished goods and error quantities</span></span>
<span data-ttu-id="8f90f-117">在生产订单报告为完工入库时，在库存管理中通过完工入库的日记帐更新已完成成品的数量。</span><span class="sxs-lookup"><span data-stu-id="8f90f-117">When a production order is reported as finished, the quantity of the finished goods that have been completed is updated in Inventory management through the Report as finished journal.</span></span> <span data-ttu-id="8f90f-118">如果您在使用 WIP 会计（可在生产参数中设置），则生成分类帐日记帐以减少 WIP 帐户和增加成品库存。</span><span class="sxs-lookup"><span data-stu-id="8f90f-118">If you're using WIP accounting, which can be set up in the production parameters, a ledger journal is made to reduce the WIP accounts and increase the inventory of the finished goods.</span></span> <span data-ttu-id="8f90f-119">日记帐使用为产品定义的标准成本。</span><span class="sxs-lookup"><span data-stu-id="8f90f-119">The journal uses the standard cost that is defined for the product.</span></span>

## <a name="ending-the-production-order"></a><span data-ttu-id="8f90f-120">结束生产订单</span><span class="sxs-lookup"><span data-stu-id="8f90f-120">Ending the production order</span></span>
<span data-ttu-id="8f90f-121">在结束生产订单前，为生成的数量计算实际成本。</span><span class="sxs-lookup"><span data-stu-id="8f90f-121">Before a production order is ended, actual costs are calculated for the quantity that was produced.</span></span> <span data-ttu-id="8f90f-122">物料、人工和开销的所有预估成本都被冲销，并用实际成本替代。</span><span class="sxs-lookup"><span data-stu-id="8f90f-122">All estimated costs of material, labor, and overhead are reversed and replaced with actual costs.</span></span> <span data-ttu-id="8f90f-123">成品的总计成本从库存“收货”帐户中借记，并贷记到库存“发货”帐户。</span><span class="sxs-lookup"><span data-stu-id="8f90f-123">The overall cost of the finished item is debited from the inventory Receipt account and credited to the inventory Issues account.</span></span> <span data-ttu-id="8f90f-124">如果您在运行成本计算时选中 **结束作业** 复选框，则生产订单的状态将更改为 **已结束**。</span><span class="sxs-lookup"><span data-stu-id="8f90f-124">If you select the **End job** check box when you run the cost calculation, the status of the production order is changed to **Ended**.</span></span> <span data-ttu-id="8f90f-125">此状态将阻止将任何额外成本无意中过帐到已完成的生产订单。</span><span class="sxs-lookup"><span data-stu-id="8f90f-125">This status prevents any additional costs from being unintentionally posted to a completed production order.</span></span> <span data-ttu-id="8f90f-126">您可以指定应将完工入库期间报告的残次数量的值分配到报告为已完工入库的完好数量。</span><span class="sxs-lookup"><span data-stu-id="8f90f-126">You can specify that the value of error quantities that are reported during reporting as finished should be allocated to the good quantities that are reported as finished.</span></span> <span data-ttu-id="8f90f-127">或者，您可以指定应将残次数量的值过帐到专用的报废科目。</span><span class="sxs-lookup"><span data-stu-id="8f90f-127">Alternatively, you can specify that the value of error quantities should be posted to a dedicated scrap account.</span></span>

## <a name="controlling-the-level-of-ledger-posting"></a><span data-ttu-id="8f90f-128">控制分类帐过帐的级别</span><span class="sxs-lookup"><span data-stu-id="8f90f-128">Controlling the level of ledger posting</span></span>
<span data-ttu-id="8f90f-129">在 **生产控制参数** 中，可以使用 **分类帐过帐** 字段设置生产流程的分类帐过帐级别。</span><span class="sxs-lookup"><span data-stu-id="8f90f-129">In the **Production control parameters**, you can use the **Ledger posting** field to set the level of ledger posting for production processes.</span></span> <span data-ttu-id="8f90f-130">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="8f90f-130">The following values are available:</span></span>

-   <span data-ttu-id="8f90f-131">**物料和资源** – 为原材料和成品使用在物料组上设置的会计科目。</span><span class="sxs-lookup"><span data-stu-id="8f90f-131">**Item and resource** – Use the ledger accounts that are set up on the item groups for raw materials and finished goods.</span></span> <span data-ttu-id="8f90f-132">从工艺路线工序中的资源或资源组提取时间消耗量的 WIP。</span><span class="sxs-lookup"><span data-stu-id="8f90f-132">WIP for time consumption is taken from resource or resource group from the route operations.</span></span>
-   <span data-ttu-id="8f90f-133">**物料和类别** – 为原材料和成品使用在物料组上设置的会计科目。</span><span class="sxs-lookup"><span data-stu-id="8f90f-133">**Item and category** – Use the ledger accounts that are set up on the item groups for raw materials and finished goods.</span></span> <span data-ttu-id="8f90f-134">从与工艺路线工序关联的成本类别提取时间消耗量的 WIP。</span><span class="sxs-lookup"><span data-stu-id="8f90f-134">WIP for time consumption is taken from the cost categories that are associated with the route operations.</span></span>
-   <span data-ttu-id="8f90f-135">**生产组** – 为材料和时间消耗量使用在生产组中设置的会计科目。</span><span class="sxs-lookup"><span data-stu-id="8f90f-135">**Production groups** – Use the ledger accounts that are set up on the production groups for both material and time consumption.</span></span> <span data-ttu-id="8f90f-136">生产组与已发布产品关联，并会在创建生产订单时复制到这些订单。</span><span class="sxs-lookup"><span data-stu-id="8f90f-136">The production groups are associated with the released products and copied to the production orders when those orders are created.</span></span> <span data-ttu-id="8f90f-137">随后，对生产订单的过帐将在与生产订单关联的生产组之后进行。</span><span class="sxs-lookup"><span data-stu-id="8f90f-137">The posting on the production orders will then follow the production groups that are associated with the production order.</span></span>

<span data-ttu-id="8f90f-138">**注意：** 如果使用了计算成品成本的标准方法，则最终交易记录中将反映此情况。</span><span class="sxs-lookup"><span data-stu-id="8f90f-138">**Note:** If the standard method for calculating the cost of the finished item was used, the final transactions reflect this fact.</span></span> <span data-ttu-id="8f90f-139">如果实际成本和使用标准方法计算的成本之间存在差别，它将过帐到显示利润或损失的科目中。</span><span class="sxs-lookup"><span data-stu-id="8f90f-139">If actual costs and the costs that are calculated by using the standard method differ, the difference is posted to the account that shows profit or loss.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]