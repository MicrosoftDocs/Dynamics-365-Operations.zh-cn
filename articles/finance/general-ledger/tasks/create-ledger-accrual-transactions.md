---
title: 创建分类帐应计交易记录
description: 此任务指南介绍生成基于应计架构的分类帐应计交易记录的步骤。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2112336045086d0eb3b2fb0018f33631528a05ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440658"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="4ae27-103">创建分类帐应计交易记录</span><span class="sxs-lookup"><span data-stu-id="4ae27-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ae27-104">此任务指南介绍生成基于应计架构的分类帐应计交易记录的步骤</span><span class="sxs-lookup"><span data-stu-id="4ae27-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="4ae27-105">转到“总帐”>“日记帐条目”>“普通日记帐”。</span><span class="sxs-lookup"><span data-stu-id="4ae27-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="4ae27-106">在列表中，查找并选择所需日记帐或创建新日记帐。</span><span class="sxs-lookup"><span data-stu-id="4ae27-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="4ae27-107">单击以访问“日记帐批号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="4ae27-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="4ae27-108">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4ae27-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="4ae27-109">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="4ae27-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="4ae27-110">在此示例中，我们将定义保险的费用。</span><span class="sxs-lookup"><span data-stu-id="4ae27-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="4ae27-111">这将会是定期费用金额。</span><span class="sxs-lookup"><span data-stu-id="4ae27-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="4ae27-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4ae27-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="4ae27-113">在“借方”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="4ae27-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="4ae27-114">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="4ae27-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="4ae27-115">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="4ae27-115">Click Functions.</span></span>
10. <span data-ttu-id="4ae27-116">单击“应计分类帐”。</span><span class="sxs-lookup"><span data-stu-id="4ae27-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="4ae27-117">在“应计标识”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="4ae27-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="4ae27-118">在列表中，查找并选择您想要应用的应计架构。</span><span class="sxs-lookup"><span data-stu-id="4ae27-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="4ae27-119">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4ae27-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="4ae27-120">在“开始日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="4ae27-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="4ae27-121">单击“交易记录”。</span><span class="sxs-lookup"><span data-stu-id="4ae27-121">Click Transactions.</span></span>
16. <span data-ttu-id="4ae27-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4ae27-122">Close the page.</span></span>
17. <span data-ttu-id="4ae27-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4ae27-123">Click OK.</span></span>
18. <span data-ttu-id="4ae27-124">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="4ae27-124">Click Post.</span></span>

