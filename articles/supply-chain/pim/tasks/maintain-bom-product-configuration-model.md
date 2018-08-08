--- 
title: "维护产品配置模型的物料清单"
description: "运行该过程要求有现有的产品配置模型。"
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 9c83b5a100ba039701137eb93ecf3ae5c5d36adc
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="ee8c1-103">维护产品配置模型的物料清单</span><span class="sxs-lookup"><span data-stu-id="ee8c1-103">Maintain BOM for a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee8c1-104">运行该过程要求有现有的产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="ee8c1-105">该过程使用演示公司 USMF 的“高端扬声器模型”创建。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="ee8c1-106">添加物料清单行</span><span class="sxs-lookup"><span data-stu-id="ee8c1-106">Add a BOM line</span></span>
1. <span data-ttu-id="ee8c1-107">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ee8c1-108">单击“产品配置模型”。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="ee8c1-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ee8c1-110">为该过程选择“高端扬声器”。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="ee8c1-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ee8c1-112">展开“物料清单行”部分。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="ee8c1-113">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-113">Click Add.</span></span>
7. <span data-ttu-id="ee8c1-114">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="ee8c1-115">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="ee8c1-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="ee8c1-117">添加物料清单行详细信息</span><span class="sxs-lookup"><span data-stu-id="ee8c1-117">Add BOM line details</span></span>
1. <span data-ttu-id="ee8c1-118">单击“物料清单行详细信息”。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-118">Click BOM line details.</span></span>
2. <span data-ttu-id="ee8c1-119">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="ee8c1-120">例如，可以选择物料 M0055。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="ee8c1-121">对于每个物料清单行属性，您可以选择是否带固定值或映射到属性中。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="ee8c1-122">选择“设置”复选框。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-122">Select the Set check box.</span></span>
4. <span data-ttu-id="ee8c1-123">在“计算”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="ee8c1-124">设置“计算”属性为“是”，确保物料清单行包括在成本计算中。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="ee8c1-125">单击“设置”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="ee8c1-126">选择“设置”复选框。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-126">Select the Set check box.</span></span>
7. <span data-ttu-id="ee8c1-127">在“数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="ee8c1-128">数量字段确定物料清单中包含的物料数。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="ee8c1-129">这可能为属性映射的明显候选项。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="ee8c1-130">单击“维度”选项卡。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="ee8c1-131">核实产品维度是否有效，因此必须有分配的值或属性。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="ee8c1-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="ee8c1-132">Click OK.</span></span>


