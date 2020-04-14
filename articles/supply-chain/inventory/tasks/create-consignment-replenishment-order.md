---
title: 创建托运补货订单
description: 此主题介绍如何创建托运补货订单，可将其用于跟踪供应商预期交货到您的托运库存。
author: mkirknel
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 766f29f7511c16eccd37e93f2de366ac23c35545
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145793"
---
# <a name="create-a-consignment-replenishment-order"></a>创建托运补货订单

[!include [banner](../../includes/banner.md)]

此主题介绍如何创建托运补货订单，可将其用于跟踪供应商预期交货到您的托运库存。 还显示如何记录物料收据，以便将托运库存登记为供应商拥有的现有库存。 此过程通常由采购专员完成。 您可以使用演示数据公司 USMF 运行此指南。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。

## <a name="create-a-consignment-replenishment-order"></a>创建托运补货订单
1. 在导航窗格中，转到**模块 > 采购 > 托运 > 托运补货订单**。
2. 选择**新建**。
3. 在**供应商帐户**字段中，选择供应商 **US-104**（必须选择在**库存所有者**页中注册为所有者的供应商）。 
4. 选择**确定**。
5. 选择**添加行**。
6. 在**物料编号**字段中，键入 `M9211CI`（必须选择为托运库存设置的物料）。
7. 在**数量**字段中，输入一个数字。
8. 在**请求交付日期**字段中，输入一个日期。 请求日期和确认日期由 MRP 引擎用于货物的预期到达。  
9. 在**确认交货日期**字段中，输入一个日期。
10. 展开**行详细信息**部分。
11. 选择**库存维度**选项卡。
12. 若要在**库存维度负责人**字段中显示负责人，请刷新页面。 供应商 US-104 现在作为所有者列出。  

## <a name="check-the-inventory-transaction-status"></a>检查库存交易记录状态。
1. 选择**库存**。
2. 选择**交易记录**。
3. 请注意，**收货**字段设置为**已订购**。  
4. 关闭该页面。

## <a name="receive-items"></a>接收多个物料
1. 选择**物料收货**。
2. 在**外部物料收据**字段中，输入一个值。
3. 在**数量**字段中，输入一个比此处显示的数字更小的数字。 
4. 选择**确定**。

## <a name="check-the-on-hand-inventory"></a>检查现有库存量
1. 选择**库存**。
2. 选择**现有**。
3. 选择**概览**。 已作为供应商拥有的托运库存接收的物料现有可用。 托运补货订单的剩余数量在**订购总数**字段中显示。  
4. 关闭该页面。

