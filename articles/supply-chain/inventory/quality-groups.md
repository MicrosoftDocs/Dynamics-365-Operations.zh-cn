---
title: 物料质量组
description: 本文介绍如何使用和创建物料质量组来对产品进行逻辑分组，以便可以将其分配给质量关联来自动生成质检订单。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf1ce49fa58fd1a8a5aa07636e0b2bd7e2fc10e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875356"
---
# <a name="item-quality-groups"></a>物料质量组

[!include [banner](../includes/banner.md)]

质量组表示物料的公共测试要求。 本文介绍如何使用和创建物料质量组来对产品进行逻辑分组，以便可以将其分配给质量关联来自动生成质检订单。

要设置、编辑和查看分配给质量组的物料或分配给物料的质量组，转到 **库存管理 \> 设置 \> 质量组**。 在 **测试组** 页上定义测试要求后，您可以定义用于自动生成质检订单的规则。 为了简化该流程，您不为各个物料定义规则。 而是可以在 **质量关联** 页为质量组定义规则。

## <a name="example-of-an-item-quality-group"></a>物料质量组示例

某制造公司采购的多种原材料具有相同的进货检查测试要求。 因此，公司定义了一个质量组，然后将与原材料关联的物料编号分配给该组。 之后，公司采购一个新类型的原材料，具有相同的测试要求。 公司不是为新物料设置新的测试要求，而是将新物料的物料编号添加到现有的质量组。

这家公司还生产具有相同测试要求的物料，并装运具有相同装运前测试要求的物料。 因此，公司定义两个附加质量组，然后将相关物料编号分配给每个组。

## <a name="create-a-quality-group"></a>创建质检组

要创建质量组，请执行以下步骤。

1. 转到 **库存管理 \> 设置 \> 质量控制 \> 质量组**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **质量组** – 为质量组输入唯一 ID 或名称。
    - **描述** – 输入质量组的详细描述。

1. 关闭该页面。

## <a name="manually-add-items-to-a-quality-group"></a>手动向质量组添加物料

要手动向质量组添加物料，请按照下列步骤操作。

1. 转到 **库存管理 \> 设置 \> 质量控制 \> 质量组**。
1. 选择要添加物料的质量组。
1. 在操作窗格上，选择 **物料**。
1. 在 **质量组中的物料** 页上的操作窗格上，选择 **新建** 在网格中添加一行。 然后，对于新行，将 **物料编号** 字段设置为要添加的物料编号。
1. 对必须添加的其他每个物料重复上一个步骤。
1. 关闭页面。

## <a name="add-multiple-items-to-a-quality-group"></a>向质量组添加多个物料

要向质量组添加多个物料，请按照下列步骤操作。

1. 转到 **库存管理 \> 设置 \> 质量控制 \> 质量组**。
1. 创建或选择要添加物料的质量组。
1. 在操作窗格上，选择 **添加物料**。
1. 在 **查询** 对话框中，输入要添加的物料的筛选条件。 例如，您可以筛选特定物料组中的所有物料。
1. 选择 **确定**。
1. 在 **添加物料** 对话框中，网格将显示与查询匹配的所有物料。 查看结果。

    如果需要任何更改，选择 **选择** 返回到 **查询** 对话框，然后调整您的查询。

1. 当结果包括要添加的所有物料时，选择 **确定**。
1. 关闭该页面。

## <a name="manually-associate-an-item-with-a-quality-group"></a>手动将物料与质量组关联

要手动将物料与质量组关联，请按照下列步骤操作。

1. 转到 **库存管理 \> 设置 \> 质量控制 \> 物料质量组**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **物料编号** – 选择要添加的物料编号。
    - **质量组** – 选择要分配给物料的质量组。

1. 对必须添加的物料和质量组的每个其他组合重复上一个步骤。
1. 关闭页面。

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>从“已发布产品”页手动添加质量组

要从 **已发布产品** 页手动添加质量组，请按照以下步骤操作。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 选择您要向其分配质量组的产品。
1. 在操作窗格上 **管理库存** 选项卡的 **质量** 组中，选择 **物料质量组**。
1. 在 **质量组中的物料** 页上的操作窗格上，选择 **新建** 在网格中添加一行。 然后，对于新行，将 **质量组** 字段设置为要分配给产品的质量组。
1. 对要分配给产品的每个其他质量组重复上一个步骤。
1. 关闭页面。

## <a name="additional-resources"></a>其他资源

- [质量管理测试仪器](quality-test-instruments.md)
- [质量管理测试](quality-tests.md)
- [质量管理测试组](quality-test-groups.md)
- [质量管理测试变量](quality-test-variables.md)
- [质量关联](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
