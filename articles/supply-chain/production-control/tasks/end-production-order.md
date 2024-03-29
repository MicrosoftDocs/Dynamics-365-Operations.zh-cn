---
title: 结束生产订单
description: 该过程显示如何结束生产订单。
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb87a8df77ecced213b4bd61c40fa372b092ab765528e1cd96274cf79537d521
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765946"
---
# <a name="end-a-production-order"></a>结束生产订单

[!include [banner](../../includes/banner.md)]

该过程显示如何结束生产订单。 创建此程序的演示数据公司是 USMF。 这是解释生产订单周期的七个步骤中的最后一步。


## <a name="end-a-production-order"></a>结束生产订单
1. 转到“生产控制”>“生产订单”>“全部生产订单”。
    * 选择状态“报告”为完工的生产订单。  
2. 在操作窗格上单击“生产订单”。
3. 单击“结束”。
    * 在此页，您可以确认您是否想结束生产订单。  
4. 单击“常规”选项卡。
5. 在“日期”字段中，输入一个日期。
6. 在“报废方法”字段中，选择“分配”。
    * 当您选择“分配方法”时，报废物料的成本将添加到成品中。  
7. 单击“确定”。

## <a name="validate-calculation-results"></a>验证计算结果
1. 在“操作窗格”中，单击“管理成本”。
2. 单击“查看成本比较”。
    * 在结束生产订单后，可以将已实现的成本价与估计成本对比获得生产差异概览。  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]