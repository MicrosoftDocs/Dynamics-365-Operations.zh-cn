--- 
title: "为可配置产品设置基于属性的定价"
description: "此过程显示如何设置基于属性的定价。"
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 88402bef6fd5dad38a74795cd31a4046085d6db7
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>为可配置产品设置基于属性的定价

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何设置基于属性的定价。 首先必须有一个拥有一个或多个组件和属性的产品配置模型。 此示例使用 USMF 演示数据公司中的高端扬声器产品模型。 通常，产品经理使用此过程。


## <a name="create-a-new-price-model"></a>创建新的价格模型
1. 单击“产品变型模型定义”。
2. 单击“产品配置模型”。
3. 在列表中，选择“高端扬声器”行，但是不单击名称的链接。
4. 在“操作窗格”上单击“模型”。
5. 单击“价格模型”。
6. 单击“新建”。
7. 在“价格模型名称”字段中，键入一个值。
    * 使用易于识别模型的名称。  
8. 在“描述”字段中，键入一个值。
9. 单击“保存”。

## <a name="add-price-elements"></a>添加价格元素
1. 单击“编辑”。
    * 产品模型中的每个组件可以有一个基价元素和任意数量的价格表达式规则。 还可以添加不同币种的价格。  
2. 在“基价表达式”字段中，输入一个值。
    * 例如，键入“100”。   基价表达式可以是数值，也可以包含涉及一个或多个属性的算术计算。  
3. 单击“添加”。
4. 在“名称”字段中，键入“红木”。
    * 价格表达式名称帮助识别价格元素的含义。 在此示例中，我们为红木扬声器机箱装饰选件创建一个价格元素。  
5. 单击“编辑条件”。
    * 价格条件帮助确保仅当存在特定属性组合时，销售价中才包含价格表达式元素。  
6. 在“约束体”字段中，输入“机箱装饰 =="红木"”。
7. 单击“确定”。
8. 在“表达式”字段中，键入一个值。
    * 例如，键入“50”。  
9. 关闭该页面。
10. 关闭该页面。


