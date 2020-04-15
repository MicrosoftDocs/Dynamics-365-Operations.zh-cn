---
title: 结算会计年度
description: 此过程介绍将余额转移到新会计年度的年终结算的步骤。
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 593ab5b45cc0c2e1a8b876aa89de014fd9df1a13
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137938"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="4c419-103">结算会计年度</span><span class="sxs-lookup"><span data-stu-id="4c419-103">Close the fiscal year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c419-104">此过程介绍将余额转移到新会计年度的年终结算的步骤。</span><span class="sxs-lookup"><span data-stu-id="4c419-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="4c419-105">验证年终结算参数</span><span class="sxs-lookup"><span data-stu-id="4c419-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="4c419-106">转到**导航窗格 > 模块 > 总帐 > 分类帐设置 > 总帐参数**。</span><span class="sxs-lookup"><span data-stu-id="4c419-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="4c419-107">展开**会计年度关帐**部分。</span><span class="sxs-lookup"><span data-stu-id="4c419-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="4c419-108">为**在结转期间删除年末结转交易记录**选项选择“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="4c419-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="4c419-109">如果此会计年度已关闭，并且正在再次运行年终结算，则此设置非常重要。</span><span class="sxs-lookup"><span data-stu-id="4c419-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="4c419-110">如果设置为“是”，将删除上一个年终结算的凭证，并为所有开始结余的帐户创建一个新凭证。</span><span class="sxs-lookup"><span data-stu-id="4c419-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="4c419-111">如果设置为“否”，将保留上一个凭证，并且仅为上一个年终结算后过帐的调整条目创建一个新凭证。</span><span class="sxs-lookup"><span data-stu-id="4c419-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="4c419-112">为**在结转期间创建期末交易记录**选项选择“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="4c419-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="4c419-113">如果设置为“是”，将创建两笔交易。</span><span class="sxs-lookup"><span data-stu-id="4c419-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="4c419-114">在正在关闭的会计年度中创建一个凭证，以便将损益会计科目的余额降为零，并在下一个会计年度中为期初余额创建第二个凭证。</span><span class="sxs-lookup"><span data-stu-id="4c419-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="4c419-115">如果设置为“否”，将在下一个会计年度中为期初余额创建一个凭证。</span><span class="sxs-lookup"><span data-stu-id="4c419-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="4c419-116">为**将会计年度状态设置为永久关闭**选项选择“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="4c419-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="4c419-117">如果设置为“是”，将把会计年度设置为“永久关闭”。</span><span class="sxs-lookup"><span data-stu-id="4c419-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="4c419-118">由于不能重新打开已永久关闭的年度，所以最好是将此选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="4c419-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="4c419-119">为**必须在年终结算期间填写凭证号**选项选择“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="4c419-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="4c419-120">如果设置为“是”，则必须在年终结算流程中手动输入凭证号。</span><span class="sxs-lookup"><span data-stu-id="4c419-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="4c419-121">生成此凭证号时不使用编号规则。</span><span class="sxs-lookup"><span data-stu-id="4c419-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="4c419-122">最好是将此选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="4c419-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="4c419-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4c419-123">Close the page.</span></span>
8. <span data-ttu-id="4c419-124">转到**总帐 > 期间结转 > 年终结算**。</span><span class="sxs-lookup"><span data-stu-id="4c419-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="4c419-125">单击**新建**创建年终结算模板。</span><span class="sxs-lookup"><span data-stu-id="4c419-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="4c419-126">可为要对其运行年终结算的一组法人创建模板。</span><span class="sxs-lookup"><span data-stu-id="4c419-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="4c419-127">可以长年累月地重复使用此模板。</span><span class="sxs-lookup"><span data-stu-id="4c419-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="4c419-128">在**组名称**字段中，输入年终结算模板名称。</span><span class="sxs-lookup"><span data-stu-id="4c419-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="4c419-129">在**会计日历**字段中，选择将为其创建模板的会计年度。</span><span class="sxs-lookup"><span data-stu-id="4c419-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="4c419-130">只有使用相同会计年度的法人才能在年终结算模板中分为一组。</span><span class="sxs-lookup"><span data-stu-id="4c419-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="4c419-131">这是因为年终结算通过选择会计年度，而不是选择日期来完成。</span><span class="sxs-lookup"><span data-stu-id="4c419-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="4c419-132">在**操作窗格**上，单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="4c419-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="4c419-133">在**法人**部分中，单击**添加**为此模板选择法人。</span><span class="sxs-lookup"><span data-stu-id="4c419-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="4c419-134">可通过选择法人或通过选择组织层次结构来添加法人。</span><span class="sxs-lookup"><span data-stu-id="4c419-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="4c419-135">只能添加组织层次结构中选择了相同会计日历的法人。</span><span class="sxs-lookup"><span data-stu-id="4c419-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="4c419-136">选择法人还是组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="4c419-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="4c419-137">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="4c419-137">Click **OK**.</span></span>
16. <span data-ttu-id="4c419-138">在**转移资产负债表维度**中选择“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="4c419-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="4c419-139">最好为资产负债表科目将此选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="4c419-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="4c419-140">这将保留为资产负债表科目创建期初余额时过帐的交易的财务维度。</span><span class="sxs-lookup"><span data-stu-id="4c419-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="4c419-141">对于损益科目，可以在余额移动到“留存收益”时选择财务维度（全部关闭），也可以选择将财务维度替换为其他维度值（关闭单个）。</span><span class="sxs-lookup"><span data-stu-id="4c419-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="4c419-142">如果选择“关闭单个”，可以为每个维度定义一个特定维度值，甚至选择将其保留为空。</span><span class="sxs-lookup"><span data-stu-id="4c419-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="4c419-143">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="4c419-143">Click **Save**.</span></span>
18. <span data-ttu-id="4c419-144">通过在**操作窗格**中选择**运行会计结算**开始年终结算。</span><span class="sxs-lookup"><span data-stu-id="4c419-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="4c419-145">将为所选模板运行年终结算。</span><span class="sxs-lookup"><span data-stu-id="4c419-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="4c419-146">从模板中选择要对其运行年终结算的所有法人或一小组法人。</span><span class="sxs-lookup"><span data-stu-id="4c419-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="4c419-147">首次运行年终结算时，若要获取期初余额，大多数组织可能选择为模板内的所有法人运行年终结算。</span><span class="sxs-lookup"><span data-stu-id="4c419-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="4c419-148">如果在之后创建调整条目，您可以选择仅为拥有调整的法人运行年终结算。</span><span class="sxs-lookup"><span data-stu-id="4c419-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="4c419-149">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="4c419-149">Click **OK**.</span></span>
21. <span data-ttu-id="4c419-150">选择要对其运行年终结算的会计年度。</span><span class="sxs-lookup"><span data-stu-id="4c419-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="4c419-151">在**凭证**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4c419-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="4c419-152">最好在凭证号中包含会计年度，以便更轻松地查找创建的年终结算凭证。</span><span class="sxs-lookup"><span data-stu-id="4c419-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="4c419-153">年终结算默认批量运行。</span><span class="sxs-lookup"><span data-stu-id="4c419-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="4c419-154">最好以批处理模式运行长时间运行的流程。</span><span class="sxs-lookup"><span data-stu-id="4c419-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="4c419-155">这通常是这些流程中的一个，也是默认使用批处理模式的原因。</span><span class="sxs-lookup"><span data-stu-id="4c419-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="4c419-156">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="4c419-156">Click **OK**.</span></span>

