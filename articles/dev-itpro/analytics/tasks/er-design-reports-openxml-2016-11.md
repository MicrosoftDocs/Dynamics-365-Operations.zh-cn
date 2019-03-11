---
title: ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）
description: 以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建新电子报表 (ER) 配置，使其包含用于生成 OPENXML 格式的电子文档的模板。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "326645"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）

[!include [task guide banner](../../includes/task-guide-banner.md)]

以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建新电子报表 (ER) 配置，使其包含用于生成 OPENXML 格式的电子文档的模板。 此配置将用于处理供应商付款。



在此示例中，您将创建示例公司 Litware 公司的配置。这些步骤可以在 GBSI 公司执行。



为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。 您还必须具有在创建模板时将导入的 Excel 文件。 可从[付款报表模板](https://go.microsoft.com/fwlink/?linkid=862266)访问此文件。


## <a name="upload-the-payments-data-model-configuration"></a>上载付款数据模型配置
1. 转到“组织管理”>“工作区”>“电子申报”。
2. 在列表中，标记所选的行。
    * 为示例公司选择配置供应商“Litware 公司”。如果没有看到此配置供应商，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。  
3. 单击“设置有效”。
4. 单击“存储库”。
    * 为运营资源类型选择存储库（如果有）。 如果可用，跳过有关创建新存储库的以下步骤。  
5. 单击“添加”以打开下拉对话框。
6. 在“配置存储库类型”字段中，输入“运营资源”。
7. 单击“创建存储库”。
8. 单击“确定”。
9. 单击“打开”。
10. 在树结构中，选择“付款模型”。
11. 单击“导入”。
    * 导入此数据模型。 将它用作新格式配置中的数据源。 如果已经导入了此配置则跳过此步骤。  
12. 单击“是”。
13. 关闭该页面。
14. 关闭该页面。

## <a name="create-a-new-format-configuration"></a>创建新的格式配置
1. 单击“申报配置”。
2. 在树结构中，选择“付款模型”。
3. 单击“创建配置”，以打开下拉对话框。
4. 在“新建”字段中，输入“基于数据模型付款模型的格式”。
    * 创建一个基于 PaymentModel 数据模型的格式。  
5. 在“名称”字段中，键入“示例工作表报表”。
    * 示例工作表报表  
6. 在“描述”字段中，键入“供应商付款的示例工作表报表”。
    * 供应商付款的示例工作表报表。  
7. 在“数据模型定义”字段中，输入或选择一个值。
    * 选择“客户贷方转帐发起”定义。  
8. 单击“创建配置”。

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>以 OPENXML 工作表格式设计新文档
1. 在树结构中，选择“付款模型\示例工作表报表”。
2. 单击“设计器”。
3. 在“操作”窗格上，单击“导入”。
4. 单击“从 Excel 导入”。
5. 单击“附加”。
    * 作为模板附加现有 Excel 文档。  
6. 单击“新建”。
7. 单击“文件”。
    * 指向现有 Excel 文件。  
8. 关闭该页面。
9. 在“模板”字段中，输入或选择一个值。
    * 选择用作模板的附加的 Excel 文件。  
10. 单击“确定”。
    * 请注意，ER 格式组件已基于引用 MS Excel 文档的结构以设计格式创建（指定范围）。  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>创建新的数据源以按币种代码计算总计
1. 单击“映射”选项卡。
2. 单击“添加根”以打开下拉对话框。
3. 在树结构中，选择“功能\分组依据”。
4. 在“名称”字段中，键入 'PaymentByCurrency'。
    * 付款币种  
5. 单击“编辑分组依据”。
6. 在树结构中，展开“模型”。
7. 在树结构中，选择“模型\付款”。
8. 单击“将字段添加到”。
9. 单击“什么要分组”。
10. 在树结构中，展开“模型\付款”。
11. 在树结构中，选择“模型\付款\货币”。
12. 单击“将字段添加到”。
13. 单击“分组字段”。
14. 在树结构中，选择“模型\付款\指示金额(InstructedAmount)”。
15. 单击“将字段添加到”。
16. 单击“合并字段”。
17. 在“方法”字段中，选择一个选项。
    * 选择 SUM 合并功能。  
18. 在“名称”字段中，键入 'TotalInstructuredAmount'。
    * TotalInstructuredAmount  
19. 单击“保存”。
20. 关闭该页面。
21. 单击“确定”。

## <a name="map-format-components-to-data-sources"></a>将格式组件映射到数据源
1. 在树结构中，展开“模型”。
2. 在树结构中，展开“模型\付款”。
3. 在树结构中，展开“模型\付款\发起方(InitiatingParty)”。
4. 在树结构中，选择“模型\付款\发起方(InitiatingParty)名称”。
5. 在树结构中，展开或折叠“Excel\报表页眉”。
6. 在树结构中，选择“Excel\报表页眉\公司名称”。
7. 单击“绑定”。
8. 在树结构中，展开“模型\付款\贷方”。
9. 在树结构中，展开“模型\付款\贷方\身份证明”。
10. 在树结构中，选择“模型\付款\贷方\身份证明\源 ID(SourceID)”。
11. 在树结构中，展开或折叠“Excel\付款方式行”。
12. 在树结构中，选择“Excel\付款方式行\供应商帐户名称”。
13. 单击“绑定”。
14. 在树结构中，展开“模型\付款\贷方\名称”。
15. 在树结构中，选择“Excel\付款方式行\供应商名称”。
16. 单击“绑定”。
17. 在树结构中，展开“模型\付款\贷方代理(CreditorAgent)”。
18. 在树结构中，选择“模型\付款\贷方代理(CreditorAgent)\名称”。
19. 在树结构中，选择“Excel\付款方式行\银行”。
20. 单击“绑定”。
21. 在树结构中，选择“模型\付款\贷方代理(CreditorAgent)\银行代号(RoutingNumber)”。
22. 在树结构中，选择“Excel\付款方式行\银行代号”。
23. 单击“绑定”。
24. 在树结构中，展开“模型\付款\贷方科目(CreditorAccount)”。
25. 在树结构中，展开“模型\付款\贷方科目(CreditorAccount)\标识”。
26. 在树结构中，选择“模型\付款\贷方科目(CreditorAccount)\身份证明\编号”。
27. 在树结构中，选择“Excel\付款方式行\帐号”。
28. 单击“绑定”。
29. 在树结构中，选择“模型\付款\指示金额(InstructedAmount)”。
30. 在树结构中，选择“Excel\付款方式行\借方”。
31. 单击“绑定”。
32. 在树结构中，展开“模型\付款\贷方”。
33. 在树结构中，展开“模型\付款\贷方科目(CreditorAccount)”。
34. 在树结构中，展开“模型\付款\贷方代理(CreditorAgent)”。
35. 在树结构中，选择“模型\付款\货币”。
36. 在树结构中，选择“Excel\付款方式行\货币”。
37. 单击“绑定”。
38. 在树结构中，展开 'PaymentByCurrency'。
39. 在树结构中，展开 'PaymentByCurrency\grouped'。
40. 在树结构中，选择“PaymentByCurrency\已分组\货币”。
41. 在树结构中，展开或折叠“Excel\汇总行”。
42. 在树结构中，选择“Excel\汇总行\汇总货币”。
43. 单击“绑定”。
44. 在树结构中，展开 'PaymentByCurrency\aggregated'。
45. 在树结构中，选择 'PaymentByCurrency\aggregated\TotalInstructuredAmount'。
46. 在树结构中，选择“Excel\汇总行\汇总金额”。
47. 单击“绑定”。
48. 在树结构中，选择 'PaymentByCurrency'。
49. 在树中，选择“Excel\汇总行”。
50. 单击“绑定”。
51. 在树结构中，选择“模型\付款”。
52. 在树结构中，选择“Excel\付款方式行”。
53. 单击“绑定”。
54. 单击“保存”。
55. 关闭该页面。

## <a name="use-the-created-configuration-for-payments-processing"></a>将创建的配置用于处理付款
1. 单击“更改状态”。
2. 单击“完成”。
3. 单击“确定”。
4. 关闭该页面。
5. 关闭该页面。
6. 转至“应付账款”>“付款设置”>“付款方式”。
7. 使用快速筛选来筛选带“电子”值的“付款方式”字段。
    * 电子  
8. 单击“编辑”。
9. 展开“文件格式”部分。
10. 在“普通电子申报”字段中，选择“是”。
11. 在“导出格式配置”字段中，输入或选择一个值。
    * 选择“示例工作表报表”配置。  
12. 单击“保存”。
13. 关闭该页面。

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>使用创建的配置进行付款日记帐处理测试
1. 转至“应付账款”>“付款”>“付款日记帐”。
2. 单击“新建”。
    * 新建付款日记帐。  
3. 在“名称”字段中，键入“VendPay”。
    * VendPay  
4. 单击“行”。
5. 在“帐户”字段中，指定值 'GB_SI_000001'。
    * GB_SI_000001  
6. 将“借方”设置为 '1000'。
7. 单击“新建”。
8. 在“帐户”字段中，指定值 'GB_SI_000005'。
    * GB_SI_000005  
9. 将“借方”设置为 '2000'。
10. 在“货币”字段中，键入 'EUR'。
    * 欧元  
11. 在“对方科目”字段中，指定值为 'GBSI OPER'。
    * GBSI OPER  
12. 在“付款方式”字段中，键入“电子”。
    * 电子  
13. 单击“保存”。
14. 点击”生成付款“。
15. 在“付款方式”字段中，键入“电子”。
    * 电子  
16. 在“文件名”字段中，键入“付款”。
    * 例如，键入“付款”。  
17. 在“银行帐户”字段中，键入 'GBSI OPER'。
    * GBSI OPER  
18. 单击“确定”。
19. 单击“确定”。
    * 审查已创建的工作表，包括付款行详细信息以及用于此付款消息的每个币种代码的总计。  

