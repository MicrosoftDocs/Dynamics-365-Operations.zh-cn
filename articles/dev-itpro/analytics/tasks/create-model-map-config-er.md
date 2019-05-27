---
title: 创建电子申报 (ER) 模型映射配置
description: 此过程用于设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 614ef06fcf5761f1cf2afb6e7655558d2858d763
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544948"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="45367-103">创建电子申报 (ER) 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="45367-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45367-104">此过程用于设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。</span><span class="sxs-lookup"><span data-stu-id="45367-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="45367-105">在此过程中，您将创建示例公司“Litware 公司”的配置。</span><span class="sxs-lookup"><span data-stu-id="45367-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="45367-106">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="45367-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="45367-107">可使用任何数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="45367-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="45367-108">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="45367-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="45367-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="45367-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="45367-110">确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。</span><span class="sxs-lookup"><span data-stu-id="45367-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="45367-111">如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="45367-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="45367-112">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="45367-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="45367-113">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="45367-113">Click Show filters.</span></span>
4. <span data-ttu-id="45367-114">在“名称”字段中输入筛选器值、“内部统计”并使用筛选器运算符“begins with”。</span><span class="sxs-lookup"><span data-stu-id="45367-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="45367-115">应用此筛选器来查找“内部统计”数据模型配置。</span><span class="sxs-lookup"><span data-stu-id="45367-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="45367-116">此模型可能已在配置树中存在。</span><span class="sxs-lookup"><span data-stu-id="45367-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="45367-117">如果存在，请跳过下一个子任务。</span><span class="sxs-lookup"><span data-stu-id="45367-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="45367-118">获取 Microsoft 提供的内部统计模型配置</span><span class="sxs-lookup"><span data-stu-id="45367-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="45367-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="45367-119">Close the page.</span></span>
2. <span data-ttu-id="45367-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="45367-120">Close the page.</span></span>
3. <span data-ttu-id="45367-121">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="45367-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="45367-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="45367-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="45367-123">选择 Microsoft 提供程序磁贴。</span><span class="sxs-lookup"><span data-stu-id="45367-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="45367-124">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="45367-124">Click Repositories.</span></span>
    * <span data-ttu-id="45367-125">单击 Microsoft 提供程序磁贴上的“存储库”。</span><span class="sxs-lookup"><span data-stu-id="45367-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="45367-126">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="45367-126">Click Show filters.</span></span>
7. <span data-ttu-id="45367-127">在“类型名称”字段中输入筛选器值、“资源”并使用筛选器运算符“contains”。</span><span class="sxs-lookup"><span data-stu-id="45367-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="45367-128">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="45367-128">Click Open.</span></span>
9. <span data-ttu-id="45367-129">在树中，选择“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="45367-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="45367-130">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="45367-130">Click Import.</span></span>
11. <span data-ttu-id="45367-131">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="45367-131">Click Yes.</span></span>
    * <span data-ttu-id="45367-132">您导入了包含您将用于探索新 ER 功能如何使用的数据模型的 ER 模型配置。</span><span class="sxs-lookup"><span data-stu-id="45367-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="45367-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="45367-133">Close the page.</span></span>
13. <span data-ttu-id="45367-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="45367-134">Close the page.</span></span>
14. <span data-ttu-id="45367-135">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="45367-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="45367-136">添加新模型映射配置</span><span class="sxs-lookup"><span data-stu-id="45367-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="45367-137">在树中，选择“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="45367-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="45367-138">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="45367-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="45367-139">在“新建”字段中，输入“基于数据模型内部统计的模型映射”。</span><span class="sxs-lookup"><span data-stu-id="45367-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="45367-140">在“名称”字段中，键入“内部统计示例映射”。</span><span class="sxs-lookup"><span data-stu-id="45367-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="45367-141">内部统计示例映射</span><span class="sxs-lookup"><span data-stu-id="45367-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="45367-142">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="45367-142">Click Create configuration.</span></span>

