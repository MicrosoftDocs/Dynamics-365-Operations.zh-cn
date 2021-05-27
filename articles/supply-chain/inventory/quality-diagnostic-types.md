---
title: 不符合项的诊断类型
description: 本主题介绍如何使用和创建可用于不符合项的诊断类型。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022268"
---
# <a name="diagnostic-types-for-nonconformances"></a>不符合项的诊断类型

[!include [banner](../includes/banner.md)]

本主题介绍如何使用和创建可用于不符合项的诊断类型。

您将使用 **诊断类型** 页定义诊断操作的分类。 然后，当您为不符合项创建更正时，将选择诊断。 更正指定应对已审核的未达标采取的诊断操作类型以及应该执行操作的用户。 它还指定请求的完成日期和计划的完成日期。

## <a name="examples-of-diagnostic-types"></a>诊断类型的示例

您在一家制造公司工作，有几个物料未通过质量测试。 这些物料被移至隔离区域并标记为未达标产品。 一个不符合项记录在 Microsoft Dynamics 365 Supply Chain Management 中创建，用于跟踪问题解决过程的详细信息。

在这种情况下，出现了质量问题，因为包装物料的机器的轴承损坏，出现过热现象。 更正此问题的方法是更换机器中的零件。

配置诊断类型时，您可以创建多个记录，每个记录代表机器可能存在的一个不同问题类型。 或者，您可以创建一个代表机器维修的通用诊断类型。

## <a name="create-a-diagnostic-type"></a>创建诊断类型

1. 转到 **库存管理 \> 设置 \> 质量管理 \> 诊断类型**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **诊断** – 输入诊断类型的唯一 ID 或名称。
    - **描述** – 输入诊断类型的详细描述。

1. 关闭该页面。

## <a name="additional-resources"></a>其他资源

- [质量管理概览](quality-management-processes.md)
- [启用质量和不符合项管理](enable-quality-management.md)
- [负责审核不符合项的工作人员](quality-responsible-workers.md)
- [不符合项的隔离区域](quality-quarantine-zones.md)
- [不符合项的问题类型](quality-problem-types.md)
- [不符合项的质量费用](quality-charges.md)
- [不符合项的操作](quality-operations.md)
- [仓库流程质量管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
