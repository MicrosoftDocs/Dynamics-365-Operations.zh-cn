--- 
title: "创建产品的批属性"
description: "此过程显示如何创建批属性，分配默认值范围和在组中加入属性。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fcd0afb8005f1712b08f0854613573ef04c0cad6
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="022f8-103">创建产品的批属性</span><span class="sxs-lookup"><span data-stu-id="022f8-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="022f8-104">此过程显示如何创建批属性，分配默认值范围和在组中加入属性。</span><span class="sxs-lookup"><span data-stu-id="022f8-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="022f8-105">使用 USP2 公司演示数据创建此过程。</span><span class="sxs-lookup"><span data-stu-id="022f8-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="022f8-106">转到“库存管理”>“设置”>“批次”>“批属性”。</span><span class="sxs-lookup"><span data-stu-id="022f8-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="022f8-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="022f8-107">Click New.</span></span>
3. <span data-ttu-id="022f8-108">在“属性”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="022f8-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="022f8-109">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="022f8-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="022f8-110">在“属性类型”字段中，选择“分数”。</span><span class="sxs-lookup"><span data-stu-id="022f8-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="022f8-111">此过程使用“分数”类型以启用小数值。</span><span class="sxs-lookup"><span data-stu-id="022f8-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="022f8-112">您可以选择其他属性类型。</span><span class="sxs-lookup"><span data-stu-id="022f8-112">You can select other attribute types.</span></span> <span data-ttu-id="022f8-113">如果您选择列举类型，则您必须在列举表中输入数值才能在“目标”字段输入数值。</span><span class="sxs-lookup"><span data-stu-id="022f8-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="022f8-114">在“最小值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="022f8-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="022f8-115">在“最大值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="022f8-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="022f8-116">在“增量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="022f8-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="022f8-117">在“目标”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="022f8-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="022f8-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="022f8-118">Click Save.</span></span>
11. <span data-ttu-id="022f8-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="022f8-119">Close the page.</span></span>
12. <span data-ttu-id="022f8-120">转到“库存管理”>“设置”>“批次”>“批属性组”。</span><span class="sxs-lookup"><span data-stu-id="022f8-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="022f8-121">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="022f8-121">Click New.</span></span>
14. <span data-ttu-id="022f8-122">在“属性组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="022f8-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="022f8-123">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="022f8-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="022f8-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="022f8-124">Click Save.</span></span>
17. <span data-ttu-id="022f8-125">单击“组属性”。</span><span class="sxs-lookup"><span data-stu-id="022f8-125">Click Group attributes.</span></span>
18. <span data-ttu-id="022f8-126">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="022f8-126">Click New.</span></span>
19. <span data-ttu-id="022f8-127">在“属性”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="022f8-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="022f8-128">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="022f8-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="022f8-129">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="022f8-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="022f8-130">属性可包含在任何组中。</span><span class="sxs-lookup"><span data-stu-id="022f8-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="022f8-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="022f8-131">Click Save.</span></span>
23. <span data-ttu-id="022f8-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="022f8-132">Close the page.</span></span>


