---
title: 创建电子申报 (ER) 模型映射配置
description: 此过程用于设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a614ce0f055691e36c1aab5d84d4fc3355026f1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752548"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="fa01b-103">创建电子申报 (ER) 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="fa01b-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa01b-104">此过程用于设计新电子申报 (ER) 模型映射配置和使用内置 ER 执行有效聚合计算的信息。</span><span class="sxs-lookup"><span data-stu-id="fa01b-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="fa01b-105">在此过程中，您将创建示例公司“Litware 公司”的配置。</span><span class="sxs-lookup"><span data-stu-id="fa01b-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="fa01b-106">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="fa01b-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="fa01b-107">可使用任何数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="fa01b-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="fa01b-108">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="fa01b-108">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="fa01b-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="fa01b-110">确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="fa01b-111">如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="fa01b-111">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>  
2. <span data-ttu-id="fa01b-112">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="fa01b-113">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-113">Click Show filters.</span></span>
4. <span data-ttu-id="fa01b-114">在“名称”字段中输入筛选器值、“内部统计”并使用筛选器运算符“begins with”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="fa01b-115">应用此筛选器来查找“内部统计”数据模型配置。</span><span class="sxs-lookup"><span data-stu-id="fa01b-115">Apply this filter to find the 'Intrastat' data model configuration.</span></span> <span data-ttu-id="fa01b-116">此模型可能已在配置树中存在。</span><span class="sxs-lookup"><span data-stu-id="fa01b-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="fa01b-117">如果存在，请跳过下一个子任务。</span><span class="sxs-lookup"><span data-stu-id="fa01b-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="fa01b-118">获取 Microsoft 提供的内部统计模型配置</span><span class="sxs-lookup"><span data-stu-id="fa01b-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="fa01b-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fa01b-119">Close the page.</span></span>
2. <span data-ttu-id="fa01b-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fa01b-120">Close the page.</span></span>
3. <span data-ttu-id="fa01b-121">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="fa01b-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="fa01b-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fa01b-123">选择 Microsoft 提供程序磁贴。</span><span class="sxs-lookup"><span data-stu-id="fa01b-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="fa01b-124">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-124">Click Repositories.</span></span>
    * <span data-ttu-id="fa01b-125">单击 Microsoft 提供程序磁贴上的“存储库”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="fa01b-126">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-126">Click Show filters.</span></span>
7. <span data-ttu-id="fa01b-127">在“类型名称”字段中输入筛选器值、“资源”并使用筛选器运算符“contains”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-127">In the "Type name" field, enter the filter value, "resources" and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="fa01b-128">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-128">Click Open.</span></span>
9. <span data-ttu-id="fa01b-129">在树中，选择“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="fa01b-130">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-130">Click Import.</span></span>
11. <span data-ttu-id="fa01b-131">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-131">Click Yes.</span></span>
    * <span data-ttu-id="fa01b-132">您导入了包含您将用于探索新 ER 功能如何使用的数据模型的 ER 模型配置。</span><span class="sxs-lookup"><span data-stu-id="fa01b-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="fa01b-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fa01b-133">Close the page.</span></span>
13. <span data-ttu-id="fa01b-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fa01b-134">Close the page.</span></span>
14. <span data-ttu-id="fa01b-135">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="fa01b-136">添加新模型映射配置</span><span class="sxs-lookup"><span data-stu-id="fa01b-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="fa01b-137">在树中，选择“内部统计模型”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="fa01b-138">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="fa01b-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="fa01b-139">在“新建”字段中，输入“基于数据模型内部统计的模型映射”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="fa01b-140">在“名称”字段中，键入“内部统计示例映射”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="fa01b-141">内部统计示例映射</span><span class="sxs-lookup"><span data-stu-id="fa01b-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="fa01b-142">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="fa01b-142">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]