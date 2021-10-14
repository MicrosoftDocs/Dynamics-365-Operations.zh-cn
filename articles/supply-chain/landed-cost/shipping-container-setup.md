---
title: 装运集装箱
description: 本主题介绍如何为登陆成本模块设置装运集装箱。
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 4759faa4882bb559221708fb31e969bff12ebb0b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568751"
---
# <a name="shipping-container-setup"></a>装运集装箱设置

[!include [banner](../../includes/banner.md)]

本主题介绍如何为 **登陆成本** 模块设置装运集装箱。

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>设置装运集装箱类型

装运集装箱类型定义在装运和航行中可以使用的装运集装箱类型。

要使用装运集装箱类型，转到 **登陆成本 \> 集装箱设置 \> 装运集装箱类型**。 您可以在那里查看、添加和删除集装箱类型的记录。 下表说明了可用于每个记录的字段。

| 字段 | 说明 |
|---|---|
| 装运集装箱类型 | 为装运集装箱类型输入唯一标识名称/编号。 |
| 说明 | 输入装运集装箱类型的描述。 |
| 体积 | 输入此类型的装运集装箱允许的最大体积。 |
| 粗细 | 输入此类型的装运集装箱允许的最大重量。 |
| 可退 | 指定此类型的装运集装箱是否可以在航行中使用后退还给供应商。 如果此选项设置为 *是*，将此类型的装运集装箱退回到始发港口可能需要支付额外成本。 |

## <a name="set-up-shipping-containers"></a>设置装运集装箱

您可以使用装运集装箱记录来识别您在航行中使用的每个集装箱。 创建航行时，您可以在您在此处定义的所有装运集装箱记录的列表中为航行选择特定集装箱。 如果您的公司有自己的装运集装箱，此功能尤其有用。

您不必为仅使用一次的装运集装箱输入装运集装箱编号。 而是可以在创建航行时添加装运集装箱编号。

装运集装箱记录仅在登陆成本中使用。 它们在标准 **运输管理** 模块 (TMS) 中不可用。

要使用装运集装箱，转到 **登陆成本 \> 集装箱设置 \> 装运集装箱**。 您可以在那里查看、添加和删除装运集装箱的记录。 下表说明了可用于每个记录的字段。

| 字段 | 说明 |
|---|---|
| 装运集装箱 | 为装运集装箱输入唯一标识名称/编号。 |
| 装运集装箱类型 | 选择装运集装箱的类型。 有关详细信息，请参阅本主题前面的[设置装运集装箱类型](#shipping-container-types)一节。 |

> [!NOTE]
> - 装运集装箱设置是可选的。 通常，仅当您的公司有自己的装运集装箱或经常重复使用相同的装运集装箱时，您才会使用它。
> - 不会为装运集装箱编号计算校验位。

## <a name="set-up-unit-types"></a><a name="unit-types"></a>设置单位类型

单位类型为装运集装箱设定额外的分组和标识方法。 单位类型通常用于标识包装货物的集装箱的类型，如托盘或桶。 在 **所有装运集装箱** 页上设置集装箱时，您可以选择单位类型。

单位类型仅在登陆成本中使用。 它们在 TMS 中不可用。

要使用单位类型，转到 **登陆成本 \> 集装箱设置 \> 单位类型**。 您可以在那里查看、添加和删除单位类型的记录。 下表说明了可用于每个记录的字段。

| 字段 | 说明 |
|---|---|
| 单位类型 | 为单位类型输入唯一标识名称/编号。 |
| 说明 | 输入单位类型的描述。 |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>设置冷冻类型

冷冻类型为装运集装箱（通常是冷藏集装箱）设定额外的分组和标识方法。 在 **所有装运集装箱** 页上设置集装箱时，您可以选择冷冻类型。

要使用冷冻类型，转到 **登陆成本 \> 集装箱设置 \> 冷冻类型**。 您可以在那里查看、添加和删除冷冻类型的记录。 下表说明了可用于每个记录的字段。

| 字段 | 说明 |
|---|---|
| 冷冻类型 | 为冷冻类型输入唯一标识名称/编号。 |
| 说明 | 输入冷冻类型的描述。 |
