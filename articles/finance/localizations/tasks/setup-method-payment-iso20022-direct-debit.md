---
title: 为 ISO20022 银行转帐设置付款方式
description: 此过程显示如何通过电子申报生成文件来为 ISO20022 直接借记或其他任何付款类型设置客户付款方式。
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c6a692553867d7e8679099210dc44b9d9e4d0f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838674"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>为 ISO20022 银行转帐设置付款方式

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]