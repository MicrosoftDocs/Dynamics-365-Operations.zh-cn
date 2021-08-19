---
title: 按时间顺序对文件和凭证编号
description: 本主题说明如何为适用的单据和相关凭证设置和使用时间顺序编号。
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ced09fb4be49dbfd10dac9f9ece86372d38e854460c7ca6cd72922c64ac7cce4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724127"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>按时间顺序对文件和凭证编号

[!include [banner](../includes/banner.md)]


在某些国家/地区，法律要求按时间顺序对文件和相关凭证编号。 时间顺序必须受期间支持。 属于较早期间的所有编号必须小于属于较晚期间的编号。 为了满足此要求，实现了按时间顺序编号的功能。 本主题说明如何为适用的单据和相关凭证配置和使用时间顺序编号。

## <a name="prerequisites"></a>先决条件

在“功能管理”工作区中，开启 **按时间顺序编号** 功能： 有关更多信息，请参见[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。

## <a name="configure-chronological-numbering"></a>配置按时间顺序编号

按时间顺序编号会影响以下单据。

**应收账款**
- 客户账单
- 客户账单凭证
- 销售贷方通知单
- 销售贷方通知单凭证
- 普通账单
- 普通账单凭证
- 普通贷方通知单
- 普通贷方通知单凭证
- 装箱单
- 装箱单凭证
- 装箱单更正凭证
- 利息单凭证
- 催款单凭证

**应付帐款**
- 账单凭证
- 贷方通知单凭证
- 物料收货凭证

**项目管理**
- 账单
- 账单凭证
- 贷方通知单
- 贷方通知单凭证 

### <a name="define-number-sequences"></a>定义编号规则

要定义编号规则，转到 **组织管理** > **编号规则** > **编号规则**。 您可以根据需要定义任意数量的编号规则，以覆盖所需单据的受影响期间。 

为每个编号规则指定一个公司。 必须定义编号规则的细分，让它们为期间提供时间顺序。 例如，细分名称可以包含标识特定期间的特殊前缀。

![编号规则设置。](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>配置编号规则组

要配置编号规则组，转到 **应收帐款** > **设置** > **应收帐款参数**。 在 **编号规则** 选项卡上，根据需要定义任意数量的编号规则组以覆盖受影响的期间。 

对于每个组，在 **引用** 部分，选择其中一个受支持的单据引用，在 **编号规则代码** 字段中，引用先前为相关期间创建的编号规则。

![编号规则组设置。](media/chrono-num-sequence-group.jpg)

同样，在 **应付帐款** 和 **项目管理和会计** 模块中配置编号规则组。

### <a name="configure-number-sequence-groups-chronology"></a>配置编号规则组的时间顺序

要配置编号规则组的时间顺序，转到 **组织管理** > **编号规则** > **时间顺序编号规则组**。 定义编号规则组的适用条件。

![时间顺序编号设置。](media/chrono-num-sequence-group-period.jpg)

| 字段            | 说明                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 生效日期  | 编号规则组适用性的开始日期。 |
| 到期日期      | 编号规则组适用性的结束日期。 如果不应用结束日期，选择 **从不**。 |
| 编号规则组 | 将用于在期间内生成单据编号的编号规则组。 |
| 原始编号规则组 | 此编号规则组代码用于在单据已分配了特定的 *永久* 编号规则组的情况下进行其他筛选。 空值被视为特定值。 如果您需要忽略初步分配的组，请为此设置使用 **默认** 选项。 |
| 默认值 | 如果打开，系统将忽略初步分配的单据编号规则组，仅使用期间开始和结束日期进行适用性分析。 如果关闭，系统将使用完整组合 **生效日期** + **到期日期** + **原始编号规则组** 进行选择。 |

## <a name="document-posting"></a>单据过帐
当您过帐单据时，会根据单据的过帐日期将适当的编号规则组分配给该单据，然后根据检测到的编号规则将该编号规则组用于生成单据编号。 系统将提供有关编号规则组分配的消息。

![单据编号。](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> 对于有些国家/地区，已经为单据编号实现了特定逻辑。 在这种情况下，国家/地区特定的逻辑将替代 **按时间顺序编号** 功能。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
