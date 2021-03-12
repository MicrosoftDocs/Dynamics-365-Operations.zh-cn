---
title: 对 POS 登录启用 Azure Active Directory 身份验证
description: 此主题介绍如何为 Microsoft Dynamics 365 Commerce 销售点 (POS) 配置登录体验，以便使用 Azure Active Directory 身份验证。
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982732"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>对 POS 登录启用 Azure Active Directory 身份验证
[!include [banner](includes/banner.md)]


许多使用 Microsoft Dynamics 365 Commerce 的客户也使用其他 Microsoft 云服务，并且可能使用 Azure Active Directory (Azure AD) 来管理这些服务的用户凭据。 在这些情况下，客户可能希望在多个应用程序中使用同一个 Azure AD 帐户。 此主题介绍如何配置 Commerce 销售点 (POS) 登录体验，以便使用 Azure AD 身份验证。

## <a name="configure-azure-ad-authentication"></a>配置 Azure AD 身份验证

若要将 Azure AD 设置为商店的 POS 登录身份验证方法，必须配置商店的功能配置文件设置，然后将这些设置应用于 POS 客户端。

若要配置功能配置文件，请执行以下步骤。

1. 转至 **Retail 和 Commerce** \> **渠道设置** \> **POS 设置** \> **POS 配置文件** \> **功能配置文件**。
1. 选择要更改的功能配置文件。
1. 在 **功能** 快速选项卡上的 **POS 职员登录** 部分中，将 **登录身份验证方法** 字段的值从 **个人 ID 和密码** 更改为 **Azure Active Directory**。

默认情况下，所有功能配置文件都使用 **个人 ID 和密码** 作为 POS 身份验证方法。 因此，如果要使用 Azure AD，必须更改 **登录身份验证方法** 字段的值。 此更改将影响链接到所选功能配置文件的每家零售商店。

若要将这些设置应用于 POS 客户端，请执行以下步骤。

1. 转到 **Retail 和 Commerce** \> **Retail 和 Commerce IT** \> **配送计划**。
1. 运行 **1070**（**渠道配置**）配送计划。

> [!NOTE]
> Azure AD 身份验证需要 Internet 连接。 如果 POS 处于脱机模式，将不能工作。
> 
> 目前，**经理覆盖** 功能不支持将 Azure AD 作为身份验证方法。 即使将 Azure AD 配置为 POS 登录的身份验证方法，也需要操作员 ID 和密码。

## <a name="associate-an-azure-ad-account-with-a-worker"></a>将 Azure AD 帐户与工作人员关联

必须先将 Azure AD 帐户与商店工作人员关联，该工作人员才能使用 Azure AD 帐户登录 POS 应用程序。

若要将 Azure AD 帐户与工作人员关联，请执行以下步骤。

1. 转到 **Retail 和 Commerce** \> **员工** \> **工作人员**。
1. 打开工作人员的详细信息页面。
1. 在操作窗格中 **Commerce** 选项卡上的 **外部标识** 组中，选择 **关联现有标识**。
1. 在 **使用现有外部标识** 对话框中，选择 **使用电子邮件搜索**，输入 Azure AD 电子邮件地址，然后选择 **搜索**。
1. 选择返回的 Azure AD 帐户，然后选择 **确定**。

将填写该工作人员详细信息页的 **Commerce** 选项卡中的 **别名**、**UPN** 和 **外部子标识** 字段。

> [!NOTE]
> 更新工作记录后，例如，如果关联了新的 Azure AD 帐户，更改了密码或更新了员工通讯簿，建议您运行 **1060**（**人员**）分配计划将最新的人员信息同步到渠道。 这样，POS 应用程序可以获取正确的数据以进行用户身份验证和授权检查。

## <a name="additional-resources"></a>其他资源

[为 MPOS 和 Cloud POS 设置扩展登录功能](extended-logon.md)

[创建零售功能配置文件](retail-functionality-profile.md)

[配置工作人员](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
