---
title: 完成已发布基础产品的基本设置
description: 本主题显示在基础产品可用于物料清单版本之前，如何完成所需的最低设置。
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ac4ceeb3e21ab089eb16565bb6e38c7eb44be80
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986399"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>完成已发布基础产品的基本设置

[!include [banner](../../includes/banner.md)]

本主题显示在基础产品可用于物料清单版本之前，如何完成所需的最低设置。

这是八个过程中第三个说明如何构建基于维度的配置组合的过程。 创建此程序的演示数据公司是 USMF。

1. 转到**导航窗格 > 模块 > 产品信息管理 > 产品 > 已发放产品**。
2. 在列表中，找到并选择所需记录。 选择您已在第二个过程中发布的基础产品。 此基础产品是使用基于维度的配置技术创建的。  
3. 在操作窗格上，选择**产品**。
4. 单击**维度组**以打开下拉对话框。
5. 在**存储维度组**字段中，选择下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。 存储维度组确定哪些存储维度用于产品交易记录。 选择该过程适用的**站点**。  
7. 在**跟踪维度组**字段中，选择下拉按钮以打开查找。
8. 在列表中，找到并选择所需记录。 跟踪维度组确定哪些跟踪维度用于产品交易记录。 针对该过程选择**无**。  
9. 单击 **确定**。
10. 单击**编辑**。
11. 在**物料模型组**字段中，选择下拉按钮以打开查找。
12. 在列表中，找到并选择所需记录。 物料模型组包含决定在进行物料收货和发货时如何控制和处理物料的设置。 它们还决定着如何计算物料消耗量。 选择该过程适用的 **FIFO**。  
13. 展开**管理成本**部分。
14. 在**物料组**字段中，选择下拉按钮以打开查找。
15. 在列表中，找到并选择所需记录。 物料组基于物料特征将库存物料分成不同的组，可用于管理库存。 选择该过程适用的 **CarAudio**。  
16. 在操作窗格上，选择**计划**。
17. 选择**默认订单设置**。
18. 在**默认订单类型**字段中，选择一个选项。 选择**生产**以指定此基础产品的默认值供应选项将会生产它。  
19. 选择**保存**。
20. 关闭该页面。
21. 关闭**已发布产品详情**窗体。

