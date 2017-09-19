--- 
title: "创建日记帐高级规则"
description: "该过程介绍创建日记帐高级规则的步骤。"
author: aprilolson
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
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1bb1663b0f5d7e6a550e1ffd2ee2edf3771a13b3
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="60d7f-103">创建日记帐高级规则</span><span class="sxs-lookup"><span data-stu-id="60d7f-103">Create advanced rules for journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60d7f-104">该过程介绍创建日记帐高级规则的步骤。</span><span class="sxs-lookup"><span data-stu-id="60d7f-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="60d7f-105">这包括设置日记帐控制和用户过帐限制。</span><span class="sxs-lookup"><span data-stu-id="60d7f-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="60d7f-106">此过程使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="60d7f-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="60d7f-107">设置日记帐控制</span><span class="sxs-lookup"><span data-stu-id="60d7f-107">Set up journal control</span></span>
1. <span data-ttu-id="60d7f-108">转到“总帐”>“日记帐设置”>“日记帐名称”。</span><span class="sxs-lookup"><span data-stu-id="60d7f-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="60d7f-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60d7f-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="60d7f-110">单击“日记帐控制”。</span><span class="sxs-lookup"><span data-stu-id="60d7f-110">Click Journal control.</span></span>
4. <span data-ttu-id="60d7f-111">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="60d7f-111">Click Add.</span></span>
5. <span data-ttu-id="60d7f-112">在“公司帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="60d7f-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="60d7f-113">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60d7f-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="60d7f-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="60d7f-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="60d7f-115">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="60d7f-115">Click Add.</span></span>
9. <span data-ttu-id="60d7f-116">在“科目结构”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="60d7f-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="60d7f-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60d7f-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="60d7f-118">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="60d7f-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="60d7f-119">在“分部”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="60d7f-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="60d7f-120">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="60d7f-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="60d7f-121">在“起始值”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="60d7f-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="60d7f-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60d7f-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="60d7f-123">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="60d7f-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="60d7f-124">在“目标值”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="60d7f-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="60d7f-125">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="60d7f-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="60d7f-126">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="60d7f-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="60d7f-127">设置过帐限制</span><span class="sxs-lookup"><span data-stu-id="60d7f-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="60d7f-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="60d7f-128">Close the page.</span></span>
2. <span data-ttu-id="60d7f-129">单击“过帐限制”。</span><span class="sxs-lookup"><span data-stu-id="60d7f-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="60d7f-130">在“如何设置过帐限制”字段中，选择“按用户组”。</span><span class="sxs-lookup"><span data-stu-id="60d7f-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="60d7f-131">在树形图中，单击“您允许该日记帐过帐的组”。</span><span class="sxs-lookup"><span data-stu-id="60d7f-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="60d7f-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="60d7f-132">Click OK.</span></span>

