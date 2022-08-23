---
title: 跟踪电子申报格式的执行以解决性能问题
description: 本文介绍如何使用电子报告 (ER) 中的性能跟踪功能以解决性能问题。
author: kfend
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 9f088228b140a42ee097c9e810166550ab0fae81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289935"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>跟踪 ER 格式的执行情况以解决性能问题

[!include[banner](../includes/banner.md)]

在设计电子申报 (ER) 配置过程中，您将定义用于从应用程序获取数据并在生成的输出中输入的方法。 ER 性能跟踪功能有助于显著减少收集 ER 格式执行情况并将其用于解决性能问题的时间和成本。 本教程提供有关如何对执行的 ER 格式进行性能跟踪和如何使用来自这些跟踪的信息帮助提高性能的说明。

## <a name="prerequisites"></a>先决条件

要完成本教程中的示例，您必须具有以下访问权限：

- 访问以下其中一个角色：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

- 对于下列角色之一，已为与应用程序相同的租户配置的 Regulatory Configuration Services (RCS) 的实例：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

还必须下载并在本地存储以下文件。

| 文件                                  | 内容                               |
|---------------------------------------|---------------------------------------|
| Performance trace model.version.1     | [示例 ER 数据模型配置](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| Performance trace metadata.version.1  | [示例 ER 元数据配置](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| Performance trace mapping.version.1.1 | [示例 ER 模型映射配置](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| Performance trace format.version.1.1  | [示例 ER 格式配置](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a>配置 ER 参数

应用程序中生成的每个 Er 性能跟踪都作为执行日志记录的附件存储。 文档管理 (DM) 框架用于管理这些附件。 必须提前配置 ER 参数，以便指定应该用于附加性能跟踪的 DM 文档类型。 在 **电子申报** 工作区中，选择 **电子申报参数** 链接。 然后在 **电子申报参数** 页 **附件** 选项卡上的 **其他** 字段中，选择要用于性能跟踪的 DM 文档类型。

![“电子报告参数”页面。](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

若要让某个 DM 文档类型出现在 **其他** 查找字段中，必须在 **文档类型** 页（**组织管理 \> 文档管理 \> 文档类型**）中以下面的方式对其进行配置：

- **类：** 附加文件
- **组：** 文件

![文档类型页面。](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> 所选文档类型必须在当前实例中的每个公司内可用，因为 DM 附件特定于公司。

### <a name="configure-rcs-parameters"></a>配置 RCS 参数

将通过使用 ER 格式设计器和 ER 映射设计器把生成的 ER 性能跟踪导入 RCS 中进行分析。 因为 ER 性能跟踪以与 ER 格式有关的执行日志记录附件形式存储，所以必须提前配置 RCS 参数，以便指定应该用于附加性能跟踪的 DM 文档类型。 在已经针对贵公司进行过配置的 RCS 实例中的 **电子申报** 工作区中，选择 **电子申报参数**。 然后在 **电子申报参数** 页 **附件** 选项卡上的 **其他** 字段中，选择要用于性能跟踪的 DM 文档类型。

![RCS 中的“电子报告参数”页面。](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

若要让某个 DM 文档类型出现在 **其他** 查找字段中，必须在 **文档类型** 页（**组织管理 \> 文档管理 \> 文档类型**）中以下面的方式对其进行配置：

- **类：** 附加文件
- **组：** 文件

## <a name="design-an-er-solution"></a>设计 ER 解决方案

假设您已开始设计一种新的 ER 解决方案来生成新报表以表示供应商交易记录。 现在，您可以在 **供应商交易记录** 页（转至 **应付帐款 \> 供应商 \> 所有供应商**，选择供应商，然后在操作窗格中 **供应商** 选项卡上 **交易记录** 组中选择 **交易记录**）中找到所选供应商的交易记录。 但是，您希望同时让所有供应商交易记录都包含在一个 XML 格式的电子申报文档中。 此解决方案将由多个 ER 配置构成，这些配置中包含所需数据模型、元数据、模型映射和格式组件。

1. 登录已经针对贵公司进行过配置的 RCS 实例。
2. 在此教程中，将为示例公司 **Litware, Inc.** 创建并修改配置。 因此，请确保已经将该配置提供程序添加到了 RCS 并选择为有效。 有关说明，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程。
3. 在 **电子申报** 工作区中，选择 **报告配置** 磁贴。
4. 在 **配置** 页中，按照下面的顺序将作为先决条件下载的 ER 配置导入 RCS 中：数据模型、元数据、模型映射、格式。 为每个配置执行下列步骤:

    1. 在操作窗格上，选择 **交换 \> 从 XML 文件加载**。
    2. 选择 **浏览** 为所需 ER 配置选择 XML 格式的相应文件。
    3. 选择 **确定**。

    ![RCS 中的“配置”页面。](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>运行 ER 解决方案以跟踪执行情况

假设您已经完成了 ER 解决方案第一版的设计。 现在希望在实例中进行测试并分析执行性能。

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a>将 ER 配置从 RCS 导入财务和运营

1. 登录您的应用程序实例。
2. 对于本教程，您将把配置从 RCS 实例（即您设计 ER 组件的位置）导入实例（即测试并最终使用这些实例的位置）。 因此，您必须确保已准备好所有必需的项目。 有关说明，请参阅[从监管配置服务 (RCS) 导入电子申报 (ER) 配置](rcs-download-configurations.md)过程。
3. 执行下列步骤将配置从 RCS 导入应用程序中：

    1. 在 **电子申报** 工作区 **Litware, Inc.** 配置提供程序的磁贴中，选择 **存储库**。
    2. 在 **配置存储库** 页，选择 **RCS** 类型的存储库，然后选择 **打开**。
    3. 在 **配置** 快速选项卡上，选择 **性能跟踪格式** 配置。
    4. 在 **版本** 快速选项卡上，选择所选配置的版本 **1.1**，然后选择 **导入**。

    ![配置存储库页面。](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

将把相应的数据模型和模型映射配置版本作为所导入 ER 格式配置的先决条件自动导入。

### <a name="turn-on-the-er-performance-trace"></a>开启 ER 性能跟踪

1. 转到 **组织管理 \> 电子申报 \> 配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 在 **用户参数** 对话框的 **执行跟踪** 部分中，执行以下步骤：

    1. 在 **执行跟踪格式** 字段中，为 ER 格式和映射元素指定应该用于存储执行详细信息的所生成性能跟踪的格式。

        - **调试跟踪格式** – 如果您计划以交互方式运行执行时间较短的 ER 格式，请选择此值。 然后，开始收集有关 ER 格式执行的详细信息。 选择此值后，性能跟踪将收集有关以下操作所用时间的信息：

            - 在调用来获取数据的模型映射中运行每个数据源
            - 处理每个格式项以在生成的输出中输入数据

            如果您选择 **调试跟踪格式** 值，可以在 ER 操作设计器中分析跟踪的内容。 在那里，您可以查看跟踪中提到的 ER 格式或映射元素。

        - **聚合跟踪格式** – 如果您计划在批处理模式下运行执行时间较长的 ER 格式，请选择此值。 然后，开始收集有关 ER 格式执行的聚合详细信息。 选择此值后，性能跟踪将收集有关以下操作所用时间的信息：

            - 在调用来获取数据的模型映射中运行每个数据源
            - 在调用来获取数据的格式映射中运行每个数据源
            - 处理每个格式项以在生成的输出中输入数据

            **聚合跟踪格式** 值在 Microsoft Dynamics 365 Finance 版本 10.0.20 及更高版本中可用。

            在 ER 格式设计器和 ER 模型映射设计器中，您可以查看单个组件的总执行时间。 此外，跟踪包含有关执行的详细信息，例如执行次数以及单次执行的最短和最长时间。

            > [!NOTE]
            > 此跟踪基于跟踪的组件路径收集。 因此，当单个父组件包含多个未命名的子组件或多个子组件具有相同名称时，统计信息可能不正确。

    2. 将下列选项设置为 **是** 以收集 ER 模型映射和 ER 格式组件执行情况的具体详细信息：

        - **收集查询统计信息** – 如果开启此选项，性能跟踪将收集以下信息：

            - 数据源执行的数据库调用数量
            - 数据库的重复调用数量
            - 用于执行数据库调用的 SQL 语句的详细信息

        - **跟踪缓存访问** – 如果开启此选项，性能跟踪将收集有关 ER 模型映射的缓存使用情况的信息。
        - **跟踪数据访问** – 如果开启此选项，性能跟踪将收集有关对所执行记录列表类型数据源的数据库的调用数量的信息。
        - **跟踪列表枚举** – 如果开启此选项，性能跟踪将收集有关从记录列表类型数据源请求的记录数量的信息。

    > [!NOTE]
    > **用户参数** 对话框中的参数特定于用户和当前公司。

    ![“用户参数”对话框。](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a>运行 ER 格式

1. 选择 **DEMF** 公司。
2. 转到 **组织管理 \> 电子申报 \> 配置**。
3. 在 **配置** 页的配置树中，选择 **性能跟踪格式** 项。
4. 在操作窗格上，选择 **运行**。

请注意，生成的文件中提供有关六个供应商的 265 个交易记录的信息。

## <a name="review-the-execution-trace"></a>查看执行跟踪

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a>从应用程序导出生成的跟踪

性能跟踪将从源 ER 格式分离，并可序列化为外部 zip 文件。

1. 转到 **组织管理 \> 电子申报 \> 配置调试日志**。
2. 在 **电子申报运行日志** 页左窗格中 **配置名称** 字段中，选择 **性能跟踪格式** 查找已通过执行 **性能跟踪格式** 配置生成的日志记录。
3. 选择页面右上角的 **附件** 按钮（回形针符号），或按 **Ctrl+Shift+A**。

    ![“电子报告运行日志”页面上的“附件”按钮。](./media/GER-PerfTrace-GER-DebugLog.png)

4. 在 **电子申报运行日志的附件** 页上操作窗格中，选择 **打开** 获取 zip 文件格式的性能跟踪并存储在本地。

    ![电子报告运行日志的附件。](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> 生成的跟踪只有对源 ER 报表通过 **GUID** 格式的唯一报表标识进行的引用。 不考虑格式的版本编号。

请注意，已经为所执行 ER 格式生成的性能跟踪与 ER 模型映射之间的关联基于所用根描述符和常用数据模型。 不考虑格式和模型映射的版本编号。 也不考虑模型映射的 **模型映射默认值** 标记的设置。

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a>将生成的跟踪导入 RCS

1. 在 RCS 的 **电子申报** 工作区中，选择 **报告配置** 磁贴。
2. 在 **配置** 页的配置树中，展开 **性能跟踪模型** 项，然后选择 **性能跟踪格式** 项。
3. 在操作窗格上，选择 **设计器**。
4. 在 **格式设计器** 页的操作窗格上，选择 **性能跟踪**。
5. 在 **性能跟踪结果配置** 对话框中，选择 **导入性能跟踪**。
6. 选择 **浏览** 以选择之前导出的 zip 文件。
7. 选择 **确定**。

    ![RCS 中的“性能跟踪结果设置”对话框。](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>在 RCS 中使用性能跟踪进行分析 – 格式执行

1. 在 RCS 的 **格式设计器** 页中，选择 **展开/折叠** 以展开所有格式项的目录。

    请注意，当前格式的某些项会显示更多信息：

    - 通过使用格式项在生成的输出中输入数据实际所用时间
    - 表示为占生成整个输出所用时间总量的百分比的相同时间

    ![RCS 中的“格式设计器”页面。](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. 关闭 **格式设计器** 页。

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a>在 RCS 中使用性能跟踪进行分析 – 模型映射

1. 在 RCS 的 **配置** 页的配置树中，选择 **性能跟踪映射** 项。
2. 在操作窗格上，选择 **设计器**。
3. 选择 **设计器**。
4. 在 **模型映射设计器** 页的操作窗格上，选择 **性能跟踪**。
5. 选择之前导入的跟踪。
6. 选择 **确定**。

请注意，新信息将可用于当前模型映射的部分数据源项：

- 使用数据源获取数据实际所用时间
- 表示为占运行整个模型映射所用时间总量的百分比的相同时间

请注意，ER 将在运行 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源时通知您数据库请求的当前模型映射重复项。 出现此重复项的原因是为每个迭代的供应商记录调用了两次供应商交易记录列表：

- 一次调用是为了根据配置的绑定在数据模型中输入每个交易记录的详细信息。
- 一次调用是为了在数据模型中输入为每个供应商计算出的交易记录数量。

![RCS 中“模型映射设计器”页面上有关重复数据库请求的消息。](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

值 **\[Q:530\]** 表示 VendTrans 表被调用了 530 次以将一个记录从该表返回到 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源。 值 **\[530\]** 表示 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源被调用了 530 次以从该数据源返回一个记录并在数据模型中输入来自该记录的详细信息。

建议使用 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源的高速缓存减少为了获取 265 个交易记录所执行调用的数量，并帮助提高模型映射的性能。

减少对 LedgerTransTypeList 数据源执行的调用数量可能也很有用。 此数据源用于将 **LedgerTransType** 枚举的每个值与其标签关联。 可通过使用此数据源找到相应标签并在每个供应商交易记录的数据模型中输入。 相对 265 个交易记录而言，对此数据源的当前调用数量 (9,027) 相当高。

![RCS 中的“模型映射设计器”页面，其中显示了对数据源的 9,027 个调用。](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>根据来自执行跟踪的信息改善模型映射

### <a name="modify-the-logic-of-the-model-mapping"></a>修改模型映射的逻辑

1. 请执行以下步骤使用高速缓存来帮助避免重复调用数据库：

    1. 在 RCS 的 **模型映射设计器** 页 **数据源** 窗格中，选择 **VendTable** 项。
    2. 选择 **高速缓存**。
    3. 展开 **VendTable** 向，展开 VendTable 数据源的一对多关系列表（即 **\<Relations** 项），然后选择 **VendTrans.VendTable\_AccountNum** 项。
    4. 选择 **高速缓存**。

    ![用于帮助避免重复调用的高速缓存设置。](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. 执行以下步骤将 LedgerTransTypeList 数据源纳入 VendTable 数据源的范围内：

    1. 在 **数据源类型** 窗格中，展开 **函数** 项，然后选择 **计算字段** 项。
    2. 在 **数据源** 窗格中，选择 **VendTable** 项。
    3. 选择 **添加**。
    4. 在 **名称** 字段中，输入 **\$TransType**。
    5. 选择 **编辑公式**。
    6. 在 **公式** 字段中，输入 **LedgerTransTypeList**。
    7. 选择 **保存**。
    8. 关闭 **公式编辑器** 页。
    9. 单击 **确定**。

3. 执行下列步骤对 **\$TransType** 字段执行高速缓存：

    1. 选择 **LedgerTransTypeList** 项。
    2. 选择 **高速缓存**。
    3. 选择 **VendTable.\$TransType** 项。
    4. 选择 **高速缓存**。

    ![$TransType 字段的高速缓存设置。](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. 执行以下步骤更改 **\$TransTypeRecord** 字段，使其开始使用高速缓存的 **\$TransType** 字段：

    1. 在 **数据源** 窗格中，依次展开 **VendTable**、**\<Relations** 和 **VendTrans.VendTable\_AccountNum** 项，然后选择 **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** 项。
    2. 选择 **编辑**。
    3. 选择 **编辑公式**。
    4. 在 **公式** 字段中，找到下面的表达式：

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. 在 **公式** 字段中，输入下面的表达式：

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType))。

    6. 选择 **保存**。
    7. 关闭 **公式编辑器** 页。
    8. 选择 **确定**。

5. 选择 **保存**。
6. 关闭 **模型映射设计器** 页。
7. 关闭 **模型映射** 页。

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>完成修改后的 ER 模型映射版本

1. 在 RCS 中的 **配置** 页 **版本** 快速选项卡上，选择 **性能跟踪映射** 配置版本 **1.2**。
2. 选择 **更改状态**。
3. 选择 **完成**。

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>将修改后的 ER 模型映射配置从 RCS 导入应用程序中

重复本文前面的 [将 ER 配置从 RCS 导入财务和运营](#import-configuration) 一节中的步骤导入 **性能跟踪映射** 配置版本 1.2。

## <a name="run-the-modified-er-solution-to-trace-execution"></a>运行修改后的 ER 解决方案以跟踪执行情况

### <a name="run-the-er-format"></a>运行 ER 格式

重复本文前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。

## <a name="work-with-the-execution-trace"></a>使用执行跟踪

### <a name="export-the-generated-trace-from-the-application"></a>从应用程序导出生成的跟踪

重复本文前面的[从应用程序导出生成的跟踪](#export-trace)一节中的步骤在本地保存新的性能跟踪。

### <a name="import-the-generated-trace-into-rcs"></a>将生成的跟踪导入 RCS

重复本文前面的[将生成的跟踪导入 RCS](#import-trace) 一节中的步骤将新的性能跟踪导入 RCS。

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>在 RCS 中使用性能跟踪进行分析 – 模型映射

重复本文前面的[在 RCS 中使用性能跟踪进行分析 – 模型映射](#use-trace)一节中的步骤分析最新性能跟踪。

请注意，您对模型映射进行的调整消除了对数据库的重复查询。 还减少了对此模型映射的数据库表和数据源的调用数量。 因此提高了整个 ER 解决方案的性能。

![在 RCS 的“模型映射设计器”页面中跟踪 VendTable 数据源的信息。](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

在跟踪信息中，VendTable 数据源的值 **\[12\]** 表示此数据源被调用了 12 次。 值 **\[Q:6\]** 表示六个调用被转换为了对 VendTable 表的数据库调用。 值 **\[C:6\]** 表示已缓存了从数据库获取的记录，并且通过使用高速缓存还除了另外六个调用。

请注意，对 LedgerTransTypeList 数据源的调用数量已从 9,027 降低到了 240。

![在 RCS 的“模型映射设计器”页面中跟踪 LedgerTransTypeList 数据源的信息。](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>检查应用程序中的执行跟踪

除了 RCS，还有一些版本可能提供针对 ER 框架设计器体验的功能。 这些版本有一个可开启的 **启用设计模式** 选项。 可以在 **电子申报参数** 页（可从 **电子申报** 工作区打开该页）中的 **常规** 选项卡上找到此选项。

![在“电子报告参数”页面中启用设计模式选项。](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

如果使用这些版本中的一个，您可以直接在应用程序中分析生成的性能跟踪的详细信息。 无需将其从应用程序中导出，再导入 RCS。

## <a name="review-the-execution-trace-by-using-external-tools"></a>通过使用外部工具查看执行跟踪

### <a name="configure-user-parameters"></a>配置用户参数

1. 转到 **组织管理 \> 电子申报 \> 配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 在 **用户参数** 对话框 **执行跟踪** 部分的 **执行跟踪格式** 字段中，选择 **PerfView XML**。

### <a name="run-the-er-format"></a>运行 ER 格式

重复本文前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。

请注意，Web 浏览器提供一个可供下载的 zip 文件。 这个文件中包含 PerfView 格式的性能跟踪。 然后可使用 PerfView 性能分析工具分析 ER 格式执行情况的详细信息。

![PerfView 格式的性能跟踪信息。](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>使用外部工具查看其中包含数据库查询的执行跟踪

因为已改进了 ER 框架，所以以 PerfView 格式生成的绩效跟踪现在提供更多有关 ER 格式执行的详细信息。 在 Microsoft Dynamics 365 Finance 版本 10.0.4（2019 年 7 月）中，此跟踪中也可以包含对执行的 SQL 查询的详细信息。

### <a name="configure-user-parameters"></a>配置用户参数

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 在 **用户参数** 对话框的 **执行跟踪** 部分中，设置以下参数：

    - 在 **执行跟踪格式** 字段中，选择 **PerfView XML**。
    - 将 **收集查询统计信息** 选项设置为 **是**。
    - 将 **跟踪查询** 选项设置为 **是**。

    ![执行跟踪部分，“用户参数”对话框。](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>运行 ER 格式

重复本文前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。

请注意，Web 浏览器提供一个可供下载的 zip 文件。 这个文件中包含 PerfView 格式的性能跟踪。 然后可使用 PerfView 性能分析工具分析 ER 格式执行情况的详细信息。 执行 ER 格式期间，此跟踪中现在包含 SQL 数据库访问权限的详细信息。

![在 PerfView 中跟踪执行的 ER 格式的信息。](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [通过添加参数化的计算字段数据源提高 ER 解决方案的性能](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

