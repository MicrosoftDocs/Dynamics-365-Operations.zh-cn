---
title: 退货的装箱单更新
description: 在退回物料可以入库前，它们所属于的订单的装箱单必须更新。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aba61e6acf5fb959917da9ddea94c21fe1460d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "344861"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="18e92-103">退货的装箱单更新</span><span class="sxs-lookup"><span data-stu-id="18e92-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="18e92-104">在退回物料可以入库前，它们所属于的订单的装箱单必须更新。</span><span class="sxs-lookup"><span data-stu-id="18e92-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="18e92-105">就像发票更新流程是对财务交易记录进行的更新一样，装箱单更新流程是对库存记录的物理更新；这意味着它对库存进行更改。</span><span class="sxs-lookup"><span data-stu-id="18e92-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="18e92-106">在退货时，分配给处置操作的步骤在装箱单更新期间执行。</span><span class="sxs-lookup"><span data-stu-id="18e92-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="18e92-107">装箱单更新可通过物料到达日志或退货单进行处理。</span><span class="sxs-lookup"><span data-stu-id="18e92-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="18e92-108">作为过账装箱单的流程，可以选择将来自客户装运文档的装箱单参考编号与订单行相关联。</span><span class="sxs-lookup"><span data-stu-id="18e92-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="18e92-109">此关联可选和仅供参考。</span><span class="sxs-lookup"><span data-stu-id="18e92-109">This association is optional and for reference only.</span></span> <span data-ttu-id="18e92-110">它并不创建任何交易记录更新。</span><span class="sxs-lookup"><span data-stu-id="18e92-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="18e92-111">如果不是所有的预期退货物料都已到达，则应只包括在装箱单更新中接收的数量。</span><span class="sxs-lookup"><span data-stu-id="18e92-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="18e92-112">保留订单上的剩余物料，直至其余的退货装运已到达。</span><span class="sxs-lookup"><span data-stu-id="18e92-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="18e92-113">如果某一物料在经过检验后发送回装运和接收部门，例如，在检验人员不知道在库存中何处存储物料时，必须更新相应的装箱单，正确登记和操作指定为检验结果的处置代码。</span><span class="sxs-lookup"><span data-stu-id="18e92-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="18e92-114">在更新来自销售协议的退回物料的装箱单时，自动更新该物料的销售协议承诺反映数量或金额的变化。</span><span class="sxs-lookup"><span data-stu-id="18e92-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="18e92-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="18e92-115">See also</span></span>

[<span data-ttu-id="18e92-116">为退货执行发票更新</span><span class="sxs-lookup"><span data-stu-id="18e92-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


