--- 
title: "处理催款单"
description: "该过程说明如何创建、打印并过帐收款单。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>处理催款单

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程说明如何创建、打印并过帐收款单。 本任务使用 USMF 公司进行演示。


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>在该过帐上设置收款单的排序
1. 转到“信用征收”>“设置”>“客户过帐模板”。
2. 单击“编辑”。
    * 从下拉列表中选择收款单排序。 如果不使用该过帐模板生成交易收款单，则该字段保留空白。  
    * 通过该表格的限制选项卡，可以更改处理收款单的方式。 如果此字段设置为“是”，则将在此过帐模板创建收款单。  
3. 关闭该页面。

## <a name="create-collection-letters"></a>创建催款单
1. 转到“信用与收款”>“收款单”>“创建收款单”。
    * 必须选择收款单的交易类型。 此计算包含这些类型的所有开放交易。  
2. 在“催款单”字段中，选择一个选项。
3. 输入该收款单的日期。
    * 具有两个过帐模板选项：帐户 – 使用分配给客户帐户每张利息单的过帐模板。   选择 – 使用在“过帐模板”字段中选择的过帐模板。  
    * 如果将“使用过帐模板”更改为“选择”，则请选择一个过帐模板。  
4. 扩展“要包括的记录”部分。
5. 单击“筛选器”。
6. 在“条件”字段中，在“条件”字段中，输入一个客户 ID。 例如，输入 'US-001'。
7. 单击“确定”。
8. 单击“确定”。

## <a name="print-collection-letters"></a>打印收款单
1. 转到“信用和收款”>“收款单”>“查看并处理收款单”。
2. 在“状态”字段中，选择“创建”。
3. 在“打印”字段中，选择“不打印”。
4. 单击“打印”。
5. 单击“注解收款单”。
6. 扩展“要包括的记录”部分。
7. 输入过帐的截止日期
8. 单击“确认”以打印收款单。

## <a name="post-the-collection-letter"></a>过帐收款单
1. 单击“过帐”。
2. 输入该收款单的过帐日期
3. 扩展“要包括的记录”部分。
4. 单击“确定”。
5. 在“状态”字段中，选择“已过帐”。
6. 在“打印”字段中，选择一个选项。


