---
title: "接收退回物料的部分交货"
description: "部分交货根据退货单行（而非退货单装运）定义。"
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="fdc7d-103">接收退回物料的部分交货</span><span class="sxs-lookup"><span data-stu-id="fdc7d-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fdc7d-104">部分交货根据退货单行（而非退货单装运）定义。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="fdc7d-105">这意味着如果您收到在一个退货单行上指示的完整数量、但在退货单的其他行中未指示任何数量，则该交货不是部分交货。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="fdc7d-106">但是，如果某一退货单行要求退回 10 个单位的特定物料，但您只收到四个单位，则该交货是部分交货。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="fdc7d-107">如果退货装运包含的数量少于退货单行的完整数量，则您可以暂不考虑该装运，并且等待其余退回数量到达，或者您可以登记和过帐部分数量。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="fdc7d-108">登记和过帐部分数量</span><span class="sxs-lookup"><span data-stu-id="fdc7d-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="fdc7d-109">在**到达概览 - 仓库: %1、码头: %2、日记帐名称: %3** 窗体中为到达选择退货单后，单击**开始到达**创建到达日记帐，然后单击**日记帐** \> **显示收货的到达**打开**库位日记帐**窗体。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="fdc7d-110">选择您要处理的日志行，然后单击**行**以打开**日记帐行，库位**窗体。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="fdc7d-111">选择只有部分数量到达的物料编号的行，然后单击**功能** \> **拆分**以打开**拆分**窗体。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="fdc7d-112">在**待拆分数量**字段中，输入已收到的物料的总数量，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="fdc7d-113">在**日记帐行，库位**窗体上，选择已到达的物料数量的行，然后单击**过帐**。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="fdc7d-114">您可以在物料已到达后过帐额外的数量行。</span><span class="sxs-lookup"><span data-stu-id="fdc7d-114">You can post the line for the additional quantity after the items have arrived.</span></span>





