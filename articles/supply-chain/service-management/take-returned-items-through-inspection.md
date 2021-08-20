---
title: 将退回物料送交检查
description: 将退回物料送交检查。
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 99c53931b95816188367f903628db4e6d62b38bd16aba0014b03c8a79e815194
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760940"
---
# <a name="take-returned-items-through-inspection"></a>将退回物料送交检查 

[!include [banner](../includes/banner.md)]


1.  单击 **库存管理** \> **定期** \> **质量管理** \> **检验单**。

2.  找到与您正检查的退回物料相对应的订单行。

    > [!NOTE]
    > <P>一个检验单只能与一个物料编号关联。 如果有 10 件物料编号各不相同的物料在同一装运中退回并送交检验，则将创建 10 个单独的检验单。</P>

3.  在检查该物料后，在 **处置代码** 字段中进行选择，以便指示应该如何对该物料进行处理以及如何处理相关的财务交易记录。 例如，将物料退回库存并向客户退款，报废物料并将更换件发送给客户，或者将物料退回客户且不贷记。
    
    > [!NOTE]
    > <P>如果不能向单个物料编号批处理中的多个退回物料分配相同的处置代码，则必须拆分该检验单（<STRONG>功能</STRONG> &gt; <STRONG>拆分</STRONG>），以便将不同的处置代码分配给每个子批处理。</P>


4.  在您完成检查后，单击 **完工入库** 以便下达退回物料并创建物料到达日志条目。 接收这些物料的人员或部门随后将处理这些物料的日志，以便将其退回库存。
    
    –或者–
    
    结束检验单，并通过使用 **库存** 按钮功能之一将物料直接移回库存。

5.  关闭窗体以保存您所做更改。

## <a name="see-also"></a>请参阅

[指定如何处置退回物料](specify-how-to-dispose-of-returned-items.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]