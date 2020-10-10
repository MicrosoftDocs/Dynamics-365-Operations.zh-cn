---
title: 对流程制造的生产作业排序
description: 此过程使用油漆产品作为示例显示如何根据颜色和包装大小的优先级排序计划订单。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db2c881f60b6e5251e2bcdf198da9e1c9f39a0e6
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886913"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>对流程制造的生产作业排序

[!include [banner](../../includes/banner.md)]

此过程使用油漆产品作为示例显示如何根据颜色和包装大小的优先级排序计划订单。 创建此程序的演示数据公司是 USPI。 此程序是专为生产规划员设计的。


## <a name="run-master-planning-for-uspi"></a>运行 USPI 的主计划
1. 转到“主计划”>“主计划”>“运行”>“主计划”。
2. 在“主计划”字段中，单击下拉按钮以打开查找。
3. 在列表中，单击所选行中的链接。
    * 选择主计划。  
4. 单击“确定”。
    * 这将开始主计划，包括顺序流程。 此流程可能需要几分钟的时间。  

## <a name="view-planned-orders-for-the-paint-products"></a>查看油漆产品的计划订单
1. 转到“主计划”>“主计划”>“计划订单”。
2. 展开“物料详细信息”速见表。
3. 展开“计划详细信息”速见表。
4. 在“计划”字段中，单击下拉按钮以打开查找。
5. 在列表中，找到并选择所需记录。
    * 选择主计划。  
6. 在列表中，单击所选行中的链接。
7. 使用“快速筛选”来筛选带有值“P300”的“物料编号”字段。
    * 解锁以滚动到右侧查看订单日期和交货日期。 请注意，这些物料具有“今天”订单日期，计划订单的交货日期没有在颜色和包装尺寸优先级后序列化，如产品名称中所示。 您可以悬停到物料编号上查看产品名称和优先级。  

## <a name="sequence-planned-orders-for-paint"></a>排序油漆产品的计划订单
1. 关闭该页面。
2. 转到“主计划”>“主计划”>“序列化计划订单”。
3. 展开“物料详细信息”速见表。
4. 展开“计划详细信息”速见表。
    * 注意：这里您看到计划订单的开始日期/时间根据 28 计算时段内的颜色和包装尺寸排序。 这些期间由字段“市场活动”中的数字定义。 “序列化计划订单”窗体类似于典型的计划订单窗体，生产规划员可以在此确定计划订单。  
5. 标记所有行。
6. 单击“接受”。
    * 这将使用所选的“延期”或“提前”顺序操作更新计划订单。  

## <a name="verify-the-sequence-of-the-planned-orders"></a>确认计划订单的顺序
1. 关闭该页面。
2. 转到“主计划”>“主计划”>“计划订单”。
3. 展开“物料详细信息”速见表。
4. 展开“计划详细信息”速见表。
5. 在“计划”字段中，单击下拉按钮以打开查找。
6. 在列表中，找到并选择所需记录。
    * 选择主计划。  
7. 在列表中，单击所选行中的链接。
8. 使用“快速筛选”来筛选带有值“P300”的“物料编号”字段。
    * 请注意，订单现在根据颜色和尺寸的优先级排序，计划订单从最早订单日期和交货日期开始。 验证“计划详细信息”速见表中的订单日期列或开始日期。  

