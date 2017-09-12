--- 
title: "审核产品配置模型"
description: "该过程的运行要求至少有一个产品配置模型可用。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fa4548d3017246cbe49e2613f8990df6ea1c368b
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="2558d-103">审核产品配置模型</span><span class="sxs-lookup"><span data-stu-id="2558d-103">Approve a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2558d-104">该过程的运行要求至少有一个产品配置模型可用。</span><span class="sxs-lookup"><span data-stu-id="2558d-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="2558d-105">该过程使用演示数据公司 USMF 的高端扬声器模型。</span><span class="sxs-lookup"><span data-stu-id="2558d-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="2558d-106">请注意，此模型已通过审核，但该过程将向您介绍完整流程。</span><span class="sxs-lookup"><span data-stu-id="2558d-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="2558d-107">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="2558d-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="2558d-108">单击“产品配置模型”。</span><span class="sxs-lookup"><span data-stu-id="2558d-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="2558d-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2558d-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2558d-110">选择该过程的“高端扬声器模型”。</span><span class="sxs-lookup"><span data-stu-id="2558d-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="2558d-111">单击“版本”。</span><span class="sxs-lookup"><span data-stu-id="2558d-111">Click Versions.</span></span>
5. <span data-ttu-id="2558d-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2558d-112">Click New.</span></span>
6. <span data-ttu-id="2558d-113">在“产品编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2558d-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="2558d-114">该参考产品代表一个产品配置模型版本。</span><span class="sxs-lookup"><span data-stu-id="2558d-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="2558d-115">仅拥有基于约束的配置技术的基础产品会出现在此列表中。</span><span class="sxs-lookup"><span data-stu-id="2558d-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="2558d-116">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="2558d-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="2558d-117">选择产品模型版本何时可用。</span><span class="sxs-lookup"><span data-stu-id="2558d-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="2558d-118">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="2558d-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="2558d-119">选择此产品模型版本将过期的结束日期，或选择“从不”。</span><span class="sxs-lookup"><span data-stu-id="2558d-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="2558d-120">单击“审核”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="2558d-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="2558d-121">在“已审核”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="2558d-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="2558d-122">选择负责审批产品模型用于工序的人员。</span><span class="sxs-lookup"><span data-stu-id="2558d-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="2558d-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2558d-123">Click OK.</span></span>
12. <span data-ttu-id="2558d-124">在“定价方法”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="2558d-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="2558d-125">启用产品模型版本。</span><span class="sxs-lookup"><span data-stu-id="2558d-125">Activate the product model version.</span></span> <span data-ttu-id="2558d-126">一次只可能启用一个产品的一个产品模型。</span><span class="sxs-lookup"><span data-stu-id="2558d-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="2558d-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2558d-127">Close the page.</span></span>


