---
title: 通过添加参数化的计算字段数据源提高 ER 解决方案的性能
description: 本文介绍如何通过添加参数化的计算字段数据源提高电子报告 (ER) 解决方案的性能。
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c2c0499ac3d41c9bb6026cc05f971087799c28f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850105"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>通过添加参数化的计算字段数据源提高 ER 解决方案的性能

[!include [banner](../includes/banner.md)]

本文介绍如何通过配置参数化的 **计算字段** 数据源，对使用的[电子报告 (ER)](general-electronic-reporting.md) 格式进行[性能跟踪](trace-execution-er-troubleshoot-perf.md)，然后使用这些跟踪的信息帮助提高性能。

在设计 ER 配置以生成业务文档的过程中，您将定义用于从应用程序检索数据并在生成的输出中输入的方法。 通过设计 **计算字段** 类型的参数化 ER 数据源，可以减少数据库调用数量，从而减少收集 ER 格式执行详细信息所需时间和成本。

## <a name="prerequisites"></a>先决条件

- 要完成本文中的示例，您必须具有以下其中一个[角色](../sysadmin/tasks/assign-users-security-roles.md)的访问权限：

    - 电子报告开发人员
    - 电子申报功能顾问
    - 系统管理员

- 公司必须设置为 **DEMF**。
- 执行本文的[附录 1](#appendix1) 中的步骤，以下载完成本文中的示例所需的示例 Microsoft ER 解决方案的组件。
- 执行本文的[附录 2](#appendix2) 中的步骤，以配置使用 ER 框架提高示例 Microsoft ER 解决方案性能所需的最少 ER 参数。

## <a name="import-the-sample-er-solution"></a>导入示例 ER 解决方案

假设必须设计一种 ER 解决方案来生成新报表以显示供应商交易记录。 现在，您可以在 **供应商交易记录** 页（转至 **应付帐款** \> **供应商** \> **所有供应商**，选择供应商，然后在操作窗格中 **供应商** 选项卡上 **交易记录** 组中选择 **交易记录**）中找到所选供应商的交易记录。 但是，您希望让所有供应商交易记录都包含在一个 XML 格式的电子申报文档中。 此解决方案将由多个 ER 配置构成，这些配置中包含所需数据模型、模型映射和格式组件。

第一步是导入示例 ER 解决方案以生成供应商交易记录报表。

1. 登录为您的公司预配的 Microsoft Dynamics 365 Finance 实例。
2. 在本文中，将为示例公司 **Litware, Inc.** 创建并修改配置。 请确保已经将该配置提供程序添加到了您的 Finance 实例并标记为有效。 有关详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。
3. 在 **电子申报** 工作区中，选择 **报告配置** 磁贴。
4. 在 **配置** 页中，按照下面的顺序将作为先决条件下载的 ER 配置导入 Finance 中：数据模型、模型映射、格式。 为每个配置执行下列步骤:

    1. 在操作窗格上，选择 **交换** \> **从 XML 文件加载**。
    2. 选择 **浏览** 并为 ER 配置选择 XML 格式的相应文件。
    3. 选择 **确定**。

![“配置”页面上导入的配置。](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>检查示例 ER 解决方案

### <a name="review-the-model-mapping"></a>查看模型映射

1. 在 **配置** 页的配置树中，展开 **性能改进模型**，然后选择 **性能改进映射**。
2. 在操作窗格上，选择 **设计器**。
3. 在 **模型到数据源映射** 页面的操作窗格中，选择 **设计器**。

    此 ER 模型映射用于执行以下操作：

    - 提取 VendTrans 表中存储的供应商交易记录列表（**Trans** 数据源）。
    - 对于每笔交易记录，从 VendTable 表提取已经为其过帐的供应商的记录（**\#Vend** 数据源）。

    > [!NOTE]
    > **\#Vend** 数据源配置为使用现有的多对一关系 **\@.'\>Relations'.VendTable\_AccountNum** 提取对应的供应商记录。

    此配置中的模型映射实施为此模型创建并在 Finance 中运行的任何 ER 格式的基本数据模型。 因此，**Trans** 数据源的内容将对抽象 **model** 数据源之类 ER 格式公开。

    ![“模型映射设计器”页面上的 Trans 数据源。](media/er-calculated-field-ds-performance-mapping-1.png)

4. 关闭 **模型映射设计器** 页。
5. 关闭 **模型到数据源映射** 页。

### <a name="review-format"></a>查看格式

1. 在 **配置** 页的配置树中，展开 **性能改进模型**，然后选择 **性能改进格式**。
2. 在操作窗格上，选择 **设计器**。
3. 在 **格式设计器** 页中 **映射** 选项卡上，选择 **展开/折叠**。
4. 展开 **模型**、**数据** 和 **交易记录** 项。

    此 ER 格式用于生成 XML 格式的供应商交易记录报表。

    ![“格式设计器”页面上的 Format 数据源和配置的格式元素绑定。](media/er-calculated-field-ds-performance-format.png)

5. 关闭 **格式设计器** 页。

## <a name="run-the-sample-er-solution-to-trace-execution"></a>运行示例 ER 解决方案以跟踪执行情况

假设您已经完成了 ER 解决方案第一版的设计。 现在希望在 Finance 实例中测试解决方案并分析执行性能。

### <a name="turn-on-the-er-performance-trace"></a>开启 ER 性能跟踪

1. 选择 **DEMF** 公司。
2. 执行[开启 ER 性能跟踪](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace)中的步骤，以便在运行 ER 格式时生成性能跟踪。

    ![“用户参数”对话框。](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>运行 ER 格式

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的配置树中，选择 **性能改进格式**。
3. 在操作窗格上，选择 **运行**。

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>使用性能跟踪分析模型映射性能

1. 在 **配置** 页的配置树中，选择 **性能改进映射**。
2. 在操作窗格上，选择 **设计器**。
3. 在 **模型映射** 页面的操作窗格中，选择 **设计器**。
4. 在 **模型映射设计器** 页的操作窗格上，选择 **性能跟踪**。
5. 选择最近生成的跟踪，然后选择 **确定**。

新信息现在可用于当前模型映射的部分数据源项：

- 使用数据源获取数据实际所用时间
- 表示为占运行整个模型映射所用时间总量的百分比的相同时间

![“模型映射设计器”页面上的执行时间详细信息。](./media/er-calculated-field-ds-performance-mapping-2.png)

**性能统计信息** 网格显示 **Trans** 数据源调用一次 VendTrans 表。 **Trans** 数据源的值 **\[265\]\[Q:265\]** 说明已从应用程序表提取了 265 笔供应商交易记录并返回到了数据模型。

**性能统计信息** 网格显示运行 **\#Vend** 数据源时当前模型映射复制了数据源请求。 执行此项复制是因为：

- 将为这 265 个迭代供应商交易记录中的每一个调用供应商表两次，总计调用 530 次：

    - 调用一次以输入供应商帐户。
    - 调用一次以输入供应商名称。

- 将为每个迭代供应商记录调用供应商表，即使已经仅为五个供应商过帐了提取的交易记录也不例外。 这 530 个调用中的 525 是重复的。 下图显示收到的有关重复调用（数据库请求）的消息。

![“模型映射设计器”页面上有关重复数据库请求的消息。](./media/er-calculated-field-ds-performance-mapping-2a.png)

请注意，已使用了模型映射总执行时间（大约八秒）中超过 80%（大约六秒）从 VendTable 应用程序表检索值。 与 VendTrans 应用程序表中的信息量相比，此百分比对于五个供应商的两个属性而言太大。

若要减少为获取每个交易记录的供应商详细信息需要进行的调用数量和提高模型映射性能，可对 **\#Vend** 数据源使用缓存。

> [!NOTE]
> 运行时，将在 **Trans** 数据源的当前交易记录范围中缓存 **Trans\\\#Vend** 数据源。

可通过缓存 **\#Vend** 将重复调用数量从 525 减少到 260，但是不能完全消除重复。 若要完全消除重复，可以配置 **计算字段** 类型的新参数化数据源。

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>根据来自执行跟踪的信息改善模型映射

### <a name="change-the-logic-of-the-model-mapping"></a>更改模型映射的逻辑

执行以下步骤以使用缓存和 **计算字段** 类型的数据源避免重复调用数据库。

1. 在 **配置** 页的配置树中，选择 **性能改进映射**。
2. 在操作窗格上，选择 **设计器**。
3. 在 **模型映射** 页面的操作窗格中，选择 **设计器**。
4. 在 **模型映射设计器** 页面上，执行以下步骤添加 **表记录** 类型的数据源以访问 VendTable 应用程序表中的记录：

    1. 在 **数据源类型** 窗格中，展开 **Dynamics 365 for Operations**，然后选择 **表记录**。
    2. 选择 **添加根**。
    3. 在对话框的 **名称** 字段中，输入 **Vend**。
    4. 在 **表** 字段中，输入 **VendTable**。
    5. 选择 **确定**。

5. 仅当 **计算字段** 类型的数据源位于容器中，才能初始化对这些数据源的调用。 因此，请执行以下步骤添加 **空容器** 类型的数据源以保存 **计算字段** 类型的新参数化数据源：

    1. 在 **数据源类型** 窗格中，展开 **常规**，然后选择 **空容器**。
    2. 选择 **添加根**。
    3. 在对话框的 **名称** 字段中，输入 **Box**。
    3. 选择 **确定**。

    ![“模型映射设计器”页面上的 Box 数据源。](./media/er-calculated-field-ds-performance-mapping-3.png)

6. 执行以下步骤添加 **计算字段** 类型的参数化数据源：

    1. 在 **数据源** 窗格中选择 **Box**。
    2. 在 **数据源类型** 窗格中，展开 **函数**，然后选择 **计算字段**。
    3. 选择 **添加**。
    4. 在对话框的 **名称** 字段中，输入 **Vend**。
    5. 选择 **编辑公式**。
    6. 在 **公式设计器** 页面中，选择 **参数** 指定调用此数据源时必须提供的参数。
    7. 在 **参数** 对话框中，选择 **新建**。
    8. 在 **名称** 字段中，输入 **parmVendAccNumber**。
    9. 在 **类型** 字段中，选择 **字符串**。
    10. 选择 **确定**。
    11. 在 **公式** 字段中，输入 **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**。
    12. 选择 **保存**，然后关闭 **公式设计器** 页面。
    13. 选择 **确定** 添加新数据源。

7. 执行以下步骤将添加的数据源标记为在执行期间缓存：

    1. 在 **数据源** 窗格中，选择 **Box\\Vend**。
    2. 选择 **高速缓存**。

    > [!NOTE]
    > 运行时，将在 **Trans** 数据源的所有供应商交易记录范围中缓存 **Box\\Vend** 数据源。

8. 执行以下步骤更新嵌套的 **Trans\\\#Vend** 数据源，以使其使用 **Box\\Vend** 数据源：

    1. 在 **数据源** 窗格中，展开 **Trans**。
    2. 选择 **Trans\\\#Vend** 数据源，然后选择 **编辑** \> **编辑公式**。
    3. 在 **公式设计器** 页面的 **公式** 字段中，输入 **Box.Vend(\@.AccountNum)**。
    4. 选择 **保存**，然后关闭 **公式设计器** 页。
    5. 选择 **确定** 完成对所选数据源的更改。

9. 选择 **保存**。

    ![“模型映射设计器”页面上的 Vend 数据源。](./media/er-calculated-field-ds-performance-mapping-4.png)

10. 关闭 **模型映射设计器** 页。
11. 关闭 **模型映射** 页。

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>完成修改后的 ER 模型映射版本

1. 在 **配置** 页 **版本** 快速选项卡上，选择 **性能改进映射** 配置版本 **1.2**。
2. 选择 **更改状态** \> **完成**，然后选择 **确定**。

## <a name="run-the-modified-er-solution-to-trace-execution"></a>运行修改后的 ER 解决方案以跟踪执行情况

重复本文前面的[运行 ER 格式](#run-format)部分中的步骤生成一个新的性能跟踪。

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>使用性能跟踪分析对映射性能的调整 

1. 在 **配置** 页的配置树中，选择 **性能改进映射**。
2. 在操作窗格上，选择 **设计器**。
3. 在 **模型映射** 页面的操作窗格中，选择 **设计器**。
4. 在 **模型映射设计器** 页的操作窗格上，选择 **性能跟踪**。
5. 选择最近生成的跟踪，然后选择 **确定**。

请注意，您对模型映射进行的调整消除了对数据库的重复查询。 还减少了对此模型映射的数据库表和数据源的调用数量。

![跟踪“模型映射设计器”页面 1 上的信息。](./media/er-calculated-field-ds-performance-mapping-5.png)

总执行时间已缩短了大约 20 倍（从大约 8 秒到大约 400 毫秒）。 因此提高了整个 ER 解决方案的性能。

![跟踪“模型映射设计器”页面 2 上的信息。](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>附录 1：下载示例 Microsoft ER 解决方案的组件

必须下载以下文件并存储在本地。

| 文件                                        | 内容 |
|---------------------------------------------|---------|
| Performance improvement model.version.1     | [示例 ER 数据模型配置](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| Performance improvement mapping.version.1.1 | [示例 ER 模型映射配置](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| Performance improvement format.version.1.1  | [示例 ER 格式配置](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>附录 2：配置 ER 框架

必须先配置最低限度的 ER 参数，才能开始使用 ER 框架提高示例 Microsoft ER 解决方案的性能。

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>配置 ER 参数

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **电子申报参数**。
3. 在 **电子申报参数** 页上，在 **常规** 选项卡上，将 **启用设计模式** 选项设置为 **是**。
4. 在 **附件** 选项卡上，设置以下参数：

    - 在 **配置** 字段中，选择 **DEMF** 公司的 **文件** 类型。
    - 在 **作业存档**、**临时**、**基准** 和 **其他** 字段中，选择 **文件** 类型。

有关 ER 参数的详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>激活 ER 配置提供程序

将把添加的每个 ER 配置标记为由 ER 配置提供程序负责。 在 **电子申报** 工作区中激活的 ER 配置提供程序用于此目的。 因此，必须先在 **电子申报** 工作区中激活 ER 配置提供程序，才能开始添加或编辑 ER 配置。

> [!NOTE]
> 只有 ER 配置的负责人才能编辑此配置。 因此，必须先在 **电子申报** 工作区中激活相应 ER 配置提供程序，才能编辑 ER 配置。

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>查看 ER 配置提供程序列表

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。
3. 在 **配置提供程序表** 页面中，每条提供程序记录都有唯一名称和 URL。 查看此页面的内容。 如果已有 **Litware, Inc.** 的记录，请跳过下一过程，即[添加新 ER 配置提供程序](#ActivateProvider)。

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>添加新 ER 配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。
3. 在 **配置提供程序** 页面上，选择 **新建**。
4. 在 **名称** 字段中，输入 **Litware, Inc.**
5. 在 **Internet 地址** 字段中，输入 `https://www.litware.com`。
6. 选择 **保存**。

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>激活 ER 配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴，然后选择 **设置有效**。

有关 ER 配置提供程序的详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [跟踪电子申报格式的执行以解决性能问题](trace-execution-er-troubleshoot-perf.md)
- [支持对计算字段类型的 ER 数据源执行参数化调用](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
