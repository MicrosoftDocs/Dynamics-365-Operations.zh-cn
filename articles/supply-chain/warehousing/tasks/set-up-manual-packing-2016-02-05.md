---
title: 设置手动包装（2016 年 2 月和 2016 年 5 月）
description: 包装流程允许您验证并将产品包装到集装箱中。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67e1e99b479752a027c60a878c57bd35d4219981
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017545"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a>设置手动包装（2016 年 2 月和 2016 年 5 月）

[!include [banner](../../includes/banner.md)]

包装流程允许您验证并将产品包装到集装箱中。 在此流程中，仓库工作人员从存储位置的拣选产品并将它们移到包装站，他们在包装站检查物料数量和类型，并将其分配到相应的集装箱。 在完全包装容器时，可以封闭它并将其移至出货台，然后产品可进行装运。 该程序适用于 USMF 演示公司。 此过程仅适用于 Dynamics 365 for Operations 的 2016 年 2 月和 2016 年 5 月的版本。


## <a name="set-up-location-profiles"></a>设置位置配置文件
1. 转到“仓库管理”>“设置”>“仓库”>“位置模板”。
2. 单击“新建”。
    * 位置配置文件可用于包装站，并包含位置信息和规则。  
3. 在“位置模板 ID”字段中，键入一个值。
4. 在“名称”字段中，键入一个值。
5. 在“位置格式”字段中，输入或选择一个值。
6. 在“位置类型”字段中，输入或选择一个值。
7. 选择“允许混合物料”字段中的“是”。
8. 选择“允许混合库存状态”字段中的“是”。
9. 选择“覆盖批处理天数的规则”字段中的“是”。
10. 关闭该页面。

## <a name="set-up-warehouse-management-parameters"></a>设置仓库管理的参数 
1. 转到“仓库管理”>“设置”>“仓库管理参数”。
2. 单击“包装”选项卡。
3. 在“包装库位的模板 ID”字段中，输入或选择一个值。
    * 选择要用于包装的位置配置文件。  
4. 关闭该页面。

## <a name="set-up-container-types"></a>设置集装箱类型
1. 转到“仓库管理”>“设置”>“集装箱”>“集装箱类型”。
2. 单击“新建”。
    * 您可以定义要使用的集装箱类型： 您可以指定集装箱的物理维度，包括皮重、最大重量、最大体积、长度、宽度和重量。  属性是允许您在集装箱类型添加额外维度的自定义字段。     
3. 在“集装箱类型代码”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“皮重”字段中，输入一个数字。
6. 在“最大重量”字段中，输入一个数字。
7. 在“体积”字段中，输入一个数字。
8. 在“长度”字段中，输入一个数字。
9. 在“宽度”字段中输入数字。
10. 在“高度”字段中输入数字。
11. 单击“保存”。
12. 关闭该页面。

## <a name="set-up-packing-profiles"></a>设置包装模板
1. 转到“仓库管理”>“设置”>“包装”>“包装模板”。
2. 单击“新建”。
3. 在“包装模板 ID”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“集装箱封闭模板 ID”字段中，输入或选择一个值。
    * 集装箱封闭模板 ID 是可选的，是此包装模板的默认封闭集装箱模板。  
6. 在“集装箱 ID 模式”字段中，选择一个选项。
    * 此选项确定在创建集装箱时集装箱 ID 是否自动生成，或是否手动创建集装箱 ID。  
7. 在“集装箱类型”字段中，输入或选择一个值。
    * 默认情况下，在创建新集装箱时，将使用集装箱类型。  
8. 选择“在集装箱封闭时自动创建集装箱”复选框。
9. 单击“保存”。
10. 关闭该页面。

## <a name="set-up-container-closing-profiles"></a>设置集装箱封闭模板
1. 转到“仓库管理”>“设置”>“集装箱”>“集装箱封闭模板”。
    * 集装箱封闭模板定义在集装箱封闭时发生的情况。 您可以设置多个封闭集装箱模板。       
2. 单击“新建”。
3. 在“集装箱封闭模板 ID”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“显示时间”字段中，选择一个选项。
    * 指定在封闭集装箱或确认装运时是否显示。 请注意，显示要求运输管理。 显示必须在运输引擎中实施以正常工作。  
6. 在“仓库”字段中，输入或选择一个值。
7. 在“最终装运的默认位置”字段中，输入或选择一个值。
    * 这将是封闭集装箱后产品将移到的位置。 此位置必须具有在仓库参数中定义的位置模板。  
8. 在“重量单位”字段中，输入或选择一个值。
9. 单击“保存”。

