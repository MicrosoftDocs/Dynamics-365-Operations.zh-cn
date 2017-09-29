--- 
title: "创建询价的计分方法"
description: "此过程演示如何创建计分方法。"
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d72678db60254801c6c899f4d405f1c59de8d65
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="0a872-103">创建询价的计分方法</span><span class="sxs-lookup"><span data-stu-id="0a872-103">Create a scoring method for RFQs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a872-104">此过程演示如何创建计分方法。</span><span class="sxs-lookup"><span data-stu-id="0a872-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="0a872-105">计分方法是可用于比较在询价 (RFQ) 回复中发送的出价的一组条件。</span><span class="sxs-lookup"><span data-stu-id="0a872-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="0a872-106">例如，您可能要根据供应商以往绩效进行评级，或者评判某一公司是否为环境友好型或良好的合作者，或基于价格比较出价。</span><span class="sxs-lookup"><span data-stu-id="0a872-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="0a872-107">计分方法可以与申请类型关联，充当该类型的询价的默认计分方法。</span><span class="sxs-lookup"><span data-stu-id="0a872-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="0a872-108">这些任务通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="0a872-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="0a872-109">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="0a872-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="0a872-110">转到“采购”>“设置”>“询价”>“计分方法”。</span><span class="sxs-lookup"><span data-stu-id="0a872-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="0a872-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0a872-111">Click New.</span></span>
3. <span data-ttu-id="0a872-112">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0a872-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0a872-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0a872-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0a872-114">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="0a872-114">Click Save.</span></span>
6. <span data-ttu-id="0a872-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0a872-115">Click New.</span></span>
7. <span data-ttu-id="0a872-116">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0a872-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="0a872-117">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0a872-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0a872-118">为询价选择了计分方法时，此描述随计分方法名称一起显示。</span><span class="sxs-lookup"><span data-stu-id="0a872-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="0a872-119">在“范围起始值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="0a872-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="0a872-120">此范围限制采购专业人员可输入为分数的内容。</span><span class="sxs-lookup"><span data-stu-id="0a872-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="0a872-121">一个询价有多个计分条件时，将把已输入的分数添加到彼此，并提供总分来比较出价。</span><span class="sxs-lookup"><span data-stu-id="0a872-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="0a872-122">在“范围结束值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="0a872-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="0a872-123">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0a872-123">Click New.</span></span>
12. <span data-ttu-id="0a872-124">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0a872-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="0a872-125">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0a872-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="0a872-126">在“范围起始值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="0a872-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="0a872-127">在“范围结束值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="0a872-127">In the Range to field, enter a number.</span></span>


