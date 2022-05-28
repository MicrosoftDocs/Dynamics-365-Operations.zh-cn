---
title: 处理分类帐分配日记帐
description: 此主题介绍如何在 Dynamics 365 Finance 中处理分配请求。
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ec3653085aed278eb5d13d47f345c713cd39f1f
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722130"
---
# <a name="process-ledger-allocation-journal"></a>处理分类帐分配日记帐

[!include [banner](../../includes/banner.md)]

此主题介绍如何处理分配请求。 使用“处理分配请求”页面以创建可在过帐至总帐前检查和审核，或直接过帐至总帐的分配日记帐。 必须至少有一个有效的分类帐分配规则才能创建分配日记帐。 此任务使用 USMF 公司演示。

1. 在导航窗格中，转到 **总帐 > 分配 > 处理分配请求**。
2. 在 **规则** 字段中，在下拉菜单中选择所需记录。
3. 在 **截止日期** 字段中，输入日期。

    - **截止日期** 非常重要，因为根据规则分类帐是数据源头。 这个日期决定分配被包括哪个分类帐平衡表。  
    - 在 **零资源** 字段中，选择 **停止**。 这将停止分配过程，然后显示一条信息说”选择了零资源数“。  

4. 在 **方案选项** 字段中，选择 **仅方案**。 选择 **仅方案** 会在将分配过帐至总帐前，检查并选择性审核“分配”日记帐中的结果。  
5. 在“GL 过帐日期”字段中，输入日期。
6. 选择 **确定**。
7. 在导航窗格中，转到 **模块 > 总帐 > 分配 > 分配日记帐**。
8. 选择 **行**。
9. 选择 **过帐**。
10. 选择 **过帐**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
