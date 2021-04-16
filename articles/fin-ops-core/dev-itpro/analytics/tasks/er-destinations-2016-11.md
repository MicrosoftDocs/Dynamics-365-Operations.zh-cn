---
title: ER 配置目标
description: 此过程演示如何设置和使用不同的电子申报 (ER) 输出组件的目标，例如文件夹或文件。
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78dbcb73b47223ba1fe2ea35ef7c7af09a98d5c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754954"
---
# <a name="er-configure-destinations"></a>ER 配置目标

[!include [banner](../../includes/banner.md)]

此过程演示如何设置和使用不同的电子申报 (ER) 输出组件的目标，例如文件夹或文件。 用于创建此过程的演示数据公司是 DEMF。 德国为法人主要地址的国家/地区，但您可以为此过程使用任何法人。 

此示例使用的格式是 ISO20022 贷方转帐，不过，您可以使用您已经导入的任何格式。 请注意，此过程是单个文件和单个目标设置的示例。 有关电子申报目标管理的详细信息可以在 Dynamics 365 Finance 帮助中找到。

1. 转到“组织管理”>“电子申报”>“电子申报目标”。
2. 单击“新建”为格式创建一组新目标。
3. 在“引用”字段中，选择要为其配置目标的格式。
    * 如果您没有要选择的值，则表明您尚未导入任何电子申报格式配置。 您必须在设置目标前导入格式配置。  
4. 单击“新建”创建新文件目标。
    * 请注意，您可以为相同格式的每个输出组件创建一个文件目标，如文件夹或文件。 您可以在设置中单独启用和禁用目标。  
5. 在“名称”字段中，输入用户易识别的输出组件的名称。
    * 我们建议您使用有意义的名称，如“付款文件“或“控制报表”。 这些名称将在配置运行时间与目标设置一同呈现给用户。  
6. 在“文件名”中，选择特定于格式的文件或文件夹。
7. 单击“设置”。
8. 在“已启用”字段中选择“是”。
    * 每个选项卡的“已启用”复选框可以单独启用和禁用每个目标。 在此示例中，在生成文件时，您将启用将输出文件发送到邮件收件人。  
9. 单击"编辑"设置电子邮件收件人。
10. 单击“添加”。
11. 单击“打印管理电子邮件”。
12. 在“电子邮件源”字段中，选择一个选项。
    * 您可以选择不同的电子邮件源类型，如客户或供应商类型。 这定义将由电子邮件源帐户公式返回的参数的类型。 电子邮件源帐户公式（在下列步骤中描述）是您要绑定电子邮件源的位置。 如果您的公式将返回供应商帐户，则选择“供应商”。 如果您使用 ISO 20022 贷方转帐配置示例，同使用“供应商”。  
13. 单击“电子邮件源绑定”按钮。
14. 在“公式”中，输入您在前面选择的当事方类型的票据特定引用。
    * 不是键入，您可以查找表示当事方帐户的数据源节点，然后单击“添加数据源”按钮来更新公式。 例如，如果您使用 ISO 20022 贷方转帐配置，表示供应商帐户的节点是 '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID。 否则，输入任何字符串值，例如 "DE-001" 来保存公式。  
15. 单击“保存”。
16. 关闭该页面。
17. 单击“编辑”为当事方配置联系人详细信息。
18. 在“主要联系人”字段中选择“是”。
    * 可以使用不同选项指示应将当事方的哪种联系人类型用作此目标的电子邮件地址。 此示例中，我们使用主要联系人。  
19. 单击“确定”。
20. 单击“确定”。
21. 在“主题”字段中，键入一个值。
22. 单击“确定”。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]