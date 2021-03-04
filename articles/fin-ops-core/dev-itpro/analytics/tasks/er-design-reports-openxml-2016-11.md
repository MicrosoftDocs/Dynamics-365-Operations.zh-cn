---
title: ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）
description: 此主题介绍系统管理员或电子报表开发人员角色的用户如何创建新电子报表 (ER) 配置，使其包含用于生成 OPENXML 格式的电子文档的模板。
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf909efbac5dce8e22d9713ad2e694ce624ffeb0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681893"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）

[!include [banner](../../includes/banner.md)]

此主题介绍系统管理员或电子报表开发人员角色的用户如何创建新电子报表 (ER) 配置，使其包含用于生成 OPENXML 格式的电子文档的模板。 此配置将用于处理供应商付款。

在此示例中，您将创建示例公司 Litware 公司的配置。这些步骤可以在 GBSI 公司执行。

为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。 您还必须具有在创建模板时将导入的 Excel 文件。 可从[付款报表模板](https://go.microsoft.com/fwlink/?linkid=862266)访问此文件。


## <a name="upload-the-payments-data-model-configuration"></a>上载付款数据模型配置
1. 在导航窗格中，转到 **模块 > 组织管理 > 工作区 > 电子申报**。
2. 在列表中，标记示例公司“Litware 公司”的配置供应商。如果没有看到此配置供应商，您必须首先完成[创建配置提供程序并将其标记为有效](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。
3. 选择 **设置有效**。
4. 选择 **存储库**。 为运营资源类型选择存储库（如果有）。 如果可用，跳过有关创建新存储库的以下步骤。  
5. 选择 **添加** 以打开下拉对话框。
6. 在 **配置存储库类型** 字段中，输入 `Operations resourcesdd`。
7. 选择 **创建存储库**。
8. 选择 **确定**。
9. 选择 **打开**。
10. 在树结构中，选择 **付款模型**。
11. 选择 **导入**。 导入此数据模型。 将它用作新格式配置中的数据源。 如果已经导入了此配置则跳过此步骤。  
12. 选择 **是**。
13. 关闭此页面，直到返回到“电子申报”页面。

## <a name="create-a-new-format-configuration"></a>创建新的格式配置
1. 选择 **申报配置**。
2. 在树结构中，选择 **付款模型**。
3. 选择 **创建配置**，以打开下拉对话框。
4. 在 **新建** 字段中，输入 `Format based on data model PaymentModel`。 创建一个基于 PaymentModel 数据模型的格式。
5. 在 **名称** 字段中，键入 `Sample worksheet report`。 示例工作表报表  
6. 在 **描述** 字段中键入 `Sample worksheet report for vendors' payments`。 供应商付款的示例工作表报表。  
7. 在 **数据模型定义** 字段中，输入或选择一个值。 选择 **CustomerCreditTransferInitiation** 定义。  
8. 选择 **创建配置**。

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>以 OPENXML 工作表格式设计新文档
1. 在树结构中，选择 **付款模型\示例工作表报表**。
2. 选择 **设计器**。
3. 在操作窗格上，选择 **导入**。
4. 选择 **从 Excel 导入**。
5. 选择 **附件**。 作为模板附加现有 Excel 文档。  
6. 选择 **新建**。
7. 选择 **文件**。 指向现有 Excel 文件。  
8. 关闭该页面。
9. 在 **模板** 字段中，输入或选择一个值。 选择用作模板的附加的 Excel 文件。  
10. 选择 **确定**。 请注意，ER 格式组件已基于引用 MS Excel 文档的结构以设计格式创建（指定范围）。  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>创建新的数据源以按币种代码计算总计
1. 选择 **映射** 选项卡。
2. 选择 **添加根** 以打开下拉对话框。
3. 在树结构中，选择 **功能\分组依据**。
4. 在 **名称** 字段中，键入 `PaymentByCurrency`。
5. 选择 **编辑分组依据**。
6. 在树中，展开 **模型**，然后选择 **模型\付款**。
7. 选择 **将字段添加到**。
8. 选择 **什么要分组**。
9. 在树中，展开 **模型\付款**，然后选择 **模型\付款\货币**。
10. 选择 **将字段添加到**。
11. 选择 **分组字段**。
12. 在树结构中，选择 **模型\付款\指示金额(InstructedAmount)**。
13. 选择 **将字段添加到**，然后选择 **合并字段**。
14. 在 **方法** 字段中，选择一个选项。 选择 **SUM 合并** 功能。  
15. 在 **名称** 字段中，键入 `TotalInstructuredAmount`。
16. 选择 **保存**。
17. 关闭该页面。
18. 选择 **确定**。

## <a name="map-format-components-to-data-sources"></a>将格式组件映射到数据源
1. 在树结构中，选择 **模型\付款\发起方(InitiatingParty)\名称** 和 **Excel\ReportHeader\CompanyName**。
2. 选择 **绑定**。
3. 在树结构中，选择 **模型\付款\贷方\身份证明\源 ID(SourceID)** 和 **Excel\PaymLines\VendAccountName**。
4. 选择 **绑定**。
5. 在树中，选择 **模型\付款\贷方\名称** 和 **Excel\PaymLines\VendName**。
6. 选择 **绑定**。
7. 在树中，选择 **模型\付款\贷方代理(CreditorAgent)\名称** 和 **Excel\PaymLines\银行**。
8. 选择 **绑定**。
9. 在树中，选择 **模型\付款\贷方代理(CreditorAgent)\银行代号(RoutingNumber)** 和 **Excel\PaymLines\RoutingNumber**。
10. 选择 **绑定**。
11. 在树结构中，选择 **模型\付款\贷方帐号(CreditorAccount)\证件\编号** 和 **Excel\PaymLines\VendAccountName**。
12. 选择 **绑定**。
13. 在树结构中，选择 **模型\付款\指示金额(InstructedAmount)** 和 **Excel\PaymLines\Debit**。
14. 选择 **绑定**。
15. 在树中，选择 **模型\付款\货币** 和 **Excel\PaymLines\货币**。
16. 选择 **绑定**。
17. 在树中，选择 **PaymentByCurrency\grouped\Currency** 和 **Excel\SummaryLines\SummaryCurrency**。
18. 选择 **绑定**。
19. 在树中，选择 **PaymentByCurrency\aggregated\TotalInstructuredAmount** 和 **Excel\SummaryLines\SummaryAmount**。
20. 选择 **绑定**。
21. 在树中，选择 **PaymentByCurrency** 和 **Excel\SummaryLines**。
22. 选择 **绑定**。
23. 在树中，选择 **模型\付款** 和 **Excel\PaymLines**。
24. 选择 **绑定**。
25. 选择 **保存**，然后关闭页面。

## <a name="use-the-created-configuration-for-payments-processing"></a>将创建的配置用于处理付款
1. 选择 **更改状态**。
2. 选择 **完成**。
3. 选择 **确定**。
4. 在导航窗格中，转到 **模块 > 应付帐款 > 付款设置 > 付款方式**。
5. 使用快速筛选来筛选带 **电子** 值的 **付款方式** 字段。
6. 选择 **编辑**。
7. 展开 **文件格式** 部分。
8. 在 **普通电子申报** 字段中，选择 **是**。
9. 在 **导出格式配置** 字段中，输入或选择一个值。 选择 **示例工作表报表** 配置。  
10. 选择 **保存**。
11. 关闭该页面。

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>使用创建的配置进行付款日记帐处理测试
1. 在导航窗格中，转到 **模块 > 应付帐款 > 付款 > 付款日记帐**。
2. 选择 **新建** 以创建新付款日记帐。
3. 在 **名称** 字段中，键入 **VendPay**。
4. 选择 **行**。
5. 在 **帐户** 字段中，指定值 `GB_SI_000001`。
6. 将 **借方** 设置为 `1000`。
7. 选择 **新建**。
8. 在 **帐户** 字段中，指定值 `GB_SI_000005`。
9. 将 **借方** 设置为 `2000`。
10. 在 **货币** 字段中，键入 `EUR`。
11. 在 **抵消帐户** 字段中，指定值 `GBSI OPER`。
12. 在 **付款方式** 字段中，键入 `Electronic`。
13. 选择 **保存**。
14. 选择 **生成付款**。
15. 在 **付款方式** 字段中，键入 `Electronic`。
16. 在 **文件名** 字段中，键入 `Payments`。
17. 在 **银行帐户** 字段中，键入 `GBSI OPER`。
18. 选择 **确定**，然后再次选择 **确定**。 审查已创建的工作表，包括付款行详细信息以及用于此付款消息的每个币种代码的总计。  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]