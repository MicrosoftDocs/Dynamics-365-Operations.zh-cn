---
title: "电子申报目标"
description: "您可以为每个电子申报 (ER) 格式配置和及其输出组件（文件夹或文件）配置目标。 被授予适当访问权限的用户还可以在运行时修改目标设置。 本文介绍 ER 目标管理，支持的目标类型，以及安全考虑。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>电子申报目标

您可以为每个电子申报 (ER) 格式配置和及其输出组件（文件夹或文件）配置目标。 被授予适当访问权限的用户还可以在运行时修改目标设置。 本文介绍 ER 目标管理，支持的目标类型，以及安全考虑。

电子申报 (ER) 格式配置通常包含至少一个输出组件︰一个文件。 通常情况下，配置包含多个被分组到单个文件夹或者多个文件夹的不同类型（例如，XML、TXT 或 XLSX）的文件输出组件。 ER 目标管理允许您预配置每个组件运行时所发生的情况。 默认情况下，配置，在运行时，使用户保存或打开文件"对话框。 当您导入 ER 配置且未为其配置任何特定目标时也使用相同的行为。 为主输出组件创建目标后，该目标将覆盖默认行为，并根据目标的设置发送文件夹或文件。

## <a name="availability-and-general-prerequisites"></a>可用性和一般先决条件
目标 ER 功能在 Microsoft Dynamics 365 中是不可用于工序 7.0 (二月) 版本 2016。 因此，您必须安装的工序 (年 11 月 2016 版的 Microsoft Dynamics 365) 使用{{在此：in}}主题中描述的所有功能。 或者，您可以安装以下先决条件之一。 但是，请注意这些覆盖提供更有限的 ER 目标体验。

-   工序应用程序的版本 7.0.1 (5 月 2016 Microsoft Dynamics 365)
-   ER 目标管理[应用程序修补程序](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

您可以为已导入的 ER 配置以及**电子申报配置**页提供的格式设置目标。

## <a name="overview"></a>概述
目标 ER 管理功能是可用于组织管理电子** ** &gt; ** **国家/地区报告。 在这里，您可以覆盖配置的默认行为。 导入的配置不在此处显示，直到单击**新建**，然后在**引用**字段中，选择要为其创建目标设置的配置。

[选择一个配置的![] (在参考。/media/ger 目标 2 1611 1024x574.jpg /media/ger 1024x574.jpg 2)](。/media/ger 目标 2 1611.jpg /media/ger 1611.jpg) 

在已创建参考后，您可以创建一个文件的每个目标文件夹，或文件中。 

创建文件的![[] (目标。/media/ger 目标 1611 1024x586.jpg /media/ger)] 1024x586.jpg(。/media/ger 目标 1611.jpg)

**注意：**您可以为同一格式的每个输出组件创建一个文件目标，如在**文件名**字段中选择的文件夹或文件。 然后您可以启用和禁用文件的具体目标的目标。** **目标设置"对话框。 **设置**按钮用来控制所选文件目标的所有目标。 在**目标设置**对话框中，您可以通过设置目标的**已启用**选项来分别控制每个目标。

[] (![目标设置"对话框。/media/ger 目标设置 1024x589.jpg /media/ger)](。/media/ger 目标设置 1611.jpg)

## <a name="destination-types"></a>目标类型
支持各种类型的目标。 您可以在同一时间禁用或启用所有类型。 通过这种方式，您可以不执行任何操作或将该组件发送到所有已配置的目标。 以下各部分描述了受支持的目标。

### <a name="email-destination"></a>电子邮件目标

设置**已启用**为**是**以通过电子邮件发送输出文件。 在此选项后，启用您可以指定电子邮件收件人，以及编辑电子邮件的正文和主题。 您可以在设置电子邮件正文的主题和"定额"文本，也可以使用 ER 配方动态地创建电子邮件文本。 您可以配置 ER 的电子邮件地址通过两种方法。 Dynamics 中 365 的打印管理功能工序的完成这可以用相同方式完成的配置。 或者，可以解决电子邮件地址通过使用为 ER 的配置直接通过参考一配方。

### <a name="email-address-types"></a>电子邮件地址类型

在为单击** **编辑时** **或** "字段中，Cc ** **电子邮件**对话框中。 您可以随后选择电子邮件地址的类型。使用。

电子邮件发送到![[] (对话框。/media/ger 目标电子邮件 1024x588.jpg /media/ger)] 1(。/media/ger 目标电子邮件 1611.jpg /media/ger)

#### <a name="print-management"></a>打印管理

**如果您选择打印管理电子邮件**键入，您可以输入在的固定的电子邮件地址** **目标字段。 要使用不是固定的电子邮件地址，必须选择文件的目标电子邮件源类型。 以下值支持：** ** **客户，供应商** **，目标客户**，** **竞争对手联系人，** ** **，工作人员** **，申请人** **，潜在供应商**和**，非许可**供应商。 在电子邮件选择源类型后，请单击"下一使用按钮**则发送电子邮件源帐户** ** **打开"配方设计器"窗体。 您可以使用此窗体可以附加表示所选方帐户分配给目标电子邮件的配方。

[![配置打印管理] (电子邮件类型。/media/ger 目标电子邮件 1024x588.jpg /media/ger)] 2(。/media/ger 目标电子邮件 1611.jpg /media/ger) 

请注意，公式特定于 ER 配置。 在**公式**中，输入客户或供应商当事方类型的文档特定引用。 不是键入，您可以查找表示客户或供应商帐户的数据源节点，然后单击**添加数据源**按钮来更新公式。 例如，如果您使用 ISO 20022 贷方转帐配置，表示供应商帐户的节点是 **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**。 否则，输入任意字符串值，例如 **DE-001**，来保存公式。

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

**在电子邮件**对话框，请选中旁边的"回收站**则发送电子邮件帐户字段源**永久删除电子邮件源帐户的配方。 或者，请打开"配方设计器更改以前保存的配方。 要将电子邮件地址，请单击打开** ** **编辑分配电子邮件地址**对话框。

[将电子邮件分配目标的![] (电子邮件地址。/media/ger 目标电子邮件 1024x587.jpg /media/ger)] 3(。/media/ger 目标电子邮件 1611.jpg /media/ger)

#### <a name="configuration-email"></a>配置电子邮件

使用此电子邮件类型，则您使用的配置具有表示电子邮件地址的节点在数据源。 您在"配方设计器可以使用数据源与功能得到一个正确格式的电子邮件地址。

[将电子邮件分配目标的![一电子邮件地址] (数据源。/media/ger 目标电子邮件 1024x587.jpg /media/ger)] 4(。/media/ger 目标电子邮件 1611.jpg /media/ger) 

**注意︰**简单邮件传输协议 (SMTP) 服务器必须配置并可用。 在 Dynamics 365 可以指定所 SMTP 服务器为工序，在**系统管理** &gt; **设置** &gt; **电子邮件** &gt; ** **电子邮件参数。

### <a name="archive-destination"></a>归档目标

您可以使用此选项将输出发送到 Microsoft SharePoint 文件夹或 Microsoft Azure Storage。 将**已启用**设置为**是**以将输出发送到由所选文档类型定义的目标。 仅组设置为**文件**的文档类型可供选择。 您定义文档类型在**组织管理** &gt; **文档管理** &gt; ** **文档类型。 ER 目标的配置与文档管理系统的配置相同。

[] (![文档类型页心。/media/ger_documenttypefile-1024x542.jpg)](。/media/ger_documenttypefile.jpg) 

位置确定文件保存的位置。 **在存档**该目标后，启用配置执行结果可以在存档中保存该作业。 您可以在以下位置查看结果。**组织管理** &gt; **电子国家/地区报告** &gt; **电子国家/地区报告**存档的作业。 **注释：** **可以在组织管理** **工作区将作业选择存档的单据类型工序的 Dynamics 的 &gt; 365，** &gt; **电子国家/地区报告** &gt; **电子申报参数**国家/地区。

#### <a name="sharepoint"></a>SharePoint

您可以在指定的 SharePoint 文件夹中保存文件。 您定义默认服务器在 SharePoint **组织管理** &gt; **文档管理** &gt; **文档管理参数** **，在 SharePoint **选项卡。 在 SharePoint 文件夹配置后，您可以选择该 ER 为输出为文档类型将保存的文件夹。 

选择文件夹的![SharePoint [] (。/media/ger_sharepointfolderselection-1024x543.jpg)](。/media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure 储存

将文档类型位置设置为**归档目录**时，您可以将文件保存到 Azure Storage。

### <a name="file-destination"></a>文件目标

如果您设置为启用** ** ** **是，则打开或保存该对话框将在配置完成运行。

### <a name="screen-destination"></a>目标屏幕

如果您设置为启用** ** ** **是，输出的预览创建。 可以查看这些文件类型，例如 TXT XML、或 PDF，则在查看器窗口。 对于其他文件类型，Microsoft Office，联机服务通过使用 Microsoft Excel 或词语。

### <a name="power-bi-destination"></a>Power BI 目标

**集启用**到** **是使用您的 ER 为数据转移配置从要将实例的工序到 Microsoft Dynamics 365 的 Power BI 服务。 转移的在文件必须为该配置的目的 Microsoft SharePoint Server 实例存储。 有关详细信息，请参阅工序为 [] (常规电子申报报表的国家/地区配置安全数据 powerbi.md) 使用一国家/地区电子申报 Configuration 提供 Power BI 与从 Dynamics 365 的数据。 **提示：**要覆盖默认行为（即，配置的对话框），您可以创建主输出组件的目标引用和文件目标，然后禁用所有目标。

## <a name="security-considerations"></a>安全考虑
两类权限和职责用于 ER 目标。 一种类型控制能够维护即为法人的整体目标 (它配置到**电子国家/地区报告目标**控制页面的访问。) 其他类型控制在运行时应用程序用户覆盖 ER 开发人员或 ER 功能顾问配置的目标设置的功能。

| 角色(AOT 名称)                     | 角色名称                                  | 责任(AOT 名称)                     | 责任名称                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | 电子申报开发人员             | ERFormatDestinationConfigure        | 配置电子报告格式目标                |
| ERFunctionalConsultant              | 电子申报功能顾问 | ERFormatDestinationConfigure        | 配置电子报告格式目标                |
| PaymAccountsPayablePaymentsClerk    | 应付帐款付款员            | ERFormatDestinationRuntimeConfigure | 在运行时配置电子报告格式目标 |
| PaymAccountsReceivablePaymentsClerk | 应收帐款付款员         | ERFormatDestinationRuntimeConfigure | 在运行时配置电子报告格式目标 |

**注意：**两个权限用于先前职责。 这些权限与对应职责具有相同名称：**ERFormatDestinationConfigure** 和 **ERFormatDestinationRuntimeConfigure**。

## <a name="frequently-asked-questions"></a>常见问题
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>我已导入了电子配置，并在电子申报页看到了它们。 为什么，但未看到它们在电子国家/地区报告目标页面？

务必在** **参考字段**单击新**然后选择一个配置。 在**电子申报目标**页，您只能看到为其配置目标的配置。

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>是否有用于存储 Azure ML 的帐户和滴的任何一个存储方式定义？

编号 为文档管理系统中定义和使用的默认 Azure 的一滴存储。

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>什么是文件目标的用途在设置目标的？ 该设置有何作用？

**文件**目标用于控制对话框。 如果您实现此目标，或者，如果没有为目标定义配置，您将看到一个打开或保存该对话框，在创建输出文件后。

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>能否提供一个引用我可以向其发送电子邮件的供应商帐户的公式的示例？

此公式特定于 ER 配置。 例如，如果您使用 ISO 20022 贷方转账配置，您可以使用 **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** 或 **model.Payments.Creditor.Identification.SourceID** 来获取相关的供应商帐户。

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>格式配置中的一个包含分组到一个文件夹的多个文件（例如，Folder1 包含 File1、File2 和 File3）。 我如何设置目标才能够不创建 Folder1.zip，通过电子邮件 File1，将 File2 发送到 SharePoint，且在配置运行后我可以立即打开 File3？

先决条件是您的格式必须可用在 ER 配置中。 如果您有格式，打开**电子申报目标**页，创建此配置的一个新引用。 然后，您必须有四个文件目标，每个输出组件一个。 创建第一个文件目标，为其命名，如 **Folder**，并选择在您的配置中表示文件夹的文件名。 然后单击**设置**，并确保禁用所有目标。 对于此文件目标，将不创建文件夹。 默认情况下，由于文件和父文件夹之间的层次结果依赖性，文件将以相同方式运行。 换言之，它们不会被随处发送 若要覆盖默认行为，必须再创建三个文件目标，每个文件一个。 在每个目标的目标设置中，必须启用文件应发送到的目标。

# <a name="see-also"></a>请参阅

[电子申报概览](general-electronic-reporting.md)


