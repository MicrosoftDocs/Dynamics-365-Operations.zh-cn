---
title: "重置财务报告数据市场"
description: "此主题描述如何重置财务报告数据市场。"
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: zh-cn
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="0f93b-103">重置财务报告数据市场</span><span class="sxs-lookup"><span data-stu-id="0f93b-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0f93b-104">本主题说明如何重置以下版本的财务报告数据市场：</span><span class="sxs-lookup"><span data-stu-id="0f93b-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="0f93b-105">Microsoft Dynamics 365 for Finance and Operations 财务报告版本 7.2.6.0 及更高版本</span><span class="sxs-lookup"><span data-stu-id="0f93b-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="0f93b-106">Microsoft Dynamics 365 for Finance and Operations 财务报告版本 7.0.10000.4 及更高版本</span><span class="sxs-lookup"><span data-stu-id="0f93b-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="0f93b-107">Microsoft Dynamics 365 for Finance and Operations Enterprise edition（本地）</span><span class="sxs-lookup"><span data-stu-id="0f93b-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="0f93b-108">若要获取 Finance and Operations 财务报告版本 7.2.6.0，您可以从 <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514> 下载 KB 4052514。</span><span class="sxs-lookup"><span data-stu-id="0f93b-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="0f93b-109">重置 Finance and Operations 财务报告版本 7.2.6.0 及更高版本的财务报告数据市场</span><span class="sxs-lookup"><span data-stu-id="0f93b-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="0f93b-110">从报表设计器重置财务报告数据市场</span><span class="sxs-lookup"><span data-stu-id="0f93b-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="0f93b-111">此流程中的步骤为 Finance and Operations 财务报告版本 7.2.6.0 及更高版本提供支持。</span><span class="sxs-lookup"><span data-stu-id="0f93b-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="0f93b-112">如果您有较早的版本，请与支持团队联系获取帮助。</span><span class="sxs-lookup"><span data-stu-id="0f93b-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="0f93b-113">在特定情况下，您可能必须重置财务报告的数据市场。</span><span class="sxs-lookup"><span data-stu-id="0f93b-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="0f93b-114">您可以在报表设计器客户端完成此任务。</span><span class="sxs-lookup"><span data-stu-id="0f93b-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="0f93b-115">以下是一些您可能必须重置数据市场的情况：</span><span class="sxs-lookup"><span data-stu-id="0f93b-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="0f93b-116">Finance and Operations 数据库已还原，但数据市场数据库未还原。</span><span class="sxs-lookup"><span data-stu-id="0f93b-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="0f93b-117">您看到某个期间内有不正确的数据。</span><span class="sxs-lookup"><span data-stu-id="0f93b-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="0f93b-118">支持人员在故障排除步骤中指导您重置数据市场。</span><span class="sxs-lookup"><span data-stu-id="0f93b-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="0f93b-119">数据市场重置应仅在数据库的处理量较小时进行。</span><span class="sxs-lookup"><span data-stu-id="0f93b-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="0f93b-120">财务报告在重置流程中将不可用。</span><span class="sxs-lookup"><span data-stu-id="0f93b-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="0f93b-121">重置数据市场</span><span class="sxs-lookup"><span data-stu-id="0f93b-121">Reset the data mart</span></span>

<span data-ttu-id="0f93b-122">要重置数据市场，在报表设计器中，在**工具**菜单中，选择**重置数据市场**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="0f93b-123">出现的对话框具有两部分：**统计**和**重置**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="0f93b-124">[![“重置数据市场”对话框](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="0f93b-124">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="0f93b-125">集成尝试次数</span><span class="sxs-lookup"><span data-stu-id="0f93b-125">Integration attempts</span></span>

<span data-ttu-id="0f93b-126">**集成尝试次数**网格显示系统尝试集成交易的次数。</span><span class="sxs-lookup"><span data-stu-id="0f93b-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="0f93b-127">如果最开始的少数尝试不成功，系统将继续尝试在几天中集成数据。</span><span class="sxs-lookup"><span data-stu-id="0f93b-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="0f93b-128">如果尝试次数为 8 或更多，以及存在许多维度组合或交易记录，那么您就知道必须重置数据市场了。</span><span class="sxs-lookup"><span data-stu-id="0f93b-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="0f93b-129">在此情况下，数据将不报告。</span><span class="sxs-lookup"><span data-stu-id="0f93b-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="0f93b-130">数据状态</span><span class="sxs-lookup"><span data-stu-id="0f93b-130">Data status</span></span>

<span data-ttu-id="0f93b-131">**数据状态**网格在数据市场中提供交易、汇率和维度值的快照。</span><span class="sxs-lookup"><span data-stu-id="0f93b-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="0f93b-132">大量的过时记录指示记录已发生了许多更新。</span><span class="sxs-lookup"><span data-stu-id="0f93b-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="0f93b-133">此情况可能导致更长的报告生成时间。</span><span class="sxs-lookup"><span data-stu-id="0f93b-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="0f93b-134">未对齐的主科目类别</span><span class="sxs-lookup"><span data-stu-id="0f93b-134">Misaligned main account categories</span></span>

<span data-ttu-id="0f93b-135">如果您在使用 Microsoft Dynamics 365 for Finance and Operations 财务报告版本 7.2.1 以前的一个版本，且如果重命名科目并将科目在科目类别之间移动，您可能必须重置数据市场。</span><span class="sxs-lookup"><span data-stu-id="0f93b-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="0f93b-136">这些操作可能导致主科目类别不对齐。</span><span class="sxs-lookup"><span data-stu-id="0f93b-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="0f93b-137">**未对齐的主科目类别**字段显示您是否遇到此问题。</span><span class="sxs-lookup"><span data-stu-id="0f93b-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="0f93b-138">重置 Finance and Operations 财务报告版本 7.2.6.0 的数据市场</span><span class="sxs-lookup"><span data-stu-id="0f93b-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="0f93b-139">要重置 Finance and Operations 财务报告 7.2.6.0 及以前版本的数据市场，在**重置市场数据**对话框中，选择**重置数据市场**复选框，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="0f93b-140">您应该只在计划停机期间重置数据市场。</span><span class="sxs-lookup"><span data-stu-id="0f93b-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="0f93b-141">[![“重置数据市场”复选框](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="0f93b-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="0f93b-142">在 Microsoft Dynamics 365 for Finance and Operations 财务报告版本 7.3.0 中重置数据市场并选择原因</span><span class="sxs-lookup"><span data-stu-id="0f93b-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="0f93b-143">如果您确定需要重置数据市场，则选择**重置数据市场**复选框，然后在**原因**字段中选择一个原因。</span><span class="sxs-lookup"><span data-stu-id="0f93b-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="0f93b-144">以下是可用的选项：</span><span class="sxs-lookup"><span data-stu-id="0f93b-144">The following options are available:</span></span>

- <span data-ttu-id="0f93b-145">**缺少数据或数据错误** – 根据统计，您确定可能缺少该数据。</span><span class="sxs-lookup"><span data-stu-id="0f93b-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="0f93b-146">在继续之前，我们建议您联系支持人员确定根本原因。</span><span class="sxs-lookup"><span data-stu-id="0f93b-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="0f93b-147">**还原数据库** – Finance and Operations 数据库已还原，但财务报告数据市场的数据库未还原。</span><span class="sxs-lookup"><span data-stu-id="0f93b-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="0f93b-148">**其他** – 您出于其他原因重置数据市场。</span><span class="sxs-lookup"><span data-stu-id="0f93b-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="0f93b-149">如果您担心存在问题，请联系支持人员加以确定。</span><span class="sxs-lookup"><span data-stu-id="0f93b-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="0f93b-150">[![重置数据市场](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="0f93b-150">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="0f93b-151">在开始重置前，验证所有数据市场重置任务已完成初始加载。</span><span class="sxs-lookup"><span data-stu-id="0f93b-151">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="0f93b-152">您可以通过选择**工具** &gt; **集成状态**查找上一次运行时列中的值的方式进行确认。</span><span class="sxs-lookup"><span data-stu-id="0f93b-152">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="0f93b-153">清除用户和公司</span><span class="sxs-lookup"><span data-stu-id="0f93b-153">Clear users and companies</span></span>

<span data-ttu-id="0f93b-154">如果您还原了您的数据库，不过随后对用户或公司进行了更改，则选择**清除用户和公司**复选框。</span><span class="sxs-lookup"><span data-stu-id="0f93b-154">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="0f93b-155">您几乎不必选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="0f93b-155">You should rarely have to select this check box.</span></span>

<span data-ttu-id="0f93b-156">当您准备好开始重置流程时，请选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-156">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="0f93b-157">系统将提示您确认已准备好开始流程。</span><span class="sxs-lookup"><span data-stu-id="0f93b-157">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="0f93b-158">请注意，在重置和之后发生的初始数据集成期间财务报告将不可用。</span><span class="sxs-lookup"><span data-stu-id="0f93b-158">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="0f93b-159">如果要查看集成的状态，请选择**工具** &gt; **集成状态**以查看集成运行的上次时间和状态。</span><span class="sxs-lookup"><span data-stu-id="0f93b-159">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="0f93b-160">[![查看集成的状态](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="0f93b-160">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="0f93b-161">当所有映射显示 RanToCompletion 状态且集成状态窗口的左下角显示“集成完成”时，重置完成。</span><span class="sxs-lookup"><span data-stu-id="0f93b-161">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says “Integration complete” in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="0f93b-162">重置 Finance and Operations 财务报告版本 7.0.10000.4 及更高版本的财务报告数据市场</span><span class="sxs-lookup"><span data-stu-id="0f93b-162">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="0f93b-163">如果您从备份还原 Finance and Operations 数据库或从其他环境复制该数据库，则必须执行本部分中的步骤，以帮助确保财务报告数据市场正确使用还原的 Finance and Operations 数据库。</span><span class="sxs-lookup"><span data-stu-id="0f93b-163">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="0f93b-164">此流程中的步骤支持 Microsoft Dynamics AX 应用程序版本 7.0.1（2016 年 5 月）（应用程序版本 7.0.1265.23014 和财务报告版本 7.0.10000.4）及更高版本。</span><span class="sxs-lookup"><span data-stu-id="0f93b-164">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="0f93b-165">如果您的 Finance and Operations 版本较低，请联系支持团队获取协助。</span><span class="sxs-lookup"><span data-stu-id="0f93b-165">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="0f93b-166">导出报表定义</span><span class="sxs-lookup"><span data-stu-id="0f93b-166">Export report definitions</span></span>

<span data-ttu-id="0f93b-167">首先，按照以下步骤从报表设计器导出报表设计。</span><span class="sxs-lookup"><span data-stu-id="0f93b-167">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="0f93b-168">在报表设计器中，选择**公司** &gt; **构建基块组**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-168">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="0f93b-169">选择要导出的构建基块组，然后选择**导出**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-169">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f93b-170">对于 Finance and Operations，仅支持一个构建块组，即**默认**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-170">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="0f93b-171">选择要导出的报表定义：</span><span class="sxs-lookup"><span data-stu-id="0f93b-171">Select the report definitions to export:</span></span>

    - <span data-ttu-id="0f93b-172">若要导出所有报表定义和关联的构建基块，请选择**全选**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-172">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="0f93b-173">要导出特定报表、行、列、树或维度集，请选择相应选项卡，然后选择要导出的项。</span><span class="sxs-lookup"><span data-stu-id="0f93b-173">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="0f93b-174">按住 Ctrl 键选择选项卡上的多个项目。当您选择要导出的报表时，系统将选择关联的行、列、树和维度集。</span><span class="sxs-lookup"><span data-stu-id="0f93b-174">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="0f93b-175">选择**导出**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-175">Select **Export**.</span></span>
5. <span data-ttu-id="0f93b-176">输入文件名，然后选择要用于保存所导出报表定义的安全位置。</span><span class="sxs-lookup"><span data-stu-id="0f93b-176">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="0f93b-177">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-177">Select **Save**.</span></span>

<span data-ttu-id="0f93b-178">您可以将该文件复制或上传到安全位置。</span><span class="sxs-lookup"><span data-stu-id="0f93b-178">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="0f93b-179">通过此方法，文件以后可以导入到不同的环境。</span><span class="sxs-lookup"><span data-stu-id="0f93b-179">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="0f93b-180">有关如何使用 Microsoft Azure 存储帐户的信息，请参见[使用 AzCopy 命令行实用程序传输数据](/azure/storage/storage-use-azcopy)。</span><span class="sxs-lookup"><span data-stu-id="0f93b-180">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="0f93b-181">根据您的 Finance and Operations 协议，Microsoft 不提供存储帐户。</span><span class="sxs-lookup"><span data-stu-id="0f93b-181">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="0f93b-182">您必须购买存储帐户，或使用单独 Azure 订阅的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="0f93b-182">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="0f93b-183">请注意 Azure 虚拟机 (VM) D 盘的行为。</span><span class="sxs-lookup"><span data-stu-id="0f93b-183">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="0f93b-184">请勿在 D 盘上永久储存导出的构建基块组。有关临时驱动器的详细信息，请参阅[了解 Windows Azure 虚拟机上的临时驱动器](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)。</span><span class="sxs-lookup"><span data-stu-id="0f93b-184">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="0f93b-185">停止服务</span><span class="sxs-lookup"><span data-stu-id="0f93b-185">Stop services</span></span>

<span data-ttu-id="0f93b-186">以下 Microsoft Windows 服务具有到 Finance and Operations 数据库的开放连接。</span><span class="sxs-lookup"><span data-stu-id="0f93b-186">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="0f93b-187">因此，您必须使用 Microsoft 远程桌面连接到环境中的所有计算机，然后使用 services.msc 停止这些服务。</span><span class="sxs-lookup"><span data-stu-id="0f93b-187">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="0f93b-188">万维网 Web 发布服务（在所有应用程序对象服务器 [AOS] 计算机上）</span><span class="sxs-lookup"><span data-stu-id="0f93b-188">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="0f93b-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service（仅限非私有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="0f93b-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="0f93b-190">Management Reporter 2012 Process Service（仅限于商业智能 [BI] 计算机上）</span><span class="sxs-lookup"><span data-stu-id="0f93b-190">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="0f93b-191">重置</span><span class="sxs-lookup"><span data-stu-id="0f93b-191">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="0f93b-192">下载最新的 MinorVersionDataUpgrade.zip 程序包</span><span class="sxs-lookup"><span data-stu-id="0f93b-192">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="0f93b-193">下载最新的 MinorVersionDataUpgrade.zip 程序包。</span><span class="sxs-lookup"><span data-stu-id="0f93b-193">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="0f93b-194">有关如何查找并下载数据升级包的正确版本的说明，请参阅[下载最新的数据升级可部署程序包](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package)。</span><span class="sxs-lookup"><span data-stu-id="0f93b-194">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> 

<span data-ttu-id="0f93b-195">无需下载 MinorVersionDataUpgrade.zip 程序包即可升级。</span><span class="sxs-lookup"><span data-stu-id="0f93b-195">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="0f93b-196">因此，您只需执行该主题的“下载最新的数据升级可部署程序包”部分中的步骤。</span><span class="sxs-lookup"><span data-stu-id="0f93b-196">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="0f93b-197">您可以跳过主题中的所有其他步骤。</span><span class="sxs-lookup"><span data-stu-id="0f93b-197">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="0f93b-198">对 Finance and Operations 数据库运行脚本</span><span class="sxs-lookup"><span data-stu-id="0f93b-198">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="0f93b-199">对 Finance and Operations 数据库（而非对财务报告数据库）运行以下脚本：</span><span class="sxs-lookup"><span data-stu-id="0f93b-199">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="0f93b-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="0f93b-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="0f93b-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="0f93b-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="0f93b-202">这些脚本帮助确保用户、角色和更改跟踪设置正确无误。</span><span class="sxs-lookup"><span data-stu-id="0f93b-202">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="0f93b-203">运行 Windows PowerShell 命令来重置数据库</span><span class="sxs-lookup"><span data-stu-id="0f93b-203">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="0f93b-204">在 AOS 计算机上，作为管理员启动 Microsoft Windows PowerShell 并运行以下命令以重置 Finance and Operations 与财务报告之间的集成。</span><span class="sxs-lookup"><span data-stu-id="0f93b-204">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="0f93b-205">以下是 **Reset-DatamartIntegration** 命令中参数的说明：</span><span class="sxs-lookup"><span data-stu-id="0f93b-205">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="0f93b-206">**-Reason** 的有效值为 **SERVICING**、**BADDATA** 和 **OTHER**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-206">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="0f93b-207">**-ReasonDetail** 参数为自由文本。</span><span class="sxs-lookup"><span data-stu-id="0f93b-207">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="0f93b-208">原因和原因详细信息将记录到 telemetry/environment monitoring 中。</span><span class="sxs-lookup"><span data-stu-id="0f93b-208">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="0f93b-209">在运行命令后，系统将要求您输入 **Y** 来确认您要重置数据库。</span><span class="sxs-lookup"><span data-stu-id="0f93b-209">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="0f93b-210">重新启动服务</span><span class="sxs-lookup"><span data-stu-id="0f93b-210">Restart services</span></span>

<span data-ttu-id="0f93b-211">使用 services.msc 重新启动您前面停止的服务：</span><span class="sxs-lookup"><span data-stu-id="0f93b-211">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="0f93b-212">万维网 Web 发布服务（在所有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="0f93b-212">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="0f93b-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service（仅限非私有 AOS 计算机上）</span><span class="sxs-lookup"><span data-stu-id="0f93b-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="0f93b-214">Management Reporter 2012 Process Service（仅限于 BI 计算机上）</span><span class="sxs-lookup"><span data-stu-id="0f93b-214">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="0f93b-215">导入报表定义</span><span class="sxs-lookup"><span data-stu-id="0f93b-215">Import report definitions</span></span>

<span data-ttu-id="0f93b-216">使用导出期间创建的文件从报表设计器导入您的报表设计。</span><span class="sxs-lookup"><span data-stu-id="0f93b-216">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="0f93b-217">在报表设计器中，选择**公司** &gt; **构建基块组**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-217">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="0f93b-218">选择要导出的构建基块组，然后选择**导出**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-218">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f93b-219">对于 Finance and Operations，仅支持一个构建块组，即**默认**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-219">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="0f93b-220">选择**默认**构建块，然后选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-220">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="0f93b-221">选择包含所导出报表定义的文件，然后选择**打开**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-221">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="0f93b-222">在**导入**对话框中，选择要导入的报表定义：</span><span class="sxs-lookup"><span data-stu-id="0f93b-222">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="0f93b-223">若要导入所有报表定义和关联的构建基块，请选择**全选**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-223">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="0f93b-224">若要导入特定报表、行、列、树或维度集，请选择要导入的报表、行、列、树或维度集。</span><span class="sxs-lookup"><span data-stu-id="0f93b-224">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="0f93b-225">选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-225">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="0f93b-226">重置 Finance and Operations（本地）的财务报告数据市场</span><span class="sxs-lookup"><span data-stu-id="0f93b-226">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="0f93b-227">指导所有用户退出报表设计器和 Finance and Operations 的财务报告区域。</span><span class="sxs-lookup"><span data-stu-id="0f93b-227">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="0f93b-228">对财务报告数据库 (MRDB) 运行以下脚本。</span><span class="sxs-lookup"><span data-stu-id="0f93b-228">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="0f93b-229">从 Finance and Operations 数据库 (AXDB) 的 FINANCIALREPORTS 表中截断或删除所有记录。</span><span class="sxs-lookup"><span data-stu-id="0f93b-229">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="0f93b-230">如果 FINANCIALREPORTVERSION 表在 Finance and Operations 数据库中存在，则从此表中截断或删除所有记录。</span><span class="sxs-lookup"><span data-stu-id="0f93b-230">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="0f93b-231">如果此表不存在于 Finance and Operations 数据库中，则跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="0f93b-231">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="0f93b-232">对财务报告数据库运行 **ResetDatamart.sql** 脚本。</span><span class="sxs-lookup"><span data-stu-id="0f93b-232">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="0f93b-233">此脚本禁用数据市场集成，删除所有数据市场数据，然后重新启用数据市场集成。</span><span class="sxs-lookup"><span data-stu-id="0f93b-233">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="0f93b-234">重置后，可以通过对财务报告数据库运行以下查询来手动验证数据重新加载。</span><span class="sxs-lookup"><span data-stu-id="0f93b-234">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="0f93b-235">确认所有行均有 **LastRunTime** 值，且 **StateType** 被设置为 **5**。</span><span class="sxs-lookup"><span data-stu-id="0f93b-235">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="0f93b-236">**StateType** 值 **5** 表示数据已成功重载。</span><span class="sxs-lookup"><span data-stu-id="0f93b-236">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="0f93b-237">值 **7** 指示错误状态。</span><span class="sxs-lookup"><span data-stu-id="0f93b-237">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="0f93b-238">有时，组织层次结构映射在首次运行时具有此状态。</span><span class="sxs-lookup"><span data-stu-id="0f93b-238">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="0f93b-239">不过，错误状态应会自动解决。</span><span class="sxs-lookup"><span data-stu-id="0f93b-239">However, the faulted state but should be automatically resolved.</span></span>

