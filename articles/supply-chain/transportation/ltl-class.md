---
title: 小于货车荷载 (LTL) 类
description: 本主题说明什么是小于货车荷载 (LTL) 类，并介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中进行设置。
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941802"
---
# <a name="less-than-truckload-ltl-classes"></a>小于货车荷载 (LTL) 类

[!include [banner](../includes/banner.md)]

小于货车荷载 (LTL) 类是一个货运类，用于对可以装运的物料进行分类。 通常，每种类型的产品或商品都有全国汽车货运分类 (NMFC) 代码，该代码与 LTL 装运的特定货运类编号相对应。 LTL 货运类代表物料的类别，而 NMFC 代码与 18 个货运类中每个类的特定商品相关。

此功能让您可以使用您的系统执行以下任务：

- 定义您的公司使用的 LTL 货运类。
- 在 **NMFC 代码** 页上，将每个 LTL 类分配给 NMFC 代码。 有关详细信息，请参阅[全国汽车货运分类 (NMFC) 代码](nmfc-codes.md)。
- 在 **产品** 页上为每个产品分配 NMFC 代码（因此分配其关联的 LTL 代码）。
- 准确评估分配了 NMFC 代码的每个产品的 LTL 类。
- 通过检查国际 LTL 标准，确定每个 LTL 类的包装要求。 这样，您可以确保您的产品得到良好的保护，可以安全装运。
- 根据每种产品的 LTL 货运类，获取准确的装运估计信息。

此主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中创建 LTL 类。

## <a name="create-an-ltl-class"></a>创建 LTL 类

要创建 LTL 类，请执行以下步骤。

1. 按以下步骤之一：

    - 转到 **仓库管理 \> 设置 \> 库存 \> LTL 类**。
    - 转到 **运输管理 \> 设置 \> 运输标准 \> LTL 类**。

2. 在操作窗格上，选择 **新建** 创建一个 LTL 类。 然后设置以下字段：

    - **LTL 类** – 输入商品类型的公司内部 LTL 类标识符 (ID)。 大多数公司使用国际标准。 在这种情况下，此字段的值将与 **类** 字段的值匹配。 但是，如果您的公司使用自己的标准，请输入符合该标准的代码。
    - **名称** – 输入一个将帮助您和其他用户为每个 NMFC 代码选择正确的 LTL 类的描述性名称。
    - **类** – 输入商品类型的国际标准 LTL 类 ID。 您在此处输入的代码必须符合官方标准。

## <a name="example-set-up-ltl-classes"></a>示例：设置 LTL 类

下面的示例演示如何设置可以用于不同类型产品的两个不同的 LTL 类。

1. 转到 **仓库管理 \> 设置 \> 库存 \> LTL 类**。
1. 在操作窗格上，选择 **新建**。
1. 在新行中，设置以下值：

    - **LTL 类**：*92.5*
    - **名称**：*计算机、显示器、冰箱*
    - **类**：*92.5*

1. 在操作窗格上，选择 **保存**。
1. 在操作窗格上，选择 **新建**。
1. 在新行中，设置以下值：

    - **LTL 类**：*125*
    - **名称**：*小家电*
    - **类**：*125*

1. 在操作窗格上，选择 **保存**。

## <a name="additional-resources"></a>其他资源

- [全国汽车货运分类 (NMFC) 代码](nmfc-codes.md)
- [创建提单](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
