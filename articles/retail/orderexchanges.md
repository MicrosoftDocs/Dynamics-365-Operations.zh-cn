---
title: 配置和处理有关退货单的交换
description: 本主题将介绍如何在 Microsoft Dynamics 365 for Retail 中配置退货交换。
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a0a6a060a1b4a4d5a80c797f61b212a828d2f04
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517011"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="cf41b-103">配置和处理有关退货单的交换</span><span class="sxs-lookup"><span data-stu-id="cf41b-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf41b-104">在先前版本的 Microsoft Dynamics 365 for Retail 中，针对客户订单的退货是采用 Retail Headquarters 中的退货单文档进行处理的。</span><span class="sxs-lookup"><span data-stu-id="cf41b-104">In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail Headquarters.</span></span> <span data-ttu-id="cf41b-105">但是，退货单文档仅可用于处理要退货的产品。</span><span class="sxs-lookup"><span data-stu-id="cf41b-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="cf41b-106">退货产品由退货单行上的负数量指示。</span><span class="sxs-lookup"><span data-stu-id="cf41b-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="cf41b-107">相对比的是，销量由正数量指示。</span><span class="sxs-lookup"><span data-stu-id="cf41b-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="cf41b-108">但是，退货单文档不支持正数量。</span><span class="sxs-lookup"><span data-stu-id="cf41b-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="cf41b-109">由于此限制，先前版本的 Retail 不支持使用退货单文档进行产品交换的方案。</span><span class="sxs-lookup"><span data-stu-id="cf41b-109">Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="cf41b-110">但是，现已添加了相应功能，可支持就退货单进行产品交换的方案。</span><span class="sxs-lookup"><span data-stu-id="cf41b-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="cf41b-111">Retail 现在使用销售订单文档而不是退货单文档来处理这些类型的交易。</span><span class="sxs-lookup"><span data-stu-id="cf41b-111">Retail now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a><span data-ttu-id="cf41b-112">配置 Retail 以支持就退货单进行产品交换</span><span class="sxs-lookup"><span data-stu-id="cf41b-112">Configure Retail to support exchanges on return orders</span></span>

<span data-ttu-id="cf41b-113">请按以下步骤操作，将系统配置为支持就退货单进行产品交换。</span><span class="sxs-lookup"><span data-stu-id="cf41b-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="cf41b-114">转到 **Retail \> 总部设置 \> 参数 \> Retail 参数**。</span><span class="sxs-lookup"><span data-stu-id="cf41b-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="cf41b-115">在**客户订单**快速选项卡上，将**将退货单作为销售订单处理**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="cf41b-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="cf41b-116">运行**全局配置配送计划**作业 (**1110**)。</span><span class="sxs-lookup"><span data-stu-id="cf41b-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="cf41b-117">进行交换</span><span class="sxs-lookup"><span data-stu-id="cf41b-117">Make an exchange</span></span>

<span data-ttu-id="cf41b-118">在按照上一部分中所述配置系统之后，与在先前版本的 Retail 中的操作一样，销售终端 (POS) 用户仍将选择销售订单或销售发票来处理退货。</span><span class="sxs-lookup"><span data-stu-id="cf41b-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</span></span> <span data-ttu-id="cf41b-119">但是，在将退回物料添加到购物车之后，用户将能够向购物车添加新的销售行。</span><span class="sxs-lookup"><span data-stu-id="cf41b-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="cf41b-120">对于这些新的销售行，用户必须定义所有必需的属性才能处理客户订单行。</span><span class="sxs-lookup"><span data-stu-id="cf41b-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="cf41b-121">这些属性包括交货方法和履行位置。</span><span class="sxs-lookup"><span data-stu-id="cf41b-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="cf41b-122">交易的到期付款将是退货单行和销售订单行的净额。</span><span class="sxs-lookup"><span data-stu-id="cf41b-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="cf41b-123">当支付交易付款时，退货单将在 Retail Headquarters 中过帐为销售订单文档，系统将立即根据退货行开具发票。</span><span class="sxs-lookup"><span data-stu-id="cf41b-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="cf41b-124">为了让用户更好地了解购物车的各项金额，购物车中新增了三个金额字段。</span><span class="sxs-lookup"><span data-stu-id="cf41b-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="cf41b-125">您可以使用屏幕设计器，在 POS 用户界面 (UI) 中提供这些新字段。</span><span class="sxs-lookup"><span data-stu-id="cf41b-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="cf41b-126">**存款单已应用** – 当用户执行客户订单选择时应用于交易的存款金额。</span><span class="sxs-lookup"><span data-stu-id="cf41b-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="cf41b-127">如果不存在存款覆盖，并且配置了 10% 的存款，则此字段中的金额为客户订单总金额的 90%。</span><span class="sxs-lookup"><span data-stu-id="cf41b-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="cf41b-128">**执行金额** – 创建或编辑客户订单时或者在客户订单交换期间，交货方式设置为**执行**情况下各行的总金额。</span><span class="sxs-lookup"><span data-stu-id="cf41b-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="cf41b-129">此字段中的金额包括税款和费用。</span><span class="sxs-lookup"><span data-stu-id="cf41b-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="cf41b-130">**退货金额** – 客户订单交换期间具有负数量的行的总金额。</span><span class="sxs-lookup"><span data-stu-id="cf41b-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="cf41b-131">此字段中的金额包括税款和费用。</span><span class="sxs-lookup"><span data-stu-id="cf41b-131">The amount in this field includes taxes and charges.</span></span>
