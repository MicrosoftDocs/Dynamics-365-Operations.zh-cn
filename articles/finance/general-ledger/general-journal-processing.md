---
title: 普通日记帐处理
description: 本主题介绍 Microsoft Dynamics 365 Finance 中可以帮助使日记帐处理更加轻松以及帮助确保获取正确数据且不影响内部控制的功能。
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2becf8213cfa46e2c0cf0c553f0b5e503dfc3704
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570232"
---
# <a name="general-journal-processing"></a><span data-ttu-id="4aa37-103">普通日记帐处理</span><span class="sxs-lookup"><span data-stu-id="4aa37-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4aa37-104">本主题介绍可以帮助使日记帐处理更加轻松以及帮助确保获取正确数据且不影响内部控制的功能。</span><span class="sxs-lookup"><span data-stu-id="4aa37-104">This topic describes capabilities that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="4aa37-105">日记帐名称</span><span class="sxs-lookup"><span data-stu-id="4aa37-105">Journal names</span></span>

<span data-ttu-id="4aa37-106">要设置的最重要的区域之一是日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="4aa37-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="4aa37-107">最好为每个用途定义特定的日记帐名称，如内部公司、应计调整和错误纠正。</span><span class="sxs-lookup"><span data-stu-id="4aa37-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="4aa37-108">您可以定制每个日记帐名称以便让每个用途的数据输入都简单且安全。</span><span class="sxs-lookup"><span data-stu-id="4aa37-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="4aa37-109">在**日记帐名称**页上，您可以设置以下因素：</span><span class="sxs-lookup"><span data-stu-id="4aa37-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="4aa37-110">**工作流审核** - 要增强内部控制，请基于总借方金额等条件定义日记帐工作流（用于确定审查和审核步骤的重要性限制）。</span><span class="sxs-lookup"><span data-stu-id="4aa37-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="4aa37-111">您在**总帐工作流**页上为普通日记帐设置工作流。</span><span class="sxs-lookup"><span data-stu-id="4aa37-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="4aa37-112">**默认值** - 为对方科目、币种和财务维度选择的默认值。</span><span class="sxs-lookup"><span data-stu-id="4aa37-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="4aa37-113">**日记帐控制** - 您可以设置对公司和科目类型的限制以及对科目段值的限制。</span><span class="sxs-lookup"><span data-stu-id="4aa37-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="4aa37-114">**示例**</span><span class="sxs-lookup"><span data-stu-id="4aa37-114">**Examples**</span></span>

<span data-ttu-id="4aa37-115">日记帐名称只能用于调整。</span><span class="sxs-lookup"><span data-stu-id="4aa37-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="4aa37-116">在这种情况下，您可以指定只有**分类帐**科目类型在所有公司都有效。</span><span class="sxs-lookup"><span data-stu-id="4aa37-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="4aa37-117">[![日记帐控制科目类型](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="4aa37-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="4aa37-118">日记帐名称只能用于某个特定科目段或用于主科目的某个范围。</span><span class="sxs-lookup"><span data-stu-id="4aa37-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="4aa37-119">[![日记帐控制科目段](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="4aa37-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="4aa37-120">**自动冲销**选项可用于普通日记帐。</span><span class="sxs-lookup"><span data-stu-id="4aa37-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="4aa37-121">例如，您有一个应计调整，其中的实际单据尚未处理，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="4aa37-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="4aa37-122">[![普通日记帐冲销](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="4aa37-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="4aa37-123">用于日记帐条目的 Microsoft Excel 加载项进一步提高了自动化水平并使数据输入更容易。</span><span class="sxs-lookup"><span data-stu-id="4aa37-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="4aa37-124">**在 Excel 中打开行**操作可用于**普通日记帐**和**日记帐凭证**页。</span><span class="sxs-lookup"><span data-stu-id="4aa37-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="4aa37-125">在**期间日记帐**页上，您可以设置重复日记帐以自动执行日记帐处理。</span><span class="sxs-lookup"><span data-stu-id="4aa37-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="4aa37-126">您可以随时使用凭证模板。</span><span class="sxs-lookup"><span data-stu-id="4aa37-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="4aa37-127">在**普通日记帐**页上，**保存**和**选择凭证模板**操作可在**日志凭证**页上找到（位于凭证行的**功能**下）。</span><span class="sxs-lookup"><span data-stu-id="4aa37-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="4aa37-128">相关设置</span><span class="sxs-lookup"><span data-stu-id="4aa37-128">Related setup</span></span>
<span data-ttu-id="4aa37-129">以下设置不是特定于普通日记帐的，但有助于确保数据输入正确且容易。</span><span class="sxs-lookup"><span data-stu-id="4aa37-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="4aa37-130">主科目</span><span class="sxs-lookup"><span data-stu-id="4aa37-130">Main account</span></span>

<span data-ttu-id="4aa37-131">主科目设置为普通日记帐处理提供了很多选项：</span><span class="sxs-lookup"><span data-stu-id="4aa37-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="4aa37-132">**DC/CR 需求** - 如果主科目被限制到借方或贷方交易记录，则使用此选项。</span><span class="sxs-lookup"><span data-stu-id="4aa37-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="4aa37-133">该设置在验证或过帐日记帐时验证。</span><span class="sxs-lookup"><span data-stu-id="4aa37-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="4aa37-134">**默认对方科目**</span><span class="sxs-lookup"><span data-stu-id="4aa37-134">**Default offset account**</span></span>
-   <span data-ttu-id="4aa37-135">**暂停** - 在所有公司或为特定公司/法人暂停数据输入的主科目。</span><span class="sxs-lookup"><span data-stu-id="4aa37-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="4aa37-136">**不允许手动输入** - 防止用户为日记帐中的科目手动输入值。</span><span class="sxs-lookup"><span data-stu-id="4aa37-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="4aa37-137">**默认/验证币种**</span><span class="sxs-lookup"><span data-stu-id="4aa37-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="4aa37-138">**法人覆盖** - 此设置特定于已定义的公司/法人：</span><span class="sxs-lookup"><span data-stu-id="4aa37-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="4aa37-139">**默认/验证销售税**</span><span class="sxs-lookup"><span data-stu-id="4aa37-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="4aa37-140">**默认维度** - **不固定**或**固定值**。</span><span class="sxs-lookup"><span data-stu-id="4aa37-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="4aa37-141">**固定值**将帮助确保此主科目的所有过帐始终使用设置为**固定**的任何维度值。</span><span class="sxs-lookup"><span data-stu-id="4aa37-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="4aa37-142">**过帐验证**</span><span class="sxs-lookup"><span data-stu-id="4aa37-142">**Posting validation**</span></span>
    -   <span data-ttu-id="4aa37-143">**用户验证** - 此选项控制允许哪些用户过帐到主科目。</span><span class="sxs-lookup"><span data-stu-id="4aa37-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="4aa37-144">**过帐类型验证** - 此选项控制可对主科目使用的过帐类型。</span><span class="sxs-lookup"><span data-stu-id="4aa37-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="4aa37-145">科目结构和高级规则结构</span><span class="sxs-lookup"><span data-stu-id="4aa37-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="4aa37-146">科目结构和高级规则结构对于确保在一般日记帐处理和任何单据化期间捕获财务报告所需的数据以及绩效跟踪极其重要。</span><span class="sxs-lookup"><span data-stu-id="4aa37-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="4aa37-147">科目结构和高级规则结构可让您定制数据输入体验。</span><span class="sxs-lookup"><span data-stu-id="4aa37-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="4aa37-148">您可以仅对在所有情况下都相关的财务维度允许数据输入，还可以实施始终捕获正确数据这一必须实施的要求。</span><span class="sxs-lookup"><span data-stu-id="4aa37-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="4aa37-149">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="4aa37-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="4aa37-150">[计划：会计科目表](plan-chart-of-accounts.md)。</span><span class="sxs-lookup"><span data-stu-id="4aa37-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="4aa37-151">创建日记帐高级规则</span><span class="sxs-lookup"><span data-stu-id="4aa37-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="4aa37-152">使用模板创建日记帐条目</span><span class="sxs-lookup"><span data-stu-id="4aa37-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="4aa37-153">创建和验证日记帐</span><span class="sxs-lookup"><span data-stu-id="4aa37-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="4aa37-154">过帐期间日记帐</span><span class="sxs-lookup"><span data-stu-id="4aa37-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="4aa37-155">处理分类帐分配日记帐</span><span class="sxs-lookup"><span data-stu-id="4aa37-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="4aa37-156">模拟过帐</span><span class="sxs-lookup"><span data-stu-id="4aa37-156">Simulate posting</span></span>
<span data-ttu-id="4aa37-157">可在**验证**菜单上查找**模拟过帐**以获得更多日记帐。</span><span class="sxs-lookup"><span data-stu-id="4aa37-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="4aa37-158">使用**验证**功能验证日记帐时，系统将使用特定错误条件测试该日记帐。</span><span class="sxs-lookup"><span data-stu-id="4aa37-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="4aa37-159">如果使用**模拟过帐**功能，系统将运行过帐期间运行的全部相同过程，但不真正过帐该日记帐。</span><span class="sxs-lookup"><span data-stu-id="4aa37-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="4aa37-160">然后可以查看显示的过帐消息，修复发现的所有错误，然后打开**过帐**菜单过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="4aa37-160">You can then review the posting messages that are displayed, fix any errors that you find, and then open the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="4aa37-161">**模拟过帐**不可用于批处理。</span><span class="sxs-lookup"><span data-stu-id="4aa37-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="4aa37-162">但是，可通过代码批量模拟过帐，而开发人员可以扩展代码以添加该功能。</span><span class="sxs-lookup"><span data-stu-id="4aa37-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  

## <a name="journal-unlock"></a><span data-ttu-id="4aa37-163">日记帐解锁</span><span class="sxs-lookup"><span data-stu-id="4aa37-163">Journal unlock</span></span>
<span data-ttu-id="4aa37-164">日记帐页面中有一个按钮用于解锁“系统锁定”状态设置为“是”的日记帐。</span><span class="sxs-lookup"><span data-stu-id="4aa37-164">A button is available on the journal page to unlock a journal that has a status of "locked by system" set to Yes.</span></span> <span data-ttu-id="4aa37-165">可以有已分析了正在执行的批处理作业，并且确定批处理作业未在主动处理此日记帐的系统管理员执行此项解锁。</span><span class="sxs-lookup"><span data-stu-id="4aa37-165">This unlock can be performed by an administrator of the system who has analyzed any executing batch jobs and confirmed this journal is no longer actively being processed by a batch job.</span></span> <span data-ttu-id="4aa37-166">此按钮通过**功能管理**页中名称为**日记帐解锁按钮**的功能启用。</span><span class="sxs-lookup"><span data-stu-id="4aa37-166">This button is enabled by the feature named **Journal Unlock button** on the **Feature management** page.</span></span> 

## <a name="workflow-recall"></a><span data-ttu-id="4aa37-167">工作流撤回</span><span class="sxs-lookup"><span data-stu-id="4aa37-167">Workflow recall</span></span> 
<span data-ttu-id="4aa37-168">可使用日记帐和**工作流历史记录**页中的**工作流**按钮启用用于撤回工作流中状态为“无法恢复”的日记帐的功能。</span><span class="sxs-lookup"><span data-stu-id="4aa37-168">The ability to recall a journal in a workflow that has a status of "unrecoverable" is enabled by using the **Workflow** button on a journal, and on the **Workflow history** page.</span></span> <span data-ttu-id="4aa37-169">此功能可通过**功能管理**页中名称为**重置日记帐的工作流状态**的功能启用。</span><span class="sxs-lookup"><span data-stu-id="4aa37-169">This is enabled by the feature named **Resetting the workflow status for journals** on the **Feature management** page.</span></span>

## <a name="delete-journal-lines"></a><span data-ttu-id="4aa37-170">删除日记帐行</span><span class="sxs-lookup"><span data-stu-id="4aa37-170">Delete Journal Lines</span></span>
<span data-ttu-id="4aa37-171">可通过**功能** > **删除日记帐行**中的日记帐启用用于快速删除所有日记帐行的功能。</span><span class="sxs-lookup"><span data-stu-id="4aa37-171">The ability to delete all journal lines quickly is enabled in a journal under **Functions** > **Delete Journal Lines**.</span></span> <span data-ttu-id="4aa37-172">若要启用此功能，请在**功能管理**中选择**删除日记帐性能优化**。</span><span class="sxs-lookup"><span data-stu-id="4aa37-172">To enable this feature, on the **Feature management**, select **Delete journal performance optimizations**.</span></span>
