---
title: 不符合项的隔离区域
description: 本主题介绍如何创建和使用不符合项的隔离区域。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021796"
---
# <a name="quarantine-zones-for-nonconformances"></a>不符合项的隔离区域

[!include [banner](../includes/banner.md)]

本主题介绍如何创建和使用不符合项的隔离区域。

您将使用 **隔离区域** 页定义可以分配给不符合项的区域。 创建不符合项时，您可以在 **不符合项** 页的 **常规** 选项卡上设置 **隔离区域** 和 **隔离类型** 字段。 **隔离区域** 字段通常指示物料所在的区域或位置。 **隔离类型** 字段将物料定义为 *限制使用* 或者 *不可用*。

当您打印不符合项或不符合项的更正报告时，您可以查看物料所在的隔离区域。

您还可以为不符合项打印不符合项标记。 此报告显示分配的隔离区域和有关使用情况的信息，以提供应如何处理有缺陷物料的指导。 隔离区域可以与库存库位或运营资源对应。

## <a name="examples-of-quarantine-zones"></a>隔离区域示例

### <a name="example-1"></a>示例 1

您在一家电子制造公司工作，该公司生产和分销电视、扬声器和媒体播放器。 在这种情况下，您可以配置隔离区域来表示每种类型的产品。

### <a name="example-2"></a>示例 2

三个箱子和两个架子用来存放未达标的物料。 在这种情况下，您可以配置五个隔离区域，每个箱子和每个架子各一个。

## <a name="create-a-quarantine-zone"></a>创建隔离区域

1. 转到 **库存管理 \> 设置 \> 质量管理 \> 隔离区域**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **隔离区域** – 为隔离区域输入唯一 ID 或名称。
    - **描述** – 输入隔离区域的详细描述。

1. 关闭该页面。

## <a name="additional-resources"></a>其他资源

- [质量管理概览](quality-management-processes.md)
- [启用质量和不符合项管理](enable-quality-management.md)
- [负责审核不符合项的工作人员](quality-responsible-workers.md)
- [不符合项的问题类型](quality-quarantine-zones.md)
- [不符合项的诊断类型](quality-diagnostic-types.md)
- [不符合项的质量费用](quality-charges.md)
- [不符合项的操作](quality-operations.md)
- [仓库流程质量管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
