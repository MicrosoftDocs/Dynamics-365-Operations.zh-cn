---
title: 电子邮件 ER 目标类型
description: 本主题提供相关信息，介绍如何为配置为生成出站文档的电子报告 (ER) 格式的每个文件夹或文件组件配置电子邮件目标。
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745553"
---
# <a name="email-destination"></a>电子邮件目标

[!include [banner](../includes/banner.md)]

您可以为配置为生成出站文档的电子报告 (ER) 格式的每个文件夹或文件组件配置电子邮件目标。 根据目标设置，将生成的文档作为电子邮件的附件进行传递。

设置**已启用**为**是**以通过电子邮件发送输出文件。 启用此选项后，您可以指定电子邮件收件人，以及编辑电子邮件的主题和正文。 可以为电子邮件主题和正文设置固定文本，或者使用 ER [公式](er-formula-language.md)动态创建电子邮件文本。 

可以通过两种方法为 ER 配置电子邮件地址。 可以用打印管理功能完成配置所用的相同方式来完成此配置，或者可以通过公式使用 ER 配置的直接引用来解析电子邮件地址。

[![启用电子邮件目标](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>电子邮件地址类型

选择**收件人**或**抄送**字段中的**编辑**时，将显示**电子邮件收件人**对话框。 然后可以选择要使用的电子邮件地址类型。 当前支持**配置电子邮件**和**打印管理**电子邮件类型。

[![选择电子邮件类型](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>打印管理

如果选择**打印管理**电子邮件类型，则可以在**收件人**字段中输入固定电子邮件地址。 

[![配置固定的电子邮件地址](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

若要使用非固定电子邮件地址，您必须选择文件目标的电子邮件源类型。 支持下列值：**客户**、**供应商**、**目标客户**、**联系人**、**竞争对手**、**工作人员**、**申请人**、**潜在供应商**和**非许可供应商**。 选择电子邮件源类型后，请使用**电子邮件源帐户**字段旁边的按钮打开**公式设计器**窗体。 您可以使用此窗体附加一个公式，以在运行时将已处理文档中选定源类型的**当事方帐户**返回到电子邮件目标。

[![配置电子邮件源帐户](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

公式特定于 ER 配置。 在**公式**中，输入客户或供应商当事方类型的文档特定引用。 您可以查找表示客户或供应商帐户的数据源节点（而不是键入），然后选择**添加数据源**来更新公式。 例如，如果您使用 **ISO 20022 贷方转帐**配置，则表示供应商帐户的节点是 `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`。

如果输入字符串值，例如 `"DE-001"`，并保存公式，系统会将电子邮件发送给供应商的联系人，**DE-001**。


[![ER 公式设计器页](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![配置电子邮件源属性帐户](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>配置电子邮件

如果所用配置在数据源中有一个返回**电子邮件地址**的节点，请使用此电子邮件类型。 可使用公式设计器中的数据源和功能获取格式正确的电子邮件地址。 例如，如果您使用 **ISO 20022 贷方转帐**配置，则表示供应商联系人电子邮件地址的节点是 `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`。

[![配置电子邮件地址源](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>其他资源

- [电子报告 (ER) 概览](general-electronic-reporting.md)
- [电子报告 (ER) 目标](electronic-reporting-destinations.md)
- [电子申报中 (ER) 的配方设计器](general-electronic-reporting-formula-designer.md)
