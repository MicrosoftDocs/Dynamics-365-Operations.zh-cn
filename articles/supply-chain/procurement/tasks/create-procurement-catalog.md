---
title: 创建采购目录
description: 本文介绍如何创建采购目录。
author: GalynaFedorova
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e35e8c5b5c93fa9aac914f04e7ea658748cb052
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869537"
---
# <a name="create-a-procurement-catalog"></a>创建采购目录

[!include [banner](../../includes/banner.md)]

本文介绍如何创建采购目录。 此任务通常由采购专业人员完成。 您还将了解员工在创建申请时如何使用目录。 系统中必须已有采购类别层次结构，才能创建目录。 新目录继承层次结构，以及其中的所有产品。 可在采购类别层次结构可用的演示数据公司 USMF 中使用此指南，以及使用前面的步骤中使用的示例。


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>确保存在采购类别层次结构。
1. 转到 **导航窗格 > 模块 > 采购 > 采购目录**。 USMF 演示数据公司中可使用采购目录层次结构，并且产品已添加到 **办公设备/计算机** 类别。 如果您正在运行该过程以作为任务指南，并且要浏览类别，您需要解锁该指南。 如果层次结构不可用，可通过单击 **新建** 创建。 此操作只能执行一次。  
2. 关闭该页面。

## <a name="create-a-catalog"></a>创建目录
1. 转到 **导航窗格 > 模块 > 采购 > 目录 > 采购目录**。
2. 选择 **新采购目录** 以打开下拉对话框。
3. 在 **名称** 字段中，键入一个值。
4. 选择 **确定**。
5. 在树中，展开 **企业采购类别**。
6. 在树中，展开 **办公设备**。
7. 在树中，选择 **计算机**。

  - 列表中将显示采购类别中的产品。 如果要向类别添加产品，需要在 **采购列表层次结构** 页或 **物料详细信息** 页中执行此操作。  
  - **默认** 更新类型确定已添加到采购类别层次结构的新产品是否在目录中立即显示。 如果更新类型设置为 **动态**，将立即显示更改。 如果更新类型为 **静态**，则新产品仅在已重新发布目录后对使用该目录的人员显示。 页面顶部的操作窗格中支持 **发布** 操作。 如果从采购类别层次结构删除产品，无论 **默认** 更新类型字段中是哪个值，都将立即显示更改。  

8. 在操作窗格上，选择 **类别导航** 并确保选择 **启用**。
9. 选择 **启用目录**。
10. 关闭该页面。

## <a name="make-the-catalog-visible"></a>显示目录
1. 转到 **导航窗格 > 模块 > 采购 > 设置 > 策略 > 采购策略**。
2. 选择 **采购政策 USMF**。 您需要连接到您的用户配置文件的工作人员获准订购其产品的法人选择采购政策。 在 USMF 演示数据中，Admin 用户连接到工人 **Julia Funderburk**，而默认情况下该工人可订购 USMF 中的产品。  
3. 选择您刚创建的目录。
4. 选择 **确定**。

## <a name="use-the-catalog"></a>使用目录
1. 转到 **导航窗格 > 模块 > 采购 > 采购申请 > 所有采购申请**。
2. 选择 **新建**。
3. 在 **名称** 字段中，键入一个值。
4. 选择 **确定**。
5. 选择 **添加产品**。
6. 在列表中，找到并选择所需记录。 您可以使用左侧的类别层次结构或列表顶部的筛选器筛选产品。  
7. 选择 **添加到行**。
8. 选择 **确定**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]