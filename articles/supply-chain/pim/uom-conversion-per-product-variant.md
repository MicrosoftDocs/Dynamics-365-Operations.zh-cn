---
title: 按照产品变型的度量单位转换
description: 本主题说明如何在产品变型中设置度量单位转换。
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573226"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>按照产品变型的度量单位转换

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

本主题说明如何在产品变型中设置度量单位转换。 其中包括设置示例。

此功能使公司可以定义同一产品变型之间的不同单位换算。 以下示例将用于此主题。 公司销售小、中、大和特大号 T 恤。 T 恤被定义作为产品，不同的尺寸被定义为产品变型。 T 恤按箱打包，一箱可以有五件 T 恤，除了特大号外，只剩放四件 T 恤的空间。 公司想要以单位**件**跟踪不同的 T 恤变型，但以单位**箱**销售 T 恤。 库存单位和销售单位之间的转换为 1 箱 = 5 件，除了变型“特大号”外，转换为 1 箱 = 4 件。

## <a name="setup"></a>设置

您可以通过使用**产品信息参数**页上的**启用度量单位转换**选项来配置参数，以为启用了**所有流程**的产品使用此功能，或仅为启用了**仓库流程**的产品使用此功能。

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>按变型为单位转换设置产品

产品变型只能为**产品子类型**：**产品基础**的产品创建。 有关详细信息，请参阅[创建基础产品](tasks/create-product-master.md)。

此功能没有为为实际称重流程设置的产品启用。 

通过使用**产品详细信息**页的**启用度量单位转换**选项，在基础产品创建时启用度量单位转换。

当创建具有已发布产品变型的基础产品时，可以设置每个变型的单位转换。 您可以在以下页面找到用于在产品或产品变型上下文中打开单位转换页面的菜单项。

-   **产品详细信息**页面
-   **已发布产品详细信息**页面
-   **已发布产品变型**页面

当您在基础产品或已发布产品变型的上下文中打开**单位转换**页时，您可以选择是否要为产品或产品变型设置单位转换。 您通过在**创建转换的对象**字段中选择**产品变型**或**产品**来执行此操作。

### <a name="product-variant"></a>产品变型

如果您选择**产品变型**，那么您可以在**产品变型**字段中选择要为其设置单位转换的变型。

### <a name="product"></a>产品

如果您选择**产品**，则可以为基础产品设置单位转换。 此单位转换将应用于未定义单位转换的所有产品变型。

### <a name="example"></a>示例

基础产品 **T 恤**有四个已发布的产品变型：小、中、大和特大。 T 恤按箱打包，一箱可以有五件 T 恤，除了特大号外，只剩放四件 T 恤的空间。

首先，请从 **T 恤**的“已发放产品详细信息”页打开**单位转换**页。

在**单位转换**页上，为已发布的产品变型“特大”设置单位转换。

| **字段**             | **设置**             |
|-----------------------|-------------------------|
| 创建转换的对象 | 产品变型         |
| 产品变型       | T 恤 : : 特大 : : |
| 源单位             | 箱                   |
| 系数                | 4                       |
| 目标单位               | 件                  |

已发布的产品变型“小、中和大”在“箱”和“件”之间具有相同的单位转换，也就是说，您可以为基础产品的这些产品变型定义单位转换。

| **字段**             | **设置** |
|-----------------------|-------------|
| 创建转换的对象 | 产品     |
| 产品               | T 恤     |
| 源单位             | 箱       |
| 系数                | 5           |
| 目标单位               | 件      |

### <a name="using-excel-to-update-the-unit-conversions"></a>使用 Excel 更新单位转换

如果产品有多个具有不同单位转换的产品变型，从**单位转换**页将单位转换导出到 Excel 电子表格，更新转换，然后将其发布回 Finance and Operations 是一个好主意。

导出到 Excel 并将编辑发布回 Finance and Operations 的选项从**单位转换**页的“操作窗格”上的**在 Microsoft office 中打开**菜单项启用。
