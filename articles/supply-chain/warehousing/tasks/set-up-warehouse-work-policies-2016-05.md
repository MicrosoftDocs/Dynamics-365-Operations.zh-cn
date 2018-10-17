--- 
title: "设置仓库工作策略（申请表，2016 年 5 月）"
description: "仓库流程不是始终包括仓库工作。"
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="42a6f-103">设置仓库工作策略（申请表，2016 年 5 月）</span><span class="sxs-lookup"><span data-stu-id="42a6f-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42a6f-104">仓库流程不是始终包括仓库工作。</span><span class="sxs-lookup"><span data-stu-id="42a6f-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="42a6f-105">通过定义工作策略，您可以防止为原材料领料创建工作，并将一组产品的成品储存在特定位置。</span><span class="sxs-lookup"><span data-stu-id="42a6f-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="42a6f-106">USMF 演示数据公司用于创建此记录。</span><span class="sxs-lookup"><span data-stu-id="42a6f-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="42a6f-107">此任务指南需要 Dynamics AX 应用程序 7.0.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="42a6f-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="42a6f-108">转到“仓库管理”>“设置”>“工作”>“工作策略”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="42a6f-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-109">Click New.</span></span>
3. <span data-ttu-id="42a6f-110">在“工作策略名称”字段中，键入“无储存工作”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="42a6f-111">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-111">Click Save.</span></span>
5. <span data-ttu-id="42a6f-112">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-112">Click Add.</span></span>
6. <span data-ttu-id="42a6f-113">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="42a6f-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="42a6f-114">在“工作订单类型”字段中，选择“成品储存”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="42a6f-115">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-115">Click Add.</span></span>
9. <span data-ttu-id="42a6f-116">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="42a6f-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="42a6f-117">在“工作订单类型”字段中，选择“联产品和副产品储存”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="42a6f-118">展开“库存库位”部分。</span><span class="sxs-lookup"><span data-stu-id="42a6f-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="42a6f-119">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-119">Click Add.</span></span>
13. <span data-ttu-id="42a6f-120">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="42a6f-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="42a6f-121">在仓库列表中，输入 '51'。</span><span class="sxs-lookup"><span data-stu-id="42a6f-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="42a6f-122">在“位置”字段中，输入或选择 '001'。</span><span class="sxs-lookup"><span data-stu-id="42a6f-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="42a6f-123">展开“产品”部分。</span><span class="sxs-lookup"><span data-stu-id="42a6f-123">Expand the Products section.</span></span>
17. <span data-ttu-id="42a6f-124">在“产品选择”字段中，选择“已选择”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="42a6f-125">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-125">Click Add.</span></span>
19. <span data-ttu-id="42a6f-126">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="42a6f-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="42a6f-127">在“物料编号”字段中，输入或选择 'L0101'。</span><span class="sxs-lookup"><span data-stu-id="42a6f-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="42a6f-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="42a6f-128">Click Save.</span></span>


