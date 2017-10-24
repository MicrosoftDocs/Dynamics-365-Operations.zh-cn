---
title: "将生产订单报告为已完工入库"
description: "完工入库是生产阶段。 在此阶段，将报告成品并将其从生产订单移到库存。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f8adcbcc2157058151c26179eb2eb925b0092d2d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="a41f2-104">将生产订单报告为已完工入库</span><span class="sxs-lookup"><span data-stu-id="a41f2-104">Report production orders as finished</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a41f2-105">完工入库是生产阶段。</span><span class="sxs-lookup"><span data-stu-id="a41f2-105">Report as finished is a production stage.</span></span> <span data-ttu-id="a41f2-106">在此阶段，将报告成品并将其从生产订单移到库存。</span><span class="sxs-lookup"><span data-stu-id="a41f2-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="a41f2-107">在生产订单上将成品数量报告为完工入库时，此数量将在库存中更新为现有量。</span><span class="sxs-lookup"><span data-stu-id="a41f2-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="a41f2-108">原始计划订单数量的部分数量可报告为完工入库。</span><span class="sxs-lookup"><span data-stu-id="a41f2-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="a41f2-109">也可以在将数量报告为完工入库时报告具有关联的错误原因的错误数量。</span><span class="sxs-lookup"><span data-stu-id="a41f2-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="a41f2-110">在生产订单达到“报告为完工入库”阶段时，表示在生产订单上不再报告其他数量。</span><span class="sxs-lookup"><span data-stu-id="a41f2-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="a41f2-111">以下特征也与**“完工入库”**流程关联：</span><span class="sxs-lookup"><span data-stu-id="a41f2-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="a41f2-112">可以设置与报告的数量成比例的原材料消耗量和时间（反向刷新）</span><span class="sxs-lookup"><span data-stu-id="a41f2-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="a41f2-113">可以为已为仓库流程启用的物料生成存储工作。</span><span class="sxs-lookup"><span data-stu-id="a41f2-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="a41f2-114">成品的计划或标准成本价值可设置为报告给会计科目。</span><span class="sxs-lookup"><span data-stu-id="a41f2-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="a41f2-115">可基于质量关联的设置为报告的数量创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="a41f2-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="a41f2-116">数量将报告到输出位置。</span><span class="sxs-lookup"><span data-stu-id="a41f2-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="a41f2-117">随后，生成仓库工作以将数量从输出位置移至由存储工作的位置指令定义的最终目标位置。</span><span class="sxs-lookup"><span data-stu-id="a41f2-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="a41f2-118">在已设置质量关联的情况下将生成订单报告为完工入库时，可以创建质检订单。</span><span class="sxs-lookup"><span data-stu-id="a41f2-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="a41f2-119">将生产订单设置为完工入库</span><span class="sxs-lookup"><span data-stu-id="a41f2-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="a41f2-120">可以通过标准生产订单更新功能、工艺卡日记帐和作业卡日记帐或日记帐**“完工入库”**，将生产订单设置为**“完工入库”**。</span><span class="sxs-lookup"><span data-stu-id="a41f2-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="a41f2-121">也可以在报告生产订单的上一个作业时，通过作业卡终端页和作业卡设备页将阶段更新为**“完工入库”**。</span><span class="sxs-lookup"><span data-stu-id="a41f2-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="a41f2-122">最后，您可以启用**“完工入库”**选项作为手持式仓库设备解决方案的流程。</span><span class="sxs-lookup"><span data-stu-id="a41f2-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




