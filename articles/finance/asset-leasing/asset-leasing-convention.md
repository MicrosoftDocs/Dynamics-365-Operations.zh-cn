---
title: 资产租赁惯例
description: 文主题介绍租赁资产的惯例。
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7072c34ccbffc6bf135f55fd594cac4d9ea5a463
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237508"
---
# <a name="asset-leasing-conventions"></a>资产租赁惯例

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

文主题介绍租赁资产的惯例。 租赁惯例用于确定租赁帐簿的开始日期。 如果租赁惯例设置为 **否**，开始日期与租赁的开始日期相同（即 **租赁开始日期** 字段的值）。 如果租赁惯例设置为 **整月**，开始日期则是租赁开始日期所在月份的第一天。

开始日期确定负债摊销和资产折旧计划的期间的开始日期。 利息支出和折旧支出在相应计划的期间结束日期过帐。 初始确认和调整日记帐条目在开始日期过帐。

> [!NOTE]
> 租赁惯例功能必须通过“功能管理”打开。 在 **功能管理** 工作区中，找到并选择名为 **资产租赁的租赁惯例** 功能，然后选择 **立即启用**。

租赁惯例将被分配到租赁资产帐簿的设置。

要查看或分配租赁惯例，请按照下列步骤操作。

1. 转到 **资产租赁 \> 设置 \> 租赁帐簿**。
2. 在 **租赁惯例** 字段中，选择以下值之一。

    | 租赁惯例 | 说明 |
    |--------------------|-------------|
    | None               | 负债摊销和资产折旧计划从租赁的开始日期开始，因为开始日期等于租赁的开始日期。 结束日期是一个月后。 此租赁惯例不保证利息会在每个月的最后一天过帐。 |
    | 全月         | 对于开始日期在当月任何时间发生的租赁，负债摊销和资产折旧计划在该月的第一天开始计入费用。 此租赁惯例可确保在每个整月的最后一天计算利息。 |

3. 选择 **保存**。

租赁创建后，将根据为租赁输入的开始日期和为帐簿指定的租赁惯例自动输入每个帐簿的开始日期。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]