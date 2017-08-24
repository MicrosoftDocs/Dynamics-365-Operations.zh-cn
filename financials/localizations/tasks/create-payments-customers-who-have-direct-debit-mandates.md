--- 
title: "为有直接借记授权单的客户创建付款"
description: "此过程显示如何为有直接借记配置和有要付款发票的客户生成 ISO20022 直接借记付款文件。"
author: mrolecki
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8a0e48d4681014899a4cc1a31ba902f244c6644b
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>为有直接借记授权单的客户创建付款

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何为有直接借记配置和有要付款发票的客户生成 ISO20022 直接借记付款文件。 创建和过帐发票是可选操作。 可以在生成付款文件之前在日记帐中选择授权单，而不是创建要付款的发票，为客户预付款方案提供支持。



用于创建此过程的演示数据公司是 DEMF。



这是五个用于演示使用电子申报配置的客户付款流程的过程中的第五个。 必须先完成前面的任务，才能完成此任务。 您首先必须导入客户付款电子申报配置，配置付款方式和设置您的公司和客户信息。 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>过帐具有直接借记信息的普通发票
1. 转到“应收帐款”>“发票”>“所有普通发票”。
2. 单击“新建”。
3. 在“客户帐户”字段中，输入或选择一个值。
    * 例如，选择“DE-010”。  
4. 在“付款方式”字段中，输入或选择一个值。
    * 例如， 选择“电子”。  
5. 在“直接借记授权 ID”字段中，输入或选择一个值。
6. 单击“添加行”。
7. 在“描述”字段中，键入一个值。
8. 在“主科目”字段中，指定所需值。
9. 在“单位价格”字段中，输入一个数字。
10. 单击“过帐”。
11. 单击“确定”。

## <a name="create-a-payment"></a>创建付款
1. 转到“应收帐款”>“付款”>“付款日记帐”。
2. 单击“新建”。
3. 在“名称”字段中，输入或选择一个值。
4. 单击“行”。
5. 单击“付款方案”。
6. 单击”创建付款方案“。
7. 扩展“要包括的记录”部分。
8. 单击“筛选器”。
9. 在列表中，选择“客户交易”表和“付款方式”字段的行。
    * 您可以为选择要支付的电子交易应用任何条件。 对于本示例，请使用“电子”充当支付方法筛选交易。  
10. 在“标准”字段中，输入或选择一个值。
11. 单击“确定”。
12. 单击“确定”。
13. 单击”创建付款“。

## <a name="generate-a-payment-file"></a>生成付款文件


