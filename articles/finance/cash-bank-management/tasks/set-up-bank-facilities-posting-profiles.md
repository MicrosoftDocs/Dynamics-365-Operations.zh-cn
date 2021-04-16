---
title: 设置保函的银行设施和过帐模板
description: 此任务会创建所需的银行融资和过帐模板，以便处理保函。
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1147650944ba40d1c8054444c09db9c5ee97bde3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834612"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="b41ed-103">设置保函的银行设施和过帐模板</span><span class="sxs-lookup"><span data-stu-id="b41ed-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b41ed-104">此任务会创建所需的银行融资和过帐模板，以便处理保函。</span><span class="sxs-lookup"><span data-stu-id="b41ed-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="b41ed-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="b41ed-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="b41ed-106">总分类帐参数</span><span class="sxs-lookup"><span data-stu-id="b41ed-106">General ledger parameter</span></span>
1. <span data-ttu-id="b41ed-107">转到“现金和银行管理”>“设置”>“现金和管理银行参数”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="b41ed-108">展开“银行单据”部分。</span><span class="sxs-lookup"><span data-stu-id="b41ed-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="b41ed-109">选择“启用保函”选项。</span><span class="sxs-lookup"><span data-stu-id="b41ed-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="b41ed-110">在”交易记录日记帐“字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b41ed-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b41ed-111">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b41ed-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b41ed-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b41ed-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b41ed-113">单击“数序”选项卡。</span><span class="sxs-lookup"><span data-stu-id="b41ed-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="b41ed-114">定义保函编号的数序代码和保函交易记录参考资料</span><span class="sxs-lookup"><span data-stu-id="b41ed-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="b41ed-115">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-115">Click Save.</span></span>
9. <span data-ttu-id="b41ed-116">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b41ed-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="b41ed-117">创建银行融资</span><span class="sxs-lookup"><span data-stu-id="b41ed-117">Create Bank facility</span></span>
1. <span data-ttu-id="b41ed-118">转到“现金和银行管理”>“设置”>“银行融资”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="b41ed-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-119">Click New.</span></span>
3. <span data-ttu-id="b41ed-120">在“融资组”字段中，输入保函交易记录适用的银行融资组名称。</span><span class="sxs-lookup"><span data-stu-id="b41ed-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="b41ed-121">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b41ed-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b41ed-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-122">Click Save.</span></span>
6. <span data-ttu-id="b41ed-123">单击“融资类型”选项卡。</span><span class="sxs-lookup"><span data-stu-id="b41ed-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="b41ed-124">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-124">Click New.</span></span>
8. <span data-ttu-id="b41ed-125">在“融资类型”字段中，输入与银行融资协议有关的银行融资类型的名称。</span><span class="sxs-lookup"><span data-stu-id="b41ed-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="b41ed-126">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="b41ed-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="b41ed-127">在“融资组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b41ed-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b41ed-128">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b41ed-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b41ed-129">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b41ed-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="b41ed-130">在“融资性质”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="b41ed-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="b41ed-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-131">Click Save.</span></span>
15. <span data-ttu-id="b41ed-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b41ed-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="b41ed-133">银行过帐模板</span><span class="sxs-lookup"><span data-stu-id="b41ed-133">Bank posting profile</span></span>
1. <span data-ttu-id="b41ed-134">转到“现金和银行管理”>“设置”>“银行单据过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="b41ed-135">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-135">Click New.</span></span>
3. <span data-ttu-id="b41ed-136">在“帐户/组号码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="b41ed-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b41ed-137">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="b41ed-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b41ed-138">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="b41ed-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b41ed-139">在“结算帐户”字段中，选择结算适用的主要帐户。</span><span class="sxs-lookup"><span data-stu-id="b41ed-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="b41ed-140">在“收费帐户”字段中，选择交易费用适用的帐户。</span><span class="sxs-lookup"><span data-stu-id="b41ed-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="b41ed-141">在“利润帐户”字段中，选择交易利润适用的帐户。</span><span class="sxs-lookup"><span data-stu-id="b41ed-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="b41ed-142">在“清算帐户”字段中，选择保函交易记录使用的清除帐户。</span><span class="sxs-lookup"><span data-stu-id="b41ed-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="b41ed-143">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b41ed-143">Click Save.</span></span>
11. <span data-ttu-id="b41ed-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b41ed-144">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]