---
title: 设置 ISO20022 贷方转帐的付款方式
description: 此过程显示如何通过电子申报生成文件来为 ISO20022 贷方转帐或其他任何付款类型设置供应商付款方式。
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 643be31db625d0db12f1df18b9e797013da98ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832464"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>设置 ISO20022 贷方转帐的付款方式

[!include [banner](../../includes/banner.md)]

此过程显示如何通过电子申报生成文件来为 ISO20022 贷方转帐或其他任何付款类型设置供应商付款方式。 

必须先导出格式配置和设置付款帐户，才能完成此任务。

此任务使用 DEMF 演示数据公司是创建。

这是五个用于演示使用电子申报配置的供应商付款流程的流程中的第三个。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。

1. 转至“应付帐款”>“付款设置”>“付款方式”。
2. 使用“快速筛选器”以查找记录。 例如，含有“SEPA CT”值的“付款方式”字段。
3. 单击“编辑”。
4. 在“期间”字段中，选择“全部”。
5. 在“付款类型”字段中，选择“电子付款”。
6. 展开“文件格式”部分。
7. 在“普通电子申报”字段中，选择“是”。
8. 在“导出格式配置”字段中，输入或选择一个值。
    * 在列表中选择值 ISO20022 信用转帐 (DE)。 如果该列表为空，则供应商付款导出格式配置不导入，也不有效。  
9. 在“帐户类型”字段中，选择“银行”。
10. 在“付款帐户”字段中，指定“DEMF OPER”值。
11. 单击“保存”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]