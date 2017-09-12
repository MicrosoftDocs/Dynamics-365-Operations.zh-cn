--- 
title: "针对电子申报 (ER) 选择数据模型定义，同时创建格式"
description: "为了完成此过程中的步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。"
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 79e5c09484f9d33106194c2a8b2c9971d58d0e75
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="select-data-model-definition-while-creating-format-for-electronic-reporting-er"></a><span data-ttu-id="26420-103">针对电子申报 (ER) 选择数据模型定义，同时创建格式</span><span class="sxs-lookup"><span data-stu-id="26420-103">Select data model definition while creating format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26420-104">为了完成此过程中的步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。</span><span class="sxs-lookup"><span data-stu-id="26420-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="26420-105">此过程显示如何将模型的根项作为数据模型定义选择，以便插入为生成电子单据而设计的电子申报 (ER) 格式配置。</span><span class="sxs-lookup"><span data-stu-id="26420-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="26420-106">在此过程中，您将为示例公司 Litware 公司添加一个新的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="26420-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="26420-107">此过程针对向其分配了系统管理员角色或电子申报开发人员角色的用户。</span><span class="sxs-lookup"><span data-stu-id="26420-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="26420-108">可使用任何数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="26420-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="26420-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="26420-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="26420-110">确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。</span><span class="sxs-lookup"><span data-stu-id="26420-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="26420-111">如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="26420-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="26420-112">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="26420-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="26420-113">添加新 ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="26420-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="26420-114">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="26420-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="26420-115">我们新增一个 ER 模型配置，其中包含一个数据模型，设计为用作生成 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="26420-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="26420-116">在“名称”字段中，键入“付款模型（虚构）”。</span><span class="sxs-lookup"><span data-stu-id="26420-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="26420-117">付款模型（虚构）</span><span class="sxs-lookup"><span data-stu-id="26420-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="26420-118">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="26420-118">Click Create configuration.</span></span>
4. <span data-ttu-id="26420-119">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="26420-119">Click Designer.</span></span>
    * <span data-ttu-id="26420-120">打开 ER 设计器以指定此配置的数据模型结构。</span><span class="sxs-lookup"><span data-stu-id="26420-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="26420-121">假设为付款业务域设计数据模型，以便为贷方转帐和直接借记这两种付款方式提供支持。</span><span class="sxs-lookup"><span data-stu-id="26420-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="26420-122">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="26420-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="26420-123">在“名称”字段中，键入“付款 - 贷方转帐”。</span><span class="sxs-lookup"><span data-stu-id="26420-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="26420-124">付款 - 贷方转帐</span><span class="sxs-lookup"><span data-stu-id="26420-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="26420-125">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="26420-125">Click Add.</span></span>
8. <span data-ttu-id="26420-126">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="26420-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="26420-127">在“作为以下项的新节点”字段中，输入“模型根”。</span><span class="sxs-lookup"><span data-stu-id="26420-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="26420-128">在“名称”字段中，键入“付款 - 直接借记”。</span><span class="sxs-lookup"><span data-stu-id="26420-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="26420-129">付款 - 直接借记</span><span class="sxs-lookup"><span data-stu-id="26420-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="26420-130">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="26420-130">Click Add.</span></span>
12. <span data-ttu-id="26420-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="26420-131">Click Save.</span></span>
13. <span data-ttu-id="26420-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="26420-132">Close the page.</span></span>
14. <span data-ttu-id="26420-133">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="26420-133">Click Change status.</span></span>
    * <span data-ttu-id="26420-134">完成模型的草稿版本，以便将其提供给新模型映射和格式。</span><span class="sxs-lookup"><span data-stu-id="26420-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="26420-135">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="26420-135">Click Complete.</span></span>
16. <span data-ttu-id="26420-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="26420-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="26420-137">开始输入新 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="26420-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="26420-138">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="26420-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="26420-139">在“新建”字段中，输入“基于数据模型‘付款模型（虚构）’的格式”。</span><span class="sxs-lookup"><span data-stu-id="26420-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="26420-140">在“数据模型定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="26420-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="26420-141">请注意，所选数据模型的所有根项均可作为数据模型定义选择。</span><span class="sxs-lookup"><span data-stu-id="26420-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="26420-142">可通过使用数据模型的任何所需根项继续设计格式。</span><span class="sxs-lookup"><span data-stu-id="26420-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="26420-143">缺少所选根项的模型映射不会妨碍您继续操作。</span><span class="sxs-lookup"><span data-stu-id="26420-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="26420-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="26420-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="26420-145">添加新 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="26420-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="26420-146">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="26420-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="26420-147">在“新建”字段中，输入“基于数据模型‘付款模型（虚构）’的模型映射”。</span><span class="sxs-lookup"><span data-stu-id="26420-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="26420-148">在“名称”字段中，键入“付款模型映射（虚构）”。</span><span class="sxs-lookup"><span data-stu-id="26420-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="26420-149">付款模型映射（虚构）</span><span class="sxs-lookup"><span data-stu-id="26420-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="26420-150">在“数据模型定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="26420-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="26420-151">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="26420-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="26420-152">设计 ER 模型映射</span><span class="sxs-lookup"><span data-stu-id="26420-152">Design ER model mappings</span></span>
1. <span data-ttu-id="26420-153">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="26420-153">Click Designer.</span></span>
    * <span data-ttu-id="26420-154">使用 ER 设计器为所需根项指定模型映射。</span><span class="sxs-lookup"><span data-stu-id="26420-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="26420-155">单击“设计器”。</span><span class="sxs-lookup"><span data-stu-id="26420-155">Click Designer.</span></span>
    * <span data-ttu-id="26420-156">模拟设置所选模型的根项的所选模型映射。</span><span class="sxs-lookup"><span data-stu-id="26420-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="26420-157">在树结构中，选择“Dynamics 365 for Operations\表格记录”。</span><span class="sxs-lookup"><span data-stu-id="26420-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="26420-158">单击“添加根”。</span><span class="sxs-lookup"><span data-stu-id="26420-158">Click Add root.</span></span>
5. <span data-ttu-id="26420-159">在“名称”字段中，键入“分类帐”。</span><span class="sxs-lookup"><span data-stu-id="26420-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="26420-160">在“表格”字段中，键入“分类日记帐交易记录”。</span><span class="sxs-lookup"><span data-stu-id="26420-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="26420-161">分类日记帐交易记录</span><span class="sxs-lookup"><span data-stu-id="26420-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="26420-162">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="26420-162">Click OK.</span></span>
8. <span data-ttu-id="26420-163">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="26420-163">Click Save.</span></span>
9. <span data-ttu-id="26420-164">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="26420-164">Close the page.</span></span>
10. <span data-ttu-id="26420-165">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="26420-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="26420-166">开始输入又一个新 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="26420-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="26420-167">在树中，选择“付款模型（虚构）”。</span><span class="sxs-lookup"><span data-stu-id="26420-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="26420-168">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="26420-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="26420-169">在“新建”字段中，输入“基于数据模型‘付款模型（虚构）’的格式”。</span><span class="sxs-lookup"><span data-stu-id="26420-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="26420-170">在“数据模型定义”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="26420-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="26420-171">请注意，现在只有一个根项可映射到应用程序数据源。</span><span class="sxs-lookup"><span data-stu-id="26420-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="26420-172">如果引入了至少一个模型映射，添加 ER 格式时，只能将映射到应用程序数据源的模型根项选择为模型定义。</span><span class="sxs-lookup"><span data-stu-id="26420-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="26420-173">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="26420-173">Close the page.</span></span>


