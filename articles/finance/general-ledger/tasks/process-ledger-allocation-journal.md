---
title: 处理分类帐分配日记帐
description: 此主题介绍如何在 Dynamics 365 Finance 中处理分配请求。
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 882362a03e4fc4e249b092caea374640813eef88
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186064"
---
# <a name="process-ledger-allocation-journal"></a>处理分类帐分配日记帐

[!include [task guide banner](../../includes/task-guide-banner.md)]

此主题介绍如何处理分配请求。 使用“处理分配请求”页面以创建可在过帐至总帐前检查和审核，或直接过帐至总帐的分配日记帐。 必须至少有一个有效的分类帐分配规则才能创建分配日记帐。 此任务使用 USMF 公司演示。

1. 在导航窗格中，转到**模块 > 总帐 > 分配 > 处理分配请求**。
2. 在**规则**字段中，在下拉菜单中选择所需记录。
3. 在**截止日期**字段中，输入日期。

    - **截止日期**非常重要，因为根据规则分类账是数据源头。 这个日期决定分配被包括哪个分类账平衡表。  
    - 在**零资源**字段中，选择**停止**。 这将停止分配过程，然后显示一条信息说”选择了零资源数“。  

4. 在**方案选项**字段中，选择**仅方案**。 选择**仅方案**会在将分配过帐至总帐前，检查并选择性审核“分配”日记帐中的结果。  
5. 在“GL 过帐日期”字段中，输入日期。
6. 选择**确定**。
7. 在导航窗格中，转到**模块 > 总帐 > 分配 > 分配日记帐**。
8. 选择**行**。
9. 选择**过帐**。
10. 选择**过帐**。

