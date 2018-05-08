--- 
title: "基于采购协议创建采购下达订单"
description: "该过程会显示在创建采购订单时，如何使用采购协议。"
author: mkirknel
manager: AnnBe
ms.date: 12/04/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cecda03dd4d224d4319f2b0b196560389bb54195
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>基于采购协议创建采购下达订单

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程会显示在创建采购订单时，如何使用采购协议。 在创建采购订单时必须应用采购协议，因为存在应复制到采购订单标题的一般条件。 此任务通常由采购人员完成。 作为本指南的先决条件，您必须拥有某个供应商和物料的带产品数量承诺的有效采购协议。 如果您拥有带其他类型承诺的采购协议，则可以使用相同过程。 您可以使用 USMF 公司演示数据运行此指南。 如果您正在使用 USMF，您可以先运行“创建采购协议”，以设置本指南所需的前提条件。


## <a name="create-a-purchase-order"></a>创建采购订单
1. 打开采购订单准备工作区。
2. 单击“新采购订单”。
3. 在“供应商帐户”字段中，单击下拉按钮以打开查找。
4. 在列表中，找到并选择所需记录。
5. 在列表中，单击所选行中的链接。
6. 切换“概况”部分的扩展。
7. 在“采购协议”字段中，单击下拉按钮以打开查找。
    * 该供应商的所有可用协议皆列示于此。 查找您想要使用的有效协议。  
8. 在列表中，单击所选行中的链接。
9. 单击“是”。
10. 单击“确定”。

## <a name="add-a-line"></a>添加行
1. 在“项目编号”字段中，输入一个值。
    * 如果承诺的特定库存或位置维度存在，您必须在采购订单行上输入相同的值，以便利用协议。  
2. 在“位置”字段中，单击下拉按钮打开查询。
    * 站点可能已填充来自订单或供应商的默认值。 如果是这种情况，请跳过此步骤。  
3. 在列表中，找到并选择所需记录。
4. 在列表中，单击所选行中的链接。
5. 在“数量”字段中，输入一个数字。
    * 验证价格是从承诺复制而来的。  

## <a name="look-up-the-commitment"></a>查找承诺
1. 单击“更新行”。
2. 单击“已附加”。
    * 您可在此获得采购协议的详情。 例如，您可以查看价格以及价格和折扣是否被固定，这意味着，如果您将采购订单上的价格或折扣更改为不同于承诺载明的值，系统将会删除链接，以使采购订单行不履行承诺。 您还可以查看是否选择“最大值”是强制执行的选项，这意味着所有履行承诺的订单的数量综合不能超过承诺载明的数量。  
3. 关闭该页面。

## <a name="look-up-the-purchase-agreement"></a>查找采购协议
1. 在操作窗格上，单击“常规”。
2. 单击“采购协议”。
3. 关闭该页面。
4. 关闭该页面。


