--- 
title: "结算会计年度"
description: "此过程介绍将余额转移到新会计年度的年终结算的步骤。"
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: df864716e64c626e486279b568be4fe5cef4abf2
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="d9aff-103">结算会计年度</span><span class="sxs-lookup"><span data-stu-id="d9aff-103">Close the fiscal year</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9aff-104">此过程介绍将余额转移到新会计年度的年终结算的步骤。</span><span class="sxs-lookup"><span data-stu-id="d9aff-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="d9aff-105">验证年终结算参数</span><span class="sxs-lookup"><span data-stu-id="d9aff-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="d9aff-106">转到总分类记账>分类记账设置 >总分类记账参数。</span><span class="sxs-lookup"><span data-stu-id="d9aff-106">Go to General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="d9aff-107">扩展“会计年度关帐”部分。</span><span class="sxs-lookup"><span data-stu-id="d9aff-107">Expand the Fiscal year close section.</span></span>
3. <span data-ttu-id="d9aff-108">为“在结转期间删除年末结转交易记录”选项选择“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-108">Select Yes or No for the option Delete close-of-year transactions during transfer.</span></span>
    * <span data-ttu-id="d9aff-109">如果此会计年度已关闭，并且正在再次运行年终结算，则此设置非常重要。</span><span class="sxs-lookup"><span data-stu-id="d9aff-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="d9aff-110">如果设置为“是”，将删除上一个年终结算的凭证，并为所有开始结余的帐户创建一个新凭证。</span><span class="sxs-lookup"><span data-stu-id="d9aff-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="d9aff-111">如果设置为“否”，将保留上一个凭证，并且仅为上一个年终结算后过帐的调整条目创建一个新凭证。</span><span class="sxs-lookup"><span data-stu-id="d9aff-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>  
4. <span data-ttu-id="d9aff-112">为是否“在结转期间创建期末交易记录”选择“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-112">Select Yes or No for whether to Create closing transactions during transfer.</span></span>
    * <span data-ttu-id="d9aff-113">如果设置为“是”，将创建两笔交易。</span><span class="sxs-lookup"><span data-stu-id="d9aff-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="d9aff-114">在正在关闭的会计年度中创建一个凭证，以便将损益会计科目的余额降为零，并在下一个会计年度中为期初余额创建第二个凭证。</span><span class="sxs-lookup"><span data-stu-id="d9aff-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="d9aff-115">如果设置为“否”，将在下一个会计年度中为期初余额创建一个凭证。</span><span class="sxs-lookup"><span data-stu-id="d9aff-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  
5. <span data-ttu-id="d9aff-116">为是否“将会计年度状态设置为‘永久关闭’”选择“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-116">Select Yes or No for whether to Set fiscal year status to permanently closed.</span></span>
    * <span data-ttu-id="d9aff-117">如果设置为“是”，将把会计年度设置为“永久关闭”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="d9aff-118">由于不能重新打开已永久关闭的年度，所以最好是将此选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  
6. <span data-ttu-id="d9aff-119">为是否必须在年终结算期间填写凭证号选择“是”或“否”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-119">Select Yes or No for whether a Voucher number must be filled in during the year end close.</span></span>
    * <span data-ttu-id="d9aff-120">如果设置为“是”，则必须在年终结算流程中手动输入凭证号。</span><span class="sxs-lookup"><span data-stu-id="d9aff-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="d9aff-121">生成此凭证号时不使用编号规则。</span><span class="sxs-lookup"><span data-stu-id="d9aff-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="d9aff-122">最好是将此选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-122">It's a best practice to set this to Yes.</span></span>  
7. <span data-ttu-id="d9aff-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d9aff-123">Close the page.</span></span>
8. <span data-ttu-id="d9aff-124">转到“总帐”>“期间结转”>“年终结算”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-124">Go to General ledger > Period close > Year end close.</span></span>
9. <span data-ttu-id="d9aff-125">单击“新建”创建年终结算模板。</span><span class="sxs-lookup"><span data-stu-id="d9aff-125">Click New to create a year-end close template.</span></span>
    * <span data-ttu-id="d9aff-126">可为要对其运行年终结算的一组法人创建模板。</span><span class="sxs-lookup"><span data-stu-id="d9aff-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="d9aff-127">可以长年累月地重复使用此模板。</span><span class="sxs-lookup"><span data-stu-id="d9aff-127">This template can be reused year after year.</span></span>  
10. <span data-ttu-id="d9aff-128">在“组名称”字段中，输入年终结算模板名称。</span><span class="sxs-lookup"><span data-stu-id="d9aff-128">In the Group name field, Enter a year-end close template name..</span></span>
11. <span data-ttu-id="d9aff-129">选择将为其创建模板的会计年度。</span><span class="sxs-lookup"><span data-stu-id="d9aff-129">Select the fiscal year for which the template will be created.</span></span>
    * <span data-ttu-id="d9aff-130">只有使用相同会计年度的法人才能在年终结算模板中分为一组。</span><span class="sxs-lookup"><span data-stu-id="d9aff-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="d9aff-131">这是因为年终结算通过选择会计年度，而不是选择日期来完成。</span><span class="sxs-lookup"><span data-stu-id="d9aff-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  
12. <span data-ttu-id="d9aff-132">使用保存记录的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="d9aff-132">Use the shortcut for saving a record.</span></span>
13. <span data-ttu-id="d9aff-133">单击“添加”为此模板选择法人。</span><span class="sxs-lookup"><span data-stu-id="d9aff-133">Click Add to select the legal entities for this template.</span></span>
    * <span data-ttu-id="d9aff-134">可通过选择法人或通过选择组织层次结构来添加法人。</span><span class="sxs-lookup"><span data-stu-id="d9aff-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="d9aff-135">只能添加组织层次结构中选择了相同会计日历的法人。</span><span class="sxs-lookup"><span data-stu-id="d9aff-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  
14. <span data-ttu-id="d9aff-136">选择法人还是组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="d9aff-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="d9aff-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-137">Click OK.</span></span>
16. <span data-ttu-id="d9aff-138">选择财务维度是否转化为下一个会计年度。</span><span class="sxs-lookup"><span data-stu-id="d9aff-138">Select whether the financial dimensions will transfer to the next fiscal year.</span></span>
    * <span data-ttu-id="d9aff-139">最好为资产负债表科目将此选项设置为“是”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-139">It's a best practice to set this option to Yes for Balance sheet accounts.</span></span>  <span data-ttu-id="d9aff-140">这将保留为资产负债表科目创建期初余额时过帐的交易的财务维度。</span><span class="sxs-lookup"><span data-stu-id="d9aff-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span>  <span data-ttu-id="d9aff-141">对于损益科目，可以在余额移动到“留存收益”时选择财务维度（全部关闭），也可以选择将财务维度替换为其他维度值（关闭单个）。</span><span class="sxs-lookup"><span data-stu-id="d9aff-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="d9aff-142">如果选择“关闭单个”，可以为每个维度定义一个特定维度值，甚至选择将其保留为空。</span><span class="sxs-lookup"><span data-stu-id="d9aff-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  
17. <span data-ttu-id="d9aff-143">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-143">Click Save.</span></span>
18. <span data-ttu-id="d9aff-144">通过在“操作”窗格中选择“运行会计结算”开始年终结算。</span><span class="sxs-lookup"><span data-stu-id="d9aff-144">Start the year-end close by choosing Run fiscal close on the Action Pane.</span></span>
    * <span data-ttu-id="d9aff-145">将为所选模板运行年终结算。</span><span class="sxs-lookup"><span data-stu-id="d9aff-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="d9aff-146">从模板中选择要对其运行年终结算的所有法人或一小组法人。</span><span class="sxs-lookup"><span data-stu-id="d9aff-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>
    * <span data-ttu-id="d9aff-147">首次运行年终结算时，若要获取期初余额，大多数组织可能选择为模板内的所有法人运行年终结算。</span><span class="sxs-lookup"><span data-stu-id="d9aff-147">When first running the year-end close, to get beginning balances most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="d9aff-148">如果在之后创建调整条目，您可以选择仅为拥有调整的法人运行年终结算。</span><span class="sxs-lookup"><span data-stu-id="d9aff-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  
20. <span data-ttu-id="d9aff-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-149">Click OK.</span></span>
21. <span data-ttu-id="d9aff-150">选择要对其运行年终结算的会计年度。</span><span class="sxs-lookup"><span data-stu-id="d9aff-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="d9aff-151">在“凭证”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d9aff-151">In the Voucher field, type a value.</span></span>
    * <span data-ttu-id="d9aff-152">最好在凭证号中包含会计年度，以便更轻松地查找创建的年终结算凭证。</span><span class="sxs-lookup"><span data-stu-id="d9aff-152">It's a best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="d9aff-153">年终结算默认批量运行。</span><span class="sxs-lookup"><span data-stu-id="d9aff-153">The year-end close defaults to run in batch.</span></span>
    * <span data-ttu-id="d9aff-154">最好以批处理模式运行长时间运行的流程。</span><span class="sxs-lookup"><span data-stu-id="d9aff-154">It's a best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="d9aff-155">这通常是这些流程中的一个，也是默认使用批处理模式的原因。</span><span class="sxs-lookup"><span data-stu-id="d9aff-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="d9aff-156">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d9aff-156">Click OK.</span></span>


