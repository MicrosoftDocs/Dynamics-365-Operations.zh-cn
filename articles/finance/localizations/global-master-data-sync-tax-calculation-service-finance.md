---
title: 将“税款计算服务”的税务设置同步到 Dynamics 365 Finance
description: 本文介绍如何将税款计算服务中的税务设置主数据同步到 Microsoft Dynamics 365 Finance。
author: EricWangChen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.custom: intro-internal
ms.search.form: TaxIntegration, TaxServiceParameters
ms.openlocfilehash: 315f2b27a64906ca0fc404d704d0b170dbfa48c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283844"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>将“税款计算服务”的税务设置同步到 Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

本文介绍如何将税款计算服务中的税务设置主数据同步到 Microsoft Dynamics 365 Finance。

完成[开始使用税款计算](global-get-started-with-tax-calculation-service.md)中的必需设置步骤后，以下税务设置数据将从税款计算服务自动同步到 Finance。

## <a name="sales-tax-code"></a>销售税代码

| 税款计算服务           | Finance                             |
| --------------------------------- | ----------------------------------- |
| 税码                          | 销售税代码                      |
| Description                       | Name                                |
| 用户输入                        | 结算期间                   |
| 用户输入                        | 分类帐记帐组                |
| 用户输入                        | 销售税币种                  |
| 已配置负税率 | 允许销售税百分比为负 |

## <a name="tax-value"></a>税值

| 税款计算服务 | Finance                   |
| ----------------------- | ------------------------- |
| 开始交易记录日期   | 开始日期                 |
| 结束交易记录日期     | 截止日期                   |
| 最小金额          | 下限             |
| 最大额度          | 上限             |
| 税率                | 值                     |
| 不可扣除比率     | 不可扣除百分比 |

## <a name="tax-limits"></a>税金限制

| 税款计算服务 | Finance           |
| ----------------------- | ----------------- |
| 开始交易记录日期   | 开始日期         |
| 结束交易记录日期     | 截止日期           |
| 最小税额      | 最低销售税 |
| 最大税额      | 最高销售税 |

## <a name="sales-tax-group"></a>销售税组

| 税款计算服务                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| 税务组                                       | 销售税组                            |
| 此税组下的税码                  | 此销售税组下的销售税代码 |
| 此税码被标记为 **免税**         | 豁免                                     |
| 此税码被标记为 **免税**         | 豁免代码                                |
| 此税码被标记为 **是冲销费用** | 冲销费用                             |
| 此税码被标记为 **是销项税**        | 销项税                                    |

## <a name="item-sales-tax-group"></a>物料销售税组

| 税款计算服务             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| 物料税组                      | 物料销售税组                            |
| 此物料税组下的税码 | 此物料销售税组下的销售税代码 |

同步完成后，请继续维护 Finance 中的剩余参数以用于过帐和报告目的。

> [!NOTE]
> 不支持将税务设置从 Finance 同步到税款计算服务。 对于现有的 Finance 环境，请先在税款计算服务中创建税务设置。 然后将设置数据同步回 Finance 环境。
