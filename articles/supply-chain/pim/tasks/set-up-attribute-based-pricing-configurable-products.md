---
title: 为可配置产品设置基于属性的定价
description: 本主题介绍如何设置基于属性的定价。
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e540e0f25afa65e84cdb11fb0c56437b72891f9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220744"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>为可配置产品设置基于属性的定价

[!include [banner](../../includes/banner.md)]

本主题介绍如何设置基于属性的定价。 首先必须有一个拥有一个或多个组件和属性的产品配置模型。 此示例使用 USMF 演示数据公司中的高端扬声器产品模型。 通常，产品经理使用此过程。


## <a name="create-a-new-price-model"></a>创建新的价格模型
1. 选择主页上的 **产品变型定义**。
2. 选择 **链接** 部分中的 **产品配置模型**。
3. 在列表中，选择 **高端扬声器** 行，但是不选择名称的链接。
4. 在操作窗格上，选择 **模型**。
5. 选择 **价格模型**。
6. 选择 **新建**。
7. 在 **价格模型名称** 字段中，键入一个值。 使用易于识别模型的名称。  
8. 在 **描述** 字段中，键入一个值。
9. 选择 **保存**。

## <a name="add-price-elements"></a>添加价格元素
1. 选择 **编辑**。 产品模型中的每个组件可以有一个基价元素和任意数量的价格表达式规则。 还可以添加不同币种的价格。  
2. 在 **基价表达式** 字段中，输入一个值。 例如，键入“100”。 基价表达式可以是数值，也可以包含涉及一个或多个属性的算术计算。  
3. 选择 **添加**。
4. 在 **名称** 字段中，键入 `Rosewood`。 价格表达式名称帮助识别价格元素的含义。 在此示例中，我们为红木扬声器机箱装饰选件创建一个价格元素。  
5. 选择 **编辑条件**。 价格条件帮助确保仅当存在特定属性组合时，销售价中才包含价格表达式元素。  
6. 在 **ConstraintBody** 字段中，输入 `CabinetFinish=="Rosewood"`。
7. 选择 **确定**。
8. 在 **表达式** 字段中，键入一个值。 例如，键入 `50`。 
9. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]