---
title: 为可配置产品设置基于属性的定价
description: 本主题介绍如何设置基于属性的定价。
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5abb2e7dc33b46589c1a3699e70b56af6f694aed49294eb81a2122db6d414a96
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743546"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>为可配置产品设置基于属性的定价

[!include [banner](../../includes/banner.md)]

本主题介绍如何设置基于属性的定价。 首先必须有一个拥有一个或多个组件和属性的产品配置模型。 此示例使用 USMF 演示数据公司中的高端扬声器产品模型。 通常，产品经理使用此过程。


## <a name="create-a-new-price-model"></a>创建新的价格模型

1. 转到 **产品信息管理 \> 产品 \> 产品配置模型**。
1. 在列表中，选择 **高端扬声器** 行，但是不选择名称的链接。
1. 在操作窗格上，选择 **模型**。
1. 选择 **价格模型**。
1. 选择 **新建**。
1. 在 **价格模型名称** 字段中，键入一个值。 使用易于识别模型的名称。  
1. 在 **描述** 字段中，键入一个值。
1. 选择 **保存**。

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