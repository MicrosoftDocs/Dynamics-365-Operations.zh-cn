---
title: 创建预定义的产品变型
description: 此过程全面介绍如何使用产品维度的组合创建基础产品的产品变型。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 678e2d7207628529530dcf3decd094583d3dff22
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150096"
---
# <a name="create-predefined-product-variants"></a>创建预定义的产品变型

[!include [banner](../../includes/banner.md)]

此过程全面介绍如何使用产品维度的组合创建基础产品的产品变型。 创建此过程使用的演示数据公司为 USMF。


## <a name="create-a-product-master"></a>创建基础产品
1. 转到“产品信息管理”>“产品”>“基础产品”。
2. 单击“新建”。
3. 在“产品编号”字段中，键入一个值。
    * 如果尚未针对产品编号字段设置任何编号规则，则不需要手动输入产品编号。 换言之，如果已为该字段设置了编号规则，则跳过此步骤。  
4. 在“产品名称”字段中，键入一个值。
5. 在“产品维度组”字段中，输入或选择一个值。
    * 选择产品维度组 SizeCol（尺寸和颜色）。  
6. 单击“确定”。

## <a name="add-product-dimensions"></a>添加产品维度
1. 单击“产品维度”。
    * 此示例显示如何手动输入产品维度。 您还可以选择选择包括您要使用的产品维度值的尺寸、颜色或样式组。  
2. 单击“新建”。
3. 在列表中，标记所选的行。
4. 在“尺寸”字段中，输入或选择一个值。
5. 在“名称”字段中，键入一个值。
6. 单击“新建”。
7. 在列表中，标记所选的行。
8. 在“尺寸”字段中，输入或选择一个值。
9. 在“名称”字段中，键入一个值。
10. 单击“颜色”选项卡。
11. 单击“新建”。
12. 在列表中，标记所选的行。
13. 在“颜色”字段中，输入或选择一个值。
14. 在“名称”字段中，键入一个值。
15. 单击“新建”。
16. 在列表中，标记所选的行。
17. 在“颜色”字段中，输入或选择一个值。
18. 在“名称”字段中，键入一个值。
19. 单击“保存”。
20. 关闭该页面。

## <a name="generate-product-variants"></a>生成产品变型
1. 单击“产品变型”。
2. 单击“变型建议”。
3. 单击“选择全部”。
    * 在此示例中，选择所有可能的变型。 如果仅可能的产品维度组合的子集将用于创建变型，则您可以选择单个条目。  
4. 单击“创建”。
    * 您可以基于产品维度值的组合生成所有变型的描述。 描述是可选的。  
5. 单击“保存”。

