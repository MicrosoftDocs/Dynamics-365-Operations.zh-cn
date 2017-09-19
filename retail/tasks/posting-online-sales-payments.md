--- 
title: "过帐联机销售和付款"
description: "此程序会逐步演示如何配置和运行某一重复批处理作业，以创建针对在线商店交易的销售订单和付款。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e8c3f861a53a3f5c2de29248523ff4efd5e1d072
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="3b5af-103">过帐联机销售和付款</span><span class="sxs-lookup"><span data-stu-id="3b5af-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3b5af-104">此程序会逐步演示如何配置和运行某一重复批处理作业，以创建针对在线商店交易的销售订单和付款。</span><span class="sxs-lookup"><span data-stu-id="3b5af-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="3b5af-105">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="3b5af-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3b5af-106">转至“所有工作区”>“零售商店财务”。</span><span class="sxs-lookup"><span data-stu-id="3b5af-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="3b5af-107">单击“同步订单”。</span><span class="sxs-lookup"><span data-stu-id="3b5af-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="3b5af-108">在“组织层次结构”字段中，选择“零售商店(按地区)”。</span><span class="sxs-lookup"><span data-stu-id="3b5af-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="3b5af-109">选择一个特定在线商店，如果您想要为一组商店创建批处理作业，则选择一个节点。</span><span class="sxs-lookup"><span data-stu-id="3b5af-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="3b5af-110">单击箭头以添加您的选择。</span><span class="sxs-lookup"><span data-stu-id="3b5af-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="3b5af-111">单击“后台运行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="3b5af-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="3b5af-112">选中或取消选中“批处理”复选框。</span><span class="sxs-lookup"><span data-stu-id="3b5af-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="3b5af-113">单击“再循环”。</span><span class="sxs-lookup"><span data-stu-id="3b5af-113">Click Recurrence.</span></span>
7. <span data-ttu-id="3b5af-114">选择“无结束日期”选项。</span><span class="sxs-lookup"><span data-stu-id="3b5af-114">Select the No end date option.</span></span>
8. <span data-ttu-id="3b5af-115">在“盘点”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="3b5af-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="3b5af-116">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3b5af-116">Click OK.</span></span>
10. <span data-ttu-id="3b5af-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3b5af-117">Click OK.</span></span>

