---
title: 由于库存不可用或更新冲突导致的报表过帐错误
description: 本文提供了可能的解决方法以在 Microsoft Dynamics 365 Commerce 中过帐对帐单期间解决与库存相关的问题。
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887622"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>由于库存不可用或更新冲突导致的报表过帐错误

[!include [banner](../../includes/banner.md)]

本文提供了可能的解决方法以在 Microsoft Dynamics 365 Commerce 中过帐对帐单期间解决与库存相关的问题。

## <a name="description"></a>Description

在过帐 Commerce 交易期间，您可能会收到与库存问题或更新冲突相关的错误消息。

### <a name="inventory-issues-error-message"></a>库存问题错误消息

如果您遇到库存问题，您收到的错误消息将类似于此示例：

> xx 无法领取 ，因为只有 yy 可以从库存获得

### <a name="update-conflict-error-messages"></a>更新冲突错误信息

当库存评估方法为 *标准成本* 或 *移动平均* 时，可能会发生更新冲突问题。 因为这两种方法都是记永久成本计算方法，所以会在过帐时确定最终成本。

如果您使用的是 *移动平均* 方法，则您收到的更新冲突错误消息类似于以下示例：

> 按比例进行费用计算后，库存值 xx.xx 不是预期值

如果您使用的是 *标准成本* 方法，则您收到的更新冲突错误消息类似于以下示例：

> 标准成本在更新后与财务库存值不匹配。 值 = xx.xx，数量 = yy.yy，标准成本 = zz.zz

## <a name="resolutions"></a>解决方法

### <a name="workaround-for-the-inventory-error"></a>库存错误的解决方法

通过手动更新物料库存，或在 Commerce headquarters 中为与该物料关联的物料模型组启用实际负库存，您可以缓解库存错误。

为了获得一致的过帐体验，Microsoft 建议您为物料模型组启用实际负库存。 在某些情况下，除非启用实际负库存，否则可能不能过帐对帐单。

例如，某商品没有库存，但收银员退回该商品，然后以较低的价格将其添加回同一交易以模拟价格匹配。 在这种情况下，退货交易和销售交易都会被拉入单个客户订单的同一对帐单中。 但是，由于无法保证退货行（增加库存）会在销售行（减少库存）过帐之前过帐，因此可能会出现库存错误。 如果在这种情况下启用了实际负库存，则交易记录过帐不会受到负面影响，而系统将正确地反映库存。

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>为项目模型组启用负实际库存

要为 Commerce headquarters 的物料模型组启用负实际库存，请执行以下步骤。

1. 转到 **库存管理 \> 设置 \> 库存**。
1. 在左侧导航窗格中，选择物料模型组。
1. 在 **库存策略** 部分中的 **负库存** 下面，选中 **实际负库存** 复选框。

![已启用允许实际负库存。](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>更新冲突错误的解决方法

有关更新冲突错误的可能解决方法，请参阅[库存评估方法为“标准成本”或“移动平均”时发生更新冲突](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation)。

> [!NOTE]
> 对于更新冲突错误，您不必删除使用过帐聚合步骤生成的客户订单。 在您实施建议的解决方法后，如果您重新尝试对帐单过帐，应该会过帐该对帐单。
