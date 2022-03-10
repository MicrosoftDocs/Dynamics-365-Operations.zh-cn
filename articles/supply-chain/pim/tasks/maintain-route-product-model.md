---
title: 维护产品模型路线
description: 该过程的运行要求有现有的产品配置模型。
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88df8b867ac7f354417add0462e7999747333451
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577256"
---
# <a name="maintain-route-for-a-product-model"></a>维护产品模型路线

[!include [banner](../../includes/banner.md)]

该过程的运行要求有现有的产品配置模型。 该过程使用演示公司 USMF 的高端扬声器模型向您介绍流程步骤。

## <a name="add-a-route-operation"></a>添加一个路线运营

1. 转到 **产品信息管理 \> 产品 \> 产品配置模型**。
1. 在列表中，找到并选择所需记录。
    * 为此次练习选择“高端扬声器模型”。  
1. 在列表中，选择所选择行中的链接。
1. 展开 **工艺路线工序** 部分。
1. 选择 **添加**。
1. 在 **名称** 字段中，键入一个值。
1. 在 **描述** 字段中，键入一个值。
1. 选择 **保存**。

## <a name="enter-route-operation-details"></a>输入路线运营详细信息

1. 选择 **工艺路线工序详细信息**。
1. 在 **工序** 字段中，输入或选择一个值。
1. 在 **工序编号** 字段中，输入一个数字。
    * 工序编号确定工艺路线序列。  
    * 工艺路线工序的每个属性可获得静态值或映射到一个属性。 映射到属性会导致值设为配置的一部分。  
1. 在 **工艺路线组** 字段中，输入或选择一个值。
    * 工艺路线组确定成本、消耗量和设置的重要行为。  
1. 选择 **设置** 选项卡。
1. 选择 **时间** 选项卡。
1. 在 **处理数量** 字段中，输入一个数字。
    * 确定一次操作中将处理的量。  
1. 在 **小时/时间** 字段中，输入一个数字。
    * 输入时间比。  
1. 选择 **设置** 复选框。
1. 在 **运行时间** 字段中，输入一个数字。
    * 确定您指定的数量的处理时间。  
1. 选择 **资源要求** 选项卡。
1. 选择 **添加**。
1. 在列表中，标记所选的行。
1. 在 **要求类型** 字段中，选择一个选项。
    * 确定是否要指定必须拥有的特定资源或功能。  
1. 在 **要求** 字段中，输入或选择一个值。
1. 选择 **确定**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]