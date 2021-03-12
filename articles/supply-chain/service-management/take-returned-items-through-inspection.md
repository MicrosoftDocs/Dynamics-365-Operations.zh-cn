---
title: 将退回物料送交检查
description: 将退回物料送交检查。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53cb727cc0f001a6ac344d37f25273999f992d8a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974077"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="fa56f-103">将退回物料送交检查</span><span class="sxs-lookup"><span data-stu-id="fa56f-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="fa56f-104">单击 **库存管理** \> **定期** \> **质量管理** \> **检验单**。</span><span class="sxs-lookup"><span data-stu-id="fa56f-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="fa56f-105">找到与您正检查的退回物料相对应的订单行。</span><span class="sxs-lookup"><span data-stu-id="fa56f-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="fa56f-106">一个检验单只能与一个物料编号关联。</span><span class="sxs-lookup"><span data-stu-id="fa56f-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="fa56f-107">如果有 10 件物料编号各不相同的物料在同一装运中退回并送交检验，则将创建 10 个单独的检验单。</span><span class="sxs-lookup"><span data-stu-id="fa56f-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="fa56f-108">在检查该物料后，在 **处置代码** 字段中进行选择，以便指示应该如何对该物料进行处理以及如何处理相关的财务交易记录。</span><span class="sxs-lookup"><span data-stu-id="fa56f-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="fa56f-109">例如，将物料退回库存并向客户退款，报废物料并将更换件发送给客户，或者将物料退回客户且不贷记。</span><span class="sxs-lookup"><span data-stu-id="fa56f-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="fa56f-110">如果不能向单个物料编号批处理中的多个退回物料分配相同的处置代码，则必须拆分该检验单（<STRONG>功能</STRONG> &gt; <STRONG>拆分</STRONG>），以便将不同的处置代码分配给每个子批处理。</span><span class="sxs-lookup"><span data-stu-id="fa56f-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="fa56f-111">在您完成检查后，单击 **完工入库** 以便下达退回物料并创建物料到达日志条目。</span><span class="sxs-lookup"><span data-stu-id="fa56f-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="fa56f-112">接收这些物料的人员或部门随后将处理这些物料的日志，以便将其退回库存。</span><span class="sxs-lookup"><span data-stu-id="fa56f-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="fa56f-113">–或者–</span><span class="sxs-lookup"><span data-stu-id="fa56f-113">–or–</span></span>
    
    <span data-ttu-id="fa56f-114">结束检验单，并通过使用 **库存** 按钮功能之一将物料直接移回库存。</span><span class="sxs-lookup"><span data-stu-id="fa56f-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="fa56f-115">关闭窗体以保存您所做更改。</span><span class="sxs-lookup"><span data-stu-id="fa56f-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa56f-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="fa56f-116">See also</span></span>

[<span data-ttu-id="fa56f-117">指定如何处置退回物料</span><span class="sxs-lookup"><span data-stu-id="fa56f-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


