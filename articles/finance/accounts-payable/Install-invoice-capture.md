---
title: 安装 Invoice capture 解决方案
description: 本文提供有关如何安装 Invoice capture 解决方案并将其与 Microsoft Dynamics 365 Finance 集成的信息。
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
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691144"
---
# <a name="install-the-invoice-capture-solution"></a>安装 Invoice capture 解决方案

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> 如果您安装的是个人预览版的解决方案，必须先卸载旧解决方案，然后再继续安装。

## <a name="prerequisites"></a>先决条件

您必须先满足以下先决条件，然后才能够安装 Invoice capture 解决方案：

1. 注册应用程序，并在 Azure 订阅下向 Microsoft Azure Active Directory (Azure AD) 添加客户端密码。 有关详细信息，请参阅[通过 AAD 注册 Web 应用程序](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad)。

    > [!NOTE]
    > 记下 **应用程序（客户端）ID**、**客户端密码** 和 **租户 ID** 值，因为后面需要这些值。

2. 在 Dynamics 365 Finance 环境中注册 Azure 应用程序。 有关详细信息，请参阅[注册外部应用程序](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application)。

## <a name="install-and-set-up-the-solution"></a>安装和设置解决方案

要安装 Invoice capture 解决方案，转到 AppSource，选择 [Dynamics 365 Invoice capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture) 预览版本的链接。 安装完成后，您将在 Power Apps 中看到在选定环境中安装的解决方案。

要完成设置，请按照以下步骤操作。

1. 下载[助理解决方案](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip)来设置以下详细信息：

    - Microsoft Power Platform 与 Finance 环境之间的通信
    - 渠道将使用的 Dataverse 和 Office 365 Outlook 的连接引用

2. 在 Power Apps 中，转到您的环境，选择 **导入解决方案**。
3. 选择 **浏览**，选择您下载的助理解决方案包，然后选择 **下一步**。
4. 选择 **下一步**。
5. 分配现有连接，或选择 **新建连接** 创建新连接。
6. 包导入成功后，打开 **Dynamics 365 Invoice capture – 安装工具**。
7. 运行云端流来设置 Microsoft Power Platform 中的 Invoice capture 解决方案与 Finance 之间的连接。
8. 选择 **运行**，并指定以下参数：

    - **Dynamics 365 Finance Url** – 您要集成的 Finance 环境的 URL。
    - **租户 ID** – Finance 环境的租户 ID。
    - **客户端 ID** – 注册的 Azure 应用程序 ID。
    - **客户端密码** – 为 Azure 应用程序生成的客户端密码。
