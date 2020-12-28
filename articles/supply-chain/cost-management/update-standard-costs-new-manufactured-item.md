---
title: 为新的制造物料更新标准成本
description: 本文提供更新新制造物料的标准成本的指导。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ebd53d66eb81bbee9d3e67d05102c8df413d2a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422959"
---
# <a name="update-standard-costs-for-a-new-manufactured-item"></a><span data-ttu-id="22299-103">为新的制造物料更新标准成本</span><span class="sxs-lookup"><span data-stu-id="22299-103">Update standard costs for a new manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22299-104">本文提供更新新制造物料的标准成本的指导。</span><span class="sxs-lookup"><span data-stu-id="22299-104">This article provides guidance for updating standard costs for a new manufactured item.</span></span> 

<span data-ttu-id="22299-105">以下准则假定将双版本方法用于更新标准成本。</span><span class="sxs-lookup"><span data-stu-id="22299-105">The following guidelines assume that you use a two-version approach to update standard costs.</span></span> <span data-ttu-id="22299-106">应用此方法，一个成本计算版本包含为冻结期间最初定义的标准成本，第二个成本计算版本包含属于新制造的物料的递增更新。</span><span class="sxs-lookup"><span data-stu-id="22299-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates that pertain to the new manufactured items.</span></span> <span data-ttu-id="22299-107">将递增更新输入为第二个成本计算版本中的成本记录，最终被启用。</span><span class="sxs-lookup"><span data-stu-id="22299-107">The incremental updates are entered as cost records in the second costing version, and eventually they are enabled.</span></span> <span data-ttu-id="22299-108">双版本方法需要您定义第二个成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="22299-108">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="22299-109">以下是定义此成本计算版本的准则：</span><span class="sxs-lookup"><span data-stu-id="22299-109">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="22299-110">分配 **标准成本** 的成本计算类型。</span><span class="sxs-lookup"><span data-stu-id="22299-110">Assign a costing type of **Standard cost**.</span></span>
-   <span data-ttu-id="22299-111">分配指示成本计算版本内容的重要标识符，例如 **2016-UPDATES**。</span><span class="sxs-lookup"><span data-stu-id="22299-111">Assign a significant identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="22299-112">在 **允许价格类型** 字段组中，确保将 **成本价** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="22299-112">In the **Allow price types** field group, make sure that **Cost price** is set to **Yes**.</span></span>
-   <span data-ttu-id="22299-113">允许为所有站点输入成本记录（即，将 **站点** 字段保留为空）。</span><span class="sxs-lookup"><span data-stu-id="22299-113">Allow cost records to be entered for all sites (that is, leave the **Site** field blank).</span></span> <span data-ttu-id="22299-114">如果您输入某一站点，成本记录可以只为该站点输入。</span><span class="sxs-lookup"><span data-stu-id="22299-114">If you enter a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="22299-115">使用 **有效** 回退原则。</span><span class="sxs-lookup"><span data-stu-id="22299-115">Use a fallback principle of **Active**.</span></span>

<span data-ttu-id="22299-116">若要在整个冻结期间中添加新的制造物料，请遵循这些步骤。</span><span class="sxs-lookup"><span data-stu-id="22299-116">To add new manufacturing items throughout the frozen period, follow these steps.</span></span>

1.  <span data-ttu-id="22299-117">使用 **成本计算版本设置** 页可以使成本记录输入到包含增量更新的第二个成本计算版本中。</span><span class="sxs-lookup"><span data-stu-id="22299-117">Use the **Costing version setup** page to enable cost records to be entered into the second costing version that contains the incremental updates.</span></span> <span data-ttu-id="22299-118">阻止启用未决成本，将在未决成本已完全和精确定义后允许启用。</span><span class="sxs-lookup"><span data-stu-id="22299-118">Prevent the activation of pending costs, where activation is allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="22299-119">指示空的开始日期作为成本计算版本中的策略，然后输入您输入每个成本记录时的开始日期。</span><span class="sxs-lookup"><span data-stu-id="22299-119">Indicate a blank from-date as a policy in the costing version, and then enter the from-date when you enter each cost record.</span></span> <span data-ttu-id="22299-120">该开始日期应表示将采购或制造新物料之前的日期。</span><span class="sxs-lookup"><span data-stu-id="22299-120">The from-date should represent a date before the new items are purchased or manufactured.</span></span>
2.  <span data-ttu-id="22299-121">使用 **物料价格** 页可为新的采购物料输入成本记录。</span><span class="sxs-lookup"><span data-stu-id="22299-121">Use the **Item price** page to enter cost records for new purchased items.</span></span> <span data-ttu-id="22299-122">对于每个成本记录，输入包含增量更新的成本计算版本，并且使用在新制造物料的预期制造日期之前的开始日期。</span><span class="sxs-lookup"><span data-stu-id="22299-122">For each cost record, enter the costing version that contains incremental updates, and use a from-date that comes before the expected manufacturing date for new manufactured items.</span></span>
3.  <span data-ttu-id="22299-123">通过使用 **计算** 页计算新制造物料的成本。</span><span class="sxs-lookup"><span data-stu-id="22299-123">Calculate the cost of new manufactured items by using the **Calculation** page.</span></span> <span data-ttu-id="22299-124">从 **成本计算版本维护** 页打开 **计算** 页，然后选择包含增量更新的成本计算版本。</span><span class="sxs-lookup"><span data-stu-id="22299-124">Open the **Calculation** page from the **Costing version maintenance** page, and then select the costing version that contains the incremental updates.</span></span> <span data-ttu-id="22299-125">使用选择条件可以指定新的制造物料及其制造组件之一。</span><span class="sxs-lookup"><span data-stu-id="22299-125">Use the selection criteria to specify the new manufactured item and any one of its manufactured components.</span></span> <span data-ttu-id="22299-126">在多级产品结构内，您可能还有必要指定将新制造物料作为组件包含的任何父级物料。</span><span class="sxs-lookup"><span data-stu-id="22299-126">In a multilevel product structure, you might also have to specify any parent item that contains the new manufactured items as a component.</span></span> <span data-ttu-id="22299-127">为与开始制造新的制造物料相对应的物料清单 (BOM) 计算输入开始日期。</span><span class="sxs-lookup"><span data-stu-id="22299-127">Enter a from-date for the bill of materials (BOM) calculation that corresponds to the start of manufacturing for the new manufactured items.</span></span> <span data-ttu-id="22299-128">该开始日期应在物料的物料清单版本和工艺路线版本的生效日期内。</span><span class="sxs-lookup"><span data-stu-id="22299-128">The from-date should be in the effective dates for the item’s BOM version and route version.</span></span> <span data-ttu-id="22299-129">**注意：** 缺少成本记录可能指示新的制造物料。</span><span class="sxs-lookup"><span data-stu-id="22299-129">**Note:** A missing cost record can indicate a new manufactured item.</span></span> <span data-ttu-id="22299-130">物料清单计算可以限制为具有缺少成本的物料。</span><span class="sxs-lookup"><span data-stu-id="22299-130">BOM calculations can be limited to items that have missing costs.</span></span>
4.  <span data-ttu-id="22299-131">验证新制造物料的计算成本的完整性和精确性。</span><span class="sxs-lookup"><span data-stu-id="22299-131">Verify the completeness and accuracy of the calculated costs for new manufactured items.</span></span> <span data-ttu-id="22299-132">使用 **完成** 页来查看每个物料成本记录的已计算的成本，还可以审核所有信息日志警告消息。</span><span class="sxs-lookup"><span data-stu-id="22299-132">Use the **Complete** page to review the calculated costs for each item cost record, and also review any Infolog warning messages.</span></span> <span data-ttu-id="22299-133">或者，使用 **计算** 页可以查看计算成本的列表。</span><span class="sxs-lookup"><span data-stu-id="22299-133">Alternatively, use the **Calculation** page to review the calculated costs.</span></span>
5.  <span data-ttu-id="22299-134">使用 **成本计算版本设置** 页更改锁定标志，以便允许启用在第二个成本计算版本中的未决成本记录。</span><span class="sxs-lookup"><span data-stu-id="22299-134">Use the **Costing version setup** page to change the blocking flag to allow activation of the pending cost records in the second costing version.</span></span>
6.  <span data-ttu-id="22299-135">使用 **启用价格** 页（您从 **成本计算版本维护** 页打开的页面）启用第二个成本计算版本中的所有未决物料成本记录。</span><span class="sxs-lookup"><span data-stu-id="22299-135">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to enable all pending cost records in the second costing version.</span></span> <span data-ttu-id="22299-136">您还可以通过单击 **物料价格** 页上的 **启用** 按钮，启用单独物料的未决成本记录。</span><span class="sxs-lookup"><span data-stu-id="22299-136">You can also enable the pending cost records for individual items by clicking the **Activate** button on the **Item price** page.</span></span>
7.  <span data-ttu-id="22299-137">使用 **成本计算版本设置** 页更改在第二个成本计算版本内的锁定标志来阻止进一步的数据维护。</span><span class="sxs-lookup"><span data-stu-id="22299-137">Use the **Costing version setup** page to change the blocking flags in the second costing version to prevent additional data maintenance.</span></span> <span data-ttu-id="22299-138">这些锁定策略将阻止输入新的未决成本和启用未决成本。</span><span class="sxs-lookup"><span data-stu-id="22299-138">The blocking policies prevent the entry of new pending costs and the activation of pending costs.</span></span>




