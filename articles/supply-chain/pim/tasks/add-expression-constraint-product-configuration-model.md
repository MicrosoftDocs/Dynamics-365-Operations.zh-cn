---
title: 将表达式约束添加到产品配置模型
description: 该过程显示如何添加新的约束表达式到产品配置模型。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 411e20bd8631b70df981c5785f502693d5ba3705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987121"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>将表达式约束添加到产品配置模型

[!include [banner](../../includes/banner.md)]

该过程显示如何添加新的约束表达式到产品配置模型。 它显示，如果用户选择为金属的前格栅，应该如何授权必须应用于扬声器的护角。 该过程使用演示公司 USMF 的高端扬声器组件。


## <a name="create-an-expression-constraint"></a>创建一个表达式约束
1. 单击“产品变型模型定义”。
2. 单击“产品配置模型”。
3. 在列表中，找到并选择所需记录。
    * 此示例使用高端扬声器模型。  
4. 在列表中，单击所选行中的链接。
5. 展开“约束”部分。
6. 单击“添加”。
7. 单击“创建”。
8. 在“名称”字段中，键入一个值。

## <a name="enter-expression"></a>输入表达式
1. 单击“编辑表达式”。
    * 如果您解锁此阶段任务记录的用户界面，您可以使用 IntelliSense 和符号列表，以构建约束表达式。  
2. 在“约束体”字段中，输入“提示[前格栅==“金属”，护角]”。
    * 此表达逻辑表明：如果“前格栅”为金属，则必须选择护角选项。  
3. 单击“验证”。
    * 核实功能通过约束表达式运行并检查语法错误。  
4. 单击“关闭”。
5. 单击“确定”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]