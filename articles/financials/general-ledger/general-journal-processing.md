---
title: "普通日记帐处理"
description: "本文介绍 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中可以帮助使日记帐处理更加轻松以及帮助确保获取正确数据且不影响内部控制的功能。"
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 76386f7ab8033075f9db4cadc697f3a2a997163e
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="general-journal-processing"></a><span data-ttu-id="49b0e-103">普通日记帐处理</span><span class="sxs-lookup"><span data-stu-id="49b0e-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="49b0e-104">本文介绍 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中可以帮助使日记帐处理更加轻松以及帮助确保获取正确数据且不影响内部控制的功能。</span><span class="sxs-lookup"><span data-stu-id="49b0e-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="49b0e-105">日记帐名称</span><span class="sxs-lookup"><span data-stu-id="49b0e-105">Journal names</span></span>

<span data-ttu-id="49b0e-106">要设置的最重要的区域之一是日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="49b0e-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="49b0e-107">最好为每个用途定义特定的日记帐名称，如内部公司、应计调整和错误纠正。</span><span class="sxs-lookup"><span data-stu-id="49b0e-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="49b0e-108">您可以定制每个日记帐名称以便让每个用途的数据输入都简单且安全。</span><span class="sxs-lookup"><span data-stu-id="49b0e-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="49b0e-109">在**“日记帐名称”**页上，您可以设置以下因素：</span><span class="sxs-lookup"><span data-stu-id="49b0e-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="49b0e-110">**工作流审核** - 要增强内部控制，请基于总借方金额等条件定义日记帐工作流（用于确定审查和审核步骤的重要性限制）。</span><span class="sxs-lookup"><span data-stu-id="49b0e-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="49b0e-111">您在 **总帐工作流** 页上为普通日记帐设置工作流。</span><span class="sxs-lookup"><span data-stu-id="49b0e-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="49b0e-112">**默认值** - 为对方科目、币种和财务维度选择的默认值。</span><span class="sxs-lookup"><span data-stu-id="49b0e-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="49b0e-113">**日记帐控制** - 您可以设置对公司和科目类型的限制以及对科目段值的限制。</span><span class="sxs-lookup"><span data-stu-id="49b0e-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="49b0e-114">**示例**</span><span class="sxs-lookup"><span data-stu-id="49b0e-114">**Examples**</span></span>

<span data-ttu-id="49b0e-115">日记帐名称只能用于调整。</span><span class="sxs-lookup"><span data-stu-id="49b0e-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="49b0e-116">在这种情况下，您可以指定只有**“分类帐”**科目类型在所有公司都有效。</span><span class="sxs-lookup"><span data-stu-id="49b0e-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="49b0e-117">[![日记帐控制科目类型](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="49b0e-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="49b0e-118">日记帐名称只能用于某个特定科目段或用于主科目的某个范围。</span><span class="sxs-lookup"><span data-stu-id="49b0e-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="49b0e-119">[![日记帐控制科目段](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="49b0e-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="49b0e-120">**“自动冲销”**选项可用于普通日记帐。</span><span class="sxs-lookup"><span data-stu-id="49b0e-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="49b0e-121">例如，您有一个应计调整，其中的实际单据尚未处理，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="49b0e-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="49b0e-122">[![普通日记帐冲销](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="49b0e-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="49b0e-123">用于日记帐条目的 Microsoft Excel 加载项进一步提高了自动化水平并使数据输入更容易。</span><span class="sxs-lookup"><span data-stu-id="49b0e-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="49b0e-124">**“在 Excel 中打开行”**操作可用于**“普通日记帐”**和**日记帐凭证**页。</span><span class="sxs-lookup"><span data-stu-id="49b0e-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="49b0e-125">在**“期间日记帐”**页上，您可以设置重复日记帐以自动执行日记帐处理。</span><span class="sxs-lookup"><span data-stu-id="49b0e-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="49b0e-126">您可以随时使用凭证模板。</span><span class="sxs-lookup"><span data-stu-id="49b0e-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="49b0e-127">在**“普通日记帐”**页上，**“保存”**和**“选择凭证模板”**操作可在**“日志凭证”**页上找到（位于凭证行的**“功能”**下）。</span><span class="sxs-lookup"><span data-stu-id="49b0e-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="49b0e-128">相关设置</span><span class="sxs-lookup"><span data-stu-id="49b0e-128">Related setup</span></span>
<span data-ttu-id="49b0e-129">以下设置不是特定于普通日记帐的，但有助于确保数据输入正确且容易。</span><span class="sxs-lookup"><span data-stu-id="49b0e-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="49b0e-130">主科目</span><span class="sxs-lookup"><span data-stu-id="49b0e-130">Main account</span></span>

<span data-ttu-id="49b0e-131">主科目设置为普通日记帐处理提供了很多选项：</span><span class="sxs-lookup"><span data-stu-id="49b0e-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="49b0e-132">**DC/CR 需求** - 如果主科目被限制到借方或贷方交易记录，则使用此选项。</span><span class="sxs-lookup"><span data-stu-id="49b0e-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="49b0e-133">该设置在验证或过帐日记帐时验证。</span><span class="sxs-lookup"><span data-stu-id="49b0e-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="49b0e-134">**默认对方科目**</span><span class="sxs-lookup"><span data-stu-id="49b0e-134">**Default offset account**</span></span>
-   <span data-ttu-id="49b0e-135">**暂停** - 在所有公司或为特定公司/法人暂停数据输入的主科目。</span><span class="sxs-lookup"><span data-stu-id="49b0e-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="49b0e-136">**不允许手动输入** - 防止用户为日记帐中的科目手动输入值。</span><span class="sxs-lookup"><span data-stu-id="49b0e-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="49b0e-137">**默认/验证币种**</span><span class="sxs-lookup"><span data-stu-id="49b0e-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="49b0e-138">**法人覆盖** - 此设置特定于已定义的公司/法人：</span><span class="sxs-lookup"><span data-stu-id="49b0e-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="49b0e-139">**默认/验证销售税**</span><span class="sxs-lookup"><span data-stu-id="49b0e-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="49b0e-140">**默认维度** - **“不固定”**或**“固定值”**。</span><span class="sxs-lookup"><span data-stu-id="49b0e-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="49b0e-141">**“固定值”**将帮助确保此主科目的所有过帐始终使用设置为**“固定”**的任何维度值。</span><span class="sxs-lookup"><span data-stu-id="49b0e-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="49b0e-142">**过帐验证**</span><span class="sxs-lookup"><span data-stu-id="49b0e-142">**Posting validation**</span></span>
    -   <span data-ttu-id="49b0e-143">**用户验证** - 此选项控制允许哪些用户过帐到主科目。</span><span class="sxs-lookup"><span data-stu-id="49b0e-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="49b0e-144">**过帐类型验证** - 此选项控制可对主科目使用的过帐类型。</span><span class="sxs-lookup"><span data-stu-id="49b0e-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="49b0e-145">科目结构和高级规则结构</span><span class="sxs-lookup"><span data-stu-id="49b0e-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="49b0e-146">科目结构和高级规则结构对于确保在一般日记帐处理和任何单据化期间捕获财务报告所需的数据以及绩效跟踪极其重要。</span><span class="sxs-lookup"><span data-stu-id="49b0e-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="49b0e-147">科目结构和高级规则结构可让您定制数据输入体验。</span><span class="sxs-lookup"><span data-stu-id="49b0e-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="49b0e-148">您可以仅对在所有情况下都相关的财务维度允许数据输入，还可以强制实施“始终捕获必需和正确的数据”这一要求。</span><span class="sxs-lookup"><span data-stu-id="49b0e-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="49b0e-149">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="49b0e-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="49b0e-150">[计划：会计科目表](plan-chart-of-accounts.md)。</span><span class="sxs-lookup"><span data-stu-id="49b0e-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="49b0e-151">创建日记帐高级规则</span><span class="sxs-lookup"><span data-stu-id="49b0e-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="49b0e-152">使用模板创建日记帐条目</span><span class="sxs-lookup"><span data-stu-id="49b0e-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="49b0e-153">创建和验证日记帐</span><span class="sxs-lookup"><span data-stu-id="49b0e-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="49b0e-154">过帐期间日记帐</span><span class="sxs-lookup"><span data-stu-id="49b0e-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="49b0e-155">处理分类帐分配日记帐</span><span class="sxs-lookup"><span data-stu-id="49b0e-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



