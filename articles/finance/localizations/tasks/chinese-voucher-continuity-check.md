---
title: 中国式凭证连续性检查
description: 每个凭证类型的中国式凭证号必须从 1 开始并且具有连续性，才能结转会计期间。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerCheckList_CN,  SysQueryForm, SysDateLookUp, LedgerTransVoucher, SrsReportViewerForm, LedgerVoucherRenumberLog_CN
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 254fbbe9b13d913870032dbe6a3b883a7a54d88d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183963"
---
# <a name="chinese-voucher-continuity-check"></a>中国式凭证连续性检查

[!include [task guide banner](../../includes/task-guide-banner.md)]

每个凭证类型的中国式凭证号必须从 1 开始并且具有连续性，才能结转会计期间。
此过程显示如何检查会计期间中的所有已过帐凭证，以及如何将中国式凭证号连续编号。 此过程是会计期间结转流程的一部分，因此只能为“暂停”会计期间运行。 第一个子任务逐步演示如何停止会计期间。 

本流程是用演示公司 CNMF 数据生成的。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="stop-a-fiscal-period"></a>停止某一会计期间
1. 转到“总帐”>“日历”>“分类帐日历”。
2. 在“会计年度”字段中，输入或选择一个值。
3. 在列表中，找到并选择所需记录。
4. 在列表中，标记所选的行。
5. 单击“编辑”。
6. 单击“停止期间”。
7. 单击“验证”。
8. 单击“确定”。
9. 单击“确定”。

## <a name="check-whether-posted-vouchers-have-continuity-voucher-numbers"></a>检查已过帐凭证是否有连续性凭证号
1. 转到“总帐”>“查询和报表”>“凭证事务”。
2. 在“标准”字段中，输入或选择一个值。
3. 在“标准”字段中，输入或选择一个值。
4. 单击“确定”。

## <a name="run-the-chinese-voucher-continuity-check-process"></a>运行中国式凭证连续性检查流程
1. 转到“总帐”>“定期任务”>“中国式凭证连续性检查”。
2. 在“打印重新编号结果”字段中选择“是”。
3. 在“期间开始”字段中，输入日期。
4. 单击“确定”。
5. 转到“总帐”>“查询和报表”>“凭证连续性检查日志”。

