---
title: 故障管理
description: 本主题介绍资产管理中的故障管理。
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c87bfa057fd2808551674f2acb9d654ad47e9a42
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825654"
---
# <a name="fault-management"></a>故障管理

[!include [banner](../../includes/banner.md)]

 

在资产管理中，可使用故障设计器为资产故障设置故障特征、故障区域和故障类型。 这样就可以管理为资产检测到的故障。 此外，还可以为工作订单登记故障成因和有关解决故障的建议。

故障登记和管理流程包含以下步骤。

1. 创建资产类型可能出现的故障特征、故障区域和故障类型的列表。
2. 在故障设计器中，设置特征、故障区域和故障类型。

下面这些示例可帮助您理解故障特征、故障区域和故障类型之间的区别。

**故障特征：**

- 电压不平衡s
- 短路
- 噪声
- 泄漏
- 振动

**故障区域：**

- 电
- 机械
- 水力
- 气动

**故障类型：**

- 主定子绕组故障
- 二级管故障
- 绕组脏
- 发电机有缺陷
- 传感器有缺陷

## <a name="create-fault-symptoms"></a>创建故障特征

执行以下步骤创建可在故障设计器中使用的特征的列表。

1. 选择 **资产管理** \> **设置** \> **故障** \> **故障特征**。
2. 选择 **新建** 创建记录。
3. 在 **故障特征** 字段中，输入故障特征的名称。
4. 在 **描述** 字段中，输入描述。
5. 选择 **保存**。

## <a name="create-fault-areas"></a>创建故障区域

执行以下步骤创建可在故障设计器中使用的区域或位置的列表。

1. 选择 **资产管理** \> **设置** \> **故障** \> **故障区域**。
2. 选择 **新建** 创建记录。
3. 在 **故障区域** 字段中，输入故障区域的名称。
4. 在 **描述** 字段中，输入描述。
5. 选择 **保存**。

## <a name="create-fault-types"></a>创建故障类型

执行以下步骤创建可在故障设计器中使用的故障类型的列表。

1. 选择 **资产管理** \> **设置** \> **故障** \> **故障类型**。
2. 选择 **新建** 创建记录。
3. 在 **故障类型** 字段中，输入故障类型的名称。
4. 在 **描述** 字段中，输入描述。
5. 选择 **保存**。

## <a name="set-up-the-fault-designer"></a>设置故障设计器

可以在故障设计器中为资产类型设置故障数据。

1. 选择 **资产管理** \> **设置** \> **故障** \> **故障设计器**。
2. 在左窗格中，选择要为其设置故障记录的资产的类型。
3. 在 **故障特征** 快速选项卡上，选择 **添加行**，然后在 **故障特征** 字段中选择故障特征。
4. 在 **故障区域** 快速选项卡上，选择 **添加行**，然后在 **故障区域** 字段中选择故障区域。
5. 在 **故障类型** 快速选项卡上，选择 **添加行**，然后在 **故障类型** 字段中选择故障类型。
6. 若要快速创建所选资产类型的所有现有故障特征、区域和类型的组合，请选择 **创建故障组合**。 如果已经添加了大量故障特征、区域和类型，此功能非常有用。 相比手动创建新行，删除与资产类型无关的任何组合更容易。

    > [!NOTE]
    > 若要将故障特征、区域和类型的设置从一个资产类型复制到所选资产类型，请选择 **从资产类型复制**。

7. 选择 **保存** 以保存您的更改。

![故障设计器页面](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>创建故障成因

执行以下步骤，以便创建可添加到工作订单或维护请求的已知故障成因的列表。

1. 选择 **资产管理** \> **设置** \> **故障** \> **故障成因**。
2. 选择 **新建** 创建记录。
3. 在 **故障成因** 字段中，输入故障成因的名称。
4. 在 **描述** 字段中，输入描述。
5. 选择 **保存**。

## <a name="create-fault-remedies"></a>创建故障补救措施

执行以下步骤，以便创建可添加到工作订单或维护请求的补救措施和修复建议的列表。

1. 选择 **资产管理** \> **设置** \> **故障** \> **故障补救措施**。
2. 选择 **新建** 创建记录。
3. 在 **故障补救措施** 字段中，输入故障补救措施的名称。
4. 在 **描述** 字段中，输入描述。
5. 选择 **保存**。

> [!NOTE]
> 可根据需要更改故障特征、区域、类型、成因和补救措施的名称。 将在关联的故障登记中自动体现名称的变化。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]