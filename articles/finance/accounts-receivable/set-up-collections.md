---
title: 设置收款
description: 本文介绍如何设置收款功能。
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ce37a85477d65b9592a32dcbe430d09f9dde62b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189461"
---
# <a name="set-up-collections"></a>设置收款

[!include [banner](../includes/banner.md)]

本文介绍如何设置收款功能。 使用收款功能时，您必须完成一些设置步骤。 还有一些可选功能，包括客户池和收款团队。 

- 帐龄期间定义
- 帐龄快照
- 日记帐名称
- 勾销交易记录的原因代码
- 收款代理
- 勾销帐户
- NSF（资金不足）信息
- 使用 **收款** 页的用户的 Outlook 设置
- 电子邮件地址

在本主题的其余部分中，将对这些要点进行更详细的讨论。 

## <a name="set-up-aging-period-definitions"></a>设置帐龄期间定义

设置帐龄期间定义。 帐龄期间定义用于定义在 **帐龄余额**、**收款活动** 和 **收款案例** 列表页上显示的列。 它还定义在 **收款** 页上显示的期间。 如果设置客户池，使用池的帐龄期间定义。 如果未设置池，则使用在 **应收帐款参数** 页中指定的默认帐龄期间定义。 如果默认帐龄期间定义未指定，则在 **帐龄期间定义** 页中使用第一个帐龄期间定义。

## <a name="create-an-aging-snapshot"></a>创建一个帐龄快照
为所有客户或在客户池的客户创建帐龄快照记录。 帐龄快照信息将显示在 **帐龄余额** 列表页和 **收款** 页上。 您必须创建一个帐龄快照，然后才能使用列表页。 列表页只为已经创建帐龄快照的客户显示信息。

## <a name="optional-set-up-customer-pools"></a>可选：设置客户池
您可以设置客户池表示客户组。 您可以使用客户池用作筛选器用于显示在 **收款** 列表页上、**收款** 页上的客户信息，或者，当您创建帐龄快照时。

## <a name="optional-create-a-collections-team"></a>可选：创建集合团队
如果您的组织的多个人员执行收款工作，您可以设置收款团队。 您可以在 **应收帐款参数** 页上选择团队。 如果没有创建收款团队，则当您在 **收款代理** 页上设置收款代理时将自动创建一个团队。

## <a name="set-up-a-collections-case-category"></a>设置集合案例类别
要使用案例组织您的收款工作，请设置具有 **收款** 类别类型的案例类别。 只有当您要在 **收款** 页上使用案例功能时，这才是必需的。

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>设置日志名称（结算、冲销和资金不足）
设置当您在 **收款** 页上处理交易记录时使用的日记帐名称。 此处理包括设置交易记录，冲销交易记录和处理资金不足 (NSF) 付款。

| 说明 | 日记帐类型     |
|-------------|------------------|
| 结算  | 客户 - 付款 |
| 销帐   | 日常            |
| 资金不足         | 客户 - 付款 |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>设置冲销交易记录的原因代码
在 **收款** 页上设置在勾销交易记录时使用的默认值原因代码。 您可以在勾销流程中更改该代码。

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>设置电子邮件附件的文件夹和创建电子邮件模板
如果您从 **收款** 页发送具有 Microsoft Excel 附件的电子邮件，您可以为这些消息创建可选电子邮件模板。

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>设置集合的应收帐款参数。
设置在 **收款** 选项卡上显示的应收帐款参数。

## <a name="optional-set-up-collections-agents"></a>可选：设置收款代理
如果您的组织的多个人员执行收款工作，您可以设置收款代理。 收款代理是设置为 **用户关系** 页上的用户的工作人员。 您可以分配客户池（客户查询）到代收人员以帮助代理组织它们的工作。 收款代理添加到 **应收帐款参数** 页上选择的团队。 如果在此窗体中未选择团队，则会自动创建名为 **收款** 的新团队，并且收款代理添加到该团队。

## <a name="set-up-a-writeoff-account"></a>设置冲销帐户
交易记录已注销时，设置用于总帐冲销条目的销帐帐户。 此帐户存储在客户过帐模板中。

## <a name="set-up-nsf-information-for-bank-accounts"></a>为银行帐户设置资金不足信息
更新银行帐户，以便当在 **收款** 页上标识 NSF 支付时，这些帐户具有正确的日记帐。 在 **币种管理** 选项卡上，在 **NSF 支付日记帐** 字段中，选择一个支付日记帐。

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>为“收款”页的用户设置 Outlook 设置
在工作人员可以通过使用 **收款** 页创建活动或发送电子邮件消息前，您必须验证选择了 **Microsoft Outlook 同步** 配置键，并且为这些工作人员设置了 Outlook 同步。

## <a name="set-up-email-and-addresses"></a>设置电子邮件和地址
您可以使用电子邮件与客户和销售人员就收款问题进行沟通，以从 **收款** 页发送电子邮件。 

### <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>设置收款客户联系人的电子邮件和地址设置
设置客户联系人的电子邮件地址，以将电子邮件发送给来自 **收款** 页的那些联系人。 收款联系人用作 **收款** 页上的默认联系人。 如果报表应该使用主要地址以外的地址，您可以设置客户的报表地址。 

在客户的 **信用和收款** 快速选项卡上，在 **收款联系人** 字段中，选择客户组织中与您的收款代理合作的人员。 此人用作 **收款** 页上的默认联系人，并且是电子邮件发送到的人员。 

> [!NOTE] 
> 如果没有为客户指定收款联系人，使用客户的主要联系人。 如果未指定主要联系人，电子邮件将发送到 **联系人** 页上中列出的第一个地址。

### <a name="set-up-email-settings-for-salespeople"></a>设置销售人员的电子邮件设置
为销售人员设置电子邮件地址，以将电子邮件发送给来自 **收款** 页的销售人员。 为每个佣金销售组中的每个销售代表设置电子邮件地址。 其 **联系人** 选项被选中的销售代表是电子邮件发送到的默认销售人员。 

如果未指定销售代表，使用客户组织的主要销售人员。 如果未指定主要销售人员，电子邮件将发送到此页上列出的第一个销售人员。


有关详细信息，请参阅以下主题：

 - [创建催款单序列](tasks/create-collection-letter-sequence.md)

 - [处理催款单](tasks/process-collection-letters.md)

 - [审核收款信息](tasks/review-collections-information.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]