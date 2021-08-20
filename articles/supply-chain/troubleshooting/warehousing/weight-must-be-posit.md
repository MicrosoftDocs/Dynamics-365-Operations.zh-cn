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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776768"
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
