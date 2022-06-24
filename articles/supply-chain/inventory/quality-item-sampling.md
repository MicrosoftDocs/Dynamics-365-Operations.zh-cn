---
title: 质量管理项目抽样
description: 本文介绍如何设置物料抽样。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 644eae4fbd9f82027c1cb69efba00dc893f8fc66
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865141"
---
# <a name="quality-management-item-sampling"></a>质量管理项目抽样

[!include [banner](../includes/banner.md)]

物料抽样用作质量关联的一部分。 它定义必须检查的当前实际库存量。 抽样可以基于固定数量、百分比或完整牌照。

## <a name="set-up-item-sampling"></a>设置物料抽样

请按照以下步骤设置物料抽样。

1. 转到 **库存管理 \> 设置 \> 质量控制 \> 物料抽样**。
1. 选择 **新建**。
1. 在 **物料抽样** 字段中，输入一个值。
1. 在 **描述** 字段中，输入一个值。
1. 在 **值** 字段中，输入一个数字。 此值与在相邻字段中选择的数量规范值相关。
1. 如果测试失败，在应锁定全部批次或订单行数量时，在 **流程** 部分选中 **完全锁定** 复选框。 如果清除此复选框，测试失败时将仅锁定质检订单中的物料。
1. 选择 **保存**。
1. 关闭该页面。

> [!NOTE]
> *仓库流程质量管理* 功能提供其他的物料抽样功能。 它增加了 *物料抽样范围* 概念，让您可以将完整牌照定义为数量规范。 如果已启用此功能，请参阅[仓库流程质量管理](quality-management-for-warehouses-processes.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
