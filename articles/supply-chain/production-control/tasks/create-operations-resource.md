---
title: 创建运营资源
description: 运营资源执行项目或生产流程的活动。
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2e59b1e6a83d902df98a0b40ee6c572a6567f05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422716"
---
# <a name="create-an-operations-resource"></a>创建运营资源

[!include [banner](../../includes/banner.md)]

运营资源执行项目或生产流程的活动。 此过程显示您如何定义运营资源。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。

1. 转到“资源”。
2. 单击“新建”。
3. 在“资源”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。

## <a name="define-capacity-and-consumption-parameters"></a>定义产能和消耗参数
1. 展开“操作”部分。
2. 在“废料百分比”字段中，输入一个数字。
3. 在“创建类别”字段中，输入或选择一个值。
    * 指定定义如何计算设置成本的成本类别。  
4. 在“运行时间类别”字段中，输入或选择一个值。
    * 指定定义如何计算运行时间成本的成本类别。  
5. 在“质量类别”字段中，输入或选择一个值。
    * 指定定义如何计算基于输出数量的资源成本的成本类别。  
6. 在“产能单位”字段中，选择一个选项。
    * 指定表示运营资源的产能的单位。  
7. 在“产能”字段中，输入数字。
8. 在“效率百分比”字段中，输入数字。
    * 指定您期望的运营资源效率。 效率百分比调整运营资源的生成量，并影响为该资源预留的时间。  
9. 在“操作安排百分比”字段中，输入一个数字。
    * 指定您想要在运营计划中使用的运营资源的最大产能百分比。  
10. 在“有限产能”字段中，选择“是”。
    * 如果运营资源应根据可用的实际产能安排，以及如果应该考虑现有产能保留，将此选项设置为“是”。 如果此选项设置为“否”，则运营资源假定为无限产能，并且可能会超额订购资源。  
11. 在“瓶颈资源”字段选择“是”。

## <a name="define-working-times"></a>定义工作时间
1. 展开“日历”部分。
2. 单击“添加”。
3. 在“日历”字段中，输入或选择一个值。
    * 指定定义资源产能（按小时计算）的工作日历。  
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。

## <a name="define-resource-capabilities"></a>定义资源功能
1. 展开“功能”部分。
2. 单击“添加”。
    * 功能是运营资源执行特定活动的能力。 计划编制引擎通过将每一活动的资源要求与可用运营资源的功能匹配来分配资源。  
3. 在“功能”字段中，输入或选择一个值。
4. 在“水平”字段，输入一个数值。
    * 指定资源处理该功能的熟练程度。  
5. 在“优先”字段，输入一个数字。
    * 指定该功能相关的运营资源的优先级。 在按优先级进行计划编制时，首先选择最高优先级的（数值最小）的运营资源。  

## <a name="assign-resource-to-resource-group"></a>分配资源给资源组
1. 展开“资源组”部分。
2. 单击“添加”。
    * 资源组定义运营资源的站点、生产单位和仓库环境。 运营资源只有在分配至资源组时，以及只有在资源组所在的站点时才可安排计划。  
3. 在“资源组”字段中，输入或选择一个值。
4. 在“输入位置”字段中，输入或选择一个值。
    * 指定运营资源调用物料的仓库位置。  

