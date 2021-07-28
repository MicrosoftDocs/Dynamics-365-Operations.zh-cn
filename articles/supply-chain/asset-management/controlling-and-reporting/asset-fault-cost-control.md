---
title: 资产故障成本控制
description: 本主题介绍资产管理中的资产故障成本控制。
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bbf2d6b8e22981db76ca028073f8170cbe7f40b2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361058"
---
# <a name="asset-fault-cost-control"></a>资产故障成本控制

[!include [banner](../../includes/banner.md)]

 

在资产管理中，可计算资产故障登记的成本，以便获取实际成本与预算成本的比较概览。 实际成本基于过帐的交易记录。 日期是记录故障特征时的故障日期。

1. 单击 **资产管理** > **查询** > **资产故障** > **资产故障成本控制**。

2. 在 **资产故障成本控制** 对话框中，选择计算中要包括的财务维度集（如果需要）。

4. 如果不希望显示包含零成本的结果，请在 **忽略零** 切换按钮上选择“是”。

5. 可使用 **级别** 字段指示要与功能位置有关的成本控制行的详细程度。 

    例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有资产故障成本控制行，因此，可以从较低级别的功能位置叠加行中的工时。 
    
    如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有资产故障成本控制行。

6. 如果要限制搜索，可在 **要包括的记录** 快速选项卡上选择特定资产、故障日期和故障成因。

7. 单击 **确定** 开始计算。

8. 单击 **分组依据** 按钮显示所需的计算详细程度。 将突出显示所选 **分组依据** 按钮。 单击按钮将其激活或停用。

## <a name="example"></a>示例

此示例显示资产故障成本控制计算。

- **原始预算** 字段显示工作订单预测中的预算成本。 
- **实际成本** 字段显示工作订单中的已过帐成本。 
- **承诺成本** 字段显示在与工作订单关联时，公司承诺的总成本。

    ![图 1.](media/05-controlling-and-reporting.png)

有关如何设置故障的信息，请参阅[故障管理](../setup-for-work-orders/fault-management.md)主题。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]