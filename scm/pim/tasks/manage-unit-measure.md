--- 
title: "管理度量单位"
description: "此过程显示如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。"
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6bb7a5133e9412f4ed6fb74f0d3ee595c07a0c4b
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="f3d61-103">管理度量单位</span><span class="sxs-lookup"><span data-stu-id="f3d61-103">Manage unit of measure</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3d61-104">此过程显示如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。</span><span class="sxs-lookup"><span data-stu-id="f3d61-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="f3d61-105">您可以使用演示数据或使用您自己的数据浏览此过程。</span><span class="sxs-lookup"><span data-stu-id="f3d61-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="f3d61-106">转到“已发布产品的维护”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="f3d61-107">单击“单位”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="f3d61-108">创建度量单位</span><span class="sxs-lookup"><span data-stu-id="f3d61-108">Create a unit of measure</span></span>
1. <span data-ttu-id="f3d61-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-109">Click New.</span></span>
2. <span data-ttu-id="f3d61-110">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f3d61-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="f3d61-111">输入引用度量单位时使用的 ID 或符号。</span><span class="sxs-lookup"><span data-stu-id="f3d61-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="f3d61-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f3d61-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f3d61-113">用系统语言输入度量单位的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="f3d61-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="f3d61-114">在“单位类别”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f3d61-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="f3d61-115">单位类别定义逻辑分组，例如区域、质量或数量、度量单位所属的分组。</span><span class="sxs-lookup"><span data-stu-id="f3d61-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="f3d61-116">在“小数精度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f3d61-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="f3d61-117">指定在计算度量单位时，度量单位转换必须舍入的小数位数。</span><span class="sxs-lookup"><span data-stu-id="f3d61-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="f3d61-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="f3d61-119">定义单位转换</span><span class="sxs-lookup"><span data-stu-id="f3d61-119">Define unit translations</span></span>
1. <span data-ttu-id="f3d61-120">单击“单位文本”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-120">Click Unit texts.</span></span>
2. <span data-ttu-id="f3d61-121">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-121">Click New.</span></span>
    * <span data-ttu-id="f3d61-122">使用单位文本创建 ID 或符号转换，代表供在外部文档中以客户或供应商特定语言使用的度量单位。</span><span class="sxs-lookup"><span data-stu-id="f3d61-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="f3d61-123">在“语言”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f3d61-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="f3d61-124">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f3d61-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="f3d61-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-125">Click Save.</span></span>
6. <span data-ttu-id="f3d61-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f3d61-126">Close the page.</span></span>
7. <span data-ttu-id="f3d61-127">单击“转换单位的描述”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="f3d61-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-128">Click New.</span></span>
    * <span data-ttu-id="f3d61-129">定义度量单位的特定语言描述。</span><span class="sxs-lookup"><span data-stu-id="f3d61-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="f3d61-130">在“语言”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f3d61-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="f3d61-131">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f3d61-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f3d61-132">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-132">Click Save.</span></span>
12. <span data-ttu-id="f3d61-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f3d61-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="f3d61-134">定义单位换算规则</span><span class="sxs-lookup"><span data-stu-id="f3d61-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="f3d61-135">单击“单位换算”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="f3d61-136">定义所选单位类别中的其他度量单位间的度量单位转换规则。</span><span class="sxs-lookup"><span data-stu-id="f3d61-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="f3d61-137">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="f3d61-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="f3d61-138">在“系数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="f3d61-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="f3d61-139">源单位和目标单位之间的换算系数。</span><span class="sxs-lookup"><span data-stu-id="f3d61-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="f3d61-140">例如，由于 100 厘米等于一米，则厘米到米的转换系数为 100。</span><span class="sxs-lookup"><span data-stu-id="f3d61-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="f3d61-141">在“目标单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f3d61-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="f3d61-142">在“舍入”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f3d61-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="f3d61-143">定义转换值应如何舍入。</span><span class="sxs-lookup"><span data-stu-id="f3d61-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="f3d61-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f3d61-144">Click OK.</span></span>
7. <span data-ttu-id="f3d61-145">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f3d61-145">Close the page.</span></span>


