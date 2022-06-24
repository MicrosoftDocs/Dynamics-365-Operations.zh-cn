---
title: 设置自动过帐的默认描述
description: 本文说明如何设置用于介绍自动过帐到总帐的会计条目的默认文本。 您可以使用自由格式的文本或通过选择固定变量设置默认描述文本。
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71982a7d5b1bb08d3e238646ea0b15f17260bdcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904490"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>设置自动过帐的默认描述

[!include [banner](../includes/banner.md)]

本文说明如何设置用于介绍自动过帐到总帐的会计条目的默认文本。 您可以使用自由格式的文本或通过选择固定变量设置默认描述文本。

> [!NOTE]
> 对于一些国家或地区的某些交易记录类型，您还可以包括与这些交易记录类型相关的字段的文本。 有关交易记录类型以及国家和地区的列表，请参阅本文后面的[可选：向默认描述添加其他文本](#optional-add-other-text-to-default-descriptions)一节。

## <a name="set-up-default-descriptions"></a>设置默认描述

1. 转至 **组织管理** \> **设置** \> **默认描述**。
2. 在操作窗格上，选择 **新建**。
3. 在 **描述** 字段中，选择要为其创建默认描述的交易记录类型。
4. 在 **语言** 字段中，选择此描述适用的语言。
5. 在 **文本** 字段中，输入默认描述。 您可以在该字段中键入文本，也可以使用以下一个或多个自由文本变量：

    - **%1** – 添加交易记录日期。
    - **%2** – 添加对应于正在过帐到总帐的文档类型的标识符。 例如，对于与发票相关的交易记录类型，变量 **%2** 添加发票编号。
    - **%3** – 添加与正在过帐到总帐的文档类型相关的标识符。 例如，对于与发票相关的交易记录类型，变量 **%3** 添加客户帐号。

## <a name="optional-add-other-text-to-default-descriptions"></a>可选：向默认描述添加其他文本

对于一些国家或地区的某些交易记录类型，默认描述可以在您的数据中包括来自与这些交易记录类型相关的字段的文本。 以下列表显示了此选项适用的交易记录类型以及国家和地区。

**交易记录类型**

您可以向与以下单据类型相关的交易记录类型的默认描述中添加其他文本：

- 客户发票
- 客户贷方通知单
- 客户现金支付
- 供应商付款
- 销售订单
- 采购订单
- 库存日记帐
- 主计划 (MRP)
- 固定资产

**国家和地区**

此选项仅在以下国家和地区可用：

- 巴西
- 中国
- 捷克共和国
- 东欧
- 匈牙利
- 印度
- 日本
- 立陶宛
- 拉脱维亚
- 波兰
- 俄罗斯

### <a name="add-text-to-default-descriptions"></a>向默认描述添加其他文本

完成本文前面的[设置默认描述](#set-up-default-descriptions)一节中的步骤后，执行以下步骤，以向默认描述添加其他文本。

1. 在 **参数** 快速选项卡上，选择 **添加**。
2. 在 **引用表** 字段中，选择要从其中将参数数据添加到描述的数据库表。
3. 在 **引用字段** 字段中，选择要从其中将参数数据添加到描述的字段。
4. 重复执行第 1 步到第 3 步，以添加更多参数。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
