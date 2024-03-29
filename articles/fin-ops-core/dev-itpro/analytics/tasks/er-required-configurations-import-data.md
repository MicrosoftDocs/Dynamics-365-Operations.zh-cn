---
title: ER 创建从外部文件导入数据所需配置
description: 本文介绍如何设计电子报告配置，以将数据从外部文件导入到 Microsoft Dynamics 365 Finance 应用。
author: kfend
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
ms.openlocfilehash: 199873af83ec14d441aa3927dc84509486e4927a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290145"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>ER 创建从外部文件导入数据所需配置

[!include [banner](../../includes/banner.md)]

以下步骤说明属于系统管理员或电子报表开发人员的用户如何设计电子报表 (ER) 配置，以便将数据从外部文件导入应用程序中。 在此示例中，将为示例公司 Litware 公司创建所需 ER 配置。若要完成这些步骤，您必须首先完成任务指南“ER 创建一个配置提供程序，并标记其为当前运行的”中的步骤。 可使用 USMF 数据集完成这些步骤。 还必须下载并在本地保存以下文件： 

| 内容描述                       | 文件名                                     |
|-------------------------------------------|-----------------------------------------------|
| ER 数据模型配置 - 1099 | [1099model,xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)                  |
| ER 格式配置 - 1099    | [1099format.xml](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)                  |
| XML 格式的传入文档示例                          | [1099entries.xml](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)        |
| 管理传入文档数据的工作簿的示例                          | [1099entries.xlsx](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx) |

ER 让用户可以配置将外部数据文件以 .XML 或 .TXT 格式导入表的过程。 首先，必须设计抽象数据模型和 ER 数据模型配置来表示要导入的数据。 接下来，需要定义要导入的文件的结构和将用于把数据从文件移植到抽象数据模型的方法。 必须为该抽象数据模型创建映射到设计的数据模型的 ER 格式配置。 然后，必须使用映射扩展数据模型，该映射介绍导入的数据如何作为抽象数据模型长期存在和如何用于更新表。  必须为 ER 数据模型配置追加一个新模型映射，该映射介绍如何将数据模型绑定到应用程序的目标。  

以下方案演示 ER 数据导入功能。 其中包括在外部跟踪，然后导入，以便以后在 1099 的供应商结算中报告的供应商交易。   

## <a name="add-a-new-er-model-configuration"></a>添加新 ER 模型配置
1. 转到“组织管理”>“工作区”>“电子申报”。

    验证示例公司“Litware 公司”的配置提供程序 可用且标记为有效。 如果没有看到此配置提供程序，您必须首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。   

2. 单击“申报配置”。

    加载前面下载的 1099model.xml 文件，而不是创建新模型。 此文件中包含供应商的交易的自定义数据模型。 此数据模型映射到 AOT 数据实体中的数据组件。   

3. 单击“交换”。
4. 单击“从 XML 文件加载”。

    单击“浏览”并导航到前面下载的 1099model.xml 文件。  

5. 单击“确定”。
6. 在树结构中，选择“1099 付款模型”。

## <a name="review-data-model-settings"></a>检查数据模型设置
1. 单击“设计器”。

    此模型设计为从业务角度表示供应商的交易，并且这些交易独立于实施。   

2. 在树结构中，展开“1099-MISC”。
3. 在树结构中，选择“1099-MISC\交易”。
4. 在树结构中，展开“1099-MISC\交易”。

    此模型的“交易”元素表示单笔交易。 子元素则用于指定所需的详细信息，如每笔交易的供应商帐户和交易日期。   

5. 关闭该页面。

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>添加支持导入数据的新 ER 格式配置
此子任务中的步骤演示可如何创建新格式配置来管理数据从外部文件的导入。   
1. 单击“创建配置”，以打开下拉对话框。
2. 在“新建”字段中，输入“基于数据模型 1099 付款模型的格式”。
3. 在“支持数据导入”字段中选择"是"。
4. 按 ESC 键关闭此页。

    加载前面下载的文件 1099format.xml 文件，而不是创建新格式来支持数据导入。 此文件中包含为要导入的文件定义的结构和该结构到供应商交易的自定义数据模型的映射。   
5. 单击“交换”。
6. 单击“从 XML 文件加载”。
    单击“浏览”并导航到前面下载的 1099format.xml 文件。  
7. 单击“确定”。
8. 在树结构中，展开“1099 付款模型”。
9. 在树结构中，选择“”1099 付款模型\用于导入供应商的交易的格式“。

## <a name="review-format-settings"></a>检查格式设置
1. 单击“设计器”。
2. 打开”显示详细信息“。
3. 单击”展开/折叠“。
4. 单击”展开/折叠“。

    设计的格式表示外部文件的预期结构。 此文件必须为 XML 格式且具有结算根元素。 每个供应商的交易通过交易元素表示，交易元素定义为拥有零对多多重性。 这意味着传入的文件可能包含从零到多笔交易的任何位置。 “交易”元素的嵌套元素表示单笔交易的属性。 请注意，除国家/地区外的所有属性都标记为必需项，也就是说导入文件中必须包含这些属性。   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>检查格式到数据模型的映射的设置
1. 单击”将格式映射到模型“。

    “对于导入供应商的交易”这一映射中包含从传入的 XML 文件到所选自定义数据模型部分的数据传输规则，该规则通过选择 1099-MISC 定义来定义。  

2. 单击“设计器”。
3. 打开”显示详细信息“。
4. 在树形图中，展开“格式: 记录”。
5. 在树结构中，选择“格式: 记录”。

    请注意，设计的格式在此处表示为数据源组件。  

6. 在树中，展开 `format: Record\*settlement: XML Element 1..1 (settlement): Record`。
7. 在树中，展开 `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list`。
8. 在树中，展开 `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`。
9. 在树中，展开 `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record`。
10. 在树中，选择 `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`。

    请注意，在预定义的“格式”数据源组件中，必需格式元素和可选格式元素的表示形式不同。  
11. 在树结构中，展开“交易: 记录列表= format.settlement.'$enumerated'”。

    请注意，用于定义所导入文件的结构的格式的元素绑定到自定义数据模型的元素。 所导入 XML 文件的内容将在运行时在现有数据模型中根据这些绑定排序。 请注意国家/地区元素的绑定。 对于无此类元素的传入文件中的任何交易元素，将在数据模型中填充默认国家/地区代码“USA”。  

12. 单击“验证”选项卡。

    此格式映射中可以包含用户定义的逻辑，用于从业务角度验证导入的数据的精确性。 例如，将根据此设置为所导入文件中未定义国家/地区代码的任何交易在信息日志中生成一条警告消息，通知用户该情况，并指示交易的序列号。  

13. 关闭该页面。

## <a name="run-the-format-mapping-to-the-data-model"></a>运行格式到数据模型的映射
请为测试目的执行此格式映射。 使用前面下载的 1099entries.xml 文件。 可以从用于管理供应商交易的 1099entries.xlsx 工作簿导出此文件。 生成的输出将从所选 XML 文件导入，并在实际导入时填充自定义数据模型。  

1. 单击“运行”。

    单击“浏览”并导航到前面下载的 1099entries.xml 文件。  

2. 单击“确定”。

    请注意关于导入的文件中某笔交易缺少国家/地区代码的警告消息。  
    
    检查 XML 格式的输出，该输出表示已从所选文件导入并移植到数据模型的数据。   

3. 关闭该页面。
4. 关闭该页面。

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>检查模型到目标的映射的设置
1. 在树结构中，选择“1099 付款模型”。
2. 单击“设计器”。
3. 单击“映射模型到数据源”。

    已为“对于 1099 手动交易导入”这一映射定义了“截止目标”方向类型。 这意味着输入它是为了支持数据导入，并且其中包含有关导入并以抽象数据模型数据的形式长期存在的外部文件如何用于填充应用程序中的表的规则的设置。  

4. 单击“设计器”。
5. 在树结构中，展开“模型: 数据模型 1099 付款模型”。
6. 在树结构中，展开“模型: 数据模型 1099 付款模型\交易: 记录列表”。

    请注意，设计的模型在此处表示为数据源元素。 在运行时，其中将包含从外部文件导入的数据。 添加了若干表来充当数据源元素，以便确保导入的数据与当前应用程序的数据一致，包括导入交易供应商帐户是否在系统中可用，导入国家/地区和省/直辖市/自治州代码的组合是否存在等。  

7. 在树结构中，选择“模型: 数据模型 1099 付款模型\交易: 记录列表\$failed: 计算字段 = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean”。
8. 单击“编辑”。
9. 单击“编辑公式”。

    当导入的单笔交易至少一项验证失败，数据源属性“$failed”将把该交易标记为失败。  

10. 关闭该页面。
11. 单击“取消”。
12. 在树结构中，选择“tax1099trans: 表 'VendSettlementTax1099' 记录= model.Validated“。
13. 单击”编辑目标“。

    添加此 ER 目标是为了指定导入的数据将如何更新应用程序表。 在此案例中，已选择了数据表 VendSettlementTax1099。 由于已选择了记录操作插入，所以将把导入的交易插入到表 VendSettlementTax1099 中。 请注意，一个模型映射中可以包含多个目标。 这意味着导入的数据可用于一次更新应用程序的多个表。 表、视图和数据实体可用作 ER 目标。   

    如果将从应用程序中专门为此操作设计的某个点（如按钮或菜单项）调用映射，应将 ER 目标标记为集成点。 在此示例中，为 ERTableDestination#VendSettlementTax1099 点。  

14. 单击“取消”。
15. 单击“全部显示”。
16. 单击”只显示映射的“。
17. 在树结构中，展开“tax1099trans: 表 'VendSettlementTax1099' 记录= model.Validated“。

    请注意，仅包含已验证交易的数据源元素绑定到创建的目标。 您可以筛选导入的交易，以便跳过与应用程序的数据不兼容的交易。  

18. 在树结构中，选择“failed: 表 'VendSettlementTax1099Entity' 记录 = model.Failed“。
19. 单击“验证”选项卡。

    此模型映射中可以包含用户定义的逻辑，用于验证从现有应用程序数据导入的数据的正确性。 例如，将根据现有设置为位于所导入文件中但在系统中不存在的任何交易生成一条警告消息，通知用户并指示不正确的供应商帐户代码。  

    请注意，“验证后操作”选项可用于各项验证后，以指定是继续还是停止导入过程，以及可以保留还是回滚已执行的插入/更新。  

20. 单击”只显示映射的“。
21. 单击“全部显示”。
22. 关闭该页面。

    执行此模型映射以测试设计的格式和模型映射。 使用文件 1099entries.xml。 将把所选文件中的数据导入系统。  

23. 单击“运行”。

    请注意，此对话框中包含有关必须用于解析所导入文件，然后将数据移植到数据模型的格式映射的更多问题。 这是因为现在只有一种格式在使用此模型，这种格式标记为已设计是为了支持数据导入。  
    
    定义凭证 ID 以区分导入的交易和可能已手动输入或导入的其他交易。  

24. 在“输入凭证 ID”字段中，键入“IMPORT-001”。

    浏览以找到“1099entries.xml”文件。  

25. 单击“确定”。

    所生成警告的列表提供有关错误供应商帐户、错误税 1099 栏代码、缺少的国家/地区代码等的信息。请将此警告列表与执行 XML 文件中包含的内容比较。  

26. 关闭该页面。
27. 关闭该页面。
28. 关闭该页面。
29. 关闭该页面。
30. 转至“应付帐款 > 定期任务 > 1099 税 > 用于 1099 的供应商结算”。

    此窗体显示根据所导入交易创建的 Tax1099Summary 表中的累计交易。  

31. 在“开始日期”字段中，将日期设置为“2000-01-01”。
32. 单击“手动 1099 交易记录”。

    此窗体中包含手动添加的交易和我们刚才导入的交易的列表。  

33. 打开凭证列筛选器。
34. 使用 "开头为" 筛选器运算符在 "凭证" 字段上输入筛选器值 "IMPORT-001"。

## <a name="review-the-relationship-between-model-and-format-mappings"></a>检查模型与格式之间的映射的关系
1. 关闭该页面。
2. 关闭该页面。
3. 转到“组织管理”>“工作区”>“电子申报”。
4. 单击“申报配置”。
5. 在树结构中，选择“1099 付款模型”。

    假设您希望支持导入相同数据，但是通过 .TXT 文件格式导入。   

6. 单击“创建配置”，以打开对话框。 
7. 在“新建”字段中，输入“基于数据模型 1099 付款模型的格式”。
8. 在“名称”字段中，键入“从 TXT 文件导入数据”。
9. 在“支持数据导入”字段中选择"是"。
10. 单击“创建配置”。
11. 单击“设计器”。
12. 单击”将格式映射到模型“。
13. 单击“新建”。
14. 在“定义”字段中，输入或选择一个值。

    选择“1099-MISC”选项。  

15. 在“名称”字段中，键入“从 TXT 文件导入数据”。
16. 在“描述”字段中，键入“从 TXT 文件导入数据”。
17. 单击“保存”。
18. 关闭该页面。
19. 关闭该页面。
20. 单击“编辑”。

    如果您安装了修补程序“KB 4012871 在单独的配置中支持 GER 模型映射，以便可以为在不同版本的 Dynamics 365 Finance 上部署指定不同类型的先决条件”([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871))，请为输入的格式配置执行下一步“开启标记‘模型映射的默认值’”。 否则跳过下一步。  

21. 在“模型映射的默认值”字段中选择“是”。
22. 在树结构中，选择“1099 付款模型”。
23. 单击“设计器”。
24. 单击“映射模型到数据源”。
25. 单击“运行”。

    如果您安装了修补程序“KB 4012871 在单独的配置中支持 GER 模型映射，以便可以为在不同版本上部署指定不同类型的先决条件 ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871))，请在查找字段中选择首选模型映射。 如果您尚未安装此修补程序，请跳至下一步，因为默认格式配置的定义已选择了映射。  
    
    如果您尚未安装修补程序 KB 4012871，请注意对话框中还包含一个模型映射问题，用于解析您要导入的文件。 然后将数据从对话框移植到数据模型。 目前，您可以根据计划导入的文件类型选择必须使用哪种格式映射。  
    
    如果您计划从应用程序中专为此操作设计的某一点调用此模型映射，则必须将 ER 目标和格式映射标记为集成的组成部分。  

26. 单击“取消”。
27. 关闭该页面。
28. 关闭该页面。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
