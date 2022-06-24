---
title: 设计新的 ER 解决方案打印自定义报表
description: 本文说明如何设计电子报告 (ER) 解决方案来打印自定义报表。
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7194fa9243362d4eb61d6ce706e30a66c9cf3217
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847479"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>设计新的 ER 解决方案打印自定义报表

[!include[banner](../includes/banner.md)]

以下步骤说明了具有系统管理员、电子报告开发人员或电子报告功能顾问角色的用户如何配置 ER 框架的参数，设计新 ER 解决方案所需的 ER 配置以访问特定业务域的数据，以及如何以 Microsoft Office 格式生成自定义报表。 这些步骤可以在 **USMF** 公司完成。

- [配置 ER 框架](#ConfigureFramework)

    - [配置 ER 参数](#ConfigureParameters)
    - [激活 ER 配置提供程序](#ActivateProvider)

        - [查看 ER 配置提供程序列表](#ReviewProvidersList)
        - [添加新 ER 配置提供程序](#AddProvider)
        - [激活 ER 配置提供程序](#ActivateAddedProvider)

- [设计域特定数据模型](#DesignModel)

    - [导入新数据模型配置](#ImportDataModel)
    - [创建新的数据模型配置](#DesignDataModel)

        - [为数据模型命名](#NameDataModel)
        - [添加数据模型字段](#FieldsEntry)
        - [完成数据模型的设计](#CompleteDataModel)

- [为配置的数据模型设计模型映射](#DesignMapping)

    - [导入新模型映射配置](#ImportModelMapping)
    - [创建新模型映射配置](#CreateModelMapping)

        - [设计新模型映射组件](#DesignMappingComponent)
        - [添加数据源以访问应用程序表](#AddMmDataSource1)
        - [添加数据源以访问应用程序枚举](#AddMmDataSource2)
        - [添加 ER 标签以指定语言生成报表](#AddMmLabels)
        - [添加数据源以将比较枚举值的结果转换为文本值](#AddMmDataSource3)
        - [将数据源与数据模型字段绑定](#AddMmBindings1)
        - [完成模型映射的设计](#CompleteModelMapping)

- [为自定义报表设计模板](#DesignReportTemplate)
- [设计格式](#DesignFormat)

    - [导入设计的格式配置](#FormatImport)
    - [创建新的格式配置](#FormatCreate)

        - [导入报表模板](#ImportReportTemplate)
        - [配置格式](#ConfigureFormat)
        - [定义报表标题的数据绑定](#DefineFormatBindings)
        - [查看模型数据源](#ReviewModelDataSource)
        - [将格式元素与数据源字段绑定](#BindFormatElements)

    - [从 ER 运行设计的格式](#RunFormatFromER)

- [调整设计的格式](#TuneFormat)

    - [修改格式以更改生成文档的名称](#ModifyToChangeName)
    - [修改格式以更改问题的顺序](#ModifyToOrder)
    - [从 ER 运行修改的格式](#RunFormatFromER2)
    - [完成格式设计](#CompleteFormat)

- [开发应用程序伪像以调用设计的报表](#DevelopCustomCode)

    - [修改源代码](#ModifySourceCode)

        - [添加数据合同类](#DataContractClass)
        - [添加 UI 构建器类](#UIBuilderClass)
        - [添加数据提供程序类](#DataProviderClass)
        - [添加标签文件](#LabelsFile)
        - [添加报表服务类](#ServiceClass)
        - [添加报表控制器类](#ControllerClass)
        - [添加菜单项](#MenuItem)
        - [向菜单添加菜单项](#Menu)
        - [构建 Visual Studio 项目](#BuildVSProject)

    - [从应用程序运行格式](#RunFormatFromApp)

- [调整设计的 ER 解决方案](#TuneSolution)

    - [修改模型映射](#ModifyModelMapping)

        - [添加数据源以访问数据合同对象](#AddDataSource1)
        - [添加数据源以访问 ER 格式映射记录](#AddDataSource2)
        - [添加数据源以访问正在运行的 ER 格式的格式映射记录](#AddDataSource3)
        - [在数据模型中输入正在运行的 ER 格式的名称](#AddBinding)
        - [完成模型映射的设计](#CompleteModelMapping2)

    - [修改格式](#ModifyFormat)

        - [添加新格式元素](#AddFormatElement)
        - [绑定添加的格式元素](#BindAddedFormatElement)
        - [完成格式设计](#CompleteFormat2)

    - [从应用程序运行格式](#RunFormatFromApp2)
    - [从 ER 运行格式](#RunFormatFromER3)
    - [为屏幕预览配置格式目标](#ConfigureDestination)
    - [从应用程序运行格式以作为 PDF 文档预览](#RunFormatFromApp3)

- [其他资源](#References)

在此示例中，您将为[调查表](../../../human-resources/hr-learning-questionnaires.md)模块创建新的 ER 解决方案。 这个新的 ER 解决方案使您可以使用 Microsoft Excel 工作表作为模板来设计报表。 然后，除了生成现有的 SQL Server Reporting Services (SSRS) 报表之外，您还可以生成 Excel 或 PDF 格式的 **调查表** 报表。 您还可以稍后根据要求修改新报表。 无需进行编码。

1. 要运行现有报表，请转到 **调查表** \> **设计** \> **调查表报表**。

    ![在“调查表”模块中选择“调查表报表”菜单项来运行现有 SSRS 报表。](./media/er-quick-start1-application-menu-origin.png)

2. 在 **调查表报表** 对话框中，指定选择条件。 应用筛选器，让报表仅包含 **SBCCrsExam** 调查表。

    ![在“调查表报表”对话框中指定选择条件。](./media/er-quick-start1-ssrs-report-dialog.png)

下图显示了 **SBCCrsExam** 调查表的 SSRS 报表的生成版本。

![生成的 SSRS 报表。](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>配置 ER 框架

作为电子报告开发人员角色的用户，您必须至少配置一组 ER 参数，才能开始使用 ER 框架设计新的 ER 解决方案。

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>配置 ER 参数

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **电子申报** 工作区中，选择 **电子申报参数** 链接。
3. 在 **电子申报参数** 页上，在 **常规** 选项卡上，将 **启用设计模式** 选项设置为 **是**。
4. 在 **附件** 选项卡上，设置以下参数：

    - 将 **USMF** 公司的 **配置** 字段设置为 **文件**。
    - 将 **作业存档**、**临时**、**基准** 和 **其他** 字段设置为 **文件**。

有关 ER 参数的详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>激活 ER 配置提供程序

将把每个 ER 配置标记为由 ER 配置提供程序负责。 因此，必须先在 **电子报告** 工作区中激活 ER 配置提供程序，才能开始添加或编辑 ER 配置。

> [!NOTE]
> 只有 ER 配置的负责人才能对其进行编辑。 因此，必须先在 **电子申报** 工作区中激活相应 ER 配置提供程序，才能编辑 ER 配置。

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>查看 ER 配置提供程序列表

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **电子报告** 工作区的 **相关链接** 部分，选择 **配置提供程序**。
3. 在 **配置提供程序** 页，每条配置提供程序记录都有唯一名称和 URL。 查看此页面的内容。 如果已有 **Litware, Inc.** (`https://www.litware.com`) 的记录，请跳过下一过程，即[添加新 ER 配置提供程序](#ActivateProvider)。

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>添加新 ER 配置提供程序

1. 在 **配置提供程序** 页面上，选择 **新建**。
2. 在 **名称** 字段中，输入 **Litware, Inc.**
3. 在 **Internet 地址** 字段中，输入 `https://www.litware.com`。
4. 选择 **保存**。

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>激活 ER 配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **电子报告** 工作区中，选择 **Litware, Inc.** 配置提供程序。
3. 选择 **设置有效**。

有关 ER 配置提供程序的详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>设计域特定数据模型

您必须为 **调查表** 业务域创建一个包含数据模型组件的新 ER 配置。 此数据模型将在以后您设计 ER 格式以生成 **调查表** 报表时用作数据源。

通过完成[导入新数据模型配置](#ImportDataModel)一节的步骤，可以从提供的 XML 文件导入所需的数据模型。 或者，您可以完成[创建新数据模型配置](#DesignDataModel)一节的步骤来从头开始设计此数据模型。

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>导入新数据模型配置

1. 下载 [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) 文件，并将其保存到本地计算机。
2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **电子报告** 工作区中，选择 **报告配置**。
4. 在操作窗格上，选择 **交换** \> **从 XML 文件加载**。
5. 选择 **浏览**，然后找到并选择 **Questionnaires model.version.1.xml** 文件。
6. 选择 **确定** 导入配置。

要继续，跳过下一个过程[创建新的数据模型配置](#DesignDataModel)。

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>创建新的数据模型配置

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **电子报告** 工作区中，选择 **报告配置**。
3. 选择 **创建配置**。
4. 在下拉对话框的 **名称** 字段中，输入 **调查表模型**。
5. 选择 **创建配置** 以创建配置。

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>为数据模型命名

1. 在 **配置** 页上的配置树中，选择 **调查表模型**。
2. 选择 **设计器**。
3. 在 **数据模型设计器** 页上的 **常规** 快速选项卡上，在 **名称** 字段中，输入 <a name="DataModeName"></a>**调查表**。

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>添加新数据模型字段

1. 在 **数据模型设计器** 页上，选择 **新建**。
2. 在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：

    1. 选择 **模型根** 作为新节点的类型。
    2. 在 **名称** 字段中，输入 <a name="RootDefinitionName"></a>**根**。
    3. 选择 **添加** 添加新节点。

    此根描述符将用于为 **调查表** 报表提供数据。 单个数据模型可以有多个描述符。 可以为一个 ER 格式指定每个描述符，来标识生成报表所需的数据。

3. 再次选择 **新建**，然后，在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：

    1. 选择 **活动节点的子节点** 作为新节点的类型。
    2. 在 **名称** 字段中，输入 **公司名称**。
    3. 在 **物料类型** 字段中，选择 **字符串**。
    4. 选择 **添加** 添加新字段。

    将当前公司的名称传递到使用此数据模型作为数据源的 ER 报表时，此字段是必需的。

4. 再次选择 **新建**，然后，在用于添加数据模型节点的下拉对话框中，按照下列步骤操作：

    1. 选择 **活动节点的子节点** 作为新节点的类型。
    2. 在 **名称** 字段中，输入 **调查表**。
    3. 在 **物料类型** 字段中，选择 **记录列表**。
    4. 选择 **添加** 添加新字段。

    此字段将用于将调查表列表传递到使用此数据模型作为数据源的 ER 报表。

5. 选择 **调查表** 节点。
6. 继续以相同方式添加可编辑数据模型的必需字段，直到完成以下数据模型结构。

    | 字段路径                                                    | 数据类型   | 字段指定/返回值 |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | 根                                                          |             | 请求调查表数据的参考点。 |
    | 根\\公司名称                                             | 字符串      | 当前公司的名称。 |
    | 根\\执行上下文                                        | 录制      | 格式执行详细信息。 |
    | 根\\执行上下文\\格式名称                            | 字符串      | 正在运行的 ER 格式的名称。 |
    | 根\\调查表                                           | 记录列表 | 调查表列表 |
    | 根\\调查表\\活动                                   | 字符串      | 当前调查表的状态。 |
    | 根\\调查表\\代码                                     | 字符串      | 当前调查表的代码。 |
    | 根\\调查表\\说明                              | 字符串      | 当前调查表的说明。 |
    | 根\\调查表\\调查表类型                        | 字符串      | 当前调查表的类型。 |
    | 根\\调查表\\问题顺序                            | 字符串      | 当前调查表的数字顺序。 |
    | 根\\调查表\\结果组                             | 录制      | 当前调查表的结果参数。 |
    | 根\\调查表\\结果组\\代码                       | 字符串      | 当前结果组的标识代码。 |
    | 根\\调查表\\结果组\\说明                | 字符串      | 当前结果组的说明。 |
    | 根\\调查表\\结果组\\最高分数          | 实数        | 可能获得的最高分数。 |
    | 根\\调查表\\问题                                 | 记录列表 | 当前调查表的问题列表。 |
    | 根\\调查表\\问题\\集合序列号       | 整数     | 当前答案集合的序列号。 |
    | 根\\调查表\\问题\\ID                             | 字符串      | 当前问题的标识代码。 |
    | 根\\调查表\\问题\\必须完成                | 字符串      | 指示是否必须回答当前问题的标记。 |
    | 根\\调查表\\问题\\主要问题                | 字符串      | 指示当前问题是否是主要问题的标记。 |
    | 根\\调查表\\问题\\序列号                 | 整数     | 当前问题的序列号。 |
    | 根\\调查表\\问题\\文本                           | 字符串      | 当前问题的文本。 |
    | 根\\调查表\\问题\\答案                         | 记录列表 | 当前问题的答案列表。 |
    | 根\\调查表\\问题\\答案\\正确答案          | 字符串      | 指示当前答案是否正确的标记。 |
    | 根\\调查表\\问题\\答案\\分数                 | 实数        | 选择当前答案获得的分数。 |
    | 根\\调查表\\问题\\答案\\序列号         | 整数     | 当前答案的序列号。 |
    | 根\\调查表\\问题\\答案\\文本                   | 字符串      | 当前答案的文本。 |

    下图显示了 **数据模型设计器** 页上完成的可编辑数据模型。

    ![ER 数据模型设计器中配置的数据模型。](./media/er-quick-start1-model2.png)

7. 保存所做的更改。
8. 关闭 **数据模型设计器** 页。

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>完成数据模型的设计

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页上的配置树中，选择 **调查表模型**。
3. 在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。
4. 选择 **更改状态** \> **完成**。

此配置的版本 1 的状态将从 **草稿** 更改为 **已完成**。 版本 1 不能再更改。 此版本包含已配置的数据模型，可以用作其他 ER 配置的基础。 此配置的版本 2 将创建，状态为 **草稿**。 您可以编辑此版本来调整 **调查表** 数据模型。

![“配置”页面上可编辑配置的版本。](./media/er-quick-start1-model-configuration.png)

有关 ER 配置的版本控制的详细信息，请参阅[电子报告 (ER) 概述](general-electronic-reporting.md#component-versioning)。

> [!NOTE]
> 配置的数据模型是 **调查表** 业务域的抽象表示，不包含与 Microsoft Dynamics 365 Finance 特定的伪像的关系。

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>为配置的数据模型设计模型映射

作为电子报告开发人员角色的用户，您必须为 **调查表** 数据模型创建一个新的 ER 配置，其中包含模型映射组件。 由于此组件为 Finance 实现配置的数据模型，因此它是 Finance 特定组件。 您必须配置模型映射组件来指定必须用于在运行时使用应用程序数据填充配置的数据模型的应用程序对象。 要完成此任务，您必须了解 Finance 中 **调查表** 业务域的数据结构的实现详细信息。

通过完成后面的[导入新模型映射配置](#ImportModelMapping)一节的步骤，可以从提供的 XML 文件导入所需的模型映射配置。 或者，您可以完成[创建新模型映射配置](#CreateModelMapping)一节的步骤来从头开始设计此模型映射。

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>导入新模型映射配置

1. 下载 [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) 文件，并将其保存到本地计算机。
2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **电子报告** 工作区中，选择 **报告配置**。
4. 在操作窗格上，选择 **交换** \> **从 XML 文件加载**。
5. 选择 **浏览**，然后找到并选择 **Questionnaires mapping.version.1.1.xml** 文件。
6. 选择 **确定** 导入配置。

要继续，跳过下一个过程[创建新模型映射配置](#CreateModelMapping)。

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>创建新模型映射配置

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页上的配置树中，选择 **调查表模型**。
3. 选择 **创建配置**。
4. 在下拉对话框中，执行以下步骤：

    1. 在 **新建** 字段中，选择 **基于数据模型调查表的模型映射**。
    2. 在 **名称** 字段中输入 **调查表映射**。
    3. 在 **数据模型定义** 字段中，选择 **根** 定义。
    4. 选择 **创建配置** 以创建配置。

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>设计新模型映射组件

1. 在 **配置** 页上的配置树中，选择 **调查表映射**。
2. 选择 **设计器** 来打开映射列表。
3. 选择为 **根** 定义自动添加的 **调查表映射** 映射。
4. 选择 **设计器** 开始配置选定的映射。

系统会自动为 **根** 定义添加新映射。 此映射具有 **到模型** 方向。 因此，此映射可用于使用所需数据填充数据模型。

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>添加数据源以访问应用程序表

您必须配置数据源以访问包含调查表详细信息的应用程序表。

1. 在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表记录**。
2. 添加将用于访问 KMCollection 表的新数据源，其中每个记录代表一个调查表：

    1. 在 **数据源** 窗格中，选择 **添加根**。
    2. 在对话框的 **名称** 字段中，输入 **调查表**。
    3. 在 **表** 字段中，输入 **KMCollection**。
    4. 将 **要求查询** 选项设置为 **是**。 然后，您可以在运行时在系统查询对话框中为此表指定[筛选](../../fin-ops/get-started/advanced-filtering-query-options.md)选项。
    5. 选择 **确定** 添加新数据源。

3. 在 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表记录**。
4. 添加将用于访问 KMQuestion 表的新数据源，其中每个记录代表调查表中的一个问题：

    1. 在 **数据源** 窗格中，选择 **添加根**。
    2. 在对话框的 **名称** 字段中，输入 **问题**。
    3. 在 **表** 字段中，输入 **KMQuestion**。
    4. 选择 **确定** 添加新数据源。

5. 在 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表记录**。
6. 添加将用于访问 KMAnswer 表的新数据源尝试，其中每个记录代表调查表中问题的一个答案：

    1. 在 **数据源** 窗格中，选择 **添加根**。
    2. 在 **名称** 字段中，输入 **答案**。
    3. 在 **表** 字段中，输入 **KMAnswer**。
    4. 选择 **确定** 添加新数据源。

7. 在 **数据源类型** 窗格中，选择 **函数\\计算字段**。
8. 添加将用于从父 KMCollection 表的每个记录访问 KMQuestionResultGroup 表的记录的新计算字段：

    1. 在 **数据源** 窗格中，选择 **调查表**。
    2. 选择 **添加**。
    3. 在对话框的 **名称** 字段中，输入 **\$ResultGroup**。
    4. 选择 **编辑公式**。
    5. 在 [ER 公式编辑器](general-electronic-reporting-formula-designer.md)中，在 **公式** 字段中，输入 **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** 以使用 KMCollection 和 KMQuestionResultGroup 表之间的一对多关系的[路径](er-formula-language.md#Paths)。
    6. 选择 **保存**，然后关闭公式编辑器。
    7. 选择 **确定** 添加新计算字段。

9. 在 **数据源类型** 窗格中，选择 **函数\\计算字段**。
10. 添加将用于从父 KMCollectionQuestion 表的每个记录访问 KMQuestion 表的问题记录的新计算字段：

    1. 在 **数据源** 窗格中，选择 **调查表**。
    2. 展开包含 KMCollection 表的一对多关系的 **\<Relations** 节点。
    3. 选择相关的 **KMCollectionQuestion** 表，然后选择 **添加**。
    4. 在对话框的 **名称** 字段中，输入 **\$Question**。
    5. 选择 **编辑公式**。
    6. 在公式编辑器的 **公式** 字段中，输入 **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** 以从 KMQuestion 表返回相应的问题记录。
    7. 选择 **保存**，然后关闭公式编辑器。
    8. 选择 **确定** 添加新计算字段。

11. 在 **数据源类型** 窗格中，选择 **函数\\计算字段**。
12. 添加将用于从父 KMQuestion 表的每个记录访问 KMAnswer 表的答案记录的新计算字段：

    1. 在 **数据源** 窗格中，选择 **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**，然后选择 **添加**。
    2. 在对话框的 **名称** 字段中，输入 **\$Answer**。
    3. 选择 **编辑公式**。
    4. 在公式编辑器的 **公式** 字段中，输入 **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** 以从 KMAnswer 表返回相应的答案记录。
    5. 选择 **保存**，然后关闭公式编辑器。
    6. 选择 **确定** 添加新计算字段。

13. 在 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表**。
14. 添加将用于访问 CompanyInfo 表的方法的新数据源。 请注意，此表的 **find()** 方法将返回一条记录，该记录表示在其上下文中调用此映射的当前 Finance 实例的公司。

    1. 在 **数据源** 窗格中，选择 **添加根**。
    2. 在对话框的 **名称** 字段中，输入 **公司信息**。
    3. 在 **表** 字段中，输入 **公司信息**。
    4. 选择 **确定** 添加新数据源。

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>添加数据源以访问应用程序枚举

您必须配置数据源以访问应用程序枚举，并将其值与应用程序表中 **枚举** 类型的字段的值进行比较。 您必须使用比较的结果来填充数据模型的相应字段。

1. 在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\枚举**。
2. 添加将用于访问 **EnumAppNoYes** 枚举的值的新数据源。

    1. 在 **数据源** 窗格中，选择 **添加根**。
    2. 在对话框的 **名称** 字段中，输入 **EnumAppNoYes**。
    3. 在 **枚举** 字段中，输入 **NoYes**。
    4. 选择 **确定** 添加新数据源。

3. 在 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\枚举**。
4. 添加将用于访问 **KMCollectionQuestionMode** 枚举的值的新数据源。

    1. 在 **数据源** 窗格中，选择 **添加根**。
    2. 在对话框的 **名称** 字段中，输入 **EnumAppQuestionOrder**。
    3. 在 **枚举** 字段中，输入 **KMCollectionQuestionMode**。
    4. 选择 **确定** 添加新数据源。

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>添加 ER 标签以指定语言生成报表

您可以添加 ER 标签来配置一些数据源以返回取决于在模型映射调用的上下文中定义的语言的值。

1. 在 **模型映射设计器** 页的 **数据源** 窗格中，选择 **答案**，然后选择 **编辑**。
2. 激活 **标签** 字段。
3. 选择 **翻译**。
4. 在 **文本翻译** 对话框中，执行以下步骤：

    1. 在 **标签 ID** 字段中，输入 **PositiveAnswer**。
    2. 在 **语言为默认语言的文本** 字段中，输入 **是**。
    3. 选择 **翻译**。
    4. 在 **标签 ID** 字段中，输入 **NegativeAnswer**。
    5. 在 **语言为默认语言的文本** 字段中，输入 **否**。
    6. 选择 **翻译**。

5. 关闭 **文本翻译** 对话框。
6. 选择 **取消**。

![为可编辑模型映射添加 ER 标签。](./media/er-quick-start1-adding-labels.png)

您仅为默认语言输入了 ER 标签。 有关如何将 ER 标签翻译为其他语言的信息，请参阅[设计多语言报表](er-design-multilingual-reports.md)。

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>添加数据源以将比较枚举值的结果转换为文本值

因为必须为差异源多次转换枚举值和文本值之间的比较结果，所以最好将此逻辑配置为单个数据源。 但是，要使此数据源可以重用，必须将其配置为参数化数据源。 有关详细信息，请参阅[支持对计算字段类型的 ER 数据源的参数化调用](er-calculated-field-type.md)。

1. 在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **常规\\空容器**。
2. 添加新容器数据源：

    1. 在 **数据源** 窗格中，选择 **添加根**。
    2. 在对话框的 **名称** 字段中，输入 **帮助程序**。
    3. 选择 **确定** 添加新容器数据源。

3. 在 **数据源类型** 窗格中，选择 **函数\\计算字段**。
4. 添加新数据源：

    1. 在 **数据源** 窗格中，选择 **帮助程序**。
    2. 选择 **添加**。
    3. 在对话框的 **名称** 字段中，输入 **NoYesEnumToString**。
    4. 选择 **编辑公式**。
    5. 在公式编辑器中，选择 **参数**。
    6. 按照以下步骤为配置的表达式指定参数：

        1. 选择 **新建**。
        2. 在对话框的 **名称** 字段中，输入 **参数**。
        3. 在 **类型** 字段中，选择 **布尔** 数据类型。
        4. 选择 **确定**。

    7. 在 **公式** 字段中，输入 **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")**，以根据执行上下文的语言和指定参数的值返回相应的 ER 标签的文本。
    8. 选择 **保存**，然后关闭公式编辑器。
    9. 选择 **确定** 添加新数据源。

![ER 模型映射设计器中配置的模型映射。](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>将数据源与数据模型字段绑定

您必须将配置的数据源与数据模型的字段绑定，来指定在运行时如何使用应用程序数据填充数据模型。

1. 在 **模型映射设计器** 页的 **数据模型** 窗格中，选择 **公司名称**。
2. 在 **数据源** 窗格中，展开 **公司信息**，然后按照以下步骤操作：

    1. 展开代表“公司信息”表的 **find()** 方法的 **CompanyInfo.find()** 节点。
    2. 选择 **CompanyInfo.find().Name**。
    3. 选择 **绑定** 以在运行时的上下文中填写要调用配置的模型映射的公司的名称。

3. 在 **数据模型** 窗格中，选择 **调查表**。
4. 在 **数据源** 窗格中，选择 **调查表**，然后选择 **绑定** 填充调查表记录。
5. 在 **数据模型** 窗格中，展开 **调查表**，然后按照以下步骤操作：

    1. 在 **数据模型** 窗格中，选择 **活动**。
    2. 在 **数据模型** 窗格中，选择 **编辑**。
    3. 在 **公式** 字段中，输入 **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** 以填充枚举值之间比较的文本相关和语言相关结果。

6. 继续以相同的方式将数据源绑定到数据模型字段，直到获得以下结果。

    | 字段路径                                              | 数据类型   | 行动 | 绑定表达式 |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | 公司名称                                             | 字符串      | 绑定   | CompanyInfo.'find()'.Name |
    | 调查表                                           | 记录列表 | 绑定   | 调查表 |
    | 调查表\\活动                                   | 字符串      | 编辑​​   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | 调查表\\代码                                     | 字符串      | 绑定   | \@.kmCollectionId |
    | 调查表\\说明                              | 字符串      | 绑定   | \@.Description |
    | 调查表\\调查表类型                        | 字符串      | 绑定   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | 调查表\\问题顺序                            | 字符串      | 编辑​​   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Conditional",<br>EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",<br>EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",<br>EnumAppQuestionOrder.Sequence, "Sequential",<br>"") |
    | 调查表\\结果组                             | 录制      |        | |
    | 调查表\\结果组\\代码                       | 字符串      | 绑定   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | 调查表\\结果组\\说明                | 字符串      | 绑定   | \@.'\$ResultGroup'.description |
    | 调查表\\结果组\\最高分数          | 实数        | 绑定   | \@.'\$ResultGroup'.maxPoint |
    | 调查表\\问题                                 | 记录列表 | 绑定   | \@.'&lt;Relations'.KMCollectionQuestion |
    | 调查表\\问题\\集合序列号       | 整数     | 绑定   | \@.answerCollectionSequenceNumber |
    | 调查表\\问题\\ID                             | 字符串      | 绑定   | \@.kmQuestionId |
    | 调查表\\问题\\必须完成                | 字符串      | 编辑​​   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | 调查表\\问题\\主要问题                | 字符串      | 绑定   | \@.parentQuestionId |
    | 调查表\\问题\\序列号                 | 整数     | 绑定   | \@.SequenceNumber |
    | 调查表\\问题\\文本                           | 字符串      | 绑定   | \@.'\$Question'.text |
    | 调查表\\问题\\答案                         | 记录列表 | 绑定   | \@.'\$Question'.'\$Answer' |
    | 调查表\\问题\\答案\\正确答案          | 字符串      | 编辑​​   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | 调查表\\问题\\答案\\分数                 | 实数        | 绑定   | \@.point |
    | 调查表\\问题\\答案\\序列号         | 整数     | 绑定   | \@.sequenceNumber |
    | 调查表\\问题\\答案\\本文                   | 字符串      | 绑定   | \@.text |

    下图显示了 **模型映射设计器** 页面上配置的模型映射的最终状态。

    ![ER 模型映射设计器中完全配置的模型映射。](./media/er-quick-start1-mapping2.png)

7. 保存所做的更改。
8. 关闭 **模型映射设计器** 页。

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>完成模型映射的设计

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页上的配置树中，选择 **调查表映射**。
3. 在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。
4. 选择 **更改状态** \> **完成**。

此配置的版本 1.1 的状态将从 **草稿** 更改为 **已完成**。 版本 1.1 不能再更改。 此版本包含已配置的模型映射，可以用作其他 ER 配置的基础。 此配置的版本 1.2 将创建，状态为 **草稿**。 您可以编辑此版本来调整 **调查表映射** 配置。

![“配置”页面上可编辑 ER 配置的版本。](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> 配置的模型映射是表示 **调查表** 业务域的抽象数据模型的 Finance 特定实现。

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>为自定义报表设计模板

ER 框架使用预定义的模板生成 Microsoft Office 格式（Excel 工作簿或 Word 文档）的报表。 在生成所需报表时，将根据配置的数据流使用所需数据填充模板。 因此，您必须首先为自定义报表设计模板。 此模板必须设计为 Excel 工作簿，其结构代表自定义报表的布局。 您必须为计划填充所需数据的每个 Excel 项命名。

1. 下载 [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) 文件，并将其保存到本地计算机。
2. 在 Excel 中打开文件，查看工作簿的结构。

如下图所示，下载的模板已设计为打印指定的调查表，这些调查表显示调查表的问题以及相应的答案。

![可打印指定调查表的 Excel 模板。](./media/er-quick-start1-template-layout.png)

Excel 名称已添加到此模板中以填充调查表详细信息。 您可以使用名称管理器来查看 Excel 名称。

![使用名称管理器查看提供的 Excel 模板中的 Excel 名称。](./media/er-quick-start1-template-names.png)

报表标签已添加为英语的固定文本。 您可以使用 ER 格式[标签](#AddMmLabels)将报表标签替换为将使用语言相关文本填充标签的新的 Excel 名称，就像在配置的模型映射中使用语言相关表达式一样。 在这种情况下，必须以可编辑的 ER 格式添加 ER 标签。

如下图所示，已指定自定义报表标题来使 Excel 能够分页。

![提供的 Excel 模板中的自定义报表标题。](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>设计格式

作为电子报告功能顾问角色的用户，您必须创建一个新的 ER 配置，其中包含格式组件。 您必须配置格式组件来指定运行时如何使用所需数据填充报表模板。

通过完成[导入设计的格式配置](#FormatImport)一节的步骤，可以从提供的 XML 文件导入所需的格式。 或者，您可以完成[创建新格式配置](#FormatCreate)一节的步骤来从头开始设计此格式。

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>导入设计的格式配置

1. 下载 [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) 文件，并将其保存到本地计算机。
2. 转到 **组织管理** \> **工作区** \> **电子申报**。
3. 在 **电子报告** 工作区中，选择 **报告配置**。
4. 在操作窗格上，选择 **交换** \> **从 XML 文件加载**。
5. 选择 **浏览**，然后找到并选择 **Questionnaires format.version.1.1.xml** 文件。
6. 选择 **确定** 导入配置。

要继续，跳过下一个过程[创建新格式配置](#FormatCreate)。

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>创建新的格式配置
 
1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页上的配置树中，选择 **调查表模型**。
3. 选择 **创建配置**。
4. 在下拉对话框中，执行以下步骤：

    1. 在 **新建** 字段中，选择 **基于数据模型调查表的格式**。
    2. 在 **名称** 字段中输入 **调查表报表**。
    3. 在 **数据模型版本** 字段中，选择 **1**。

        > [!NOTE]
        > - 如果您选择基础数据模型的特定版本，此数据模型的相应版本的结构将以创建的格式以 **模型** 数据源的结构向您呈现。
        > - 您可以将此字段保留为空。 在这种情况下，数据模型 **草稿** 版本的结构将以创建的格式以 **模型** 数据源的结构向您呈现。 然后，您可以调整模型，并立即以您的格式查看这些调整。 当您同时配置数据模型、模型映射和格式时，此方法可以提高 ER 解决方案设计的效率。
        > - 如果选择基础数据模型的特定版本，以后在开始编辑格式时，可以切换为使用 **草稿** 版本。

    4. 在 **数据模型定义** 字段中，选择 **根** 定义。

5. 选择 **创建配置** 以创建配置。

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>导入报表模板

1. 在 **配置** 页上的配置树中，选择 **调查表报表**。
2. 选择 **设计器** 开始配置自定义格式。
3. 在 **格式设计器** 页的操作窗格上，选择 **导入** \> **从 Excel 导入**。
4. 在对话框中，执行以下步骤：

    1. 选择 **添加模板**。
    2. 找到并选择本地保存的 **Questionnaires report template.xslx** 文件，然后选择 **打开**。
    3. 选择 **确定** 导入模板。

    ![导入报表模板。](./media/er-quick-start1-template-import.png)

**Excel\\文件** 格式元素将作为根元素自动添加到可编辑格式中。 此外，将为导入模板的每个确认的 Excel 名称自动添加 **Excel\\范围** 格式元素或 **Excel\\单元格** 格式元素。 具有嵌套 **字符串** 元素的 **Excel\\标题** 格式会自动添加，以反映导入模板的标题设置。

![包括在 ER 操作设计器中自动添加的元素的格式结构。](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>配置格式

1. 在 **格式设计器** 页面的格式树中，选择 **Excel** 根元素。
2. 在页面右侧的 **格式** 选项卡上的 **名称** 字段中，输入 <a name="AddFormatRootElement"></a>**报表**。
3. 在 **语言首选项** 字段中，选择 **用户首选项** 以用户的首选语言运行报表。
4. 在 **区域性首选项** 字段中，选择 **用户首选项** 以用户的首选区域性运行报表。

    有关如何为 ER 流程指定语言和区域性上下文的信息，请参阅[设计多语言报表](er-design-multilingual-reports.md)。

    ![在 ER 操作设计器中为设计的报表配置语言和区域性设置。](./media/er-quick-start1-template-format-structure1.png)

5. 在格式树中，展开根节点，然后选择 **结果组**。
6. 在 **格式** 选项卡中，在 **复制方向** 字段中，选择 **不复制**，因为您不希望单个调查表具有多个结果组。

    ![在 ER 操作设计器中定义范围格式元素的复制方向。](./media/er-quick-start1-template-format-structure2.png)

7. 选择 **保存**。

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>定义报表标题的数据绑定

您必须为用于填充生成报表的标题的格式元素指定数据绑定。

1. 在 **格式设计器** 页上右侧的 **映射** 选项卡上，选择 **报表\\报表标题** 元素。
2. 选择 **编辑公式**。
3. 在公式编辑器中，选择 **翻译**。
4. 在 **文本翻译** 对话框中，执行以下步骤：

    1. 在 **标签 ID** 字段中，输入 **ReportTitle**。
    2. 在 **语言为默认语言的文本** 字段中，输入 **调查表报表**。
    3. 选择 **翻译**，然后选择 **保存**。
    4. 选择 **翻译** 关闭 **文本翻译** 对话框。

5. 关闭公式编辑器。

    ![配置绑定以填充生成报表的标题。](./media/er-quick-start1-add-report-title-label.png)

您可以使用此方法让当前模板的所有其他标签成为语言相关标签。 有关如何将单个 ER 配置的已添加标签翻译为所有支持语言的信息，请参阅[设计多语言报表](er-design-multilingual-reports.md)。

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>查看模型数据源

1. 在 **格式设计器** 页的 **映射** 选项卡上，选择表示此 ER 格式的基础数据模型的 <a name="ModelDSName"></a>**模型** 数据源。
2. 选择 **编辑**。
3. 查看 **数据源属性** 对话框中的信息。 此数据源表示位于 **调查表模型** ER 配置中的 **调查表** 数据模型组件的版本 1。

![ER 操作设计器中模型数据源的属性。](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>将格式元素与数据源字段绑定

若要指定在运行时如何填充模板，必须将与相应的 Excel 名称相关联的每个格式元素与此格式的数据源的单个字段绑定。

1. 在 **格式设计器** 页面的格式树中，选择 **报表\\公司名称** 格式元素。
2. 在 **映射** 选项卡上，选择 **字符串** 类型的 **model.CompanyName** 数据源字段。
3. 选择 **绑定** 在模板中输入公司名称。
4. 在格式树中，选择 **报表\\调查表** 元素。
5. 在 **映射** 选项卡上，选择 **记录列表** 类型的 **model.Questionnaire** 数据源字段。
6. 选择 **绑定**。
7. 选择 **显示详细资料** 查看格式元素的更多详细信息。

    **调查表** 范围格式元素已配置为垂直复制。 将其绑定到 **记录列表** 类型的数据源时，将对绑定数据源的每条记录重复 Excel 模板的相应的 **调查表** 范围。
 
    ![在 ER 操作设计器中将调查表范围格式元素绑定到相应的记录列表数据源。](./media/er-quick-start1-bindings1.png)

    由于 Excel 模板的 **调查表** 范围是在第 5 到 14 行之间定义的，因此每个报告的调查表都将重复这些行。

    ![生成报表中将为记录列表数据源的每条记录重复的 Excel 模板中的行。](./media/er-quick-start1-template-questionnaire-range.png)

8. 为其余格式元素配置类似的绑定，如下表所述。

    > [!NOTE]
    > 在此表中，“数据源路径”列中的信息假定[相对路径](relative-path-data-bindings-er-models-format.md) ER 功能已打开。

    | 格式元素路径                                      | 数据源路径 |
    |----------------------------------------------------------|------------------|
    | Excel\\报告标题                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\公司名称                                       | **model.CompanyName** |
    | Excel\\调查表                                     | **model.Questionnaire** |
    | Excel\\调查表\\活动                             | **\@.Active**，其中 **\@** 是 **model.Questionnaire** |
    | Excel\\调查表\\代码                               | **\@.Code** |
    | Excel\\调查表\\说明                        | **\@.Description** |
    | Excel\\调查表\\调查表类型                  | **\@.QuestionnaireType** |
    | Excel\\调查表\\问题顺序                      | **\@.QuestionOrder** |
    | Excel\\调查表\\结果组\\代码\_               | **\@.ResultsGroup.Code** |
    | Excel\\调查表\\结果组\\说明\_        | **\@.ResultsGroup.Description** |
    | Excel\\调查表\\结果组\\最高分数    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\调查表\\问题                           | **\@.Question** |
    | Excel\\调查表\\问题\\集合序列号 | **\@.CollectionSequenceNumber**，其中 **\@** 是 **model.Questionnaire.Question** |
    | Excel\\调查表\\问题\\ID                       | **\@.Id** |
    | Excel\\调查表\\问题\\必须完成          | **\@.MustBeCompleted** |
    | Excel\\调查表\\问题\\主要问题          | **\@.PrimaryQuestion** |
    | Excel\\调查表\\问题\\序列号           | **\@.SequenceNumber** |
    | Excel\\调查表\\问题\\文本                     | **\@.Text** |
    | Excel\\调查表\\问题\\答案                   | **\@.Answer** |
    | Excel\\调查表\\问题\\答案\\正确答案    | **\@.CorrectAnswer**，其中 **\@** 是 **model.Questionnaire.Answer** |
    | Excel\\调查表\\问题\\答案\\分数           | **\@.Points** |
    | Excel\\调查表\\问题\\答案\\文本             | **\@.Text** |

9. 当您完成时，选择 **保存**。

下图显示了 **模式设计器** 页面上配置的数据绑定的最终状态。

![ER 操作设计器中配置的数据绑定。](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> 指定数据源和绑定的整个集合表示已配置格式的格式映射组件。 当您运行配置的格式以生成报表时，将调用此格式映射。

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>从 ER 运行设计的格式

现在，您可以从 **配置** 页面运行设计的格式来进行测试。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表报表**。
3. 为状态为 **草稿** 的格式版本选择 **设计器**。
4. 在 **格式设计器** 页上，选择 **运行**。
5. 在 **ER 参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。
6. 选择 **确定** 确认筛选选项。
7. 选择 **确定** 运行报表。
8. 查看生成的报表。

[默认](electronic-reporting-destinations.md#default-behavior)情况下，生成的报表以 Excel 文件的形式提供，您可以进行下载。 下图以 Excel 格式显示了生成报表的两个页面。

![Excel 格式的生成报表的示例，第 1 页。](./media/er-quick-start1-report1a.png)

![Excel 格式的生成报表的示例，第 2 页。](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>调整设计的格式

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>修改格式以更改生成文档的名称

默认情况下，使用当前用户的别名来命名生成的文档。 通过修改格式，您可以更改此行为，以根据您的自定义逻辑来命名生成的文档。 例如，生成文档的名称可以基于当前会话的日期和时间以及报表的标题。

1. 在 **格式设计器** 页中，选择 **报表** 根项。
2. 在 **映射** 选项卡上，选择 **编辑文件名**。
3. 在 **公式** 字段中，输入 **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**。
4. 选择 **保存**，然后关闭公式编辑器。
5. 选择 **保存**。

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>修改格式以更改问题的顺序

问题在生成的报表中未正确排序。 您可以通过修改格式来更改顺序。

1. 在 **格式设计器** 页中，选择 **报表** 根项。
2. 在 **映射** 选项卡上的格式树中，展开 **报表\\调查表\\问题**。

    ![ER 操作设计器中范围类型的问题格式元素。](./media/er-quick-start1-bindings3.png)

3. 在 **映射** 选项卡上，选择 **model.Questionnaire**。
4. 选择 **添加** \> **函数\\计算字段**，然后在 **名称** 字段中输入 **OrderedQuestions**。
5. 选择 **编辑公式**。
6. 在公式编辑器的 **公式** 字段中，输入 **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)**，以按序列顺序编号对当前调查表的问题列表进行排序。
7. 选择 **保存**，然后关闭公式编辑器。
8. 选择 **确定** 完成新计算字段的输入。
9. 在 **映射** 选项卡上，选择 **model.Questionnaire.OrderedQuestions**。
10. 在格式树中，选择 **Excel\\调查表\\问题**。
11. 选择 **绑定**，然后确认在嵌套元素的所有绑定中，当前的 **model.Questionnaire.Questions** 路径已被新的 **model.Questionnaire.OrderedQuestions** 路径替换。
12. 选择 **保存**。

![在 ER 操作设计器中将问题格式元素绑定到配置的 OrderedQuestions 数据源。](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>从 ER 运行修改的格式

现在，您可以从 ER 框架运行修改的格式来进行测试。

1. 在 **格式设计器** 页上，选择 **运行**。
2. 在 **ER 参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。
3. 选择 **确定** 确认筛选选项。
4. 选择 **确定** 运行报表。
5. 查看生成的报表。

下图显示了 Excel 格式的生成报表，其中问题已正确排序。

![问题已正确排序的 Excel 格式的生成报表。](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>完成格式设计

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表报表**。
3. 在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。
4. 选择 **更改状态** \> **完成**。

此配置的版本 1.1 的状态将从 **草稿** 更改为 **已完成**。 版本 1.1 不能再更改。 此版本包含配置的格式，可用于打印自定义报表。 此配置的版本 1.2 将创建，状态为 **草稿**。 您可以编辑此版本来调整 **调查表** 报表的格式。

![“配置”页面上的可编辑 ER 配置。](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> 配置的格式是您的 **调查表** 报表的设计，不包含与 Finance 特定伪像的关系。

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>开发应用程序伪像以调用设计的报表

作为系统管理员角色的用户，您必须开发新逻辑，以可以从应用程序用户界面 (UI) 调用配置的 ER 格式来生成自定义报表。 当前，ER 不提供任何配置此类逻辑的功能。 因此，需要一些工程工作。 

要开发新逻辑，必须部署支持连续生成的拓扑。 有关详细信息，请参阅[部署支持连续生成和测试自动化的拓扑](../perf-test/continuous-build-test-automation.md)。 还必须可以访问此拓扑的开发环境。 有关可用 ER API 的详细信息，请参阅 [ER 框架 API](er-apis-app73.md)。

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>修改源代码

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>添加数据合同类

将新 **QuestionnairesErReportContract** 类添加到您的 Microsoft Visual Studio 项目中，并编写指定应用于运行配置的 ER 格式的数据合同的代码。

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>添加 UI 构建器类

将新 **QuestionnairesErReportUIBuilder** 类添加到您的 Visual Studio 项目中，并编写代码以生成将用于查找必须运行的 ER 格式的格式映射 ID 的运行时对话框。 提供的代码仅查找包含引用 **[调查表](#DataModeName)** 数据模型的 **数据模型** 类型的数据源的 ER 格式，查找使用 **[根](#RootDefinitionName)** 定义。

> [!NOTE]
> 或者，您可以使用 ER 集成点来筛选 ER 格式。 有关详细信息，请参阅[用于显示格式映射查找的 API](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup)。

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>添加数据提供程序类

将新 **QuestionnairesErReportDP** 类添加到您的 Visual Studio 项目中，并编写引入应用于运行配置的 ER 格式的数据提供程序的代码。 提供的代码仅包含此数据提供程序的数据合同。

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>添加标签文件

将新的 **QuestionnairesErReportLabels\_en-US** 标签文件添加到您的 Visual Studio 项目中，并为新的 UI 资源指定以下标签：

- 包含以下使用美国英语 (en-US) 显示的文本的新菜单项的 **\@QuestionnairesReport** 标签：**Questionnaires report (powered by ER)**
- 计划将选定的 ER 格式作为批处理作业执行时批处理作业标题的 **\@QuestionnairesReportBatchJobDescription** 标签

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>添加报表服务类

将新 **QuestionnairesErReportService** 类添加到您的 Visual Studio 项目中，并编写调用 ER 格式、使用格式映射 ID 加以标识并提供数据合同作为参数的代码。

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

如果必须使用运行应用程序数据的 ER 格式，则必须在格式映射中配置 **数据模型** 类型的数据源。 此数据源通过使用单个根定义来引用指定数据模型的特定部分。 运行 ER 格式时，它将调用此数据源以访问为给定模型和根定义配置的相应 ER 模型映射。

您可以使用此类型的 ER 模型映射，将您可能在源代码中准备并存储为数据合同一部分的所有信息传递到正在运行的 ER 格式。 在 ER 模型映射中，必须配置引用 **[QuestionnairesErReportContract](#DataContractClass)** 类的 **对象** 类型的数据源。 要标识模型映射，必须指定一个调用此模型映射的数据源。 在提供的代码中，此数据源由具有 **[模型](#ModelDSName)** 值的 **ERModelDataSourceName** 常量指定。 若要标识哪个数据源用于在模型映射中公开数据合同，必须指定一个数据源名称。 在提供的代码中，此名称由具有 <a name="DataContractDSName"></a>**RunTimeParameters** 值的 **ParametersDataSourceName** 常量指定。

> [!NOTE]
> 在新环境中，您可能必须刷新 ER 元数据，以可以在 ER 模型映射设计器中使用这种类型的类。 有关详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md#frequently-asked-questions)。

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>添加报表控制器类

将新 **QuestionnairesErReportController** 类添加到您的 Visual Studio 项目中，并根据您的需要，在基于提供的 **QuestionnairesErReportUIBuilder** 类的逻辑构建的对话框中，编写以同步模式或批处理模式运行 ER 格式的代码。

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>添加菜单项

将新的 **QuestionnairesErReport** 菜单项添加到您的 Visual Studio 项目中。 在 **对象** 属性中，此菜单项引用 **QuestionnairesErReportController** 类，用于指定选择和运行 ER 格式的用户权限。 在 **标签** 属性中，此菜单项引用您之前创建的 **\@QuestionnairesReport** 标签，以在应用程序 UI 中呈现正确的文本。

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>向菜单添加菜单项

将现有的 **KM** 菜单添加到您的 Visual Studio 项目中。 您必须在此菜单中添加 **输出** 类型的新 **QuestionnairesErReport** 项目。 此项目必须引用上一节中介绍的 **QuestionnairesErReport** 菜单项。

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>构建 Visual Studio 项目

构建项目以使新菜单项可供用户使用。

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>从应用程序运行格式

1. 转到 **调查表** \> **设计** \> **调查表报表(由 ER 提供支持)**。

    ![在“调查表”模块中选择“调查表报表（由 ER 提供支持）”菜单项来运行配置的 ER 格式。](./media/er-quick-start1-application-menu-modified.png)

2. 在对话框中，在 **格式映射** 字段中，选择 **调查表报表**。
3. 选择 **确定**。
4. 在 **电子报表参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。
5. 选择 **确定** 确认筛选选项。
6. 选择 **确定** 运行报表。

    ![在“电子报表”对话框中指定选择条件。](./media/er-quick-start1-report-run-dialog-page.png)

7. 查看生成的报表。

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>调整设计的 ER 解决方案

您可以修改配置的 ER 解决方案，让它使用您开发的数据提供程序类访问正在运行的 ER 格式的详细信息，并在生成的报表中输入此 ER 格式的名称。

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>修改模型映射

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>添加数据源以访问数据合同对象

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表映射**。
3. 选择 **设计器** 打开 **模型到数据源映射** 页面。
4. 选择 **设计器** 在模型映射设计器中打开选定的映射。
5. 在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\对象**。
6. 在 **数据源** 窗格中，选择 **添加根**。
7. 在对话框中，在 **名称** 字段中，输入 **[RunTimeParameters](#DataContractDSName)**，如 **QuestionnairesErReportService** 类的源代码中所定义的。
8. 在 **类** 字段中，输入 **[QuestionnairesErReportContract](#DataContractClass)**，之前已编码。
9. 选择 **确定**。
10. 展开 **RunTimeParameters**。

添加的数据源提供有关正在运行的 ER 格式映射的记录 ID 的信息。

![ER 模型映射设计器中添加的数据源。](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>添加数据源以访问 ER 格式映射记录

通过添加数据源以访问 ER 格式映射记录，继续编辑所选的模型映射。

1. 在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **Dynamics 365 for Operations\\表记录**。
2. 在 **数据源** 窗格中，选择 **添加根**。
3. 在对话框的 **名称** 字段中，输入 **ER1**。
4. 在 **表** 字段中，输入 **ERFormatMappingTable**。
5. 选择 **确定**。

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>添加数据源以访问正在运行的 ER 格式的格式映射记录

通过添加数据源以访问正在运行的 ER 格式的格式映射记录，继续编辑所选的模型映射。

1. 在 **模型映射设计器** 页的 **数据源类型** 窗格中，选择 **函数\\计算字段**。
2. 在 **数据源** 窗格中，选择 **添加根**。
3. 在对话框的 **名称** 字段中，输入 **ER2**。
4. 选择 **编辑公式**。
5. 在公式编辑器中的 **公式** 字段中，输入 **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**。
6. 选择 **保存**，然后关闭公式编辑器。
7. 选择 **确定**。

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>在数据模型中输入正在运行的 ER 格式的名称

继续编辑所选的模型映射，以在数据模型中输入正在运行的 ER 格式的名称。

1. 在 **模型映射设计器** 页的 **数据模型** 窗格中，展开 **ExecutionContext**，然后选择 **ExecutionContext\\FormatName**。
2. 在 **数据模型** 窗格中，选择 **编辑** 为所选数据模型的字段配置数据绑定。
3. 在公式编辑器中的 **公式** 字段中，输入 **FIRSTORNULL (ER2.'\>Relations'.Format).Name**。
4. 选择 **保存**，然后关闭公式编辑器。

由于您使用了 **FormatName** 字段，配置的模型映射现在公开在执行期间调用此模型映射的 ER 格式的名称。

![在 ER 模型映射设计器中将数据模型字段绑定到添加的数据源的方法。](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>完成模型映射的设计

1. 在 **模型映射设计器** 页上，选择 **保存**。
2. 关闭该页面。
3. 关闭模型映射页。
4. 在 **配置** 页面的配置树中，确保仍选择 **调查表映射** 配置。 然后，在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。
5. 选择 **更改状态** \> **完成**。

此配置的版本 1.2 的状态将从 **草稿** 更改为 **已完成**。 版本 1.2 不能再更改。 此版本包含已配置的模型映射，可以用作其他 ER 配置的基础。 此配置的版本 1.3 将创建，状态为 **草稿**。 您可以编辑此版本来调整 **调查表** 模型映射。

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>修改格式

您可以修改配置的 ER 格式，以使其名称显示在运行 ER 格式时生成的报表的页脚中。

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>添加新格式元素

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表报表**。
3. 选择 **设计器**。
4. 在 **格式设计器** 页中，选择 **报表** 根项。
5. 选择 **添加** 为所选的 **报表** 根项添加新的嵌套格式元素。
6. 选择 **Excel\\页脚**。
7. 在 **名称** 字段中，输入 **页脚**。
8. 选择 **报表\页脚**，然后选择 **添加**。
9. 选择 **文本\\字符串**。

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>绑定添加的格式元素

1. 在 **格式设计器** 页面的 **映射** 选项卡上，在格式树中，为活动的 **页脚\\字符串** 元素选择 **编辑公式**。
2. 在公式编辑器中的 **公式** 字段中，输入 **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**。
3. 选择 **保存**，然后关闭公式编辑器。
4. 选择 **保存**。

配置的格式现在已经修改，以使用 **页脚\\字符串** 元素将其名称输入到生成报表的页脚中。

![在 ER 操作设计器中将页脚格式元素添加到配置的格式。](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>完成格式设计

1. 关闭 **格式设计器** 页。
2. 在 **配置** 页面的配置树中，确保仍选择 **调查表报表** 配置。 然后，在 **版本** 快速选项卡上，选择状态为 **草稿** 的配置版本。
3. 选择 **更改状态** \> **完成**。

此配置的版本 1.2 的状态将从 **草稿** 更改为 **已完成**。 版本 1.2 不能再更改。 此版本包含已配置的格式，可以用作其他 ER 配置的基础。 此配置的版本 1.3 将创建，状态为 **草稿**。 您可以编辑此版本来调整 **调查表** 报表。

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>从应用程序运行格式

1. 转到 **调查表** \> **设计** \> **调查表报表(由 ER 提供支持)**。
2. 在对话框中，在 **格式映射** 字段中，选择 **调查表报表**。
3. 选择 **确定**。
4. 在 **ER 参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。
5. 选择 **确定** 确认筛选选项。
6. 选择 **确定** 运行报表。
7. 查看生成的 Excel 格式的报表。

请注意，生成的报表的页脚包含用于生成报表的 ER 格式的名称。

![以 Excel 格式生成的报表。](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>从 ER 运行格式

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的配置树中，展开 **调查表模型**，然后选择 **调查表报表**。
3. 在操作窗格上，选择 **运行**。
4. 在 **电子报表参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。
5. 选择 **确定** 确认筛选选项。
6. 选择 **确定** 运行报表。
7. 查看生成的 Excel 格式的报表。

请注意，生成的报表的页脚不包含用于生成报表的 ER 格式的名称，因为当数据合同对象被从 ER 运行的 ER 格式调用时，它未被传递到运行的模型映射。

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>为屏幕预览配置格式目标

1. 转到 **组织管理** \> **电子报告** \> **电子报告目标**。
2. 在 **电子报告目标** 页面上，为已配置的 **调查表报表** ER 格式添加目标记录。
3. 在 **文件目标** 快速选项卡上，为已作为配置的 **调查表报表** ER 格式的根元素 [添加](#AddFormatRootElement)的 **报表** 格式组件设置 **屏幕**[目标](er-destination-type-screen.md)。
4. 在 **PDF 转换设置** 快速选项卡上，配置目标以将报表转换为使用 **横向** 页面方向的 [PDF 格式](electronic-reporting-destinations.md#OutputConversionToPDF)。

![在电子报告目标页面上为 ER 格式配置自定义屏幕目标。](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>从应用程序运行格式以作为 PDF 文档预览

1. 转到 **调查表** \> **设计** \> **调查表报表(由 ER 提供支持)**。
2. 在对话框中，在 **格式映射** 字段中，选择 **调查表报表**。
3. 选择 **确定**。
4. 在 **电子报表参数** 对话框的 **要包括的记录** 快速选项卡上，配置筛选选项，以仅包括 **SBCCrsExam** 调查表。
5. 选择 **确定** 确认筛选选项。

    在 **目标** 快速选项卡上，注意 **输出** 字段已设置为 **屏幕**。 如果要更改配置的目标，选择 **更改**。

    ![您可以在其中更改配置目标的 ER 报表运行时对话框。](./media/er-quick-start1-run-settings.png)

6. 选择 **确定** 运行报表。
7. 查看生成的 PDF 格式的报表。

    ![以 PDF 格式生成的报表的屏幕预览。](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [电子申报公式语言](er-formula-language.md)
- [设计多语言报告](er-design-multilingual-reports.md)
- [电子报告框架 API](er-apis-app73.md)
- [CASE 函数](er-functions-logical-case.md)
- [CONCATENATE 函数](er-functions-text-concatenate.md)
- [DATETIMEFORMAT 函数](er-functions-datetime-datetimeformat.md)
- [FILTER 函数](er-functions-list-filter.md)
- [FIRSTORNULL 函数](er-functions-list-firstornull.md)
- [FORMAT 函数](er-functions-text-format.md)
- [IF 函数](er-functions-logical-if.md)
- [ORDERBY 函数](er-functions-list-orderby.md)
- [SESSIONNOW 函数](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
