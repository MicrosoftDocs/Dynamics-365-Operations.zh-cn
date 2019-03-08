---
title: 创建采购目录
description: 此指南演示如何创建采购目录。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f2a010e21f16b3908a6ee5f18d8f144c5130be7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "314685"
---
# <a name="create-a-procurement-catalog"></a>创建采购目录

[!include [task guide banner](../../includes/task-guide-banner.md)]

此指南演示如何创建采购目录。 此任务通常由采购专业人员完成。 您还将了解员工在创建申请时如何使用目录。 系统中必须已有采购类别层次结构，才能创建目录。 新目录继承层次结构，以及其中的所有产品。 可在采购类别层次结构可用的演示数据公司 USMF 中使用此指南，以及使用前面的步骤中使用的示例。


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>确保存在采购类别层次结构。
1. 转到采购>采购目录。 
    * USMF 演示数据公司中可使用采购目录层次结构，并且产品已添加到“办公设备/计算机”类别。 如果您正在运行该过程以作为任务指南，并且要浏览类别，您需要解锁该指南。 如果层次结构不可用，可通过单击“新建”创建。 此操作只能执行一次。  
2. 关闭该页面。

## <a name="create-a-catalog"></a>创建目录
1. 转到“采购”>“目录”>“采购目录”。
2. 单击“新采购目录”以打开下拉对话框。
3. 在“名称”字段中，键入一个值。
4. 单击“确定”。
5. 在树中，展开“企业采购类别”。
6. 在树中，展开“办公设备”。
7. 在树中，选择“计算机”。
    * 列表中将显示采购类别中的产品。 如果要向类别添加产品，需要在“采购列表层次结构”页或“物料详细信息”页中执行此操作。  
    * 默认更新类型确定已添加到采购类别层次结构的新产品是否在目录中立即显示。 如果更新类型设置为“动态”，将立即显示更改。 如果更新类型为“静态”，则新产品仅在已重新发布目录后对使用该目录的人员显示。 页面顶部的操作窗格中支持发布操作。 如果从采购类别层次结构删除产品，无论“默认更新类型”字段中是哪个值，都将立即显示更改。  
8. 在列表中，找到并选择所需记录。
9. 点击“隐藏”。
10. 在“操作窗格”上单击“类别导航”。
11. 单击“禁用”。
12. 在“操作窗格”上单击“类别导航”。
13. 单击“启用”。
14. 单击“启用目录”。
15. 关闭该页面。

## <a name="make-the-catalog-visible"></a>显示目录
1. 转到“采购”>“设置”>“策略”>“采购策略”。
2. 选择“采购政策 USMF”。
    * 您需要连接到您的用户配置文件的工作人员获准订购其产品的法人选择采购政策。 在 USMF 演示数据中，Admin 用户连接到工作人员 Julia Funderburk，而默认情况下该工作人员可订购 USMF 中的产品。  
3. 在列表中，单击所选行中的链接。
4. 选择您刚创建的目录。
5. 单击“确定”。
6. 关闭该页面。
7. 关闭该页面。

## <a name="use-the-catalog"></a>使用目录
1. 转到“采购”>“采购申请”>“所有采购申请”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 单击“确定”。
5. 单击 添加产品。
6. 在列表中，找到并选择所需记录。
    * 您可以使用左侧的类别层次结构或列表顶部的筛选器筛选产品。  
7. 单击“添加到行”。
8. 在列表中，找到并选择所需记录。
9. 单击“添加到行”。
10. 单击“确定”。

