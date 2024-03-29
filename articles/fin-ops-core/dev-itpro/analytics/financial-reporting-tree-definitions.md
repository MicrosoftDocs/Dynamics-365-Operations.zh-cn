---
title: 财务报表中的报告结构树定义
description: 本文介绍报告树定义。 报告树定义是定义组织结构的报表组件。
author: jinniew
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: cf5062cfc7ce47a2356c72462da805e8d0d6a756
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727781"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>财务报表中的报告结构树定义

[!include [banner](../includes/banner.md)]

本文提供了有关报告结构树定义的信息。 报告结构树定义是报表组件或构造基块，可帮助定义组织的结构和层次结构。

财务报告支持灵活报告，以便在您的业务结构发生变化时您可以轻松进行更改。 报表通过不同的组件或构建基块构建。 这些构建基块之一是报告结构树定义。 报告结构树定义帮助定义您组织的结构和层次结构。 这是基于财务数据中的维度关系的跨维层次结构。 它在报告单位级别和摘要级别为结构树中的所有单位提供信息。 可将报告结构树定义与列定义和报表定义组合以创建可由多个公司使用的构建基块组。 为组织结构图中的每个框使用一个报告单位。 一个报告单位可以是财务数据中一个单独的部门，也可以是将其他报告单位的信息组合在一起的较高级别的汇总单位。 对于包含报告结构树的报表定义，为每个报告单位和汇总级别生成一个报表。 除非报表定义指定应使用来自行定义的报告结构树，否则所有这些报表将使用报表定义中指定的行和列定义。 行和列定义是财务报表中的设计和功能的重要组件。 在业务结构发生更改时，报告结构树会增强组件的功能并支持灵活报告。 未基于报告结构树的财务报表仅使用财务报告的部分功能。 您可以使用多个报告结构树定义以及相同行和列定义来以各种方式查看组织的数据。

## <a name="reporting-tree-best-practices"></a>报告结构树最佳实践
在创建报告结构树之前，请考虑以下最佳实践：

- 首先，确定法人或公司所需的报告维度。
- 考虑如何设置结构，然后绘制您公司的组织结构图。 组织结构图将帮助您以直观方式显示如何将报告单位分组到一个或多个报告树中。
- 从最低的可用详细信息级别开始，例如财务数据中定义的部门和项目。 将所需数目的框添加到详细信息级别以显示较高级别的分部或地区。 每个框均表示您创建的任何报告结构树中的一个潜在报告单位。
- 您还必须考虑生成树的最佳方式。 您可以使用自动化的流程来生成报告结构树，也可以手动创建报告结构树。 在您设计树之前，了解这两种方法很重要。
- 您可以使用财务数据系统中定义的报告单位将报告单位添加到报告结构树定义。

## <a name="create-multiple-reporting-trees"></a> 创建多个报告结构树
您可以创建数量不限的报告结构树来以各种方式查看组织的数据。 每个报告树可以包含部门和汇总单位的任意组合。 报表定义一次只能包含一个指向报告结构树的链接。 通过重新安排报告单位的结构，可以创建不同的报告结构树。 然后可以为每个报告结构树使用相同的行和列定义。 以这种方式，您可以快速创建不同的财务报表布局。 如果您创建多个报告结构树，您可以每个月打印一系列财务报表来以各种方式分析和呈现公司的运营。 有关详细信息，请参阅本文结尾的报告单位结构示例。

## <a name="create-a-reporting-tree-definition"></a> 创建报告结构树定义
报告结构树定义包含下表中描述的列。

| 报告结构树列 | 说明 |
|-----------------------|-------------|
| 公司               | 报告单位的公司名称。 **\@ANY** 值（通常只分派给汇总级别）允许将报告树用于所有公司。 所有子分支都会分得一个公司。 |
| 单位名称             | 用于在图形报告结构树中标识此报告单位的代码。 请一定要建立一个一致的而且便于用户理解的唯一编码系统。 |
| 单位描述      | 如果您输入 **UnitDesc** 作为报表定义的 **页眉和页脚** 选项卡上的代码，则报告单位标题将显示在报表页面或页脚中。 如果在行定义的 **描述** 单元格中输入 **UnitDesc**，则标题将显示在报表行描述中。 |
| 维度            | 直接从财务数据中提取信息的报告单位。 它定义帐户和相关细分市场的逻辑定位和长度。 每个报告单位行必须在此列具有维度。 您还可以将维度放置在汇总单位行（例如，与该单位直接有关的费用）。 如果您在汇总单位行中输入维度，则不应在子单位中使用父单位中使用的帐户。 否则，金额可能会出现重复。 |
| 行定义       | 报告单位的行定义的名称。 将对报告树中的每个单位使用相同的行定义。 生成报表时，将对每个报告单位使用此行定义。 行定义可以包括多个财务维度链接。 如果在报告结构树中指定行定义，则选择报表定义的 **报表** 选项卡上的 **使用报告结构树中的行定义** 复选框。 |
| 财务维度链接| 用于报告单位的财务维度链接。 为行定义定义财务维度链接以标识要链接到的财务维度。 |
| 页面选项          | 此列控制在查看或打印报表时是否取消报告单位的详细信息。 |
| 累积百分比              | 应分配给父单位的报告单位的百分比。 在将行中的值添加到父报表之前，您在此列中输入的百分比适用于行定义的每个行。 例如，如果必须在两个部门之间均匀划分子单位，则会先将每个行中的金额乘以 50%，然后再将该值添加到部门报表。 一个报告单位不能具有两个父单位。 要将一个报告单位中的金额分配给两个父单位，可创建另一个具有相同维度的报告单位以累积额外的 50%。 键入完整百分比（不带小数点）。 例如，**25** 表示 25% 分配给父单位。 如果包含小数点 (**.25**)，0.25% 分配给父单位。 要使用小于 1% 的百分比，可使用报表定义中的 **允许累积 &lt;1%** 选项。 此选项位于 **报表设置** 对话框中的 **其他选项** 选项卡上。 从报表定义的 **设置** 选项卡上的 **其他** 按钮访问此对话框。 |
| 单位安全性         | 有关哪些用户和组可访问报告单位的信息的限制。 |
| 附加文本       | 包括在报表中的文本。 |

要创建报告结构树定义，请完成以下步骤。

1. 打开报表设计器。
2. 单击 **文件** &gt; **新建** &gt; **报告结构树定义**。
3. 单击 **编辑**&gt; **从维度插入报告单位**。
4. 在 **从维度插入报告单位** 对话框中，选中要包含在报告结构树中的每个维度的复选框。 **从维度插入报告单位** 对话框包含以下部分。

    | 节                          | 说明 |
    |----------------------------------|-------------|
    | 报告维度细分 | 使用 **拆分科目段** 和 **合并科目段** 按钮可更改科目段的数量和长度。<blockquote>[!NOTE] 您只能合并已拆分的科目段。 要合并多个维度，可在维度值中使用通配符。</blockquote> |
    | 包括/字符位置       | 此部分列出了财务数据中定义的维度并显示为每个维度定义的最长值中的字符数。 选中维度的这个复选框以在报告结构树层次结构中包括该维度。 |
    | 细分层次结构和范围     | 此部分显示维度层次结构。 您可以移动列表中的维度来更改其报告顺序。 在 **起始维度** 和 **结束维度** 字段中，指定每个维度中的值的范围。 如果您不指定一个范围，所有维度值都将插入报告结构树。<blockquote>[!NOTE] 如果您使用了多个维度，结果中将只返回已发布的维度组合。</blockquote> |

    有关显示 **从维度插入报告单位** 对话框示例的图示，请参阅本文后面的“‘从维度插入报告单位’对话框的示例”部分。

5. 要创建其他段（例如，将一个段拆分成两个较短的段），请在 **字符位置** 字段中单击正确的位置，然后单击 **拆分段**。
6. 要将两个段合并为一个段，请单击要合并段的任一段框，然后单击 **合并段**。
7. 层次结构定义维度如何相互报告和每个维度的范围。 要在 **段层次结构和范围** 区域中更改维度的层次结构，请选择要移动的维度，然后单击 **上移** 或 **下移**。
8. 要指定要添加到新报告结构树的维度值的范围，请在 **细分层次结构和范围** 区域中，执行以下步骤：

    1. 在该维度的 **起始维度** 字段中，输入范围中的第一个值。
    2. 在 **结束维度** 字段中，输入范围内的最后一个值。

9. 对于 **段层次结构和范围** 区域中的每个维度，重复步骤 7 和 8。
10. 在定义完将报告单位引入新报告结构树的方式后，单击 **确定**。
11. 单击 **文件** &gt; **保存** 以保存报告结构树。 为报告结构树输入一个唯一的名称和描述，然后单击 **确定**。

### <a name="open-an-existing-reporting-tree-definition"></a>打开现有报告结构树定义

1. 在报表设计器的导航窗格中，单击 **报告结构树定义**。
2. 双击报告结构树列表中的名称以打开报告结构树。
3. 要查看与报告结构树关联的任何构建基块，请右键单击报告结构树定义，然后选择 **关联**。

### <a name="roll-up-data-in-a-reporting-tree"></a>累积报告结构树中的数据

在使用报告结构树时，您可以在父报告单位级别聚合子报告单位中的金额。 此聚合称为累积数据。 以下规则用于将金额累积到报告结构树中的父单位：

- 在报告结构树中，子单位必须包含维度，除非报告结构树是单级别树。 父单位在报表结构树中通常不包含维度。

    > [!NOTE]
    > 如果指定子单位和父单位的维度，可能导致报表中的数据重复。

- 在报告结构树包含维度的报告单位对应于在行和列定义中使用的维度。 维度的组合确定为该单位返回的金额。 例如，在本文稍后的示例 2 中，行 6 和 7 仅分别返回部门 00 和 01 的值。
- 在报告结构树中不包含维度的父报告单位的金额由子单位报表确定，并且将金额累积到指定的父单位。 例如，如果父单位（请参阅累积数据示例 2 中的“Contoso 美国”）具有两个子单位（022 和 023）且不包含维度，则为每个子单位和父单位生成一个报表。 父总计是两个子金额的和。

### <a name="manage-reporting-units"></a>管理报告单位

每个报告结构树定义在唯一视图中显示。 有一个显示父/子层次结构的图形视图和一个显示每个报告单位的特定信息的工作表视图。 图形视图和工作表视图是关联的。 如果在一个视图中选择一个报告单位，则也会在另一个视图中选择此报告单位。 可以根据财务数据中的维度关系来生成跨维层次结构。 在创建报告结构树定义时，可以多次使用相同的行定义，无论您是生成部门收入报表还是合并的汇总收入报表。 在行定义中定义的维度可与报告结构树定义中的维度合并，以提供您组织的绩效的各种视图。

### <a name="reporting-unit-structure"></a> 报告单位结构

在财务报告中使用以下类型的报告单位：

- 详细信息单位直接从财务数据中提取信息。
- 汇总单位将汇总较低级别单位中的数据。

父报告单位是用于聚合详细信息单位中的汇总信息的汇总单位。 汇总单位可以是详细信息单元和汇总单位。 因此，汇总单位可以从较低级别单位或财务数据中提取信息。 父单位可以是较高级的父单位的子单位。 子报告单位可以是直接从财务数据中提取信息的详细信息单位。 子报告单位还可以是中间汇总单位。 换句话说，它可以是较低级单位的上级单位，也可以是较高级汇总单位的子单位。 报告单位的最常见方案中，父单位在 **维度** 列中具有空的单元格，且子单位具有指向特定的或通配符维度组合的链接。

### <a name="organize-reporting-units"></a> 组织报告单位

通过移动图形视图中的报告单位，你可以重新排列报告树定义的组织结构。 您还可以在报告结构树中将报告单位提升到更高的级别，或将其降到更低级别。

1. 在报表设计器中，打开要修改的报告结构树定义。
2. 在报告结构树定义的图形视图中，选择一个报告单位。
3. 将单位拖动到新位置。 或者，右键单击单位并选择 **升级报告单位** 或 **降级报告单位**。
4. 单击 **文件** &gt; **保存** 以保存您的更改。

### <a name="add-text-about-a-reporting-unit"></a> 添加有关报告单位的文本

附加的文本条目为静态文本字符串（最多 255 个字符），该字符串将信息添加到报告结构树定义。 例如，附加的文本可以是简短的公司描述。 可在报告结构树定义中为每个报告单位创建最多 10 个附加文本条目。 附加文本显示在将文本分配到的报告单位的报表中。 可以添加来自行定义的 **描述** 列和报表定义中的 **页眉和页脚** 选项卡的文本条目。

1. 在报表设计器中，打开要修改的报告结构树定义。
2. 双击报告单位行的 **附加文本** 单元格。
3. 在 **附加文本** 对话框的第一个空白行中，输入文本。 第一个包含文本的行被视作 UnitText1，无论其在 **附加文本** 对话框中的位置如何。
4. 要为此报告单位添加更多文本条目，请在空白行中输入文本。
5. 单击 **OK**。

### <a name="remove-additional-text-from-a-reporting-unit"></a>从报告单位中删除附加文本

1. 在报表设计器中，打开要修改的报告树定义。
2. 双击报告单位行的 **附加文本** 单元格。
3. 在 **附加文本** 对话框中，选择要删除的条目，然后单击 **清除**。 或右键单击该条目，然后选择 **剪切**。
4. 单击 **OK**。

### <a name="restrict-access-to-a-reporting-unit"></a>限制对报告单位的访问

您可以阻止某些用户和组访问报告单位， 您还可以定义限制，使其适用于报告单位的子报告单位。

1. 在报表设计器中，打开要修改的报告结构树定义。
2. 双击要限制对其的访问权的报告单位行的 **单位安全性** 单元格。
3. 在 **单位安全性** 对话框中，单击 **用户和组**。
4. 选择应有权访问报告单位的用户或组，然后单击 **确定**。
5. 要限制对子报告单位的访问，请选中 **向子报告单位添加安全性** 复选框。
6. 单击 **OK**。

### <a name="remove-access-to-a-reporting-unit"></a>取消对报告单位的访问权

1. 在报表设计器中，打开要修改的报告结构树定义。
2. 双击要取消其访问权的报告单位行的 **单位安全性** 单元格。
3. 在 **单位安全性** 对话框中，选择一个名称，然后单击 **删除**。
4. 单击 **确定**。

## <a name="examples"></a>示例
### <a name="reporting-unit-structure--example-1"></a>报告单位结构 – 示例 1

此处是以下报告结构树中的报告单位：

- Contoso 日本报告单位是 Contoso 日本销售和 Contoso 日本咨询子单位的父单位。
- Contoso 日本分部单位既是Contoso 日本单位的子单位，又是 Home Sales 和 Auto Sales 单位的父单位。
- 最低级别的详细信息报告单位（Home Sales、Auto Sales、Client Services 和 Operations）代表财务数据中的部门。 这些报告单位在图中的阴影区域中。
- 更高级别的汇总单位汇总了详细信息单位中的信息。

[![Contoso 汇总报表结构 - 示例 1。](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>报告单位结构 – 示例 2

在下图中，报告结构树具有按业务职能划分的组织结构树。

[![Contoso 汇总报表结构 - 示例 2。](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>“从维度插入报告单位”对话框的示例

下图显示了 **从维度插入报告单位** 对话框的示例。 在本示例中，结果将返回业务单位、成本中心和部门的组合。

[![插入报告单位。](./media/insertreportingunits.png)](./media/insertreportingunits.png)

结果报告结构树定义按业务单位排序，然后按成本中心，再然后按部门。 第五个报告单位的维度是 **业务单位 = \[001\]、成本中心 =\[\]、部门 = \[022\]**，标识特定于业务单位 001 和部门 022 的帐户的报告单位。

[![报告树的图示。](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>数据累积的示例

以下示例显示了可能在报告结构树定义中为累积的数据使用的信息。

#### <a name="example-1"></a>示例 1

[![多公司累积。](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>示例 2

[![跨公司部门累积。](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>其他资源

[财务报告](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
