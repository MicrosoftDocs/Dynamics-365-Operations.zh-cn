--- 
title: "处理分类帐分配日记帐"
description: "使用“处理分配请求”页面以创建可在过帐至总帐前检查和审核，或直接过帐至总帐的分配日记帐。"
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1189ffeae052c72542b3b403a6b7a6e415b005c4
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="process-ledger-allocation-journal"></a>处理分类帐分配日记帐

[!include[task guide banner](../../includes/task-guide-banner.md)]

使用“处理分配请求”页面以创建可在过帐至总帐前检查和审核，或直接过帐至总帐的分配日记帐。 必须至少有一个有效的分类帐分配规则才能创建分配日记帐。 此任务使用 USMF 公司演示。

1. 转到总分类记账>分配>处理分配请求。
2. 在“规则”字段中，单击下拉按钮以打开查找。
3. 在列表中，找到并选择所需记录。
4. 在列表中，单击所选行中的链接。
5. 在“截止日期”字段中，输入日期。
    * “截止日期”非常重要，因为根据规则分类账是数据源头。 这个日期决定分配被包括哪个分类账平衡表。     在“零资源“字段， 选“停止”。 这将停止分配过程，然后显示一条信息说”选择了零资源数“。  
6. 在“方案选项”字段中，选择“仅方案”。
    * 选择“仅方案”会在将分配过帐至总帐前，检查并选择性审核“分配”日记帐中的结果。  
7. 在“GL 过帐日期”字段中，输入日期。
8. 单击“确定”。
9. 转到总分类记账>分配>分配日记账。
10. 单击“行”。
11. 单击“过帐”。
12. 单击“过帐”。


