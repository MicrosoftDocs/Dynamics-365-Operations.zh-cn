---
title: 电子邮件 ER 目标类型
description: 本文说明如何为电子报告 (ER) 格式的每个文件夹或文件组件配置电子邮件目标。
author: kfend
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 5e58618618d9125db4c81f49f62f48c2ce2f5e62
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285416"
---
# <a name="email-er-destination-type"></a>电子邮件 ER 目标类型

[!include [banner](../includes/banner.md)]

运行电子申报 (ER) 格式时，可以生成一个或多个传出文档。 ER 格式中使用 **文件夹** 或 **文件** 格式组件指定传出文档的结构。 您可以为这些类型的组件配置电子邮件目标，以将传出文档作为电子邮件附件发送。

您可以为 ER 格式的每个 **文件夹** 或 **文件** 组件配置电子邮件目标。 在此示例中，**每个传出文档分别通过电子邮件发送**。 根据此目标设置，将生成的文档作为电子邮件的附件进行传递。 

> [!NOTE]
> 如果没有生成文档，因为已经为相关 **文件** 组件配置了 **已启用** 表达式，以便返回 **False** 布尔值，所以不会发送任何电子邮件，即使为组件配置并启用了电子邮件目标。

你也可以 [组合](#grouping)多个 **文件夹** 或 **文件** 在一些，然后为该组中的所有组件配置一个电子邮件目标。 在这种情况下，属于该组的组件生成的所有传出文档 **作为一封电子邮件的多个附件发送**。 根据此目标设置，将生成的每个文档作为一封电子邮件的附件进行传递。

> [!NOTE]
> 如果一组组件中的一个 **文件** 生成了至少一个文档，将发送一封电子邮件。 如果组合组件没有生成文档，因为已经配置了每个 **文件** 组件的 **已启用** 表达式，以便返回 **False** 布尔值，所以不会发送任何电子邮件，即使为该组组件配置并启用了电子邮件目标。
>
> **电子邮件** 是唯一可以为一组组件配置的目标。 要传递基于组的电子邮件目标设置通过电子邮件发送的文档，请再添加一个目标记录，选择所需的组件，然后再为此记录配置一个目标。

可以为一个 ER 格式配置配置多组组件。 这样，您可以为每组组件配置一个电子邮件目标，并为每个组件配置一个电子邮件目标。

## <a name="enable-an-email-destination"></a>启用电子邮件目标

要通过电子邮件发送一个或多个输出文件，请按照以下步骤操作。

1. 在 **电子申报目标** 页面上的 **文件目标** 快速选项卡上，选择网格中的一个或一组组件。
2. 选择 **设置**，然后在 **目标设置** 对话框的 **电子邮件** 选项卡上，将 **已启用** 选项设置为 **是**。

[![将电子邮件目标的“已启用”选项设置为“是”。](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="configure-an-email-destination"></a>配置电子邮件目标

### <a name="email-content"></a>电子邮件内容

您可以编辑电子邮件的主题和正文。

在 **主题** 字段中，输入电子邮件主题文本，此文本应显示在运行时生成的电子消息的主题字段中。 在 **正文** 字段中，输入电子邮件正文文本，此文本应显示在电子消息的正文字段中。 可以为电子邮件主题和正文设置固定文本，或者使用 ER [公式](er-formula-language.md)在运行时动态创建电子邮件文本。 配置的公式必须返回[字符串](er-formula-supported-data-types-primitive.md#string)类型的值。

电子邮件正文采用文本或 HTML 格式组成，具体取决于电子邮件客户端。 可使用 HTML 和内嵌级联样式表 (CSS) 允许的任何布局、样式和品牌。

> [!NOTE]
> 每个电子邮件客户端实施的布局和样式限制可能需要调整用于消息正文的 HTML 和 CSS。 建议您自己熟悉有关最受欢迎电子邮件客户端将支持的 HTML 创建最佳实践。
>
> 使用正确的编码实现回车，具体取决于正文格式。 有关详细信息，请参阅[字符串](er-formula-supported-data-types-primitive.md#string)数据类型的定义。

### <a name="email-addresses"></a>电子邮件地址

您可以指定电子邮件发件人和电子邮件收件人。 默认情况下，将代表当前用户发送电子邮件。 若要指定其他电子邮件发件人，您必须配置 **发件人** 字段。

> [!NOTE]
> 配置电子邮件目标后，**发件人** 字段仅对具有 `ERFormatDestinationSenderEmailConfigure` 安全特权的用户可见，请 **为 ER 格式目标配置发件人电子邮件地址**。
>
> 提供电子邮件目标以在 [运行时](electronic-reporting-destinations.md#security-considerations)修改时，**发件人** 字段仅对具有 `ERFormatDestinationSenderEmailMaintain` 安全特权的用户可见，请 **为 ER 格式目标维护发件人电子邮件地址**。
>
> 当 **发件人** 字段配置为使用当前用户电子邮件地址之外的其他电子邮件地址时，**发送人** 或 **发送人代表** 权限必须提前正确[设置](/microsoft-365/solutions/allow-members-to-send-as-or-send-on-behalf-of-group)。 否则，运行时会引发以下异常：“无法从 \<current user account\> 帐户以 \<from email account\> 身份发送电子邮件，请检查 \<from email account\> 上的“发送人”权限。

您可以配置 **发件人** 字段以返回多个电子邮件地址。 在这种情况下，列表中的第一个地址用作电子邮件发件人地址。

若要指定电子邮件收件人，您必须配置 **收件人** 和 **抄送** 字段（可选）。

可以通过两种方法为 ER 配置电子邮件地址。 可以用打印管理功能所用的相同方式来完成此配置，或者可以通过公式使用 ER 配置的直接引用来解析电子邮件地址。

## <a name="email-address-types"></a>电子邮件地址类型

如果选择 **目标设置** 对话框中 **发件人**、**收件人** 或 **抄送** 旁边的 **编辑**，将显示相应的 **电子邮件发件人**、**电子邮件收件人** 或 **电子邮件抄送** 对话框。 在那里，您可以配置电子邮件发件人和电子邮件收件人。 选择 **添加**，然后选择要使用的电子邮件地址类型。 现在支持两种类型：**打印管理电子邮件** 和 **配置电子邮件**。

[![选择电子邮件地址的类型。](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>打印管理电子邮件

如果选择 **打印管理电子邮件** 作为电子邮件地址类型，您可以通过设置以下字段在 **电子邮件发件人**、**电子邮件收件人** 或 **电子邮件抄送** 对话框中输入固定电子邮件地址：

- 在 **电子邮件源** 字段中，选择 **无**。
- 在 **更多电子邮件，以“;”分隔** 字段中，输入固定电子邮件地址。

或者，您也可以从为其生成传出文档的一方的联系方式详细信息中获取电子邮件地址。 若要使用非固定电子邮件地址，请在 **电子邮件源** 字段中为文件目标选择相关方的[角色](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles)。 支持以下角色：

- 客户
- 供应商
- 目标客户
- 联系人
- 竞争对手
- 工作线程
- 申请人
- 潜在供应商
- 非许可供应商
- 法人

例如，若要为用于处理供应商付款的 ER 格式配置电子邮件目标，请选择 **供应商** 角色。

选择所需角色之后，选择 **电子邮件源帐户** 字段旁边的 **绑定** 按钮（链符号）打开[公式设计器](general-electronic-reporting-formula-designer.md)页面。 然后可以使用此页面配置公式，以便在运行时将分配给所配置角色的相关方帐号从处理的文档返回到电子邮件目标。

> [!NOTE]
> 公式特定于 ER 配置。

在 **公式设计器** 页面的 **公式** 字段中，输入对受支持角色的特定于文档的引用。 请不要键入此引用，而是在 **数据源** 页面中找到并选择表示所配置角色的帐户的数据源节点，然后选择 **添加数据源** 以更新公式。 例如，如果为用于处理供应商付款的 **ISO 20022 贷方转帐** 配置配置电子邮件目标，则提供供应商帐户的角色为 `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`。

![配置电子邮件源帐户。](./media/er_destinations-emaildefineaddresssource.gif)

如果所配置角色的帐号对整个 Microsoft Dynamics 365 Finance 实例是唯一的，则 **电子邮件收件人** 对话框中的 **电子邮件源公司** 字段可以保留为空。

或者，您可能会遇到以下情况：[全球通讯录](../../fin-ops/organization-administration/overview-global-address-book.md)中的不同相关方已在不同公司（[法人](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)）按照全部使用同一个帐号以填充所配置角色的方式注册。 在这种情况下，所配置角色的帐号在整个 Finance 实例中不是唯一的。 因此，要明确选择一个相关方，不能仅指定一个帐号。 您还必须指定已注册相关方的范围所属公司以填充所配置角色。 选择 **电子邮件收件人** 对话框中 **电子邮件源公司** 旁边的 **绑定** 按钮（链符号）打开[公式设计器](general-electronic-reporting-formula-designer.md)页面。 然后，您可以使用此页面来配置公式，该公式在运行时返回必须在其范围内找到所需来源的公司的代码。

> [!TIP]
> 如果您必须使用公司代码来运行 ER 格式，但 ER 格式不提供可从其获取公司代码的任何数据源，请配置使用内置的 [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md) ER 函数配置 `GetCurrentCompany()` 公式。

> [!NOTE]
> 公式特定于 ER 配置。

要指定运行时必须使用的电子邮件地址类型，请在 **电子邮件收件人** 对话框中，选择 **收件人** 字段旁边的 **编辑** 打开 **分配电子邮件地址** 下拉对话框。 然后设置以下字段：

- 在 **目的** 字段中，选择所需的目的。 仅使用来自所发现相关方联系人的选定目的的电子邮件地址。
- 将 **主要联络人** 选项设置为 **是** 以将为所发现相关方的电子邮件地址用作主要电子邮件地址。

> [!NOTE]
> 如果在 **目的** 字段中选择了目标，同时将 **主要联系人** 选项设置为了 **是**，则在运行时将使用至少满足一个所配置条件的每封电子邮件。

### <a name="configuration-email"></a>配置电子邮件

如果所用配置在数据源中有一个返回一个电子邮件地址或多个电子邮件地址（以分号 (;) 分隔）的节点，请选择 **配置电子邮件** 作为电子邮件地址类型。 可以在公式设计器中使用数据源和[函数](er-formula-language.md#Functions)获取格式正确的一个电子邮件地址或多个电子邮件地址（以分号分隔）。 例如，如果使用 **ISO 20022 贷方转帐** 配置，则应该将表示供应商联系人详细信息中的供应商主要电子邮件地址（包括字母）设置为 `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`。

[![配置电子邮件地址源。](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>为格式组件分组

要为格式组件分组，请在 **电子申报目标** 页面上的 **文件目标** 快速选项卡上，选择网格中的组件，然后选择 **分组**。

**电子邮件** 是之前配置且所选组件仍然可用的唯一目标。 之前配置的其他任何目标均不可用，因为这些目标被视为不支持一组组件。 将在合适时通知您这些更改。

您之前添加的记录被视为创建的组的标题。 该标题记录保存该组的电子邮件目标设置。 其他记录是将使用组标题记录的电子邮件目标设置的组成员。

要取消格式组件的分组，请在 **文件目标** 快速选项卡中选择一个属于该组的记录，然后选择 **取消分组**。

- 如果选择标题记录，则整个组将被取消分组。
- 如果您选择一个成员记录，并且它是组中的最后一个成员记录，则整个组将被取消分组。
- 如果选择的成员记录不是组中的最后一个成员记录，则该记录将从当前组中排除。

下图显示了 ER 格式的结构，该格式已配置为生成压缩的传出文件，该文件中包含催款单和 PDF 格式的相应客户发票。

[![生成传出文档的 ER 格式的结构。](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

下图显示了本文中所述的以下流程：将各个组件分组并为新组启用 **电子邮件** 目标，以便将催款单和相应的客户发票一起作为电子邮件附件发送。

[![为单个组件分组并启用电子邮件目标。](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>其他资源

- [电子报告 (ER) 概览](general-electronic-reporting.md)
- [电子报告 (ER) 目标](electronic-reporting-destinations.md)
- [电子申报中 (ER) 的公式设计器](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
