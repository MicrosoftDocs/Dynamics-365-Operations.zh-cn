---
title: 财务报告常见问题
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
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923017"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="a296d-103">财务报告常见问题</span><span class="sxs-lookup"><span data-stu-id="a296d-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="a296d-104">本主题提供有关财务报告的常见问题的解答。</span><span class="sxs-lookup"><span data-stu-id="a296d-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="a296d-105">如何使用树安全限制对报表的访问？</span><span class="sxs-lookup"><span data-stu-id="a296d-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="a296d-106">以下示例说明了如何使用树安全来限制对报表的访问。</span><span class="sxs-lookup"><span data-stu-id="a296d-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="a296d-107">USMF 演示公司有一个资产负债报表，并非所有财务报告用户都应具有对该报表的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a296d-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="a296d-108">要限制访问，可以使用树安全来限制对单个报表的访问，以便只有某些用户可以访问该报表。</span><span class="sxs-lookup"><span data-stu-id="a296d-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="a296d-109">请按照以下步骤操作以限制访问：</span><span class="sxs-lookup"><span data-stu-id="a296d-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="a296d-110">登录到 Financial Reporter Report Designer。</span><span class="sxs-lookup"><span data-stu-id="a296d-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="a296d-111">创建一个新的树定义。</span><span class="sxs-lookup"><span data-stu-id="a296d-111">Create a new tree definition.</span></span> <span data-ttu-id="a296d-112">转到 **文件 > 新建 > 树定义**。</span><span class="sxs-lookup"><span data-stu-id="a296d-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="a296d-113">双击 **单位安全性** 列中的 **摘要** 行。</span><span class="sxs-lookup"><span data-stu-id="a296d-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="a296d-114">选择 **用户和组**。</span><span class="sxs-lookup"><span data-stu-id="a296d-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="a296d-115">选择需要访问此报表的用户或组。</span><span class="sxs-lookup"><span data-stu-id="a296d-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="a296d-116">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a296d-116">Select **Save**.</span></span>
7. <span data-ttu-id="a296d-117">在报表定义中，添加您的新树定义。</span><span class="sxs-lookup"><span data-stu-id="a296d-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="a296d-118">在树定义中，选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="a296d-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="a296d-119">在 **报告单位选择** 下，选择 **包括所有单位**。</span><span class="sxs-lookup"><span data-stu-id="a296d-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="a296d-120">如何确定哪些帐户与我的余额不匹配？</span><span class="sxs-lookup"><span data-stu-id="a296d-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="a296d-121">如果您的报表没有匹配的余额，则可以采取以下步骤来确定每一个帐户及差异。</span><span class="sxs-lookup"><span data-stu-id="a296d-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="a296d-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="a296d-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="a296d-123">在 Financial Reporter Report Designer 中，创建一个新的行定义。</span><span class="sxs-lookup"><span data-stu-id="a296d-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="a296d-124">选择 **编辑 > 插入维度中的行**。</span><span class="sxs-lookup"><span data-stu-id="a296d-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="a296d-125">选择 **主帐户**。</span><span class="sxs-lookup"><span data-stu-id="a296d-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="a296d-126">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a296d-126">Select **OK**.</span></span>
5. <span data-ttu-id="a296d-127">保存行定义。</span><span class="sxs-lookup"><span data-stu-id="a296d-127">Save the row definition.</span></span>
6. <span data-ttu-id="a296d-128">创建一个新的列定义</span><span class="sxs-lookup"><span data-stu-id="a296d-128">Create a new column definition</span></span>
7. <span data-ttu-id="a296d-129">创建一个新的报表定义。</span><span class="sxs-lookup"><span data-stu-id="a296d-129">Create a new report definition.</span></span>
8. <span data-ttu-id="a296d-130">选择 **设置** 并取消标记此选项。</span><span class="sxs-lookup"><span data-stu-id="a296d-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="a296d-131">生成报表。</span><span class="sxs-lookup"><span data-stu-id="a296d-131">Generate the report.</span></span> 
10. <span data-ttu-id="a296d-132">将报表导出到 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="a296d-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="a296d-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="a296d-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="a296d-134">在 Dynamics 365 Finance 中，转到 **总帐 > 查询和报表 > 试算平衡表**。</span><span class="sxs-lookup"><span data-stu-id="a296d-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="a296d-135">设置以下参数：</span><span class="sxs-lookup"><span data-stu-id="a296d-135">Set the following parameters:</span></span>
   - <span data-ttu-id="a296d-136">**开始日期** - 输入会计年度的开始日期。</span><span class="sxs-lookup"><span data-stu-id="a296d-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="a296d-137">**结束日期** - 输入报表的生成日期。</span><span class="sxs-lookup"><span data-stu-id="a296d-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="a296d-138">**财务维度** - 将此字段设置为 **主帐户集**。</span><span class="sxs-lookup"><span data-stu-id="a296d-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="a296d-139">选择 **计算**。</span><span class="sxs-lookup"><span data-stu-id="a296d-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="a296d-140">将报表导出到 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="a296d-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="a296d-141">您现在应该能够将 Financial Reporter Excel 报表中的数据复制到试算平衡表报表，因此可以比较 **期末余额** 列。</span><span class="sxs-lookup"><span data-stu-id="a296d-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]