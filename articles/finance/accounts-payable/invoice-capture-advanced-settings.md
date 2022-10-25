---
title: Invoice capture 解决方案高级设置
description: 本文提供有关 Invoice capture 解决方案中的高级设置的信息。
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691137"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Invoice capture 解决方案高级设置

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文提供有关 Invoice capture 解决方案中的高级设置的信息。

## <a name="create-additional-connections-for-channels"></a>为渠道创建更多连接

您必须创建与电子邮件或文件存储的连接，来实现对来自不同渠道的传入发票的监视。 您必须在开始时注册连接来授予解决方案中使用的自动化流的访问权限。

以下连接类型用于导入发票：

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

发票导入渠道将在后续的配置步骤中使用连接。 必须先向用户授予 **管理员** 安全角色，并且用户必须创建连接，然后才能够创建特定连接的渠道。

要创建到 Microsoft Dataverse 的连接，请执行以下步骤。

1. 转到 **管理系统 \> 默认解决方案**。
2. 选择 **新建**，然后选择 **连接引用**。
3. 在 **显示名称** 字段中，输入一个名称。
4. 选择 **Microsoft Dataverse** 作为连接器。
5. 如果您是第一次设置连接，选择 **新建连接**。
6. 在出现的对话框中，创建一个 Dataverse 连接，然后选择 **创建**。
7. 输入 Dataverse 帐户和密码。
8. 验证通过后，转到连接页面，选择 **刷新**，选择帐户，然后选择 **创建**。

要创建电子邮件或文件存储连接，请按照下列步骤操作。

1. 在 **连接创建** 页面，在 **连接类型** 字段中，选择 **Office 365 Outlook**。
2. 对于电子邮件连接，您可以选择 **Outlook.com** 或 **Office 365 Outlook** 作为连接器。 对于文件存储连接，您可以选择 **OneDrive** 或 **SharePoint**。

要查看现有连接，转到 **默认解决方案 \> 对象 \> 连接引用**。 除了特定电子邮件或文件存储连接之外，创建渠道的用户应至少有一个 Dataverse 连接。 新渠道的创建者应该是连接的负责人。
