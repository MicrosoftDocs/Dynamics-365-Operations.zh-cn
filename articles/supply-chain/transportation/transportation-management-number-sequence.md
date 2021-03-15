---
title: 运输管理编号规则
description: 此主题介绍如何设置运输管理的编号规则。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b7bb6c9338808828a41801a85a1b93b420e9c75b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004722"
---
# <a name="transportation-management-number-sequence"></a>运输管理编号规则

[!include [banner](../includes/banner.md)]

使用运输管理模块中的 **编号规则** 页来设置不同专业编号。 承运人使用专业编号来组织和跟踪每个装运的进度。

## <a name="create-a-number-sequence-for-a-pro-number"></a>创建专业编号的编号规则

要为专业编号创建编号规则，请执行以下操作：

1. 转到 **运输管理 \> 设置 \> 承运人 \> 编号规则**。
1. 选择 **新建** 创建新编号规则。
1. 为编号规则输入唯一 ID 和描述名称。
1. 在 **编号规则类型** 字段中，*专业编号* 是唯一选项。
1. 在 **校验位** 字段中，*校验位* 是唯一选项，设置为通用引擎。
1. 在 **序列** 快速选项卡上，提供有关序列的信息。
1. 关闭该页面。

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a>将编号规则链接到装运承运人

要将编号规则链接到承运人，请执行以下操作：

1. 转到 **运输管理 \> 设置 \> 承运人 \> 装运承运人**。
1. 选择装运承运人。
1. 选择 **编辑**。
1. 在 **概览** 快速选项卡上，在 **专业编号规则** 字段中选择一个选项。
1. 关闭该页面。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]