---
title: 使用装载计划工作台计划负荷和装运
description: 本主题显示如何使用装载计划工作台创建销售订单的装载量。
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4fdff8bdc383a85d604fa6e545c625d5782241f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976805"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>使用装载计划工作台计划负荷和装运

[!include [banner](../../includes/banner.md)]

本主题显示如何使用装载计划工作台创建销售订单的装载量。 作为先决条件，我们将首先创建销售订单。 此过程为运输协调员日常工作的一部分。 创建此程序的演示数据公司是 USMF。


## <a name="create-a-sales-order"></a>创建销售订单
1. 转到 **导航窗格 > 模块 > 应收帐款 > 订单 > 所有销售订单**。
2. 选择 **新建**。
3. 在 **客户帐户** 字段中，选择下拉按钮以打开查找。
4. 选择帐户 **US-004**。
5. 选择 **确定**。
6. 在 **物料编号** 字段中，选择下拉按钮以打开查找。
7. 选择物料 **A0001**。 **A0001** 可供运输管理流程使用。  
8. 在 **站点** 字段中，选择下拉按钮以打开查找，然后选择物料。
9. 在 **数量** 字段中，输入一个数字。
10. 在 **仓库** 字段中，为此示例键入“24”。 此仓库可供运输管理和高级仓库管理使用。  
11. 选择 **保存**。
12. 关闭该页面。

## <a name="create-a-new-load"></a>创建“新装载”。
1. 找到 **导航窗格 > 模块 > 运输管理 > 计划 > 装载计划工作台**。
2. 选择 **销售行** 选项卡。现在将构建您刚创建的销售订单的装载量。 装载量的构建基于采购订单、转移订单和销售订单的供应和需求。  
3. 在操作窗格上，选择 **供应与需求**。
4. 选择 **至新负荷**。
5. 在 **装载模板 ID** 字段中，选择下拉按钮以打开查找。 装载量模板定义整个装载量的重量和体积的最大度量值。 例如，装载量模板可能表示卡车或集装箱的大小。 选择某一物料。
6. 选择 **确定**。

## <a name="rate-and-route-the-load"></a>为装载量评级和路线选择
1. 选择 **评级和路线选择**。
2. 选择 **费率路线工作台**。
3. 选择 **费率工场**。
4. 在列表中，找到并选择所需记录。
5. 选择 **分配**。
6. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]