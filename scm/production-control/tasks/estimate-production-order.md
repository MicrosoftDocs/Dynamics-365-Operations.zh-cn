--- 
title: "估计生产订单"
description: "您可以使用演示数据公司 USMF 或使用您自己的数据运行该过程。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1d34a891a5b655f801e46b8c07525cdcbc7a65c8
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="estimate-a-production-order"></a><span data-ttu-id="9d479-103">估计生产订单</span><span class="sxs-lookup"><span data-stu-id="9d479-103">Estimate a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d479-104">您可以使用演示数据公司 USMF 或使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="9d479-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="9d479-105">在这两种情况下，您需要有一个状态为“已创建”的未结生产订单。</span><span class="sxs-lookup"><span data-stu-id="9d479-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="9d479-106">这是解释生产订单周期的七个步骤中的第二步。</span><span class="sxs-lookup"><span data-stu-id="9d479-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="9d479-107">估计生产订单</span><span class="sxs-lookup"><span data-stu-id="9d479-107">Estimate a production order</span></span>
1. <span data-ttu-id="9d479-108">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="9d479-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="9d479-109">选择网格中状态为“已创建”的某个订单。</span><span class="sxs-lookup"><span data-stu-id="9d479-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="9d479-110">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="9d479-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="9d479-111">单击“估计”。</span><span class="sxs-lookup"><span data-stu-id="9d479-111">Click Estimate.</span></span>
    * <span data-ttu-id="9d479-112">通过此步骤可以计算出单个生产订单的预估成本。</span><span class="sxs-lookup"><span data-stu-id="9d479-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="9d479-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9d479-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="9d479-114">查看计算明细</span><span class="sxs-lookup"><span data-stu-id="9d479-114">View the calculation details</span></span>
1. <span data-ttu-id="9d479-115">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="9d479-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="9d479-116">单击“查看计算明细”。</span><span class="sxs-lookup"><span data-stu-id="9d479-116">Click View calculation details.</span></span>
    * <span data-ttu-id="9d479-117">此页显示了成本分解情况。</span><span class="sxs-lookup"><span data-stu-id="9d479-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="9d479-118">例如，您可以查看第一成品行的单位总成本价。</span><span class="sxs-lookup"><span data-stu-id="9d479-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="9d479-119">根据物料清单、生产工艺路线和间接成本，后续行还包括很多成本。</span><span class="sxs-lookup"><span data-stu-id="9d479-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  


