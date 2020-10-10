---
title: 管理订单保留
description: 此过程演示如何将销售订单置于暂停状态、如何使用订单保留签出，以及如何删除订单保留。
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: edb3c6941af132f9ea1bf9f52f94cd6acc008d6c
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830026"
---
# <a name="manage-order-holds"></a>管理订单保留

[!include [banner](../../includes/banner.md)]

此过程演示如何将销售订单置于暂停状态、如何使用订单保留签出，以及如何删除订单保留。 订单可能出于多种原因被置于暂停状态。 例如，在验证客户地址或付款方式之前，或在经理可以查看客户的信用额度之前，您可以保留订单。 订单出于保留状态时，仓库不能为装运处理该订单。 

您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。


## <a name="set-up-order-holds"></a>设置订单暂停
1. 转到**导航窗格 > 模块 > 销售和营销 > 设置 > 销售订单 > 订单保留代码**。
2. 单击**新建**。
3. 在**保留代码**字段中，键入一个值。 例如，输入“回电”。  
4. 在**描述**字段中，键入一个值。
    - 例如，已保留并在等待客户回电的订单。  
    - 或者，也可以选中**删除预留**复选框，以便在添加此保留代码时从订单中删除所有实际预留。  
5. 单击**保存**。

## <a name="place-order-on-hold"></a>将订单设置为保留状态
1. 转到**导航窗格 > 模块 > 销售和营销 > 销售订单 > 所有销售订单**。
2. 单击**新建**。
3. 在**客户帐户**字段中，输入或选择一个值。
4. 单击 **确定**。
5. 在**物料编号**字段中，输入或选择一个值。
6. 在**数量**字段中，输入一个数字。
7. 在**操作窗格**上，单击**销售订单**。
8. 单击**订单保留**。
9. 单击**新建**。
10. 在**保留代码**字段中，选择在上一个子任务中已创建的代码。
11. 单击**保存**。
12. 关闭该页面。
13. 转到**销售和营销 > 销售订单 > 所有销售订单**。
14. 在列表中，标记所选的行。 当前处于保留状态的订单的“请勿处理”和“保留”字段带有标记。
15. 在“操作窗格”中，单击**领料和装箱**。

## <a name="manage-order-holds"></a>管理订单保留
1. 转到**销售和市场营销 > 销售订单 > 未结订单 > 订单保留**。 工作台形式的**订单保留**页面功能，可在其中获取所有当前保留和已处理保留的概述，以及处理这些保留和关联的销售订单。     
2. 在列表中，标记所选的行。
3. 在**操作窗格**上，单击**保留签出**。
4. 单击**签出**。
5. 在列表中，取消标记所选的行。 **签出目标**字段现在显示您的用户 ID。   
6. 单击**清除签出**。
7. 在**操作窗格**上，单击**清除保留**。
    - 准备好删除保留并允许订单继续到下一个履行步骤时，必须清除保留。 如果不需要更改订单，可以运行“清除保留”操作。 但是，如果在清除保留时必须更新订单，可以使用“清除并修改”操作。      
    - 仅当您使用呼叫中心功能时，**清除并提交**操作才适用。  
8. 单击**清除保留**。 保留现在已从订单中清除，并且已从“活动保留”列表中删除。 若要根据特定状态查看所有保留及其子集，请更改“显示”字段中的值。     

