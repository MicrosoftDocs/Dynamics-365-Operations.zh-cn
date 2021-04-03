---
title: 添加到绩效日记帐并向某人发送表扬
description: 绩效日记帐中包含与如何满足目标或您在某个期间的表现有关的信息。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a865ee37ed650c564961f6b3dd8773eea4f7b9ea
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465622"
---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="bf04c-103">添加到绩效日记帐并向某人发送表扬</span><span class="sxs-lookup"><span data-stu-id="bf04c-103">Add to your performance journal and send praise to someone</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bf04c-104">绩效日记帐中包含与如何满足目标或您在某个期间的表现有关的信息。</span><span class="sxs-lookup"><span data-stu-id="bf04c-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="bf04c-105">您还可以从日记帐表扬同事的操作。</span><span class="sxs-lookup"><span data-stu-id="bf04c-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="bf04c-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="bf04c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bf04c-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="bf04c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="bf04c-108">转到“所有工作区”>“员工自助服务”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="bf04c-109">单击“绩效日记帐”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-109">Click Performance journal.</span></span>
3. <span data-ttu-id="bf04c-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-110">Click New.</span></span>
4. <span data-ttu-id="bf04c-111">在“标题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="bf04c-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="bf04c-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="bf04c-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="bf04c-113">绩效日记帐日期是日记帐的创建日期。</span><span class="sxs-lookup"><span data-stu-id="bf04c-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="bf04c-114">源表示绩效日记帐的来源。</span><span class="sxs-lookup"><span data-stu-id="bf04c-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="bf04c-115">如果您创建一个，则创建的这个来自“我的日记帐”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="bf04c-116">如果您的经理创建一个，则创建的这个来自“经理日记帐”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="bf04c-117">您可以与您的经理共享此日记帐，或将其设置为只有您才可以看到。</span><span class="sxs-lookup"><span data-stu-id="bf04c-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="bf04c-118">在“开始日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="bf04c-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="bf04c-119">在“完成日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="bf04c-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="bf04c-120">在“开发计划”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="bf04c-121">在“关键字”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="bf04c-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="bf04c-122">单击“添加外部链接”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-122">Click Add external link.</span></span>
11. <span data-ttu-id="bf04c-123">在“描述”字段中，键入“构想”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="bf04c-124">在”Internet 地址“字段中，键入“https://www.microsoft.com/en/envision/default”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="bf04c-125">单击“保存”按钮下的标题“绩效日记帐”返回网格。</span><span class="sxs-lookup"><span data-stu-id="bf04c-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="bf04c-126">您可以将所选日记帐添加到目标，以便其在您打开该目标时显示。</span><span class="sxs-lookup"><span data-stu-id="bf04c-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="bf04c-127">将在“链接”快速选项卡中添加一个链接。如果您向目标添加一个日记帐，然后将该目标添加到审核，将自动在该审核中显示这个日记帐。</span><span class="sxs-lookup"><span data-stu-id="bf04c-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="bf04c-128">您可以将所选日记帐添加到审核，以便其在您打开该审核时显示。</span><span class="sxs-lookup"><span data-stu-id="bf04c-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="bf04c-129">将在“链接”快速选项卡中添加一个链接。</span><span class="sxs-lookup"><span data-stu-id="bf04c-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="bf04c-130">单击“快速添加”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-130">Click Quick add.</span></span>
15. <span data-ttu-id="bf04c-131">在“标题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="bf04c-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="bf04c-132">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="bf04c-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="bf04c-133">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-133">Click Save.</span></span>
18. <span data-ttu-id="bf04c-134">单击“发送表扬”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-134">Click Send praise.</span></span>
19. <span data-ttu-id="bf04c-135">从公司员工列表选择一个人。</span><span class="sxs-lookup"><span data-stu-id="bf04c-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="bf04c-136">在"描述"字段中，输入“感谢所有人在会议中的帮助！”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="bf04c-137">单击“发送”。</span><span class="sxs-lookup"><span data-stu-id="bf04c-137">Click Send.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]