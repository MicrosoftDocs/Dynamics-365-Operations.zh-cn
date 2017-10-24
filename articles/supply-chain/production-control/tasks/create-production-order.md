--- 
title: "创建生产订单"
description: "此程序说明如何创建一个生产订单。"
author: johanhoffmann
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
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 730adcea0ac59f683ecae8cbb62025bd7db75c55
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-order"></a>创建生产订单

[!include[task guide banner](../../includes/task-guide-banner.md)]

此程序说明如何创建一个生产订单。 创建此程序的演示数据公司是 USMF。 这七个程序中的第一个诠释了生产订单的生命周期。


## <a name="create-a-production-order"></a>创建生产订单
1. 转到“生产控制”>“生产订单”>“全部生产订单”。
2. 单击“新建生产订单”。
3. 在“物料编号”字段中，键入“D0001”。
4. 在“交货”字段中，输入一个日期。
    * 交货日期说明生产订单应已完成以便按时交货。 此日期可以在计划流程中使用。 例如，您可以根据交货日期制定之后的订单。  
5. 将“数量”设置为“20”。
    * 注意：物料清单编号字段自动显示当前物料的所有有效物料清单的编号，但是，您可以通过从审核的物料清单版本列表中选择有效物料清单来更改生产订单的物料清单。    工艺路线编号字段自动显示当前物料的所有有效工艺路线的编号，但是，您可以通过从审核的工艺路线版本列表中选择有效工艺路线来更改生产订单的工艺路线。  
6. 单击“创建”。

## <a name="validate-the-production-order"></a>确认生产订单
1. 在列表中，单击所选行中的链接。
    * 单击您所创建的生产订单编号的链接。 可以打开订单的详细信息页面。  
2. 单击“编辑”。
3. 在“交货”字段中，输入一个日期。
    * 例如，可以更改生产订单的交货日期。  
4. 单击“保存”。
5. 关闭该页面。

## <a name="update-the-bom"></a>更新物料清单
1. 在操作窗格上单击“生产订单”。
2. 单击“物料清单”。
    * 打开“物料清单”页面并确认物料清单数据是订单创建时所复制的默认数据。 在此程序中，需要更新物料清单的数量。  
3. 单击“编辑”。
4. 在“数量”字段中，输入一个数字。
    * 更改该物料清单行的数量将会影响生产订单物料消耗的成本预估。  
5. 单击“保存”。
6. 关闭该页面。

## <a name="update-the-production-route"></a>更新生产路径
1. 在操作窗格上单击“生产订单”。
2. 单击“路径”。
    * 打开“路径”页面并确认生产流程的数据是创建订单之时所复制的默认数据。 在此程序中，需要更新生产流程中的操作步骤数量。  
3. 在列表中，找到并选择所需记录。
4. 单击“编辑”。
5. 在“进程数量“ 字段中，输入一个数字。
    * 更改生产时间将会影响生产订单的路线消耗预估和成本预估。  
6. 单击“保存”。
7. 关闭该页面。


