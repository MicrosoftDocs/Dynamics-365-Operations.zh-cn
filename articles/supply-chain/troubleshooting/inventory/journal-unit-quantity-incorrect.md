---
title: 单位和单位数量在库存日记帐中不能正常工作
description: 单位和单位数量在库存日记帐中不能正常工作
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475669"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>单位和单位数量在库存日记帐中不能正常工作

## <a name="symptoms"></a>故障特征

在库存日记帐中使用单位和数量时，您可能会遇到以下一个或两个问题：

- 为已发布产品设置转换单位时，在库存日记帐中看不到单位或数量，也无法在库存日记帐中更改单位。
- 您在库存日记帐中看到 **数量** 和 **单位** 字段，但是看不到 **单位数量** 字段。 如果您更改单位、输入数量和过帐日记帐，日记帐仍显示该数量的原始度量单位。

## <a name="resolution"></a>解决方法

若要解决此问题，请按照以下步骤操作。

1. 在 **功能管理** 工作区，请确保 *在库存日记帐中使用度量单位和单位数量* 功能已开启。 此功能会将 **单位** 和 **单位数量** 字段添加到日记帐中。
1. 开启此功能后，通过以下方式使用 **数量**、**单位数量** 和 **单位** 字段：

    - **数量** – 使用为已发布产品定义的默认单位指定数量。 但是，默认单位本身不在此处显示。 如果在默认单位和 **单位** 字段中选择的单位之间设置了转换，**数量** 字段将根据 **单位数量** 和 **单位** 字段中的选择自动更新。
    - **单位数量** – 使用在 **单位** 字段中选择的单位指定数量。
    - **单位** – 在 **单位数量** 字段中选择要应用于值的单位。
