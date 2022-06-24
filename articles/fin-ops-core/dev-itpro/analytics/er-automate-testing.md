---
title: 自动测试电子报告
description: 本文介绍如何使用电子报告 (ER) 框架的基准功能自动测试功能。
author: NickSelin
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: df2baa988bb634db11d819dd84ef73eaa560bab9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892760"
---
# <a name="automate-testing-with-electronic-reporting"></a>自动测试电子报告

[!include[banner](../includes/banner.md)]

本文介绍如何使用电子报告 (ER) 框架自动测试某些功能。 本文中的示例演示如何自动测试供应商付款处理。

供应商付款处理期间，应用程序使用 ER 框架生成付款文件和相应单据。 ER 框架中包含数据模型、模型映射，以及格式组件，它们支持对不同付款类型进行付款处理和生成不同格式的单据。 可以从 Microsoft Dynamics Lifecycle Services (LCS) 下载这些组件并导入到实例中。

还可以自定义每个 Microsoft 组件，并将其用作您自己的自定义组件的基础。 通过创建自定义版本，您可以进行支持特定要求的更改。 例如，可调整 ER 数据模型和 ER 模型映射以访问客户特定的应用程序数据，也可以更改 ER 格式以修改所生成单据的布局。

可使用自定义的 ER 格式处理用于生成供应商付款的付款文件，以及处理控制报表。 ER 组件中支持版本控制。 因此，Microsoft 可以提供更新后的 ER 解决方案版本来处理供应商付款，而您可以通过为其重定基本值来自动将更新后的版本与自定义的组件合并。 但是，必须测试重定基本值后的版本，以确保其正常工作。

ER 数据模型和 ER 模型映射支持大量 ER 格式，用于处理不同类型的付款和生成国家/地区特定的付款单据。 因此，非常需要自动执行用户接受度与集成测试，以便在多家公司中自动完成此操作，但是请注意各目标公司的国家/地区上下文，使用不同数据集，等等。

有关如何使用基于从配置提供程序收到的格式的自定义格式版本的详细信息，请参阅 [ER 通过采用该格式的新的基本版本升级格式](./tasks/er-upgrade-format.md)。

## <a name="key-concepts"></a>重要概念

高级功能用户不必编写源代码即可创作接受度和集成测试。

- 使用 ER 基准功能将生成的单据与主副本进行比较。 有关详细信息，请参阅[跟踪生成的报告结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)。
- 使用任务录制器录制测试用例，并包含基准评估。 有关详细信息，请参阅[任务录制器资源](../user-interface/task-recorder.md)。
- 针对所需测试场景为测试用例分组。 有关详细信息，请参阅[创建和自动执行用户接受度测试](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)。

    - 使用 LCS 中的业务流程建模器 (BPM) 为用户接受度测试创建库。
    - 在 Microsoft Azure DevOps Services (Azure DevOps) 中使用 BPM 测试库创建测试计划和测试套件。

高级功能用户可运行用户接受度和集成测试。

- 使用 Regression Suite Automation Tool (RSAT) 运行所需测试套件的测试用例。
- 将测试结果导出到 Azure DevOps，以及使用此服务调查这些结果。

## <a name="prerequisites"></a>先决条件

必须先完成以下先决条件，才能完成本文中的任务：

- 部署支持测试自动化的拓扑。 必须可以访问 **系统管理员** 角色的此拓扑的实例。 此拓扑中必须包含此示例中将使用的演示数据。 有关详细信息，请参阅[部署和使用支持连续生成和测试自动化的环境](../perf-test/continuous-build-test-automation.md)。
- 若要自动运行用户接受度和集成测试，必须在要测试的拓扑中安装 RSAT，并以适当方式配置。 有关如何安装和配置 RSAT 以支持 Finance and Operations 应用程序和 Azure DevOps 的信息，请参阅 [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)。 请注意有关使用此工具的先决条件。 下图显示 RSAT 设置的示例。 蓝色方框中的是用于指定 Azure DevOps 的访问权限的参数。 蓝色方框内的是用于指定实例的访问权限的参数。

    ![RSAT 设置。](media/GER-Configure.png "“RSAT 设置”对话框的屏幕截图")

- 若要组织套件中的测试用例以帮助确保正确的执行顺序，以便收集测试的执行日志来进一步报告和调查，必须可以从部署的拓扑访问 Azure DevOps。
- 若要完成本文中的示例，建议下载 [ER RSAT 测试的用法](https://go.microsoft.com/fwlink/?linkid=874684)。 这个 zip 文件中包含以下任务指南：

    | 内容                                           | 文件名和位置 |
    |---------------------------------------------------|------------------------|
    | 用于为测试准备数据的示例任务录制 | Prepare\\Recording.xml |
    | 用于处理供应商付款的示例任务录制   | Process\\Recording.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>准备应付帐款模块以处理供应商付款

1. 登录您的实例。
2. 从 LCS 下载以下 ER 配置。 有关说明，请参阅 [ER 从 Lifecycle Services 导入配置](./tasks/er-import-configuration-lifecycle-services.md)。

    - **付款模型** ER 模型配置
    - **付款模型映射 1611** ER 模型映射配置
    - **BACS (UK)** ER 格式配置

    ![电子报告配置。](media/GER-Configurations.png "电子申报中的“配置”页的屏幕截图")

3. 选择 **GBSI** 演示数据公司，该公司在英国拥有国家/地区上下文。
4. 配置应付帐款参数：

    1. 转至 **应付帐款 \> 付款设置 \> 付款方式**。
    2. 选择 **电子** 付款方式。
    3. 配置所选付款方式，以便使用您之前下载的 **BACS (UK)** ER 格式处理客户付款：

        1. 在 **文件格式** 快速选项卡上，将 **一般电子导出格式** 选项设置为 **是**。
        2. 在 **导出格式配置** 字段中，选择 **BACS (UK)**。

    ![付款方式页面。](media/GER-APParameters.png "“付款方式”页的屏幕截图")

    > [!NOTE]
    > 如果有为了支持自定义设置而为此 ER 格式创建的派生版本，可以在 **电子** 付款方式中选择此配置。

5. 创建示例供应商付款：

    1. 转到 **应付帐款 \> 付款 \> 付款日记帐**。
    2. 确保尚未过帐付款日记帐。

        ![付款日记帐页面。](media/GER-APJournal.png "“付款日记帐”页的屏幕截图")

    3. 选择 **行**。然后输入包含以下信息的行。

        | 字段               | 示例值   |
        |---------------------|-----------------|
        | 供应商名称         | GB\_SI\_000001  |
        | 借记               | 1,000.00        |
        | 货币            | GBP             |
        | 对方科目类型 | 银行            |
        | 对方科目      | GBSI OPER       |
        | 付款方式   | 电子      |

    ![供应商付款页面。](media/GER-APJournalLines.png "“供应商付款”页的屏幕截图")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>准备 ER 框架以测试供应商付款处理

### <a name="configure-er-parameters"></a>配置 ER 参数

1. 转到 **组织管理 \> 电子报表 \> 电子报表参数**。
2. 在 **附件** 选项卡上 **基准** 字段中，选择 **文件** 作为文档管理 (DM) 框架用于保留作为 DM 附件与基准功能有关的单据的单据类型。

    ![“电子报告参数”页面。](media/GER-ERParameters.png "“电子申报”参数页面的屏幕截图")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>生成与供应商付款有关的单据的基准副本

1. 转到 **应付帐款 \> 付款 \> 付款日记帐**。
2. 选择 **行**。
3. 选择 **生成付款**。
4. 选择 **电子** 付款方式。
5. 选择 **GBSI OPER** 银行帐户。
6. 将 **打印控制报表** 选项设置为 **是**。
7. 将生成的输出作为 zip 文件下载。
8. 打开下载的文件。
9. 从下载的文件提取以下文件：

    - **File** 文本格式的付款文件
    - **ERVendOutPaymControlReport** XLSX 格式的控制报表文件

    ![提取的文件。](media/GER-APJournalProcessed.png "Windows 资源管理器中提取的文件名的屏幕截图")

### <a name="turn-on-the-er-baseline-feature"></a>开启 ER 基准功能

1. 转到 **组织管理 \> 电子申报 \> 配置**。
2. 在操作窗格上的 **配置** 选项卡上，选择 **用户参数**。
3. 将 **以调试模式运行** 选项设置为 **是**。

通过开启 **以调试模式运行** 参数，在执行用于生成传出单据的任何 ER 格式之后强制 ER 框架执行以下操作：

1. 确定是否为所执行 ER 格式的任何组件配置了基准。
2. 确定配置的每个基准（已登录公司的公司代码、生成的输出的文件名和文件扩展名等）在当前条件中是否适用。
3. 对每个适用的基准执行以下操作：

    1. 将执行 ER 格式期间生成的输出与相应基准进行比较。
    2. 将比较结果存储到 ER 配置调试日志中。

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>为供应商付款处理配置 ER 基准

1. 转到 **组织管理 \> 电子申报 \> 配置**。
2. 选择 **基准**。
3. 选择 **新建**。
4. 在 **引用** 字段中，选择 **BACS (UK)** 格式。
5. 选择 **附件**。
6. 为供应商付款文件添加新基准：

    1. 选择 **新建**。
    2. 在 **类型** 字段中，选择您在 ER 参数中配置 DM 文档类型 **文件** 以存储基准项目。
    3. 浏览并选择本地存储的文本格式的付款文件 **File**。
    4. 在 **说明** 字段中，输入 **付款 TXT 文件**。

7. 为供应商付款的控制报表添加新基准：

    1. 选择 **新建**。
    2. 在 **类型** 字段中，选择您在 ER 参数中配置 DM 文档类型 **文件** 以存储基准项目。
    3. 浏览并选择本地存储的 XLSX 格式的 **ERVendOutPaymControlReport** 控制报表文件。
    4. 在 **说明** 字段中，输入 **付款 XLSX 控制报表**。

    ![供应商付款文件和控制报表的基准。](media/GER-BaselineAttachments.png "已选择了付款 XLSX 控制报表的“配置”页的屏幕截图")

8. 关闭该页面。
9. 在 **基准** 快速选项卡上，选择 **新建** 为付款文件配置一个基准：

    1. 将行命名为 **付款文件的基准设置**。
    2. 在 **文件组件名称** 字段中，选择 **文件** 将此基准应用于 ER 格式输出以生成 BACS (UK) 文本格式的付款文件。
    3. 在 **公司** 字段中，选择 **GBSI**，以便在 GBSI 公司中运行 **BACS (UK)** ER 格式时应用此基准。
    4. 在 **文件名掩码** 字段中，输入 **\*.TXT**，以便将此基准仅应用于 **文件** 格式组件的具有 **.txt** 文件扩展名的输出。
    5. 在 **基准** 字段中，选择 **付款 TXT 文件**，以便将此基准用于与生成的输出进行比较。

10. 选择 **新建** 为控制报表配置基准：

    1. 将行命名为 **控制报表的基准设置**。
    2. 在 **文件组件名称** 字段中，选择 **ERVendOutPaymControlReport** 将此基准应用于 ER 格式输出以生成控制报表。
    3. 在 **公司** 字段中，选择 **GBSI**，以便在 GBSI 公司中运行 **BACS (UK)** ER 格式时应用此基准。
    4. 在 **文件名掩码** 字段中，输入 **\*.XLSX**，以便将此基准仅应用于 **ERVendOutPaymControlReport** 格式组件的具有 **.xslx** 文件扩展名的输出。
    5. 在 **基准** 字段中，选择 **付款 XLSX 控制报表**，以便将此基准用于与生成的输出进行比较。

    ![“配置”页面上的“基准”快速选项卡。](media/GER-BaselineRules.png "“配置”页上的“基准”快速选项卡的屏幕截图")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>录制测试以验证供应商付款处理

高级功能用户可录制自己的步骤以测试供应商付款处理。 建议播放（如果需要，并编辑）之前下载的 **Prepare\\Recording.xml** 任务录制。 此录制用于将所有测试数据设置为正确状态。 需要执行此步骤，因为可以多次进行测试，并且每次测试都必须使用同一种状态的数据。

### <a name="reset-user-settings"></a>重置用户设置

1. 打开默认仪表板。
2. 选择 **设置** 按钮（齿轮符号）。
3. 选择 **用户选项**。
4. 选择 **应用数据**。
5. 选择 **重置**。
6. 选择 **是** 确认要重置应用数据。
7. 关闭该页面。

### <a name="record-the-steps-to-prepare-data-for-testing"></a>录制步骤为测试准备数据

1. 选择 **设置** 按钮（齿轮符号）。
2. 选择 **任务录制器**。
3. 选择 **播放录制**。
4. 选择 **从此 PC 中打开**。
5. 选择 **浏览**，然后选择本地保存的 **Prepare\\Recording.xml** 文件。
6. 选择 **开始**。
7. 重复选择 **播放下一个等待步骤**，直到播放完录制中的所有步骤。

此任务录制执行以下操作：

1. 将处理付款行的状态设置为 **无**。

    ![任务录制步骤 3 到 4。](media/GER-Recording1Review1.png "任务录制步骤 3 到 4 的屏幕截图")

2. 开启 **以调试模式运行** ER 用户参数。

    ![任务录制步骤 9 到 10。](media/GER-Recording1Review2.png "任务录制步骤 9 到 10 的屏幕截图")

3. 清除其中包含所生成文件与基准的比较结果的 ER 调试日志。

    ![任务录制步骤 13 到 15。](media/GER-Recording1Review3.png "任务录制步骤 13 到 15 的屏幕截图")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>录制这些步骤以测试供应商付款处理

建议播放（如果需要，并编辑）之前下载的 **Process\\Recording.xml** 任务录制。 此录制用于处理供应商付款和验证生成的单据与相应基准的比较结果。

1. 选择 **设置** 按钮（齿轮符号）。
2. 选择 **任务录制器**。
3. 选择 **播放录制**。
4. 选择 **从此 PC 中打开**。
5. 选择 **浏览**，然后选择本地保存的 **Process\\Recording.xml** 文件。
6. 选择 **开始**。
7. 重复选择 **播放下一个等待步骤**，直到播放完录制中的所有步骤。

此任务录制执行以下操作：

1. 启动供应商付款处理。
2. 选择正确的运行时参数，然后开启控制报表的生成。

    ![任务录制步骤 3 到 8。](media/GER-Recording2Review1.png "任务录制步骤 3 到 8 的屏幕截图")

3. 访问 ER 调试日志以录制所生成输出与相应基准的比较结果。

    在 ER 调试日志中，**生成的文本** 字段中将显示比较结果。 **格式组件** 和 **生成日志条目的格式路径** 字段引用为其比较所生成输出与基准的文件组件。

    ![“电子报告运行日志”页面上的条目。](media/GER-ERDebugLog.png "“电子申报运行日志”页上的条目的屏幕截图")

4. 将使用 **验证** 任务录制器选项和选择 **当前值** 录制当前输出与基准的比较。

    ![使用“验证”选项比较当前值。](media/GER-TRRecordValidation.png "使用“验证”选项比较当前值的屏幕截图")

    下图显示任务录制中录制的验证步骤的情况。

    ![任务录制步骤 13 和 15。](media/GER-Recording2Review2.png "任务录制步骤 13 和 15 的屏幕截图")

## <a name="add-the-recorded-tests-to-azure-devops"></a>将录制的测试添加到 Azure DevOps

1. 打开 Azure DevOps 环境。
2. 选择[配置工具时](#prerequisites)在 RSAT 参数中定义的项目。
3. 选择[配置工具时](#prerequisites)在 RSAT 参数中定义的测试计划。
4. 为所选测试计划创建新测试用例：

    1. 将测试用例命名为 **准备数据以测试供应商对电子付款的处理**。
    2. 附加 **Prepare** 文件夹中您之前下载的 **Recording.xml** 文件。

5. 为所选测试计划创建新测试用例：

    1. 将测试用例命名为 **使用 ER 格式 BACS (UK) 测试对供应商付款的处理**。
    2. 附加 **Process** 文件夹中您之前下载的 **Recording.xml** 文件。

    ![所选测试计划的新测试用例。](media/GER-RSAT-DevOps-Tests-Passed.png "所选测试计划的新测试用例的屏幕截图")

> [!NOTE]
> 注意所添加测试的正确执行顺序。

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>准备 RSAT 以运行录制的测试

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>将测试从 Azure DevOps 加载到 RSAT

1. 打开当前拓扑中的本地 RSAT 应用程序。
2. 选择 **加载** 以将 Azure DevOps 中的当前测试加载到 RSAT 中。

    ![加载到 RSAT 中的测试。](media/GER-RSAT-RSAT-Tests-Loaded.png "加载到 RSAT 中的测试的屏幕截图")

### <a name="create-automation-and-parameters-files"></a>创建自动化和参数文件

1. 在 RSAT 中，选择从 Azure DevOps 加载的测试。
2. 选择 **新建** 以创建 RSAT 自动化和参数文件。

    ![在 RSAT 中创建的 RSAT 自动化和参数文件。](media/GER-RSAT-RSAT-Tests-Initiated.png "在 RSAT 汇总创建的 RSAT 自动化和参数文件的屏幕截图")

### <a name="modify-the-parameters-files"></a>修改参数文件

1. 在 RSAT 中，选择 **准备数据以测试供应商对电子付款的处理** 测试用例。
2. 选择 **编辑**。
3. 在打开的 Microsoft Excel 工作簿中 **General** 工作表上，将公司代码更改为 **GBSI**，因为此公司将用于执行测试。
4. 在 RSAT 中，选择 **使用 ER 格式 BACS (UK) 测试对供应商付款的处理** 测试用例。
5. 选择 **编辑**。
6. 在打开的 Excel 工作簿中 **General** 工作表上，将公司代码更改为 **GBSI**。
7. 请注意，**ERFormatMappingRunLogTable** 工作表上的单元格 A:3 和 C:3 中包含 ER 调试日志表中用于验证输出和基准比较结果的字段的文本。 这些文本将用于评估执行测试期间创建的 ER 调试日志记录。

    ![ERFormatMappingRunLogTable 工作表。](media/GER-RSAT-RSAT-ExcelParameters.png "ERFormatMappingRunLogTable 工作表的屏幕截图")

## <a name="run-the-tests-and-analyze-the-results"></a>执行测试和分析结果

### <a name="run-the-tests-in-rsat"></a>在 RSAT 中运行测试

1. 在 RSAT 中，选择加载的测试。
2. 选择 **运行**。

请注意，将使用 Web 浏览器在应用程序中自动运行测试用例。

### <a name="analyze-the-results-of-test-execution"></a>分析测试的执行结果

测试的执行结果存储在 RSAT 中。 请注意，两项测试均已通过。

![RSAT 中通过的测试。](media/GER-RSAT-RSAT-Tests-Passed.png "RSAT 中通过了的测试的屏幕截图")

请注意，还会将测试的执行结果发送到 Azure DevOps，以便执行进一步的分析。

![Azure DevOps 中的测试执行结果。](media/GER-RSAT-DevOps-Tests-Added.png "Azure DevOps 中的测试执行结果的屏幕截图")

### <a name="simulate-a-situation-where-tests-fail"></a>模拟测试失败的情况

如果生成的输出中至少一个与相应基准不匹配，则此测试套件必定会失败。 若要实现此情况，则可使用 **BACS (UK)** 格式的派生版本，以便生成内容与相应基准不匹配的付款文件。 若要模拟此情况，则可使用同一个 **BACS (UK)** 格式，但更改所处理付款行中的付款金额。

1. 打开应用程序，然后转到 **应付帐款 \> 付款 \> 付款日记帐**。
2. 选择 **行**。
3. 选择付款行，然后选择 **付款状态 \> 无**。
4. 在 **借记** 字段中，将值从 **1,000.00** 更改为 **2,000.00**。
5. 选择 **保存** 以保存您的更改。

### <a name="run-the-tests-in-rsat"></a>在 RSAT 中运行测试

1. 在 RSAT 中，选择加载的测试。
2. 选择 **运行**。

请注意，将使用 Web 浏览器在应用程序中自动运行测试用例。

### <a name="analyze-the-results-of-test-execution"></a>分析测试的执行结果

测试的执行结果存储在 RSAT 中。 请注意，第二次执行时，第二项测试失败。

![RSAT 中的失败测试结果。](media/GER-RSAT-RSAT-Tests-Failed.png "RSAT 中的失败测试结果的屏幕截图")

请注意，还会将测试的执行结果发送到 Azure DevOps，以便执行进一步的分析。

![Azure DevOps 中的失败测试结果。](media/GER-RSAT-DevOps-Tests-Failed.png "Azure DevOps 中的失败测试结果的屏幕截图")

可访问每个测试的状态。 也可以访问执行日志，以便分析任何失败的原因。 在下图中，执行日志显示失败的原因是所生成付款文件与其基准之间内容不同。

![Azure DevOps 中用于分析失败的执行日志。](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Azure DevOps 中用于分析失败原因的执行日志的屏幕截图")

因此，如您所见，可以通过将 RSAT 用作测试平台和使用基于任务录制器且使用 ER 基准功能的测试用例自动评估任何 ER 格式的运行。

## <a name="additional-resources"></a>其他资源

- [任务录制器资源](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [创建和自动执行用户接受度测试](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [部署和使用支持连续生成和测试自动化的环境](../perf-test/continuous-build-test-automation.md)
- [跟踪生成的报表结果并将其与基准值进行比较](er-trace-reports-compare-baseline.md)
- [ER 通过采用该格式的新的基本版本升级格式](tasks/er-upgrade-format.md)
- [ER 从 Lifecycle Services 导入配置](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]