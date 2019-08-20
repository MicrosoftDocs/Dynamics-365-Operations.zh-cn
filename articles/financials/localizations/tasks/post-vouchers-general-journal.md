---
title: 过帐普通日记帐的凭证
description: 此过程逐步演示如何使用普通日记帐过帐中国式凭证。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransDimension, DimensionLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e04a9b122fc6843feef855424d9af4c793fd4b49
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852615"
---
# <a name="post-vouchers-from-the-general-journal"></a><span data-ttu-id="698a8-103">过帐普通日记帐的凭证</span><span class="sxs-lookup"><span data-stu-id="698a8-103">Post vouchers from the general journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="698a8-104">此过程逐步演示如何使用普通日记帐过帐中国式凭证。</span><span class="sxs-lookup"><span data-stu-id="698a8-104">This procedure walks you through posting Chinese vouchers using the general journal.</span></span>  <span data-ttu-id="698a8-105">必须确保已创建所有必需的会计日历，才能完成此过程。</span><span class="sxs-lookup"><span data-stu-id="698a8-105">Before you can complete this procedure, be sure that you’ve created all of the necessary fiscal calendars.</span></span> 

<span data-ttu-id="698a8-106">本流程是用演示公司 CNMF 数据生成的。</span><span class="sxs-lookup"><span data-stu-id="698a8-106">This procedure was created using the demo data company CNMF.</span></span> <span data-ttu-id="698a8-107">对于 CNMF 演示数据，必须在会计年度“Fiscal_CN”中创建当年整年的会计年度。</span><span class="sxs-lookup"><span data-stu-id="698a8-107">For the CNMF demo data, you must create fiscal years through the current year in the fiscal calendar ‘Fiscal_CN’.</span></span> <span data-ttu-id="698a8-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="698a8-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="post-vouchers-from-general-ledger-journals"></a><span data-ttu-id="698a8-109">从总帐日记帐过帐凭证</span><span class="sxs-lookup"><span data-stu-id="698a8-109">Post vouchers from general ledger journals</span></span>
1. <span data-ttu-id="698a8-110">转到“总帐”>“日记帐条目”>“普通日记帐”。</span><span class="sxs-lookup"><span data-stu-id="698a8-110">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="698a8-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="698a8-111">Click New.</span></span>
3. <span data-ttu-id="698a8-112">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="698a8-112">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="698a8-113">在“名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="698a8-113">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="698a8-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="698a8-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="698a8-115">在“凭证类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="698a8-115">In the Voucher type field, enter or select a value.</span></span>
7. <span data-ttu-id="698a8-116">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="698a8-116">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="698a8-117">在“描述”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="698a8-117">In the Description field, enter or select a value.</span></span>
9. <span data-ttu-id="698a8-118">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="698a8-118">In the Description field, type a value.</span></span>
10. <span data-ttu-id="698a8-119">在“借方”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="698a8-119">In the Debit field, enter a number.</span></span>
11. <span data-ttu-id="698a8-120">在“抵销帐户类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="698a8-120">In the Offset account type field, select an option.</span></span>
12. <span data-ttu-id="698a8-121">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="698a8-121">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="698a8-122">单击“财务维度”。</span><span class="sxs-lookup"><span data-stu-id="698a8-122">Click Financial dimensions.</span></span>
14. <span data-ttu-id="698a8-123">单击“对方科目”。</span><span class="sxs-lookup"><span data-stu-id="698a8-123">Click Offset account.</span></span>
15. <span data-ttu-id="698a8-124">在“Cashflow_CN”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="698a8-124">In the Cashflow_CN field, enter or select a value.</span></span>
16. <span data-ttu-id="698a8-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="698a8-125">Click OK.</span></span>
17. <span data-ttu-id="698a8-126">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="698a8-126">Click Validate.</span></span>
    * <span data-ttu-id="698a8-127">对于此示例，必须满足凭证类型“付款”的条件。</span><span class="sxs-lookup"><span data-stu-id="698a8-127">For this example, the criteria for the voucher of type Pay must be met.</span></span> <span data-ttu-id="698a8-128">这意味着一个借方和贷方帐户必须为属于现金帐户的银行帐户，否则不能通过验证。</span><span class="sxs-lookup"><span data-stu-id="698a8-128">This means that one of the debit and credit accounts must be a bank account that is a cash account, otherwise the validation will not pass.</span></span>  
18. <span data-ttu-id="698a8-129">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="698a8-129">Click Validate.</span></span>
19. <span data-ttu-id="698a8-130">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="698a8-130">Click Post.</span></span>
20. <span data-ttu-id="698a8-131">单击“打印”。</span><span class="sxs-lookup"><span data-stu-id="698a8-131">Click Print.</span></span>
21. <span data-ttu-id="698a8-132">单击“凭证”。</span><span class="sxs-lookup"><span data-stu-id="698a8-132">Click Voucher.</span></span>
22. <span data-ttu-id="698a8-133">在“打印布局代码”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="698a8-133">In the Print layout code field, enter or select a value.</span></span>
23. <span data-ttu-id="698a8-134">选中“打印科目维度”复选框。</span><span class="sxs-lookup"><span data-stu-id="698a8-134">Select the Print account dimension check box.</span></span>
24. <span data-ttu-id="698a8-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="698a8-135">Click OK.</span></span>

