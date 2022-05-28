---
title: 全国汽车货运分类 (NMFC) 代码
description: 本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中使用全国汽车货运分类 (NMFC) 代码
author: Weijiesa
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 5127e132a8c06815e9ecd11338c729cd8bb87f18
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670571"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>全国汽车货运分类 (NMFC) 代码

[!include [banner](../includes/banner.md)]

全国汽车货运分类 (NMFC) 代码可帮助您对可以装运的物料进行分类。 NMFC 代码是用于对商品进行分组的符号。 它让运输公司能够根据卡车装配、装载问题、处理问题和易腐性等考虑事项对物料进行分类，从而评估要装运的货物。 商品将使用从 50 到 500 的数字范围分组到 18 个货运类之一。 商品被分组的类基于对四个运输特征的评估：密度、耐藏性、处理和责任。 这些特征共同确定商品的可运输性。

NMFC 代码与每个小于货车荷载 (LTL) 装运物料关联。 例如，可能为笔记本电脑分配了分类为 2.5 的 NMFC，而为电线分配了分类为 65 的 NMFC。

此功能可以帮助工作人员使用 NMFC 代码对 LTL 装运物料进行分类。 下面举了一些示例加以说明：

- 如果您的公司在提单 (BOL) 上包含货运描述，那么承运人将对装运的货物有所了解。 货运是一个重要的分类，因为很多运输公司的整个业务模型是基于所装运货物的类型。
- 此分类对于您的公司可能是必不可少的，因为它用于确定给定负荷的成本。
- 您的公司可以确定 LTL 物流运输公司的利润率。

此主题描述如何在 Microsoft Dynamics 365 Supply Chain Management 中使用 NMFC 代码。

## <a name="prerequisites"></a>先决条件

您必须先设置必须映射到 NMFC 代码的所有 LTL 货运类，然后才能够创建 NMFC 代码。 LTL 货运类代表物料的类别，而 NMFC 代码与 18 个货运类中每个类的特定商品相关。 有关如何使用 LTL 类的详细信息，请参阅[小于货车荷载 (LTL) 类](ltl-class.md)。

## <a name="create-an-nmfc-code"></a>创建 NMFC 代码

要创建 NMFC 代码，请执行以下步骤。

1. 按以下步骤之一：

    - 转到 **仓库管理 \> 设置 \> 库存 \> NMFC 代码**。
    - 转到 **运输管理 \> 设置 \> 运输标准 \> NMFC 代码**。

1. 选择 **新建** 创建一个 NMFC 代码。 然后设置以下字段：

    - **NMFC 代码** – 输入商品类型的 NMFC 代码。
    - **名称** – 为 NMFC 代码输入一个名称。
    - **LTL 类** – 选择与 NMFC 代码关联的 LTL 类。
    - **BOL 处理单元** – 定义装运的默认处理类型。

## <a name="example-set-up-nmfc-codes"></a>示例：设置 NMFC 代码

下面的示例演示如何设置可以用于不同产品的两个不同的 NMFC 代码。

1. 转到 **仓库管理 \> 设置 \> 库存 \> NMFC 代码**。
1. 在操作窗格上，选择 **新建**。
1. 在新行中，设置以下值：

    - **NMFC 代码**：*92.5*
    - **名称**：*计算机*
    - **LTL 类**：*92.5*
    - **BOL 处理单元**：*单元*

1. 在操作窗格上，选择 **保存**。
1. 在操作窗格上，选择 **新建**。
1. 在新行中，设置以下值：

    - **NMFC 代码**：*125*
    - **名称**：*手机*
    - **LTL 类**：*125*
    - **BOL 处理单元**：*单元*

1. 在操作窗格上，选择 **保存**。

## <a name="additional-resources"></a>其他资源

- [小于货车荷载 (LTL) 类](ltl-class.md)
- [创建提单](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
