---
title: 质量管理测试变量
description: 本文介绍如何创建可用于在 Microsoft Dynamics 365 Supply Chain Management 中对质检订单进行定性测试的测试变量。
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
ms.openlocfilehash: 10fe206b76f2e50e09cb6aaa6055614c2fe9425d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857625"
---
# <a name="quality-management-test-variables"></a>质量管理测试变量

[!include [banner](../includes/banner.md)]

本文介绍如何创建可用于在 Microsoft Dynamics 365 Supply Chain Management 中对质检订单进行定性测试的测试变量。

对于 **测试** 页上定义的每个定性测试，您必须定义一个测试变量及其可能的结果。 （对于定性测试，将 **测试** 页上的 **类型** 字段设置为 *选项*。）

您将使用 **测试变量** 页设置、编辑和查看与定性测试关联的测试变量的可能结果。 对于每个结果，您将分配 *通过* 或 *失败* 结果状态，来指示测试在选择该结果作为测试结果时是通过还是失败。 您将使用 **测试组** 页将测试变量及其默认结果分配给单独的定性测试。

对于每个测试变量，我们建议您至少定义两个结果：一个结果状态为 *通过*，另一个结果状态为 *失败*。 可定义的变量或结果的总数没有限制。 此外，多个测试可以使用相同的测试变量来记录结果。

## <a name="examples-of-test-variables"></a>测试变量示例

### <a name="example-1"></a>示例 1

一家制造公司对制造的材料执行两项测试。 在一项测试中，pH 值与色条关联。 可接受的 pH 值以浅色显示，不可接受的 pH 值以深色显示。 在另一项测试中，执行了多次外观检查，质量工作人员根据自己的判断来确定物料是否通过外观检查。

### <a name="example-2"></a>示例 2

一个生产饼干的制造公司对成品使用检查测试。 此检查测试具有多个变量。 一个变量是味道，其可能结果是好和坏。 第二个变量是颜色，其可能结果是过暗、过浅和正好。

## <a name="create-a-test-variable"></a>创建测试变量

请按照以下步骤创建测试变量。

1. 转到 **库存管理 \> 设置 \> 质量控制 \> 测试变量**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **变量** – 为变量输入唯一 ID 或名称。
    - **描述** – 输入变量的详细描述。

1. 在仍选择新行的同时，在操作窗格上选择 **结果**。
1. 在 **测试变量结果** 页上的操作窗格上，选择 **新建** 在网格中添加一行。 然后，针对新行设置以下字段：

    - **结果** – 为结果输入唯一 ID 或名称。
    - **描述** – 输入结果的详细描述。
    - **结果状态** – 选择 *通过* 或 *失败* 来指示测试在选择该结果作为测试结果时是通过还是失败。

1. 对其他每个结果重复上一个步骤。 确保至少一个结果的结果状态为 *通过*，至少一个结果的结果状态为 *失败*。
1. 关闭页面。

## <a name="additional-resources"></a>其他资源

- [质量管理测试仪器](quality-test-instruments.md)
- [质量管理测试](quality-tests.md)
- [质量管理测试组](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
