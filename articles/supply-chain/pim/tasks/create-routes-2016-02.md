---
title: 创建工艺路线（2016 年 2 月）
description: 此任务的重点是为一件成品和一件半成品创建生产工艺路线。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567824"
---
# <a name="create-routes-february-2016"></a>创建工艺路线（2016 年 2 月）

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务的重点是为一件成品和一件半成品创建生产工艺路线。 这是 BOM 计算系列中的第五个任务。 创建此任务的演示数据公司是 USMF。


## <a name="create-a-route-for-a-semi-finished-product"></a>为一件半成品创建工艺路线
1. 转到“产品信息管理”>“产品”>“已发布产品”。
2. 在列表中，单击所选行中的链接。
    * 选择物料编号 BOM_2。  
3. 在“操作”窗格上，单击“设计”。
4. 单击“路径”。
5. 单击“新建”。
6. 单击“工艺路线”和“工艺路线版本”。
7. 在“描述”字段中，键入一个值。
    * 例如，键入“ROUTE_2”。  
8. 在“站点”字段中，输入或选择一个值。
    * 在这个例子中，请输入或选择“站点 1”.  
9. 单击“确定”。
10. 单击“新建”。
11. 在“运营”字段中，输入或选择一个值。
    * 在这个例子中，选择“组装件”。  
12. 在“运行时间”字段中，输入一个数字。
    * 例如，键入“1”。 运行时间通常是为某项计算的价格的组成部分。  
13. 在“路线组”字段中，输入或选择一个值。
    * 在这个例子中，选择“标准”。  
14. 单击“设置”选项卡。
15. 在“创建类别”字段中，输入或选择一个值。
    * 在这个例子中，选择“组装件”。  
16. 单击“时间”选项卡。
17. 在“设置时间”字段中，输入一个数字。
    * 在这个例子中，输入 1。 设置时间通常是为某项计算的价格的组成部分。  
18. 在“操作窗格”上单击“工艺路线版本”。
19. 单击“审核”。
20. 在“是否还要审核该工艺路线?“字段中选择”是“。
21. 单击“确定”。
22. 在“操作窗格”上单击“工艺路线版本”。
23. 单击“启用”。
24. 关闭该页面。
25. 关闭该页面。

## <a name="create-a-route-for-a-finished-product"></a>创建成品的工艺路线
1. 在列表中，单击所选行中的链接。
    * 选择物料编号 BOM_1。  
2. 在“操作”窗格上，单击“设计”。
3. 单击“路径”。
4. 单击“新建”。
5. 单击“工艺路线”和“工艺路线版本”。
6. 在“描述”字段中，键入一个值。
    * 在这个例子中，键入“ROUTE_1”。  
7. 在“站点”字段中，输入或选择一个值。
    * 在这个例子中，请输入或选择“站点 1”.  
8. 单击“确定”。
9. 单击“新建”。
10. 在“运营”字段中，输入或选择一个值。
    * 在这个例子中，选择“包装”。  
11. 在“运行时间”字段中，输入一个数字。
    * 在这个例子中，输入 1。  
12. 在“路线组”字段中，输入或选择一个值。
    * 在这个例子中，选择“标准”。  
13. 单击“设置”选项卡。
14. 在“创建类别”字段中，输入或选择一个值。
    * 在这个例子中，选择“包装”。  
15. 单击“时间”选项卡。
16. 在“设置时间”字段中，输入一个数字。
    * 在这个例子中，输入 1。  
17. 在“操作窗格”上单击“工艺路线版本”。
18. 单击“审核”。
19. 单击“确定”。
20. 在“操作窗格”上单击“工艺路线版本”。
21. 单击“启用”。
22. 关闭该页面。
23. 关闭该页面。

## <a name="enable-automatic-consumption-of-setup-time"></a>启用自动消耗设置时间
1. 转到“生产控制 > 设置 > 工艺路线 > 工艺路线组”。
2. 在列表中，找到并选择所需记录。
    * 选择列表中的“标准”。  
3. 单击“编辑”。
4. 在“设置时间”字段中，选择“是”。
    * 设置时间通常是为某项计算的价格的组成部分。  
5. 单击“保存”。
6. 关闭该页面。

