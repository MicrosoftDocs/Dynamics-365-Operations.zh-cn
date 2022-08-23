---
title: 其他州供应商的产品 ICMS-DIF 税计算的基数更改
description: 本文介绍在巴西南里奥格兰德州 (RS) 或圣保罗 (SP) 州收到会计单据时的 ICMS-DIF 税务类型计算配置。
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218640"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>其他州供应商的产品 ICMS-DIF 税计算的基数更改（双基数）

本文介绍在巴西南里奥格兰德州 (RS) 或圣保罗 (SP) 州收到会计单据时的 **ICMS-DIF** 税务类型计算配置。

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
    - 在 **边际基数** 字段中，选择 **每行净额**。
    - 定义纳税代码，以便其会计值为 **3**。 这样，启用 **会计帐簿** 模块后，将自动创建调整交易。
    - 在销售税组的配置中，针对 **ICMS-DIF** 销售税代码选择 **销项税** 选项。

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>在双基数 ICMS-DIF 销售税代码的配置中使用增量税率

使用之前描述的设置后，将在双基数规则中计算 **ICMS-DIF** 销售税代码。 但是，标准税率将变为 18%，这与简单基本规则中的 6% 的税率不同。 此差异会导致会计单据和税务申报中出现不一致问题。 从 Microsoft Dynamics 365 Finance 版本 10.0.29 开始，您可以在 **功能管理** 中启用 **（巴西）使用 ICMS-DIF 税码为双基数情况配置增量税率** 功能，以消除不一致。

- 除了完成上一节中的步骤外，请在 **税上税** 字段中选择 **ICMS 12** 销售税代码。
- 将 **ICMS-DIF** 销售税代码的税率设置为 18%。 **百分比/金额** 字段将标准税率显示为 6%。

> [!NOTE]
> 必须在同一销售税组中分配 **ICMS-DIF** 和 **ICMS 12** 销售税代码。

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>其他州中非纳税人消费者 (DIFAL) 的产品 ICMS-DIF 税计算中的基数更改（双基数）

在 **功能管理** 中启用 **（巴西）销售交易中的 ICMS-DIFAL 双基数计算** 功能，以针对与其他州中的非纳税人消费者进行的贸易支持 ICMS-DIF 基数更改。 示例 ICMS-DIF 销售税代码在销售订单和普通发票交易中生效。

在 **功能管理** 中启用 **（巴西）IPI 案例的 ICMS-DIFAL 双基数计算** 功能，以支持与其他州中的非纳税人消费者进行贸易也应缴纳工业产品税 (IPI) 的情况。 ICMS-DIFAL 税基数中将确认并应用 IPI 销售税代码的税额。

- 在销售订单或普通发票的标头上，在 **会计信息** 快速选项上，**最终用户** 选项必须设置为 **是**。
- 在采购订单或供应商发票的标头上，在 **会计信息** 快速选项上，**使用和消耗** 选项必须设置为 **是**。
