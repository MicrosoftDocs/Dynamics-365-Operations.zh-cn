--- 
title: "CN-00016 按中国工作规则的用户操作日志"
description: "此过程演示如何创建用户操作日志。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysDatabaseLogSetup, SysDatabaseLogWizard, BankAccountTable, ComplianceUserOperationLogConfig_CN
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 7fd291073de7d0437201a858f9ed5e4cc9cb8b27
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="cn-00016-user-operation-log-by-china-working-rule"></a><span data-ttu-id="788a4-103">CN-00016 按中国工作规则的用户操作日志</span><span class="sxs-lookup"><span data-stu-id="788a4-103">CN-00016 User operation log by China working rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="788a4-104">此过程演示如何创建用户操作日志。</span><span class="sxs-lookup"><span data-stu-id="788a4-104">This procedure demonstrates how to generate a user operation log.</span></span> <span data-ttu-id="788a4-105">必须先设置数据库日志，才能生成用户操作日志。</span><span class="sxs-lookup"><span data-stu-id="788a4-105">The database log must be set up before you can generate the user operation log.</span></span>  

<span data-ttu-id="788a4-106">根据您指定的条件跟踪用户操作并记录在日志中，包括操作类型、用户名，以及时间和日期。</span><span class="sxs-lookup"><span data-stu-id="788a4-106">Based on the criteria that you specify,  user operations are tracked and recorded in a log, including the type of operation, user name, and time and date.</span></span> <span data-ttu-id="788a4-107">此过程逐步演示如何为跟踪银行帐户的创建设置条件，为演示目的创建银行帐户，然后生成用户日志。</span><span class="sxs-lookup"><span data-stu-id="788a4-107">This procedure walks you through setting up criteria for tracking bank account creation, creating a bank account for demonstration purposes, and then generating the user log.</span></span>

<span data-ttu-id="788a4-108">此程序使用 CNMF 演示数据。</span><span class="sxs-lookup"><span data-stu-id="788a4-108">This procedure uses the CNMF demo data.</span></span> <span data-ttu-id="788a4-109">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="788a4-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-the-database-log"></a><span data-ttu-id="788a4-110">设置数据库日志</span><span class="sxs-lookup"><span data-stu-id="788a4-110">Set up the database log</span></span>
1. <span data-ttu-id="788a4-111">转到“系统管理”>“设置”>“数据库日志配置”。</span><span class="sxs-lookup"><span data-stu-id="788a4-111">Go to System administration > Setup > Database log setup.</span></span>
2. <span data-ttu-id="788a4-112">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="788a4-112">Click New.</span></span>
3. <span data-ttu-id="788a4-113">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="788a4-113">Click Next.</span></span>
4. <span data-ttu-id="788a4-114">在树中，展开“银行”。</span><span class="sxs-lookup"><span data-stu-id="788a4-114">In the tree, expand 'Bank'.</span></span>
5. <span data-ttu-id="788a4-115">在树中，检查“银行\银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="788a4-115">In the tree, check 'Bank\Bank accounts'.</span></span>
    * <span data-ttu-id="788a4-116">对于此演示，我们希望跟踪谁创建银行帐户，但是您可能希望跟踪其他用户操作。</span><span class="sxs-lookup"><span data-stu-id="788a4-116">For this demonstration, we want to keep track of who creates bank accounts, but you may want to track other user actions.</span></span>  
6. <span data-ttu-id="788a4-117">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="788a4-117">Click Next.</span></span>
7. <span data-ttu-id="788a4-118">选中“跟踪新交易记录”复选框。</span><span class="sxs-lookup"><span data-stu-id="788a4-118">Select the Track new transactions check box.</span></span>
8. <span data-ttu-id="788a4-119">选中“更新”复选框。</span><span class="sxs-lookup"><span data-stu-id="788a4-119">Select the Update check box.</span></span>
9. <span data-ttu-id="788a4-120">选中“删除”复选框。</span><span class="sxs-lookup"><span data-stu-id="788a4-120">Select the Delete check box.</span></span>
10. <span data-ttu-id="788a4-121">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="788a4-121">Click Next.</span></span>
11. <span data-ttu-id="788a4-122">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="788a4-122">Click Finish.</span></span>

## <a name="create-a-new-bank-account-for-demonstration-purposes"></a><span data-ttu-id="788a4-123">出于演示目的新建银行帐户</span><span class="sxs-lookup"><span data-stu-id="788a4-123">Create a new bank account for demonstration purposes</span></span>
1. <span data-ttu-id="788a4-124">转至“现金和银行管理”>“银行对账单对帐”>“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="788a4-124">Go to Cash and bank management > Bank statement reconciliation > Bank accounts.</span></span>
2. <span data-ttu-id="788a4-125">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="788a4-125">Click New.</span></span>
3. <span data-ttu-id="788a4-126">在“银行帐户”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="788a4-126">In the Bank account field, type a value.</span></span>
4. <span data-ttu-id="788a4-127">在“银行帐号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="788a4-127">In the Bank account number field, type a value.</span></span>
5. <span data-ttu-id="788a4-128">在“主科目”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="788a4-128">In the Main account field, specify the desired values.</span></span>
6. <span data-ttu-id="788a4-129">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="788a4-129">Click Save.</span></span>

## <a name="print-the-user-operation-log-report"></a><span data-ttu-id="788a4-130">打印用户操作日志报告</span><span class="sxs-lookup"><span data-stu-id="788a4-130">Print the user operation log report</span></span>
1. <span data-ttu-id="788a4-131">转到“系统管理”>“查询”>“用户操作日志查询”。</span><span class="sxs-lookup"><span data-stu-id="788a4-131">Go to System administration > Inquiries > User operation log inquiry.</span></span>
2. <span data-ttu-id="788a4-132">在树中，展开“银行”。</span><span class="sxs-lookup"><span data-stu-id="788a4-132">In the tree, expand 'Bank'.</span></span>
3. <span data-ttu-id="788a4-133">在树中，检查“银行\银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="788a4-133">In the tree, check 'Bank\Bank accounts'.</span></span>
4. <span data-ttu-id="788a4-134">展开“按用户”部分。</span><span class="sxs-lookup"><span data-stu-id="788a4-134">Expand the By user section.</span></span>
5. <span data-ttu-id="788a4-135">在“用户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="788a4-135">In the User field, enter or select a value.</span></span>
    * <span data-ttu-id="788a4-136">对于此示例，如果您在上一个子任务中创建了银行帐户，请选择您的用户名。</span><span class="sxs-lookup"><span data-stu-id="788a4-136">For this example, select your user name if you created the bank account in the previous subtask.</span></span> <span data-ttu-id="788a4-137">否则选择最近创建了银行帐户的其他用户。</span><span class="sxs-lookup"><span data-stu-id="788a4-137">Otherwise, select another user who created a bank account recently.</span></span>  
6. <span data-ttu-id="788a4-138">展开“按日期”部分。</span><span class="sxs-lookup"><span data-stu-id="788a4-138">Expand the By date section.</span></span>
7. <span data-ttu-id="788a4-139">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="788a4-139">In the From date field, enter a date.</span></span>
8. <span data-ttu-id="788a4-140">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="788a4-140">In the To date field, enter a date.</span></span>
9. <span data-ttu-id="788a4-141">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="788a4-141">Click OK.</span></span>
10. <span data-ttu-id="788a4-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="788a4-142">Click OK.</span></span>


