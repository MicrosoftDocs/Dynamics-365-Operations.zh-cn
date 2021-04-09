---
title: 财务报告常见问题解答
description: 本主题列出了与其他用户已有的财务报告相关的问题。
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0718db77399901acc8c88278c5b373b77b3cb16
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811295"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="935c7-103">财务报告常见问题解答</span><span class="sxs-lookup"><span data-stu-id="935c7-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="935c7-104">本主题列出了与其他用户已有的财务报告相关的问题。</span><span class="sxs-lookup"><span data-stu-id="935c7-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="935c7-105">如何使用树安全限制对报表的访问？</span><span class="sxs-lookup"><span data-stu-id="935c7-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="935c7-106">场景：USMF 演示公司有一个资产负债表报表，它不希望所有财务报告用户都可以在 D365 中查看它。</span><span class="sxs-lookup"><span data-stu-id="935c7-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="935c7-107">解决方案：您可以利用树安全来限制对单个报表的访问，以便只有某些用户可以访问该报表。</span><span class="sxs-lookup"><span data-stu-id="935c7-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="935c7-108">登录到 Financial Reporter 报表设计器</span><span class="sxs-lookup"><span data-stu-id="935c7-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="935c7-109">创建一个新的树定义（文件 | 新建 | 树定义）a.</span><span class="sxs-lookup"><span data-stu-id="935c7-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="935c7-110">双击 **单位安全性** 列中的 **摘要** 行。</span><span class="sxs-lookup"><span data-stu-id="935c7-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="935c7-111">i.</span><span class="sxs-lookup"><span data-stu-id="935c7-111">i.</span></span>    <span data-ttu-id="935c7-112">单击“用户和组”。</span><span class="sxs-lookup"><span data-stu-id="935c7-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="935c7-113">1. 选择要访问此报表的用户或组。</span><span class="sxs-lookup"><span data-stu-id="935c7-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="935c7-114">[![用户屏幕](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="935c7-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="935c7-115">[![安全性屏幕](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="935c7-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="935c7-116">b.</span><span class="sxs-lookup"><span data-stu-id="935c7-116">b.</span></span>    <span data-ttu-id="935c7-117">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="935c7-117">Click **Save**.</span></span>
  
<span data-ttu-id="935c7-118">[![“保存”按钮](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="935c7-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="935c7-119">在报表定义中添加新的树定义</span><span class="sxs-lookup"><span data-stu-id="935c7-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="935c7-120">[![树定义窗体](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="935c7-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="935c7-121">A.</span><span class="sxs-lookup"><span data-stu-id="935c7-121">A.</span></span>  <span data-ttu-id="935c7-122">在“树定义”中单击“设置”并在“报告单位选择”下选中“包括所有单位”时</span><span class="sxs-lookup"><span data-stu-id="935c7-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="935c7-123">[![报告单位选择窗体](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="935c7-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="935c7-124">**之前：**[![屏幕截图前](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="935c7-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="935c7-125">**之后：**[![屏幕截图后](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="935c7-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="935c7-126">注意：出现上述消息的原因是我的用户在应用单位安全性后无权访问该报表</span><span class="sxs-lookup"><span data-stu-id="935c7-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="935c7-127">如何确定哪些帐户与 D365 中的余额不匹配？</span><span class="sxs-lookup"><span data-stu-id="935c7-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="935c7-128">如果您的报表与 D365 中的期望不符，则可以采取以下步骤来确定这些帐户和差异。</span><span class="sxs-lookup"><span data-stu-id="935c7-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="935c7-129">在 Financial Reporter 报表设计器中</span><span class="sxs-lookup"><span data-stu-id="935c7-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="935c7-130">创建一个新的行定义 a.</span><span class="sxs-lookup"><span data-stu-id="935c7-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="935c7-131">单击“编辑”|“插入维度中的行”i.</span><span class="sxs-lookup"><span data-stu-id="935c7-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="935c7-132">选择 MainAccount [![选择主帐户屏幕](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="935c7-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="935c7-133">ii.</span><span class="sxs-lookup"><span data-stu-id="935c7-133">ii.</span></span> <span data-ttu-id="935c7-134">单击“确定”b.</span><span class="sxs-lookup"><span data-stu-id="935c7-134">Click Ok b.</span></span>    <span data-ttu-id="935c7-135">保存行定义</span><span class="sxs-lookup"><span data-stu-id="935c7-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="935c7-136">创建一个新的列定义     [![创建一个新的列定义](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="935c7-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="935c7-137">创建一个新的报表定义 a.</span><span class="sxs-lookup"><span data-stu-id="935c7-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="935c7-138">单击“设置”并取消选中[![设置窗体](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="935c7-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="935c7-139">生成报表。</span><span class="sxs-lookup"><span data-stu-id="935c7-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="935c7-140">将报表导出到 Excel。</span><span class="sxs-lookup"><span data-stu-id="935c7-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="935c7-141">在 D365 中：</span><span class="sxs-lookup"><span data-stu-id="935c7-141">In D365:</span></span> 
1.  <span data-ttu-id="935c7-142">单击“总帐”|“查询和报表”|“试算平衡表”a.</span><span class="sxs-lookup"><span data-stu-id="935c7-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="935c7-143">参数 i.</span><span class="sxs-lookup"><span data-stu-id="935c7-143">Parameters i.</span></span>  <span data-ttu-id="935c7-144">开始日期：会计年度的开始日期 ii.</span><span class="sxs-lookup"><span data-stu-id="935c7-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="935c7-145">结束日期：生成报表的日期 iii.</span><span class="sxs-lookup"><span data-stu-id="935c7-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="935c7-146">财务维度集“主帐户集”[![“主帐户”窗体](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="935c7-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="935c7-147">b.</span><span class="sxs-lookup"><span data-stu-id="935c7-147">b.</span></span>    <span data-ttu-id="935c7-148">单击“计算”</span><span class="sxs-lookup"><span data-stu-id="935c7-148">Click Calculate</span></span>

2.  <span data-ttu-id="935c7-149">将报表导出到 Excel</span><span class="sxs-lookup"><span data-stu-id="935c7-149">Export the report to Excel</span></span>

<span data-ttu-id="935c7-150">您现在应该能够将 FR Excel 报表中的数据复制到 D365 试算平衡表报表，并比较“期末余额”列。</span><span class="sxs-lookup"><span data-stu-id="935c7-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]