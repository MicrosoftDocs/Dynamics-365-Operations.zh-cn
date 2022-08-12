---
title: 对齐日期方案
description: 本文提供的示例演示了订阅计费中的对齐日期如何工作。
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 102e3a104be5be287f914172160e95aff65d0b18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872606"
---
# <a name="alignment-date-scenarios"></a>对齐日期方案

本文提供的示例演示了订阅计费中的对齐日期如何工作。

对于这些示例，计费计划的计费详细信息的对齐日期为 2019 年 10 月 31 日。 行的第一个计费明细于 2019 年 10 月 31 日结束，并按比例相应分配。 使用 11 月 11 日的续订开始日期自动续订了该行。

> [!NOTE]
> 年份是相对年份，因为它可能导致对齐日期多于或少于一年。 对于这些示例，在 **定期合同计费参数** 页面上，按比例分配方法设置为 **每月**。 如果设置为 **每日**，则某些部分金额将有所不同。

## <a name="scenario-1-no-alignment"></a>方案 1：无对齐

使用以下数据设置计费计划：

- **开始日期：** 2019 年 5 月 1 日
- **结束日期：** 2024 年 12 月 31 日
- **金额：**$1,000

| 计费开始日期 | 计费结束日期 | 上一个读数 | 当前读数 | 已输入数量 | 可用数量 | 可计费数量 | 单位价格 |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 4/30/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2020 | 4/30/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2021 | 4/30/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2022 | 4/30/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2023 | 4/30/2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>方案 2：已缩短对齐

使用以下数据设置计费计划：

- **开始日期：** 2019 年 5 月 1 日
- **结束日期：** 2024 年 12 月 31 日
- **金额：**$1,000
- **对齐日期：** 2019 年 12 月 31 日

第一个续订金额适用于不到一年的期间。

| 计费开始日期 | 计费结束日期 | 上一个读数 | 当前读数 | 已输入数量 | 可用数量 | 可计费数量 | 单位价格 |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 1/1/2020 | 12/31/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>方案 3：已扩展对齐

使用以下数据设置计费计划：

- **开始日期：** 2019 年 5 月 1 日
- **结束日期：** 2024 年 12 月 31 日
- **金额：**$1,000
- **对齐日期：** 2020 年 12 月 31 日

第一个续订金额适用于超过一年的期间。

| 计费开始日期 | 计费结束日期 | 上一个读数 | 当前读数 | 已输入数量 | 可用数量 | 可计费数量 | 单位价格 |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2020 | | | 1.00 | | 1.00 | 1,666.67 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>方案 4：与其他结束月保持一致

使用以下数据设置计费计划：

- **开始日期：** 2019 年 5 月 1 日
- **结束日期：** 2024 年 10 月 31 日
- **金额：**$1,000
- **对齐日期：** 2019 年 12 月 31 日

> [!NOTE]
> 这种情况并不常见。

| 计费开始日期 | 计费结束日期 | 上一个读数 | 当前读数 | 已输入数量 | 可用数量 | 可计费数量 | 单位价格 |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 1/1/2020 | 12/31/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>方案 5：单个部分年度

使用以下数据设置计费计划：

- **开始日期：** 2019 年 5 月 1 日
- **结束日期：** 2019 年 12 月 31 日
- **金额：**$1,000
- **对齐日期**：2019 年 12 月 31 日

在此方案中，不需要对齐日期。 这种情况对于自动续订很常见。

| 计费开始日期 | 计费结束日期 | 上一个读数 | 当前读数 | 已输入数量 | 可用数量 | 可计费数量 | 单位价格 |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>方案 6：计算的日期

使用以下数据设置支持和续订：

- **覆盖开始日期：** 否
- **支持和续订开始日期：** 下月初
- **发票过帐日期：** 2019 年 6 月 22 日
- **对齐日期：** 2020 年 12 月 31 日

| 计费开始日期 | 计费结束日期 | 上一个读数 | 当前读数 | 已输入数量 | 可用数量 | 可计费数量 | 单位价格 |
|---|---|---|---|---|---|---|---|
| 7/1/2019 | 7/31/2019 | | | 1.00 | | 1.00 | 297.60 |
| 8/1/2019 | 12/31/2020 | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>方案 7：计算的日期和将来过帐

使用以下数据设置支持和续订：

- **覆盖开始日期：** 否
- **支持和续订开始日期：** 下月初
- **发票过帐日期：** 2019 年 6 月 22 日
- **对齐日期：** 2020 年 12 月 31 日

对于此方案，对齐日期更改为 2021 年 12 月 31 日。

| 计费开始日期 | 计费结束日期 | 上一个读数 | 当前读数 | 已输入数量 | 可用数量 | 可计费数量 | 单位价格 |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0.00 |
| 8/1/2019 | 12/31/2020 | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>方案 8：手动日期和多个年份

使用以下数据设置支持和续订：

- **覆盖开始日期：** 是
- **续订开始日期：** 2020 年 7 月 1 日
- **续订结束日期：** 2024 年 12 月 31 日
- **对齐日期：** 2021 年 12 月 31 日

| 计费开始日期 | 计费结束日期 | 上一个读数 | 当前读数 | 已输入数量 | 可用数量 | 可计费数量 | 单位价格 |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0.00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 250.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 250.00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>方案 9：手动日期、多个年份以及不同的结束月份

使用以下数据设置支持和续订：

- **覆盖开始日期：** 是
- **续订开始日期：** 2020 年 7 月 1 日
- **续订结束日期：** 2024 年 10 月 31 日
- **对齐日期：** 2021 年 12 月 31 日

| 计费开始日期 | 计费结束日期 | 上一个读数 | 当前读数 | 已输入数量 | 可用数量 | 可计费数量 | 单位价格 |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0.00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1/1/2022 | 12/31/2022 | | | 1.00 | | 1.00 | 250.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250.00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>方案 10：不按比例对齐

使用以下数据设置支持和续订：

- **覆盖开始日期：** 否
- **发票过帐日期：** 2019 年 6 月 22 日
- **对齐日期：** 2019 年 12 月 31 日

调整续订开始日期和对齐日期，以便两个开始日期都在过帐日期之后。

- **续订开始日期：** 2020 年 1 月 1 日
- **续订结束日期：** 2020 年 12 月 31 日