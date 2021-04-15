---
title: 为公共部门生成基本预算
description: 您可以为特定的预算模型和维度值创建初步预算登记条目。
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c7937402f63db23c2b42d61c584c17dce5e1bf10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811207"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="2a6f5-103">为公共部门生成基本预算</span><span class="sxs-lookup"><span data-stu-id="2a6f5-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a6f5-104">您可以为特定的预算模型和维度值创建初步预算登记条目。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="2a6f5-105">在实际预算经过审核后，您可以创建原始预算登记簿条目。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="2a6f5-106">通过使用 PSUS 演示公司数据的公共扇区分区创建该过程。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="2a6f5-107">转到“预算”>“预算登记条目”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="2a6f5-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-108">Click New.</span></span>
3. <span data-ttu-id="2a6f5-109">在“预算模型”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2a6f5-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2a6f5-111">在“预算代码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2a6f5-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2a6f5-113">在“原因代码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2a6f5-114">在列表中，单击“所需记录”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="2a6f5-115">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-115">Click Save.</span></span>
10. <span data-ttu-id="2a6f5-116">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-116">Click Add line.</span></span>
    * <span data-ttu-id="2a6f5-117">可选：如果您想更改标题中的日期，则请输入新日期。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="2a6f5-118">该日期决定了记录预算的会计周期。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="2a6f5-119">当查看任务指南以填写其他字段时，请单击此页上方的“解锁”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="2a6f5-120">在“科目结构”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="2a6f5-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="2a6f5-122">在“维度值”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="2a6f5-123">在“金额”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="2a6f5-124">您还可以输入金额类型。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="2a6f5-125">在“货币”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="2a6f5-126">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="2a6f5-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-127">Click Save.</span></span>
18. <span data-ttu-id="2a6f5-128">单击“更新预算余额”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="2a6f5-129">单击“更新”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-129">Click Update.</span></span>
    * <span data-ttu-id="2a6f5-130">要查看更新的结果，请单击蓝色栏上的“详细消息”。</span><span class="sxs-lookup"><span data-stu-id="2a6f5-130">To see the results of the update, click Message details on the blue bar.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]