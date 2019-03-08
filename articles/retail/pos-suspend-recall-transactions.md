---
title: 暂停和恢复销售点 (POS) 的交易
description: 本主题说明用户如何使用 Microsoft Dynamics 365 for Retail 暂停正在进行的交易，然后在以后或在其他收银机上恢复交易。
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "333890"
---
# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a><span data-ttu-id="3bae9-103">暂停和恢复销售点 (POS) 的交易</span><span class="sxs-lookup"><span data-stu-id="3bae9-103">Suspend and resume transactions in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3bae9-104">销售点 (POS) 用户可以暂停正在进行的交易，然后在以后或在其他收银机上恢复交易。</span><span class="sxs-lookup"><span data-stu-id="3bae9-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="3bae9-105">暂停交易通常是为了快速释放收银机以处理其他任务，而不会丢失当前交易的任何进度。</span><span class="sxs-lookup"><span data-stu-id="3bae9-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="3bae9-106">例如，售货员开始在移动设备上处理客户交易，但必须先在具有银箱的收银机上完成此交易。</span><span class="sxs-lookup"><span data-stu-id="3bae9-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="3bae9-107">在这种情况下，售货员可以暂停移动设备上的交易，然后在收银机上撤回和恢复交易。</span><span class="sxs-lookup"><span data-stu-id="3bae9-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="3bae9-108">配置暂停和恢复功能</span><span class="sxs-lookup"><span data-stu-id="3bae9-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="3bae9-109">POS 操作</span><span class="sxs-lookup"><span data-stu-id="3bae9-109">POS operations</span></span>

<span data-ttu-id="3bae9-110">两个 [POS 操作](pos-operations.md)允许 POS 支持暂停和恢复方案。</span><span class="sxs-lookup"><span data-stu-id="3bae9-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="3bae9-111">您可以在交易记录页面或欢迎页面将这些操作分配到[按钮网格](pos-screen-layouts.md)。</span><span class="sxs-lookup"><span data-stu-id="3bae9-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="3bae9-112">503：暂停交易</span><span class="sxs-lookup"><span data-stu-id="3bae9-112">503: Suspend transaction</span></span>
- <span data-ttu-id="3bae9-113">504：撤回交易</span><span class="sxs-lookup"><span data-stu-id="3bae9-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="3bae9-114">收据模板</span><span class="sxs-lookup"><span data-stu-id="3bae9-114">Receipt template</span></span>

<span data-ttu-id="3bae9-115">POS 可以配置为在暂停交易时生成打印单。</span><span class="sxs-lookup"><span data-stu-id="3bae9-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="3bae9-116">该单以后可以用于快速识别和撤销交易。</span><span class="sxs-lookup"><span data-stu-id="3bae9-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="3bae9-117">若要支持 POS 打印清单，您必须将**暂停交易**收据格式添加到商店的收据模板。</span><span class="sxs-lookup"><span data-stu-id="3bae9-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="3bae9-118">您可以设计收据格式，使其包括或排除有关交易的具体详细信息。</span><span class="sxs-lookup"><span data-stu-id="3bae9-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="3bae9-119">例如，格式可以包括支持扫描的条码。</span><span class="sxs-lookup"><span data-stu-id="3bae9-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="3bae9-120">收据编号</span><span class="sxs-lookup"><span data-stu-id="3bae9-120">Receipt numbering</span></span>

<span data-ttu-id="3bae9-121">对于生成打印收据的其他 POS 交易类型，您可以在商店的功能配置文件的**收据编号**部分为暂停交易定义编号规则。</span><span class="sxs-lookup"><span data-stu-id="3bae9-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="3bae9-122">在结束班次时失效</span><span class="sxs-lookup"><span data-stu-id="3bae9-122">Void when closing shift</span></span>

<span data-ttu-id="3bae9-123">您可以使用**在结束班次时失效**选项要求用户在结束其班次前完成或取消任何暂停交易。</span><span class="sxs-lookup"><span data-stu-id="3bae9-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="3bae9-124">在执行**结束班次**操作期间，POS 将提示用户查看或取消所有未清的暂停交易。</span><span class="sxs-lookup"><span data-stu-id="3bae9-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="3bae9-125">暂停和恢复交易</span><span class="sxs-lookup"><span data-stu-id="3bae9-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="3bae9-126">暂停交易</span><span class="sxs-lookup"><span data-stu-id="3bae9-126">Suspend a transaction</span></span>

<span data-ttu-id="3bae9-127">具有足够权限并且具有包含**暂停交易**操作的屏幕布局的用户，可以暂停交易，以便交易可以在以后或在其他收银机上撤销。</span><span class="sxs-lookup"><span data-stu-id="3bae9-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="3bae9-128">只有当交易**不**包含以下行类型时交易才可以被暂停：</span><span class="sxs-lookup"><span data-stu-id="3bae9-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="3bae9-129">有效付款行</span><span class="sxs-lookup"><span data-stu-id="3bae9-129">Active payment lines</span></span>
- <span data-ttu-id="3bae9-130">礼品卡行（签发礼品卡或添加到礼品卡余额）</span><span class="sxs-lookup"><span data-stu-id="3bae9-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="3bae9-131">暂停交易不会影响商店的销售信息或库存现有量信息。</span><span class="sxs-lookup"><span data-stu-id="3bae9-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="3bae9-132">恢复暂停交易</span><span class="sxs-lookup"><span data-stu-id="3bae9-132">Resume a suspended transaction</span></span>

<span data-ttu-id="3bae9-133">暂停交易可以在同一商店内由具有足够权限，并且还具有包含**撤销交易**操作的布局的任何用户撤销和恢复。</span><span class="sxs-lookup"><span data-stu-id="3bae9-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="3bae9-134">若要快速轻松地撤销暂停交易，在您查看**撤销交易**操作的交易列表时扫描打印单上的条码。</span><span class="sxs-lookup"><span data-stu-id="3bae9-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="3bae9-135">脱机模式的注意事项</span><span class="sxs-lookup"><span data-stu-id="3bae9-135">Considerations for offline mode</span></span>

- <span data-ttu-id="3bae9-136">在 POS 处于联机模式时暂停的任何交易都不能在脱机模式下恢复，因为数据不同步到脱机数据库。</span><span class="sxs-lookup"><span data-stu-id="3bae9-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="3bae9-137">如果您在 POS 处于脱机模式时暂停交易，您可以在脱机模式下撤销它，前提是从您暂停交易起，POS 未在任何时间切换回联机模式。</span><span class="sxs-lookup"><span data-stu-id="3bae9-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="3bae9-138">在 POS 切换回脱机模式后，暂停交易的相关数据将移到脱机数据库，并被从联机数据库中删除。</span><span class="sxs-lookup"><span data-stu-id="3bae9-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="3bae9-139">因此，交易只能在脱机模式下恢复。</span><span class="sxs-lookup"><span data-stu-id="3bae9-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="3bae9-140">如果您将 POS 切换回脱机模式，您将无法恢复暂停交易，因为它们已被从脱机数据库中删除。</span><span class="sxs-lookup"><span data-stu-id="3bae9-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="3bae9-141">取消暂停交易</span><span class="sxs-lookup"><span data-stu-id="3bae9-141">Void a suspended transaction</span></span>

<span data-ttu-id="3bae9-142">您可以通过撤销交易然后执行**取消交易**操作来取消暂停交易，或者通过选择**撤销交易**列表中的交易并选择应用栏上的**取消**来取消。</span><span class="sxs-lookup"><span data-stu-id="3bae9-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="3bae9-143">或者，可以将商店配置为提示用户在结束班次时取消暂停交易。</span><span class="sxs-lookup"><span data-stu-id="3bae9-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
