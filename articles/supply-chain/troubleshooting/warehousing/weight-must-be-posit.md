---
title: 重量必须为正
description: 重量必须为正
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924295"
---
# <a name="weight-must-be-positive"></a>重量必须为正

错误代码：WeightMustBePositive

## <a name="symptoms"></a>故障特征

系统将显示以下错误消息：

> 重量必须为正。

## <a name="cause"></a>原因

**毛重** 字段设置为 *0*（零）或负值。

## <a name="resolution"></a>解决方法

要指定重量，请执行以下步骤之一。

- 在 **毛重** 字段中，设置一个值。 然后在下拉列表中选择一个单位。
- 选择 **获取系统重量** 来计算 **毛重** 值。
