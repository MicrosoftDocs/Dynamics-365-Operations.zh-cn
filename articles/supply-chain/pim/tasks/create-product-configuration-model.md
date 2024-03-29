---
title: 创建产品配置模型
description: 该过程显示如何创建产品配置模型和输入基础信息，如属性和子组件。
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca99c0346a3f982164076167c3429587aac18be6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568416"
---
# <a name="create-a-product-configuration-model"></a>创建产品配置模型

[!include [banner](../../includes/banner.md)]

该过程显示如何创建产品配置模型和输入基础信息，如属性和子组件。 创建此程序的演示数据公司是 USMF。


## <a name="create-a-product-model"></a>创建产品模型

1. 转到 **产品信息管理 \> 产品 \> 产品配置模型**。
1. 选择 **新建**。
1. 在 **名称** 字段中，键入一个值。
1. 在 **描述** 字段中，键入一个值。
1. 在 **求解器策略** 字段中，选择一个选项。
    * 求解器策略确定如何处理基于约束的产品配置模型中的约束。 此选择可对产品配置模型的性能造成影响。  
1. 在 **名称** 字段中，键入一个值。
    * 根组件表示产品配置模型，但是还可用于其他产品模型中。  
1. 选择 **确定**。
1. 在 **重复使用配置** 字段中，选择一个选项。
    * 如果重复使用配置参数设置为“是”，且在每一配置会话和重复使用后发现有完全匹配，系统将检查相同的配置。  

## <a name="add-attributes"></a>添加属性

1. 展开 **属性** 部分。
2. 选择 **添加**。
3. 在列表中，标记所选的行。
4. 在 **名称** 字段中，键入一个值。
5. 在 **求解器名称** 字段中，键入一个值。
    * 求解器名称由产品配置器的约束求解器使用。 该名称不能包含空格或特殊字符（下划线 _ 除外）。  
6. 在 **描述** 字段中，键入一个值。
    * 描述文本将显示给配置用户，因此可帮助选择正确的属性值。  
7. 在 **属性类型** 字段中，输入或选择一个值。
    * 属性类型确定可供属性使用的值。  
8. 在 **加入重复使用** 复选框。
    * 该选项只有选择“重复使用配置”选项后才可用。 在“重复使用”复选框中加入属性表示，在系统寻找完全匹配时将考虑该属性。  

## <a name="add-subcomponents"></a>添加子组件

1. 展开 **子组件** 部分。
2. 选择 **添加**。
3. 在列表中，标记所选的行。
4. 在 **名称** 字段中，键入一个值。
5. 在 **求解器名称** 字段中，键入一个值。
6. 在 **描述** 字段中，键入一个值。
7. 在 **组件** 字段中，输入或选择一个值。
    * 每个子组件必须引用一个组件定义。 此设计支持可重复使用的组件，并确保一旦定义一个组件，其可用于许多产品模型中。  
8. 选择 **保存**。
9. 选择 **物料清单行详细信息**。
    * 物料清单行详细信息窗体使得用户能够为子组件选择所需的属性。 每一性能可被给予固定值或映射到一个属性。 映射到一个属性将导致物料清单行性能有不同的值（取决于配置选择）。  
10. 在 **物料编号** 字段中，输入或选择一个值。
    * 每一子组件表示含基于约束的配置技术的可配置基础产品。 此引用通过物料编号作出。  
11. 选择 **设置** 复选框。
12. 在 **计算** 字段中选择 **是**。
    * 设置计算选项，确保在运行产品成本计算时将产品包含在内。  
13. 选择 **设置** 选项卡。
14. 选择 **设置** 复选框。
15. 在 **数量** 字段中，输入一个数字。
    * “数量”字段确定在配置产品中消耗的产品数量。  
16. 选择 **设置** 复选框。
17. 在 **每个系列** 字段中，输入一个数字。
18. 选择 **确定**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]