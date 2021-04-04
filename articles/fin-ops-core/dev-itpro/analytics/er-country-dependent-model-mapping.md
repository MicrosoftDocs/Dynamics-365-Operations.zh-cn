---
title: 配置依赖于国家/地区上下文的 ER 模型映射
description: 本主题说明如何设置 ER 模型映射，以使其依赖于控制其使用的法人的国家/地区上下文。
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 48d2e3c81d038cc55f6f100f3081561506946199
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562278"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>配置依赖于国家/地区上下文的 ER 模型映射

[!include[banner](../includes/banner.md)]

您可以配置电子报告 (ER) 模型映射，以便它们实现通用的 ER 数据模型，但特定于 Dynamics 365 Finance。 本主题说明如何为 ER 数据模型设计多个 ER 模型映射，以控制来自具有不同国家/地区上下文的公司的相应 ER 格式如何使用它们。

## <a name="prerequisites"></a>先决条件

要完成本主题中的示例，您必须具有以下访问权限：

- 访问 Finance 的以下其中一个角色：
    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

- 对于下列角色之一，已为与 Finance 相同的租户配置的 Regulatory Configuration Services (RCS) 的实例：
    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

本主题中的某些步骤需要执行 ER 格式。 在某些情况下，ER 格式的执行会受到您当前登录的公司所在的国家地区上下文的影响。 如果具有所需国家/地区上下文的公司在 RCS 中可用，则可以在当前 RCS 实例中运行 ER 格式。 否则，您必须将使用 ER 数据模型的 ER 模型映射和 ER 格式配置的已完成版本上载到 Finance 实例，然后在该 Finance 实例中运行 ER 格式。 有关如何将 RCS 中驻留的配置导入到 Finance 实例中的信息，请参阅[从 RCS 导入配置](rcs-download-configurations.md)。

## <a name="single-model-mapping-case"></a>单个模型映射案例

请按照本主题的[附录 1](#appendix1) 中的步骤设计所需的 ER 组件。 现在，您具有 **映射(一般)** 模型映射配置，其中包含 **入口点 1** 定义的模型映射。

![ER 配置页](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>运行配置的格式

1.  在 **配置页** 的 **版本** 快速选项卡上，选择 **运行**。
2.  选择 **确定**。

请注意，Web 浏览器提供了下载由执行的 ER 格式生成的文本文件的功能。 因为此格式已配置为使用 **入口点 1** 定义，并且当前仅单个模型映射可用于包含此定义的映射的基本模型，所以执行的 ER 格式使用 **映射(一般)** 配置的 **映射(一般)** 模型映射作为数据源。 因此，下载的文件包含 **通用功能 1** 文本。

## <a name="multiple-shared-model-mappings-case"></a>多个共享模型映射案例

请按照本主题的[附录 2](#appendix2) 中的步骤设计所需的 ER 组件。 现在，您具有 **映射(一般)** 和 **映射(一般)自定义** 模型映射配置，每个配置都包含 **入口点 1** 定义的模型映射。

![ER 配置页](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>运行配置的格式

1.  在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。
2.  在 **版本** 快速选项卡上，选择 **运行**。
3.  选择 **确定**。

请注意，所选 ER 格式的执行将不成功。 一条错误消息通知您，**映射(一般)** 和 **映射(一般)自定义** 模型映射配置中的 **用于了解映射的模型** 模型和 **入口点 1** 定义存在多个模型映射。 此消息还建议您选择这些配置之一作为默认配置。

![ER 配置页](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>定义默认映射配置

请按照以下步骤将 **映射(一般)自定义** 模型映射配置定义为默认配置，以便其映射可用作 **用于了解映射的格式** ER 格式的数据源。

1.  在 **配置** 页上的配置树中，选择 **映射(一般)自定义**。
2.  根据需要，选择 **编辑** 以使当前页面可供编辑。
3.  将 **模型映射的默认值** 选项设置为 **是**。
4.  选择 **保存**。

![ER 配置页](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>运行配置的格式

1.  在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。
2.  在 **版本** 快速选项卡上，选择 **运行**。
3.  选择 **确定**。

请注意，所选 ER 格式的执行将成功。 Web 浏览器提供了下载由执行的 ER 格式生成的文本文件的功能。 由于此格式已配置为使用 **入口点 1** 定义，并且选择了 **映射(一般)自定义** 模型映射配置作为默认配置，因此执行的 ER 格式使用了 **映射(一般)自定义** 配置的 **映射(一般)复制** 模型映射作为数据源。 因此，下载的文件包含 **通用功能 1 自定义** 文本。

> [!NOTE]
> 如果您更改当前登录的公司并再次运行此 ER 格式，则在生成的文件中将获得相同的内容，因为默认的 ER 模型映射配置不包含任何依赖于公司的限制。

## <a name="multiple-mixed-model-mappings-case"></a>多个混合模型映射案例

请按照本主题的[附录 3](#appendix3) 中的步骤设计所需的 ER 组件。 您现在具有 **映射(一般)**、**映射(一般)自定义** 和 **映射(FR)模型映射** 配置，其包含 **入口点 1** 定义的模型映射。

请注意，已配置 **映射(FR)** 模型映射配置的版本 1，使其仅应用于在具有法国国家/地区上下文的 Finance 公司中运行的 **用于了解映射的模型** 模型的格式。

![ER 配置页](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>运行配置的格式

1.  将公司更改为 **FRSI**。
2.  在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。
3.  在 **版本** 快速选项卡上，选择 **运行**。
4.  选择 **确定**。

请注意，所选 ER 格式的执行将成功。 Web 浏览器提供了下载由执行的 ER 格式生成的文本文件的功能。 由于此格式已配置为使用 **入口点 1** 定义，并且选择了 **映射(一般)自定义** 模型映射配置作为默认配置，因此执行的 ER 格式使用了 **映射(一般)自定义** 配置的 **映射(一般)复制** 模型映射作为数据源。 因此，下载的文件包含 **通用功能 1 自定义** 文本。

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>将特定于法国的映射配置定义为默认配置

请按照以下步骤将自定义 **映射(FR)** 模型映射配置定义为默认配置。 请注意，由于此映射特定于法国，因此将被视为所有在 **ISO 国家/地区代码** 字段中指定了 **FR** 国家/地区代码的模型映射配置之间的默认映射。

1.  在 **配置** 页上的配置树中，选择 **映射(FR)**。
2.  根据需要，选择 **编辑** 以使当前页面可供编辑。
3.  将 **模型映射的默认值** 选项设置为 **是**。
4.  选择 **保存**。

![ER 配置页](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>运行配置的格式

1.  在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。
2.  在 **版本** 快速选项卡上，选择 **运行**。
3.  选择 **确定**。

请注意，所选 ER 格式的执行将成功。 Web 浏览器提供了下载由执行的 ER 格式生成的文本文件的功能。 由于此格式已配置为使用 **入口点 1** 定义，并且选择了 **映射(FR)** 模型映射配置作为默认配置，因此执行的 ER 格式使用了 **映射(FR)** 配置的 **映射(FR)** 模型映射作为数据源。 因此，下载的文件包含 **FR 功能 1** 文本。

> [!NOTE]
> 如果您更改当前登录的公司并再次运行此 ER 格式，则输出将依赖于所选公司的国家/地区上下文。

## <a name="other-model-mapping-cases"></a>其他模型映射案例

如您所见，选择用于执行 ER 格式的模型映射的工作方式如下：

- 指定 ER 格式使用的模型映射定义（本主题示例中的 **入口点 1**）。
- 包含具有指定定义的映射并且满足已配置的任何国家/地区上下文限制的所有映射配置，都可能能够用于运行 ER 格式（本主题示例中的 **映射(一般)**、**映射(一般)自定义** 和 **映射(FR)**）。
- 具有国家/地区上下文限制的任何默认模型映射都具有最高的选择优先级（本主题示例中的 **映射(FR)**）。
- 没有国家/地区上下文限制的任何默认模型映射都具有更高的选择优先级（本主题示例中的 **映射(一般)自定义**）。
- 具有国家/地区上下文限制的任何模型映射都比没有国家/地区上下文限制的模型映射具有更高的选择优先级。

下表提供了有关模型映射设置的所有可能案例的模型映射选择结果的信息：

- 第 1 列指示是否显示没有国家/地区上下文限制的第一个模型映射（例如，共享的 **映射(一般)** 映射），如果显示，则指示其 **模型映射的默认值** 选项是否设置为 **是**。
- 第 2 列指示是否显示没有国家/地区上下文限制的第二个模型映射（例如，共享的 **映射(一般)自定义** 映射），如果显示，则指示其 **模型映射的默认值** 选项是否设置为 **是**。
- 第 3 列指示是否显示具有国家/地区 A 上下文限制的第一个模型映射（例如，特定于法国的 **映射(FR)** 映射），如果显示，则指示其 **模型映射的默认值** 选项是否设置为 **是**。
- 第 4 列指示是否显示具有国家/地区 A 上下文限制的第二个模型映射，如果显示，则指示其 **模型映射的默认值** 选项是否设置为 **是**。
- 第 5 列显示在具有国家/地区 A 上下文的公司的控制下执行 ER 格式的模型映射选择的结果。
- 第 6 列显示在具有国家/地区 B 上下文的公司的控制下执行 ER 格式的模型映射选择的结果。

在表中，加号 (+) 表示用于运行 ER 格式（Finance 或 RCS）的 Microsoft Azure 服务的当前实例中是否存在模型映射配置。

| 包装箱 | 没有国家/地区上下文的模型映射 1 (MM1) | 没有国家/地区上下文的模型映射 2 (MM2) | 具有国家/地区 A 上下文的模型映射 1 (MM1A) | 具有国家/地区 A 上下文的模型映射 2 (MM2A) | 在具有国家/地区 A 上下文的公司的控制下运行 | 在具有国家/地区 B 上下文的公司的控制下运行 |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | 错误（缺少映射）   | 错误（缺少映射）    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | 错误（多个映射） | 错误（多个映射）  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | 错误（多个映射） | MM1                        |
|     6   |     +   | 默认 |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | 默认 |         | MM1A                      | MM1                        |
|     8   |     +   |         | 默认 |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | 默认 | 默认 | 错误（多个映射） | MM1                        |
|    10   | 默认 |         |         |         | MM1                       | MM1                        |
|    11   | 默认 |    +    |         |         | MM1                       | MM1                        |
|    12   | 默认 |         |    +    |         | MM1                       | MM1                        |
|    13   | 默认 | 默认 |         |         | 错误（多个映射） | 错误（多个映射）  |
|    14   | 默认 |         | 默认 |         | MM1A                      | MM1                        |
|    15   | 默认 |         | 默认 | 默认 | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | 默认 | 默认 | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>了解在执行 ER 格式时使用了什么映射

### <a name="configure-er-user-parameters"></a>配置 ER 用户参数

1.  在 **配置** 页操作窗格中的 **配置** 选项卡上，选择 **用户参数**。
2.  将 **以调试模式运行** 选项设置为 **是**。
4.  选择 **确定**。

### <a name="run-the-configured-format"></a>运行配置的格式

1.  在 **配置** 页上的配置树中，选择 **用于了解映射的格式**。
2.  在 **版本** 快速选项卡上，选择 **运行**。
3.  选择 **确定**。

### <a name="review-the-er-debug-log"></a>查看 ER 调试日志

1.  在导航窗格中，转到 **模块 \> 组织管理 \> 电子报告 \> 配置调试日志**。
2.  选择 **重新加载此页面** 按钮。

![ER 运行日志页](./media/RCS-Context-specific-mapping-DebugLog.PNG)

请注意，已为执行的 ER 格式将新记录添加到 ER 调试日志中。 由于此记录的 **级别** 字段设置为 **信息**，因此此记录是信息性的。 由于格式组件字段设置为 **映射配置**，因此记录会通知您有关执行 **用于了解映射的格式** ER 格式（已在 **配置名称** 字段中选择）期间使用的模型映射的信息。 **生成的文本** 字段的内容会通知您，位于 **映射(FR)** 配置中的 **映射(FR)** 映射组件已用于运行此报表。

## <a name="appendix-1"></a><a name="appendix1"></a> 附录 1

### <a name="configure-a-sample-data-model"></a>配置示例数据模型

登录您的 RCS 实例。

在此示例中，将为示例公司 Litware 公司创建一个配置。要完成这些步骤，您必须首先在 RCS 中完成[创建一个配置提供程序，并标记其为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程中的步骤。

#### <a name="create-an-er-data-model-configuration"></a>创建 ER 数据模型配置

1.  在默认仪表板中，选择 **电子申报**。
2.  选择 **报告配置** 磁贴。
3.  在 **配置** 页上，选择 **创建配置**。
4.  在下拉对话框的 **名称** 字段中，输入 **用于了解映射的模型**。
5.  选择 **创建配置**。
6.  选择 **配置组件** 快速选项卡。

请注意，此 ER 配置的草稿版本 1 已可以进行编辑。 此版本包含数据模型组件。

#### <a name="design-a-sample-data-model"></a>设计示例数据模型

1.  在 **配置页** 上，选择 **设计器**。
2.  选择 **新建**。
3.  在下拉对话框的 **名称** 字段中，输入 **入口点 1**。
4.  选择 **添加**。
5.  选择 **新建**。
6.  在下拉对话框的 **名称** 字段中，输入 **功能描述**。
7.  选择 **添加**。
8.  选择 **新建**。
9.  在下拉对话框的 **新建节点** 字段组中，选择 **模型根**。
10. 在 **名称** 字段中，输入 **入口点 2**。
11. 选择 **入口点 2**。
12. 选择 **添加**。
13. 选择 **新建**。
14. 在下拉对话框的 **名称** 字段中，输入 **功能描述**。
15. 选择 **添加**。

    ![ER 数据模型设计器页面](./media/RCS-Context-specific-mapping-Model.PNG)

16. 选择 **保存**。
17. 关闭该页面。

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>完成修改后的模型配置版本

1.  在 **配置** 页的 **版本** 快速选项卡上，选择 **更改状态**。

    > 将设计的模型配置的状态从 **草稿** 更改为 **已完成**，以便可以将其用于设计所需的模型映射和格式。

2.  选择 **完成**。
3.  选择 **确定**。

请注意已创建的配置保存为已完成版本 1。

### <a name="configure-a-sample-model-mapping"></a>配置示例模型映射

#### <a name="create-an-er-model-mapping-configuration"></a>创建 ER 模型映射配置

1.  在 **配置** 页上，选择 **创建配置**。
2.  在下拉对话框中的 **新建** 字段组中，选择 **用于了解映射的基于数据模型的模型映射**。
3.  在 **名称** 字段中，输入 **映射(一般)**。
4.  在 **数据模型定义** 字段中，选择 **入口点 1**。
5.  选择 **创建配置**。

请注意，此 ER 配置的草稿版本 1 已可以进行编辑。 此版本包含模型映射组件。

#### <a name="design-a-sample-model-mapping"></a>设计示例模型映射

1.  在 **配置** 页上，选择 **设计器**。

    请注意，对于 **入口点 1** 定义，**目标模型** 方向类型的模型映射已自动添加到此组件。
    
2.  选择 **设计器** 开始编辑添加的模型映射。
3.  在 **数据模型** 部分，选择 **编辑**。
4.  在 **公式** 字段中，输入 **通用功能 1**。
5.  选择 **保存**。
6.  关闭 **公式设计器** 页。

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  选择 **保存**。
8.  关闭 **模型映射设计器** 页。
9.  选择 **新建**。
10. 在 **定义** 字段中，选择 **入口点 2**。
11. 在 **名称** 字段中，输入 **映射(一般) 2**。
12. 选择 **设计器**。
13. 在 **数据模型** 部分，选择 **编辑**。
14. 在 **公式** 字段中，输入 **通用功能 2**。
15. 选择 **保存**。
16. 关闭 **公式设计器** 页。

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. 选择 **保存**。
18. 关闭 **模型映射设计器** 页。

    ![ER 模型映射页](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. 关闭 **模型映射** 页。

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>完成修改后的模型映射配置版本

1.  在 **配置页** 的 **版本** 快速选项卡上，选择 **更改状态**。

    > 将设计的模型映射配置的状态从 **草稿** 更改为 **已完成**，以便可以将其用于 ER 格式。

2.  选择 **完成**。
3.  选择 **确定**。

请注意已创建的配置保存为已完成版本 1。

### <a name="configure-a-sample-format"></a>配置示例格式

#### <a name="create-an-er-format-configuration"></a>创建 ER 格式配置

1.  在 **配置** 页上的配置树中，选择 **用于了解映射的模型**。
2.  选择 **创建配置**。
3.  在下拉对话框中的 **新建** 字段组中，选择 **用于了解映射的基于数据模型的格式**。
4.  在 **名称** 字段中，输入 **用于了解映射的格式**。
5.  在 **数据模型定义** 字段中，选择 **入口点 1**。
6.  选择 **创建配置**。

请注意，此 ER 配置的草稿版本 1 已可以进行编辑。 此版本包含格式组件。

#### <a name="design-a-sample-format"></a>设计示例格式

1.  在 **配置** 页上，选择 **设计器**。
2.  选择 **添加根**。
3.  在 **文本** 组中，选择 **字符串** 项。
4.  选择 **确定**。

#### <a name="bind-format-elements-to-a-data-source"></a>将格式元素绑定到数据源

1.  在 **格式设计器** 页上的 **映射** 选项卡上，展开模型数据源。
2.  选择 **功能描述** 字段。
3.  选择 **绑定**。

    ![ER 格式设计器页面](./media/RCS-Context-specific-mapping-Format.PNG)

4.  选择 **保存**。
5.  关闭该页面。

## <a name="appendix-2"></a><a name="appendix2"></a> 附录 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>配置示例模型映射以进行一般自定义

您可能想要自定义配置提供商（合作伙伴）提供给您的模型映射，然后将自定义版本用作 ER 格式的数据源。 在这种情况下，您必须创建自定义 ER 模型映射配置，以在现有模型映射中进行所需的更改。 此附录中的过程以 **映射(一般)** 模型映射为例。

#### <a name="create-an-er-model-mapping-configuration"></a>创建 ER 模型映射配置

1.  在 **配置** 页上的配置树中，选择 **映射(一般)**。
2.  选择 **创建配置**。
3.  在下拉对话框的 **新建** 字段组中，选择 **从以下名称派生: 映射(一般)，Litware, Inc.**。
4.  在 **名称** 字段中，输入 **映射(一般)自定义**。
5.  选择 **创建配置**。

请注意，此 ER 配置的草稿版本 1 已可以进行编辑。

#### <a name="design-a-sample-model-mapping"></a>设计示例模型映射

1.  在 **配置** 页上，选择 **设计器**。

    > 请注意，基本配置的模型映射已自动复制到此配置。

2.  选择 **映射(一般)复制** 映射。
3.  选择 **设计器**。
4.  在 **数据模型** 部分，选择 **编辑**。
5.  在 **公式** 字段中，输入 **通用功能 1 自定义**。
6.  选择 **保存**。
7.  关闭该页面。

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  选择 **保存**。
9.  关闭该页面。
10. 选择 **映射(一般) 2 复制** 映射。
11. 选择 **设计器**。
12. 在 **数据模型** 部分，选择 **编辑**。
13. 在 **公式** 字段中，输入 **通用功能 2 自定义**。
14. 选择 **保存**。
15. 关闭该页面。

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. 选择 **保存**。
17. 关闭该页面。

    ![ER 模型映射页](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. 关闭该页面。

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>完成修改后的模型映射配置版本

1.  在 **配置** 页的 **版本** 快速选项卡上，选择 **更改状态**。

    > 将设计的模型映射配置的状态从 **草稿** 更改为 **已完成**，以便可以将其用于 ER 格式。

2.  选择 **完成**。
3.  选择 **确定**。

请注意已创建的配置保存为已完成版本 1。

## <a name="appendix-3"></a><a name="appendix3"></a> 附录 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>配置示例模型映射以进行国家/地区特定自定义

对于某些 ER 格式，可能需要针对国家/地区进行数据准备。 在这种情况下，您可以管理单独的 ER 模型映射配置，并将这些特定于国家/地区要求的实现与常规实现隔离开来。 此附录中的过程以 **用于了解映射的格式** ER 格式和特定于法国的要求为例。

#### <a name="create-an-er-model-mapping-configuration"></a>创建 ER 模型映射配置

首先，创建新的 ER 模型映射配置，以实现国家/地区的特定要求。 使用您的自定义 ER 模型映射配置作为基础。

1.  在 **配置** 页上的配置树中，选择 **映射(一般)自定义**。
2.  选择 **创建配置**。
3.  在下拉对话框的 **新建** 字段组中，选择 **从以下名称派生: 映射(一般)自定义，Litware, Inc.**。
4.  在 **名称** 字段中，输入 **映射(FR)**。
5.  选择 **创建配置**。

请注意，此 ER 配置的草稿版本 1 已可以进行编辑。

#### <a name="design-a-sample-model-mapping"></a>设计示例模型映射

1.  在 **配置** 页上，选择 **设计器**。

    > 请注意，基本配置的模型映射已自动复制到此配置。

2.  选择 **映射(一般)复制** 映射。
3.  将其重命名为 **映射(FR)**。
4.  选择 **设计器**。
5.  在 **数据模型** 部分，选择 **编辑**。
6.  在 **公式** 字段中，输入 **FR 功能 1**。
7.  选择 **保存**。
8.  关闭该页面。

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  选择 **保存**。
10. 关闭该页面。
11. 选择 **映射(一般) 2 复制** 映射。
12. 将其重命名为 **映射(FR) 2**。
13. 选择 **设计器**。
14. 在 **数据模型** 部分，选择 **编辑**。
15. 在 **公式** 字段中，输入 **FR 功能 2**。
16. 选择 **保存**。
17. 关闭该页面。

    ![ER 模型映射设计器页面](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. 选择 **保存**。
19. 关闭该页面。

    ![ER 模型映射页](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. 关闭该页面。

#### <a name="specify-countryregion-context-restrictions-for-use"></a>指定要使用的国家/地区上下文限制

1.  在 **配置** 页的 **ISO 国家/地区代码** 快速选项卡上，选择 **新建**。
2.  在 **ISO** 字段中，选择 **FR**。
3.  选择 **保存**。

请注意，您必须登录 Finance 中的特定公司才能运行 ER 格式。 因此，此公司可以被视为同时控制基本 ER 数据模型的 ER 格式执行和正确 ER 模型映射选择的一方。 通过添加 **FR** 国家/地区代码，您可以指定仅当在具有法国国家/地区上下文的公司的控制下运行基本数据模型的 ER 格式时，此模型映射才可供选择。

您可以为单个版本的 ER 模型映射配置添加多个国家/地区代码。 这样，可以将驻留在该模型映射配置中的模型映射用于在具有不同国家/地区上下文的公司控制下运行的 ER 格式。

请注意，国家/地区代码列表是为 ER 模型映射配置的每个版本指定的，可能因版本而异。

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>完成修改后的模型映射配置版本

1.  在 **配置** 页的 **版本** 快速选项卡上，选择 **更改状态**。

    > 将设计的模型映射配置的状态从 **草稿** 更改为 **已完成**，以便可以将其用于 ER 格式。

2.  选择 **完成**。
3.  选择 **确定**。

请注意已创建的配置保存为已完成版本 1。

## <a name="additional-resources"></a>其他资源

[电子申报 (ER) 概览](general-electronic-reporting.md)

[管理单独电子报告配置中的电子报告模型映射](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[应用国家/地区上下文](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>常见问题

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>我在 RCS 中配置了两个共享 ER 模型映射配置，并将其中一个标记为默认模型映射配置。 我成功运行了为相同的基本 ER 数据模型配置创建的 ER 格式，以测试模型映射。 然后，我将整个 ER 解决方案（ER 数据模型、两个 ER 模型映射配置和 ER 格式配置）导入了 Finance。 当我尝试在 Finance 中运行相同的 ER 格式时，为什么会收到错误消息？
默认的模型映射设置是特定于环境的。 它是在 RCS 中配置的，但没有导出到 Finance。 要成功运行此 ER 格式，您还必须在 Finance 中将其中一个 ER 模型映射配置标记为默认模型映射配置。

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>我将一个模型映射配置为共享模型映射，并完成了其草稿版本。 然后，我为相同的数据模型添加了新的模型映射配置，并将其配置为特定于法国。 为什么即使我运行的 ER 格式使用正确的根定义并且在具有法国国家/地区上下文的公司控制下进行执行，在运行此 ER 格式时仍然选择了共享模型映射？
请确保未将共享模型映射配置标记为默认模型映射配置。 否则，它将在映射选择期间具有更高的优先级。 另外，在 ER 格式执行期间选择映射时，还请确保考虑了特定于法国的模型映射配置。 仅当满足以下条件中的至少一项时，才可以选择 ER 模型映射配置：
- 至少一个版本的 ER 模型映射配置具有 **已完成** 或 **共享** 状态。 在这种情况下，具有最高版本号的版本将用于 ER 格式执行。
- ER 模型映射配置的 **运行草稿** 选项已打开。 在这种情况下，**草稿** 状态的版本将用于 ER 格式执行。
> 打开 **运行设置** ER 用户参数后，每个 ER 模型映射配置的 **运行草稿** 选项在 **配置** 页面上将可用。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]