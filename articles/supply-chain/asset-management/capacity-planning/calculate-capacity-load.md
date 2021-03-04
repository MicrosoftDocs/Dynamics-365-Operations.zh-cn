---
title: 计算产能负荷
description: 本主题介绍如何在资产管理中计算产能负荷。
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5015955338a4cbc2b51585d6297756f20dccee8b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423116"
---
# <a name="calculate-capacity-load"></a>计算产能负荷

[!include [banner](../../includes/banner.md)]


在资产管理中，可计算以下对象的产能负荷：

- 维护安排行  
- 尚未安排的工作订单  
- 已计划的工作订单

如果要获取特定期间的预计产能负荷的概览，这非常有用。 可以计算所有资产或所选资产的产能负荷。 也可以对维护停机时间活动或工作订单池进行计算。

1. 单击 **资产管理** > **查询** > **产能负荷**，或 **资产管理** > **常用** > **工作订单池** > **所有工作订单池** / **有效的工作订单池** > 在列表中选择工作订单池 > **产能负荷** 按钮，或 **资产管理** > **常用** > **维护停机时间活动** > **所有维护停机时间活动** / **有效的维护停机时间活动** > 在列表中选择维护活动 > **产能负荷** 按钮。

2. 在 **计算产能负荷** 对话框的 **开始日期/时间** 和 **结束日期/时间** 字段中，为计算选择期间。

3. 如果要在计算中包括维护安排行，请在 **包括维护安排** 切换按钮上选择“是”。

4. 如果要在计算中包括工作订单作业，请在 **包括工作订单** 切换按钮上选择“是”。

5. 可使用 **级别** 字段指示要与功能位置有关的产能负荷行的详细程度。 

    例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有维护安排行和工作订单，因此，可以从较低级别的功能位置叠加行中的工时。 
    
    如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有维护安排行和所有工作订单行。

6. 单击 **确定** 开始计算。

7. 在 **分组依据...** 组中，单击相关按钮显示所需成本计算详细程度。 在下面的屏幕截图中，选中的 **分组依据** 按钮以蓝色突出显示。 单击按钮将其激活或停用。

    ![图 1](media/01-capacity-planning.png)

>[!NOTE]
>如果要仅侧重有关计划的工作订单的产能计划，请参阅[对计划的工作订单计算产能负荷](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md)。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]