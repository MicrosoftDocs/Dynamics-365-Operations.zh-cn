---
title: 按照产品变型的度量单位转换
description: 本文说明如何为产品变型设置度量单位转换。 其中包括设置示例。
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: a605e510ac8faa1f92e105c9fcc30222ef78e05e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869624"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>按照产品变型的度量单位转换

[!include [banner](../includes/banner.md)]

本文说明如何为各种产品变型设置度量单位转换。

您可以使用产品变型创建单个产品的差异，而不是创建多个必须维护的单品。 例如，指定尺寸和颜色的 T 恤就是一个产品变型。

以前只能为基础产品设置单位转换。 因此，所有产品变型的单位转换规则都相同。 但是，如果开启了 *产品变型的度量单位转换* 功能，并且您的 T 恤成箱出售，而一箱中可容纳的 T 恤数量取决于 T 恤的尺寸，现在可以设置不同 T 恤的尺寸与包装箱之间的单位转换。

## <a name="turn-on-the-feature-in-your-system"></a>在系统中开启此功能

如果尚未在系统中看到此功能，请转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，然后开启 *产品变型的度量单位转换* 功能。

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>按变型为单位转换设置产品

只能为基础产品创建产品变型。 有关详细信息，请参阅[创建基础产品](tasks/create-product-master.md)。 为实际称重流程设置的产品不支持 *产品变型的度量单位转换* 功能。

若要将基础产品配置为支持按变型的单位转换，请执行以下步骤。

1. 转到 **产品信息管理 \> 产品 \> 基础产品**。
1. 创建或打开一个基础产品以转到其 **产品详细信息** 页。
1. 将 **启用度量单位转换** 选项设置为 *是*。
1. 在操作窗格的 **产品** 选项卡的 **设置** 组中，选择 **单位转换**。
1. 将打开 **单位转换** 页。 选择以下选项卡之一：

    - **类别内部转换** – 如果要在属于同一个单位类别的单位之间转换，请选择此选项卡。
    - **类别之间的转换** – 如果要在属于不同单位类别的单位之间转换，请选择此选项卡。

1. 选择 **新建** 添加新的单位转换。
1. 将 **创建转换的对象** 字段设置为以下值之一：

    - **产品** – 如果您选择此值，则可以为基础产品设置单位转换。 此单位转换用作没有为其定义任何单位转换的所有产品变型的应变计划。
    - **产品变型** – 如果您选择此值，则可以为特定产品变型设置单位转换。 请使用 **产品变型** 字段选择变型。

    ![添加新单位转换。](media/uom-new-conversion.png "添加新单位转换")

1. 请使用提供的其他字段设置单位转换。
1. 选择 **确定** 保存新单位转换。

> [!TIP]
> 可以从下面的任何页面打开产品或产品变型的 **单位转换** 页：
> 
> - 产品详细信息
> - 已发布产品详细信息
> - 已发布的产品变型

## <a name="example-scenario"></a>示例场景

在此方案中，一家公司公司销售小、中、大和特大号 T 恤。 T 恤被定义作为产品，不同的尺寸被定义为该产品的变型。 T 恤装在箱子里。 如果是小、中和大尺寸，每箱可以有五件。 但是，如果是特大尺寸，则每箱的空间只能放四件。

公司想要以单位 *件* 跟踪不同变型，但以单位 *箱* 销售。 对于小、中和大尺寸，库存单位与销售单位之间的转换为 1 箱 = 5 件。 对于特大尺寸，转换为 1 箱= 4 件。

1. 从 **T 恤** 产品的 **已发布产品详细信息** 页，打开 **单位转换** 页。
1. 在 **单位转换** 页，为 **特大** 已发布产品变型设置以下单位转换。

    | 字段                 | 设置                 |
    |-----------------------|-------------------------|
    | 创建转换的对象 | 产品变型         |
    | 产品变型       | T 恤 : : 特大 : : |
    | 源单位             | 箱                   |
    | 系数                | 4                       |
    | 目标单位               | 件                  |

1. 因为 **小**、**中** 和 **大** 产品变型全部在单位 *箱* 和 *件* 之间具有相同的单位转换，所以您可以在基础产品中为这些产品变型定义以下单位转换。

    | 字段                 | 设置 |
    |-----------------------|---------|
    | 创建转换的对象 | 产品 |
    | 产品               | T 恤 |
    | 源单位             | 箱   |
    | 系数                | 5       |
    | 目标单位               | 件  |

## <a name="using-excel-to-update-the-unit-conversions"></a>使用 Excel 更新单位转换

如果一个产品有大量采用不同单位转换的产品变型，最好将这些单位转换导出到 Microsoft Excel 工作簿，更新，然后发布回 Dynamics 365 Supply Chain Management。

若要将单位转换导出到 Excel，请在 **单位转换** 页的操作窗格上，选择 **在 Microsoft Office 中打开**。

## <a name="additional-resources"></a>其他资源

[管理度量单位](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]