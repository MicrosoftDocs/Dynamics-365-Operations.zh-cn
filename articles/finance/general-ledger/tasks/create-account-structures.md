---
title: 创建科目结构
description: 此任务指南介绍创建科目结构的步骤。
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a8df7d7d9c4555bf46ac1cc3f71695837b1369b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968571"
---
# <a name="create-account-structures"></a>创建科目结构

[!include [banner](../../includes/banner.md)]

此任务指南介绍创建科目结构的步骤。 步骤使用演示数据公司 USMF。

1. 转到 **导航窗格 > 模块 > 总帐 > 会计科目表 > 结构 > 配置科目结构**。
2. 在 **操作窗格** 中，单击 **新建** 打开对话框。
3. 在 **科目结构** 字段中，输入描述科目结构的用途的名称。
4. 在 **描述** 字段中，输入指出科目结构用途的描述。
5. 单击 **创建**。
6. 在 **段落和允许的值**，单击 **添加段落**。
7. 在维度列表中，选择要添加到科目结构的维度。
8. 在列表末尾，单击 **添加段落**。
9. 根据需要重复步骤 6 到 9。
10. 在 **允许的值详细信息** 部分中，选择分部以编辑允许的值。
    例如，单击 **主科目** 字段。  
11. 在 **运算符** 字段中，选择一个选项，例如“介于并包含”。
12. 在 **值** 字段中，键入一个值。 例如：600000。  
13. 在 **范围** 字段中，键入一个值。 例如：699999。  
14. 在 **允许的值详细信息** 部分中，单击 **应用**。
15. 根据需要重复步骤 10 到 15。  
16. 在 **允许的值详细信息** 部分中，单击 **添加新条件**。
17. 在“运算符”字段中，选择一个选项，例如“介于并包含”。
18. 在 **值** 字段中，键入一个值。 例如：033。  
19. 在 **范围** 字段中，键入一个值。 例如：034。  
20. 单击 **应用**。
21. 在网格中，选择分部以编辑允许的值。 例如：成本中心。  
22. 在 **成本中心** 字段中，键入一个值。 例如：007..021。  
23. 在 **段落和允许的值**，单击 **添加**。
24. 在 **主科目** 字段中，键入一个值。 例如：600000..699999  
25. 在网格中，选择分部以编辑允许的值。 例如：部门。  
26. 在“部门”字段中，键入一个值。 例如：032。  
27. 在“成本中心”字段中，键入一个值。 例如：086。  
28. 在 **操作窗格** 上，单击 **验证**。
29. 在 **操作窗格** 上，单击 **激活**。
30. 单击 **启用**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]