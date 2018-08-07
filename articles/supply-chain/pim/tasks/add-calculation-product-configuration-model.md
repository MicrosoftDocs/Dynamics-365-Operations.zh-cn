--- 
title: "将计算添加到产品配置模型"
description: "该过程显示如何添加新计算到产品配置模型。"
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2db8fb922b085a7f118822ef4fd974ac338f4d99
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>将计算添加到产品配置模型

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程显示如何添加新计算到产品配置模型。 它显示如何通过使用“If”运算符将白色扬声器高度设置为 10，将所有其他完工机柜设置为 15 来创建逻辑表达式。 该过程使用演示公司 USMF 的高端扬声器组件。


## <a name="add-a-calculation"></a>添加一个计算

## <a name="create-calculation-expression"></a>创建计算表达式
1. 单击“编辑表达式”。
2. 在“约束体”字段中，输入“如果[完工机柜==“白色”，10, 15]”。
3. 单击“验证”。
4. 单击“关闭”。
5. 单击“确定”。


