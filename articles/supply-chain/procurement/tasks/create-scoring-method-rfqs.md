---
title: 创建询价的计分方法
description: 此过程演示如何创建计分方法。
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b098975f5557e9b99e7a951c0f8035bbaea5210
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812078"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="f8277-103">创建询价的计分方法</span><span class="sxs-lookup"><span data-stu-id="f8277-103">Create a scoring method for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8277-104">此过程演示如何创建计分方法。</span><span class="sxs-lookup"><span data-stu-id="f8277-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="f8277-105">计分方法是可用于比较在询价 (RFQ) 回复中发送的出价的一组条件。</span><span class="sxs-lookup"><span data-stu-id="f8277-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="f8277-106">例如，您可能要根据供应商以往绩效进行评级，或者评判某一公司是否为环境友好型或良好的合作者，或基于价格比较出价。</span><span class="sxs-lookup"><span data-stu-id="f8277-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="f8277-107">计分方法可以与申请类型关联，充当该类型的询价的默认计分方法。</span><span class="sxs-lookup"><span data-stu-id="f8277-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="f8277-108">这些任务通常由采购经理完成。</span><span class="sxs-lookup"><span data-stu-id="f8277-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="f8277-109">您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="f8277-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="f8277-110">转到“采购”>“设置”>“询价”>“计分方法”。</span><span class="sxs-lookup"><span data-stu-id="f8277-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="f8277-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f8277-111">Click New.</span></span>
3. <span data-ttu-id="f8277-112">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f8277-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f8277-113">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f8277-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f8277-114">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f8277-114">Click Save.</span></span>
6. <span data-ttu-id="f8277-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f8277-115">Click New.</span></span>
7. <span data-ttu-id="f8277-116">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f8277-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="f8277-117">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f8277-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f8277-118">为询价选择了计分方法时，此描述随计分方法名称一起显示。</span><span class="sxs-lookup"><span data-stu-id="f8277-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="f8277-119">在“范围起始值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f8277-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="f8277-120">此范围限制采购专业人员可输入为分数的内容。</span><span class="sxs-lookup"><span data-stu-id="f8277-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="f8277-121">一个询价有多个计分条件时，将把已输入的分数添加到彼此，并提供总分来比较出价。</span><span class="sxs-lookup"><span data-stu-id="f8277-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="f8277-122">在“范围结束值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f8277-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="f8277-123">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f8277-123">Click New.</span></span>
12. <span data-ttu-id="f8277-124">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f8277-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="f8277-125">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f8277-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="f8277-126">在“范围起始值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f8277-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="f8277-127">在“范围结束值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f8277-127">In the Range to field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]