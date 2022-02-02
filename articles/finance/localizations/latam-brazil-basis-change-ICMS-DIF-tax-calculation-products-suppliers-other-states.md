---
title: 其他州供应商的产品 ICMS-DIF 税计算的基数更改
description: 本主题介绍在巴西南里奥格兰德州 (RS) 或圣保罗 (SP) 州收到会计单据时的 ICMS-DIF 税务类型计算配置。
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 16f78b85567e6d08c588e621119513ff070bf618
ms.sourcegitcommit: 68655c5673aef9892063e5913ffee6bfc3817387
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/21/2022
ms.locfileid: "8016160"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>其他州供应商的产品 ICMS-DIF 税计算的基数更改

本主题介绍在巴西南里奥格兰德州 (RS) 或圣保罗 (SP) 州收到会计单据时的 **ICMS-DIF** 税务类型计算配置。

根据州法律中的规定，收集的 Imposto sobre Circulação de Mercadorias e Serviços (ICMS) 必须遵循以下规则：

*要收集的 ICMS* =（[（*运营金额* - *源 ICMS*）÷（1 - *ICMS % 内部*）] × *ICMS % 内部*）- *源 ICMS 金额*

## <a name="example"></a>示例

RS 州中的巴西公司从 SP 州中的供应商处接收采购的会计单据。 公司必须收集 RS 州（18%）和 SP 州（12%）之间的 ICMS 百分比差异。 但是，必须根据前一规则计算基数。

- **运营金额：** 1,000.00 巴西雷亚尔 (R$ 1,000.00)
- **ICMS 州际：** R$ 120.00
- **RS 州的 ICMS 百分比：** 18%
- **要在 RS 州中收集的 ICMS：** (\[(1,000 – 120) ÷ (1 – 0.18)\] × 0.18 ) – 120 = R$ 73.17 

## <a name="resolution"></a>解决方法

要根据 RS 州的规则计算差异 ICMS (ICMS-DIF)，您必须按以下方式设置销售税代码和销售税组：

1. 创建销售税代码以接收 12% 的 ICMS（针对其他州）。 此代码用于登记供应商的应收税额。
2. 创建销售税代码以收集 ICMS-DIF。 此销售税代码应具有 18% 的百分比金额（适用于您自己的州），以确定 18% 和 12% 之间的差异。 将纳税类型设置为 **ICMS-DIF**。 必须在计算参数中按以下方式定义此销售税代码：

    - 在 **源** 字段中，选择 **总额百分比**。
    - 在 **边际基数** 字段中，选择 **每行净额** 或 **发票余额净额**。
    - 定义纳税代码，以便其会计值为 **3**。 这样，启用 **会计帐簿** 模块后，将自动创建调整交易。
    - 在销售税组的配置中，针对 **ICMS-DIF** 销售税代码选择 **销项税** 选项。
