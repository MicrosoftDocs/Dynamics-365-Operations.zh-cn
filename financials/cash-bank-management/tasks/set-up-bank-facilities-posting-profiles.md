--- 
title: "设置保函的银行设施和过帐模板"
description: "此任务会创建所需的银行融资和过帐模板，以便处理保函。"
author: kweekley
manager: AnnBe
ms.date: 02/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c23fe66c58e9ceff74469cc8eab61eb606c57ee1
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="f9c95-103">设置保函的银行设施和过帐模板</span><span class="sxs-lookup"><span data-stu-id="f9c95-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9c95-104">此任务会创建所需的银行融资和过帐模板，以便处理保函。</span><span class="sxs-lookup"><span data-stu-id="f9c95-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="f9c95-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="f9c95-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="f9c95-106">总分类帐参数</span><span class="sxs-lookup"><span data-stu-id="f9c95-106">General ledger parameter</span></span>
1. <span data-ttu-id="f9c95-107">转到“现金和银行管理”>“设置”>“现金和管理银行参数”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="f9c95-108">展开“银行单据”部分。</span><span class="sxs-lookup"><span data-stu-id="f9c95-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="f9c95-109">选择“启用保函”选项。</span><span class="sxs-lookup"><span data-stu-id="f9c95-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="f9c95-110">在”交易记录日记帐“字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f9c95-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f9c95-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f9c95-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f9c95-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f9c95-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f9c95-113">单击“数序”选项卡。</span><span class="sxs-lookup"><span data-stu-id="f9c95-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="f9c95-114">定义保函编号的数序代码和保函交易记录参考资料</span><span class="sxs-lookup"><span data-stu-id="f9c95-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="f9c95-115">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-115">Click Save.</span></span>
9. <span data-ttu-id="f9c95-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f9c95-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="f9c95-117">创建银行融资</span><span class="sxs-lookup"><span data-stu-id="f9c95-117">Create Bank facility</span></span>
1. <span data-ttu-id="f9c95-118">转到“现金和银行管理”>“设置”>“银行融资”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="f9c95-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-119">Click New.</span></span>
3. <span data-ttu-id="f9c95-120">在“融资组”字段中，输入保函交易记录适用的银行融资组名称。</span><span class="sxs-lookup"><span data-stu-id="f9c95-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="f9c95-121">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f9c95-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f9c95-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-122">Click Save.</span></span>
6. <span data-ttu-id="f9c95-123">单击“融资类型”选项卡。</span><span class="sxs-lookup"><span data-stu-id="f9c95-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="f9c95-124">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-124">Click New.</span></span>
8. <span data-ttu-id="f9c95-125">在“融资类型”字段中，输入与银行融资协议有关的银行融资类型的名称。</span><span class="sxs-lookup"><span data-stu-id="f9c95-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="f9c95-126">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f9c95-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="f9c95-127">在“融资组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f9c95-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f9c95-128">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f9c95-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f9c95-129">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f9c95-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="f9c95-130">在“融资性质”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f9c95-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="f9c95-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-131">Click Save.</span></span>
15. <span data-ttu-id="f9c95-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f9c95-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="f9c95-133">银行过帐模板</span><span class="sxs-lookup"><span data-stu-id="f9c95-133">Bank posting profile</span></span>
1. <span data-ttu-id="f9c95-134">转到“现金和银行管理”>“设置”>“银行单据过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="f9c95-135">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-135">Click New.</span></span>
3. <span data-ttu-id="f9c95-136">在“帐户/组号码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f9c95-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f9c95-137">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f9c95-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f9c95-138">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="f9c95-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f9c95-139">在“结算帐户”字段中，选择结算适用的主要帐户。</span><span class="sxs-lookup"><span data-stu-id="f9c95-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="f9c95-140">在“收费帐户”字段中，选择交易费用适用的帐户。</span><span class="sxs-lookup"><span data-stu-id="f9c95-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="f9c95-141">在“利润帐户”字段中，选择交易利润适用的帐户。</span><span class="sxs-lookup"><span data-stu-id="f9c95-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="f9c95-142">在“清算帐户”字段中，选择保函交易记录使用的清除帐户。</span><span class="sxs-lookup"><span data-stu-id="f9c95-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="f9c95-143">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f9c95-143">Click Save.</span></span>
11. <span data-ttu-id="f9c95-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f9c95-144">Close the page.</span></span>


