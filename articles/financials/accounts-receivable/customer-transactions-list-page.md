---
title: "客户交易记录列表页"
description: "此主题提供有关 Microsoft Dynamics 365 for Finance and Operations 的“客户交易记录列表”页的信息。"
author: mikefalkner
manager: aolson
ms.date: 08/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e828cb292ad48bb4690117b41589b25edcdf28bc
ms.contentlocale: zh-cn
ms.lasthandoff: 08/31/2018

---

# <a name="customer-transaction-list-page"></a><span data-ttu-id="d4c7d-103">客户交易记录列表页</span><span class="sxs-lookup"><span data-stu-id="d4c7d-103">Customer transaction list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="d4c7d-104">查看结算</span><span class="sxs-lookup"><span data-stu-id="d4c7d-104">View settlements</span></span>

<span data-ttu-id="d4c7d-105">可通过操作窗格上的**查看结算**选项卡快速访问结算历史记录和有关整个结算交易记录的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-105">The **View settlements** tab on the action pane provides quick access to settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="d4c7d-106">还可以显示与所选交易记录有关的其他交易记录，因为这些交易记录属于相同结算，或因为这些交易记录是同一个付款日记帐中创建的付款。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="d4c7d-107">选择**应收帐款 \> 客户**。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-107">Select **Accounts receivable \> Customers**.</span></span>
2. <span data-ttu-id="d4c7d-108">选择具有交易记录的客户，然后选择 **客户 \> 交易记录**。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-108">Select a customer that has transactions, and then select **Customer \> Transactions**.</span></span>
3. <span data-ttu-id="d4c7d-109">选择要研究的交易记录。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-109">Select a transaction to research.</span></span>
4. <span data-ttu-id="d4c7d-110">在操作窗格上选择**查看结算**选项卡。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-110">Select the **View settlements** tab on the action pane.</span></span>

    <span data-ttu-id="d4c7d-111">**查看结算**对话框将显示所选交易记录以及已为其结算的所有单据。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-111">The **View settlements** dialog box shows the selected transaction and all documents that have been settled against it.</span></span> <span data-ttu-id="d4c7d-112">此对话框类似结算历史记录视图，不过其中包含所有相关单据。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-112">This dialog box resembles the settlement history view, but it includes all related documents.</span></span> 

5. <span data-ttu-id="d4c7d-113">可以通过此对话框执行多种任务。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-113">You can perform various tasks from this dialog box.</span></span> <span data-ttu-id="d4c7d-114">选择一个或多个凭证，然后选择以下菜单之一：</span><span class="sxs-lookup"><span data-stu-id="d4c7d-114">Select one or more vouchers, and then select one of the following menus:</span></span>

   - <span data-ttu-id="d4c7d-115">**查看记帐** – 将显示与所选单据相关的所有凭证。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-115">**View accounting** – All vouchers that are related to the selected documents appear.</span></span> <span data-ttu-id="d4c7d-116">选择**关闭**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-116">Select **Close** to close the dialog box.</span></span>
   - <span data-ttu-id="d4c7d-117">**导出** – 将所选凭证导出到 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-117">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
   - <span data-ttu-id="d4c7d-118">–**查看相关付款**  – 将显示在与所选单据关联的付款日记帐中创建的所有付款日记帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-118">**View related payments** – All the payment journal transactions that were created in the payment journal that is related to the selected document appear.</span></span> <span data-ttu-id="d4c7d-119">此外，还将显示与这些付款有关的所有结算。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-119">In addition, all the settlements that are related to those payments appear.</span></span> <span data-ttu-id="d4c7d-120">此菜单的标签还会变为**查看结算**。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-120">The label of this menu also changes to **View settlements**.</span></span> <span data-ttu-id="d4c7d-121">选择**查看结算**将仅显示首次打开**查看结算**对话框时显示的交易记录。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-121">Select **View settlements** to show only the transactions that were shown when you first opened the  **View settlements** dialog box.</span></span>
    - <span data-ttu-id="d4c7d-122">**结算交易记录** – 如果未完全结算选择的原始单据，将显示此菜单。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-122">**Settle transactions** – This menu appears if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="d4c7d-123">选择后，将显示**结算交易记录**对话框，可在此处选择要结算的交易记录。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-123">When you select it, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="d4c7d-124">**撤消结算** – 如果已完全结算选择的原始单据，将显示此菜单。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-124">**Undo settlements** – This menu appears if the original document that was selected was fully settled.</span></span> <span data-ttu-id="d4c7d-125">选择后，将显示**撤消结算**对话框，可在此处撤消已对该单据执行的结算。</span><span class="sxs-lookup"><span data-stu-id="d4c7d-125">When you select it, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>
    

