---
title: 将表达式约束添加到产品配置模型
description: 该过程显示如何添加新的约束表达式到产品配置模型。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920873"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>将表达式约束添加到产品配置模型

[!include [banner](../../includes/banner.md)]

该过程显示如何添加新的约束表达式到产品配置模型。 它显示，如果用户选择为金属的前格栅，应该如何授权必须应用于扬声器的护角。 该过程使用演示公司 USMF 的高端扬声器组件。

## <a name="create-an-expression-constraint"></a>创建一个表达式约束

1. 转到 **产品信息管理 \> 产品 \> 产品配置模型**。
3. 在列表中，找到并选择所需记录。
    * 此示例使用高端扬声器模型。  
4. 在列表中，选择所选择行中的链接。
5. 展开 **约束** 部分。
6. 选择 **添加**。
7. 选择 **创建**。
8. 在 **名称** 字段中，键入一个值。

## <a name="enter-expression"></a>输入表达式

1. 选择 **编辑表达式**。
    * 如果您解锁此阶段任务记录的用户界面，您可以使用 IntelliSense 和符号列表，以构建约束表达式。  
2. 在 **ConstraintBody** 字段中，输入“Implies[FrontGrill=="Metal", CornerProtection]”。
    * 此表达逻辑表明：如果“前格栅”为金属，则必须选择护角选项。  
3. 选择 **验证**。
    * 核实功能通过约束表达式运行并检查语法错误。  
4. 选择 **关闭**。
5. 选择 **确定**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]