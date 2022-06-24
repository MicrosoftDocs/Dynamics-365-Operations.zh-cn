---
title: 检查货物质量
description: 本文说明如何处理质检订单。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eeb14a3b0a61f34819bdd8d524e65ac214a81c35
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857567"
---
# <a name="inspect-the-quality-of-goods"></a>检查货物质量

[!include [banner](../../includes/banner.md)]

本文说明如何处理质检订单。 质量检查通常由质检员执行。

如果安装了标准演示数据，您可以使用它来完成本文中的过程。 要使用演示数据，在开始前选择 *USMF* 法人。 然后，必须确认采购订单 *000016* 并过帐产品收据。 质检订单将自动生成。

## <a name="step-1-select-a-quality-order"></a>步骤 1：选择质检订单

要选择质检订单，请按照以下步骤操作。

1. 转到 **库存管理 \> 定期任务 \> 质量管理 \> 质检订单**。
1. 在开始此过程前，选择生成的质检订单。

## <a name="step-2-record-test-results"></a>步骤 2：记录测试结果

要记录测试结果，请按照下列步骤操作。

1. 选择 **结果**。
1. 选择 **编辑**。
1. 在 **结果数量** 字段中，输入一个数字。
1. 在 **结果** 字段中，选择所需记录。 在此示例中，结果将基于预定义的结果。 通常，您将记录更具体的测试结果，如尺寸或其他维度。
1. 选择 **保存**。
1. 关闭该页面。

## <a name="step-3-validate-the-quality-order"></a>步骤 3：验证质检订单

要验证质检订单，请按照以下步骤操作。

1. 选择 **验证**。
1. 在 **验证者** 字段中，选择执行检查的用户。
1. 选择 **选择**。
1. 选择 **确定**。
1. 关闭该页面。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
