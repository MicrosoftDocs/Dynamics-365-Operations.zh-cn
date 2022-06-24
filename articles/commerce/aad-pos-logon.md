---
title: 为 POS 登录配置 Azure Active Directory 身份验证
description: 本文说明如何将 Azure Active Directory 配置为 Microsoft Dynamics 365 Commerce 销售点中的身份验证方法。
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 47da2c78cef2bbee324fbc2202898fbabd927c4d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853920"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>为 POS 登录配置 Azure Active Directory 身份验证

[!include [banner](includes/banner.md)]

本文说明如何将 Azure Active Directory (Azure AD) 配置为 Microsoft Dynamics 365 Commerce 销售点 (POS) 中的身份验证方法。

将 Dynamics 365 Commerce 与其他 Microsoft 云服务（如 Microsoft Azure、Microsoft 365 和 Microsoft Teams）一起使用的零售商通常希望使用 Azure AD 集中管理用户凭据，以跨各个应用程序实现安全、无缝的登录体验。 若要将 Azure AD 身份验证用于 Commerce POS，必须首先将 Azure AD 配置为 Commerce Headquarters 中的身份验证方法。

## <a name="configure-pos-authentication-method"></a>配置 POS 身份验证方法

要在 Commerce headquarters 中配置 POS 身份验证方法，请按照下列步骤操作。
    
1. 转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**，选择要更改的功能配置文件。
1. 在 **功能** 快速选项卡的 **POS 人员登录** 部分，从 **登录身份验证方法** 下拉列表中选择所需的身份验证方法选项。

    **登录身份验证方法** 有三个选项：
    
    - **个人 ID 和密码** - 此默认选项需要 POS 用户输入个人 ID 和密码来登录 POS 和访问经理替代功能。
    - **未采用单一登录的 Azure AD** - 此选项需要 POS 用户使用 Azure AD 凭据登录 POS 和访问经理替代功能。 刷新或重新打开 POS 客户端时，POS 用户必须提供 Azure AD 凭据才能再次登录。
    - **采用单一登录的 Azure AD** - 选择此选项后，POS 用户可以使用同一 Web 浏览器中其他 Web 应用程序正在使用的活动 Azure AD 凭据登录 Cloud POS (CPOS)，或使用登录到 Windows 的 Azure AD 凭据登录 Modern POS。 使用这两种方法登录时都不需要在 POS 登录屏幕上输入 Azure AD 凭据。 但是，访问 POS 经理替代功能仍然需要使用 Azure AD 凭据登录。

1. 转到 **Retail 和 Commerce > Retail 和 Commerce IT > 分配计划**，运行 **1070 (渠道配置)** 作业，将最新功能配置文件设置同步到 POS 客户端。

> [!NOTE]
> - **未采用单一登录的 Azure AD** 身份验证方法选项替换了 Commerce 版本 10.0.18 及更早版本中的 **Azure Active Directory** 选项。
> - Azure AD 身份验证需要有效的 Internet 连接，在 POS 处于离线状态时无法运行。

## <a name="associate-azure-ad-accounts-with-pos-users"></a>将 Azure AD 帐户与 POS 用户关联

要将 Azure AD 用作 POS 身份验证方法，必须将 Azure AD 帐户与 Commerce headquarters 中的 POS 用户关联。 

要将 Azure AD 帐户与 Commerce headquarters 中的 POS 用户相关联，请按照下列步骤操作。
    
1. 转到 **Retail 和 Commerce > 员工 > 工作人员**，打开一个工作人员记录。
1. 在操作窗格上，选择 **Commerce** 选项卡，然后在 **外部标识** 下选择 **关联现有标识**。 
1. 在 **使用现有外部标识** 对话框中，选择 **使用电子邮件搜索**，输入 Azure AD 电子邮件地址，然后选择 **搜索**。
1. 选择返回的 Azure AD 帐户，然后选择 **确定**。

完成上述配置步骤后，将填写该工作人员详细信息页的 **Commerce** 选项卡中的 **别名**、**UPN** 和 **外部子标识** 字段。

您必须运行 **Retail 和 Commerce > Retail 和 Commerce IT > 分配计划** 中的 **1060 (人员)** 作业，来将最新的 POS 用户和 Azure AD 帐户数据同步到渠道。

> [!NOTE]
> 最佳做法是，在 Commerce headquarters 中更新工作人员信息（如密码、POS 权限、关联的 Azure AD 帐户或员工通讯簿）后，强烈建议运行 **1060 (人员)** 作业将最新的工作人员信息同步到渠道。 然后，POS 客户端可以提取正确的数据来进行用户身份验证和授权检查。

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>使用 Azure AD 身份验证的 POS 锁定收银机和注销

将 POS 配置为使用 Azure AD 身份验证方法时，会发生以下情况：

- **锁定收银机** 功能在 POS 应用程序中不可用。 
- **自动锁定** 功能与 **自动注销** 功能的行为相同。
- 如果 POS 用户选择 **注销**，下次 POS 启动时将要求该用户使用 Azure AD 凭据登录，无论是否启用了单一登录。

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>使用 Azure AD 身份验证的经理替代功能

当 POS 配置为使用 Azure AD 身份验证时，经理替代功能将打开一个对话框，提示输入经理用户的 Azure AD 凭据。 经理登录被批准后，将丢弃经理的 Azure AD 凭据，先前用户的 Azure AD 凭据将用于后续的 POS 操作。

> [!NOTE]
> - 在 Commerce 版本 10.0.18 和更早版本中，经理替代功能不支持 Azure AD。 即使将 POS 配置为使用 Azure AD 身份验证方法，也需要个人 ID 和密码。
> - 在 Apple iOS 设备上通过 Safari Web 浏览器使用 CPOS 时，必须首先在 Safari 设置中关闭 **阻止弹出窗口**，这样经理替代功能才能使用 Azure AD 身份验证。 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>在共享设备上使用基于 Azure AD 的 POS 身份验证的最佳安全实践

很多零售商设置零售商店环境时采取的方式是多个用户需要从共享物理设备访问 POS 应用程序。 在这种情况下，虽然单一登录提供了方便、无缝的身份验证体验，但它也可能会造成安全漏洞：当前 POS 用户可能不会意识到另一个用户的凭据正被用于在 POS 中执行交易或操作。 在将 POS 配置为使用 Azure AD 身份验证方法之前，强烈建议查看您的安全策略和共享设备的登录设置，以确定最适合的选项。

- 如果您的零售环境使用共享帐户（例如，本地帐户）进行物理设备登录，则建议使用 **未采用单一登录的 Azure AD** 选项。 这样可以确保每个 POS 用户明确提供 Azure AD 凭据来登录 POS。
- 如果您的零售环境需要员工使用自己的 Azure AD 帐户登录 POS 及其托管物理设备，则建议使用 **采用单一登录的 Azure AD** 选项。

## <a name="additional-resources"></a>其他资源

[配置工作人员](tasks/worker.md)

[创建零售功能配置文件](retail-functionality-profile.md)


[为 MPOS 和 Cloud POS 设置扩展登录功能](extended-logon.md)

[共享环境中 Cloud POS 的最佳安全实践](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
