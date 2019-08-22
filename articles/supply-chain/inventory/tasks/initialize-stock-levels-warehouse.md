---
title: 初始化仓库中的库存级别
description: 该过程说明如何利用“库存移动日记帐”手动更新现有库存。
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbd6dc6c2e5b7c1abe6e19f00a5df285e0147a92
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845372"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>初始化仓库中的库存级别

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程说明如何利用“库存移动日记帐”手动更新现有库存。 （也可根据导入交易的数据实体更新现有库存。）您可以通过演示数据公司 USMF 运行此指南，通过它可以获得所有的必要条件，如日记帐名称、项目设置、过帐文件以及帐号。 该指南显示了所使用的物料和维度的特定值。 如果选择不同的项目，则需要输入不同的维度值。

1. 转到“库存管理”>“日记帐条目”>“物料”>“移动”。
2. 单击“新建”。
3. 在“名称”字段中，单击下拉按钮以打开查找。
4. 选择“IMov”。
    * 根据不同的业务用途使用不同的日记帐名称模板是一个很好的实践。  
5. 在列表中，单击所选行中的链接。
6. 在“抵消帐户”字段中，设定值“140200”。
    * 该抵消帐户将默认为日记帐行的帐户。 给抵消帐户每一行分配不同的名称可以覆盖默认帐户名称。  
7. 单击“确定”。
8. 单击“新建”。
9. 在“物料编号”字段中，单击下拉按钮以打开查找。
10. 选择物料 A0001。
11. 在列表中，单击所选行中的链接。
12. 单击“库存维度”选项卡。
13. 在“位置”字段中，单击下拉按钮打开查询。
14. 选择“站点 1”。
15. 在“仓库”字段，单击下拉按钮以打开查找。
16. 选择“仓库 13”。
17. 在列表中，单击所选行中的链接。
18. 在“地点”字段中，单击下拉按钮以打开查找。
19. 选择“库位 13”。
20. 在“数量”字段中，输入一个数字。
21. 单击“保存”。
22. 单击“过帐”。
23. 选中或取消选中“将所有错误过帐至一个新日记帐”的复选框。
    * 如果您选取该选项，任意行过帐失败都将被复制到一个新的日记帐中。 您可以利用原信息更正该问题，然后再过帐该行。  
24. 单击“确定”。
25. 关闭该页面。
26. 关闭该页面。

