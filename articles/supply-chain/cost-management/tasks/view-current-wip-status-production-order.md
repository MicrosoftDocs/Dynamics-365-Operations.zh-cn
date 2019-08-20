---
title: 查看生产订单当前的 WIP 状态
description: 该过程显示如何查看生产订单的“WIP 报表”。
author: AndersGirke
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, CostAdminWorkspace, CostLastInventoryCloseCard, CostLastBackflushCostingCard, CostStatementCacheCard, CostReleasedProductsMissingCostingDataFormPart, CostCalculationPeriodTopVariancesChartFormPart, ProdTable, CostStatement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 026a847ce63c96865dcb8c094fec205396f810ba
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836424"
---
# <a name="view-current-wip-status-on-a-production-order"></a><span data-ttu-id="399b3-103">查看生产订单当前的 WIP 状态</span><span class="sxs-lookup"><span data-stu-id="399b3-103">View current WIP status on a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="399b3-104">该过程显示如何查看生产订单的“WIP 报表”。</span><span class="sxs-lookup"><span data-stu-id="399b3-104">This procedure shows how to view WIP statement on a production order.</span></span> <span data-ttu-id="399b3-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="399b3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="399b3-106">此程序是专为成本控制设计的。</span><span class="sxs-lookup"><span data-stu-id="399b3-106">This procedure is intended for the cost controller.</span></span>

1. <span data-ttu-id="399b3-107">单击“成本管理”。</span><span class="sxs-lookup"><span data-stu-id="399b3-107">Click Cost administration.</span></span>
2. <span data-ttu-id="399b3-108">单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="399b3-108">Click Production orders.</span></span>
3. <span data-ttu-id="399b3-109">使用“快速筛选”筛选带有“p000153”值的“生产”字段。</span><span class="sxs-lookup"><span data-stu-id="399b3-109">Use the Quick Filter to filter on the Production field with a value of 'p000153'.</span></span>
4. <span data-ttu-id="399b3-110">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="399b3-110">On the Action Pane, click Manage costs.</span></span>
5. <span data-ttu-id="399b3-111">单击“生产 WIP 报表”。</span><span class="sxs-lookup"><span data-stu-id="399b3-111">Click Production WIP statement.</span></span>
6. <span data-ttu-id="399b3-112">在“开始日期”字段中，设置日期为“2012-12-01”。</span><span class="sxs-lookup"><span data-stu-id="399b3-112">In the From date field, set the date to '2012-12-01'.</span></span>
7. <span data-ttu-id="399b3-113">在“结束日期”字段中，设置日期为“2012-12-31”。</span><span class="sxs-lookup"><span data-stu-id="399b3-113">In the To date field, set the date to '2012-12-31'.</span></span>

