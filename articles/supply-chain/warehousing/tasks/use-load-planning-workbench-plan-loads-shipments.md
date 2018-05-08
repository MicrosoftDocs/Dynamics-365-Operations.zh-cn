--- 
title: "使用装载计划工作台计划负荷和装运"
description: "此过程显示如何使用装载计划工作台创建销售订单的装载量。"
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>使用装载计划工作台计划负荷和装运

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何使用装载计划工作台创建销售订单的装载量。 作为先决条件，我们将首先创建销售订单。 此过程为运输协调员日常工作的一部分。 创建此程序的演示数据公司是 USMF。


## <a name="create-a-sales-order"></a>创建销售订单
1. 转到应收帐项目>订单>所有销售订单。
2. 单击“新建”。
3. 在“客户帐户”字段中，单击下拉按钮以打开查找。
4. 选择帐户 US-004。
5. 单击“确定”。
6. 在“物料编号”字段中，单击下拉按钮以打开查找。
7. 选择物料 A0001。
    * A0001 可供运输管理流程使用。  
8. 在列表中，单击所选行中的链接。
9. 在“数量”字段中，输入一个数字。
10. 在“仓库”字段中，键入“24”。
    * 在此示例中，选择仓库 24。 此仓库可供运输管理和高级仓库管理使用。  
11. 单击“保存”。
12. 关闭该页面。

## <a name="create-a-new-load"></a>创建“新装载”。
1. 转到“运输管理”>“计划”>“装载计划工作台”。
2. 单击“销售行”选项卡。
    * 现在将构建您刚创建的销售订单的装载量。 装载量的构建基于采购订单、转移订单和销售订单的供应和需求。  
3. 在操作窗格上，单击“供应与需求”。
4. 单击“至新装载量”。
5. 在“装载模板 ID”字段中，单击下拉按钮以打开查找。
    * 装载量模板定义整个装载量的重量和体积的最大度量值。 例如，装载量模板可能表示卡车或集装箱的大小。  
6. 在列表中，单击所选行中的链接。
7. 单击“确定”。

## <a name="rate-and-route-the-load"></a>为装载量评级和路线选择
1. 单击“评级和路线选择”。
2. 单击“费率路线工作台”。
3. 单击“费率工场”。
4. 在列表中，找到并选择所需记录。
5. 单击“分配”。
6. 关闭该页面。
7. 关闭该页面。


