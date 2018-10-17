---
title: "供应商交易记录列表页"
description: "此主题提供有关 Microsoft Dynamics 365 for Finance and Operations 的“供应商交易记录列表”页的信息。"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 53740f6ed0d463de5ba962f1ba15b208634a0739
ms.contentlocale: zh-cn
ms.lasthandoff: 10/01/2018

---

# <a name="vendor-transactions-list-page"></a><span data-ttu-id="6f06f-103">供应商交易记录列表页</span><span class="sxs-lookup"><span data-stu-id="6f06f-103">Vendor transactions list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="6f06f-104">查看结算</span><span class="sxs-lookup"><span data-stu-id="6f06f-104">View settlements</span></span>

<span data-ttu-id="6f06f-105">可通过操作窗格上的**查看结算**按钮快速访问结算历史记录和有关整个结算交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6f06f-105">The **View settlements** button on the Action Pane provides quick access to the settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="6f06f-106">还可以显示与所选交易记录有关的其他交易记录，因为这些交易记录属于相同结算，或因为这些交易记录是同一个付款日记帐中创建的付款。</span><span class="sxs-lookup"><span data-stu-id="6f06f-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="6f06f-107">选择**应付帐款 \> 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-107">Select **Accounts payable \> All vendors**.</span></span>
2. <span data-ttu-id="6f06f-108">选择具有交易记录的供应商，然后在操作窗格的**供应商**选项卡上选择**交易记录**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-108">Select a vendor that has transactions, and then, on the Action Pane, on the **Vendor** tab, select **Transactions**.</span></span>
3. <span data-ttu-id="6f06f-109">选择要研究的交易记录，然后在操作窗格上选择**查看结算**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-109">Select a transaction to research, and then, on the Action Pane, select **View settlements**.</span></span>

    <span data-ttu-id="6f06f-110">将显示**查看结算**对话框，其中显示所选交易记录以及已为其结算的所有单据。</span><span class="sxs-lookup"><span data-stu-id="6f06f-110">The **View settlements** dialog box appears, and shows the selected transaction and all documents that have been settled against it.</span></span> <span data-ttu-id="6f06f-111">此对话框类似结算历史记录视图，不过其中包含所有相关单据。</span><span class="sxs-lookup"><span data-stu-id="6f06f-111">This dialog box resembles the settlement history view, but it includes all related documents.</span></span>

4. <span data-ttu-id="6f06f-112">可在此对话框中执行多种任务。</span><span class="sxs-lookup"><span data-stu-id="6f06f-112">In the dialog box, you can perform various tasks.</span></span> <span data-ttu-id="6f06f-113">选择一个或多个凭证，然后选择以下按钮之一：</span><span class="sxs-lookup"><span data-stu-id="6f06f-113">Select one or more vouchers, and then select one of the following buttons:</span></span>

    - <span data-ttu-id="6f06f-114">–**查看相关**  – 显示在与所选单据关联的付款日记帐中创建的所有付款日记帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-114">**View related** – Show all the payment journal transactions that were created in the payment journal that is related to the selected document.</span></span> <span data-ttu-id="6f06f-115">此外，还将显示与这些付款有关的所有结算。</span><span class="sxs-lookup"><span data-stu-id="6f06f-115">In addition, all the settlements that are related to those payments are shown.</span></span> <span data-ttu-id="6f06f-116">查看相关付款时，此按钮的标签将变为**查看结算**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-116">While you're viewing related payments, the label of this button changes to **View settlements**.</span></span> <span data-ttu-id="6f06f-117">选择**查看结算**将仅显示首次打开**查看结算**对话框时显示的交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-117">Select **View settlements** to show only the transactions that were shown when you first opened the **View settlements** dialog box.</span></span>
    - <span data-ttu-id="6f06f-118">**查看历史记录** – 显示凭证的结算历史记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-118">**View history** – Show the settlement history for the vouchers.</span></span> <span data-ttu-id="6f06f-119">选择**关闭**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6f06f-119">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="6f06f-120">**查看记帐** – 显示与所选单据相关的所有凭证。</span><span class="sxs-lookup"><span data-stu-id="6f06f-120">**View accounting** – Show all vouchers that are related to the selected documents.</span></span> <span data-ttu-id="6f06f-121">选择**关闭**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6f06f-121">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="6f06f-122">**导出** – 将所选凭证导出到 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="6f06f-122">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
    - <span data-ttu-id="6f06f-123">**结算交易记录** – 仅当未完全结算选择的原始单据，才显示此按钮。</span><span class="sxs-lookup"><span data-stu-id="6f06f-123">**Settle transactions** – This button appears only if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="6f06f-124">选择此按钮后，将显示**结算交易记录**对话框，可在此处选择要结算的交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-124">When you select this button, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="6f06f-125">**撤消结算** – 仅当已完全结算选择的原始单据，才显示此按钮。</span><span class="sxs-lookup"><span data-stu-id="6f06f-125">**Undo settlements** – This button appears only if the original document that was selected was fully settled.</span></span> <span data-ttu-id="6f06f-126">选择此按钮后，将显示**撤消结算**对话框，可在此处撤消已对该单据执行的结算。</span><span class="sxs-lookup"><span data-stu-id="6f06f-126">When you select this button, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>

## <a name="global-transactions"></a><span data-ttu-id="6f06f-127">全球交易</span><span class="sxs-lookup"><span data-stu-id="6f06f-127">Global transactions</span></span>

<span data-ttu-id="6f06f-128">已将**全局交易记录** 按钮添加到供应商。</span><span class="sxs-lookup"><span data-stu-id="6f06f-128">The **Global transactions** button has been added to the vendor.</span></span> <span data-ttu-id="6f06f-129">此按钮用于查看某个供应商在所有法人中的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-129">This button lets you view all transactions for a vendor across all legal entities.</span></span> <span data-ttu-id="6f06f-130">**供应商交易记录**列表页仅显示用户根据自己的安全设置可访问的法人的交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-130">The **Vendor transactions** list page shows transactions only for the legal entities that the user has access to, based on his or her security settings.</span></span>

<span data-ttu-id="6f06f-131">该列表页显示当事方 ID 与您开始处理的供应商相同的供应商的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-131">The list page will show all transactions for vendors that have the same party ID as the vendor that you started with.</span></span> <span data-ttu-id="6f06f-132">例如，如果一个法人中的供应商 US-001 的当事方 ID 与另一个法人中的供应商 DE-001 相同，则显示这两个供应商 ID 的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-132">For example, if vendor US-001 in one legal entity has the same party ID as vendor DE-001 in another legal entity, all transactions for both vendor IDs are shown.</span></span>

<span data-ttu-id="6f06f-133">**供应商交易记录**列表页中的菜单取决于交易记录的法人。</span><span class="sxs-lookup"><span data-stu-id="6f06f-133">The menus on the **Vendor transactions** list page vary, depending on the legal entity for the transaction.</span></span> <span data-ttu-id="6f06f-134">例如，如果某项功能仅可用于瑞士法人，则仅当选择了瑞士交易记录时才显示该功能的菜单选项。</span><span class="sxs-lookup"><span data-stu-id="6f06f-134">For example, if a feature is available only for Swiss legal entities, the menu options for that feature appear only when a Swiss transaction is selected.</span></span>

<span data-ttu-id="6f06f-135">若要访问该功能，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6f06f-135">To access the feature, follow these steps.</span></span>

1. <span data-ttu-id="6f06f-136">选择**应付帐款** \> **所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-136">Select **Accounts payable** \> **All vendors**.</span></span>
2. <span data-ttu-id="6f06f-137">选择供应商，然后在操作窗格的**供应商**选项卡上的**交易记录**组中，选择**全局交易记录**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-137">Select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Global transactions**.</span></span>

## <a name="more-transaction-filters"></a><span data-ttu-id="6f06f-138">其他交易记录筛选器</span><span class="sxs-lookup"><span data-stu-id="6f06f-138">More transaction filters</span></span>

<span data-ttu-id="6f06f-139">已将用于显示未结交易记录的筛选器替换为了新筛选器，可通过该筛选器查看更多交易记录组合。</span><span class="sxs-lookup"><span data-stu-id="6f06f-139">The filter for showing open transactions has been replaced with a new filter that lets you view more combinations of transactions.</span></span> <span data-ttu-id="6f06f-140">**显示**字段中具有以下选项：</span><span class="sxs-lookup"><span data-stu-id="6f06f-140">The following options are available in the **Show** field:</span></span>

- <span data-ttu-id="6f06f-141">**全部** – 显示所选供应商的所有交易记录（未结和已结）。</span><span class="sxs-lookup"><span data-stu-id="6f06f-141">**All** – Show all transactions for the selected vendors (open and closed).</span></span>
- <span data-ttu-id="6f06f-142">**已结** – 仅显示已完全结算并结束的交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-142">**Closed** – Show only transactions that have been fully settled and closed.</span></span>
- <span data-ttu-id="6f06f-143">**未结** – 仅显示尚未完全结算的交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-143">**Open** – Show only transactions that haven't been fully settled.</span></span>
- <span data-ttu-id="6f06f-144">**截止指定日期未结** – 仅显示截止指定日期尚未完全结算的交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-144">**Open as of date** – Show only transactions that haven't been fully settled as of a date that you specify.</span></span> <span data-ttu-id="6f06f-145">如果选择此选项你，则可更改筛选器旁边显示的日期。</span><span class="sxs-lookup"><span data-stu-id="6f06f-145">When you select this option, you can change the date that is shown next to the filter.</span></span> <span data-ttu-id="6f06f-146">列表中显示**最后结算日期**值在您指定的日期之后的交易记录，即使这些交易记录在当天完全结算。</span><span class="sxs-lookup"><span data-stu-id="6f06f-146">Transactions that have a **Last settlement date** value after the date that you specify are shown in the list, even if those transactions are fully settled as of the current date.</span></span> <span data-ttu-id="6f06f-147">但是，余额显示截止当前日期的余额，而不是截止所选日期的余额。</span><span class="sxs-lookup"><span data-stu-id="6f06f-147">However, the balance represents the balances as of the current date, not as of the selected date.</span></span>

<span data-ttu-id="6f06f-148">还添加了一个筛选器，用于隐藏货币折算交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-148">A filter has also been added that lets you hide currency translation transactions.</span></span> <span data-ttu-id="6f06f-149">只需选中**隐藏货币重估**复选框。</span><span class="sxs-lookup"><span data-stu-id="6f06f-149">Just select the **Hide currency revaluations** check box.</span></span>

## <a name="more-easily-modify-due-dates-and-discount-dates"></a><span data-ttu-id="6f06f-150">更轻松地修改到期日期和折扣日期</span><span class="sxs-lookup"><span data-stu-id="6f06f-150">More easily modify due dates and discount dates</span></span>

<span data-ttu-id="6f06f-151">可以更新未结客户交易记录的到期日期和折扣日期。</span><span class="sxs-lookup"><span data-stu-id="6f06f-151">You can update due dates and discount dates for open customer transactions.</span></span> <span data-ttu-id="6f06f-152">版本 8.1 中已改进了体验。</span><span class="sxs-lookup"><span data-stu-id="6f06f-152">In release 8.1, the experience has been improved.</span></span> <span data-ttu-id="6f06f-153">现在可以向**供应商交易记录**列表页添加到期日期。</span><span class="sxs-lookup"><span data-stu-id="6f06f-153">You can now add due dates to the **Vendor transactions** list page.</span></span> <span data-ttu-id="6f06f-154">也可以通过在**供应商交易记录**列表页中单击到期日期，更改**更新到期日期和现金折扣日期**对话框中的到期日期、折扣日期、付款期限和现金折扣期限。</span><span class="sxs-lookup"><span data-stu-id="6f06f-154">By clicking on the due date in the **Vendor transactions** list page, you can also change due dates, discount dates, payment terms, and cash discount terms in the **Update due date and cash discount dates**  dialog box.</span></span>

### <a name="activate-the-feature"></a><span data-ttu-id="6f06f-155">激活功能</span><span class="sxs-lookup"><span data-stu-id="6f06f-155">Activate the feature</span></span>

<span data-ttu-id="6f06f-156">要通过使用 **更新到期日期和现金折扣日期**对话框向**供应商交易记录**列表页添加到到期日期和更改交易记录的付款设置，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6f06f-156">To add due dates to the **Vendor transactions** list page and change payment settings for a transaction by using the **Update due date and cash discount dates** dialog box, follow these steps.</span></span>

1. <span data-ttu-id="6f06f-157">选择**应付帐款 \> 设置 \> 应付帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-157">Select **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="6f06f-158">在**结算**选项卡上，将**显示到期日期并允许编辑**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-158">On the **Settlements** tab, Set the **Show due date and allow edit** option to **Yes**.</span></span>
3. <span data-ttu-id="6f06f-159">要启用此功能，应该已将新字段添加到了供应商交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-159">To enable this feature, new fields have been added to vendor transactions.</span></span> <span data-ttu-id="6f06f-160">完成新交易记录时，将填写这些字段。</span><span class="sxs-lookup"><span data-stu-id="6f06f-160">Those fields will be filled in when a new transaction is completed.</span></span> <span data-ttu-id="6f06f-161">打开**更新到期日期和现金折扣日期**对话框时，也将填写这些字段。</span><span class="sxs-lookup"><span data-stu-id="6f06f-161">They will also be filled in when you open the **Update due date and cash discount dates** dialog box.</span></span> <span data-ttu-id="6f06f-162">如果将**显示到期日期并允许编辑**选项设置为**是**，将显示**更新付款信息**对话框。</span><span class="sxs-lookup"><span data-stu-id="6f06f-162">When you set the **Show due date and allow edit** option to **Yes**, you will see the **Update payment information** dialog box.</span></span>  <span data-ttu-id="6f06f-163">要立即更新现有交易记录，请选择**更新所有现有交易记录**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-163">To update existing transactions immediately, select **Update all existing transactions**.</span></span> <span data-ttu-id="6f06f-164">此外，要仅为新交易记录填写这些字段，请选择**继续但不更新**。</span><span class="sxs-lookup"><span data-stu-id="6f06f-164">Alternatively, to fill in the fields only for new transactions, select **Continue without update**.</span></span>

<span data-ttu-id="6f06f-165">到期日期现在已添加到**供应商交易记录** 列表页，而您可以更轻松地修改交易记录的到期日期和现金折扣日期。</span><span class="sxs-lookup"><span data-stu-id="6f06f-165">The due date is now added to the **Vendor transactions** list page, and you can more easily modify the due date and cash discount dates for transactions.</span></span>

### <a name="modify-the-payment-settings"></a><span data-ttu-id="6f06f-166">修改付款设置</span><span class="sxs-lookup"><span data-stu-id="6f06f-166">Modify the payment settings</span></span>

<span data-ttu-id="6f06f-167">**供应商交易记录**列表页显示供应商的所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="6f06f-167">The **Vendor transactions** list page shows all transactions for a vendor.</span></span> <span data-ttu-id="6f06f-168">选择交易记录的到期日期时，将显示一个对话框。</span><span class="sxs-lookup"><span data-stu-id="6f06f-168">When you select the due date for a transaction, a dialog box appears.</span></span> <span data-ttu-id="6f06f-169">此对话框显示到期日期和折扣计算、到期日期、付款期限、现金折扣期限和现金折扣日期的基准日期。</span><span class="sxs-lookup"><span data-stu-id="6f06f-169">This dialog box shows the base date for due date and discount calculations, the due date, the payment terms, the cash discount terms, and the cash discount dates.</span></span>

<span data-ttu-id="6f06f-170">编辑时，每个字段对交易记录的影响各不相同：</span><span class="sxs-lookup"><span data-stu-id="6f06f-170">Each field has a different effect on the transaction when you edit it:</span></span>

- <span data-ttu-id="6f06f-171">**编辑基准日期：** 将单据日期视为基准日期来更改到期日期和折扣日期。</span><span class="sxs-lookup"><span data-stu-id="6f06f-171">**Edit the base date:** The due date and discount dates are changed as if the base date is the document date.</span></span>
- <span data-ttu-id="6f06f-172">**编辑到期日期：** 仅更改了到期日期</span><span class="sxs-lookup"><span data-stu-id="6f06f-172">**Edit the due date:** Only the due date is changed</span></span>
- <span data-ttu-id="6f06f-173">**编辑折扣日期：** 仅更改折扣日期。</span><span class="sxs-lookup"><span data-stu-id="6f06f-173">**Edit the discount dates:** Only the discount dates are changed.</span></span>
- <span data-ttu-id="6f06f-174">**编辑付款期限：** 根据基准日期和付款期限更改到期日期。</span><span class="sxs-lookup"><span data-stu-id="6f06f-174">**Edit the payment terms:** The due date is changed, based on the base date and the payment terms.</span></span>
- <span data-ttu-id="6f06f-175">**编辑现金折扣期限：** 根据基准日期和现金折扣期限更改现金折扣。</span><span class="sxs-lookup"><span data-stu-id="6f06f-175">**Edit the cash discount terms:** The cash discounts are changed, based on the base date and the cash discount terms.</span></span>

<span data-ttu-id="6f06f-176">付款设置编辑完毕后，请选择**关闭**以保存更改。</span><span class="sxs-lookup"><span data-stu-id="6f06f-176">When you've finished editing the payment settings, select **Close** to save your changes.</span></span>

