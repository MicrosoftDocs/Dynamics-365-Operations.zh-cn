---
title: 登记和删除工作人员的福利
description: 该过程演示了如何在一项或多项福利中登记单个工作人员，以及如何在一项福利中等级多个工作人员。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92da6d24f3fc4282de5673a8155b6ab6316e55aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190411"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="a05e4-103">登记和删除工作人员的福利</span><span class="sxs-lookup"><span data-stu-id="a05e4-103">Enroll and remove benefits from workers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a05e4-104">该过程演示了如何在一项或多项福利中登记单个工作人员，以及如何在一项福利中等级多个工作人员。</span><span class="sxs-lookup"><span data-stu-id="a05e4-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="a05e4-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="a05e4-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="a05e4-106">登记单个工作人员的福利</span><span class="sxs-lookup"><span data-stu-id="a05e4-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="a05e4-107">转到“人力资源”>“工作人员”>“员工”</span><span class="sxs-lookup"><span data-stu-id="a05e4-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="a05e4-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a05e4-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a05e4-109">单击“福利”。</span><span class="sxs-lookup"><span data-stu-id="a05e4-109">Click Benefits.</span></span>
4. <span data-ttu-id="a05e4-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a05e4-110">Click New.</span></span>
5. <span data-ttu-id="a05e4-111">在“福利”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a05e4-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="a05e4-112">在“覆盖范围开始日期”字段中，输入一个日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a05e4-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="a05e4-113">在“覆盖范围结束日期”字段中，输入一个日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a05e4-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="a05e4-114">如果需要将受益人添加到福利，则展开“受益人”部分。</span><span class="sxs-lookup"><span data-stu-id="a05e4-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="a05e4-115">还可以从此页添加依赖项（如果适用于该福利）。</span><span class="sxs-lookup"><span data-stu-id="a05e4-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="a05e4-116">还可以在此页编辑福利登记的详细信息，或者取消登记。</span><span class="sxs-lookup"><span data-stu-id="a05e4-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="a05e4-117">完成福利登记信息更改后关闭此页。</span><span class="sxs-lookup"><span data-stu-id="a05e4-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="a05e4-118">登记多个工作人员的福利</span><span class="sxs-lookup"><span data-stu-id="a05e4-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="a05e4-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a05e4-119">Close the page.</span></span>
2. <span data-ttu-id="a05e4-120">转到“人力资源”>“工作人员”>“员工”</span><span class="sxs-lookup"><span data-stu-id="a05e4-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="a05e4-121">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a05e4-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a05e4-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a05e4-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a05e4-123">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a05e4-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="a05e4-124">单击“登记福利”。</span><span class="sxs-lookup"><span data-stu-id="a05e4-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="a05e4-125">在“福利”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a05e4-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="a05e4-126">在“覆盖范围开始日期”字段中，输入一个日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a05e4-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="a05e4-127">在“覆盖范围结束日期”字段中，输入一个日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a05e4-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="a05e4-128">单击“登记”。</span><span class="sxs-lookup"><span data-stu-id="a05e4-128">Click Enroll.</span></span>
11. <span data-ttu-id="a05e4-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a05e4-129">Close the page.</span></span>
12. <span data-ttu-id="a05e4-130">转到“人力资源”>“福利”>“登记”>“福利登记结果”。</span><span class="sxs-lookup"><span data-stu-id="a05e4-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="a05e4-131">查找您所需的福利结果记录。</span><span class="sxs-lookup"><span data-stu-id="a05e4-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="a05e4-132">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a05e4-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="a05e4-133">您可以在此页查看哪些员工已登记此福利，哪些员工未登记。</span><span class="sxs-lookup"><span data-stu-id="a05e4-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

