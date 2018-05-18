--- 
title: "针对电子申报 (ER) 使用格式配置生成付款的电子单据"
description: "以下步骤说明属于系统管理员或电子申报开发人员的用户如何使用新电子申报 (ER) 格式配置来生成用于处理付款的电子单据。"
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a>针对电子申报 (ER) 使用格式配置生成付款的电子单据

[!include [task guide banner](../../includes/task-guide-banner.md)]

以下步骤说明属于系统管理员或电子申报开发人员的用户如何使用新电子申报 (ER) 格式配置来生成用于处理付款的电子单据。 这些步骤可以在 GBSI 示例公司执行。

为了完成这些步骤，您必须首先完成“使用付款单据格式创建配置”这一过程中的步骤。


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>更改电子付款方式的配置
1. 转至“应付账款”>“付款设置”>“付款方式”。
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
1. 转至“应付账款”>“付款”>“付款日记帐”。
2. 单击“新建”。
3. 在列表中，标记所选的行。
4. 在“名称”字段中，单击下拉按钮以打开查找。
5. 在列表中，单击所选行中的链接。
    * 选择 VendPay。  
6. 单击“保存”。
7. 单击“行”。
8. 在“公司”字段中，键入 'DEMF'。
    * DEMF  
9. 在账号字段，设定值为“DE-01001"。
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


