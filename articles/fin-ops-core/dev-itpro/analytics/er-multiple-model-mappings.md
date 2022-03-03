---
title: 管理单个模型根的多个派生映射
description: 本主题说明如何管理为单个模型根配置的多个派生映射。
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d71b05b3f2eda93a93f728926e675c040371781e
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324104"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>管理单个模型根的多个派生映射

[!include [banner](../includes/banner.md)]

[电子报告 (ER)](general-electronic-reporting.md) 数据模型组件在每个配置的 ER 格式组件中用作生成传出文档的数据源。 要描述单个业务域，请配置具有多个根定义的数据模型组件。 

每个根定义让您可以最适合特定报告目的的方式表示该域的数据。 对于每个根定义，您可以将一个 ER 模型映射组件配置为数据模型的 Microsoft Dynamics 365 Finance 特定实现。 通过这种方式，您将描述在运行时数据模型如何填充。

ER 模型映射组件可以放在 ER 数据模型[配置](general-electronic-reporting.md#Configuration)和 ER 模型映射配置中。 单个 ER 配置可以包含多个映射组件，每个映射组件针对单个根定义进行配置。 或者，单个 ER 配置可以仅包含为单个根定义配置的一个映射组件。

多个配置提供程序可能会为同一个 ER 数据模型提供 ER 模型映射配置。 这些模型映射配置可能包含不同根定义的映射组件。 您可以对一个[提供程序](general-electronic-reporting.md#Provider)提供的一个根定义使用一个模型映射，对另一个提供程序提供的另一个根定义使用一个模型映射。

本主题中的过程说明当 ER 模型映射配置包含为同一个根定义配置的不同模型映射组件时，如何管理 ER 数据模型的多个 ER 模型映射配置。 

要完成本主题中的过程，您必须被分配系统管理员或电子报告开发人员角色。

以下所有过程均可在 USMF 公司中完成。 无需进行编码。

## <a name="configure-the-er-framework"></a>配置 ER 框架

作为具有电子报告开发人员角色的用户，在使用 ER 框架生成业务文档之前，请先[配置最小 ER 参数集](er-quick-start2-customize-report.md#ConfigureFramework)。

## <a name="import-the-standard-er-format-configurations"></a>导入标准 ER 格式配置

若要向当前 Finance 实例添加标准 ER 配置，必须从为该实例配置的 ER 存储库中导入这些配置。 按照[从配置服务的全局存储库下载 ER 配置](er-download-configurations-global-repo.md)中的步骤导入以下 ER 格式配置：

- **普通发票 (Excel)**，版本 220.106
- **项目发票 (Excel)**，版本 226.27

## <a name="review-the-imported-er-configurations"></a>查看导入的 ER 配置

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。
3. 在 **配置** 页的左侧窗格的配置树中，展开 **发票模型**。

    ![在“配置”页面上查看导入的配置。](./media/er-multiple-model-mappings-image1.png)

4. 查看 **普通发票 (Excel)** 格式：

    1. 在左侧窗格的配置树中，选择 **普通发票 (Excel)**。
    2. 在操作窗格上，选择 **设计器**。
    3. 在 **格式设计器** 页上的 **映射** 选项卡上，在数据源列表中，选择 **模型**。
    4. 选择 **查看**。
    
       当前 ER 格式配置为使用 **发票模型** 的 **InvoiceCustomer** 根定义。 当运行此格式并调用 **模型** 数据源时，为 **InvoiceCustomer** 根定义配置的模型映射用于访问应用程序数据和填充数据模型。

        ![在“格式设计器”页面上查看模型数据源。](./media/er-multiple-model-mappings-image2.png)

    6. 关闭 **格式设计器** 页。

5. 查看 **发票模型映射** 配置的内容：

    1. 在左侧窗格的配置树中，选择 **发票模型映射**。
    2. 在操作窗格上，选择 **设计器**。
    3. 在 **模型到数据源映射** 页上，注意当前的 ER 模型映射配置包含几个模型映射组件：

        + **客户发票** 模型映射是为 **发票模型** 的 **InvoiceCustomer** 根定义配置的。 因此，当 **普通发票 (Excel)** ER 格式运行时，可以选择此 ER 配置的 **客户发票** 模型映射来访问应用程序数据和填充数据模型。
        + **项目发票** 模型映射是为 **发票模型** 的 **InvoiceProject** 根定义配置的。 因此，当 **项目发票 (Excel)** ER 格式运行时，可以选择此 ER 配置的 **项目发票** 模型映射来访问应用程序数据和填充数据模型。

        ![“模型到数据源映射”页面上的发票模型映射。](./media/er-multiple-model-mappings-image3.png)

    4. 关闭 **模型到数据源映射** 页。
    5. 在 **版本** 快速选项卡上，选择 **删除** 删除此 ER 配置所有晚于 240.175 版本的版本。

6. 查看 **项目发票模型映射(RDP)** 配置的内容：

    1. 在左侧窗格的配置树中，选择 **项目发票模型映射(RDP)**。
    2. 在操作窗格上，选择 **设计器**。
    3. 在 **模型到数据源映射** 页上，注意当前的 ER 模型映射配置包含 **InvoiceProject** 模型映射，并且此模型映射是为 **发票模型** 的 **InvoiceProject** 根定义配置的。 当 **项目发票 (Excel)** ER 格式运行时，选择此 ER 配置的 **InvoiceProject** 模型映射来访问应用程序数据和填充数据模型。

        ![“模型到数据源映射”页面上的项目发票模型映射。](./media/er-multiple-model-mappings-image4.png)

    4. 关闭 **模型到数据源映射** 页。
    5. 在 **版本** 快速选项卡上，选择 **删除** 删除此 ER 配置所有晚于 226.35 版本的版本。

## <a name="customize-the-imported-er-configurations"></a>自定义导入的 ER 配置

本节说明如何[自定义](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) Microsoft 提供的模型映射。 例如，可能需要自定义来实现您的自定义逻辑或添加缺少的绑定。

### <a name="customize-the-invoice-model-mapping-configuration"></a>自定义发票模型映射配置

1. 在 **配置** 页面上，在左侧窗格的配置树中，选择 **发票模型映射**。
2. 在操作窗格中选择 **创建配置**。
3. 在 **创建配置** 下拉对话框的 **新建** 字段中，选择 **从名称派生: 发票模型映射, Microsoft**。
4. 在 **名称** 字段中，输入 **发票模型映射 Litware**。
5. 选择 **创建配置**。
6. 将派生映射的[草稿](general-electronic-reporting.md#component-versioning)版本[标记](er-quick-start2-customize-report.md#MarkFormatRunnable)为可以在运行时使用：

    1. 在操作窗格的 **配置** 选项卡上，在 **高级设置** 组中，选择 **用户参数**。
    2. 在 **使用参数** 对话框中，将 **运行设置** 选项设置为 **是**，然后选择 **确定**。
    3. 根据需要，选择 **编辑** 使页面可供编辑。
    4. 对于配置树中当前选择的 **发票模型映射 Litware** 配置，将 **运行草稿** 选项设置为 **是**。

7. 在操作窗格上，选择 **设计器** 查看此配置的模型映射。

    ![在“模型到数据源映射”页面上查看发票模型映射。](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > 现在，您可以在设计器中打开此 ER 配置的任何 ER 模型映射组件，来配置您的自定义逻辑。 有关详细信息，请参阅[自定义模型映射配置](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration)。

8. 关闭 **模型到数据源映射** 页。

现在，您有 **发票模型映射** 和 **发票模型映射 Litware** 配置，每个配置都有为 **InvoiceCustomer** 根定义配置的模型映射。 明确指定其中一个模型映射作为任何 ER 格式所使用的默认模型映射，如包含具有 **InvoiceCustomer** 根定义的模型数据源的 **普通发票 (Excel)** 格式。 否则，当您运行、编辑或验证其中一个 ER 格式时，将引发以下异常，通知您未明确分配默认模型映射：
 
> 配置 \<configuration names separated by commas\> 中的“\<model name\> (\<root descriptor\>)”数据模型存在多个模型映射。 将其中一个配置设置为默认配置。

![在“配置”页面上打开格式进行编辑。](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>自定义项目发票模型映射 (RDP) 配置

1. 在 **配置** 页面上，在左侧窗格的配置树中，选择 **项目发票模型映射 (RDP)**。
2. 在操作窗格中选择 **创建配置**。
3. 在 **创建配置** 对话框的 **新建** 字段中，选择 **从名称派生: 项目发票模型映射 (RDP), Microsoft**。
4. 在 **名称** 字段中，输入 **项目发票模型映射 Litware**。
5. 选择 **创建配置**。
6. 对于配置树中当前选择的 **项目发票模型映射 Litware** 配置，将 **运行草稿** 选项设置为 **是**。
7. 在操作窗格上，选择 **设计器** 查看此配置的模型映射。

    ![在“模型到数据源映射”页面上查看自定义的项目发票模型映射。](./media/er-multiple-model-mappings-image7.png)

8. 关闭 **模型到数据源映射** 页。

您现在有 **发票模型映射**、**项目发票模型映射 (RDP)** 和 **项目发票模型映射 Litware** 配置。 这些配置中的每一个都为 **InvoiceProject** 根定义配置了模型映射。 明确分配其中一个模型映射作为任何 ER 格式使用的默认模型映射。 例如，使用包含具有 **InvoiceProject** 根定义的模型数据源的 **项目发票 (Excel)** 格式。 否则，当您运行或编辑其中一个 ER 格式时，将引发异常，通知您未明确分配默认模型映射。

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>选择派生的“发票模型映射 Litware”配置作为包含默认模型映射的配置

1. 在 **配置** 页面上，在左侧窗格的配置树中，选择 **发票模型映射 Litware**。
2. 将 **模型映射的默认值** 选项设置为 **是**。

    ![在“配置”页面上将模型映射设置为默认模型映射。](./media/er-multiple-model-mappings-image8.png)

    由于此设置，当您运行 **普通发票 (Excel)** 或对其进行编辑或验证时，将使用 **客户发票副本** 模型映射。 **发票模型映射** 配置中的 **客户发票** 模型映射将被忽略。

    您现在可以打开 **普通发票 (Excel)** 格式来在格式设计器中查看。

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>选择派生的“项目发票模型映射 Litware”配置作为包含默认模型映射的配置

1. 在 **配置** 页面上，在左侧窗格的配置树中，选择 **项目发票模型映射 Litware**。
2. 将 **模型映射的默认值** 选项设置为 **是**。

    在这种情况下，与上一节中介绍的 **发票模型映射 Litware** 配置的情况不同，您无法从 **项目发票模型映射 Litware** 配置开始使用 **InvoiceProject 副本** 模型映射。 包含 **InvoiceProject** 根定义的模型映射的两个配置当前被标记为默认配置。 因此，它们具有相同的使用优先级。 要解决此问题，请完成此过程的其余步骤。

3. 在左侧窗格的配置树中，选择 **发票模型映射 Litware**。
4. 在操作窗格上，选择 **设计器**。
5. 在 **模型到数据源映射** 页上，根据需要选择 **编辑** 让页面可编辑。
6. 选择 **项目发票副本** 模型映射，然后选择它对应的 **已删除** 复选框。

    ![在“模型到数据源映射”页面上将模型映射设置为虚拟删除。](./media/er-multiple-model-mappings-image9.png)

    由于此设置，**发票模型映射 Litware** 配置被视为没有 **InvoiceProject** 根定义的模型映射。 将默认发布 **InvoiceProject 副本** 模型映射。 包含此模型映射的配置 **项目发票模型映射 Litware** 被标记为默认配置。 由于被标记为默认配置，它的优先级高于 **项目发票模型映射 (RDP)** 配置中的 **InvoiceProject** 模型映射。

## <a name="other-considerations"></a>其他注意事项

**项目发票模型映射 Litware** 配置的 **InvoiceProject 副本** 模型映射被设计为使用 **ReportDataProvider** 数据源。 此数据源是引用 **PsaProjInvoiceDP** 应用程序类的 *对象* 类型的一部分。 此类作为打印管理框架的项目发票 SQL Server Reporting Services (SSRS) 报表的数据提供程序实现。 选择此数据源作为 ER [集成点](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents)。 打印管理报表的当前 ER 实现会考虑此设置。 有关更多详细信息，请查看 **ERPrintMgmtDataProviderReport** 应用程序类的源代码。 在运行时，将 **ReportDataProvider** 数据源作为模型映射集成点分配，会强制 Finance 将此映射组件视为具有高于 **项目发票模型映射 (RDP)** 配置中的 **InvoiceProject** 映射组件的优先级。

## <a name="see-also"></a>请参阅

- [管理单独电子报告配置中的电子报告模型映射](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [配置与国家/地区上下文相关的电子报告模型映射](er-country-dependent-model-mapping.md)
- [电子报告框架 API 更改](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
