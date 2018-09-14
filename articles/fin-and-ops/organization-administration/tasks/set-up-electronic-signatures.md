--- 
title: "设置电子签名"
description: "使用该过程设置电子签名。"
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: eb6bf529b1e94d598e219482f182140402f2928a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="47890-103">设置电子签名</span><span class="sxs-lookup"><span data-stu-id="47890-103">Set up electronic signatures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47890-104">使用该过程设置电子签名。</span><span class="sxs-lookup"><span data-stu-id="47890-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="47890-105">电子签名确认要启动或审核计算流程的人员的身份。</span><span class="sxs-lookup"><span data-stu-id="47890-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="47890-106">用于创建该过程的演示数据公司是 DAT。</span><span class="sxs-lookup"><span data-stu-id="47890-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="47890-107">启用“电子签名配置密钥”</span><span class="sxs-lookup"><span data-stu-id="47890-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="47890-108">转到“系统管理”>“设置”>“允许”>“许可证配置”。</span><span class="sxs-lookup"><span data-stu-id="47890-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="47890-109">在树形图中，展开“管理”。</span><span class="sxs-lookup"><span data-stu-id="47890-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="47890-110">核实“电子签名”复选框是否已选中。</span><span class="sxs-lookup"><span data-stu-id="47890-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="47890-111">如果“电子签名”复选框未选中，您必须启用维护模式。</span><span class="sxs-lookup"><span data-stu-id="47890-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="47890-112">通过运行来自“生命周期服务”的维护作业，或通过在本地使用 Deployment.Setup 工具，可以在此环境下启用维护模式。</span><span class="sxs-lookup"><span data-stu-id="47890-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="47890-113">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="47890-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="47890-114">设置电子签名参数</span><span class="sxs-lookup"><span data-stu-id="47890-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="47890-115">转到“组织管理”>“设置”>“电子签名”>“电子签名参数”。</span><span class="sxs-lookup"><span data-stu-id="47890-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="47890-116">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="47890-116">Click Edit.</span></span>
3. <span data-ttu-id="47890-117">在“通知”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="47890-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="47890-118">输入在请求签名时签名人将要收到的通知。</span><span class="sxs-lookup"><span data-stu-id="47890-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="47890-119">您可以输入任意文本。</span><span class="sxs-lookup"><span data-stu-id="47890-119">You can enter any text.</span></span> <span data-ttu-id="47890-120">一般此文本将告诉用户对文档进行电子签名意味着什么。</span><span class="sxs-lookup"><span data-stu-id="47890-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="47890-121">如果您想使用其他语言输入“通知”文本，请单击“翻译”按钮。</span><span class="sxs-lookup"><span data-stu-id="47890-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="47890-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="47890-122">Click Save.</span></span>
5. <span data-ttu-id="47890-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="47890-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="47890-124">设置电子签名的原因代码</span><span class="sxs-lookup"><span data-stu-id="47890-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="47890-125">转到“组织管理”>“设置”>“电子签名”>“电子签名原因代码”。</span><span class="sxs-lookup"><span data-stu-id="47890-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="47890-126">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="47890-126">Click New.</span></span>
    * <span data-ttu-id="47890-127">在使用电子签名前必须设置原因代码。</span><span class="sxs-lookup"><span data-stu-id="47890-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="47890-128">对文档签名时需要有效的原因代码。</span><span class="sxs-lookup"><span data-stu-id="47890-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="47890-129">签名人选择指示电子签名用途的原因代码。</span><span class="sxs-lookup"><span data-stu-id="47890-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="47890-130">例如，原因代码可以用于指示合法性。</span><span class="sxs-lookup"><span data-stu-id="47890-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="47890-131">在“原因代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="47890-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="47890-132">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="47890-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="47890-133">如果需要，输入其他原因代码。</span><span class="sxs-lookup"><span data-stu-id="47890-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="47890-134">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="47890-134">Click Save.</span></span>
6. <span data-ttu-id="47890-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="47890-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="47890-136">现有流程所需的电子签名</span><span class="sxs-lookup"><span data-stu-id="47890-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="47890-137">转到“组织管理”>“设置”>“电子签名”>“电子签名要求”。</span><span class="sxs-lookup"><span data-stu-id="47890-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="47890-138">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="47890-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="47890-139">选择一个需要电子签名的流程。</span><span class="sxs-lookup"><span data-stu-id="47890-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="47890-140">选择或取消选择“所需的签名”复选框。</span><span class="sxs-lookup"><span data-stu-id="47890-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="47890-141">对于需要电子签名的每一个流程，重复执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="47890-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="47890-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="47890-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="47890-143">创建电子签名的自定义要求</span><span class="sxs-lookup"><span data-stu-id="47890-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="47890-144">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="47890-144">Click New.</span></span>
2. <span data-ttu-id="47890-145">选择或取消选择“所需的签名”复选框。</span><span class="sxs-lookup"><span data-stu-id="47890-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="47890-146">在“名称”字段中，输入需要电子签名流程中适用的名称。</span><span class="sxs-lookup"><span data-stu-id="47890-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="47890-147">在“表格名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="47890-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="47890-148">在列表中，查找并选择必须签名的数据将存储在其中的表格。</span><span class="sxs-lookup"><span data-stu-id="47890-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="47890-149">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="47890-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="47890-150">在“字段名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="47890-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="47890-151">在列表中，查找并选择您想要监控的表格中的字段。</span><span class="sxs-lookup"><span data-stu-id="47890-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="47890-152">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="47890-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="47890-153">指定何时需要签名。</span><span class="sxs-lookup"><span data-stu-id="47890-153">Specify when a signature is required.</span></span>     <span data-ttu-id="47890-154">如果当字段中的数据发生更改时需要签名，请选择“始终”。</span><span class="sxs-lookup"><span data-stu-id="47890-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="47890-155">如果仅在某些情况下需要签名，请选择“仅”。</span><span class="sxs-lookup"><span data-stu-id="47890-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="47890-156">如果您选择“仅”，您还必须选择以下选项之一：在插入记录时，在更新记录或删除记录时。</span><span class="sxs-lookup"><span data-stu-id="47890-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="47890-157">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="47890-157">Click Save.</span></span>
11. <span data-ttu-id="47890-158">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="47890-158">Close the page.</span></span>


