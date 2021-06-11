---
title: 电子报告 (ER) 目标
description: 本主题提供有关电子报告目标管理、受支持的目标类型以及安全注意事项的信息。
author: nselin
ms.date: 05/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 088f1b13e20602345dbec5179c343e27be9cec44
ms.sourcegitcommit: 2cd82983357b32f70f4e4a0c15d4d1f69e08bd54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085492"
---
# <a name="electronic-reporting-er-destinations"></a>电子报告 (ER) 目标

[!include [banner](../includes/banner.md)]

您可以为每个电子申报 (ER) 格式配置和及其输出组件（文件夹或文件）配置目标。 具有相应的访问权限的用户还可以在运行时修改目标设置。 本主题介绍 ER 目标管理、支持的目标类型以及安全注意事项。

ER 格式配置通常包含至少一个输出组件︰一个文件。 通常情况下，配置包含多个被分组到单个文件夹或者多个文件夹的不同类型（例如，XML、TXT、XLSX、DOCX 或 PDF）的文件输出组件。 ER 目标管理允许您预配置每个组件运行时所发生的情况。 默认情况下，当运行配置时，将显示一个对话框，供您保存或打开文件。 当您导入 ER 配置且未为其配置任何特定目标时也会发生相同的行为。 为主输出组件创建目标后，该目标将覆盖默认行为，并根据目标的设置发送文件夹或文件。

## <a name="availability-and-general-prerequisites"></a>可用性和一般先决条件

ER 目标功能不在 Microsoft Dynamics AX 7.0（2016 年 2 月）中提供。 因此，您必须安装 Microsoft Dynamics 365 for Operations 版本 1611（2016 年 11 月）或更高版本才能使用以下目标类型：

- [电子邮件地址](er-destination-type-email.md)
- [存档](er-destination-type-archive.md)
- [文件](er-destination-type-file.md)
- [屏幕](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

也可以安装以下先决条件之一。 但是请注意，这些备用方法提供的 ER 目标体验受到的限制更多。

- Microsoft Dynamics AX 应用程序版本 7.0.1（2016 年 5 月）
- [电子报告目标管理应用程序修补程序](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

还有一个[打印](er-destination-type-print.md)目标类型。 要使用它，您必须安装 Microsoft Dynamics 365 Finance 版本 10.0.9（2020 年 4 月）。

## <a name="overview"></a>概览

您只能为已 [导入](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally)到 Finance 实例的 ER 配置以及 **电子报告配置** 页提供的格式设置目标。 ER 目标管理功能在 **组织管理** \> **电子报告** \> **电子报告目标** 中可用。

### <a name="default-behavior"></a>默认行为

ER 格式配置的默认行为取决于您在 ER 格式启动时指定的执行类型。

在 **内部统计报表** 对话框中的 **在后台运行** 快速选项卡上，如果将 **批处理** 选项设置为 **否**，则会直接在互动模式下运行 ER 格式。 成功完成此执行后，可以下载生成的出站文档。

如果将 **批处理** 选项设置为 **是**，则 ER 格式会在[批](../sysadmin/batch-processing-overview.md)模式下运行。 系统会根据您在 **ER 参数** 对话框的 **在后台运行** 选项卡上指定的参数创建适当的批处理作业。

> [!NOTE]
> 作业描述通知您 ER 格式映射运行相关信息。 它还包含已运行的 ER 组件的名称。

[![运行 ER 格式](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

您可以在以下几个地方找到有关此作业的信息：

- 转到 **公用** \> **查询** \> **批处理作业** \> **我的批处理作业** 以检查计划作业的状态。
- 转到 **组织管理** \> **电子申报** \> **电子申报作业**，以检查计划作业的状态以及已完成作业的执行结果。 作业执行成功完成后，请在 **电子申报作业** 页面上选择 **显示文件**，以获取生成的出站文档。

    > [!NOTE]
    > 该文档存储为当前作业记录的附件，并受[文档管理](../../fin-ops/organization-administration/configure-document-management.md)框架控制。 [ER 参数](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)中配置了用于存储此类 ER 项目的[文档类型](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types)。

- 在 **电子申报作业** 页面上选择 **显示文件**，以查看作业执行期间生成的任何错误和警告的列表。

    [![审阅 ER 作业列表](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>用户配置的行为

在 **电子报告目标** 页面上，您可以覆盖配置的默认行为。 直到选择 **新建**，然后在 **引用** 字段中选择要为其创建目标设置的配置，才会在此页面上显示导入的配置。

[![在“参考”字段中选择一个配置](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

创建引用后，可以为引用的 ER 格式的每个 **文件夹** 或 **文件** 输出组件创建文件目标。

[![创建文件目标](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

然后，在 **目标设置** 对话框中，您可以针对文件目标启用和禁用单个目标。 **设置** 按钮用来控制所选文件目标的所有目标。 在 **目标设置** 对话框中，您可以通过设置目标的 **已启用** 选项来分别控制每个目标。

在 **版本 10.0.9 之前** 的 Finance 版本中，您可以为同一格式的每个输出组件创建 **一个文件目标**，如在 **文件名** 字段中选择的文件夹或文件。 但是，在 **版本 10.0.9 及更高版本** 中，您可以为相同格式的每个输出组件创建 **多个文件目标**。

例如，您可以使用此功能为用于生成 Excel 格式出站文档的文件组件配置文件目标。 可以配置一个目标 ([存档](er-destination-type-archive.md))，以将原始 Excel 文件存储在 ER 作业归档文件中；可以配置另一个目标([电子邮件](er-destination-type-email.md))，以同时将 Excel 文件[转换](#OutputConversionToPDF)为 PDF 格式，并通过电子邮件发送 PDF 文件。

[![为单个格式元素配置多个目标](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

运行 ER 格式时，始终会运行为该格式的组件配置的所有目标。 此外，在 Finance **版本 10.0.17 和更高版本** 中，ER 目标功能已得到改进，现在您可以为单个 ER 格式配置不同的目标集。 此配置将每个集标记为为特定用户操作配置。 ER API [已扩展](er-apis-app10-0-17.md)，因此可以提供用户通过运行 ER 格式执行的操作。 提供的操作代码将传递到 ER 目标。 您可以运行 ER 格式的不同目标，具体取决于提供的操作代码。 有关详细信息，请参阅[配置依赖操作的 ER 目标](er-action-dependent-destinations.md)。

## <a name="destination-types"></a>目标类型

ER 格式当前支持以下目标。 您可以在同一时间禁用或启用所有类型。 通过这种方式，您可以不执行任何操作或将该组件发送到所有已配置的目标。

- [电子邮件地址](er-destination-type-email.md)
- [存档](er-destination-type-archive.md)
- [文件](er-destination-type-file.md)
- [屏幕](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [打印](er-destination-type-print.md)

## <a name="applicability"></a>适用性

您可以为已导入的 ER 配置以及 **电子申报配置** 页提供的格式设置目标。

> [!NOTE]
> 配置的目标特定于公司。 如果计划在当前 Finance 实例的不同公司中使用 ER 格式，则必须为每个公司配置的该 ER 格式的目标。

在为选定格式配置文件目标时，可以针对整个格式配置它们。

[![配置链接](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

同时，您可能有该格式的多个已导入到当前 Finance 实例中的[版本](general-electronic-reporting.md#component-versioning)。 如果您选择在选择 **参考** 字段时提供的配置 **链接**，则可以查看它们。

[![配置版本](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

默认情况下，仅当您运行状态为 **已完成** 或 **已共享** 的 ER 格式版本时，才会应用配置的目标。 但是，有时在运行 ER 格式的草稿版本时必须使用配置的目标。 例如，您修改格式的草稿版本，并且想要使用配置的目标来测试将如何传递生成的输出。 运行草稿版本时，请按照以下步骤为 ER 格式应用目标。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 将 **将目标用于草稿状态** 选项设置为 **是**。

[![将目标用于草稿状态选项](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

要使用 ER 格式的草稿版本，必须相应地标记 ER 格式。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 将 **运行设置** 选项设置为 **是**。

[![运行设置选项](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

完成此设置后，**运行草稿** 选项可用于您修改的 ER 格式。 将此选项设置为 **是**，以在运行格式时开始使用该格式的草稿版本。

[![运行草稿选项](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>目标故障处理

通常，ER 格式在特定业务流程范围内运行。 但是，在执行 ER 格式期间生成的出站文档的交付有时必须被视为该业务流程的一部分。 在这种情况下，如果将生成的出站文档传送到配置的目标失败，则必须取消执行业务流程。 要配置适当的 ER 目标，请选择 **失败时停止处理** 选项。

例如，您配置供应商付款处理，以便运行 **ISO20022 贷方转帐** ER 格式以生成付款文件和补充文件（例如，随函和控制报表）。 如果仅在通过电子邮件成功发送随函后才应该认为付款已成功处理，则必须针对适当文件目标中的 **随函** 组件选中 **失败时停止处理** 复选框，如下图所示。 在这种情况下，仅当成功接受了生成的随函以由 Finance 实例中配置的电子邮件提供程序传送时，所选择要处理的付款的状态才将从 **无** 更改 **已发送**。

[![为文件目标故障配置流程处理](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

如果针对目标中的 **随函** 组件清除 **失败时停止处理** 复选框，则付款将被认为已成功处理，即使未通过电子邮件成功传送随函也不例外。 即使无法发送随函，比如说因收件人或发件人的电子邮件地址丢失或不正确，付款状态也将从 **无** 更改为 **已发送**。

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>输出转换为 PDF

您可以使用 PDF 转换选项将 Microsoft Office（Excel 或 Word）格式的输出转换为 PDF 格式。

### <a name="make-pdf-conversion-available"></a>使 PDF 转换可用

要在当前的 Finance 实例中提供 PDF 转换选项，请打开 **功能管理** 工作区，然后打开 **将电子报告传出文档从 Microsoft Office 格式转换为 PDF** 功能。

[![在功能管理中打开传出文档 PDF 转换功能](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>适用性

只能对用于以 Office（Excel 或 Word）格式（**Excel 文件**）生成输出的文件组件打开 PDF 转换选项。 启用此选项后，以 Office 格式生成的输出会自动转换为 PDF 格式。 在 **版本 10.0.18 之前** 的 Finance 版本中，您只能为 **Excel\\ 文件** 类型的组件打开此选项，这些组件用于生成 [Excel](er-fillable-excel.md) 或 [Word](er-design-configuration-word.md) 格式的输出。 但是，在 **版本 10.0.18 及更高版本** 中，您还可以为 **常见\\文件** 类型的组件打开此选项。

> [!NOTE]
> 当您针对 **常见\\文件** 类型的 ER 组件打开 PDF 转换选项时，请注意收到的警告消息。 该消息通知您，在设计时无法保证所选文件组件将在运行时公开 PDF 格式的内容或 PDF 可转换型内容。 因此，只有在确定所选文件组件已配置为在运行时公开 PDF 格式的内容或 PDF 可转换型内容时，才应打开该选项。
> 
> 如果您针对 **Excel\\文件** 类型的组件打开了 PDF 转换选项，该组件以 PDF 以外的格式公开内容，并且公开的内容不能转换为 PDF 格式，则在运行时会发生异常。 您收到的消息会告诉您生成的内容无法转换为 PDF 格式。

### <a name="limitations"></a>限制

PDF 转换选项仅可用于云部署。

生成的 PDF 文档的最大长度为 300 页。

在 Finance **版本 10.0.9** 中，从 Excel 输出生成的 PDF 文档中仅支持横向页面方向。 在 Finance **版本 10.0.10（2020 年 5 月）及更高版本** 中，配置 ER 目标期间，您可以指定从 Excel 输出生成的 PDF 文档的[页面方向](#SelectPdfPageOrientation)。

仅 Windows 操作系统的常用系统字体用于转换不包含嵌入式字体的输出。

### <a name="use-the-pdf-conversion-option"></a>使用 PDF 转换选项

要为文件目标打开 PDF 转换，请选择 **转换成 PDF** 复选框。

[![为文件目标打开 PDF 转换](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">选择 PDF 转换的页面方向</a>

如果您以 Excel 格式生成 ER 配置并将其转换为 PDF 格式，您可以指定 PDF 文档的页面方向。 当您选择 **转换为 PDF** 复选框以打开文件目标（生成 Excel 格式的输出文件）的 PDF 转换时，**页面方向** 字段在 **PDF 转换设置** 快速选项卡上显示。 在 **页面方向** 字段中，选择首选方向。

[![选择 PDF 转换的页面方向](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

> [!NOTE]
> 若要有选择 PDF 页面方向的选项，您必须安装 Finance 版本 10.0.10 或更高版本。
>
> 所选页面方向将应用于以 Excel 格式生成然后转换为 PDF 格式的所有 ER 配置。
>
> 如果将 Word 格式的 ER 配置转换为 PDF 格式，PDF 文档的页面方向将从 Word 文档中获取。

## <a name="output-unfolding"></a>输出展开

当您为电子报告格式的 **文件夹** 组件配置目标时，可以指定该组件的输出如何传递到配置的目标。

### <a name="make-output-unfolding-available"></a>使输出展开可用

要使输出展开选项在当前 Finance 实例中可用，打开 **功能管理** 工作区，然后打开 **允许配置电子报告目标以将文件夹内容作为单独文件发送** 功能。

### <a name="applicability"></a>适用性

输出展开选项只能为 **文件夹** 类型的格式组件配置。 当您开始配置 **文件夹** 组件时，**常规** 快速选项卡在 **电子报告目标** 页将变为可用。 

### <a name="use-the-output-unfolding-option"></a>使用输出展开选项

在 **常规** 快速选项卡上，在 **文件夹发送形式** 字段中，选择以下值之一：

- **ZIP 存档** – 将生成的文件作为 zip 文件传递。
- **单独文件** – 将生成的 zip 文件的每个文件作为一个单独文件传递。

    > [!NOTE]
    > 当您选择 **单独文件** 时，生成的输出以压缩状态在内存中收集。 因此，当实际文件大小可能超过此限制时，将对压缩输出应用最大[文件大小限制](er-compress-outbound-files.md)。 当您预期生成的输出的大小会非常大时，建议您选择此值。

[![为文件夹格式组件配置目标](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>限制

对于包含其他嵌套 **文件夹** 组件的 **文件夹** 组件，如果您将其 **文件夹发送形式** 字段设置为 **单独文件**，此设置不会递归应用于嵌套 **文件夹** 组件。

## <a name="security-considerations"></a>安全考虑

两类权限和职责用于 ER 目标。 一种类型控制用户维护为法人配置的目标的整体功能（即，控制对 **电子报告目标** 页的访问）。 另一种类型控制运行时应用程序用户覆盖 ER 开发人员或 ER 功能顾问配置的目标设置的功能。

| 角色(AOT 名称)                     | 角色名称                                  | 责任(AOT 名称)                     | 责任名称                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | 电子申报开发人员             | ERFormatDestinationConfigure        | 配置电子报告格式目标                |
| ERFunctionalConsultant              | 电子申报功能顾问 | ERFormatDestinationConfigure        | 配置电子报告格式目标                |
| PaymAccountsPayablePaymentsClerk    | 应付帐款付款员            | ERFormatDestinationRuntimeConfigure | 在运行时配置电子报告格式目标 |
| PaymAccountsReceivablePaymentsClerk | 应收帐款付款员         | ERFormatDestinationRuntimeConfigure | 在运行时配置电子报告格式目标 |

> [!NOTE]
> 两个权限用于先前职责。 这些权限与对应职责具有相同名称：**ERFormatDestinationConfigure** 和 **ERFormatDestinationRuntimeConfigure**。

## <a name="frequently-asked-questions"></a>常见问题

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>我已导入了电子配置，并在电子申报页看到了它们。 但为何我没在电子申报目标页看到它们？

请确保选择 **新建**，然后在 **引用** 字段选择配置。 **电子报告目标** 页仅显示为其配置目标的配置。

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>是否有方法可以定义使用哪个 Microsoft Azure Storage 帐户和 Azure Blob 存储？

编号 使用为文档管理系统定义和使用的默认 Microsoft Azure Blob 存储。

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>目标设置中的文件目标的目的是什么？ 该设置有何作用？

当您在交互模式下运行 ER 格式时，**文件** 目标用于控制 Web 浏览器的对话框。 如果您启用此目标，或如果未为配置定义目标，在创建输出文件后将在您的 Web 浏览器中显示打开或保存对话框。

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>能否提供一个引用我可以向其发送电子邮件的供应商帐户的公式的示例？

此公式特定于 ER 配置。 例如，如果您使用 ISO 20022 贷方转帐配置，您可以使用 **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** 或 **model.Payments.Creditor.Identification.SourceID** 来获取相关的供应商帐户。

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>格式配置中的一个包含分组到一个文件夹的多个文件（例如，Folder1 包含 File1、File2 和 File3）。 我如何设置目标才能够不创建 Folder1.zip，通过电子邮件 File1，将 File2 发送到 SharePoint，且在配置运行后我可以立即打开 File3？

您的格式必须首先在 ER 配置中可用。 如果满足了此先决条件，请打开 **电子报告目标** 页，创建此配置的一个新引用。 然后，您必须有四个文件目标，每个输出组件一个。 创建第一个文件目标，为其命名，如 **Folder**，并选择在您的配置中表示文件夹的文件名。 然后选择 **设置**，并确保禁用所有目标。 对于此文件目标，将不创建文件夹。 默认情况下，由于文件和父文件夹之间的层次结构依赖性，文件将以相同方式运行。 换言之，它们不会被随处发送 若要覆盖默认行为，必须再创建三个文件目标，每个文件一个。 在每个目标的目标设置中，必须启用文件应发送到的目标。

## <a name="additional-resources"></a>其他资源

[电子报告 (ER) 概览](general-electronic-reporting.md)

[配置依赖操作的 ER 目标](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
