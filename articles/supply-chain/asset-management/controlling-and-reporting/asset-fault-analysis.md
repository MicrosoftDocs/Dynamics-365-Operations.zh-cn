---
title: 资产故障分析
description: 本文介绍资产管理中的资产故障分析。
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d4503c39a643461c75878c6c7096d824642ad1a2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869769"
---
# <a name="asset-fault-analysis"></a>资产故障分析

[!include [banner](../../includes/banner.md)]

 

在资产管理中，可以分析资产故障登记，以便获取特定期间登记的故障总数的概览。 可以从不同角度分析故障登记，例如，重点关注资产、资产类型、功能位置、故障特征或故障类型。

1. 单击 **资产管理** > **查询** > **资产故障** > **资产故障分析**。

2. 在 **资产故障分析计算** 对话框中，可使用 **级别** 字段指示希望资产故障行与功能位置之间的关系的详细程度。 

    例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有资产故障行，因此，可以从较低级别的功能位置叠加行中的工时。 
        
    如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有资产故障行。

3. 如果要限制搜索，可在 **要包括的记录** 快速选项卡上选择特定资产、故障日期、故障成因和故障补救措施。

4. 单击 **确定** 开始计算。

5. 在 **资产故障分析** 选项卡上，单击一个或多个 **分组依据** 按钮以显示要查看的详细程度。 将突出显示已激活的按钮。 通过单击按钮激活或停用这些按钮。

6. 若要在屏幕上显示所选内容，请单击 **更新计算**。 

>[!NOTE]
>每次您激活或停用 **分组依据** 按钮时，请记住单击 **更新计算** 按钮。 之所以需要执行此操作，是因为重新计算故障概率时要处理大量数据。

## <a name="examples"></a>示例

可以通过多种方法分析故障登记。 本节有五个在分析资产故障登记时，不同数据选择如何提供更多见解和详细信息的示例。

### <a name="group-by-symptoms"></a>按特征分组

在下面的屏幕截图中，将仅选择 **特征** 按钮。

- 已对三种故障特征创建了故障登记：“漏气”、“保险丝熔断”和“设备卡住”。  
- 在 **概率 %** 列中，所有百分比之和为 100%。 在此故障分析中，概率基于所有 **特征** 登记。

![图 1.](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>按特征和时段分组

在下面的屏幕截图中，添加了 **年** 和 **月** 以显示如何查看所选期间内的故障登记。

- 故障特征现在显示为每年/月的登记。  
- 在 **概率 %** 列，如果将每月的所有百分比相加，则总和为 100%。 在此故障分析中，概率基于 **特征** 登记。 如果一个资产有大量行，但是某个行占用的百分比较大，说明需要更仔细地检查某个故障特征以找到方法来限制该故障特征的登记数量。

![图 2.](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>按多个特征和资产分组

资产和资产类型的组合用作下面三个屏幕截图中显示的计算的基础，这将在详细程度增加。  

**按日期分组**、**按资产分组**、**按功能位置分组** 操作窗格组中的按钮和 **故障** 按钮（故障 ID）中通常包含期间或资产关联。 **特征**、**区域**、**类型**、**成因** 和 **补救措施** 按钮是故障管理中用于分析资产故障登记和找出问题区域的分类。  

**按特征、资产和资产类型分组**

在下面的屏幕截图中，添加了 **资产** 和 **资产类型**，以便提供有关故障登记的更多详细信息。

- 故障特征现在已拆分为 **资产** / **资产类型** / **特征** 组合。  
- 在 **概率 %** 列，如果将 **资产** / **资产类型** / **特征** 的所有百分比分别相加，则相加之和分别为 100%。 在此故障分析中，概率基于 **特征** 登记。 如果一个资产有大量行，但是某个行占用的百分比较大，说明需要更仔细地检查某个故障特征以找到方法来限制该故障特征的登记数量。

![图 3.](media/08-controlling-and-reporting.png)

**按两个特征、资产和资产类型分组**

在下面的屏幕截图中，向 **特征**、**资产** 和 **资产类型** 添加了 **区域**，以便提供有关故障登记的更多详细信息。

- 在 **概率 %** 列，如果资产的 **资产** / **资产类型** / **特征** 的所有百分比分别相加，则相加之和分别为 100%。 在此故障分析中，概率基于 **特征** 和 **区域** 的组合。 如果一个资产有大量行，但是某个行占用的百分比较大，说明需要更仔细地检查某个故障区域以找到方法来限制该故障区域的登记数量。  

![图 4.](media/09-controlling-and-reporting.png)

**按三个特征、资产和资产类型分组**

在下面的屏幕截图中，添加了 **类型**，并显示了此示例中最详细的计算。
 
- 在 **概率 %** 列，如果资产的 **资产** / **资产类型** / **特征** 的所有百分比分别相加，则相加之和分别为 100%。 在此故障分析中，概率基于 **特征**、**区域** 和 **类型** 的组合。 如果一个资产有大量行，但是某个行占用的百分比较大，说明需要更仔细地检查某个故障类型以找到方法来限制该故障类型的登记数量。

![图 5.](media/10-controlling-and-reporting.png)


>[!NOTE]
>有关为工人和维护请求创建的所有故障登记的概览，请单击 **资产管理** > **查询** > **资产故障** > **资产故障**。 在 **资产故障** 页中，选择一个资产故障登记，然后展开 **相关信息** 窗格以查看与关联的工作订单或维护请求有关的信息。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]