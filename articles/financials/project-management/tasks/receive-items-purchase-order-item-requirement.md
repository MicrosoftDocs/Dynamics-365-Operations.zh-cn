---
title: 根据物料需求接收采购订单上的物料
description: 本主题介绍如何根据物料需求接收某一采购订单的物料。
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867287"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>根据物料需求接收采购订单上的物料

[!include [task guide banner](../../includes/task-guide-banner.md)]

本主题介绍如何根据物料需求接收某一采购订单的物料。

通过使用物料需求来代替物料交易记录，您可以计划刚好在实际使用物料之前交货，创建采购订单，在贸易协议框架中包括物料，以及在生产计划中包括物料需求。 

此任务使用 USSI 数据集。

1. 在导航窗格中，转到**模块 > 项目管理与核算 > 项目 > 所有项目**。
2. 在列表中，选择所需行中的链接。
3. 在操作窗格上，选择**计划**。
4. 选择**物料需求**。
5. 选择**新建**。
6. 在新行的**物料编号**字段中，输入或选择一个值。
7. 在**数量**字段中，输入一个数字。
8. 选择**保存**。
9. 在操作窗格上，选择**管理**。
10. 选择**功能**。
11. 选择**创建采购订单**。
12. 选中**全部包括**复选框。
13. 在**供应商帐户**字段中，输入或选择一个值。
14. 选择**确定**。
15. 在导航窗格中，转到**模块 > 应付帐款 > 采购订单 > 所有采购订单**。
16. 在列表中，选择所需行中的链接。
17. 在操作窗格上，选择**采购**。
18. 选择**确认**。
19. 在操作窗格上，选择**接收**。
20. 选择**物料收货**。
21. 在**产品收据**字段中，键入一个值。
22. 选择**确定**。

