---
title: 为配置的产品变型创建产品编号命名法
description: 此步骤显示如何为配置的产品变型设置产品编号命名法，以及如何将其附加到可配置的基础产品。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921003"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>为配置的产品变型创建产品编号命名法

[!include [banner](../../includes/banner.md)]

此步骤显示如何为配置的产品变型设置产品编号命名法，以及如何将其附加到可配置的基础产品。 此过程还演示如何为产品配置模型组件构建配置命名法。 创建此程序的演示数据公司是 USMF。 为基础产品 D0004 分配了新的产品编号命名法。 此任务通常由产品设计师完成。

## <a name="create-a-product-number-nomenclature"></a>创建产品编号命名法

1. 转到 **产品信息管理 \> 设置 \> 产品命名法**。
1. 选择 **新建**。
1. 在 **名称** 字段中，键入一个值。
1. 在 **描述** 字段中，键入一个值。
1. 选择 **添加**。
1. 选择 **基础产品编号**。
1. 选择 **添加**。
1. 选择 **文本常量**。
1. 在列表中，标记所选的行。
1. 在 **文本** 字段中，键入一个值。
1. 选择 **添加**。
1. 选择 **配置**。
1. 关闭该页面。

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>为基础产品分配产品编号命名法

1. 转到 **产品信息管理 \> 产品 \> 基础产品**。
1. 使用“快速筛选器”以查找记录。 例如，使用值“D”在 **产品编号** 字段中进行筛选。
1. 在列表中，选择所选择行中的链接。
1. 选择 **编辑**。
1. 在 **使用命名法** 字段中选择 *是*。
1. 在 **产品变型编号命名法** 字段中，输入或选择一个值。
1. 关闭该页面。
1. 关闭该页面。

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>为产品配置模型组件创建命名法

1. 转到 **产品信息管理 \> 产品 \> 产品配置模型**。
1. 在列表中，找到并选择所需记录。
1. 在列表中，选择所选择行中的链接。
1. 选择 **编辑**。
1. 在 **使用配置命名法** 字段中选择 *是*。
1. 选择 **添加**。
1. 选择 **属性值**。
1. 在列表中，标记所选的行。
1. 在 **属性** 字段中，输入或选择一个值。
1. 选择 **添加**。
1. 选择 **文本常量**。
1. 在列表中，标记所选的行。
1. 在 **文本** 字段中，键入一个值。
1. 选择 **添加**。
1. 选择 **属性值**。
1. 在列表中，标记所选的行。
1. 在 **属性** 字段中，输入或选择一个值。
1. 选择 **添加**。
1. 选择 **文本常量**。
1. 在列表中，标记所选的行。
1. 在 **文本** 字段中，键入一个值。
1. 选择 **添加**。
1. 选择 **属性值**。
1. 在列表中，标记所选的行。
1. 在 **属性** 字段中，输入或选择一个值。
1. 选择 **添加**。
1. 选择 **文本常量**。
1. 在列表中，标记所选的行。
1. 在 **文本** 字段中，键入一个值。
1. 选择 **添加**。
1. 选择 **属性值**。
1. 在列表中，标记所选的行。
1. 在 **属性** 字段中，输入或选择一个值。
1. 选择 **添加**。
1. 选择 **文本常量**。
1. 在列表中，标记所选的行。
1. 在 **文本** 字段中，键入一个值。
1. 选择 **添加**。
1. 选择 **编号规则值**。
1. 在列表中，标记所选的行。
1. 在 **编号规则** 字段中，输入或选择一个值。
1. 关闭该页面。
1. 关闭该页面。
1. 关闭该页面。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]