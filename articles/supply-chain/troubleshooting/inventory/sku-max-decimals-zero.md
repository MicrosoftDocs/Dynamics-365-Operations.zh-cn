---
title: 库存单位的最大小数位数为 0
description: 当您尝试过帐库存交易记录或库存预留时，收到以下错误：“库存单位的最大小数位数为 0”。
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
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475727"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>库存单位的最大小数位数为 0


## <a name="symptoms"></a>故障特征

尝试过帐库存交易记录或库存预留时，收到以下错误消息：

> 库存单位的最大小数位数为 0。

当库存交易数量被指定为字段支持的精度级别以下的十进制值时，会发生此问题。 例如，为库存交易指定了数量 *0.5*，但仅支持整数数量。 因此，值应为 *1*，而不是 *0.5*。

## <a name="resolution"></a>解决方法

1. 在 SQL Server 实例上运行以下脚本来舍入库存交易中的数量。 此脚本将更正 **inventTrans** 表中的值。

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. 在 **修复错误** 选项打开时运行现有量一致性检查。 此检查将更正 **inventSum** 表中的值。

> [!IMPORTANT]
> 强烈建议您根据环境的需要仔细编辑脚本，在测试环境中进行测试，然后在生产环境中运行脚本之前检查结果数据。
