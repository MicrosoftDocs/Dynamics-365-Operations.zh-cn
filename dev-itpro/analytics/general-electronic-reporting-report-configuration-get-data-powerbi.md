---
title: "提供 Power BI 的安装电子国家/地区报告与从 Dynamics 365 的工序数据。"
description: "本主题说明您可以如何使用您的电子申报 (ER) 配置安排数据从您的 Dynamics 365 for Operations 实例转移至 Power BI 服务。 例如，本主题使用内部统计交易记录作为必须转移的业务数据。 Power BI 地图可视化使用此内部统计交易记录数据显示 Power BI 报表上的公司导入/导出活动的分析视图。"
author: kfend
manager: AnnBe
ms.date: 2016-10-31 13 - 22 - 29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ed0192c44b6d7e88120c64e539ebb0ac3b379831
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-electronic-reporting-to-provide-power-bi-with-data-from-dynamics-365-for-operations"></a>提供 Power BI 的安装电子国家/地区报告与从 Dynamics 365 的工序数据。

本主题说明您可以如何使用您的电子申报 (ER) 配置安排数据从您的 Dynamics 365 for Operations 实例转移至 Power BI 服务。 例如，本主题使用内部统计交易记录作为必须转移的业务数据。 Power BI 地图可视化使用此内部统计交易记录数据显示 Power BI 报表上的公司导入/导出活动的分析视图。

<a name="overview"></a>概览
--------

Microsoft Power BI 是一组软件服务、应用程序和连接器的集合，它们共同将外部数据源转换为一致、直观和交互的见解。 电子申报 (ER) 允许 Microsoft Dynamics 365 for Operations 用户轻松配置数据源和安排数据从 Dynamics 365 for Operations 转移到 Power BI。 数据作为 OpenXML 工作表（Microsoft Excel 工作簿文件）格式的文件传输。 转移的文件存储在为该目的而配置的 Microsoft SharePoint Server 上。 存储的文件在 Power BI 中用来制作包含可视化项（表格、图标、地图等）的报表。 Power BI 报表与 Power BI 用户共享，因为他们在 Power BI 仪表板和 Dynamics 365 for Operations 页面上访问。 本主题对以下任务进行解释：

-   配置 Dynamics 365 for Operations。
-   准备您的 ER 格式配置，以从 Dynamics 365 for Operations 获取数据。
-   配置将数据转移至 Power BI 的 ER 环境。
-   使用转移的数据创建 Power BI 报表。
-   制作可在 Dynamics 365 for Operations 中访问的 Power BI 报表。

## <a name="prerequisites"></a>先决条件
要完成本主题中的示例，您必须具有以下访问权限：

-   访问 Dynamics 365 for Operations 的以下其中一个角色：
    -   电子申报开发人员
    -   电子申报功能顾问
    -   系统管理员
-   访问为了与 Dynamics 365 for Operations 一起使用而配置的 SharePoint Server
-   访问 Power BI 框架

## <a name="configure-document-management-parameters"></a>配置文档管理参数
1.  在**文档管理参数**页面上，配置您登录的公司中使用的 SharePoint Server 访问权限为（在此示例中为 DEMF 公司）。
2.  测试与 SharePoint Server 的连接性，确保您已被授予访问权限。 文档管理参数![[] (页面。高级/media/ger BI SharePoint 服务器安装 1024x369.png)](。高级/media/ger BI SharePoint setting.png 服务器)
3.  打开配置的 SharePoint 站点。 创建 ER 将存储 Excel 文件的新文件夹，这些 Excel 文件中含有 Power BI 报表要求用作 Power BI 数据集源的业务数据。
4.  在 Dynamics 365 for Operations 中的“**文档类型**”页面上创建将用来访问您刚才创建的 SharePoint 文件夹的新文档类型。 在“**组**”字段中输入“**文件**”，在“**位置**”字段中输入“**SharePoint**”，然后输入 SharePoint 文件夹的地址。 [] (![文档类型页心。高级/media/ger BI SharePoint 文档类型 1024x485.png)](。高级/media/ger BI SharePoint 文档 type.png)

## <a name="configure-er-parameters"></a>配置 ER 参数
1.  在“**电子申报**”工作区中，单击“**电子申报参数**”链接。
2.  在“**附件**”选项卡上，对所有字段选择“**文件**”文档类型。
3.  在“**电子申报**”工作区中，通过单击“**设置有效**”使所需的提供商有效。 有关详细信息，请播放“**ER 选择服务提供商**”任务指南。

## <a name="use-an-er-data-model-as-the-source-of-data"></a>使用 ER 数据模型作为数据源
您必须具有作为业务数据源在 Power BI 报表上使用的 ER 数据模型。 此数据模型从 ER 配置库上载。 有关详细信息，请参阅“[从 Lifecycle Services 下载电子申报配置](download-electronic-reporting-configuration-lcs.md)”或播放“**ER 从 Lifecycle Services 导入配置**”任务指南。 选择**内部统计**作为从选定的 ER 配置库中上载的数据模型。 (在此示例中，这 1 使用模型的版本。) 然后可以在配置** **访问页面的内部统计 ER ** **模型配置。 [] (![配置"页面。高级/media/ger BI 数据模型 1024x371.png)](。高级/media/ger BI 数据 model.png)

## <a name="design-an-er-format-configuration"></a>设计 ER 格式配置
您必须创建使用**内部统计**数据模型作为业务数据源的新 ER 格式配置。 此格式配置必须将输出结果生成为 OpenXML（Excel 文件）格式的电子文档。 有关详细信息，请播放“**ER 创建 OPENXML 格式的报表配置**”任务指南。 将新配置命名为“**导入/导出活动**”，如下图所示。 使用“[ER 数据导入和导出详细信息](https://go.microsoft.com/fwlink/?linkid=845208)”Excel 文件作为设计 ER 格式时的模板。 有关如何导入格式模板的信息，请播放 (，任务指南。)![导入导出/[] (配置活动媒体热镇/高级格式 configuration.png)] BI 媒体 (/热镇 BI 高级格式) configuration.png 修改**导出/导入活动**配置格式，请执行以下步骤。

1.  单击“设计器”****。
2.  在“**格式**”选项卡上，将此格式的文件元素命名为“**Excel 输出文件**”。 [![Excel 输出文件] (元素。高级格式/media/ger BI 配置文件 1024x395.png)] 元素名称 (。高级格式/media/ger BI 配置文件 name.png 元素)
3.  在“**映射**”选项卡上，指定在任何时候运行此格式时将生成的 Excel 文件名。 将相关表达式配置为返回值“**导入和导出详细信息**”（将自动添加 .xlsx 文件扩展名）。 [![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  为此格式添加新的数据源项目。 （进一步绑定数据将需要此枚举。）
    1.  给定数据源**方向\_枚举**。
    2.  选择“**数据模型枚举**”作为数据源类型。
    3.  请参阅“**方向**”数据模型枚举。

    [] (![方向\_枚举。高级格式映射配置/media/ger BI 添加枚举 1024x454.png)](。高级格式映射配置/media/ger BI 添加 enum.png)
5.  完成“**内部统计**”数据模型元素与设计格式元素的绑定，如下图所示。 [] (![绑定完成的。高级格式映射/media/ger BI 配置详细信息 1024x454.png)](。高级/media/ger BI 配置格式映射 details.png)

在运行后，ER 格式将生成 Excel 格式的输出结果。 它将内部统计交易记录的详细信息发送至输出结果，并通过将交易记录描述为导入活动或导出活动的方式对它们进行区分。 **测试内部统计交易记录列表中为新的 ER 格式单击"运行** **在内部统计**的页面 (** ** &gt; **税申报** &gt; **外贸** &gt; ** **内部统计。) [] (内部统计![页面。高级格式/media/ger BI 运行测试交易记录 1024x322.png)](。高级格式/media/ger BI 运行测试) transactions.png 以下结果生成输出。 文件命名为“**导入和导出详细信息.xlsx**”，正如您在格式设置中所指定的。 [![导入和导出 details.xlsx] (。高级格式/media/ger BI 运行测试 1024x472.png)] 输出 (。高级格式/media/ger BI 运行测试 output.png)

## <a name="configure-the-er-destination"></a>配置 ER 目标
您必须将 ER 框架配置为以特殊方式发送新 ER 格式配置的输出结果。

-   输出结果必须发送至选定的 SharePoint Server 的文件夹。
-   每次执行格式配置必须创建相同 Excel 文件的新版本。

**在电子国家/地区报告**页面 (**组织管理** &gt; **电子国家/地区报告**)，请单击"电子目标** **国家/地区报告物料，并且添加新目标。 在“**参考**”字段中，选择您之前创建的“**导入/导出活动**”格式配置。 按照以下步骤为参考添加新的文件目标记录。

1.  在“**命名**”字段中，输入文件目标的标题。
2.  在“**文件名**”字段中，为 Excel 文件格式组件选择名称“**Excel 输出文件**”。

单击新目标记录的“**设置**”按钮。 然后在“**目标设置**”对话框中执行以下步骤。

1.  在“**Power BI**”选项卡上，将“**启用**”选项设置为“**是**”。
2.  在“**SharePoint**”字段中，选择您先前创建的“**共享**”文档类型。

## <a name="schedule-execution-of-the-configured-er-format"></a>计划配置的 ER 格式的执行
** **在配置"页上 (**组织管理** &gt; **电子国家/地区报告** &gt; ** **配置)，在配置此该树中，选择您之前创建的导出/活动** **导入配置。 将版本 1.1 的状态从“**草稿**”更改为“**完成**”，使此格式可使用。 [] (![配置"页面。高级格式/media/ger BI 配置完全 1024x401.png)](。高级格式/media/ger BI 配置 complete.png) 选中**导出/导入配置活动**已完成版本，然后单击** **运行。 注意配置目标应用到以 Excel 格式生成的输出结果。 将“**批处理**”选项设置为“**是**”，从而以未看管模式运行此报表。 单击“**重复执行**”以计划此批处理执行所需的重复周期。 重复周期定义了更新数据从 Dynamics 365 for Operations 转移至 Power BI 的频率。 电子![[] (国家/地区报告参数对话框。高级格式/media/ger BI 配置运行对计划 1024x413.png)](。{{/media/ger:/media/ger-power-bi-format-configuration-run-to-schedule.png}} {{高级：/media/ger-power-bi-format-configuration-run-to-schedule.png}} {{双：/media/ger-power-bi-format-configuration-run-to-schedule.png}} {{格式：/media/ger-power-bi-format-configuration-run-to-schedule.png}} {{配置：/media/ger-power-bi-format-configuration-run-to-schedule.png}} {{运行：/media/ger-power-bi-format-configuration-run-to-schedule.png}} {{对：/media/ger-power-bi-format-configuration-run-to-schedule.png}} {{schedule.png:/media/ger-power-bi-format-configuration-run-to-schedule.png}})，才能配置后，可以查找在** **页面批处理作业的 ER 报表执行的工作 (**系统管理查询 &gt; **批 &gt; 处理作业)。 批处理作业![[] (页面。高级格式/media/ger BI 配置运行作业 1024x410.png)](。高级格式/media/ger BI 配置为运行 job.png)，当这第一次运行作业，则目标创建具有配置的名称中选择文件夹的新的 SharePoint 的 Excel 文件。 以后每次运行作业时，目标都会创建此 Excel 文件的新版本。 [Excel 文件的![] (新版本。高级/media/ger BI 输出文件在 SharePoint 服务器文件夹 1024x412.png /media/ger)](。高级/media/ger BI 输出文件在 SharePoint 服务器文件夹 2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>使用 ER 格式的输出结果创建 Power BI 数据集
登录 Power BI，打开现有 Power BI 组（工作区）或新建组。 **单击下添加** ** **文件在**请导入或连接到数据**部分或单击加号 (+** **)。{{旁边：next_to}} ** **数据集在左窗格。 [] (![数据集创建的。高级/media/ger BI 添加 1024x524.png)] 数据集 (。高级/media/ger BI 添加 dataset.png) 选中** SharePoint –团队网站**选项，然后输入您使用 SharePoint Server 的路径在 (**我们的示例中的 https://ax7partner.spoppe.com**)。 然后浏览到 **/Shared Documents/GER data/PowerBI** 文件夹，再选择您作为新 Power BI 数据集的数据源创建的 Excel 文件。 选择 Excel 文件的![[] (。/media/ger 数据集-高级 BI 添加 Excel 文件 1024x522.png)](。高级/media/ger BI 添加 Excel) file.png 数据集-单击连接** **，然后单击"导入** **。 基于选择的 Excel 文件创建新的数据集。 数据集也可以自动添加到新创建的仪表板。 ["仪表板的![数据集] (。高级/media/ger BI 添加 1024x489.png)] 数据集 (。高级/media/ger BI 添加 dataset.png) 配置此数据集的刷新计划必须定期更新。 定期更新允许通过定期执行 ER 报表来自 Dynamics 365 for Operations 的新业务数据通过在 SharePoint Server 上创建的 Excel 文件的新版本消耗。

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>使用新的数据集创建 Power BI 报表
要创建新的 Power BI 报表，单击您创建的“**导入和导出详细信息**”Power BI 数据集。 然后配置可视化。 例如，选择“**填充的地图**”可视化，然后进行以下配置：

-   将“**CountryOrigin**”数据集字段分配到地图可视化的“**位置**”字段。
-   将“**量**”数据集字段分配到地图可视化的“**色饱和度**”字段。
-   将“**活动**”和“**年度**”数据集字段添加到地图可视化的“**筛选器**”字段集合。

将 Power BI 报表保存为“**导入和导出详细报表**”。 [![导入和导出] (明细报表。高级/media/ger BI 添加报表 1024x498.png)](。高级/media/ger BI 添加的注释 report.png) 表显示在 Excel 文件中提及的国家/地区 (奥地利和瑞士本示例中。) 这些国家/地区通过颜色显示每个国家/地区开票金额的比例。 更新内部统计交易记录列表。 添加由意大利发起的导出交易记录。 内部![[] (统计交易记录的列表。高级/media/ger BI 新运行新交易记录 1024x321.png)](。高级/media/ger BI 新运行新 transaction.png) 请等待 ER 报表和 Power BI 的数据集下一个计划更新的下一次编制计划时执行。 然后查看 Power BI 报表（选择仅显示导入交易记录）。 更新地图现在仅显示意大利。 [] (![更新的映射。高级/media/ger BI 新执行新的映射 1024x511.png)](。高级/media/ger BI 新运行新 map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>在 Dynamics 365 for Operations 中访问 Power BI 报表
设置 Dynamics 365 for Operations 与 Power BI 之间的集成。 有关详细信息，请参阅“[配置工作区的 Power BI 集成](configure-power-bi-integration.md)”。 **在电子国家/地区报告**工作区支持"页上 Power BI 集成 (** ** &gt; **组织管理工作区** &gt; **电子国家/地区报告工作区**)，单击"选项** &gt; ** **目录**打开报表。 选择您创建的“**导入和导出详细信息**”Power BI 报表使报表在选择的页面上显示为操作项。 单击操作项以打开显示您在 Power BI 中设计的报表的 Dynamics 365 for Operations 页面。 [![导入和导出] (明细报表。高级/media/ger BI 查看 BI 报表在 AX 1024x586.png] 窗体)(。高级/media/ger BI 查看 BI 报表在 AX form.png)

<a name="see-also"></a>请参阅
--------

[电子申报目标](electronic-reporting-destinations.md)

[电子申报概览](general-electronic-reporting.md)


