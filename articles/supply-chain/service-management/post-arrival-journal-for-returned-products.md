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
ms.openlocfilehash: 184ce418ff2ec4b891a24b2b75d37b6b4f5d23f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006633"
---
# <a name="post-arrival-journal-for-returned-products"></a>过帐退回物料的到达日志 

[!include [banner](../includes/banner.md)]


若要处理退货，首先现在退货数量，然后在物料到达日志中更新数量字段。 然后选择一个处置代码，或指示必须检查退回的物料。 在完成这些步骤后，您可以为退货单过帐物料到达日志。

1.  单击 **库存管理** \> **定期** \> **到达概览**。

2.  在 **设置名称** 筛选器中，选择 **退货单**。

3.  如果收货列表过长，则使用 **范围** 区域中的字段缩减该列表。

4.  定位您要过帐的退货单行，选中其 **选择用于到达** 框，然后单击 **开始到达**。

5.  单击 **日记帐** \> **显示收货的到达** 打开 **库位日记帐** 窗体。
    

    > [!TIP]
    > <P>若要查看详细信息，请选择某一日志，然后单击<STRONG>行</STRONG>。</P>


6.  进行任何必要的更新，然后单击 **过帐**。

在过帐日志后，在库存中登记退回物料，并且 **退货单** 窗体将指示物料已到达仓库。

## <a name="see-also"></a>请参阅

[库位日志（窗体）](https://technet.microsoft.com/library/aa584822\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]