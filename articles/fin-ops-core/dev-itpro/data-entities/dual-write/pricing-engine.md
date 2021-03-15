---
title: 按需与 Supply Chain Management 定价引擎同步
description: 本主题介绍如何在 Dynamics 365 Sales 的 Microsoft Dynamics 365 Supply Chain Management 中使用定价引擎。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 45a9de18a3ff9c50eba8b316171b492605d683d4
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130645"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>按需与 Supply Chain Management 定价引擎同步

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management 包括处理贸易协议、价目表、客户会员计划、促销和折扣的定价引擎。 定价引擎使用复杂的规则来确定给定报价单或订单的最佳价格。 使用双向写入时，您可以在 Dynamics 365 Sales 中的“报价单”和“订单”页面上使用 Dynamics 365 Supply Chain Management 中的静态定价或定价引擎。

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>使用 Sales 中的 Supply Chain Management 中的定价引擎

1. 在 Sales 中，转到 **销售 \> 订单**。
2. 选择 **新建** 创建新订单，或在 **我的订单** 列表中选择现有订单。
3. 添加新订单行。
4. 如果您要创建新订单，请选择在操作窗格上 **价格订单**。 如果您要更新现有订单，请选择在操作窗格上 **重新计算**。

    以下列将自动填充：

    + 详细信息金额
    + 折扣百分比
    + 折扣
    + 不计运费金额
    + 运费金额
    + 税金总计
    + 总金额
    
5. 为确保系统考虑贸易和销售协议来计算价格：
    1. 导航到您的 Supply Chain Management 环境。
    2. 导航到 **应收帐款 \> 设置 \> 应收帐款参数**。
    3. 选择侧导航栏中的 **价格** 选项卡。
    4. 在 **贸易协议评估** 快速选项卡下，取消选中 **手动输入** 选项。

## <a name="how-it-works"></a>工作原理

当您在 Sales 中选择 **价格订单** 时，将为关联销售订单调用 Supply Chain Management 中 **销售订单 \> 视图** 选项卡上的 **总计** 函数。 Sales 中订单总计中的值用于填写 Supply Chain Management 中的对应列。

在 Supply Chain Management 中计算销售订单总计时，计算将评估客户的现有贸易协议和销售协议以及销售订单中列出的产品。 此信息用于计算总计。 选择 **价格订单** 时，Sales 会自动反映 Supply Chain Management 中已经完成的所有设置。

## <a name="limitations"></a>限制

填写 Sales 中的列后，将应用以下限制：

+ Supply Chain Management 中的费用设置和费用分配不会在 Sales 中复制。
+ 定价不考虑在 Supply Chain Management 中销售订单行页面上的 **零售渠道** 列中指定的特殊零售定价。
+ 不考虑 Supply Chain Management 的 **贸易折让管理** 部分定义的折扣。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]