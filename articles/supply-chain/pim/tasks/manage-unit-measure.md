--- 
title: "管理度量单位"
description: "此过程显示如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。"
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3e208b7f1faab77f2b97ff7b440a228656684fca
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="3667d-103">管理度量单位</span><span class="sxs-lookup"><span data-stu-id="3667d-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3667d-104">此过程显示如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。</span><span class="sxs-lookup"><span data-stu-id="3667d-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="3667d-105">您可以使用演示数据或使用您自己的数据浏览此过程。</span><span class="sxs-lookup"><span data-stu-id="3667d-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="3667d-106">转到“已发布产品的维护”。</span><span class="sxs-lookup"><span data-stu-id="3667d-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="3667d-107">单击“单位”。</span><span class="sxs-lookup"><span data-stu-id="3667d-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="3667d-108">创建度量单位</span><span class="sxs-lookup"><span data-stu-id="3667d-108">Create a unit of measure</span></span>
1. <span data-ttu-id="3667d-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3667d-109">Click New.</span></span>
2. <span data-ttu-id="3667d-110">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3667d-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="3667d-111">输入引用度量单位时使用的 ID 或符号。</span><span class="sxs-lookup"><span data-stu-id="3667d-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="3667d-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3667d-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3667d-113">用系统语言输入度量单位的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="3667d-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="3667d-114">在“单位类别”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="3667d-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="3667d-115">单位类别定义逻辑分组，例如区域、质量或数量、度量单位所属的分组。</span><span class="sxs-lookup"><span data-stu-id="3667d-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="3667d-116">在“小数精度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="3667d-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="3667d-117">指定在计算度量单位时，度量单位转换必须舍入的小数位数。</span><span class="sxs-lookup"><span data-stu-id="3667d-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="3667d-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3667d-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="3667d-119">定义单位转换</span><span class="sxs-lookup"><span data-stu-id="3667d-119">Define unit translations</span></span>
1. <span data-ttu-id="3667d-120">单击“单位文本”。</span><span class="sxs-lookup"><span data-stu-id="3667d-120">Click Unit texts.</span></span>
2. <span data-ttu-id="3667d-121">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3667d-121">Click New.</span></span>
    * <span data-ttu-id="3667d-122">使用单位文本创建 ID 或符号转换，代表供在外部文档中以客户或供应商特定语言使用的度量单位。</span><span class="sxs-lookup"><span data-stu-id="3667d-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="3667d-123">在“语言”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3667d-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="3667d-124">在“文本”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3667d-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="3667d-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3667d-125">Click Save.</span></span>
6. <span data-ttu-id="3667d-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3667d-126">Close the page.</span></span>
7. <span data-ttu-id="3667d-127">单击“转换单位的描述”。</span><span class="sxs-lookup"><span data-stu-id="3667d-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="3667d-128">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="3667d-128">Click New.</span></span>
    * <span data-ttu-id="3667d-129">定义度量单位的特定语言描述。</span><span class="sxs-lookup"><span data-stu-id="3667d-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="3667d-130">在“语言”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3667d-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="3667d-131">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3667d-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="3667d-132">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="3667d-132">Click Save.</span></span>
12. <span data-ttu-id="3667d-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3667d-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="3667d-134">定义单位换算规则</span><span class="sxs-lookup"><span data-stu-id="3667d-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="3667d-135">单击“单位换算”。</span><span class="sxs-lookup"><span data-stu-id="3667d-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="3667d-136">定义所选单位类别中的其他度量单位间的度量单位转换规则。</span><span class="sxs-lookup"><span data-stu-id="3667d-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="3667d-137">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="3667d-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="3667d-138">在“系数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="3667d-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="3667d-139">源单位和目标单位之间的换算系数。</span><span class="sxs-lookup"><span data-stu-id="3667d-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="3667d-140">例如，由于 100 厘米等于一米，则厘米到米的转换系数为 100。</span><span class="sxs-lookup"><span data-stu-id="3667d-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="3667d-141">在“目标单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3667d-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="3667d-142">在“舍入”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="3667d-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="3667d-143">定义转换值应如何舍入。</span><span class="sxs-lookup"><span data-stu-id="3667d-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="3667d-144">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="3667d-144">Click OK.</span></span>
7. <span data-ttu-id="3667d-145">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3667d-145">Close the page.</span></span>


