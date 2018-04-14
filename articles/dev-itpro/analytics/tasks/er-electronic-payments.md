--- 
title: "针对电子申报 (ER) 使用格式配置生成付款的电子单据"
description: "以下步骤说明属于系统管理员或电子申报开发人员的用户如何使用新电子申报 (ER) 格式配置来生成用于处理付款的电子单据。"
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 98c25b884deb82f9d0655dde7790dfb57d7c13f6
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="04bda-103">针对电子申报 (ER) 使用格式配置生成付款的电子单据</span><span class="sxs-lookup"><span data-stu-id="04bda-103">Generate electronic documents for payments using a format configuration for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04bda-104">以下步骤说明属于系统管理员或电子申报开发人员的用户如何使用新电子申报 (ER) 格式配置来生成用于处理付款的电子单据。</span><span class="sxs-lookup"><span data-stu-id="04bda-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="04bda-105">这些步骤可以在 GBSI 示例公司执行。</span><span class="sxs-lookup"><span data-stu-id="04bda-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="04bda-106">为了完成这些步骤，您必须首先完成“使用付款单据格式创建配置”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="04bda-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="04bda-107">更改电子付款方式的配置</span><span class="sxs-lookup"><span data-stu-id="04bda-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="04bda-108">转至“应付账款”>“付款设置”>“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="04bda-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="04bda-109">如果需要，切换“文件格式”部分以展开它。</span><span class="sxs-lookup"><span data-stu-id="04bda-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="04bda-110">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="04bda-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="04bda-111">例如，在含有“电子”值的“付款方式”字段中筛选。</span><span class="sxs-lookup"><span data-stu-id="04bda-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="04bda-112">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="04bda-112">Click Edit.</span></span>
5. <span data-ttu-id="04bda-113">将“一般电子申报”字段设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="04bda-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="04bda-114">选择是为付款文件生成使用常规电子申报模式。</span><span class="sxs-lookup"><span data-stu-id="04bda-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="04bda-115">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="04bda-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="04bda-116">选择 BACS（英国虚构）格式配置。</span><span class="sxs-lookup"><span data-stu-id="04bda-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="04bda-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="04bda-117">Click Save.</span></span>
9. <span data-ttu-id="04bda-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="04bda-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="04bda-119">测试生成的付款文件的格式</span><span class="sxs-lookup"><span data-stu-id="04bda-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="04bda-120">转至“应付账款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="04bda-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="04bda-121">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="04bda-121">Click New.</span></span>
3. <span data-ttu-id="04bda-122">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="04bda-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="04bda-123">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="04bda-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="04bda-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="04bda-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="04bda-125">选择 VendPay。</span><span class="sxs-lookup"><span data-stu-id="04bda-125">Select VendPay.</span></span>  
6. <span data-ttu-id="04bda-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="04bda-126">Click Save.</span></span>
7. <span data-ttu-id="04bda-127">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="04bda-127">Click Lines.</span></span>
8. <span data-ttu-id="04bda-128">在“公司”字段中，键入 'DEMF'。</span><span class="sxs-lookup"><span data-stu-id="04bda-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="04bda-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="04bda-129">DEMF</span></span>  
9. <span data-ttu-id="04bda-130">在账号字段，设定值为“DE-01001"。</span><span class="sxs-lookup"><span data-stu-id="04bda-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="04bda-131">DE-01001</span><span class="sxs-lookup"><span data-stu-id="04bda-131">DE-01001</span></span>  
10. <span data-ttu-id="04bda-132">在“描述”字段中，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="04bda-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="04bda-133">付款</span><span class="sxs-lookup"><span data-stu-id="04bda-133">Payment</span></span>  
11. <span data-ttu-id="04bda-134">在“借方”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="04bda-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="04bda-135">1000</span><span class="sxs-lookup"><span data-stu-id="04bda-135">1000</span></span>  
12. <span data-ttu-id="04bda-136">单击“付款”选项卡。</span><span class="sxs-lookup"><span data-stu-id="04bda-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="04bda-137">在“付款方式”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="04bda-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="04bda-138">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="04bda-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="04bda-139">选择“电子值”。</span><span class="sxs-lookup"><span data-stu-id="04bda-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="04bda-140">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="04bda-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="04bda-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="04bda-141">Click Save.</span></span>
17. <span data-ttu-id="04bda-142">点击”生成付款“。</span><span class="sxs-lookup"><span data-stu-id="04bda-142">Click Generate payments.</span></span>
18. <span data-ttu-id="04bda-143">在“付款方式”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="04bda-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="04bda-144">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="04bda-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="04bda-145">选择“电子值”。</span><span class="sxs-lookup"><span data-stu-id="04bda-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="04bda-146">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="04bda-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="04bda-147">选择“电子值”。</span><span class="sxs-lookup"><span data-stu-id="04bda-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="04bda-148">在文件名字段，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="04bda-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="04bda-149">例如，键入“付款”。</span><span class="sxs-lookup"><span data-stu-id="04bda-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="04bda-150">在“银行帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="04bda-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="04bda-151">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="04bda-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="04bda-152">选择值 GBSI OPER。</span><span class="sxs-lookup"><span data-stu-id="04bda-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="04bda-153">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04bda-153">Click OK.</span></span>
25. <span data-ttu-id="04bda-154">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="04bda-154">Click OK.</span></span>
    * <span data-ttu-id="04bda-155">分析以 XML 格式创建的付款文件。</span><span class="sxs-lookup"><span data-stu-id="04bda-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="04bda-156">将其与设计的文档格式和定义的付款交易记录属性比较。</span><span class="sxs-lookup"><span data-stu-id="04bda-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  


