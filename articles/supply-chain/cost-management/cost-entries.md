---
title: "成本条目"
description: "本文提供有关成本条目及其何时创建的信息。 成本条目是登记指定事件的数量和成本的记录。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4d8a443d03f8eb2d6ff44d869964b47b6569ce4c
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="cost-entries"></a>成本条目

[!INCLUDE [banner](../includes/banner.md)]

本文提供有关成本条目及其何时创建的信息。 成本条目是登记指定事件的数量和成本的记录。

成本条目是在活动财务库存维度上记录的库存交易记录的合并。

## <a name="examples"></a>示例
### <a name="example-1-no-cost-entries-are-created"></a>示例 1：未创建任何成本条目

登记转移日记帐事件。 该事件将一件物料 A 从库位 A 转移到库位 B。Location 库存维度不被视为成本对象的一部分。 因此，该事件将创建两个库存交易记录，但不创建成本条目。

### <a name="example-2-cost-entries-are-created"></a>示例 2：创建成本条目

登记转移日记帐事件。 该事件将一件物料 A 从站点 1 转移到站点 2。 Site 库存维度被视为成本对象的一部分。 因此，该事件将创建两个库存交易记录和两个成本条目。

### <a name="example-3-one-cost-entry-is-created"></a>示例 3：创建一个成本条目

登记采购订单的产品收据事件。 该事件登记 100 件物料 A（单位成本为 10.00 美元 (USD)）。 由于物料 A 使用序列号跟踪库存管理的目的，因此将为接收的每个物料创建一个唯一的序列号。 因此，该事件将创建 100 个库存交易记录和一个成本条目。

## <a name="cost-entries-page"></a>成本条目页面
利用新的**“成本条目”**页面，可以查看和控制数量和成本的登记。 此页面对**“库存交易记录”**和**“库存结算”**页面进行了补充。 按时间顺序登记事件的记录。 因此，您可以快速查找和控制与文档相关的一个特定事件或所有事件的累计成本。 以下是一个示例：

-   为物料 A 登记产品收据事件。以单位成本 10.00 美元接收 100 件物料。
-   在登记发票事件几天后，单位成本增加到 11.00 美元。 因此，总金额为 1,100 美元。 创建另一个凭证来说明 100 美元的差额。
-   几天后，将在采购订单上登记 15.00 美元的杂费（含运输成本）。

| 凭证 | 日期       | 参考      | 数字 | 批次 ID  | 数量 | 本币金额  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01-01-2015 | 采购订单 | 100001 | 0000101 | 100.00   | 1000.00 |
| 00002   | 20-01-2015 | 采购订单 | 100001 | 0000101 |          | 100.00  |
| 00003   | 31-01-2015 | 调整     | 100001 | 0000101 |          | 15.00   |

**“成本条目”**页面支持按文档 ID 和文档日期进行筛选。 

> [!NOTE]
> 成本条目仅适用于[成本对象](cost-object.md)或已发布的产品。

<a name="see-also"></a>请参阅
--------

[成本对象](cost-object.md)




