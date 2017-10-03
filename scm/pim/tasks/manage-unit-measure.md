--- 
title: "管理度量单位"
description: "此过程显示如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。"
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: de5baa1e5c30ee998d113f7366c445a65723dfdc
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="manage-unit-of-measure"></a>管理度量单位

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何定义度量单位，提供单位换算及其描述，以及定义相关单位的转换规则。 您可以使用演示数据或使用您自己的数据浏览此过程。

1. 转到“已发布产品的维护”。
2. 单击“单位”。

## <a name="create-a-unit-of-measure"></a>创建度量单位
1. 单击“新建”。
2. 在“单位”字段中，键入一个值。
    * 输入引用度量单位时使用的 ID 或符号。  
3. 在“描述”字段中，键入一个值。
    * 用系统语言输入度量单位的描述性名称。  
4. 在“单位类别”字段中，选择一个选项。
    * 单位类别定义逻辑分组，例如区域、质量或数量、度量单位所属的分组。  
5. 在“小数精度”字段中，输入一个数字。
    * 指定在计算度量单位时，度量单位转换必须舍入的小数位数。  
6. 单击“保存”。

## <a name="define-unit-translations"></a>定义单位转换
1. 单击“单位文本”。
2. 单击“新建”。
    * 使用单位文本创建 ID 或符号转换，代表供在外部文档中以客户或供应商特定语言使用的度量单位。  
3. 在“语言”字段中，输入或选择一个值。
4. 在“文本”字段中，键入一个值。
5. 单击“保存”。
6. 关闭该页面。
7. 单击“转换单位的描述”。
8. 单击“新建”。
    * 定义度量单位的特定语言描述。  
9. 在“语言”字段中，输入或选择一个值。
10. 在“描述”字段中，键入一个值。
11. 单击“保存”。
12. 关闭该页面。

## <a name="define-unit-conversion-rules"></a>定义单位换算规则
1. 单击“单位换算”。
    * 定义所选单位类别中的其他度量单位间的度量单位转换规则。  
2. 单击“新建”，以打开对话框。
3. 在“系数”字段中，输入一个数字。
    * 源单位和目标单位之间的换算系数。 例如，由于 100 厘米等于一米，则厘米到米的转换系数为 100。  
4. 在“目标单位”字段中，输入或选择一个值。
5. 在“舍入”字段中，选择一个选项。
    * 定义转换值应如何舍入。  
6. 单击“确定”。
7. 关闭该页面。


