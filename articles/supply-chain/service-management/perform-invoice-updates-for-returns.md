---
title: 为退货执行发票更新
description: 此功能支持组织选择采用的业务流程，即同时由同一人对退货单和销售订单开票。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41d3b884d1ed11d2f79e968a5a099860486ef600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810646"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="508bd-103">为退货执行发票更新</span><span class="sxs-lookup"><span data-stu-id="508bd-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="508bd-104">退货单是一种标记为退回订单的销售订单。</span><span class="sxs-lookup"><span data-stu-id="508bd-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="508bd-105">因此，**所有销售订单** 列表页用于生成退货单的发票，而不是从 **退货单** 窗体中生成。</span><span class="sxs-lookup"><span data-stu-id="508bd-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="508bd-106">此功能支持组织选择采用的业务流程，即同时由同一人对退货单和销售订单开票。</span><span class="sxs-lookup"><span data-stu-id="508bd-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="508bd-107">由于退回物料的发票用于负金额，称作贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="508bd-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="508bd-108">在您为批处理设置发票更新时，**退回订单** 类型的销售订单必须具有 **已接收** 的退货单行状态，指示该订单的装箱单已更新。</span><span class="sxs-lookup"><span data-stu-id="508bd-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="508bd-109">过帐退货单的发票</span><span class="sxs-lookup"><span data-stu-id="508bd-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="508bd-110">单击 **应收帐款** \> **通用** \> **销售订单** \> **所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="508bd-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="508bd-111">选择在 **订单类型** 字段中显示的 **退回订单** 的销售订单。</span><span class="sxs-lookup"><span data-stu-id="508bd-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="508bd-112">在操作窗格 **发票** 选项卡的 **常规** 组中，单击 **发票**。</span><span class="sxs-lookup"><span data-stu-id="508bd-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="508bd-113">在 **参数** 选项卡上，选中 **过帐** 复选框。</span><span class="sxs-lookup"><span data-stu-id="508bd-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="508bd-114">查看窗体中的信息，并进行必要的更改。</span><span class="sxs-lookup"><span data-stu-id="508bd-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="508bd-115">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="508bd-115">Click **OK**.</span></span> <span data-ttu-id="508bd-116">– 贷方通知单已过帐。</span><span class="sxs-lookup"><span data-stu-id="508bd-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="508bd-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="508bd-117">See also</span></span>

[<span data-ttu-id="508bd-118">退货的装箱单更新</span><span class="sxs-lookup"><span data-stu-id="508bd-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]