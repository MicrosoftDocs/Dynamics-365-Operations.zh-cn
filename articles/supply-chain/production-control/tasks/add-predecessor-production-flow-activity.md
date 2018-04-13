--- 
title: "将前导活动添加到生产流活动"
description: "在生产流版本中，必须为所有活动排序。"
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>将前导活动添加到生产流活动

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

在生产流版本中，必须为所有活动排序。 一个活动可以有一个或多个前导活动或后续活动。 

此过程显示如何将前导活动关联到活动。 

若要执行此任务，需要草稿版本至少有两个可连接的活动的生产流。 

若要了解详细信息，请阅读白皮书“lean manufacturing 中的生产流和活动”。


## <a name="find-the-production-flow-and-version"></a>找到生产流和版本
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 在列表中，找到并选择所需记录。
5. 单击“活动”。

## <a name="select-an-activity-and-add-a-predecessor"></a>选择活动和添加前导活动
1. 在列表中，找到并选择所需记录。
2. 单击“添加前导活动”。
3. 在“活动”字段中，输入或选择一个值。
4. 在“周期时间比率”字段中，输入一个数字。
    * 活动关系的默认周期时间比率为 1。 这假设两个活动按照相同的速度或单位产品生产时间运行。 如果前导活动按照较高的速度（较低的单位产品生产时间）运行，则比率应低于 1，如果前导活动以较慢的速度（较高的单位产品生产时间）运行，则周期时间比率大于 1。  
5. 单击“确定”。


