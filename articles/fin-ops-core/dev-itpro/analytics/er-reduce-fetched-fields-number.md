---
title: 通过减少运行时获取的表字段的数量来提高 ER 解决方案的性能
description: 本文说明如何通过减少运行时获取的表字段的数量来帮助提高 ER 解决方案的性能。
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: eb76c415da87d421b8135a93b84f4e905f01e70d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847442"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>通过减少运行时获取的表字段的数量来提高 ER 解决方案的性能

[!include[banner](../includes/banner.md)]

可以设计[电子申报](general-electronic-reporting.md) (ER) [格式](er-overview-components.md#format-components-for-outgoing-electronic-documents)以生成各种格式的传出单据。 生成单据时，ER 格式调用在相应 ER [模型映射](er-overview-components.md#model-mapping-component)中配置的数据源。 若要配置对申请表、查询或实体的访问以检索记录，可使用 *表记录* 类型的 ER 数据源。 默认情况下，*表记录* 类型的数据源将检索所请求记录中所有字段的值。 但是，您可以配置这种类型的数据源，使其仅获取运行 ER 格式所需的字段值。 此配置有助于减少执行数据检索和进一步记录缓存的应用程序服务器的内存消耗。

要详细了解如何限制 *表记录* 类型的数据源的提取字段列表，请完成本文中的示例。

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>示例：减少运行时提取的表字段数

以下过程显示系统管理员或电子报告开发人员角色的用户如何配置 ER 模型映射，使其仅获取运行 ER 格式所需的字段，以帮助减少应用程序服务器内存的消耗。

这些程序可以在 Microsoft Dynamics 365 Finance 中的 **USMF** 公司中完成。 无需进行编码。

若要完成本示例，您必须能够用以下角色之一访问 **USMF** 公司：

- 电子报告功能顾问
- 系统管理员

在此示例中，将使用为示例公司 **Litware, Inc.** 提供的 ER [配置](general-electronic-reporting.md#Configuration)。 确保为 ER 框架列出了 **Litware, Inc.** (`http://www.litware.com`) 示例公司的配置提供程序，并且它被标记为 **活动**。 如果未列出此配置提供程序，或者未将其标记为 **活动** 状态，请按照[创建一个配置提供程序，并标记其为活动状态](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤操作。

### <a name="configure-the-er-framework"></a>配置 ER 框架

按照[配置电子报告框架](er-quick-start2-customize-report.md#ConfigureFramework)中的步骤设置最低限度的电子报告参数集。 在开始使用 ER 框架修改提供的 ER 解决方案的数据源之前，您必须完成此设置。

### <a name="import-the-sample-er-configurations"></a>导入示例 ER 配置

如果您尚未完成[设计新的 ER 解决方案以打印自定义报告](er-quick-start1-new-solution.md)一文中的示例，请下载并在本地存储 XML 文件，以获取所提供的 ER 解决方案的以下配置。

| 内容描述            | 文件名 |
|--------------------------------|-----------|
| ER 数据模型配置    | [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| ER 模型映射配置 | [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER 格式配置        | [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

然后按照以下步骤将提供的 ER 解决方案的配置上传到您的 Finance 实例。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 选择 **申报配置**。
3. 在 **配置** 页面上，导入 ER 数据模型配置。

    1. 选择 **交换**，然后选择 **从 XML 文件加载**。
    2. 选择 **浏览**，找到并选择 **Questionnaires model.version.1.xml** 文件，然后选择 **确定**。

4. 导入 ER 模型映射配置。

    1. 选择 **交换**，然后选择 **从 XML 文件加载**。
    2. 选择 **浏览**，找到并选择 **Questionnaires mapping.1.1.xml** 文件，然后选择 **确定**。

5. 导入 ER 格式配置。

    1. 选择 **交换**，然后选择 **从 XML 文件加载**。
    2. 选择 **浏览**，找到并选择 **Questionnaires format.1.1.xml** 文件，然后选择 **确定**。

6. 在配置树中，展开 **调查表模型**。
7. 在配置树中查看导入的 ER 配置的列表。

    ![在“配置”页面上查看导入的 ER 配置列表。](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>查看提供的 ER 模型映射

1. 在 **配置** 页上，选择 **调查表映射**。
2. 在操作窗格上，选择 **设计器**。
3. 在 **模型到数据源映射** 页面上，选择 **设计器**。
4. 在 **模型映射设计器** 页面的操作窗格上，选择 **组视图** 以打开 **组** 视图。
5. 在 **数据模型** 窗格中，展开 **调查表**。

    请注意，**调查表** 数据源已配置为访问 `KMCollection` 应用程序表。

6. 在 **数据源** 窗格中，展开 **表记录** \> **调查表** \> **字段**。

    请注意 `KMCollection` 应用程序表中有多少个字段被 *表记录* 类型的 **调查表** 数据源公开。

    ![打开组视图时，在模型映射设计器页面上查看提供的模型映射。](./media/er-reduce-fetched-fields-number-mapping1.png)

7. 在操作窗格上，再次选择 **组视图** 以关闭 **组** 视图，然后选择 **全部显示** \> **只显示映射的**。

    请注意，`KMCollection` 应用程序表的几个字段用于填写 ER 数据模型中的 **调查表** 记录列表：

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![关闭组视图时，在模型映射设计器页面上查看提供的模型映射。](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>开启 ER 性能跟踪

执行[开启 ER 性能跟踪](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace)中的步骤，设置 ER 用户参数，以允许跟踪 ER 组件的执行情况。

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>使用提供的模型映射运行提供的 ER 格式

执行 [从 ER 运行设计的格式](er-quick-start1-new-solution.md#RunFormatFromER)中的步骤，从 **配置** 页面运行为单个调查表提供的 ER 格式。

### <a name="review-the-execution-trace-of-the-first-run"></a>检查首次运行的执行跟踪

1. 转到 **组织管理** \> **电子申报 \> 配置**。
2. 在 **配置** 页面上，展开 **调查表模型**，并选择 **调查表映射**。

    > [!NOTE]
    > **版本** 快速选项卡上的详细信息指明您选择了 **调查表映射** 配置的草稿版本。 因此，您可以修改此模型映射的内容。

3. 在操作窗格上，选择 **设计器**。
4. 在 **模型到数据源映射** 页面上，选择 **设计器**。
5. 在 **模型映射设计器** 页的操作窗格上，选择 **性能跟踪**。
6. 在 **性能跟踪结果设置** 对话框中，选择上次格式运行期间生成的跟踪。

    ![在“性能跟踪结果设置”对话框中选择跟踪。](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. 选择 **确定**。 
8. 在 **详细信息** 快速选项卡上，筛选指向 **调查表** 数据源的 **调查表** 路径。
9. 查看调用 **调查表** 数据源时生成的数据库查询的详细信息。

    请注意，调用 **调查表** 数据源时，已在运行时提取 `KMCollection` 应用程序表的所有字段。

    ![查看“模型映射设计器”页面上的数据库查询的详细信息。](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>修改提供的 ER 模型映射

1. 在 **模型映射设计器** 页上的 **数据源** 窗格中，选择 **调查表** 数据源。
2. 在 **数据源** 窗格中，选择 **编辑**。
3. 在 **数据源属性** 对话框中，选择 **选择字段** 以指定引用的 `KMCollection` 应用程序表的字段列表，如果调用了可编辑的 **调查表** 数据源，则将在运行时提取这些字段。

    ![在“数据源属性”对话框中选择“选择字段”以开始配置将使用可编辑数据源从应用程序表中提取的字段列表。](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. 在 **选择字段** 页面上，选择 **自动填充**。

    根据模型映射的预配置伪像自动填写 **所选字段** 列表。 模型映射的任何绑定、公式或数据源中提到的引用表的所有字段和关系都将添加到列表中。

    ![在“选择字段”页面上配置将从应用程序表中获取的字段列表。](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. 选择 **保存**，然后关闭 **选择字段** 页面。
6. 选择 **确定** 以存储您对数据源设置所做的更改。
7. 在操作窗格上，选择 **全部显示**。

    请注意，**调查表** 数据源现在显示文本 **\<Fields are filtered\>**。 此文本指示数据源已配置为从引用的应用程序表中提取数量有限的字段。

    ![在“模型映射设计器”页面上查看更新的模型映射。](./media/er-reduce-fetched-fields-number-mapping3.png)

8. 选择 **保存** 以存储您对可编辑模型映射所做的更改。

    > [!NOTE]
    > 在运行时，ER 分析添加的关系并将其中使用的所有字段添加到数据库查询中，即使这些字段在设计时没有显式添加到获取的字段列表中。

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>使用更新的模型映射运行提供的 ER 格式

执行 [从 ER 运行设计的格式](er-quick-start1-new-solution.md#RunFormatFromER)中的步骤，从 **配置** 页面运行为单个调查表提供的 ER 格式。

### <a name="review-the-execution-trace-of-the-second-run"></a>检查二次运行的执行跟踪

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，展开 **调查表模型**，并选择 **调查表映射**。
3. 在操作窗格上，选择 **设计器**。
4. 在 **模型到数据源映射** 页面上，选择 **设计器**。
5. 在 **模型映射设计器** 页的操作窗格上，选择 **性能跟踪**。
6. 在 **性能跟踪结果设置** 对话框中，选择上次格式运行期间生成的跟踪。
7. 选择 **确定**。
8. 在 **详细信息** 快速选项卡上，筛选指向 **调查表** 数据源的 **调查表** 路径。
9. 查看调用 **调查表** 数据源时生成的数据库查询的详细信息。

    请注意，仅在调用 **调查表** 数据源时，才在运行时从 `KMCollection` 应用程序表中获取填写数据源所需的字段。

    > [!NOTE]
    > 某些字段，例如分区 ID、数据区域 ID 和记录 ID 的字段，由 Finance 应用的数据管理框架自动添加。

    ![查看“模型映射设计器”页面上已更新模型映射的数据库查询的详细信息。](./media/er-reduce-fetched-fields-number-query2.png)

当您必须通过运行 ER 模型映射和 ER 格式减少内存消耗时，您可以使用此技术来减少提取的记录数。

## <a name="limitations"></a>限制

当您限制 *表记录* 类型的数据源的已获取字段数时，您不能使用数据源引用的应用程序表的方法，因为应用程序元数据不提供有关调用这些方法所需的表字段的信息。

## <a name="usage-notes"></a>使用说明

尽管 **自动填充** 命令会自动添加字段，但它不会自动删除先前添加的字段，即使这些字段不再用于可编辑模型映射的绑定、公式和数据源中也是如此。

选择 **自动填充** 时，ER 分析绑定、公式和可编辑模型映射在您打开它进行编辑时所具有的数据源。 如果您更改可编辑模型映射的绑定、公式和数据源，并且想要使用 **自动填充** 命令，请关闭模型映射设计器，然后重新打开它以编辑您的模型映射。 

## <a name="additional-resources"></a>其他资源

- [跟踪电子申报格式的执行以解决性能问题](trace-execution-er-troubleshoot-perf.md)
- [解决 ER 配置中的性能问题](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
