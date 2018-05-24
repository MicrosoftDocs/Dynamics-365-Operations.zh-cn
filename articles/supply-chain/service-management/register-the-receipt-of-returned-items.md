---
title: "登记退回物料的接收"
description: "可使用“到达概览”窗体或“登记”窗体登记退回物料的接收。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 550b59a64fb0e81a56d6fea921e1b1df20c5f6e6
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---


# <a name="register-the-receipt-of-returned-items"></a>登记退回物料的接收 

[!include [banner](../includes/banner.md)]


可通过两种方法来登记退回物料的接收。 第一种方法是仓库接收使用**到达概览**窗体的流程。 第二种方法是使用**登记**窗体。

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>在“到达概览”窗体中登记退回物料的接收

您可以使用**到达概览**窗体，以通过其 Return Materials Authorization (RMA) 编号标识退货装运。 如果日志名称在**设置**选项卡上定义，且对应于**到达概览**窗体上选择的行的日志行存在，则，您单击**开始到达**时，创建新的日志标题。

1.  单击**库存管理** \> **定期** \> **到达概览**。

2.  在**设置名称**字段中，选择**退货单**，然后单击**更新**。
    

    > [!TIP]
    > <P>可以使用<STRONG>范围</STRONG>字段使搜索范围变窄。 在<STRONG>物料退回授权号</STRONG>字段中键入或选择物料退回授权号则可以得到精确的搜索结果。 若要定义和保存一组用于限制显示哪些传入到达的筛选器，请单击<STRONG>设置</STRONG>选项卡。可用筛选器包括类型、仓库和货台。</P>

    

    > [!WARNING]
    > <P>退货单不能与<STRONG>到达概览</STRONG>窗体中的其他到达类型混合。 因此，该参考将始终为销售订单，但是不会在日志标题中指定销售订单 ID。</P>



3.  在**收货**网格中查找与要退回的物料匹配的行，然后在**选择用于到达**列中选中该复选框。

4.  若要从退货接收中排除某些行，如不包括在退回装运货物的原始订单中的物料，请在窗体下半部分的**行**表中清除关联的**选择用于到达**复选框。

5.  单击**开始到达**按钮创建到达日志。
    

    > [!NOTE]
    > <P>可以选择多个退货单并将它们全部包括在一个到达流程中。 每个退货单行将复制到相应的物料到达日志行。</P>

    

    > [!NOTE]
    > <P>通过使用<STRONG>物料到达</STRONG>窗体，也可以手动创建到达日志。 



6.  单击**库存管理** \> **日记帐** \> **物料到达** \> **物料到达**。

7.  选择您刚创建的到达日志，然后单击**行**打开**日记帐行、库位**窗体。

8.  如果需要，在**常规**选项卡上，调整**数量**字段中的编号，然后在**处置代码**字段中分配处置代码。
    
    或者，您可以选中**检验管理**复选框将退回的物料通过检验单上下文中的检查流程发送。
    

    > [!NOTE]
    > <P>如果您通过检验发送退回物料，则您不能指定处置代码。</P>



9.  单击**验证**按钮。

10. 如果验证过程中没有出错，则单击**过帐**。

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>在“登记”窗体中登记退回物料的接收

作为使用**到达概览**窗体的备选方案，您可以使用**登记**窗体登记退回物料的到达。

1.  单击**销售和市场营销** \> **通用** \> **退货单** \> **所有退货单**。 创建新退货单或从该列表中打开退货单。 在**行**快速选项卡上，选择该退货单行。 单击**更新行**，然后单击**登记**。

2.  在**处置代码**字段中分配某一处置代码，然后单击**确定**。
    

    > [!NOTE]
    > <P>无法使用<STRONG>登记</STRONG>窗体为检查发送物料作为检验单。</P>



3.  在**交易记录**网格中，选择要登记的交易记录。

4.  在**立即登记**网格中，单击**添加**。 在所有退回物料出现在**立即登记**网格中前，重复前两个步骤。

5.  单击**全部过帐**。

## <a name="see-also"></a>请参阅

[到达概览（窗体）](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))

  



