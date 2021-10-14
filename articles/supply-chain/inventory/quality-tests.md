---
title: 质量管理测试
description: 本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中创建可用于质检订单的测试。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c10b67f86fc29b5e8c08081a9b789d4f42c24cf4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573841"
---
# <a name="quality-management-tests"></a>质量管理测试

[!include [banner](../includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中创建可用于质检订单的测试。

您将使用 **测试** 页定义和查看用于确定产品是否符合质量规范的各个测试。 您可以将一个或多个单独测试分配给测试组。 在这种情况下，您还可以指定测试特定信息，例如可接受的度量值。 度量值用于定量测试。 对于定性测试，将使用测试变量。

- 对于定量测试，**类型** 字段将设置为 *整数* 或 *分数*。 另外还将指定度量单位。 质量规范和测试结果表示为数字。
- 对于定性测试，**类型** 字段将设置为 *选项*。 定性测试需要有关要度量的质量变量及其枚举选项的附加信息。 质量规范和测试结果根据结果表示。

您可以选择将测试仪器分配给测试。 不过，创建和使用针对质检订单的测试不需要测试仪器。 有关详细信息，请参阅[质量管理测试仪器](quality-test-instruments.md)。

您还可以选择为测试指定单位，来指示记录测试结果所使用的度量单位。 例如，针对温度的测试可能包含华氏度或摄氏度单位。

## <a name="example-of-a-test"></a>测试示例

某个制造公司对采购物料执行两个测试：针对物料质量的定量测试和针对包装损坏的定性测试。 该公司指定有关质量测试的附加信息来定义测试变量（例如，损坏的包装）及其结果。 公司使用 **测试组** 页将两个测试分配给一个测试组并指定测试特定信息。 将测试组分配给质检订单，以便公司可以报告这两个测试的测试结果。

## <a name="create-a-test"></a>创建测试

请按照以下步骤创建测试。

1. 转到 **库存管理 \> 设置 \> 质量控制 \> 测试**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **测试** – 为测试输入唯一 ID 或名称。
    - **描述** – 输入测试的详细描述。
    - **类型** – 选择测试产生的结果类型。 对于定量测试，选择 *分数* 或 *整数*。 对于定性测试，选择 *选项*。
    - **测试仪器** – 选择应用于测试的[测试仪器](quality-test-instruments.md)。
    - **单位** – 如果您在 **类型** 字段中选择了 *分数* 或 *整数*（即如果测试是定量测试），则选择记录测试结果应使用的度量单位。

1. 关闭该页面。

> [!NOTE]
> 保存测试后，您将无法再编辑网格中的 **类型** 字段。 如果必须更改将为测试记录的测试结果的类型，在操作窗格上选择 **更改质量测试类型**。 在 **更改质量测试类型** 对话框中，将 **新类型** 字段设置为所需类型，然后选择 **确定** 关闭对话框。

## <a name="additional-resources"></a>其他资源

- [质量管理测试仪器](quality-test-instruments.md)
- [质量管理测试组](quality-test-groups.md)
- [质量管理测试变量](quality-test-variables.md)
- [质量关联](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
