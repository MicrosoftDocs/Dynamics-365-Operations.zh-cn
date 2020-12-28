---
title: 固定资产折旧惯例
description: 文主题介绍了固定资产的折旧惯例。
author: saraschi2
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4315f70e7959e2576e9b87dfb3898318f47aa46d
ms.sourcegitcommit: 0efa93f11847a2b75d13cd0a49e716c76130ec44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/14/2020
ms.locfileid: "4440914"
---
# <a name="fixed-asset-depreciation-conventions"></a>固定资产折旧惯例

[!include [banner](../includes/banner.md)]

文主题介绍了固定资产的折旧惯例。 折旧惯例用于确定何时和如何为固定资产的购买年份和处置年份计算折旧。

可为固定资产组帐簿的设置指定折旧惯例。 若要查看或分配折旧惯例，请在固定资产的设置区域中选择 **固定资产** 组。 选择 **帐簿** 按钮。 在此情况下，创建固定资产帐簿时，指定的折旧惯例用作默认值。 也可以对单个固定资产帐簿设置折旧惯例。 方法是，在固定资产的设置区域中选择 **帐簿**，然后选择 **固定资产组** 按钮。

| 折旧惯例   | 说明 |
|---------------------------|-------------|
| 无                      | 资产在<strong>已投入使用</strong>日期开始折旧。 |
| 半年                 | 为财产折旧的第一年和最后一年扣减半年的折旧。 回收期内每隔一年扣减全年折旧。 |
| 全月                | <strong>已投入使用</strong>日期在当月任何时间的资产在该月第一天开始折旧。 出于折旧目的，考虑在上个月的最后一天停用资产。 不考虑资产停用的月份的特定日期。 |
| 季度中间               | 若要计算将财产投入服务时的年份的折旧扣减，请将全年的折旧乘以财产投入服务时的季度的百分比，如下表所示。<table><thead><tr><th>季度</th><th>百分比</th></tr></thead><tbody><tr><td>首页</td><td>87.5</td></tr><tr><td>第二</td><td>62.5</td></tr><tr><td>第三</td><td>37.5</td></tr><tr><td>第四</td><td>12.5</td></tr></tbody></table>将从处置资产的季度（或整个折旧的季度）扣减半季度的折旧。 |
| 月中间(月的第 1 天)  | <strong>已投入使用</strong>日期在前半月（1 号到 15 号）的资产在<strong>已投入使用</strong>日期所在月份的第一天开始折旧。 <strong>已投入使用</strong>日期在后半月（16 号到月末）的资产在当月<strong>已投入使用</strong>日期之后的第一天开始折旧。 出于折旧目的，前半月（1 号到 15 号）停用的资产被视为在上月最后一天停用。 出于折旧目的，后半月（16 号到月末）停用的资产被视为在停用月份最后一天停用。 |
| 月中间(月的第 15 天) | 若要为将财产投入使用的年份计算折旧扣减，请将全年的折旧乘以一个分数。 这个分数的分子（即上面的数字）是财产的当前所有使用月数再加上 1/2，即 0.5。 分布（下面的数字）为 12。 如果在回收期结束前处置财产，请使用相同方法计算处置年份的折旧扣减。 |
| 半年(年度开始) | <strong>已投入使用</strong>日期在上半年的资产在当年的第一天开始折旧（即全年折旧）。 <strong>已投入使用</strong>日期在下半年的资产在当年年中开始折旧。 |
| 半年(下一年)     | <strong>已投入使用</strong>日期在上半年的资产在当年的第一天开始折旧（即全年折旧）。 <strong>已投入使用</strong>日期在下半年的资产在下一年的第一天开始折旧。 出于折旧目的，上半年停用的资产被视为在上一年的最后一天停用。 必须冲销或调出当年过帐的所有折旧。出于折旧目的，下半年停用的资产被视为在停用年份最后一天停用。 |
