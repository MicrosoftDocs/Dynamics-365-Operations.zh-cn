---
title: 冲销已过帐租赁交易
description: 本主题说明如何冲销已过帐的租赁交易。 通过资产租赁创建的任何交易都可以冲销。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 22d8eee22221efaf5e7a715c8b95dff261bee62f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249717"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="65387-104">冲销已过帐租赁交易</span><span class="sxs-lookup"><span data-stu-id="65387-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65387-105">通过资产租赁创建的任何交易都可以冲销。</span><span class="sxs-lookup"><span data-stu-id="65387-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="65387-106">通过资产租赁冲销的交易会更新您的租赁数据。</span><span class="sxs-lookup"><span data-stu-id="65387-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="65387-107">因此，它们还会更新租赁负债和使用权 (ROU) 资产的帐面价值。</span><span class="sxs-lookup"><span data-stu-id="65387-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="65387-108">要为租赁创建冲销交易，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="65387-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="65387-109">在 **资产交易** 页面或 **负债交易** 页面上，选择交易，然后选择 **冲销交易**。</span><span class="sxs-lookup"><span data-stu-id="65387-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="65387-110">在出现的对话框中，可以编辑冲销条目的过帐日期。</span><span class="sxs-lookup"><span data-stu-id="65387-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="65387-111">默认情况下，**日期** 字段设置为所选交易的交易过帐日期。</span><span class="sxs-lookup"><span data-stu-id="65387-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="65387-112">冲销条目不能早于所选交易的原始过帐日期过帐。</span><span class="sxs-lookup"><span data-stu-id="65387-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="65387-113">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="65387-113">Select **OK**.</span></span> <span data-ttu-id="65387-114">将过帐日记帐条目，以冲销您选择的条目。</span><span class="sxs-lookup"><span data-stu-id="65387-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="65387-115">将在 **资产交易** 或 **责任交易** 页上显示冲销，并更新该页上显示的当前余额的净额总计。</span><span class="sxs-lookup"><span data-stu-id="65387-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="65387-116">当您选择 **冲销追踪** 时，会出现一个对话框，其中显示原始交易和冲销的交易，以及一个链接号，称为 *跟踪号*。</span><span class="sxs-lookup"><span data-stu-id="65387-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="65387-117">为了使冲销更容易理解并提高可见性，您还可以使用租赁计划来跟踪冲销。</span><span class="sxs-lookup"><span data-stu-id="65387-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="65387-118">**计划** 页上的 **最近日记帐编号** 字段显示交易的日记帐编号。</span><span class="sxs-lookup"><span data-stu-id="65387-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="65387-119">冲销交易时，将使用冲销交易的日记帐编号更新此字段。</span><span class="sxs-lookup"><span data-stu-id="65387-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="65387-120">此外，将选中 **已冲销** 复选框，以指示交易已冲销，并且将选中 **已过帐** 字段。</span><span class="sxs-lookup"><span data-stu-id="65387-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="65387-121">撤消已冲销交易</span><span class="sxs-lookup"><span data-stu-id="65387-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="65387-122">要撤消已冲销交易，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="65387-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="65387-123">在 **计划** 页面或 **交易** 页上，选择原始交易。</span><span class="sxs-lookup"><span data-stu-id="65387-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="65387-124">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="65387-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="65387-125">如果您在 **计划** 页上选择了交易，请按照[批量创建月度日记帐条目](create-monthly-journals-batch.md)中有关创建日记帐的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="65387-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="65387-126">您必须手动过帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="65387-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="65387-127">如果您在 **交易** 页面上选择了交易，请选择 **冲销交易**。</span><span class="sxs-lookup"><span data-stu-id="65387-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="65387-128">您将收到一条消息，指出该撤回是对先前冲销的撤销，并且您可以编辑此撤销的过帐日期。</span><span class="sxs-lookup"><span data-stu-id="65387-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="65387-129">但是，一般业务验证会影响可以在 **日期** 字段中输入的日期。</span><span class="sxs-lookup"><span data-stu-id="65387-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="65387-130">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="65387-130">Select **OK**.</span></span> <span data-ttu-id="65387-131">将过帐日记帐条目，以冲销您选择的条目。</span><span class="sxs-lookup"><span data-stu-id="65387-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="65387-132">将在 **交易** 页中显示冲销，并将当前总净余额恢复为第一次冲销之前的值。</span><span class="sxs-lookup"><span data-stu-id="65387-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="65387-133">因此，避免了冲销对余额的影响。</span><span class="sxs-lookup"><span data-stu-id="65387-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="65387-134">当您选择 **冲销追踪** 时，会出现一个对话框，其中显示原始交易和冲销的交易，以及一个链接号。</span><span class="sxs-lookup"><span data-stu-id="65387-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="65387-135">您还可以使用相应 **计划** 页来跟踪冲销。</span><span class="sxs-lookup"><span data-stu-id="65387-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="65387-136">将清除 **冲销** 字段，但选中 **已过帐的日记帐** 字段。</span><span class="sxs-lookup"><span data-stu-id="65387-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="65387-137">此外，将使用撤回交易的日记帐编号更新 **最近的日记帐编号** 字段，并使用冲销日记帐编号更新 **日记帐编号** 字段。</span><span class="sxs-lookup"><span data-stu-id="65387-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]