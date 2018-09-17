--- 
title: "保函交易记录"
description: "该过程简单介绍了保函的处理流程。"
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c2e215f1ae16f907c8b64ea1f05cf67bfb0a04b6
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="letter-of-guarantee-transaction"></a>保函交易记录

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程简单介绍了保函的处理流程。



在完成该过程之前必须先完成以下任务：

- 设置银行设施和过帐保函模板。

- 创建保函的银行信贷协议。



该程序适用于 USMF 演示公司。


## <a name="create-sales-order-with-letter-of-guarantee"></a>创建“保函销售订单”
1. 转到应收帐项目>订单>所有销售订单。
2. 单击“新建”。
3. 在“客户帐户”字段中，输入或选择一个值。
4. 展开“常规”部分。
5. 在“站点”字段中，输入或选择一个值。
6. 在列表中，单击所选行中的链接。
7. 在“仓库”字段中，输入或选择一个值。
8. 在列表中，单击所选行中的链接。
9. 在“银行文档类型”字段中，选择“保函”。
10. 单击“确定”。
11. 在“物料编号”字段中，输入或选择一个值。
12. 在“单位价格”字段中，输入一个数字。
13. 展开“行明细”部分。
14. 单击“交货”选项卡。
    * 说明：选择“交货日期控制 = 无”  
15. 在“请求装运日期”字段中，输入一个日期。
16. 在“确认装运日期”字段中，输入一个日期。

## <a name="process-letter-of-guaranteerequest"></a>处理保函_请求
1. 在“操作窗格”上单击“管理”。
2. 单击“保函”。
3. 在“操作窗格”上单击“保函”。
4. 单击“请求”打开下拉对话框。
5. 在“类型”字段中，输入或选择一个值。
6. 在列表中，单击所选行中的链接。
7. 在“值”字段中，输入一个数字。
8. 在“到期日期”字段中，输入日期和时间。
9. 单击“确定”。
10. 关闭该页面。

## <a name="process-letter-of-guaranteesubmit-to-bank"></a>处理保函_提交至银行
1. 转到“现金和银行管理”>“保函”>“保函”。
2. 在列表中，找到并选择所需记录。
3. 单击“提交至银行”以打开下拉对话框。
4. 在“银行帐户”字段中，输入或选择一个值。
5. 在列表中，单击所选行中的链接。
6. 单击“确定”。

## <a name="process-letter-of-guaranteereceive-from-bank"></a>处理保函_从银行处收到
1. 单击“从银行处收到”以打开下拉对话框。
2. 在“银行号码”字段中，键入一个值。
    * 核实“毛利和费用”字段中所计算出的值。  
3. 单击“确定”。
4. 展开“行为”部分。
    * 核实“从银行处收到”记录。  
5. 单击以访问“日记帐批号”字段中的链接。
6. 单击“行”。
    * 核实日记帐条目的过帐信息。  
7. 关闭该页面。

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a>处理保函_给受益人
1. 转到应收帐项目>订单>所有销售订单。
2. 在列表中，单击所选行中的链接。
3. 在“操作窗格”上单击“管理”。
4. 单击“保函”。
5. 在“操作窗格”上单击“保函”。
6. 单击“给受益人”以打开下拉对话框。
7. 单击“确定”。
8. 转到“现金和银行管理”>“保函”>“保函”。
9. 在列表中，找到并选择所需记录。
10. 单击“给受益人”以打开下拉对话框。
11. 单击“确定”。
12. 展开“行为”部分。
    * 验证“给受益人”记录。  

## <a name="process-letter-of-guaranteeincrease-value"></a>处理保函_增加值
1. 转到应收帐项目>订单>所有销售订单。
2. 在列表中，单击所选行中的链接。
3. 在“操作窗格”上单击“管理”。
4. 单击“保函”。
5. 在“操作窗格”上单击“保函”。
6. 单击“增加值”以打开下拉对话框。
7. 在“添加值”字段中，输入一个数字。
8. 单击“确定”。
9. 转到“现金和银行管理”>“保函”>“保函”。
10. 在列表中，找到并选择所需记录。
11. 单击“增加值”以打开下拉对话框。
12. 单击“确定”。
13. 展开“行为”部分。
    * 核实“增加值”记录。  
14. 在列表中，找到并选择所需记录。
15. 单击以访问“日记帐批号”字段中的链接。
16. 单击“行”。
    * 核实已过帐的日记帐条目。  

## <a name="process-letter-of-guaranteeliquidate"></a>处理保函_清算
1. 转到应收帐项目>订单>所有销售订单。
2. 在列表中，单击所选行中的链接。
3. 在“操作窗格”上单击“管理”。
4. 单击“保函”。
5. 在“操作窗格”上单击“保函”。
6. 单击“清算”以打开下拉对话框。
7. 单击“确定”。
8. 转到“现金和银行管理”>“保函”>“保函”。
9. 在列表中，找到并选择所需记录。
10. 单击“清算”以打开下拉对话框。
11. 单击“确定”。
12. 展开“行为”部分。
    * 核实“清算”记录。  
13. 在列表中，找到并选择所需记录。
14. 单击以访问“日记帐批号”字段中的链接。
15. 单击“行”。
    * 核实已过帐的日记帐条目。  
16. 关闭该页面。


