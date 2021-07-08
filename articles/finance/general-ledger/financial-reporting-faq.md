---
title: 财务报告常见问题解答
description: 本主题提供有关财务报告的一些常见问题的解答。
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266625"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="3d3fb-103">财务报告常见问题解答</span><span class="sxs-lookup"><span data-stu-id="3d3fb-103">Financial reporting FAQ</span></span>

<span data-ttu-id="3d3fb-104">本主题提供有关财务报告的常见问题的解答。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="3d3fb-105">如何使用树安全限制对报表的访问？</span><span class="sxs-lookup"><span data-stu-id="3d3fb-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="3d3fb-106">以下示例说明了如何使用树安全来限制对报表的访问。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="3d3fb-107">USMF 演示公司有一个 **资产负债表** 报表，并非所有财务报告用户都应具有对该报表的访问权限。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="3d3fb-108">您可以使用树安全来限制对单个报表的访问，以便只有特定用户可以访问该报表。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="3d3fb-109">登录到 Financial Reporter Report Designer。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="3d3fb-110">选择 **文件 \> 新建 \> 树定义** 以创建一个新的树定义。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="3d3fb-111">两次点击（或双击）**单位安全性** 列中的 **摘要** 行。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="3d3fb-112">选择 **用户和组**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="3d3fb-113">选择需要访问此报表的用户或组。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="3d3fb-114">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-114">Select **Save**.</span></span>
7. <span data-ttu-id="3d3fb-115">在报表定义中，添加您的新树定义。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="3d3fb-116">在树定义中，选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="3d3fb-117">然后，在 **报告单位选择** 下，选择 **包括所有单位**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="3d3fb-118">如何确定哪些帐户与我的余额不匹配？</span><span class="sxs-lookup"><span data-stu-id="3d3fb-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="3d3fb-119">如果您的报表没有匹配的余额，可以按照以下过程来确定每一个帐户及差异。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="3d3fb-120">在 Financial Reporter Report Designer 中</span><span class="sxs-lookup"><span data-stu-id="3d3fb-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="3d3fb-121">创建一个新的行定义。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-121">Create a new row definition.</span></span>
2. <span data-ttu-id="3d3fb-122">选择 **编辑 \> 插入维度中的行**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="3d3fb-123">选择 **MainAccount**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="3d3fb-124">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-124">Select **OK**.</span></span>
5. <span data-ttu-id="3d3fb-125">保存行定义。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-125">Save the row definition.</span></span>
6. <span data-ttu-id="3d3fb-126">创建一个新的列定义。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-126">Create a new column definition.</span></span>
7. <span data-ttu-id="3d3fb-127">创建一个新的报表定义。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-127">Create a new report definition.</span></span>
8. <span data-ttu-id="3d3fb-128">选择 **设置** 并取消标记此选项。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="3d3fb-129">生成报表。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-129">Generate the report.</span></span> 
10. <span data-ttu-id="3d3fb-130">将报表导出到 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="3d3fb-131">在 Dynamics 365 Finance 中</span><span class="sxs-lookup"><span data-stu-id="3d3fb-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="3d3fb-132">转到 **总帐 \> 查询和报表 \> 试算平衡表**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="3d3fb-133">设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="3d3fb-133">Set the following fields:</span></span>

    - <span data-ttu-id="3d3fb-134">**开始日期** - 输入会计年度的开始日期。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="3d3fb-135">**结束日期** - 输入报表的生成日期。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="3d3fb-136">**财务维度** - 将此字段设置为 **主科目集**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="3d3fb-137">选择 **计算**。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="3d3fb-138">将报表导出到 Excel。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-138">Export the report to Excel.</span></span>

<span data-ttu-id="3d3fb-139">您现在应该能够将 Financial Reporter Excel 报表中的数据复制到 **试算平衡表** 报表，以便可以比较 **期末余额** 列。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="3d3fb-140">当我在 Report Designer 中设计报表或生成财务报表时，收到以下消息：“由于数据提供程序框架出现问题，无法完成此操作。”</span><span class="sxs-lookup"><span data-stu-id="3d3fb-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="3d3fb-141">我应如何处理？</span><span class="sxs-lookup"><span data-stu-id="3d3fb-141">How should I respond?</span></span>

<span data-ttu-id="3d3fb-142">该消息指示在您使用财务报告时，系统尝试从数据市场中检索财务元数据时出现问题。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="3d3fb-143">处理此问题有两种方法：</span><span class="sxs-lookup"><span data-stu-id="3d3fb-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="3d3fb-144">通过转到 Report Designer 中的 **工具 \> 集成状态**，查看数据的集成状态。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="3d3fb-145">如果集成未完成，请等待它完成。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="3d3fb-146">然后，在收到消息时重试所执行的操作。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="3d3fb-147">联系支持人员以确定并解决问题。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="3d3fb-148">系统中可能存在不一致的数据。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="3d3fb-149">支持工程师可以帮助您确定服务器上的问题，并找到可能需要更新的特定数据。</span><span class="sxs-lookup"><span data-stu-id="3d3fb-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
