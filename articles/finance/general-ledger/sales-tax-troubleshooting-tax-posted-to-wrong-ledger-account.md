---
title: 税款过帐到凭证中错误的会计科目
description: 本主题提供可以在税款过帐到凭证中错误的会计科目时提供帮助的故障排除信息。
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020083"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="ad7cb-103">税款过帐到凭证中错误的会计科目</span><span class="sxs-lookup"><span data-stu-id="ad7cb-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad7cb-104">过帐期间，税款可能被过帐到凭证中错误的会计科目。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="ad7cb-105">要解决此问题，请根据需要按照以下各节中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="ad7cb-106">本主题中的示例使用销售订单作为业务文档。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="ad7cb-107">查找错误过帐的税收交易的税代码</span><span class="sxs-lookup"><span data-stu-id="ad7cb-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="ad7cb-108">在 **凭证交易** 页上，选择要处理的交易，然后选择 **已过帐销售税**。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="ad7cb-109">[![“凭证交易”页上的已过帐销售税按钮](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="ad7cb-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="ad7cb-110">查看 **销售税代码** 字段中的值。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="ad7cb-111">在此示例中，是 **增值税 19**。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="ad7cb-112">[![“已过帐销售税”页上的“销售税代码”字段](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="ad7cb-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="ad7cb-113">检查税代码的分类帐过帐组</span><span class="sxs-lookup"><span data-stu-id="ad7cb-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="ad7cb-114">转到 **税** \> **间接税** \> **销售税** \> **销售税代码**。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="ad7cb-115">找到并选择税代码，然后查看 **分类帐过帐组** 字段中的值。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="ad7cb-116">在此示例中，是 **增值税**。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="ad7cb-117">[![“销售税代码”页上的“分类帐过帐组”字段](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="ad7cb-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="ad7cb-118">**分类帐过帐组** 字段中的值是一个链接。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="ad7cb-119">要查看组配置的详细信息，选择该链接。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="ad7cb-120">或者，在字段中选择并按住（或右键单击），然后选择 **查看详细信息**。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="ad7cb-121">[![“查看详细信息”命令](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="ad7cb-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="ad7cb-122">在 **应付销售税** 字段中，根据交易类型验证科目编号是否正确。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="ad7cb-123">如果不正确，请选择要过帐到的正确科目。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="ad7cb-124">在此示例中，应将销售订单的销售税过帐到应付销售税科目 222200。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="ad7cb-125">[![“分类帐过帐组”页上的“应付销售税”字段](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="ad7cb-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="ad7cb-126">下表提供了有关 **分类帐过帐组** 页上每个字段的信息。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="ad7cb-127">字段</span><span class="sxs-lookup"><span data-stu-id="ad7cb-127">Field</span></span>                  | <span data-ttu-id="ad7cb-128">说明</span><span class="sxs-lookup"><span data-stu-id="ad7cb-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="ad7cb-129">应付销售税</span><span class="sxs-lookup"><span data-stu-id="ad7cb-129">Sales tax payable</span></span>      | <span data-ttu-id="ad7cb-130">应付给税务主管机构的输出销售税的主科目。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="ad7cb-131">应收销售税</span><span class="sxs-lookup"><span data-stu-id="ad7cb-131">Sales tax receivable</span></span>   | <span data-ttu-id="ad7cb-132">从税务主管机构收到的进项税的主科目。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="ad7cb-133">销项税支出</span><span class="sxs-lookup"><span data-stu-id="ad7cb-133">Use tax expense</span></span>        | <span data-ttu-id="ad7cb-134">此主科目用于过帐供应商不在欧盟 (EU) 反向计费商品劳务税 (GST)/统一销售税 (HST) 中向税务主管机构要求或报告的可扣减销项税。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="ad7cb-135">必须为在交易中使用的销售税组的销售税代码选择 **销项税**。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="ad7cb-136">如果在 **总帐参数** 页上选择了 **应用销售税纳税规则**，此字段则不可用。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="ad7cb-137">应付销项税</span><span class="sxs-lookup"><span data-stu-id="ad7cb-137">Use tax payable</span></span>        | <span data-ttu-id="ad7cb-138">用于过帐应付给税务主管机构的所得销项税的主科目。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="ad7cb-139">结算帐户</span><span class="sxs-lookup"><span data-stu-id="ad7cb-139">Settlement account</span></span>     | <span data-ttu-id="ad7cb-140">用于过帐在 **应付销项税** 和 **应收销售税** 字段中指定的会计科目的净余额的主科目。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="ad7cb-141">供应商现金折扣</span><span class="sxs-lookup"><span data-stu-id="ad7cb-141">Vendor cash discount</span></span>   | <span data-ttu-id="ad7cb-142">用于过帐与此分类帐过帐组关联的销售税代码的现金折扣的主科目。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="ad7cb-143">客户折扣</span><span class="sxs-lookup"><span data-stu-id="ad7cb-143">Customer case discount</span></span> | <span data-ttu-id="ad7cb-144">用于过帐与此分类帐过帐组关联的销售税代码的现金折扣的主科目。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="ad7cb-145">有关详细信息，请参阅[设置销售税分类帐过帐组](tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="ad7cb-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="ad7cb-146">调试代码以检查分类帐维度</span><span class="sxs-lookup"><span data-stu-id="ad7cb-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="ad7cb-147">在代码中，过帐科目由分类帐维度确定。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="ad7cb-148">分类帐维度将科目的记录 ID 保存在数据库中。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="ad7cb-149">对于销售订单，在 **Tax::saveAndPost()** 和 **Tax::post()** 方法处添加中断点。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="ad7cb-150">注意 **\_ledgerDimension** 的值。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="ad7cb-151">[![具有中断点的销售订单代码示例](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="ad7cb-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="ad7cb-152">对于采购订单，在 **TaxPost::saveAndPost()** 和 **TaxPost::postToTaxTrans()** 方法处添加中断点。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="ad7cb-153">注意 **\_ledgerDimension** 的值。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="ad7cb-154">[![具有中断点的采购订单代码示例](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="ad7cb-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="ad7cb-155">运行以下 SQL 查询，根据分类帐维度保存的记录 ID 在数据库中查找科目的显示值。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="ad7cb-156">[![记录 ID 的显示值](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="ad7cb-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="ad7cb-157">检查调用堆栈，查找分配 **_ledgerDimension** 值的位置。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="ad7cb-158">通常，此值来自 **TmpTaxWorkTrans**。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="ad7cb-159">在这种情况下，您应该在 **TmpTaxWorkTrans::insert()** 和 **TmpTaxWorkTrans::update()** 处添加中断点来查找分配值的位置。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="ad7cb-160">确定是否存在自定义</span><span class="sxs-lookup"><span data-stu-id="ad7cb-160">Determine whether customization exists</span></span>

<span data-ttu-id="ad7cb-161">如果您已经完成了前面几节中的步骤，但未发现问题，请确定是否存在自定义。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="ad7cb-162">如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。</span><span class="sxs-lookup"><span data-stu-id="ad7cb-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
