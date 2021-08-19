---
title: 计算物料预测
description: 本主题介绍如何在资产管理中计算物料预测。
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5773149760ecb2a26f4916036fe36c9cc04f654039dee4eab9bfac86eb02e1fd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713022"
---
# <a name="calculate-item-forecast"></a>计算物料预测

[!include [banner](../../includes/banner.md)]

 

就像可以创建上一部分中介绍的产能负荷计算，也可以为以下对象创建物料预测计算：

- 维护安排行  
- 尚未安排的工作订单  
- 已计划的工作订单

如果要获取特定期间的预计物料消耗（为了完成工作订单需要的备件和其他物料）的概览，此功能非常有用。 可以计算所有资产或所选资产的物料预测。 也可以为维护停机时间活动（**所有维护停机时间活动** 或 **有效维护停机时间活动**）或工作订单池（**所有工作订单池** 或 **有效工作订单池**）创建计算。

1. 单击 **资产管理** > **查询** > **物料预测**，或 **资产管理** > **常用** > **工作订单池** > **所有工作订单池** / **有效的工作订单池** > 在列表中选择工作订单池 > **物料预测** 按钮，或 **资产管理** > **常用** > **维护停机时间活动** > **所有维护停机时间活动** / **有效的维护停机时间活动** > 在列表中选择维护停机时间活动 > **物料预测** 按钮。

2. 在 **计算物料预测** 对话框的 **开始日期/时间** 和 **结束日期/时间** 字段中，为计算选择期间。

3. 如果要在预测计算中包括维护安排行，请在 **包括维护安排** 切换按钮上选择“是”。

4. 如果要在预测计算中包括工作订单作业，请在 **包括工作订单** 切换按钮上选择“是”。

5. 可使用 **级别** 字段指示要与功能位置有关的物料预测行的详细程度。 

      例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有维护安排行和工作订单，因此，可以从较低级别的功能位置叠加行中的工时。 
  
      如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有维护安排行和所有工作订单行。

6. 单击 **确定** 开始计算。

7. 在 **分组依据...** 组中，单击相关按钮显示所需成本计算详细程度。 在下面的屏幕截图中，选中的 **分组依据** 按钮以蓝色突出显示。 单击按钮将其激活或停用。

8. 如果要查看与物料关联的产品、存储或跟踪维度，请单击 **显示维度** 按钮。 选中相关复选框，然后单击 **确定**。

![图 1.](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]