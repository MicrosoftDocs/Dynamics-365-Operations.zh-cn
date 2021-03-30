---
title: 过帐退回物料的到达日志
description: 过帐退回物料的到达日志。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14619069c0e984060f67fc4536b311c6802bfec7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214290"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="c1f95-103">过帐退回物料的到达日志</span><span class="sxs-lookup"><span data-stu-id="c1f95-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c1f95-104">若要处理退货，首先现在退货数量，然后在物料到达日志中更新数量字段。</span><span class="sxs-lookup"><span data-stu-id="c1f95-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="c1f95-105">然后选择一个处置代码，或指示必须检查退回的物料。</span><span class="sxs-lookup"><span data-stu-id="c1f95-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="c1f95-106">在完成这些步骤后，您可以为退货单过帐物料到达日志。</span><span class="sxs-lookup"><span data-stu-id="c1f95-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="c1f95-107">单击 **库存管理** \> **定期** \> **到达概览**。</span><span class="sxs-lookup"><span data-stu-id="c1f95-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="c1f95-108">在 **设置名称** 筛选器中，选择 **退货单**。</span><span class="sxs-lookup"><span data-stu-id="c1f95-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="c1f95-109">如果收货列表过长，则使用 **范围** 区域中的字段缩减该列表。</span><span class="sxs-lookup"><span data-stu-id="c1f95-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="c1f95-110">定位您要过帐的退货单行，选中其 **选择用于到达** 框，然后单击 **开始到达**。</span><span class="sxs-lookup"><span data-stu-id="c1f95-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="c1f95-111">单击 **日记帐** \> **显示收货的到达** 打开 **库位日记帐** 窗体。</span><span class="sxs-lookup"><span data-stu-id="c1f95-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="c1f95-112">若要查看详细信息，请选择某一日志，然后单击<STRONG>行</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="c1f95-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="c1f95-113">进行任何必要的更新，然后单击 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="c1f95-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="c1f95-114">在过帐日志后，在库存中登记退回物料，并且 **退货单** 窗体将指示物料已到达仓库。</span><span class="sxs-lookup"><span data-stu-id="c1f95-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1f95-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1f95-115">See also</span></span>

<span data-ttu-id="c1f95-116">[库位日志（窗体）](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="c1f95-116">[Location journal (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]