---
title: 将物料模型组复制到另一个法人时缺少字段设置
description: 将物料模型组复制到另一个法人时缺少字段设置。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 128caead04cf467c65a50bc6cd2f9e76e318f536b7eafa7972ffc1b5da5bceba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738835"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>将物料模型组复制到另一个法人时缺少字段设置

知识库编号：4612800

## <a name="symptoms"></a>故障特征

当您使用 *物料模型组库存策略* 实体将物料模型组复制到另一个法人（公司）时，目标法人中的新模型组缺少某些字段设置（例如，库存模型和描述）。

## <a name="resolution"></a>解决方法

要创建物料模型组到另一个法人的完整副本，还必须选择与该物料模型组关联的物料模型组库存策略 (`InventInventoryPolicyEntity`) 和成本流假设策略 (`InventCostFlowAssumptionPolicyEntity`)。
