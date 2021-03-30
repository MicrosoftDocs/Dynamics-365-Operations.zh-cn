---
title: 维护产品模型路线
description: 该过程的运行要求有现有的产品配置模型。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13bbdc706280317c5a1ab7fb21c9585f1c7d48ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247782"
---
# <a name="maintain-route-for-a-product-model"></a>维护产品模型路线

[!include [banner](../../includes/banner.md)]

该过程的运行要求有现有的产品配置模型。 该过程使用演示公司 USMF 的高端扬声器模型向您介绍流程步骤。


## <a name="add-a-route-operation"></a>添加一个路线运营
1. 单击“产品变型模型定义”。
2. 单击“产品配置模型”。
3. 在列表中，找到并选择所需记录。
    * 为此次练习选择“高端扬声器模型”。  
4. 在列表中，单击所选行中的链接。
5. 展开“路线运营”部分。
6. 单击“添加”。
7. 在“名称”字段中，键入一个值。
8. 在“描述”字段中，键入一个值。
9. 单击“保存”。

## <a name="enter-route-operation-details"></a>输入路线运营详细信息
1. 单击“路线运营详细信息”。
2. 在“运营”字段中，输入或选择一个值。
3. 在“工序 编号 字段中，输入一个数字。
    * 工序编号确定工艺路线序列。  
    * 工艺路线工序的每个属性可获得静态值或映射到一个属性。 映射到属性会导致值设为配置的一部分。  
4. 在“路线组”字段中，输入或选择一个值。
    * 工艺路线组确定成本、消耗量和设置的重要行为。  
5. 单击“设置”选项卡。
6. 单击“时间”选项卡。
7. 在“进程数量“ 字段中，输入一个数字。
    * 确定一次操作中将处理的量。  
8. 在“小时/时间”字段中，输入一个数字。
    * 输入时间比。  
9. 选择“设置”复选框。
10. 在“运行时间”字段中，输入一个数字。
    * 确定您指定的数量的处理时间。  
11. 单击“资源要求”选项卡。
12. 单击“添加”。
13. 在列表中，标记所选的行。
14. 在“要求类型”字段中，选择一个选项。
    * 确定是否要指定必须拥有的特定资源或功能。  
15. 在“要求”字段中，输入或选择一个值。
16. 单击“确定”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]