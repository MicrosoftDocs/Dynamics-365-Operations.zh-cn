---
title: 结算会计科目之间的交易记录
description: 该过程显示如何结算会计科目间的交易和取消分类帐结算。
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440776"
---
# <a name="settle-transactions-between-ledger-accounts"></a>结算会计科目之间的交易记录

[!include [banner](../../includes/banner.md)]

该过程显示如何结算会计科目间的交易和取消分类帐结算。 此过程使用演示数据公司 USMF。


## <a name="settle-transaction-between-ledger-accounts"></a>结算会计科目之间的交易记录
1. 转到“总帐”>“定期任务”>“分类帐结算”。
2. 在列表中，找到您要结算的交易记录。
   > [!NOTE]
   > 余额必须为零。  
3. 单击“包括”。
4. 单击“接受”。

## <a name="cancel-a-ledger-settlement"></a>取消分类帐结算

1. 转到“总帐”>“查询和报表”>“试算平衡表”。
2. 单击“参数”以打开下拉对话框。
3. 单击“更新”。
4. 在列表中，找到您已结算交易记录的科目。
5. 单击“所有交易记录”。
6. 使用筛选器轻松查找列表中的交易记录。
7. 单击“分类帐结算”。
8. 在列表中，标记所选的行。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]