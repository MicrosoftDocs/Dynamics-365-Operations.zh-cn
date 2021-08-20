---
title: 设计 ER 表达式以调用应用类方法
description: 本主题介绍如何通过调用必需的应用程序类方法来在电子报告配置中重用现有的应用程序逻辑。
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78e7596760c4707578e2458a93631b571a7bfec86b9c51d877502ba04ed843a2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726277"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>设计 ER 表达式以调用应用类方法

[!include [banner](../../includes/banner.md)]

本指南提供有关如何通过在 ER 表达式中调用必需的应用类方法来在电子报告 (ER) 配置中重用现有应用逻辑的信息。 用于调用类的参数值可以在运行时动态定义：例如，根据分析文档中的信息确保其正确性。 在此指南中，将为示例公司 Litware 公司创建所需 ER 配置。此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。 

可使用任何数据集完成这些步骤。 您还必须下载和本地保存以下文件：(https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt。

为了完成这些步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。

1. 转到“组织管理”>“工作区”>“电子申报”。
    * 验证示例公司 Litware 公司的配置提供程序可用且标记为有效。 如果没有看到此配置提供程序，您必须首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。   
    * 您在设计一个流程，用于分析传入的银行对帐单以进行应用程序数据更新。 您将以包含 IBAN 代码的 TXT 文件形式收到传入的银行对帐单。 作为银行对帐单导入过程的一部分，您需要使用已经提供的逻辑验证此 IBAN 代码的更正。   

## <a name="import-a-new-er-model-configuration"></a>导入新 ER 模型配置
1. 在列表中，找到并选择所需记录。
    * 选择 Microsoft 提供程序磁贴。  
2. 单击“存储库”。
3. 单击“显示筛选器”。
4. 添加筛选器字段“类型名称”。 在“名称”字段中，输入值“资源”，选择“包含”筛选器运算符，然后单击“应用”。
5. 单击“打开”。
6. 在树结构中，选择“付款模型”。
    * 如果“版本”快速选项卡上的“导入”按钮未启用，说明您已导入了一个 ER 配置“付款模型”的版本 1。 您可以跳过此子任务的其余步骤。   
7. 单击“导入”。
8. 单击“是”。
9. 关闭该页面。
10. 关闭该页面。

## <a name="add-a-new-er-format-configuration"></a>添加新 ER 格式配置
1. 单击“申报配置”。
    * 添加新的 ER 格式来分析 TXT 格式的传入银行对帐单。  
2. 在树结构中，选择“付款模型”。
3. 单击“创建配置”，以打开对话框菜单。
4. 在“新建”字段中，输入“基于数据模型付款模型的格式”。
5. 在“名称”字段中，键入“银行对帐单导入格式（示例）”。
    * 银行对帐单的导入格式（示例）  
6. 在“支持数据导入”字段中选择"是"。
7. 单击“创建配置”。

## <a name="design-the-er-format-configuration---format"></a>设计 ER 格式配置 - 格式
1. 单击“设计器”。
    * 设计的格式表示 TXT 格式的外部文件的预期结构。  
2. 单击“添加根”以打开对话框菜单。
3. 在树中，选择“文本\序列”。
4. 在“名称”字段中，键入“根”。
    * 根  
5. 在"特殊字符"字段中，选择“换行 - Windows (CR LF)”。
    * 已在“特殊字符”字段中选择选项“新行 - Windows (CR LF)”。 基于此设置，分析文件中的每一行均被视为单独的记录。  
6. 单击“确定”。
7. 单击“添加”以打开下拉对话框。
8. 在树中，选择“文本\序列”。
9. 在“名称”字段中键入“Rows”。
    * 行数  
10. 在“多样性”字段中，选择“一个 多个”。
    * 已选择“多样性”字段中的选项“一个 多个”。 基于此设置，应该至少在分析文件中存在一个行。  
11. 单击“确定”。
12. 在树中，选择“Root\Rows”。
13. 单击“添加序列”。
14. 在“名称”字段中，键入“Fields”。
    * 字段  
15. 在“多样性”字段中，选择“正好一个”。
16. 单击“确定”。
17. 在树中，选择“Root\Rows\Fields”。
18. 单击“添加”以打开下拉对话框。
19. 在树结构中，选择“文本\字符串”。
20. 在“名称”字段中，键入“IBAN”。
    * IBAN / 国际银行帐号  
21. 单击“确定”。
    * 已配置为分析文件的每一行只包含一个 IBAN 代码。  
22. 单击“保存”。

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>设计 ER 格式配置 – 数据模型映射
1. 单击”将格式映射到模型“。
2. 单击“新建”。
3. 在“定义”字段中，键入“BankToCustomerDebitCreditNotificationInitiation”。
    * BankToCustomerDebitCreditNotificationInitiation  
4. 改变定义。
5. 在“名称”字段中，键入“数据模型映射”。
    * 数据模型映射  
6. 单击“保存”。
7. 单击“设计器”。
8. 在树中，选择“Dynamics 365 for Operations\Class”。
9. 单击“添加根”。
    * 添加新的数据源以调用 IBAN 代码验证使用的现有应用程序逻辑。  
10. 在“名称”字段中，键入“check_codes”。
    * check_codes  
11. 在“类”字段中，键入“ISO7064”。
    * ISO7064  
12. 单击“确定”。
13. 在树中，展开“格式”。
14. 在树中，展开“format\Root: Sequence(Root)”。
15. 在树中，选择“format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)”。
16. 单击“绑定”。
17. 在树中，展开“format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)”。
18. 在树中，展开“format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)”。
19. 在树中，选择“format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)”。
20. 在树中，展开“付款 = format.Root.Rows”。
21. 在树结构中，展开“付款 = format.Root.Rows\Creditor Account(CreditorAccount)”。
22. 在树结构中，展开“付款 = format.Root.Rows\Creditor Account(CreditorAccount)\Identification”。
23. 在树中，选择“付款 = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN”。
24. 单击“绑定”。
25. 单击“验证”选项卡。
26. 单击“新建”。
    * 增加新的验证规则，其显示包含无效的 IBAN 代码的分析文件中任何行的错误。  
27. 单击“编辑条件”。
28. 在树结构中，展开“check_codes”。
29. 在树中，选择“check_codes\verifyMOD1271_36”。
30. 单击“添加数据源”。
31. 在“公式”字段中，输入“check_codes.verifyMOD1271_36(”。
    * check_codes.verifyMOD1271_36(  
32. 在树中，展开“格式”。
33. 在树中，展开“format\Root: Sequence(Root)”。
34. 在树中，展开“format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)”。
35. 在树中，展开“format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)”。
36. 在树中，选择“format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)”。
37. 单击“添加数据源”。
38. 在“公式”字段中，输入“check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)”。
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. 单击“保存”。
40. 关闭该页面。
    * 验证条件已配置为通过调用应用程序类“ISO7064”的现有方法“verifyMOD1271_36”为任何无效的 IBAN 代码返回 FALSE。 请注意，IBAN 代码的值在运行时被动态定义为基于分析 TXT 文件的内容调用方法的参数。   
41. 单击“编辑消息”。
42. 在“公式”字段中，输入“CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)”。
    * CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)  
43. 单击“保存”。
44. 关闭该页面。
45. 单击“保存”。
46. 关闭该页面。

## <a name="run-the-format-mapping"></a>运行格式映射
为了测试，请使用以前下载的 SampleIncomingMessage.txt 文件执行格式映射。 生成的输出包含将从所选 TXT 文件导入，并在实际导入时填充到自定义数据模型的数据。   
1. 单击“运行”。
    * 单击“浏览”并导航到前面下载的 SampleIncomingMessage.txt 文件。  
2. 单击“确定”。
    * 检查 XML 格式的输出，该输出表示已从所选文件导入并移植到数据模型的数据。 请注意，导入的 TXT 文件只有 3 行被处理。 无效的第 4 行中的 IBAN 代码已跳过，并在信息日志中提供错误消息。  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]