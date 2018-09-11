--- 
title: "从现有配方版本中复制联产品"
description: "该过程展示如何为发布的产品从现有配方版本向不同的配方版本中复制联产品。"
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 91212851a011536f17acef57e842587be1934e3e
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="91350-103">从现有配方版本中复制联产品</span><span class="sxs-lookup"><span data-stu-id="91350-103">Copy co-products from an existing formula version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91350-104">该过程展示如何为发布的产品从现有配方版本向不同的配方版本中复制联产品。</span><span class="sxs-lookup"><span data-stu-id="91350-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="91350-105">它是与联产品关联至少一个配方版本的先决条件。</span><span class="sxs-lookup"><span data-stu-id="91350-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="91350-106">用于创建该过程的是演示数据公司 USP2。</span><span class="sxs-lookup"><span data-stu-id="91350-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="91350-107">查找一个已发布产品</span><span class="sxs-lookup"><span data-stu-id="91350-107">Find a released product</span></span>
1. <span data-ttu-id="91350-108">转至“产品发布”。</span><span class="sxs-lookup"><span data-stu-id="91350-108">Go to Released products.</span></span>
2. <span data-ttu-id="91350-109">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="91350-109">Click Show filters.</span></span>
    * <span data-ttu-id="91350-110">您即将在筛选器对话框中添加字段“生产类型”。</span><span class="sxs-lookup"><span data-stu-id="91350-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="91350-111">单击“添加筛选器”字段将添加字段“生产类型”。</span><span class="sxs-lookup"><span data-stu-id="91350-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="91350-112">在下一步中，您需要在选择“应用”前在“生产类型”字段中手动输入配方。</span><span class="sxs-lookup"><span data-stu-id="91350-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="91350-113">这设置已发布产品列表的筛选器。</span><span class="sxs-lookup"><span data-stu-id="91350-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="91350-114">在“生产类型”字段中手动输入配方。</span><span class="sxs-lookup"><span data-stu-id="91350-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="91350-115">单击“应用”。</span><span class="sxs-lookup"><span data-stu-id="91350-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="91350-116">选择一个已发布产品。</span><span class="sxs-lookup"><span data-stu-id="91350-116">Select a released product</span></span>
1. <span data-ttu-id="91350-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="91350-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="91350-118">单击“配方版本”。</span><span class="sxs-lookup"><span data-stu-id="91350-118">Click Formula versions.</span></span>
    * <span data-ttu-id="91350-119">在“工程操作窗格”上单击“配方版本”。</span><span class="sxs-lookup"><span data-stu-id="91350-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="91350-120">复制联产品: </span><span class="sxs-lookup"><span data-stu-id="91350-120">Copy co-products</span></span>
1. <span data-ttu-id="91350-121">在“操作窗格”上单击“配方版本”。</span><span class="sxs-lookup"><span data-stu-id="91350-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="91350-122">单击“联产品”。</span><span class="sxs-lookup"><span data-stu-id="91350-122">Click Co-products.</span></span>
3. <span data-ttu-id="91350-123">单击“复制”。</span><span class="sxs-lookup"><span data-stu-id="91350-123">Click Copy.</span></span>
4. <span data-ttu-id="91350-124">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91350-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="91350-125">在“配方版本”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="91350-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="91350-126">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="91350-126">Click OK.</span></span>
7. <span data-ttu-id="91350-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="91350-127">Close the page.</span></span>


