---
title: 创建询价的申请类型和计分条件
description: 此指南演示如何创建申请类型和将其与计分方法关联。
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d28cb4bf20ba50aae6b85e835339e2df711c99d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812054"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="6c36a-103">创建询价的申请类型和计分条件</span><span class="sxs-lookup"><span data-stu-id="6c36a-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c36a-104">此指南演示如何创建申请类型和将其与计分方法关联。</span><span class="sxs-lookup"><span data-stu-id="6c36a-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="6c36a-105">还演示如何在随后将设置默认计分方法的询价 (RFQ) 中使用申请类型。</span><span class="sxs-lookup"><span data-stu-id="6c36a-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="6c36a-106">这些任务通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="6c36a-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="6c36a-107">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="6c36a-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6c36a-108">首先需要有计分方法。</span><span class="sxs-lookup"><span data-stu-id="6c36a-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="6c36a-109">创建请求类型</span><span class="sxs-lookup"><span data-stu-id="6c36a-109">Create a solicitation type</span></span>
1. <span data-ttu-id="6c36a-110">转到“采购”>“设置”>“询价”>“申请类型”。</span><span class="sxs-lookup"><span data-stu-id="6c36a-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="6c36a-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6c36a-111">Click New.</span></span>
3. <span data-ttu-id="6c36a-112">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6c36a-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6c36a-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6c36a-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6c36a-114">在“计分方法”字段中，选择要用于此申请类型的计分方法。</span><span class="sxs-lookup"><span data-stu-id="6c36a-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="6c36a-115">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6c36a-115">Click Save.</span></span>
7. <span data-ttu-id="6c36a-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c36a-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="6c36a-117">使用申请类型</span><span class="sxs-lookup"><span data-stu-id="6c36a-117">Use the solicitation type</span></span>
1. <span data-ttu-id="6c36a-118">转到“采购”>“询价”>“所有询价”。</span><span class="sxs-lookup"><span data-stu-id="6c36a-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="6c36a-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6c36a-119">Click New.</span></span>
3. <span data-ttu-id="6c36a-120">在“申请类型”字段中，选择刚才创建的申请类型。</span><span class="sxs-lookup"><span data-stu-id="6c36a-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="6c36a-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c36a-121">Click OK.</span></span>
5. <span data-ttu-id="6c36a-122">单击“计分条件”。</span><span class="sxs-lookup"><span data-stu-id="6c36a-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="6c36a-123">显示的计分条件来自您为申请类型关联的计分方法。</span><span class="sxs-lookup"><span data-stu-id="6c36a-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="6c36a-124">您可以选择在此页中添加或删除条件。</span><span class="sxs-lookup"><span data-stu-id="6c36a-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="6c36a-125">还可以通过从其他计分方法复制条件来添加新条件。</span><span class="sxs-lookup"><span data-stu-id="6c36a-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="6c36a-126">单击“复制条件”。</span><span class="sxs-lookup"><span data-stu-id="6c36a-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="6c36a-127">在“计分方法”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6c36a-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="6c36a-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6c36a-128">Click OK.</span></span>
9. <span data-ttu-id="6c36a-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6c36a-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]