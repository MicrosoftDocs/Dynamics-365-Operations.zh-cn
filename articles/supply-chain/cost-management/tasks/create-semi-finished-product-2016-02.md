--- 
title: "创建半成品（仅 2016 年 2 月）"
description: "此任务的重点是创建半成品。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4d06f291036c656731a00fcf312e229ed9e9f3d0
ms.openlocfilehash: 038d8cd9333635d3269bb4f62a5402c2309bfd3c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-semi-finished-product-february-2016-only"></a>创建半成品（仅 2016 年 2 月）

[!include[task guide banner](../../includes/task-guide-banner.md)]

此任务的重点是创建半成品。 这是 BOM 计算系列中的第二个任务。 创建此任务的演示数据公司是 USMF。

1. 转到“产品信息管理”>“产品”>“已发布产品”。
2. 单击“新建”。
3. 在“产品编号”字段中，键入一个值。
    * 在这个例子中，输入“BOM_2”。  
4. 在“物料模型组”字段中，输入或选择一个值。
    * 选择“标准”。 “标准”指的是标准成本，是计算成本时最常用的模型。  
5. 在“物料组”字段中，输入或选择一个值。
    * 例如，选择“音频”。 这不影响成本计算。  
6. 在“存储维度组”字段中，输入或选择一个值。
    * 选择“SiteWH”。 将对此示例仅使用站点和仓库。  
7. 在“跟踪维度组”字段中，输入或选择一个值。
    * 将不对此示例使用跟踪维度。请选择"无"。  
8. 单击“确定”。
9. 在“操作窗格”上，单击“库存管理”。
10. 点击默认订单设置。
11. 在“默认订单类型”字段中，选择“生产”。
    * 因为这是将生产的半成品，所以请选择“生产”。  
12. 在“采购站点”字段中，输入或选择一个值。
    * 在这个例子中选择“站点 1”。  
13. 在“库存站点”字段中，输入或选择一个值。
    * 在这个例子中选择“站点 1”。  
14. 在“销售站点”字段中，输入或选择一个值。
    * 在这个例子中选择“站点 1”。  
15. 关闭该页面。
16. 在“操作窗格”中，单击“管理成本”。
17. 单击“物料价格”。
18. 单击“新建”。
19. 在列表中，标记所选的行。
20. 在“版本”字段中，输入或选择一个值。
    * 在这个例子中选择“版本 10”。  
21. 在“站点”字段中，输入或选择一个值。
    * 在这个例子中选择“站点 1”。  
22. 将“价格”设为“10”。
    * 对于此示例，请输入成本价 10。  
23. 单击“保存”。
24. 单击“激活未决价格”。
25. 关闭该页面。
26. 关闭该页面。
27. 单击“BOM_2”将其打开。
28. 展开“管理成本”部分。
29. 在“成本组”字段中，输入或选择一个值。
    * 在这个例子中，选择“成本组 M1”。  
30. 使用保存记录的快捷方式。
31. 关闭该页面。


