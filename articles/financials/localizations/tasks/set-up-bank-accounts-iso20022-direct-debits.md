---
title: 设置 ISO20022 直接借记的客户及客户银行帐户
description: 此任务通过设置所需的客户银行帐户和客户直接借记授权以生成客户付款文件（如 ISO20022 直接借记）。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82a8a3eff1f882d0d9b3d4943e352a8f3d1a6ae4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852590"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>设置 ISO20022 直接借记的客户及客户银行帐户

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务通过设置所需的客户银行帐户和客户直接借记授权以生成客户付款文件（如 ISO20022 直接借记）。 客户或客户银行帐户可能需要此过程中未介绍的更多信息，具体取决于设置的客户付款格式。 

本任务所用的演示数据公司为“DEMF“， 其法定注册国家主地址为”德国“。



这是五个用于演示使用电子申报配置的客户付款流程的过程中的第四个。


## <a name="set-up-a-customer-bank-account"></a>设置客户银行帐户
1. 转到“应付账款”>“客户”>“所有客户”。
2. 使用“快速筛选器”以查找记录。 例如，在含有“DE-010”值的“帐户”字段中筛选。
3. 在列表中，单击所选行中的链接。
4. 在“操作窗格”上，单击“客户”。
5. 单击“银行帐户”。
6. 单击“新建”。
7. 在“银行帐户”字段中，键入一个值。
8. 在“名称”字段中，键入一个值。
    * 例如，输入“EUR 银行”。  
9. 在“银行组”字段中，输入或选择一个值。
10. 在“IBAN”字段，键入一个值。
    * 例如，输入“DE36200400000628808808”。  
11. 在“SWIFT 代码”字段中，键入一个值。
    * 例如，输入 'COBADEFFXXX'。  请注意，许多付款格式不需要 SWIFT\BIC，但是建议还是为银行帐户登记。  
12. 单击“保存”。
13. 关闭该页面。
14. 单击“编辑”。
15. 展开“默认付款”部分。
16. 在“银行帐户”字段中，输入或选择一个值。

## <a name="add-a-direct-debit-mandate"></a>添加直接借记授权单
1. 展开“直接借记授权”部分。
2. 单击“添加”。
3. 在“贷方银行帐户”字段中，输入或选择一个值。
    * 例如，选择“DEMF OPER”。  
4. 在“签署日期”字段中，输入一个日期。
5. 单击“是”以确认日期的更新。
6. 在“输入位置”字段中，输入或选择一个值。
7. 在“付款期望值”字段中，输入一个数字。
8. 单击“确定”。
9. 单击“保存”。

