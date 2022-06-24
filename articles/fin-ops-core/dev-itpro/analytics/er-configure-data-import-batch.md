---
title: 以批处理模式从手动选择的文件中导入数据
description: 本文介绍如何在批处理模式下从手动选择的文件导入数据。
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 2dec838439876fd8e57ea4a7078d97267e5ea1a2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890174"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>以批处理模式从手动选择的文件中导入数据

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

要使用[电子报告 (ER)](general-electronic-reporting.md) 框架以批处理模式从手动选择的传入文件导入数据，请配置支持导入的 ER [格式](er-overview-components.md#format-component)。 然后运行使用该格式作为数据源的 **截止目标** 类型的[模型映射](er-overview-components.md#model-mapping-component)。 要导入数据，浏览到要导入的文件，然后手动选择它。 

支持以批处理模式导入数据的新 ER 功能支持将此过程配置为无人参与。 您可以通过从 ER 用户界面 (UI) 计划新的批处理作业来使用 ER 配置执行数据导入。

本文介绍如何以批处理方式从手动选择的文件完成数据导入。 示例将供应商交易记录用作业务数据。 这些示例的步骤可以在 **USMF** 公司完成。 无需进行编码。

## <a name="prerequisites"></a>先决条件

要完成本文中的示例，您必须具有以下访问权限：

- 以下其中一个角色：

    - 电子报告开发人员
    - 电子报告功能顾问
    - 系统管理员

- 1099 付款的 ER 格式和模型配置

### <a name="create-the-required-er-configurations"></a>创建所需的 ER 配置

要创建所需的 ER 配置并满足其他先决条件，请按照以下步骤之一操作：

- 播放 **ER 从 Microsoft Excel 文件导入数据** 任务指南，该任务指南属于 **7.5.4.3 获取/开发 IT 服务/解决方案产品 (10677)** 业务流程。 这些任务指南将引导您完成设计和使用以交互方式从 Microsoft Excel 文件导入供应商交易记录的 ER 配置的过程。 有关详细信息，请参阅[分析 Excel 格式的传入文档](parse-incoming-documents-excel.md)。
- 完成[配置从 SharePoint 的数据导入](er-configure-data-import-sharepoint.md)中的示例。 这些示例将引导您完成设计和使用以交互方式从存储在 SharePoint 文件夹中的 Excel 文件导入供应商交易记录的 ER 配置的过程。

### <a name="download-the-required-er-configurations"></a>下载所需的 ER 配置

1. 下载以下 ER 配置，并将其保存在本地。

    | 内容描述 | 文件 |
    |---------------------|------|
    | **1099 付款模型** ER 数据模型配置 | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **用于导入供应商交易 (Excel)** ER 格式配置 | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. 使用[从 XML 文件加载](er-defer-sequence-element.md#import-the-sample-er-configurations) ER 选项按以下顺序将下载的 ER 配置导入您的 Dynamics 365 Finance 实例：

    1. ER 数据模型配置
    2. ER 格式配置

### <a name="download-the-required-excel-files"></a>下载所需的 Excel 文件

- 下载以下示例数据集，并将其保存到本地。

    | 内容描述 | 文件 |
    |---------------------|------|
    | 包含要导入的示例数据的传入 **1099import-data.xlsx** 文件 | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>查看先决条件

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，查看为以批处理模式导入数据准备的 ER 解决方案。
3. 查看 **用于导入供应商交易记录 (Excel)** 格式配置。

    - 此配置的格式组件用于分析传入 Excel 文件。
    - 此配置的模型映射组件用于使用分析的 Excel 文件中的数据填充基础数据模型。

    ![用于从 ER UI 以批处理模式导入数据的 ER 格式配置。](./media/er-configure-data-import-batch-configurations-1.png)

4. 查看 **1099 付款模型** 数据模型配置。

    - 此配置的模型组件表示用于在运行的 ER 组件之间传递数据的数据模型的结构。
    - 此配置的模型映射组件用于从已执行格式组件中拉取数据，然后更新应用程序表。

    ![用于从 ER UI 以批处理模式导入数据的 ER 数据模型配置。](./media/er-configure-data-import-batch-configurations-2.png)

5. 在 Excel 中打开 **1099import-data.xlsx** 文件。

    ![包含要以批处理模式导入的数据的示例 Excel 文件。](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>启用从 UI 批次导入 ER 数据

1. 转到 **系统管理** \> **工作区** \> **功能管理**。
2. 在 **功能管理** 工作区中，选择 **批量对手动上传的文档运行电子报告导入** 功能，然后选择 **立即启用**。

## <a name="import-data-from-manually-selected-excel-files"></a>从手动选择的 Excel 文件导入数据

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页面上，选择 **1099 付款模型** 数据模型配置。
3. 在 **配置组件** 快速选项卡上，选择 **用于 1099 手动交易记录导入** 链接。
4. 在 **模型到数据源映射** 页面上，已预先选择了 **用于 1099 手动交易记录导入** 模型映射。 选择 **运行**。
5. 在 **参数** 选项卡上，选择 **浏览**。 找到并选择 **1099import-data.xlsx** 文件，然后选择 **确定**。
6. 在 **输入凭证 ID** 字段中，输入 **V-00001**。
7. 在 **在后台运行** 选项卡上，将 **批处理** 选项设置为 **是**。

    请注意，**任务描述** 字段已设置为 **运行模型映射“用于 1099 手动交易记录导入”，配置“1099 付款模型”**。 此值表示所选模型映射的执行将计划为新批处理作业。

    ![在“电子报告参数”对话框中指定批处理模式数据导入的详细信息。](./media/er-configure-data-import-batch-execution-parameters.png)

8. 选择 **确定**。 一条消息将通知您已计划新的批处理作业。

    ![有关“模型到数据源映射”页上的新计划批处理作业的消息。](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>查看批处理作业页上的数据导入结果

1. 转到 **通用** \> **查询** \> **批处理作业** \> **我的批处理作业**。
2. 在 **批处理作业** 页上，筛选批处理作业列表以查找计划的批处理，然后选择它。
3. 选择 **作业 ID** 链接可查看作业详细信息。
4. 在 **批处理任务** 快速选项卡中，选择 **日志**。

    ![批处理作业页上的“日志”按钮。](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. 查看执行详细信息。

    ![批处理作业页上计划的批处理作业的执行日志。](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>更改数据导入参数

计划批处理后，如果它还未运行，您可以更改计划的数据导入的参数。

1. 转到 **通用** \> **查询** \> **批处理作业** \> **我的批处理作业**。
2. 在 **批处理作业** 页上，筛选批处理作业列表以查找计划的批处理，然后选择它。
3. 选择 **更改状态**。
4. 在 **选择新状态** 对话框中，选择 **保留**，然后选择 **确定**。
5. 选择 **作业 ID** 链接可访问作业详细信息。
6. 在 **批处理任务** 快速选项卡中，选择 **参数**。
7. 在 **电子报告参数** 对话框中，按照以下步骤操作：

    1. 选择 **浏览** 为数据导入选择替代文件。
    2. 选择 **输入凭证 ID** 更改用于导入供应商交易记录的凭证号。

        ![更改电子报告参数对话框中计划批处理作业的数据导入参数。](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. 选择 **确定**。

8. 请确保仍然选择该批处理，然后再次选择 **更改状态**。
9. 在 **选择新状态** 对话框中，选择 **等待**，然后选择 **确定**。

## <a name="review-the-data-import-results-on-the-er-source-page"></a>查看 ER 来源页面上的数据导入结果

1. 转到 **组织管理** \> **电子报告** \> **电子报告来源**。
2. 选择在数据导入期间自动创建的 **用于导入供应商交易记录 (Excel)** 记录。

    ![电子报告来源页上“用于导入供应商交易记录 (Excel)”配置的记录。](./media/er-configure-data-import-batch-files-source-1.png)

3. 选择 **来源的文件状态**。
4. 在 **文件** 和 **导入格式的来源日志** 快速选项卡上，查看导入详细信息。
5. 在 **文件** 快速选项卡上，选择记录。 请注意，导入的文件将附加到此记录。

    ![附加到“来源的文件状态”页面的记录的导入文件。](./media/er-configure-data-import-batch-files-source-2.png)

6. 选择 **附件** 可查看导入的文件。

    ![文档视图页上的导入文件。](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > 为保留这些附件，ER 框架在 ER 参数的 **Others** 字段中使用为当前公司[设置](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)的文档类型。

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>查看“用于 1099 的供应商结算”页面上的数据导入结果

1. 转到 **应付帐款** \> **定期任务** \> **1099 税** \> **用于 1099 的供应商结算**。
2. 在 **开始日期** 字段中输入 **12/31/2017**（2017 年 12 月 31 日）。
3. 选择 **手动 1099 交易记录**。

    ![1099 税交易记录页上的导入的供应商交易记录。](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
