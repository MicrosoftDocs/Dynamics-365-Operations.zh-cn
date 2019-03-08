---
title: 为配置的产品变型创建产品编号命名法
description: 此步骤显示如何为配置的产品变型设置产品编号命名法，以及如何将其附加到可配置的基础产品。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 800afdf075f0675185514158f3b712a0fe7675e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "336075"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>为配置的产品变型创建产品编号命名法

[!include [task guide banner](../../includes/task-guide-banner.md)]

此步骤显示如何为配置的产品变型设置产品编号命名法，以及如何将其附加到可配置的基础产品。 此过程还演示如何为产品配置模型组件构建配置命名法。 创建此程序的演示数据公司是 USMF。 为基础产品 D0004 分配了新的产品编号命名法。 此任务通常由产品设计师完成。


## <a name="create-a-product-number-nomenclature"></a>创建产品编号命名法
1. 单击“产品变型模型定义”。
2. 单击“产品命名法”。
3. 单击“新建”。
4. 在“名称”字段中，键入一个值。
5. 在“描述”字段中，键入一个值。
6. 单击“添加”。
7. 单击“基础产品编号”。
8. 单击“添加”。
9. 单击“文本常量”。
10. 在列表中，标记所选的行。
11. 在“文本”字段中，键入一个值。
12. 单击“添加”。
13. 单击“配置”。
14. 关闭该页面。

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>为基础产品分配产品编号命名法
1. 单击“基础产品”。
2. 使用“快速筛选器”以查找记录。 例如，使用值“D”在“产品编号”字段中进行筛选。
3. 在列表中，单击所选行中的链接。
4. 单击“编辑”。
5. 在“使用命名法”字段中选择“是”。
6. 在“产品变型编号命名法”字段中，输入或选择一个值。
7. 关闭该页面。
8. 关闭该页面。

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>为产品配置模型组件创建命名法
1. 单击“产品配置模型”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 单击“编辑”。
5. 在“使用配置命名法”字段中选择“是”。
6. 单击“添加”。
7. 单击“属性值”。
8. 在列表中，标记所选的行。
9. 在“属性”字段中，输入或选择一个值。
10. 单击“添加”。
11. 单击“文本常量”。
12. 在列表中，标记所选的行。
13. 在“文本”字段中，键入一个值。
14. 单击“添加”。
15. 单击“属性值”。
16. 在列表中，标记所选的行。
17. 在“属性”字段中，输入或选择一个值。
18. 单击“添加”。
19. 单击“文本常量”。
20. 在列表中，标记所选的行。
21. 在“文本”字段中，键入一个值。
22. 单击“添加”。
23. 单击“属性值”。
24. 在列表中，标记所选的行。
25. 在“属性”字段中，输入或选择一个值。
26. 单击“添加”。
27. 单击“文本常量”。
28. 在列表中，标记所选的行。
29. 在“文本”字段中，键入一个值。
30. 单击“添加”。
31. 单击“属性值”。
32. 在列表中，标记所选的行。
33. 在“属性”字段中，输入或选择一个值。
34. 单击“添加”。
35. 单击“文本常量”。
36. 在列表中，标记所选的行。
37. 在“文本”字段中，键入一个值。
38. 单击“添加”。
39. 单击“编号规则值”。
40. 在列表中，标记所选的行。
41. 在“编号规则”字段中，输入或选一个值。
42. 关闭该页面。
43. 关闭该页面。
44. 关闭该页面。

