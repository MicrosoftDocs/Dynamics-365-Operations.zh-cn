---
title: 创建预定义的产品变型
description: 此过程全面介绍如何使用产品维度的组合创建基础产品的产品变型。
author: t-benebo
ms.date: 08/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a26439b8c7346cdce2b4c9804493fea94c29ac31
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335906"
---
# <a name="predefined-product-variants"></a>预定义的产品变型

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>示例场景：创建预定义的产品变型

此示例场景演示如何使用产品维度的组合创建基础产品的产品变型。

### <a name="make-demo-data-available"></a>提供演示数据

要使用此处建议的值来练习此场景，必须安装演示数据，并且必须选择 *USMF* 法人。

### <a name="step-1-create-a-product-master"></a>步骤 1：创建基础产品

创建基础产品：

1. 转到 **产品信息管理 > 产品 > 基础产品**。
1. 选择 **新建**。
1. 如果 **产品编号** 字段尚未显示数字，则输入一个值。 仅当未为此字段设置编号规则时才需要此操作。
1. 在 **产品名称** 字段中输入一个名称。
1. 在 **产品维度组** 字段中，选择产品维度组 *SizeCol*（尺寸和颜色）。
1. 选择 **确定** 创建并打开新基础产品。

### <a name="step-2-add-product-dimensions"></a>步骤 2：添加产品维度

此示例显示如何手动输入产品维度。 您还可以选择选择包括您要使用的产品维度值的尺寸、颜色或样式组。

添加产品维度：

1. 在您的新基础产品仍然打开的情况下，在操作窗格上选择 **产品维度**。
1. 打开 **尺寸** 选项卡，在工具栏上选择 **新建** 在网格中添加一行。 对新行进行以下设置：
    - **尺寸：** 选择一个尺寸值。
    - **名称：** 为尺寸输入一个名称。
1. 在工具栏上选择 **新建**，使用新的 **尺寸** 和 **名称** 向网格添加第二个尺寸。
1. 打开 **颜色** 选项卡，在工具栏上选择 **新建** 在网格中添加一行。 对新行进行以下设置：
    - **颜色：** 选择一个颜色值。
    - **名称：** 为颜色输入一个名称。
1. 在工具栏上选择 **新建**，使用新的 **颜色** 和 **名称** 向网格添加第二个颜色。
1. 选择 **保存**。
1. 关闭页面返回到新基础产品。

### <a name="step-3-generate-product-variants"></a>步骤 3：生成产品变型

> [!NOTE]
> 此节介绍未启用 *变型建议页改进* 功能时如何生成产品变型。 有关如何在该功能可用时生成产品变型的详细信息，请参阅下一节。

生成产品变型：

1. 在您的新基础产品仍然打开的情况下，在操作窗格上选择 **产品变型**。
1. 在操作窗格上选择 **变型建议**。
1. 系统将生成一个列表，其中包含您为产品定义的尺寸和颜色的所有可能组合。 在工具栏上选择 **全选**。
    - 在此示例中，选择所有可能的变型。 如果您只想使用可能的产品维度组合的子集，则根据需要只选中所需的复选框。  
1. 选择 **创建**。
1. 选择 **保存**。

## <a name="improved-variant-suggestions"></a>改进的变型建议

*变型建议页改进* 功能将改进 **变型建议** 页，为具有大量产品维度组合的公司解决性能和可用性问题。 选择要生成变型建议的产品维度值的增强流程可以更快、更轻松地识别和发布相关的产品变型集。

此功能添加了以下改进：

- **延迟生成变型建议**：**变型建议** 页在您第一次打开时不再显示建议。 您必须明确选择所需的值，然后选择 **建议** 按钮生成组合。 这使流程更具可见性和交互性。
- **选择维度值：** 当您有多个维度值时，您通常会希望生成仅包含其中几个维度值的变型建议（如在引入一组新的颜色或样式时）。 通过改进的设计，您可以选择要生成产品变型建议的维度值。 这将显著提高所建议变型的相关性，并提高系统性能和用户生产率。

### <a name="turn-the-variant-suggestions-page-improvements-feature-on-or-off"></a>打开或关闭“变型建议页改进”功能

要使用此功能，必须为您的系统打开它。 从 Supply Chain Management 版本 10.0.25 开始，此功能默认开启。 从 Supply Chain Management 版本 10.0.29 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.29，管理员可以通过在 [功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *变型建议页改进* 功能来打开或关闭此功能。

### <a name="work-with-the-improved-variant-suggestions"></a>使用改进的变型建议

在启用 *变型建议页改进* 功能时生成产品变型建议：

1. 如上一节所述，打开或创建基础产品并向其添加所需的产品维度。
1. 在基础产品打开的情况下，在操作窗格上选择 **产品变型**。
1. 在操作窗格上选择 **变型建议**。
1. 选择要用于每个维度的值。
1. 在顶部工具栏上，选择 **建议**。
1. 系统将生成一个列表，其中包含您选择的尺寸和颜色的所有可能组合。 在 **建议的变型** 快速选项卡上，选中要使用的每个产品维度组合的复选框，或在工具栏上选择 **全选** 全部选择。  
1. 选择 **创建** 将变型添加到当前的基础产品中。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
