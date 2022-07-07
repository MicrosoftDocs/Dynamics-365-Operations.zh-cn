---
title: 创建物料更换单
description: 在退回和检查产品后，通常创建物料更换单。
author: josaw1
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14751fb0e0632ca986d6eddf55c93d44fbd68276
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015455"
---
# <a name="create-an-item-replacement-order"></a>创建物料更换单 

[!include [banner](../includes/banner.md)]


在退回和检查产品后，通常创建物料更换单。 但是，当物料必须在退回前更换或将不退回原始物料时，可以在创建退货单后立即创建物料更换单。

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>收到退回的物料后，创建更换单。

1.  单击 **销售和市场营销** \> **销售退货** \> **所有退货单**。

2.  创建新的退货单，或从列表中选择已退货的订单以打开 **退货单 - 物料退回授权号: %1、%2** 窗体。

3.  单击 **退货行**，然后选择 **更换物料**。

4.  选择要替换退回的物料的物料。 输入物料描述，然后单击 **应用**。

5.  单击 **装箱单** 以便为退货单生成装箱单。 已为您选择的更换物料生成销售订单。
    
    为更换物料创建销售订单后，将自动搜索销售协议，如果有适用的销售协议，系统会将其应用到销售订单。

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>在接收到将退回的物料前，创建更换单。

1.  单击 **销售和市场营销** \> **销售退货** \> **所有退货单**。

2.  创建新的退货单，或从列表中选择退货订单以打开 **退货单 - 物料退回授权号: %1、%2** 窗体。

3.  如果您要标识已退回物料的销售订单，请单击 **查找销售订单**。 完成 **查找销售订单** 窗体，然后单击 **确定** 以关闭该窗体并回到 **退货单 - 物料退回授权号: %1、%2** 窗体。 已退回物料的销售订单行复制到退货单。

4.  单击 **更换单** 以打开 **创建销售订单** 窗体。

5.  选中 **复制退货单行** 复选框以将您在 **退货单 - 物料退回授权号: %1、%2** 窗体上选择的退货单的详细信息转移到此销售订单。

6.  必要时输入或修改详细信息。
    
    如果您在步骤 3 标识销售订单，以及如果已退回物料的销售订单行与销售协议关联，物料更换单的适用销售协议的标识符将自动显示在 **销售协议 ID** 字段中。

7.  单击 **确定** 以关闭 **创建销售订单** 窗体并打开 **销售订单** 窗体，其中您可以继续为新的销售订单输入信息。 所有适用的退货单行将复制到新的销售订单。 
    
    如果销售协议的标识符将自动显示在 **销售协议 ID** 字段中，则销售协议已与物料更换单的销售订单标题关联。 如果销售协议中存在尚未履行的承诺，并且销售订单在销售协议过期之前创建，则关联在销售协议行和销售订单行之间建立。 因此，销售协议中的信息（如，物料价格）复制到新的销售订单行。 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]