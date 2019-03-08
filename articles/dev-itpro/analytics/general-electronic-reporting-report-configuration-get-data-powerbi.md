---
title: 配置电子申报 (ER) 以便将数据导入 Power BI
description: 本主题说明您可以如何使用您的电子申报 (ER) 配置安排数据从您的 Finance and Operations 实例转移至 Power BI 服务。
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
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
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e2d3c03a75fd03dfd3a96a181eff20f934546ec4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "335776"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>配置电子申报 (ER) 以便将数据导入 Power BI

[!include [banner](../includes/banner.md)]

本主题说明您可以如何使用您的电子申报 (ER) 配置安排数据从您的 Finance and Operations 实例转移至 Power BI 服务。 例如，本主题使用内部统计交易记录作为必须转移的业务数据。 Power BI 地图可视化使用此内部统计交易记录数据显示 Power BI 报表上的公司导入/导出活动的分析视图。

## <a name="overview"></a>概览

Microsoft Power BI 是一组软件服务、应用程序和连接器的集合，它们共同将外部数据源转换为一致、直观和交互的见解。 电子申报 (ER) 允许 Microsoft Dynamics 365 for Finance and Operations 用户轻松配置数据源和安排数据从 Finance and Operations 转移到 Power BI。 数据作为 OpenXML 工作表（Microsoft Excel 工作簿文件）格式的文件传输。 转移的文件存储在为该目的而配置的 Microsoft SharePoint Server 上。 存储的文件在 Power BI 中用来制作包含可视化项（表格、图标、地图等）的报表。 Power BI 报表与 Power BI 用户共享，因为他们在 Power BI 仪表板和 Finance and Operations 页面上访问。 本主题对以下任务进行解释：

- 配置 Finance and Operations。
- 准备您的 ER 格式配置，以从 Finance and Operations 获取数据。
- 配置将数据转移至 Power BI 的 ER 环境。
- 使用转移的数据创建 Power BI 报表。
- 使 Power BI 报表在 Finance and Operations 中可访问。

## <a name="prerequisites"></a>先决条件
要完成本主题中的示例，您必须具有以下访问权限：

- 访问 Finance and Operations 的以下其中一个角色：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

- 访问为了与 Finance and Operations 一起使用而配置的 SharePoint Server
- 访问 Power BI 框架

## <a name="configure-document-management-parameters"></a>配置文档管理参数
1. 在**文档管理参数**页面上，配置您登录的公司中使用的 SharePoint Server 访问权限为（在此示例中为 DEMF 公司）。
2. 测试与 SharePoint Server 的连接性，确保您已被授予访问权限。

    [![文档管理参数页面](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. 打开配置的 SharePoint 站点。 创建 ER 将存储 Excel 文件的新文件夹，这些 Excel 文件中含有 Power BI 报表要求用作 Power BI 数据集源的业务数据。
4. 在 Finance and Operations 中的**文档类型**页面上创建将用来访问您刚才创建的 SharePoint 文件夹的新文档类型。 在**组**字段中输入**文件**，在**位置**字段中输入 **SharePoint**，然后输入 SharePoint 文件夹的地址。

    [![文档类型页面](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>配置 ER 参数
1. 在**电子申报**工作区中，单击**电子申报参数**链接。
2. 在**附件**选项卡上，对所有字段选择**文件**文档类型。
3. 在**电子申报**工作区中，通过单击**设置有效**使所需的提供商有效。 有关详细信息，请播放**ER 选择服务提供商**任务指南。

## <a name="use-an-er-data-model-as-the-source-of-data"></a>使用 ER 数据模型作为数据源
您必须具有作为业务数据源在 Power BI 报表上使用的 ER 数据模型。 此数据模型从 ER 配置库上载。 有关详细信息，请参阅[从 Lifecycle Services 下载电子申报配置](download-electronic-reporting-configuration-lcs.md)或播放**ER 从 Lifecycle Services 导入配置**任务指南。 选择**内部统计**作为从选定的 ER 配置库中上载的数据模型。 （在此示例中，使用模型的版本 1。）然后可以访问**配置**页面上的**内部统计** ER 模型配置。

[![配置页面](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>设计 ER 格式配置
您必须创建使用**内部统计**数据模型作为业务数据源的新 ER 格式配置。 此格式配置必须将输出结果生成为 OpenXML（Excel 文件）格式的电子文档。 有关详细信息，请播放**ER 创建 OPENXML 格式的报表配置**任务指南。 将新配置命名为**导入/导出活动**，如下图所示。 使用[ER 数据导入和导出详细信息](https://go.microsoft.com/fwlink/?linkid=845208)Excel 文件作为设计 ER 格式时的模板。 （有关如何导入格式模板的信息，请播放任务指南。）

[![导入/导出活动配置](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

要修改**导入/导出活动**格式配置，请执行以下步骤。

1. 单击**设计器**。
2. 在**格式**选项卡上，将此格式的文件元素命名为**Excel 输出文件**。

    [![Excel 输出文件元素](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. 在**映射**选项卡上，指定在任何时候运行此格式时将生成的 Excel 文件名。 将相关表达式配置为返回值**导入和导出详细信息**（将自动添加 .xlsx 文件扩展名）。

    [![格式设计器](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. 为此格式添加新的数据源项目。 （进一步绑定数据将需要此枚举。）

    1. 将数据源命名为 **direction\_enum**。
    2. 选择**数据模型枚举**作为数据源类型。
    3. 请参阅**方向**数据模型枚举。

    [![direction_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. 完成**内部统计**数据模型元素与设计格式元素的绑定，如下图所示。

    [![完成绑定](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

在运行后，ER 格式将生成 Excel 格式的输出结果。 它将内部统计交易记录的详细信息发送至输出结果，并通过将交易记录描述为导入活动或导出活动的方式对它们进行区分。 单击**运行**为**内部统计**页面上的内部统计交易记录列表测试新的 ER 格式（**税金** &gt; **申报** &gt; **外贸** &gt; **内部统计**）。

[![内部统计页面](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

生成以下输出结果。 文件命名为**导入和导出详细信息.xlsx**，正如您在格式设置中所指定的。

[![导入和导出详细信息.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>配置 ER 目标
您必须将 ER 框架配置为以特殊方式发送新 ER 格式配置的输出结果。

- 输出结果必须发送至选定的 SharePoint Server 的文件夹。
- 每次执行格式配置必须创建相同 Excel 文件的新版本。

在**电子申报**页面（**组织管理** &gt; **电子申报**）上，单击**电子申报目标**项目，然后添加新目标。 在**参考**字段中，选择您之前创建的**导入/导出活动**格式配置。 按照以下步骤为参考添加新的文件目标记录。

1. 在**命名**字段中，输入文件目标的标题。
2. 在**文件名**字段中，为 Excel 文件格式组件选择名称**Excel 输出文件**。

单击新目标记录的**设置**按钮。 然后在**目标设置**对话框中执行以下步骤。

1. 在 **Power BI** 选项卡上，将**已启用**选项设置为**是**。
2. 在 **SharePoint** 字段中，选择您先前创建的**共享**文档类型。

## <a name="schedule-execution-of-the-configured-er-format"></a>计划配置的 ER 格式的执行
1. 在**配置**页面（**组织管理** &gt; **电子申报** &gt; **配置**）上的配置树中，选择您先前创建的**导入/导出活动**配置。
2. 将版本 1.1 的状态从**草稿**更改为**完成**，使此格式可使用。

    [![配置页面](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. 选择**导入/导出活动**配置的已完成版本，然后点击**运行**。 注意配置目标应用到以 Excel 格式生成的输出结果。
4. 将**批处理**选项设置为**是**，从而以未看管模式运行此报表。
5. 单击**重复执行**以计划此批处理执行所需的重复周期。 重复周期定义了更新数据从 Finance and Operations 转移至 Power BI 的频率。

    [![电子报表参数对话框](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. 在配置后，您可以在**批处理作业**页面上找到 ER 报表执行作业（**系统管理 &gt; 查询 &gt; 批处理作业**）。

    [![批处理作业页面](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. 第一次运行此作业时，目标创建的新 Excel 文件具有在选定的 SharePoint 文件夹中配置的名称。 以后每次运行作业时，目标都会创建此 Excel 文件的新版本。

    [![Excel 文件的新版本](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>使用 ER 格式的输出结果创建 Power BI 数据集
1. 登录 Power BI，打开现有 Power BI 组（工作区）或新建组。 单击**导入或连接数据**部分的**文件**下的**添加**，或者单击左窗格中的**数据集**旁边的加号 (**+**)。

    [![创建数据集](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. 选择 **SharePoint - 团队站点**选项，然后输入您正在使用的 SharePoint Server 的路径（在我们的示例中为 `https://ax7partner.litware.com`）。
3. 浏览到 **/Shared Documents/GER data/PowerBI** 文件夹，再选择您作为新 Power BI 数据集的数据源创建的 Excel 文件。

    [![选择 Excel 文件](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. 单击**连接**，然后单击**导入**。 基于选择的 Excel 文件创建新的数据集。 数据集也可以自动添加到新创建的仪表板。

    [![仪表板上的数据集](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. 为此数据集配置强制定期更新的刷新计划。 定期更新允许通过定期执行 ER 报表来自 Finance and Operations 的新业务数据通过在 SharePoint Server 上创建的 Excel 文件的新版本消耗。

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>使用新的数据集创建 Power BI 报表
1. 单击您创建的**导入和导出详细信息** Power BI 数据集。
2. 配置可视化。 例如，选择**填充的地图**可视化，然后进行以下配置：

    - 将**CountryOrigin**数据集字段分配到地图可视化的**位置**字段。
    - 将**量**数据集字段分配到地图可视化的**色饱和度**字段。
    - 将**活动**和**年度**数据集字段添加到地图可视化的**筛选器**字段集合。

3. 将 Power BI 报表保存为**导入和导出详细报表**。

    [![导入和导出详细报表](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    注意地图显示 Excel 文件中提及的国家/地区（在此示例中为奥地利和瑞士）。 这些国家/地区通过颜色显示每个国家/地区开票金额的比例。

4. 更新内部统计交易记录列表。 添加由意大利发起的导出交易记录。

    [![内部统计交易记录列表](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. 等待下一次计划的 ER 报表执行和下一次计划的 Power BI 数据集更新。 然后查看 Power BI 报表（选择仅显示导入交易记录）。 更新地图现在仅显示意大利。

    [![更新地图](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance-and-operations"></a>访问 Finance and Operations 中的 Power BI 报表
设置 Finance and Operations 与 Power BI 之间的集成。 有关详细信息，请参阅[配置工作区的 Power BI 集成](configure-power-bi-integration.md)。

1. 在支持 Power BI 集成的**电子申报**工作区页面上（**组织管理** &gt; **工作区s** &gt; **电子申报工作区**），单击**选项** &gt; **打开报表目录**。
2. 选择您创建的**导入和导出详细信息** Power BI 报表使报表在选择的页面上显示为操作项。
3. 单击操作项以打开显示您在 Power BI 中设计的报表的 Finance and Operations 页面。

    [![导入和导出详细报表](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>其他资源

[电子申报目标](electronic-reporting-destinations.md)

[电子申报概览](general-electronic-reporting.md)
