---
title: 比较生产订单上的有效、估计和实际成本
description: 此程序显示如何查看生产订单出现高产量差异的原因。
author: AndersGirke
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, CostAdminWorkspace, CostLastInventoryCloseCard, CostLastBackflushCostingCard, CostStatementCacheCard, CostReleasedProductsMissingCostingDataFormPart, CostCalculationPeriodTopVariancesChartFormPart, CostSelectPeriodDialogForm, CostCalculationPeriodTopVariancesListFormPart, ProdTable, CostCalculationCompareDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c2bc7c214ac8f9f6cbdc1ea3385b59f275dc6c9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845610"
---
# <a name="compare-active-estimated-and-realized-costs-on-a-production-order"></a><span data-ttu-id="c0285-103">比较生产订单上的有效、估计和实际成本</span><span class="sxs-lookup"><span data-stu-id="c0285-103">Compare active, estimated, and realized costs on a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0285-104">此程序显示如何查看生产订单出现高产量差异的原因。</span><span class="sxs-lookup"><span data-stu-id="c0285-104">This procedure shows how to view reasons for high production variance for a production order.</span></span> <span data-ttu-id="c0285-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="c0285-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c0285-106">此程序是专为成本控制设计的。</span><span class="sxs-lookup"><span data-stu-id="c0285-106">This procedure is intended for the cost controller.</span></span>

1. <span data-ttu-id="c0285-107">单击“成本管理”。</span><span class="sxs-lookup"><span data-stu-id="c0285-107">Click Cost administration.</span></span>
2. <span data-ttu-id="c0285-108">在“日期”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c0285-108">In the Date field, enter or select a value.</span></span>
    * <span data-ttu-id="c0285-109">此程序适用于 2012 财政年度。</span><span class="sxs-lookup"><span data-stu-id="c0285-109">This procedure uses the fiscal year 2012.</span></span> <span data-ttu-id="c0285-110">您可以把日期设置为 2012 年 1 月 1 日至 2012 年 12 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="c0285-110">You can set From date to January 1, 2012 and To date to December 31, 2012.</span></span>  
3. <span data-ttu-id="c0285-111">单击“高产量差异”选项卡。</span><span class="sxs-lookup"><span data-stu-id="c0285-111">Click the High production variances tab.</span></span>
4. <span data-ttu-id="c0285-112">单击以访问“生产”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="c0285-112">Click to follow the link in the Production field.</span></span>
    * <span data-ttu-id="c0285-113">单击“P000116”以访问“生产”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="c0285-113">Click P000116 to follow the link in the Production field.</span></span>  
5. <span data-ttu-id="c0285-114">在“操作窗格”中，单击“管理成本”。</span><span class="sxs-lookup"><span data-stu-id="c0285-114">On the Action Pane, click Manage costs.</span></span>
6. <span data-ttu-id="c0285-115">单击“查看成本比较”。</span><span class="sxs-lookup"><span data-stu-id="c0285-115">Click View cost comparison.</span></span>
7. <span data-ttu-id="c0285-116">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="c0285-116">Click Close.</span></span>

