---
title: 创建和维护库存锁定
description: 本主题介绍如何使用库存锁定防止实际现有库存量被其他出站源单据预留。
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956150"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>创建和维护库存锁定

[!include [banner](../../includes/banner.md)]

本主题介绍如何使用库存锁定防止实际现有库存量被其他出站源单据预留。 在开始本主题中的过程之前，您必须有可以达到实际现有库存量的物料。

## <a name="block-inventory"></a>锁定库存

要创建库存锁定记录以锁定库存，请按照下列步骤操作。

1. 转到 **库存管理 \> 定期任务 \> 库存锁定**。
1. 在操作窗格上，选择 **新建**。
1. 在新锁定记录的标头上，将 **物料编号** 字段设置为要锁定的物料，然后输入描述。
1. 在 **常规** 快速选项卡上，在 **数量** 字段中，输入要锁定的物料数量。
1. 在 **库存维度** 快速选项卡上，指定您要锁定的物料当前所在的站点和仓库。
1. 在操作窗格上，选择 **保存**。

## <a name="update-the-conditions-of-the-inventory-blocking"></a>更新库存锁定的条件

要更新库存锁定记录，请按照下列步骤操作。

1. 转到 **库存管理 \> 定期任务 \> 库存锁定**。
1. 在列表窗格中，选择相关的锁定记录。
1. 根据需要编辑记录。 例如，您可以更改 **预期日期** 字段的值，来指示被锁定的库存预计在何时可以预留。 如果选择了 **预期收货** 选项，此日期将出现在预期交易中。 （**预期收货** 选项在您手动创建锁定记录时默认选择。）
1. 在操作窗格上，选择 **保存**。

## <a name="unblock-inventory"></a>解锁库存

要删除库存锁定记录以解锁库存，请按照下列步骤操作。

1. 转到 **库存管理 \> 定期任务 \> 库存锁定**。
1. 在列表窗格中，选择相关的锁定记录。
1. 在操作窗格上，选择 **删除**。
1. 系统将提示您确认操作。 选择 **是** 继续。
1. 关闭该页面。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
