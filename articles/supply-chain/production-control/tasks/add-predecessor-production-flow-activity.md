---
title: 将前导活动添加到生产流活动
description: 在生产流版本中，必须为所有活动排序。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9b761e61bf6a810da9258870e9a994da4ced125
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981423"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>将前导活动添加到生产流活动

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]