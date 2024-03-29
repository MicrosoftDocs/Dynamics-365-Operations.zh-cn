---
title: ER 使用格式配置生成付款的电子单据
description: 本文介绍如何使用新的电子报告 (ER) 格式配置生成用于处理付款的电子文档。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
ms.openlocfilehash: b70b246e3618e8f083e5f6757ee8a97d8072a635
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290865"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>ER 使用格式配置生成付款的电子单据

[!include [banner](../../includes/banner.md)]

以下步骤说明属于系统管理员或电子申报开发人员的用户如何使用新电子申报 (ER) 格式配置来生成用于处理付款的电子单据。 这些步骤可以在 GBSI 示例公司执行。

为了完成这些步骤，您必须首先完成“使用付款单据格式创建配置”这一过程中的步骤。


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>更改电子付款方式的配置
1. 转至“应付帐款”>“付款设置”>“付款方式”。
2. 如果需要，切换“文件格式”部分以展开它。
3. 使用“快速筛选器”以查找记录。 例如，在含有“电子”值的“付款方式”字段中筛选。
4. 单击“编辑”。
5. 将“一般电子申报”字段设置为“是”。
    * 选择是为付款文件生成使用常规电子申报模式。  
6. 在“名称”字段中，单击下拉按钮以打开查找。
7. 选择 BACS（英国虚构）格式配置。
8. 单击“保存”。
9. 关闭该页面。

## <a name="test-the-format-of-generated-payment-files"></a>测试生成的付款文件的格式
1. 转至“应付帐款”>“付款”>“付款日记帐”。
2. 单击“新建”。
3. 在列表中，标记所选的行。
4. 在“名称”字段中，单击下拉按钮以打开查找。
5. 在列表中，单击所选行中的链接。
    * 选择 VendPay。  
6. 单击“保存”。
7. 单击“行”。
8. 在“公司”字段中，键入 'DEMF'。
    * DEMF  
9. 在帐号字段，设定值为“DE-01001"。
    * DE-01001  
10. 在“描述”字段中，键入“付款”。
    * 付款  
11. 在“借方”字段中，输入一个数值。
    * 1000  
12. 单击“付款”选项卡。
13. 在“付款方式”字段中，单击下拉按钮以打开查找。
14. 在列表中，找到并选择所需记录。
    * 选择“电子值”。  
15. 在列表中，单击所选行中的链接。
16. 单击“保存”。
17. 点击”生成付款“。
18. 在“付款方式”字段中，单击下拉按钮以打开查找。
19. 在列表中，找到并选择所需记录。
    * 选择“电子值”。  
20. 在列表中，单击所选行中的链接。
    * 选择“电子值”。  
21. 在文件名字段，输入一个值。
    * 例如，键入“付款”。  
22. 在“银行帐户”字段中，单击下拉按钮以打开查找。
23. 在列表中，单击所选行中的链接。
    * 选择值 GBSI OPER。  
24. 单击“确定”。
25. 单击“确定”。
    * 分析以 XML 格式创建的付款文件。 将其与设计的文档格式和定义的付款交易记录属性比较。  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
