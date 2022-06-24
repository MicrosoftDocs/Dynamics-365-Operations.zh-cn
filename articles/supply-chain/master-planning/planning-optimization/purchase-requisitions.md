---
title: 采购申请
description: 本文介绍计划优化中如何支持采购申请。
author: t-benebo
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b4dcae11e83748da3ec0368e1ddf47fedf5de23c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867889"
---
# <a name="purchase-requisitions"></a>采购申请

[!include [banner](../../includes/banner.md)]

主计划可以补充已审核的采购申请。 因此，要覆盖采购申请，用户不必使用工作流来创建采购订单。 而可以通过主计划覆盖采购申请。 由于此功能，采购申请可以生成采购订单、转移单或生产订单，具体取决于为相关产品设置的 **计划订单类型** 值。

## <a name="enable-master-plans-to-include-requisitions"></a>让主计划包括申请

要在主计划的覆盖范围计算期间包括申请，请按照以下步骤操作。

1. 转到 **主计划** \> **设置** \> **计划** \> **主计划**。
1. 创建或选择主计划。
1. 在 **常规** 快速选项卡上，将 **包括申请** 选项设置为 *是*。
1. 对要包括申请的其他每个主计划重复步骤 2 和 3。

## <a name="approved-requisitions-time-fence"></a>已审核的申请时限

*已审核的申请时限* 确定主计划包括已审核的补货申请的需求要追溯多长时间（以天为单位）。 您可以在覆盖范围组级别和主计划级别设置已审核的申请时限。

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>为覆盖范围组设置已审核的申请时限

1. 转到 **主计划** \> **设置** \> **覆盖范围** \> **覆盖范围组**。
1. 创建或选择一个覆盖范围组。
1. 在 **其他** 快速选项卡上，将 **已审核的申请时限(天)** 字段设置为时限要包括的天数。
1. 对要设置已审核的申请时限的其他每个覆盖范围组重复步骤 2 和 3。

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>为各个主计划设置已审核的申请时限

当您为单个主计划设置已审核的申请时限时，设置将替代任何适用覆盖范围组的时限设置。

1. 转到 **主计划** \> **设置** \> **计划** \> **主计划**。
1. 创建或选择主计划。
1. 在 **时限(天)** 快速选项卡上，将 **已审核的申请时限(天)** 字段设置为时限要包括的天数。
1. 对要设置已审核的申请时限的其他每个主计划重复步骤 2 和 3。

> [!IMPORTANT]
> **即将推出：** 计划优化尚不支持已审核的申请时限。 在支持之前，您在 **已审核的申请时限(天)** 字段中输入的所有值都将被忽略。

## <a name="independent-supply-regardless-of-coverage-code"></a>独立供应，不考虑覆盖范围代码

采购申请始终由独立的计划订单覆盖，而不考虑覆盖范围代码。 此行为将确保采购申请和补货订单之间具有清晰的可追溯性和工作流。

### <a name="example-1"></a>示例 1

设置产品时，其 **覆盖范围代码** 值为 *最小值/最大值*。它具有以下库存和申请状态：

- 现有库存数量 = 10。
- 最小库存数量 = 15。
- 最大库存数量 = 20。
- 存在针对一件产品的采购申请。 请求日期是今天。

当主计划运行时，创建了两个计划订单：一个是将库存补充到最大数量的 10 件产品的计划订单，另一个是补充采购申请的 1 件产品的计划订单。

### <a name="example-2"></a>示例 2

设置产品时，其 **覆盖范围代码** 值为 *最小值/最大值*。它具有以下库存和申请状态：

- 现有库存数量 = 17。
- 最小库存数量 = 15。
- 最大库存数量 = 20。
- 存在针对一件产品的采购申请。 请求日期是今天。

主计划运行时，创建了一个针对一件产品的计划订单来补充采购申请。

### <a name="example-3"></a>示例 3

设置产品时，其 **覆盖范围代码** 值为 *期间*，期间长度为 7 天。 它具有以下库存、销售订单和请购状态：

- 现有库存数量 = 0。
- 存在采购五件产品的采购订单。 预期装运日期是今天加上一天。
- 存在针对三件产品的采购申请。 请求日期是今天加上三天。

当主计划运行时，创建了两个计划订单：一个是补充采购申请的 3 件产品的计划订单，另一个是补充销售订单需求的 5 件产品的计划订单。

> [!NOTE]
> 限定到采购申请的计划订单确认后，计划引擎保留采购申请限定。 如果后来发现确认订单缺少一些满足采购申请所需的数量，系统将为相差数量创建一个新的计划订单。

有关采购申请的详细信息，请参阅[采购申请概述](../../procurement/purchase-requisitions-overview.md)。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]