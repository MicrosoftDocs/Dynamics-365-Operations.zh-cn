---
title: 150% 余额递减法
description: 本文提供了 150% 余额递减法折旧方法的概览。
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f3bccb9d64851901d43b55887bb66c9b1b4e5a70
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870211"
---
# <a name="150-percent-reducing-balance-depreciation"></a>150% 余额递减法

[!include [banner](../includes/banner.md)]

本文提供了 150% 余额递减法折旧方法的概览。

如果您设置固定资产折旧模板并在 **折旧模板** 页面上的 **方法** 字段中选择 **150% 余额递减法**，已分配此折旧模板的固定资产将在每个折旧期间按相同的百分比进行折旧。 此百分比按资产的使用年限进行计算。 例如，如果资产的使用年限为 5 年，则该百分比按 30% (150% ÷ 5) 计算。 

要设置 150% 余额递减法，您还必须在 **折旧模板** 页面上的 **折旧年份** 字段和 **期间频率** 字段中选择选项。 **期间频率** 字段中提供的选项因 **折旧年份** 字段中所选的值而异。

## <a name="selection-of-depreciation-year"></a>折旧年份的选择
您可以在 **折旧模板** 页上的 **折旧年份** 字段中选择 **日历** 或 **会计**。 

默认值是 **日历**。 您的选择将决定 **期间频率** 字段中可用的选项。 此字段定义整个日历年度的折旧应计过帐日期和金额。

### <a name="calendar"></a>日历

可以保留 **折旧年份** 字段中的默认值，即 **日历**。 

**日历** 选项在每年的 1 月 1 日更新折旧基数。 通常，折旧基数为帐面净值减去残值所得的结果。 在本文后面的示例中，折旧基数是计算列中第一个表达式的分子。 

如果选择 **日历** 作为折旧年份，则 **期间频率** 字段中提供以下选项：

-   **每年** 在 12 月 31 日过帐金额。
-   **每月** 在每个日历月末过帐每月金额。
-   **每季度** 在每个日历季度末（3 月 31 日、6 月 30 日、9 月 30 日和 12 月 31 日）过帐季度金额。
-   **每半年** 在每个日历半年末（6 月 30 日和 12 月 31 日）过帐半年金额。
-   **日常** 通过对每天使用一个交易记录来过帐每日折旧方法的折旧金额。

### <a name="fiscal"></a>会计

如果在 **折旧年份** 字段中选择 **会计**，则 150% 余额递减法将基于用于帐簿中指定的会计日历的会计年度或者在 **分类帐** 页面上选择的会计日历的会计年度进行计算。 会计年度是在 **会计日历** 页上设置的。 

例如，对于会计年度 7 月 1 日至次年 6 月 30 日，折旧计算从 7 月 1 日开始。 会计年度可以长于或短于 12 个月。 对于每个期间，都可以调整折旧。 下一会计年度的长度由 **会计日历** 页面上的期间设置决定。 

如果选择 **会计** 作为折旧年份，则 **期间频率** 字段中提供以下选项：

-   **每年** 在会计年度的最后一天过帐针对会计年度计算的折旧总额。
-   **会计期间** 将过帐为该会计年度计算的折旧总额。 此金额计入在 **会计日历** 页上定义的会计期间。

## <a name="example-of-150-reducing-balance-depreciation"></a>150% 余额递减法的示例

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| 购置成本               | 11,000 |
| Salvage value / 残值                  | 1,000  |
| 折旧基数              | 10,000 |
| 服务年限             | 5      |
| 每年折旧百分比 | 30%    |

150% 余额递减法将 150% 除以使用年限。 用此百分比乘以资产的帐面净值来确定年折旧金额。

| 期间 | 年折旧金额的计算 | 帐面值             | 年末帐面净值 |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| 第 1 年 | (11,000 – 1,000) × 30% = 3,000                | 11,000 – 3,000 = 8,000 | 11,000 – 1,000 – 3,000 = 7,000        |
| 第 2 年 | 7,000 × 30% = 2,100                           | 8,000 – 2,100 = 5,900  | 7,000 – 2,100 = 4,900                 |
| 第 3 年 | 4,900 × 30% = 1,470                           | 5,900 – 1,470 = 4,430  | 4,900 – 1,470 = 3,430                 |

> [!NOTE]
> 通常，当使用 150% 余额递减折旧法计算的金额小于使用直线法计算的金额时，对剩余年限转换到直线法。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
