---
title: 物料的使用位置
description: 本文介绍如何在资产管理中获取有关物料使用位置的概览。
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5232b7554f542fd183d3002e6d94ca49bfde06ec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861006"
---
# <a name="item-where-used"></a>物料的使用位置

[!include [banner](../../includes/banner.md)]

 

可对特定物料进行计算，以便在资产管理中获取有关物料使用位置的概览。 结果显示物料在其生命周期内的使用上下文。 **物料使用位置** 页可以从资产管理主菜单打开，也可以从以下页访问：

- [资产 BOM](../objects/object-BOM.md)

- [资产类型默认的备件](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [维护作业类型类别和维护工作类型、维护作业类型变型、维护作业贸易和维护清单](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [维护预告](../work-orders/maintenance-forecasts.md)

- [采购](../work-orders/procurement.md)

- [工作订单采购](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>创建物料使用位置计算

1. 单击 **资产管理** > **查询** > **物料使用位置**，或在上面介绍的页面之一中选择 **物料使用位置** 按钮。

2. 在 **物料使用位置** 对话框的 **物料编号** 字段中，选择要为其创建计算的物料。

3. 可使用 **级别** 字段指示要与功能位置有关的物料行的详细程度。 

    例如，如果在此字段中插入数字“1”，并且采用了多级别功能位置结构，则在最上级别显示功能位置的所有物料行。 因此，可以从较低级别的功能位置开始叠加行中的关联/数量。 
    
    如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有物料行。

4. 在 **包括** 部分中，在要包括到计算中的切换按钮上选择“是”。

5. 单击 **确定** 开始计算。

6. 在 **物料使用位置** 选项卡上，选择 **分组依据** 按钮可以显示所需计算详细程度。 将突出显示所选 **分组依据** 按钮。 单击按钮将其激活或停用。

7. 如果要显示与物料关联的维度，请单击 **显示维度**，然后选择要显示的维度。

## <a name="example"></a>示例

在下面的屏幕截图中，可以看到编号为“1000”的物料的物料使用位置计算的示例。

![使用位置计算的物料的示例。](media/12-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]