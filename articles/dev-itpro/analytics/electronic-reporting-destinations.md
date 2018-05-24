---
title: "电子申报目标"
description: "您可以为每个电子申报 (ER) 格式配置和及其输出组件（文件夹或文件）配置目标。 被授予适当访问权限的用户还可以在运行时修改目标设置。 本文介绍 ER 目标管理，支持的目标类型，以及安全考虑。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fb7d0dc8b3ff9e8f1e4ade5cacfeed8f1a6871ab
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="electronic-reporting-destinations"></a>电子申报目标

[!include [banner](../includes/banner.md)]

您可以为每个电子申报 (ER) 格式配置和及其输出组件（文件夹或文件）配置目标。 被授予适当访问权限的用户还可以在运行时修改目标设置。 本文介绍 ER 目标管理，支持的目标类型，以及安全考虑。

电子申报 (ER) 格式配置通常包含至少一个输出组件︰一个文件。 通常情况下，配置包含多个被分组到单个文件夹或者多个文件夹的不同类型（例如，XML、TXT 或 XLSX）的文件输出组件。 ER 目标管理允许您预配置每个组件运行时所发生的情况。 默认情况下，当运行配置时，将显示一个对话框，供用户保存或打开文件。 当您导入 ER 配置且未为其配置任何特定目标时也使用相同的行为。 为主输出组件创建目标后，该目标将覆盖默认行为，并根据目标的设置发送文件夹或文件。

## <a name="availability-and-general-prerequisites"></a>可用性和一般先决条件
ER 目标功能不在 Microsoft Dynamics AX 7.0（2016 年 2 月）中提供。 因此，必须安装 Microsoft Dynamics 365 for Operations 版本 1611（2016 年 11 月），以便使用本主题中描述的所有功能。 也可以安装以下先决条件之一。 但是请注意，这些备用方法提供的 ER 目标体验受到的限制更多。

-   Microsoft Dynamics AX 应用程序版本 7.0.1（2016 年 5 月）
-   ER 目标管理[应用程序修补程序](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

您可以为已导入的 ER 配置以及**电子申报配置**页提供的格式设置目标。

## <a name="overview"></a>概述
ER 目标管理功能通过**组织管理** &gt; **电子申报**提供。 在这里，您可以覆盖配置的默认行为。 导入的配置不在此处显示，直到单击**新建**，然后在**引用**字段中，选择要为其创建目标设置的配置。

[![在“参考”字段中选择一个配置](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

创建一个引用后，您可以创建每个文件夹或文件的文件目标。 

[![创建文件目标](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

> [!NOTE] 
> 您可以为同一格式的每个输出组件创建一个文件目标，如在**文件名**字段中选择的文件夹或文件。 然后可以在**目标设置**对话框中单独启用和禁用文件目标的目标。 **设置**按钮用来控制所选文件目标的所有目标。 在**目标设置**对话框中，您可以通过设置目标的**已启用**选项来分别控制每个目标。

[![“目标设置”对话框](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>目标类型
支持各种类型的目标。 您可以在同一时间禁用或启用所有类型。 通过这种方式，您可以不执行任何操作或将该组件发送到所有已配置的目标。 以下各部分描述了受支持的目标。

### <a name="email-destination"></a>电子邮件目标

设置**已启用**为**是**以通过电子邮件发送输出文件。 启用此选项后，您可以指定电子邮件收件人，以及编辑电子邮件的主题和正文。 可以为电子邮件主题和正文设置固定文本，或者使用 ER 公式动态创建电子邮件文本。 可以通过两种方法为 ER 配置电子邮件地址。 可按照 Finance and Operations 中的“打印管理”功能完成配置的相同方法完成此配置。 也可以通过公式使用 ER 配置的直接引用，解析电子邮件地址。

### <a name="email-address-types"></a>电子邮件地址类型

单击**收件人**或**抄送**字段的**编辑**时，将显示**电子邮件收件人**对话框。 然后可以选择要使用的电子邮件地址类型。

[![“电子邮件收件人”对话框](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>打印管理

如果选择**打印管理电子邮件**类型，则可以在**收件人**字段中输入固定电子邮件地址。 若要使用非固定电子邮件地址，您必须选择文件目标的电子邮件源类型。 支持下列值：**客户**、**供应商**、**目标客户**、**联系人**、**竞争对手**、**工作人员**、**申请人**、**潜在供应商**和**非许可供应商**。 选择电子邮件源类型后，请使用**电子邮件源帐户**字段旁边的按钮打开**公式设计器**窗体。 可以使用此窗体将表示所选方帐户的公式附加到电子邮件目标。

[![配置打印管理电子邮件类型](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

请注意，公式特定于 ER 配置。 在**公式**中，输入客户或供应商当事方类型的文档特定引用。 不是键入，您可以查找表示客户或供应商帐户的数据源节点，然后单击**添加数据源**按钮来更新公式。 例如，如果您使用 ISO 20022 贷方转帐配置，表示供应商帐户的节点是 **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**。 否则，输入任意字符串值，例如 **DE-001**，来保存公式。

[![公式设计器](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

在**电子邮件收件人**对话框中，单击**电子邮件源帐户**字段旁边的回收站永久删除电子邮件源帐户的公式。 也可以打开公式设计器更改以前保存的公式。 若要分配电子邮件地址，单击**编辑**打开**分配电子邮件地址**对话框。

[![分配电子邮件目标的电子邮件地址](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>配置电子邮件

如果所用配置在数据源中有一个表示电子邮件地址的节点，请使用此电子邮件类型。 可使用公式设计器中的数据源和功能获取格式正确的电子邮件地址。

[![分配电子邮件目标的电子邮件地址数据源](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**注意︰** 简单邮件传输协议 (SMTP) 服务器必须配置并可用。 您可以在**系统管理** &gt; **设置** &gt; **电子邮件** &gt; **电子邮件参数**在 Finance and Operations 中指定 SMTP 服务器。

### <a name="archive-destination"></a>归档目标

您可以使用此选项将输出发送到 Microsoft SharePoint 文件夹或 Microsoft Azure Storage。 将**已启用**设置为**是**以将输出发送到由所选文档类型定义的目标。 仅组设置为**文件**的文档类型可供选择。 您在**组织管理** &gt; **文档管理** &gt; **文档类型**定义文档类型。 ER 目标的配置与文档管理系统的配置相同。

[![文档类型页面](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

位置确定文件保存的位置。 启用**存档**目标之后，可将配置的执行结果保存到作业存档中。 可以在**组织管理** &gt; **电子申报** &gt; **电子申报存档作业**中查看结果。 **注意：** 可在 Finance and Operations 中的**组织管理** &gt; **工作区** &gt; **电子申报** &gt; **电子申报参数**中为作业存档选择票据类型。

#### <a name="sharepoint"></a>SharePoint

您可以在指定的 SharePoint 文件夹中保存文件。 您在 **SharePoint** 选项卡上，在**组织管理** &gt; **文档管理** &gt; **文档管理参数**定义默认 SharePoint 服务器。配置 SharePoint 文件夹后，您可以选择该文件夹以充当用于保存该票据类型的 ER 输出的文件夹。 

[![选择 SharePoint 文件夹](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure 储存

将文档类型位置设置为**归档目录**时，您可以将文件保存到 Azure Storage。

### <a name="file-destination"></a>文件目标

如果将**已启用**设置为**是**，配置运行完毕之后，将显示打开或保存对话框。

### <a name="screen-destination"></a>屏幕目标

如果将**已启用**设置为**是**，将创建输出的预览。 可以直接在浏览器窗口中查看某些文件类型，如 XML、TXT 或 PDF。 对于其他文件类型（如 Microsoft Excel 或 Word），将使用 Microsoft Office Online 服务。

### <a name="power-bi-destination"></a>Power BI 目标

将**已启用**设置为**是**，以便使用您的 ER 配置安排数据从您的 Finance and Operations 实例转移至 Microsoft Power BI 服务。 转移的文件存储在必须为该目的而配置的 Microsoft SharePoint Server 实例上。 有关详细信息，请参阅 [使用电子申报配置为 Power BI 提供来自 Finance and Operations 的数据](general-electronic-reporting-report-configuration-get-data-powerbi.md)。 **提示：** 要覆盖默认行为（即，配置的对话框），您可以创建主输出组件的目标引用和文件目标，然后禁用所有目标。

## <a name="security-considerations"></a>安全考虑
两类权限和职责用于 ER 目标。 仅类型控制维护为法人配置的整体目标的功能（即，控制对**电子申报目标**页的访问）。 其他类型控制在运行时应用程序用户覆盖 ER 开发人员或 ER 功能顾问配置的目标设置的功能。

| 角色(AOT 名称)                     | 角色名称                                  | 责任(AOT 名称)                     | 责任名称                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | 电子申报开发人员             | ERFormatDestinationConfigure        | 配置电子报告格式目标                |
| ERFunctionalConsultant              | 电子申报功能顾问 | ERFormatDestinationConfigure        | 配置电子报告格式目标                |
| PaymAccountsPayablePaymentsClerk    | 应付账款付款员            | ERFormatDestinationRuntimeConfigure | 在运行时配置电子报告格式目标 |
| PaymAccountsReceivablePaymentsClerk | 应收账款付款员         | ERFormatDestinationRuntimeConfigure | 在运行时配置电子报告格式目标 |

> [!NOTE]
> 两个权限用于先前职责。 这些权限与对应职责具有相同名称：**ERFormatDestinationConfigure** 和 **ERFormatDestinationRuntimeConfigure**。

## <a name="frequently-asked-questions"></a>常见问题
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>我已导入了电子配置，并在电子申报页看到了它们。 但为何我没在电子申报目标页看到它们？

请确保单击**新建**，然后在**引用**字段选择配置。 在**电子申报目标**页，您只能看到为其配置目标的配置。

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>是否有方法可以定义使用哪个 Azure Storage 帐户和 Azure Blob 存储？

编号 使用为文档管理系统定义和使用的默认 Azure Blob 存储。

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>目标设置中的文件目标的目的是什么？ 该设置有何作用？

**文件**目标用于控制对话框。 如果您启用此目标，或如果未为配置定义目标，在创建输出文件后您将看到打开或保存对话框。

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>能否提供一个引用我可以向其发送电子邮件的供应商帐户的公式的示例？

此公式特定于 ER 配置。 例如，如果您使用 ISO 20022 贷方转账配置，您可以使用 **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** 或 **model.Payments.Creditor.Identification.SourceID** 来获取相关的供应商帐户。

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>格式配置中的一个包含分组到一个文件夹的多个文件（例如，Folder1 包含 File1、File2 和 File3）。 我如何设置目标才能够不创建 Folder1.zip，通过电子邮件 File1，将 File2 发送到 SharePoint，且在配置运行后我可以立即打开 File3？

先决条件是您的格式必须在 ER 配置中可用。 如果您有格式，打开**电子申报目标**页，创建此配置的一个新引用。 然后，您必须有四个文件目标，每个输出组件一个。 创建第一个文件目标，为其命名，如 **Folder**，并选择在您的配置中表示文件夹的文件名。 然后单击**设置**，并确保禁用所有目标。 对于此文件目标，将不创建文件夹。 默认情况下，由于文件和父文件夹之间的层次结构依赖性，文件将以相同方式运行。 换言之，它们不会被随处发送 若要覆盖默认行为，必须再创建三个文件目标，每个文件一个。 在每个目标的目标设置中，必须启用文件应发送到的目标。

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)




