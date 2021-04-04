---
title: 设计 ER 配置以从 CSV 格式的外部文件导入数据
description: 使用此过程可以设计电子报告配置以从 CSV 格式的外部文件将数据导入 Finance and Operations 应用。
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: 82c3af7d49f725a045b17cbef00b56fdfa0383f3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564110"
---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>设计 ER 配置以从 CSV 格式的外部文件导入数据

[!include [banner](../../includes/banner.md)]

使用此过程可以设计电子报告 (ER) 配置以从 CSV 格式的外部文件将数据导入应用程序。 在此过程中，将为示例公司 Litware 公司创建所需 ER 配置。若要完成这些步骤，您必须首先完成过程“ER 创建一个配置提供程序，并标记其为当前运行的”中的步骤。

此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。 可使用 USMF 数据集完成这些步骤。

还必须下载以下文件并保存到本地：[Dynamics 365 Finance 电子申报示例](https://go.microsoft.com/fwlink/?linkid=862266)：1099model.xml、1099formatcsv.xml、1099entriescsv.csv。

1. 转到“组织管理”>“工作区”>“电子申报”。
    * 您可以配置一个流程，以 XML、TXT 或 CSV 格式将外部文件导入应用程序的表中。 首先，必须从业务角度创建一个抽象数据模型来代表导入的数据 – 为此创建 ER 数据模型配置。 接下来，将映射到设计的数据模型的导入文件结构定义为将数据从文件转移到抽象数据模型的方式 – 为此创建 ER 格式配置。 然后，必须使用新的模型映射扩展 ER 数据模型配置，该映射介绍导入文件的数据和抽象数据模型的永久性数据如何用于更新申请表或数据实体。
    * 以下步骤显示外部跟踪的供应商交易记录如何从外部 CSV 文件导入以便以后用于 1099 窗体的供应商结算。
    * 验证示例公司 Litware 公司的配置提供程序可用且标记为有效。 如果没有看到此配置提供程序，您必须首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。
2. 单击“申报配置”。
3. 应用“1099 付款模型”筛选器。 如果您已经完成了过程“ER 针对电子申报创建从外部文件导入数据所需配置”，并且“1099 付款模型”配置在配置树中可用，则跳过下一个子任务的所有步骤。

## <a name="add-a-new-er-model-configuration"></a>添加新 ER 模型配置

1. 加载前面下载的 1099model.xml 文件，而不是创建新模型。 此文件中包含供应商的交易的自定义数据模型。 此数据模型已映射到必要的数据组件。
2. 单击“交换”。
3. 单击“从 XML 文件加载”。
4. 单击“浏览”并导航到前面下载的 1099model.xml 文件。
5. 单击“确定”。

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>添加支持导入数据的新 ER 格式配置

1. 在树结构中，选择“1099 付款模型”。
2. 单击“创建配置”，以打开下拉对话框。
3. 在“新建”字段中，输入“基于数据模型 1099 付款模型的格式”。
4. 在“支持数据导入”字段中选择"是"。
5. 按 ESC 键关闭此页。
    * 加载前面下载的文件 1099formatcsv.xml 文件，而不是创建新的 ER 格式来支持数据导入。 此文件中包含所需的 ER 格式，该格式定义传入 CSV 文件的结构以及此结构与供应商交易的数据模型的映射。
6. 单击“交换”。
7. 单击“从 XML 文件加载”。
    * 单击“浏览”并导航到前面下载的 1099formatcsv.xml 文件。
8. 单击“确定”。
9. 在树结构中，展开“1099 付款模型”。
10. 在树结构中，选择“1099 付款模型\用于导入供应商的交易 (CSV)”。

## <a name="review-format-settings"></a>检查格式设置

1. 单击“设计器”。
2. 单击”展开/折叠“。
3. 打开”显示详细信息“。
    * 设计的格式表示 CSV 格式的外部文件的预期结构。
4. 在树中，选择“Incoming: File\Root: Sequence”。
    * 对于类型 SEQUENCE 的根元素，已选择了“特殊字符”字段中的选项“新行 - Windows (CR LF)”。 基于此设置，必须将分析文件的每一行视为单独的记录。
5. 在树中，选择 `Incoming: File\Root: Sequence\Line: Sequence 1..*`。
    * 对于类型 SEQUENCE 的 Root\Line 元素，已选择了“多样性”字段中的选项“一个 多个”。 基于此设置，至少在分析文件中存在一个行。
6. 在树中，选择 `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case`。
    * 请注意，类型 CASE 的 Root\Line\Types 元素已添加为 Root\Line 序列的嵌套元素。 由于此 CASE 元素包含 3 个嵌套序列元素，此设置假定我们在分析文件中预期要达到 3 个不同的行类型。
7. 在树中，选择 `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Header: Sequence 1..1`。
    * 类型 SEQUENCE 的 Root\Line\Types\Header 元素包含嵌套的 STRING 元素，其值已被定义为固定字符串值。 此序列将分析分析文件的标题行。
8. 在树中，选择 `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)`。
    * 类型 SEQUENCE 的 Root\Line\Types\Record 元素已被配置为分析交易记录行。 请注意，“自定义分隔符”字符选项已被配置为逗号。 这意味着逗号将用作分析文件中此行类型的字段的分隔符。
    * 请注意，已为 Root\Line\Types\Record 元素添加了多个不同数据类型的嵌套元素以用于作为分隔的字段分析交易记录行。 请注意，“报价单申请表”选项没有配置为“无”。 这意味着在分析文件中，此类型的所有字段都将被视为包含括住的字符。
9. 在树中，选择 `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\TransactionDate: DateTime`。
    * 例如，类型 DATETIME 的 Root\Line\Types\Record\TransactionDate 元素已被配置为从“M/d/yyyy”格式的分析文件获取交易日期和时间值。
10. 在树中，选择 `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\CountryCode: String 0..1`。
    * 请注意，类型 STRING 的 Root\Line\Types\Record\CountryCode 元素已被配置为在“多样性”字段中包含选项“零个 一个”。 此设置将分析行中的 CountryCode 字段的值视为可选。
11. 在树中，选择 `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\Remark: Sequence 1..1 (,)`。
    * 请注意，类型 SEQUENCE 的 Root\Line\Types\Record\Remark 元素已被配置为在“报价单申请表”字段中包含选项“所有”，并在“报价单标记”字段中包含双引号字符。 这意味着分析文件（由嵌套元素描述：STRING 类型的文本）中此行类型的所有字段都将被视为以双引号括住的字符。
12. 在树中，选择 `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Unparsed: Sequence 1..1`。
    * 类型 SEQUENCE 的 Root\Line\Types\Unparsed 元素已被配置为分析与父 CASE 元素中的上述结构不一致的结构的交易记录行。

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>检查格式到数据模型的映射的设置

1. 单击”将格式映射到模型“。
    * 模型映射“从 CSV 格式的模型映射”描述从传入的 CSV 文件到数据模型的数据传输的数据流。
2. 单击“设计器”。
3. 在树中，展开“格式”。
    * 请注意，设计的格式在此处表示为数据源组件。
4. 在树中，展开“format\Incoming: File(Incoming)”。
5. 在树中，展开“format\Incoming: File(Incoming)\Root: Sequence(Root)”。
6. 在树中，展开 `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)`。
7. 在树中，展开 `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)`。
8. 在树中，展开 `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)`。
9. 在树中，展开 `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data`。
10. 在树中，展开 `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\CountryCode: String 0..1 (CountryCode)`。
11. 在树中，选择 `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\TransactionDate: DateTime(TransactionDate)`。
    * 请注意，所需格式元素和可选格式元素，如 TransactionDate 和 CountryCode，在预定义的“格式”数据源组件中看上去不同。
12. 在树中，展开“交易记录 = '$both'”。
    * 请注意，用于定义所导入文件的结构的格式的元素绑定到数据模型的元素。 所导入 CSV 文件的内容将在运行时在现有数据模型中根据这些绑定排序。 请注意 CountryRegion 元素的绑定。 对于未指定国家/地区代码值的传入文件中的任何交易元素，将在数据模型中填充默认国家/地区代码“USA”。
13. 打开“显示详细信息”。
14. 单击“验证”选项卡。
15. 单击“搜索”。
16. 在“查找”字段中，键入“供应商”。
17. 单击“查找下一个”。
    * 此格式映射中可以包含用户定义的逻辑，用于从业务角度验证导入的数据的精确性。 例如，基于此设置，对于导入文件中的任何行（其结构既不与标题行也不与交易记录行一致），将在通知用户此情况的信息日志中生成警告消息，在文件中指示交易记录的序列号。
18. 关闭该页面。

## <a name="run-the-format-mapping"></a>运行格式映射

为了进行测试，请使用以前下载的 1099entriescsv.csv 文件执行格式映射。 生成的输出代表将从所选 CSV 文件导入，并在实际导入时填充到自定义数据模型的数据。

1. 单击“运行”。
    * 单击“浏览”并导航到前面下载的 1099entriescsv.csv 文件。
2. 单击“确定”。
    * 请注意有关不接受的行的警告消息。 行 4 包含以不接受格式表示的收入值，而行 7 不包含使用双引号括住的交易注解文本。
    * 检查 XML 格式的输出，该输出表示已从所选文件导入并移植到数据模型的数据。 请注意，导入的 CSV 文件的所有 7 行都被处理。 包含字段的标题行 1 已跳过，4 个交易已正确分析，2 个交易被识别为无效。
3. 关闭该页面。
4. 关闭该页面。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]