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
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026298"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="eeba9-103">将物料模型组复制到另一个法人时缺少字段设置</span><span class="sxs-lookup"><span data-stu-id="eeba9-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="eeba9-104">知识库编号：4612800</span><span class="sxs-lookup"><span data-stu-id="eeba9-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="eeba9-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="eeba9-105">Symptoms</span></span>

<span data-ttu-id="eeba9-106">当您使用 *物料模型组库存策略* 实体将物料模型组复制到另一个法人（公司）时，目标法人中的新模型组缺少某些字段设置（例如，库存模型和描述）。</span><span class="sxs-lookup"><span data-stu-id="eeba9-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="eeba9-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="eeba9-107">Resolution</span></span>

<span data-ttu-id="eeba9-108">要创建物料模型组到另一个法人的完整副本，还必须选择与该物料模型组关联的物料模型组库存策略 (`InventInventoryPolicyEntity`) 和成本流假设策略 (`InventCostFlowAssumptionPolicyEntity`)。</span><span class="sxs-lookup"><span data-stu-id="eeba9-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
