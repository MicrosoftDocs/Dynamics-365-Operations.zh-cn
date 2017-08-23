--- 
title: "设置 ISO20022 直接借记的付款方式"
description: "此过程显示如何通过电子申报生成文件来为 ISO20022 直接借记或其他任何付款类型设置客户付款方式。"
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
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
ms.openlocfilehash: 16ff0cc28b272add80b08ae43b9fe5b8e7370b70
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a>设置 ISO20022 直接借记的付款方式

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何通过电子申报生成文件来为 ISO20022 直接借记或其他任何付款类型设置客户付款方式。 



必须先设置导出格式配置和付款帐户，才能完成此任务。



本流程用演示公司DEMF数据生成的。



这是五个用于演示使用电子申报配置的客户付款流程的过程中的第三个。

1. 转到“应收帐款”>“付款设置”>“付款方式”。
2. 使用“快速筛选器”以查找记录。 例如，在含有“ELECTRONIC”值的“付款方式”字段中筛选。
3. 单击“编辑”。
4. 在“付款帐户”字段中，指定“DEMF OPER”值。
5. 展开“文件格式”部分。
6. 在“普通电子申报”字段中，选择“是”。
7. 在“导出格式配置”字段中，输入或选择一个值。
    * 在列表中，选择“ISO20022 直接借记（德国）”。  如果该列表为空，则客户付款导出格式配置尚未导入，也不有效。  
8. 在“需要授权”字段选择“是”。
    * 为客户付款格式选择“需要授权单参数”，这些格式要求付款消息中包含授权单信息，如 SEPA 直接借记。  
9. 单击“保存”。


