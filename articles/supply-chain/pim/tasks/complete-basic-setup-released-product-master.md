--- 
title: "完成已发布基础产品的基本设置"
description: "该过程会显示在基础产品可用于物料清单版本之前，如何完成所需的最低设置。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 35617f5bec877fbe8a89d015eda16a66ee14d335
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="complete-basic-setup-of-a-released-product-master"></a>完成已发布基础产品的基本设置

[!include[task guide banner](../../includes/task-guide-banner.md)]

该过程会显示在基础产品可用于物料清单版本之前，如何完成所需的最低设置。

这是八个过程中第三个说明如何构建基于维度的配置组合的过程。 创建此程序的演示数据公司是 USMF。

1. 转到“产品信息管理”>“产品”>“已发布产品”。
2. 在列表中，找到并选择所需记录。
    * 选择您已在第二个过程中发布的基础产品。 此基础产品是使用基于维度的配置技术创建的。  
3. 在操作窗格上，单击“产品”。
4. 单击“维度组”以打开下拉对话框。
5. 在“存储维度组”字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
    * 存储维度组确定哪些存储维度用于产品交易记录。 选择该过程适用的站点。  
7. 在列表中，单击所选行中的链接。
8. 在“跟踪维度组”字段中，单击下拉按钮以打开查找。
9. 在列表中，找到并选择所需记录。
    * 跟踪维度组确定哪些跟踪维度用于产品交易记录。 针对该过程选择“无”。  
10. 在列表中，单击所选行中的链接。
11. 单击“确定”。
12. 在列表中，单击所选行中的链接。
13. 单击“编辑”。
    * 打开“已发布产品详情”窗体以继续执行设置任务。  
14. 在“物料模型组”字段中，单击下拉按钮以打开查找。
15. 在列表中，找到并选择所需记录。
    * 物料模型组包含决定在进行物料收货和发货时如何控制和处理物料的设置。 它们还决定着如何计算物料消耗量。 选择该过程适用的 FIFO。  
16. 在列表中，单击所选行中的链接。
17. 展开或折叠“管理成本”部分。
18. 在“物料组”字段中，单击下拉按钮以打开查找。
19. 在列表中，找到并选择所需记录。
    * 物料组基于物料特征将库存物料分成不同的组，可用于管理库存。 选择该过程适用的 CarAudio。  
20. 在列表中，单击所选行中的链接。
21. 在操作窗格上，单击“计划”。
22. 点击默认订单设置。
23. 在“默认订单类型”字段中，选择一个选项。
    * 选择“生产”以指定此基础产品的默认值供应选项将会生产它。  
24. 关闭该页面。
25. 关闭“已发布产品详情”窗体。


