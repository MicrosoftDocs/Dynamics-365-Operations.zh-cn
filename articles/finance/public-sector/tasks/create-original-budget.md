---
title: 在公共部门创建原始预算，然后预留初步预算条目
description: 本主题提供有关如何使用具有初步预算金额的预算模型和维值来创建和冲销原始预算条目的信息。
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0120e4aa895d70da418c643a81bd0046a96c031de0ca660e31bb3e0d8f8c2df
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744242"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a>在公共部门创建原始预算，然后预留初步预算条目

[!include [banner](../../includes/banner.md)]

当您创建了原始预算条目并使用了包含初步预算金额的预算模型和维度值时，则可冲销初步预算金额。 通过使用 PSUS 演示公司数据的公共扇区分区创建该过程。

1. 转到“预算”>“预算登记条目”。
2. 单击“新建”。
3. 在“预算模型”字段中，单击下拉按钮以打开查找。
4. 在列表中，找到并选择所需记录。
5. 在“预算代码”字段中，单击下拉按钮以打开查找。
6. 在列表中，单击“原始预算”。
7. 单击“保存”。
8. 单击“添加行”。
9. 可选：如果您想更改标题中的日期，则请输入新日期。 该日期决定了记录预算的会计周期。
10. 在“科目结构”字段中，单击下拉按钮以打开查找。
11. 在列表中，找到并选择所需记录。
12. 在“维度值”字段中，指定所需值。
13. 在“金额”字段中，输入一个数字。
14. 在“货币”字段中，单击下拉按钮以打开查找。
15. 在列表中，单击所选行中的链接。
16. 单击“保存”。
17. 单击“更新预算余额”。
    * 可选：您可以选择“冲销初步预算”选择。 请注意，您可以冲销所有初步预算条目，或者仅冲销您所指定预算代码的初步预算条目。  
    * 要进行可选选择，请单击此页上方的“解锁”图标。  
18. 单击“更新”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]