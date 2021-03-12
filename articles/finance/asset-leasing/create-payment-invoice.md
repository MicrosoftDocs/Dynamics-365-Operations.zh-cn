---
title: 创建付款发票
description: 本主题说明如何创建月度租赁发票。 您可以为单个租赁创建发票，也可以使用批处理为多个租赁创建发票。
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
ms.openlocfilehash: 303fb0e70530fdc29cb129736b01c0e0e8d02075
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969570"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="48646-104">创建付款发票</span><span class="sxs-lookup"><span data-stu-id="48646-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48646-105">您可以为单个租赁创建月度发票，也可以使用批处理为多个租赁创建发票。</span><span class="sxs-lookup"><span data-stu-id="48646-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="48646-106">以下过程显示了在已开启 **租赁帐簿设置** 页上的 **向供应商付款** 参数时，如何创建单个租赁付款条目。</span><span class="sxs-lookup"><span data-stu-id="48646-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="48646-107">在 **租赁摘要** 页上，选择一个租赁，然后选择 **帐簿 \> 付款计划**。</span><span class="sxs-lookup"><span data-stu-id="48646-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="48646-108">选择必须进行的付款，然后选择 **创建日记帐**。</span><span class="sxs-lookup"><span data-stu-id="48646-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="48646-109">您将收到一条消息，指出已针对所选付款创建了日记帐。</span><span class="sxs-lookup"><span data-stu-id="48646-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="48646-110">选择 **发票日记帐**，然后选择必须支付的发票。</span><span class="sxs-lookup"><span data-stu-id="48646-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="48646-111">将日记帐条目过帐到总帐之前，在 **行** 选项卡上检查该条目。</span><span class="sxs-lookup"><span data-stu-id="48646-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="48646-112">默认情况下，创建的供应商发票行使用来自 **应付帐款参数** 页的供应商过帐模板。</span><span class="sxs-lookup"><span data-stu-id="48646-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="48646-113">选择正确的日记帐，然后选择必须支付的发票。</span><span class="sxs-lookup"><span data-stu-id="48646-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="48646-114">对于此示例，已开启了租赁帐簿上的 **向供应商付款** 参数。</span><span class="sxs-lookup"><span data-stu-id="48646-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="48646-115">因此，发票将在发票日记帐中。</span><span class="sxs-lookup"><span data-stu-id="48646-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="48646-116">**概览** 部分显示日记帐条目的摘要，**行** 部分显示实际日记帐行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="48646-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="48646-117">如果已关闭 **向供应商付款** 参数，租赁帐簿的 **资产租赁** 页上将列出付款日记帐条目，而系统将创建资产租赁条目，而不是创建发票。</span><span class="sxs-lookup"><span data-stu-id="48646-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="48646-118">租赁付款条目将过帐到在 **月度租赁日记帐** 字段中指定的日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="48646-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="48646-119">过帐交易后，您可以通过选择租赁帐簿中的 **负债交易** 来查看租赁负债的交易信息和帐面价值。</span><span class="sxs-lookup"><span data-stu-id="48646-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="48646-120">在付款计划中，将选中 **已过帐的日记帐** 复选框，行将显示发票日记帐编号。</span><span class="sxs-lookup"><span data-stu-id="48646-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="48646-121">创建付款日记帐和该日记帐的条目后，必须冲销该条目，然后才能重新创建。</span><span class="sxs-lookup"><span data-stu-id="48646-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>
