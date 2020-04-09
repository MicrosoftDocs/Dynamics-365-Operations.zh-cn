---
title: 在公共部门创建原始预算，然后预留初步预算条目
description: 当您创建了原始预算条目并使用了包含初步预算金额的预算模型和维度值时，则可冲销初步预算金额。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32d89216d49a743729de8910f738276cbddcd8bb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144539"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="2503d-103">在公共部门创建原始预算，然后预留初步预算条目</span><span class="sxs-lookup"><span data-stu-id="2503d-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2503d-104">当您创建了原始预算条目并使用了包含初步预算金额的预算模型和维度值时，则可冲销初步预算金额。</span><span class="sxs-lookup"><span data-stu-id="2503d-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="2503d-105">通过使用 PSUS 演示公司数据的公共扇区分区创建该过程。</span><span class="sxs-lookup"><span data-stu-id="2503d-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="2503d-106">转到“预算”>“预算登记条目”。</span><span class="sxs-lookup"><span data-stu-id="2503d-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="2503d-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2503d-107">Click New.</span></span>
3. <span data-ttu-id="2503d-108">在“预算模型”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2503d-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2503d-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2503d-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2503d-110">在“预算代码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2503d-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2503d-111">在列表中，单击“原始预算”。</span><span class="sxs-lookup"><span data-stu-id="2503d-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="2503d-112">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2503d-112">Click Save.</span></span>
8. <span data-ttu-id="2503d-113">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="2503d-113">Click Add line.</span></span>
9. <span data-ttu-id="2503d-114">可选：如果您想更改标题中的日期，则请输入新日期。</span><span class="sxs-lookup"><span data-stu-id="2503d-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="2503d-115">该日期决定了记录预算的会计周期。</span><span class="sxs-lookup"><span data-stu-id="2503d-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="2503d-116">在“科目结构”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2503d-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2503d-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2503d-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2503d-118">在“维度值”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="2503d-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="2503d-119">在“金额”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2503d-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="2503d-120">在“货币”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="2503d-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="2503d-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="2503d-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="2503d-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2503d-122">Click Save.</span></span>
17. <span data-ttu-id="2503d-123">单击“更新预算余额”。</span><span class="sxs-lookup"><span data-stu-id="2503d-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="2503d-124">可选：您可以选择“冲销初步预算”选择。</span><span class="sxs-lookup"><span data-stu-id="2503d-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="2503d-125">请注意，您可以冲销所有初步预算条目，或者仅冲销您所指定预算代码的初步预算条目。</span><span class="sxs-lookup"><span data-stu-id="2503d-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="2503d-126">要进行可选选择，请单击此页上方的“解锁”图标。</span><span class="sxs-lookup"><span data-stu-id="2503d-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="2503d-127">单击“更新”。</span><span class="sxs-lookup"><span data-stu-id="2503d-127">Click Update.</span></span>

