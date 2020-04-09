---
title: 定义连续性计划
description: 本主题逐步演示如何设置连续性计划（也称为重复订单）。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06fd1e23ad84fdc5e94e309717d5a96fbff45035
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140891"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="34c74-103">定义连续性计划</span><span class="sxs-lookup"><span data-stu-id="34c74-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34c74-104">本主题逐步演示如何设置连续性计划（也称为重复订单）。</span><span class="sxs-lookup"><span data-stu-id="34c74-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="34c74-105">本主题使用演示数据中的公司 USRT。</span><span class="sxs-lookup"><span data-stu-id="34c74-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="34c74-106">创建连续性计划</span><span class="sxs-lookup"><span data-stu-id="34c74-106">Create continuity program</span></span>
1. <span data-ttu-id="34c74-107">转至“Retail 和 Commerce”>“连续性”>“连续性计划”。</span><span class="sxs-lookup"><span data-stu-id="34c74-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="34c74-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="34c74-108">Click New.</span></span>
3. <span data-ttu-id="34c74-109">在“计划 ID”字段中，键入连续性计划 ID。</span><span class="sxs-lookup"><span data-stu-id="34c74-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="34c74-110">在“订单开始”字段中，选择“第一个事件”。</span><span class="sxs-lookup"><span data-stu-id="34c74-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="34c74-111">如果客户为连续性计划下一个新订单，产品将有两个装运选项：1.</span><span class="sxs-lookup"><span data-stu-id="34c74-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="34c74-112">第一个事件：将装运连续性计划中的第一个产品。</span><span class="sxs-lookup"><span data-stu-id="34c74-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="34c74-113">2</span><span class="sxs-lookup"><span data-stu-id="34c74-113">2.</span></span> <span data-ttu-id="34c74-114">当前事件：将装运当前产品。</span><span class="sxs-lookup"><span data-stu-id="34c74-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="34c74-115">例如，</span><span class="sxs-lookup"><span data-stu-id="34c74-115">For example.</span></span> <span data-ttu-id="34c74-116">计划中三个月，客户将收到计划中的第三个产品。</span><span class="sxs-lookup"><span data-stu-id="34c74-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="34c74-117">选择“是”提示输入订单的开始日期。</span><span class="sxs-lookup"><span data-stu-id="34c74-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="34c74-118">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="34c74-118">Click Add line.</span></span>
7. <span data-ttu-id="34c74-119">在“物料编号”字段中，键入第一个产品的物料编号（“0013”）。</span><span class="sxs-lookup"><span data-stu-id="34c74-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="34c74-120">键入“CP”。</span><span class="sxs-lookup"><span data-stu-id="34c74-120">Type 'CP'.</span></span>
9. <span data-ttu-id="34c74-121">输入第一个产品可供订购的日期。</span><span class="sxs-lookup"><span data-stu-id="34c74-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="34c74-122">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="34c74-122">Click Add line.</span></span>
11. <span data-ttu-id="34c74-123">在“物料编号”字段中，键入“0014”。</span><span class="sxs-lookup"><span data-stu-id="34c74-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="34c74-124">在“日期间隔代码”字段中，清除值，使该字段为空。</span><span class="sxs-lookup"><span data-stu-id="34c74-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="34c74-125">对于此过程，请清除日期间隔。</span><span class="sxs-lookup"><span data-stu-id="34c74-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="34c74-126">您将把该日期设置为从第一个物料的开始日期的增量。</span><span class="sxs-lookup"><span data-stu-id="34c74-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="34c74-127">在这里输入产品的装运间隔。</span><span class="sxs-lookup"><span data-stu-id="34c74-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="34c74-128">键入“30”。</span><span class="sxs-lookup"><span data-stu-id="34c74-128">Type '30'.</span></span>
    * <span data-ttu-id="34c74-129">对于每月计划，将为间隔输入 30 天。</span><span class="sxs-lookup"><span data-stu-id="34c74-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="34c74-130">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="34c74-130">Click Add line.</span></span>
15. <span data-ttu-id="34c74-131">在“物料编号”字段中，键入“0015”。</span><span class="sxs-lookup"><span data-stu-id="34c74-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="34c74-132">键入“结束”。</span><span class="sxs-lookup"><span data-stu-id="34c74-132">Type 'End'.</span></span>
17. <span data-ttu-id="34c74-133">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="34c74-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="34c74-134">分配给连续性物料</span><span class="sxs-lookup"><span data-stu-id="34c74-134">Assign to continuity item</span></span>
1. <span data-ttu-id="34c74-135">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="34c74-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="34c74-136">选择物料“0016”。</span><span class="sxs-lookup"><span data-stu-id="34c74-136">Select item '0016'.</span></span>
    * <span data-ttu-id="34c74-137">对于此过程，将选择物料编号 0016。</span><span class="sxs-lookup"><span data-stu-id="34c74-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="34c74-138">通常您将已经创建了一个已发布产品，在呼叫中心中为该产品下销售订单时应用了更多连续性业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="34c74-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="34c74-139">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="34c74-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="34c74-140">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="34c74-140">Click Edit.</span></span>
5. <span data-ttu-id="34c74-141">展开或折叠“销售”部分。</span><span class="sxs-lookup"><span data-stu-id="34c74-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="34c74-142">在这里输入此物料代表的连续性计划。</span><span class="sxs-lookup"><span data-stu-id="34c74-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="34c74-143">键入您之前创建的计划 ID。</span><span class="sxs-lookup"><span data-stu-id="34c74-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="34c74-144">此物料在呼叫中心售出时，将从所选连续性计划应用更多业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="34c74-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="34c74-145">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="34c74-145">Click Save.</span></span>

