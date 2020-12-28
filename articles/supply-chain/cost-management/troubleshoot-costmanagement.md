---
title: 成本管理疑难解答
description: 此主题介绍如何解决使用成本管理时可能遇到的问题。
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e84bb167395c06295b0e8ef8b9fd98aa4bc0cc14
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4423443"
---
# <a name="troubleshoot-cost-management"></a><span data-ttu-id="423ac-103">成本管理疑难解答</span><span class="sxs-lookup"><span data-stu-id="423ac-103">Troubleshoot cost management</span></span>

<span data-ttu-id="423ac-104">此主题介绍如何解决使用成本管理时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="423ac-104">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a><span data-ttu-id="423ac-105">库存值/帐龄报表与其存储版本之间的功能空白</span><span class="sxs-lookup"><span data-stu-id="423ac-105">Functional gaps between the inventory value/aging reports and their storage versions</span></span>

<span data-ttu-id="423ac-106">[库龄报表存储](inventory-aging-report-storage.md)和[库存值存储报表](inventory-value-report-storage.md)功能让 Supply Chain Management 可以显示大量库存交易。</span><span class="sxs-lookup"><span data-stu-id="423ac-106">The [Inventory aging report storage](inventory-aging-report-storage.md) and [Inventory value storage report](inventory-value-report-storage.md) features enable Supply Chain Management to display large volumes of inventory transactions.</span></span> <span data-ttu-id="423ac-107">在每种情况下，都会保存报表结果以供浏览和导出，这与这些报表的非存储版本不同。</span><span class="sxs-lookup"><span data-stu-id="423ac-107">In each case, the report results are saved for browsing and exporting, unlike with the non-storage versions of these reports.</span></span> <span data-ttu-id="423ac-108">但是，这些报表的非存储版本中存在的某些功能在存储版本中不存在。</span><span class="sxs-lookup"><span data-stu-id="423ac-108">However, some functionality that exists in the non-storage versions of these reports doesn't exist in the storage versions.</span></span> <span data-ttu-id="423ac-109">以下小节总结了存在的差异并提供了解决方法。</span><span class="sxs-lookup"><span data-stu-id="423ac-109">The following subsections summarize the differences and provide workarounds.</span></span>

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a><span data-ttu-id="423ac-110">存储报表不包括小计，即使在报表布局中启用了小计</span><span class="sxs-lookup"><span data-stu-id="423ac-110">Storage reports don't include subtotals, even if they are enabled in the report layout</span></span>

<span data-ttu-id="423ac-111">小计可能会在导出结果时导致问题，尤其是在用户更改记录序列时。</span><span class="sxs-lookup"><span data-stu-id="423ac-111">Subtotals can cause issues when the result is exported, especially if users change the record sequence.</span></span>

<span data-ttu-id="423ac-112">要检查小计，可以将结果导出到 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="423ac-112">To check the subtotals, you can export the result into Microsoft Excel.</span></span> <span data-ttu-id="423ac-113">或者，如果您要在 Supply Chain Management 中检查小计，请使用 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)启用 *新网格控件* 和 *(预览)在网格中分组* 功能，这提供了一种更加灵活的方式来按列查看任何一个组的小计。</span><span class="sxs-lookup"><span data-stu-id="423ac-113">Alternatively, if you want to check subtotals within Supply Chain Management, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to enable the *New grid control* and *(Preview) Grouping in grids* features, which provide a much more flexible way to see the subtotal for any group by column.</span></span> <span data-ttu-id="423ac-114">有关详细信息，请参阅[网格功能](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md)。</span><span class="sxs-lookup"><span data-stu-id="423ac-114">For more information, see [Grid capabilities](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).</span></span>

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a><span data-ttu-id="423ac-115">库存值存储报表不支持会计科目信息</span><span class="sxs-lookup"><span data-stu-id="423ac-115">Inventory value storage report doesn't support ledger account information</span></span>

<span data-ttu-id="423ac-116">您可以运行试算平衡表来获取库存科目余额并将其与 **库存值存储** 报表进行比较。</span><span class="sxs-lookup"><span data-stu-id="423ac-116">You can run the trial balance to get the inventory accounts balance and compare that to the **Inventory value storage** report.</span></span>

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a><span data-ttu-id="423ac-117">在不结转库存的情况下更改分类帐期间状态时会显示警告或错误</span><span class="sxs-lookup"><span data-stu-id="423ac-117">Warnings or errors are shown when changing a ledger period status without closing inventory</span></span>

<span data-ttu-id="423ac-118">Microsoft 引入了以下验证，以防止由于围绕成本计算的不正确期间结束流程而导致的问题。</span><span class="sxs-lookup"><span data-stu-id="423ac-118">Microsoft introduced the following validations to prevent issues caused by an incorrect period-end process around costing.</span></span> <span data-ttu-id="423ac-119">如果遇到以下任何错误消息，请参阅 [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) 了解如何解决这些问题的详细信息。</span><span class="sxs-lookup"><span data-stu-id="423ac-119">If you encounter any of the following error messages, refer to [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) for more information about how to resolve these issues.</span></span>

- <span data-ttu-id="423ac-120">您将要执行日期为 %1 (10-02-2019) 的重新计算。</span><span class="sxs-lookup"><span data-stu-id="423ac-120">You are about to execute a Recalculation with a date %1 (10-02-2019).</span></span> <span data-ttu-id="423ac-121">上次登记的重新计算已在日期为 %2 (20-01-2019) 的上一个期间内执行。</span><span class="sxs-lookup"><span data-stu-id="423ac-121">The last registered Recalculation was executed in a previous period with a date %2 (20-01-2019).</span></span> <span data-ttu-id="423ac-122">其日期 %3 (31-01-2019) 与期间结束匹配的库存结转未执行已登记。</span><span class="sxs-lookup"><span data-stu-id="423ac-122">No execution of an inventory close with a date %3 (31-01-2019) matching period end has been registered.</span></span> <span data-ttu-id="423ac-123">请记住在与期间结束匹配的 %3 (31-01-2019) 前执行库存结转。</span><span class="sxs-lookup"><span data-stu-id="423ac-123">Please remember to execute an inventory close as of %3 (31-01-2019) matching the period end.</span></span> <span data-ttu-id="423ac-124">执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。</span><span class="sxs-lookup"><span data-stu-id="423ac-124">The valuation of inventories, cost of goods sold and variances may not be correct in subledger or general ledger until this has been executed.</span></span>

- <span data-ttu-id="423ac-125">您即将将分类帐期间 %1 的状态更改为 %2。</span><span class="sxs-lookup"><span data-stu-id="423ac-125">You are about to change the status of ledger period %1 to %2.</span></span> <span data-ttu-id="423ac-126">其日期 %3 与期间结束匹配的库存结转未执行已登记。</span><span class="sxs-lookup"><span data-stu-id="423ac-126">No execution of inventory close with a date %3 matching period end has been registered.</span></span> <span data-ttu-id="423ac-127">请在更改状态之前在与期间结束匹配的 %3 前执行库存结转。</span><span class="sxs-lookup"><span data-stu-id="423ac-127">Please execute an inventory close as of %3 matching the period end before changing the status.</span></span> <span data-ttu-id="423ac-128">执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。</span><span class="sxs-lookup"><span data-stu-id="423ac-128">The valuation of inventories, cost of goods sold and variances may not be correct in subledger or general ledger until this has been executed.</span></span> <span data-ttu-id="423ac-129">从法人 %4 报告。</span><span class="sxs-lookup"><span data-stu-id="423ac-129">Reported from legal entity %4.</span></span> <span data-ttu-id="423ac-130">现在，它只是提供信息，但将来会要求您执行此类操作。</span><span class="sxs-lookup"><span data-stu-id="423ac-130">For now, it is informational, but you will be required to perform such action in future.</span></span>

- <span data-ttu-id="423ac-131">科目结构 %1 已更改。</span><span class="sxs-lookup"><span data-stu-id="423ac-131">The Account structure %1 has been changed.</span></span> <span data-ttu-id="423ac-132">一个或多个主科目 %2 不再存在。</span><span class="sxs-lookup"><span data-stu-id="423ac-132">One or more main accounts %2 no longer exist.</span></span> <span data-ttu-id="423ac-133">这些主科目是日期为 %4 的 %3 所需要的。</span><span class="sxs-lookup"><span data-stu-id="423ac-133">These Main accounts are required by the %3 with a date %4.</span></span> <span data-ttu-id="423ac-134">请先将这些主科目添加到科目结构 %1 中，然后才能继续 %3 作业。</span><span class="sxs-lookup"><span data-stu-id="423ac-134">Please add these Main accounts to the Account structure %1 before you can resume the %3 job.</span></span> <span data-ttu-id="423ac-135">现在，它只是提供信息，但将来会要求您执行此类操作。</span><span class="sxs-lookup"><span data-stu-id="423ac-135">For now, it is informational, but you will be required to perform such action in future.</span></span>

- <span data-ttu-id="423ac-136">您将要执行日期为 %1 (31-01-2019) 的库存结转。</span><span class="sxs-lookup"><span data-stu-id="423ac-136">You are about to execute an inventory close with a date %1 (31-01-2019).</span></span> <span data-ttu-id="423ac-137">其日期 %2 (31-01-2019) 与期间结束匹配的倒冲成本计算法计算未执行已登记。</span><span class="sxs-lookup"><span data-stu-id="423ac-137">No execution of backflush costing calculation with a date %2 (31-01-2019) matching period end has been registered.</span></span> <span data-ttu-id="423ac-138">请记住执行其日期 %3 (31-01-2019) 与期间结束匹配的倒冲成本计算法计算。</span><span class="sxs-lookup"><span data-stu-id="423ac-138">Please remember to execute a backflush costing calculation with a date of %3 (31-01-2019) matching period end.</span></span> <span data-ttu-id="423ac-139">执行之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。</span><span class="sxs-lookup"><span data-stu-id="423ac-139">The valuation of inventories, cost of goods sold and variances may not be correct in subledger or general ledger until this has been executed.</span></span>

- <span data-ttu-id="423ac-140">您将要执行日期为 %1 (28-02-2019) 的倒冲成本计算法计算。</span><span class="sxs-lookup"><span data-stu-id="423ac-140">You are about to execute a backflush costing calculation with a date %1 (28-02-2019).</span></span> <span data-ttu-id="423ac-141">上次登记的倒冲成本计算法计算已在日期为 %2 (31-01-2019) 的上一个期间内执行。</span><span class="sxs-lookup"><span data-stu-id="423ac-141">The last registered backflush costing calculation was executed in a previous period with a date %2 (31-01-2019).</span></span> <span data-ttu-id="423ac-142">其日期 %3 (31-01-2019) 与期间结束匹配的库存结转未执行已登记。</span><span class="sxs-lookup"><span data-stu-id="423ac-142">No execution of an inventory close with a date %3 (31-01-2019) matching a period end has been registered.</span></span>
<span data-ttu-id="423ac-143">请记住在与期间结束匹配的 %3 (31-01-2019) 前执行库存结转。</span><span class="sxs-lookup"><span data-stu-id="423ac-143">Please remember to execute an inventory close as of %3 (31-01-2019) matching a period end.</span></span> <span data-ttu-id="423ac-144">执行库存结转之前，子分类帐或总帐中的库存、所售货物成本和差异评估可能不正确。</span><span class="sxs-lookup"><span data-stu-id="423ac-144">The valuation of inventories, cost of goods sold and variances may not be correct in subledger or general ledger until the inventory close has been executed.</span></span>

## <a name="inventory-aging-report-discrepancies"></a><span data-ttu-id="423ac-145">库龄报表差异</span><span class="sxs-lookup"><span data-stu-id="423ac-145">Inventory aging report discrepancies</span></span>

<span data-ttu-id="423ac-146">**库龄报表** 在不同的存储维度（如站点或仓库）查看时，显示不同的值。</span><span class="sxs-lookup"><span data-stu-id="423ac-146">The **Inventory aging report** shows different values when viewed at different storage dimensions (such as site or warehouse).</span></span> <span data-ttu-id="423ac-147">有关报告逻辑的详细信息，请参阅[库龄报表示例和逻辑](inventory-aging-report.md)。</span><span class="sxs-lookup"><span data-stu-id="423ac-147">For more information about the reporting logic, see [Inventory aging report examples and logic](inventory-aging-report.md).</span></span>
