---
title: 跟踪 ER 格式的执行情况以解决性能问题
description: 此主题介绍如何使用电子申报 (ER) 中的性能跟踪功能以解决性能问题。
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576538"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>跟踪 ER 格式的执行情况以解决性能问题

[!include[banner](../includes/banner.md)]

在设计电子申报 (ER) 配置过程中，您将定义用于从 Microsoft Dynamics 365 for Finance and Operations 获取数据并在生成的输出中输入的方法。 ER 性能跟踪功能有助于显著减少收集 ER 格式执行情况并将其用于解决性能问题的时间和成本。 本教程提供有关如何对 Finance and Operations 中执行的 ER 格式进行性能跟踪和如何使用来自这些跟踪的信息帮助提高性能的说明。

## <a name="prerequisites"></a>先决条件

要完成本教程中的示例，您必须具有以下访问权限：

- 访问 Finance and Operations 的以下其中一个角色：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

- 对于下列角色之一，已为与 Finance and Operations 相同的租户配置的Regulatory Configuration Services (RCS) 的实例：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

还必须下载并在本地存储以下文件。

| 文件                                  | 内容                               |
|---------------------------------------|---------------------------------------|
| Performance trace model.version.1     | [示例 ER 数据模型配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| Performance trace metadata.version.1  | [示例 ER 元数据配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| Performance trace mapping.version.1.1 | [示例 ER 模型映射配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Performance trace format.version.1.1  | [示例 ER 格式配置](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a>配置 ER 参数

Finance and Operations 中生成的每个 Er 性能跟踪都作为执行日志记录的附件存储。 Finance and Operations 的文档管理 (DM) 框架用于管理这些附件。 必须提前配置 ER 参数，以便指定应该用于附加性能跟踪的 DM 文档类型。 在 Finance and Operation 的**电子申报**工作区中，选择**电子申报参数**。 然后在**电子申报参数**页**附件**选项卡上的**其他**字段中，选择要用于性能跟踪的 DM 文档类型。

![Finance and Operations 中的“电子申报参数”页](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

若要让某个 DM 文档类型出现在**其他**查找字段中，必须在**文档类型**页（**组织管理 \> 文档管理 \> 文档类型**）中以下面的方式对其进行配置：

- **类：** 附加文件
- **组：** 文件

![Finance and Operations 中的“文档类型”页](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> 所选文档类型必须在当前 Finance and Operations 实例中的每个公司内可用，因为 DM 附件特定于公司。

### <a name="configure-rcs-parameters"></a>配置 RCS 参数

将通过使用 ER 格式设计器和 ER 映射设计器把 Finance and Operations 中生成的 Er 性能跟踪导入 RCS 中进行分析。 因为 ER 性能跟踪以与 ER 格式有关的执行日志记录附件形式存储，所以必须提前配置 RCS 参数，以便指定应该用于附加性能跟踪的 DM 文档类型。 在已经针对贵公司进行过配置的 RCS 实例中的**电子申报**工作区中，选择**电子申报参数**。 然后在**电子申报参数**页**附件**选项卡上的**其他**字段中，选择要用于性能跟踪的 DM 文档类型。

![RCS 中的“电子申报参数”页](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

若要让某个 DM 文档类型出现在**其他**查找字段中，必须在**文档类型**页（**组织管理 \> 文档管理 \> 文档类型**）中以下面的方式对其进行配置：

- **类：** 附加文件
- **组：** 文件

## <a name="design-an-er-solution"></a>设计 ER 解决方案

假设您已开始设计一种新的 ER 解决方案来生成新报表以表示供应商交易记录。 现在，您可以在**供应商交易记录**页（转至**应付帐款 \> 供应商 \> 所有供应商**，选择供应商，然后在操作窗格中**供应商**选项卡上**交易记录**组中选择**交易记录**）中找到所选供应商的交易记录。 但是，您希望同时让所有供应商交易记录都包含在一个 XML 格式的电子申报文档中。 此解决方案将由多个 ER 配置构成，这些配置中包含所需数据模型、元数据、模型映射和格式组件。

1. 登录已经针对贵公司进行过配置的 RCS 实例。
2. 在此教程中，将为示例公司 **Litware, Inc.** 创建并修改配置。 因此，请确保已经将该配置提供程序添加到了 RCS 并选择为有效。 有关说明，请参阅[创建配置提供程序并将其标记为有效](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)过程。
3. 在**电子申报**工作区中，选择**报告配置**磁贴。
4. 在**配置**页中，按照下面的顺序将作为先决条件下载的 ER 配置导入 RCS 中：数据模型、元数据、模型映射、格式。 为每个配置执行下列步骤:

    1. 在操作窗格上，选择**交换 \> 从 XML 文件加载**。
    2. 选择**浏览**为所需 ER 配置选择 XML 格式的相应文件。
    3. 选择**确定**。

    ![RCS 中的“配置”页](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>运行 ER 解决方案以跟踪执行情况

假设您已经完成了 ER 解决方案第一版的设计。 现在希望在 Finance and Operations instance 中进行测试并分析执行性能。

### <a id='import-configuration'></a>将 ER 配置从 RCS 导入 Finance and Operations

1. 登录到 Finance and Operations 实例。
2. 对于本教程，您将把配置从 RCS 实例（即您设计 ER 组件的位置）导入 Finance and Operations 实例（即测试并最终使用这些实例的位置）。 因此，您必须确保已准备好所有必需的项目。 有关说明，请参阅[从监管配置服务 (RCS) 导入电子申报 (ER) 配置](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)过程。
3. 执行下列步骤将配置从 RCS 导入 Finance and Operations：

    1. 在**电子申报**工作区 **Litware, Inc.** 配置提供程序的磁贴中，选择**存储库**。
    2. 在**配置存储库**页，选择 **RCS** 类型的存储库，然后选择**打开**。
    3. 在**配置**快速选项卡上，选择**性能跟踪格式**配置。
    4. 在**版本**快速选项卡上，选择所选配置的版本 **1.1**，然后选择**导入**。

    ![Finance and Operations 中的“配置存储库”页](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

将把相应的数据模型和模型映射配置版本作为所导入 ER 格式配置的先决条件自动导入。

### <a name="turn-on-the-er-performance-trace"></a>开启 ER 性能跟踪

1. 在 Finance and Operations 中，转到**组织管理 \> 电子申报 \> 配置**。
2. 在**配置**页操作窗格中**配置**选项卡的**高级设置**组中，选择**用户参数**。
3. 在**用户参数**对话框的**执行跟踪**部分中，执行以下步骤：

    1. 在**执行跟踪格式**字段中，选择**调试跟踪格式**开始收集 ER 格式执行情况的详细信息。 选择此值后，性能跟踪将收集有关以下操作所用时间的信息：

        - 在调用来获取数据的模型映射中运行每个数据源
        - 处理每个格式项以在生成的输出中输入数据

        使用**执行跟踪格式**字段为 ER 格式和映射元素指定用于存储执行详细信息的所生成性能跟踪的格式。 通过选择**调试跟踪格式**作为值，您可以在 ER Operation 设计器中分析跟踪内容，并查看跟踪中介绍的 ER 格式或映射元素。

    2. 将下列选项设置为**是**以收集 ER 模型映射和 ER 格式组件执行情况的具体详细信息：

        - **收集查询统计信息** – 如果开启此选项，性能跟踪将收集以下信息：

            - 数据源执行的数据库调用数量
            - 数据库的重复调用数量
            - 用于执行数据库调用的 SQL 语句的详细信息

        - **跟踪缓存访问** – 如果开启此选项，性能跟踪将收集有关 ER 模型映射的缓存使用情况的信息。
        - **跟踪数据访问** – 如果开启此选项，性能跟踪将收集有关对所执行记录列表类型数据源的数据库的调用数量的信息。
        - **跟踪列表枚举** – 如果开启此选项，性能跟踪将收集有关从记录列表类型数据源请求的记录数量的信息。

    > [!NOTE]
    > **用户参数**对话框中的参数特定于用户和当前公司。

    ![Finance and Operations 中的“用户参数”对话框](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a>运行 ER 格式

1. 在 Finance and Operations 中，选择 **DEMF** 公司。
2. 转到**组织管理 \> 电子申报 \> 配置**。
3. 在**配置**页的配置树中，选择**性能跟踪格式**项。
4. 在操作窗格上，选择**运行**。

请注意，生成的文件中提供有关六个供应商的 265 个交易记录的信息。

## <a name="review-the-execution-trace"></a>查看执行跟踪

### <a id='export-trace'></a>从 Finance and Operations 导出生成的跟踪

性能跟踪将从源 ER 格式分离，并可序列化为外部 zip 文件。

1. 在 Finance and Operations 中，转到**组织管理 \> 电子申报 \> 配置调试日志**。
2. 在**电子申报运行日志**页左窗格中**配置名称**字段中，选择**性能跟踪格式**查找已通过执行**性能跟踪格式**配置生成的日志记录。
3. 选择页面右上角的**附件**按钮（回形针符号），或按 **Ctrl+Shift+A**。

    ![Finance and Operations 中“电子申报运行日志”页上的“附件”按钮](./media/GER-PerfTrace-GER-DebugLog.png)

4. 在**电子申报运行日志的附件**页上操作窗格中，选择**打开**获取 zip 文件格式的性能跟踪并存储在本地。

    ![Finance and Operations 中的“电子申报运行日志的附件”页](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> 生成的跟踪只有对源 ER 报表通过 **GUID** 格式的唯一报表标识进行的引用。 不考虑格式的版本编号。

请注意，已经为所执行 ER 格式生成的性能跟踪与 ER 模型映射之间的关联基于所用根描述符和常用数据模型。 不考虑格式和模型映射的版本编号。 也不考虑模型映射的**模型映射默认值**标记的设置。

### <a id='import-trace'></a>将生成的跟踪导入 RCS

1. 在 RCS 的**电子申报**工作区中，选择**报告配置**磁贴。
2. 在**配置**页的配置树中，展开**性能跟踪模型**项，然后选择**性能跟踪格式**项。
3. 在操作窗格上，选择**设计器**。
4. 在**格式设计器**页的操作窗格上，选择**性能跟踪**。
5. 在**性能跟踪结果配置**对话框中，选择**导入性能跟踪**。
6. 选择**浏览**以选择之前从 Finance and Operations 导出的 zip 文件。
7. 选择**确定**。

    ![RCS 中的“性能跟踪结果设置”对话框](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>在 RCS 中使用性能跟踪进行分析 – 格式执行

1. 在 RCS 的**格式设计器**页中，选择**展开/折叠**以展开所有格式项的目录。

    请注意，当前格式的某些项会显示更多信息：

    - 通过使用格式项在生成的输出中输入数据实际所用时间
    - 表示为占生成整个输出所用时间总量的百分比的相同时间

    ![RCS 中的“格式设计器”页](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. 关闭**格式设计器**页。

### <a id='use-trace'></a>在 RCS 中使用性能跟踪进行分析 – 模型映射

1. 在 RCS 的**配置**页的配置树中，选择**性能跟踪映射**项。
2. 在操作窗格上，选择**设计器**。
3. 选择**设计器**。
4. 在**模型映射设计器**页的操作窗格上，选择**性能跟踪**。
5. 选择之前导入的跟踪。
6. 选择**确定**。

请注意，新信息将可用于当前模型映射的部分数据源项：

- 使用数据源获取数据实际所用时间
- 表示为占运行整个模型映射所用时间总量的百分比的相同时间

请注意，ER 将在运行 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源时通知您数据库请求的当前模型映射重复项。 出现此重复项的原因是为每个迭代的供应商记录调用了两次供应商交易记录列表：

- 一次调用是为了根据配置的绑定在数据模型中输入每个交易记录的详细信息。
- 一次调用是为了在数据模型中输入为每个供应商计算出的交易记录数量。

![RCS 中“模型映射设计器”页上有关重复数据库请求的消息](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

值 **\[Q:530\]** 表示 VendTrans 表被调用了 530 次以将一个记录从该表返回到 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源。 值 **\[530\]** 表示 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源被调用了 530 次以从该数据源返回一个记录并在数据模型中输入来自该记录的详细信息。

建议使用 VendTable/\<Relations/VendTrans.VendTable\_AccountNum 数据源的高速缓存减少为了获取 265 个交易记录所执行调用的数量，并帮助提高模型映射的性能。

减少对 LedgerTransTypeList 数据源执行的调用数量可能也很有用。 此数据源用于将 **LedgerTransType** 枚举的每个值与其标签关联。 可通过使用此数据源找到相应标签并在每个供应商交易记录的数据模型中输入。 相对 265 个交易记录而言，对此数据源的当前调用数量 (9,027) 相当高。

![RCS 中的“模型映射设计器”页，其中显示了对数据源的 9,027 个调用](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>根据来自执行跟踪的信息改善模型映射

### <a name="modify-the-logic-of-the-model-mapping"></a>修改模型映射的逻辑

1. 请执行以下步骤使用高速缓存来帮助避免重复调用数据库：

    1. 在 RCS 的**模型映射设计器**页**数据源**窗格中，选择 **VendTable** 项。
    2. 选择**高速缓存**。
    3. 展开 **VendTable** 向，展开 VendTable 数据源的一对多关系列表（即 **\<Relations** 项），然后选择 **VendTrans.VendTable\_AccountNum** 项。
    4. 选择**高速缓存**。

    ![用于帮助避免重复调用的高速缓存设置](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. 执行以下步骤将 LedgerTransTypeList 数据源纳入 VendTable 数据源的范围内：

    1. 在**数据源类型**窗格中，展开**函数**项，然后选择**计算字段**项。
    2. 在**数据源**窗格中，选择 **VendTable** 项。
    3. 选择**添加**。
    4. 在**名称**字段中，输入 **\$TransType**。
    5. 选择**编辑公式**。
    6. 在**公式**字段中，输入 **LedgerTransTypeList**。
    7. 选择**保存**。
    8. 关闭**公式编辑器**页。
    9. 单击 **确定**。

3. 执行下列步骤对 **\$TransType** 字段执行高速缓存：

    1. 选择 **LedgerTransTypeList** 项。
    2. 选择**高速缓存**。
    3. 选择 **VendTable.\$TransType** 项。
    4. 选择**高速缓存**。

    ![$TransType 字段的高速缓存设置](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. 执行以下步骤更改 **\$TransTypeRecord** 字段，使其开始使用高速缓存的 **\$TransType** 字段：

    1. 在**数据源**窗格中，依次展开 **VendTable**、**\<Relations** 和 **VendTrans.VendTable\_AccountNum** 项，然后选择 **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** 项。
    2. 选择**编辑**。
    3. 选择**编辑公式**。
    4. 在**公式**字段中，找到下面的表达式：

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. 在**公式**字段中，输入下面的表达式：

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType))。

    6. 选择**保存**。
    7. 关闭**公式编辑器**页。
    8. 选择**确定**。

5. 选择**保存**。
6. 关闭**模型映射设计器**页。
7. 关闭**模型映射**页。

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>完成修改后的 ER 模型映射版本

1. 在 RCS 中的**配置**页**版本**快速选项卡上，选择**性能跟踪映射**配置版本 **1.2**。
2. 选择**更改状态**。
3. 选择**完成**。

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a>将修改后的 ER 模型映射配置从 RCS 导入 Finance and Operations

重复本主题前面的[将 ER 配置从 RCS 导入 Finance and Operations](#import-configuration) 部分中的步骤将**性能跟踪映射**配置版本 1.2 导入 Finance and Operations。

## <a name="run-the-modified-er-solution-to-trace-execution"></a>运行修改后的 ER 解决方案以跟踪执行情况

### <a name="run-the-er-format"></a>运行 ER 格式

重复本主题前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。

## <a name="review-the-execution-trace"></a>查看执行跟踪

### <a name="export-the-generated-trace-from-finance-and-operations"></a>从 Finance and Operations 导出生成的跟踪

重复本主题前面的[从 Finance and Operations 导出生成的跟踪](#export-trace)部分中的步骤在本地保存新的性能跟踪。

### <a name="import-the-generated-trace-into-rcs"></a>将生成的跟踪导入 RCS

重复本主题前面的[将生成的跟踪导入 RCS](#import-trace) 部分中的步骤将新的性能跟踪导入 RCS。

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>在 RCS 中使用性能跟踪进行分析 – 模型映射

重复本主题前面的[在 RCS 中使用性能跟踪进行分析 – 模型映射](#use-trace)部分中的步骤分析最新性能跟踪。

请注意，您对模型映射进行的调整消除了对数据库的重复查询。 还减少了对此模型映射的数据库表和数据源的调用数量。 因此提高了整个 ER 解决方案的性能。

![在 RCS 的“模型映射设计器”页中跟踪 VendTable 数据源的信息](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

在跟踪信息中，VendTable 数据源的值 **\[12\]** 表示此数据源被调用了 12 次。 值 **\[Q:6\]** 表示六个调用被转换为了对 VendTable 表的数据库调用。 值 **\[C:6\]** 表示已缓存了从数据库获取的记录，并且通过使用高速缓存还除了另外六个调用。

请注意，对 LedgerTransTypeList 数据源的调用数量已从 9,027 降低到了 240。

![在 RCS 的“模型映射设计器”页中跟踪 LedgerTransTypeList 数据源的信息](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a>在 Finance and Operations 中查看执行跟踪

除了 RCS，还有一些 Finance and Operations 版本可能提供针对 ER 框架设计器体验的功能。 这些 Finance and Operations 版本有一个可开启的**启用设计模式**选项。 可以在**电子申报参数**页（可从**电子申报**工作区打开该页）中的**常规**选项卡上找到此选项。

![在 Finance and Operations 的“电子申报参数”页中启用设计模式选项](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

如果使用这些 Finance and Operations 版本中的一个，您可以直接在 Finance and Operations 中分析生成的性能跟踪的详细信息。 无需将其从 Finance and Operation 中导出，再导入 RCS。

## <a name="review-the-execution-trace-by-using-external-tools"></a>通过使用外部工具查看执行跟踪

### <a name="configure-user-parameters"></a>配置用户参数

1. 在 Finance and Operations 中，转到**组织管理 \> 电子申报 \> 配置**。
2. 在**配置**页操作窗格中**配置**选项卡的**高级设置**组中，选择**用户参数**。
3. 在**用户参数**对话框**执行跟踪**部分的**执行跟踪格式**字段中，选择 **PerfView XML**。

### <a name="run-the-er-format"></a>运行 ER 格式

重复本主题前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。

请注意，Web 浏览器提供一个可供下载的 zip 文件。 这个文件中包含 PerfView 格式的性能跟踪。 然后可使用 PerfView 性能分析工具分析 ER 格式执行情况的详细信息。
