--- 
title: "在公共部门中创建原始预算和冲销初步预算条目"
description: "当您创建了原始预算条目并使用了包含初步预算金额的预算模型和维度值时，则可冲销初步预算金额。"
author: twheeloc
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2f50cc6bf8ec533db677d290c52dbd711d7a1de8
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-original-budget-and-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="a2ed0-103">在公共部门中创建原始预算和冲销初步预算条目</span><span class="sxs-lookup"><span data-stu-id="a2ed0-103">Create an original budget and reverse preliminary budget entries in the public sector</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2ed0-104">当您创建了原始预算条目并使用了包含初步预算金额的预算模型和维度值时，则可冲销初步预算金额。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="a2ed0-105">通过使用 PSUS 演示公司数据的公共扇区分区创建该过程。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="a2ed0-106">转到“预算”>“预算登记条目”。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="a2ed0-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-107">Click New.</span></span>
3. <span data-ttu-id="a2ed0-108">在“预算模型”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a2ed0-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a2ed0-110">在“预算代码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a2ed0-111">在列表中，单击“原始预算”。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="a2ed0-112">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-112">Click Save.</span></span>
8. <span data-ttu-id="a2ed0-113">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-113">Click Add line.</span></span>
9. <span data-ttu-id="a2ed0-114">可选：如果您想更改标题中的日期，则请输入新日期。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="a2ed0-115">该日期决定了记录预算的会计周期。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="a2ed0-116">在“科目结构”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a2ed0-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="a2ed0-118">在“维度值”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="a2ed0-119">在“金额”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="a2ed0-120">在“货币”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="a2ed0-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="a2ed0-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-122">Click Save.</span></span>
17. <span data-ttu-id="a2ed0-123">单击“更新预算余额”。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="a2ed0-124">可选：您可以选择“冲销初步预算”选择。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="a2ed0-125">请注意，您可以冲销所有初步预算条目，或者仅冲销您所指定预算代码的初步预算条目。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="a2ed0-126">要进行可选选择，请单击此页上方的“解锁”图标。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="a2ed0-127">单击“更新”。</span><span class="sxs-lookup"><span data-stu-id="a2ed0-127">Click Update.</span></span>


