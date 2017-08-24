--- 
title: "对货运进行手动对帐"
description: "此过程显示如何手动对帐货运。"
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 28de4c720cd771f476f379d925e9500e41482aa6
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="reconcile-freight-manually"></a>对货运进行手动对帐

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何手动对帐货运。 这通常由运输协调员完成。 您可以在 USMF 演示数据公司中使用此过程。


## <a name="select-a-load-to-reconcile"></a>选择要对帐的负荷
1. 转到“运输管理”>“计划”>“装载计划工作台”。
2. 清除“隐藏已装运和已接收”复选框。 
3. 在列表中，选择负荷 ID 为 00006 的负荷。

## <a name="create-a-carrier-invoice"></a>创建承运人发票
    * 如果手动对帐货运，并且不自动接收承运人发票，可以基于货运帐单创建发票。  
1. 单击“相关信息”。
2. 单击“货运帐单明细”。
3. 单击“生成货运帐单发票”。
4. 在“发票”字段中，输入一个值。
5. 单击“确定”。

## <a name="reconcile-the-invoice"></a>对发票进行对帐
    * 对帐承运人发票和货运帐单时，逐行执行。  
1. 单击“匹配货运帐单和发票”。
2. 展开“发票详细信息”部分。
3. 展开“已取消匹配的货运帐单明细”部分。
4. 在列表中，标记所选的行。
5. 单击“匹配”。
6. 展开“匹配的货运帐单明细”部分。

## <a name="submit-the-invoice-for-approval"></a>提交发票以供审核
1. 单击“提交以供审核”。
2. 关闭该页面。
3. 清除“隐藏已审核项”复选框。 
4. 单击“供应商发票日记帐”。
5. 单击以访问“参考日记帐号”字段中的链接。
6. 单击“行”。


