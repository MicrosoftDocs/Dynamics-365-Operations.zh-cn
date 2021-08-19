---
title: 启用质量和不符合项管理
description: 本主题概述了在 Microsoft Dynamics 365 Supply Chain Management 中设置和配置质量和不符合项管理功能的流程。
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b202d76e4b5bc0dfe9f0572274b3453abca58a435b70e96874155f867114a2aa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717332"
---
# <a name="enable-quality-and-nonconformance-management"></a>启用质量和不符合项管理

[!include [banner](../includes/banner.md)]

本主题概述了在 Microsoft Dynamics 365 Supply Chain Management 中设置和配置质量和不符合项管理功能的流程。

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>启用质量和不符合项管理

请按照以下步骤在系统上启用质量管理。

1. 转到 **库存管理 \> 设置 \> 库存和仓库管理参数**。
1. 在 **质量管理** 选项卡上，将 **使用质量管理** 选项设置为 *是*。
1. 在 **小时工资率** 字段中用本币输入人工小时工资率。 小时工资率用于计算与未达标相关的工序的成本。 小时工资率和计算的成本为未达标提供了参考信息。 它们不与其他功能交互。
1. 选择 **报表设置**。
1. 为各个报表类型添加新行，然后选择要用于每个报表的文档类型。
1. 关闭该页面。
1. 关闭该页面。

## <a name="quality-management-configuration-process"></a>质量管理配置流程

您必须先配置系统和先决条件，然后才能够开始使用质量管理功能和生成质检订单。 这里是配置质量管理所需的步骤列表。

1. [启用质量和不符合项管理](#enable-qm)。
1. 可选：[配置测试仪器](quality-test-instruments.md)。
1. [配置测试](quality-tests.md)。
1. [配置测试变量和结果](quality-test-variables.md)。
1. [配置测试组](quality-test-groups.md)。
1. 可选：[配置质量组，并链接到产品](quality-groups.md)。
1. 可选：[配置质量关联](quality-associations.md)。

配置完成后，您可以开始创建和处理质检订单。 有关如何创建和处理质检订单的详细信息，请参阅[质检订单](quality-orders.md)。

## <a name="nonconformance-management-configuration-process"></a>不符合项管理配置流程

您必须先配置系统和先决条件，然后才能够开始使用不符合项管理功能和生成不符合项。 这里是配置不符合项管理所需的步骤列表。

1. [启用质量和不符合项管理](#enable-qm)。
1. [配置负责审核不符合项的工作人员](quality-responsible-workers.md)。
1. [配置问题类型](quality-problem-types.md)。
1. [配置隔离区域](quality-quarantine-zones.md)。
1. [配置诊断类型](quality-diagnostic-types.md)。
1. [配置操作](quality-operations.md)。
1. 可选：[配置质量费用](quality-charges.md)。

配置完成后，您可以开始创建和处理不符合项。 有关如何创建和处理不符合项的详细信息，请参阅[创建和处理不符合项](tasks/create-process-non-conformance.md)。

## <a name="additional-resources"></a>其他资源

- [质量管理概览](quality-management-processes.md)
- [启用质量和不符合项管理](enable-quality-management.md)
- [仓库流程质量管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
