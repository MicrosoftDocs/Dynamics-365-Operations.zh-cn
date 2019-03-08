---
title: 设置信用证的银行设施和过帐模板
description: 该过程会从始至终引导您创建所需的“银行融资和过帐模板”，以便处理“信用证”。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3419d975c087350c01c6854dbbae07b6bb20bc03
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "309924"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="433af-103">设置信用证的银行设施和过帐模板</span><span class="sxs-lookup"><span data-stu-id="433af-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="433af-104">该过程会从始至终引导您创建所需的“银行融资和过帐模板”，以便处理“信用证”。</span><span class="sxs-lookup"><span data-stu-id="433af-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="433af-105">此任务使用演示公司 "USMF"。</span><span class="sxs-lookup"><span data-stu-id="433af-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="433af-106">总分类帐参数</span><span class="sxs-lookup"><span data-stu-id="433af-106">General ledger parameter</span></span>
1. <span data-ttu-id="433af-107">转到“现金和银行管理”>“设置”>“现金和管理银行参数”。</span><span class="sxs-lookup"><span data-stu-id="433af-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="433af-108">展开“银行单据”部分。</span><span class="sxs-lookup"><span data-stu-id="433af-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="433af-109">选择“启用进口信用证”选项。</span><span class="sxs-lookup"><span data-stu-id="433af-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="433af-110">选择“启用出口信用证”选项。</span><span class="sxs-lookup"><span data-stu-id="433af-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="433af-111">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="433af-111">Click Save.</span></span>
6. <span data-ttu-id="433af-112">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="433af-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="433af-113">创建银行融资</span><span class="sxs-lookup"><span data-stu-id="433af-113">Create Bank facility</span></span>
1. <span data-ttu-id="433af-114">转到“现金和银行管理”>“设置”>“银行融资”。</span><span class="sxs-lookup"><span data-stu-id="433af-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="433af-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="433af-115">Click New.</span></span>
3. <span data-ttu-id="433af-116">在“融资组”字段中，输入银行融资组名称。</span><span class="sxs-lookup"><span data-stu-id="433af-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="433af-117">在“描述”字段中，输入银行融资组的描述。</span><span class="sxs-lookup"><span data-stu-id="433af-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="433af-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="433af-118">Click Save.</span></span>
6. <span data-ttu-id="433af-119">单击“融资类型”选项卡。</span><span class="sxs-lookup"><span data-stu-id="433af-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="433af-120">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="433af-120">Click New.</span></span>
8. <span data-ttu-id="433af-121">在“融资类型”字段中，输入唯一代码。</span><span class="sxs-lookup"><span data-stu-id="433af-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="433af-122">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="433af-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="433af-123">在“融资组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="433af-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="433af-124">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="433af-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="433af-125">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="433af-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="433af-126">在“融资性质”字段中，选择银行融资的性质。</span><span class="sxs-lookup"><span data-stu-id="433af-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="433af-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="433af-127">Click Save.</span></span>
15. <span data-ttu-id="433af-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="433af-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="433af-129">银行过帐模板</span><span class="sxs-lookup"><span data-stu-id="433af-129">Bank posting profile</span></span>
1. <span data-ttu-id="433af-130">转到“现金和银行管理”>“设置”>“银行单据过帐模板”。</span><span class="sxs-lookup"><span data-stu-id="433af-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="433af-131">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="433af-131">Click New.</span></span>
3. <span data-ttu-id="433af-132">在“帐户/组号码”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="433af-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="433af-133">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="433af-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="433af-134">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="433af-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="433af-135">选择主要帐户以进行结算。</span><span class="sxs-lookup"><span data-stu-id="433af-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="433af-136">此帐户会在计算现金流预测时使用。</span><span class="sxs-lookup"><span data-stu-id="433af-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="433af-137">在“收费帐户”字段中，选择交易费用适用的帐户。</span><span class="sxs-lookup"><span data-stu-id="433af-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="433af-138">在“利润帐户”字段中，选择交易利润适用的帐户。</span><span class="sxs-lookup"><span data-stu-id="433af-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="433af-139">当过账打开的毛利时借记此科目，当过账贷款时贷记此科目。</span><span class="sxs-lookup"><span data-stu-id="433af-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="433af-140">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="433af-140">Click Save.</span></span>

