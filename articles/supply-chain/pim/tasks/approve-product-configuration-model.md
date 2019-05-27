---
title: 审核产品配置模型
description: 该过程的运行要求至少有一个产品配置模型可用。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c196731046fa01059d61f2df08f47639ba839642
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568619"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="ebf65-103">审核产品配置模型</span><span class="sxs-lookup"><span data-stu-id="ebf65-103">Approve a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ebf65-104">该过程的运行要求至少有一个产品配置模型可用。</span><span class="sxs-lookup"><span data-stu-id="ebf65-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="ebf65-105">该过程使用演示数据公司 USMF 的高端扬声器模型。</span><span class="sxs-lookup"><span data-stu-id="ebf65-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="ebf65-106">请注意，此模型已通过审核，但该过程将向您介绍完整流程。</span><span class="sxs-lookup"><span data-stu-id="ebf65-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="ebf65-107">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="ebf65-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ebf65-108">单击“产品配置模型”。</span><span class="sxs-lookup"><span data-stu-id="ebf65-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="ebf65-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ebf65-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ebf65-110">选择该过程的“高端扬声器模型”。</span><span class="sxs-lookup"><span data-stu-id="ebf65-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="ebf65-111">单击“版本”。</span><span class="sxs-lookup"><span data-stu-id="ebf65-111">Click Versions.</span></span>
5. <span data-ttu-id="ebf65-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ebf65-112">Click New.</span></span>
6. <span data-ttu-id="ebf65-113">在“产品编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf65-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="ebf65-114">该参考产品代表一个产品配置模型版本。</span><span class="sxs-lookup"><span data-stu-id="ebf65-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="ebf65-115">仅拥有基于约束的配置技术的基础产品会出现在此列表中。</span><span class="sxs-lookup"><span data-stu-id="ebf65-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="ebf65-116">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="ebf65-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="ebf65-117">选择产品模型版本何时可用。</span><span class="sxs-lookup"><span data-stu-id="ebf65-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="ebf65-118">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="ebf65-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="ebf65-119">选择此产品模型版本将过期的结束日期，或选择“从不”。</span><span class="sxs-lookup"><span data-stu-id="ebf65-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="ebf65-120">单击“审核”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="ebf65-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="ebf65-121">在“已审核”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf65-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="ebf65-122">选择负责审批产品模型用于工序的人员。</span><span class="sxs-lookup"><span data-stu-id="ebf65-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="ebf65-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ebf65-123">Click OK.</span></span>
12. <span data-ttu-id="ebf65-124">在“定价方法”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="ebf65-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="ebf65-125">启用产品模型版本。</span><span class="sxs-lookup"><span data-stu-id="ebf65-125">Activate the product model version.</span></span> <span data-ttu-id="ebf65-126">一次只可能启用一个产品的一个产品模型。</span><span class="sxs-lookup"><span data-stu-id="ebf65-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="ebf65-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ebf65-127">Close the page.</span></span>

