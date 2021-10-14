---
title: 不符合项的操作
description: 本主题介绍如何创建和使用不符合项的操作。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35619454af8b1cb1b7d383d393362f58d9dd0ea6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573865"
---
# <a name="operations-for-nonconformances"></a>不符合项的操作

[!include [banner](../includes/banner.md)]

本主题介绍如何创建和使用不符合项的操作。

您可以使用 **操作** 页定义可以对已审核的未达标执行的工作的分类。 向不符合项分配相关操作时，可以提供详细信息，如执行操作所需的关联物料、工时和费用。 系统将使用此信息计算操作的估计成本。 这些详细信息和预估成本用于参考。 针对质量的相关工序不同于可以为生产工艺路线定义的工序。

> [!NOTE]
> 虽然您可以跟踪成本、时间和与不符合项相关的操作中使用的物料，但是您输入的数据仅作为参考信息。 它不会自动与总帐、库存子分类帐或 **考勤** 模块集成。

## <a name="examples-of-operations"></a>操作示例

您在一家制造公司工作。 为未通过质量测试的物料创建并批准了不符合项。 创建了更正，指示问题与机器上损坏的轴承有关。 更换轴承需要若干步骤，并会跟踪每个操作的责任方。 例如，可能需要执行以下步骤：

1. 停止生产线，执行清理程序。
1. 维修人员更换轴承。
1. 质量保证人员在重新启动机器之前对机器之进行检查。

对于此示例，可以创建以下操作来表示必须完成的工作：

- 停止生产线。
- 清理生产线。
- 执行机器维修。
- 检查机器。

## <a name="create-an-operation"></a>创建操作

1. 转到 **库存管理 \> 设置 \> 质量管理 \> 操作**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **操作** – 为操作输入唯一 ID 或名称。
    - **描述** – 输入操作的详细描述。
    - **类型** – 如果操作只能用于与特定订单类型相关的不符合项，选择订单类型（*采购订单* 或 *销售订单*）。

1. 关闭该页面。

## <a name="additional-resources"></a>其他资源

- [质量管理概览](quality-management-processes.md)
- [启用质量和不符合项管理](enable-quality-management.md)
- [创建和处理不符合项](tasks/create-process-non-conformance.md)
- [负责审核不符合项的工作人员](quality-responsible-workers.md)
- [不符合项的隔离区域](quality-quarantine-zones.md)
- [不符合项的诊断类型](quality-diagnostic-types.md)
- [不符合项的质量费用](quality-charges.md)
- [不符合项的问题类型](quality-operations.md)
- [仓库流程质量管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
