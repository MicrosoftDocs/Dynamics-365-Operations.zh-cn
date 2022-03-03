---
title: 在 B2B 电子商务网站上管理业务合作伙伴用户
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 企业到企业 (B2B) 电子商务网站和 Commerce headquarters 中添加、删除和编辑业务伙伴用户。
author: josaw1
ms.date: 02/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: def8d4de082ceb4be77ed7e8898cbef82d52b749
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323447"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>在 B2B 电子商务网站上管理业务合作伙伴用户

[!include [banner](../../includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 企业到企业 (B2B) 电子商务网站和 Commerce headquarters 中添加、删除和编辑业务伙伴用户。

> [!NOTE]
> 完成[使用客户层次结构管理 B2B 业务合作伙伴](partners-customer-hierarchies.md)主题是阅读本文档的前提条件。 

B2B 电子商务网站需要组织进行注册才能成为业务合作伙伴。 组织将注册详细信息提交到 B2B 电子商务网站后，注册请求将通过资格认证流程。 如果组织成功取得资格，将作为业务合作伙伴加入。

组织作为业务合作伙伴加入后，发起请求成为业务合作伙伴的组织用户将被识别为管理员用户，并被授予将其他授权用户加入该 B2B 电子商务网站的特权。 这些授权用户然后可以代表业务合作伙伴下订单。

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>为新业务合作伙伴设置管理员用户

潜在的业务合作伙伴可以通过 B2B 网站上的链接提交加入请求，来启动 B2B 电子商务网站的加入流程。 然后，他们可以使用可自定义窗体来提供加入和注册所需的详细信息。 提交请求后，将显示一个提交确认页面。 如果提交获得批准，提交请求的公司将成为业务伙伴，请求者（发起加入请求的用户）将成为业务伙伴的管理员用户。

要在 Commerce headquarters 中批准业务合作伙伴请求，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce IT \> 配送计划**。
1. 运行 **P-0001** 作业，将所有业务合作伙伴的加入请求拉入 Commerce headquarters。
1. **P-0001** 作业成功运行后，转到 **Retail 和 Commerce IT \> 客户**，运行 **同步客户和渠道请求** 作业。 此作业成功运行后，加入请求将在 Commerce headquarters 中作为 **B2B 目标客户** 类型的目标客户创建。 
1. 转到 **客户 \> 所有目标客户**，然后选择新业务合作伙伴的目标客户记录打开目标客户详细信息页面。
1. 在 **常规** 选项卡上，选择 **转换 \> 批准/拒绝** 批准加入请求。 当出现确认消息时，请确认您要继续流程，然后批准请求。 批准后，目标客户记录的 **状态** 字段将更改为 **已审批**。 然后，一封电子邮件将发送到请求者的电子邮件地址，确认其组织已被批准为业务合作伙伴。 还将创建客户层次结构，其中将请求者添加为业务合作伙伴的管理员。

    > [!NOTE]
    > 目前，确认电子邮件会在批准后立即发送。 但是，未来的 Commerce 功能将允许管理员手动触发电子邮件。

1. 转到 **Retail 和 Commerce IT \> 配送计划**，运行 **1010（客户）** 作业将新客户和客户层次结构记录推送到渠道数据库。

> [!NOTE]
> 为确保将新客户记录发送到渠道数据库，与该客户关联的通讯簿中至少有一个应包含在与在线商店关联的客户通讯簿中。 您可以通过在在线商店的默认客户上配置通讯簿来自动执行此流程，以便系统将通讯簿值复制给每个新客户。

客户层次结构记录同步到渠道数据库后，请求者可以使用他们在提交加入请求时提供的电子邮件地址登录 B2B 电子商务网站。 用户可以使用注册流来定义其帐户的密码。 有关如何将 Azure Active Directory (Azure AD) B2C 标识提供者记录链接到在潜在目标批准时创建的 B2B 客户记录的信息，请参阅[启用自动链接](../identity-record-linking.md)。

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>在批准或拒绝 B2B 目标客户时通知他们

当您批准或拒绝 B2B 目标客户加入请求时，可以自动向目标客户发送电子邮件通知。

要在 Commerce Headquarters 中为 **B2B 目标客户已批准** 或 **B2B 目标客户已拒绝** 通知类型的事件设置电子邮件通知，请按照这些步骤操作。

1. 为在触发 **B2B 目标客户已批准** 或 **B2B 目标客户已拒绝** 通知类型时发送给目标客户的电子邮件创建电子邮件模板。 有关这些通知类型支持的占位符的信息，请参阅[通知类型](../email-templates-transactions.md#notification-types)。 有关如何创建电子邮件模板的信息，请参阅[创建电子邮件模板](../email-templates-transactions.md#create-an-email-template)。
1. 将 **B2B 目标客户已批准** 和 **B2B 目标客户已拒绝** 通知类型添加到电子邮件通知配置文件中，然后将它们映射到您创建的电子邮件模板。 有关通知配置文件的详细信息，请参阅[设置电子邮件通知配置文件](../email-notification-profiles.md)。

## <a name="onboard-additional-business-partner-users"></a>加入其他业务合作伙伴用户

业务合作伙伴管理员用户可以根据需要将其他业务合作伙伴用户加入 B2B 电子商务网站。

要将其他业务合作伙伴用户加入 B2B 电子商务网站，请按照以下步骤操作。

1. 以管理员身份登录 B2B 电子商务网站。
1. 转到 **我的帐户 \> 组织用户 \> 查看详细信息**，选择 **添加用户**。
1. 输入所需信息，然后选择 **保存**。 新用户的状态将设置为 **待处理**。

运行 **P-0001** 和 **同步客户和渠道请求** 作业后，将在 Commerce headquarters 中为新用户创建 **个人** 类型的客户记录。 此客户记录还将与相关业务合作伙伴的客户层次结构记录关联。 此外，还会向新用户的电子邮件地址发送一封电子邮件，通知他们已将其添加为业务合作伙伴组织的用户，他们现在可以登录 B2B 电子商务网站。

接下来，运行 **1010（客户）** 作业将新的业务合作伙伴用户同步到渠道数据库。

同步客户记录后，B2B 电子商务网站上的用户状态将设置为 **活动**，新用户可以使用其电子邮件地址登录 B2B 电子商务网站。 用户可以使用注册流来定义其帐户的密码。 有关如何将 Azure AD B2C 标识提供者记录链接到在 Commerce headquarters 中创建的 B2B 客户记录的信息，请参阅[启用自动链接](/dynamics365/commerce/identity-record-linking.md)。

## <a name="edit-business-partner-user-details"></a>编辑业务合作伙伴用户详细信息

要编辑业务合作伙伴用户的详细信息，请按照下列步骤操作。

1. 以管理员身份登录 B2B 电子商务网站。
1. 转到 **我的帐户 \> 组织用户 \> 查看详细信息**，选择 **编辑** 按钮（铅笔符号），进行所需的更改，然后选择 **保存**。 更改只有在 **P-0001**、**同步客户和渠道请求** 和 **1010（客户）** 作业运行后才会生效。

## <a name="remove-a-business-partner-user"></a>删除业务合作伙伴用户

根据需要，管理员可以从可以访问 B2B 电子商务网站的用户列表中删除业务合作伙伴组织的现有用户。
要删除业务合作伙伴用户，请按照下列步骤操作。
- 以管理员身份登录 B2B 电子商务网站。
- 转到 **我的帐户 > 组织用户 \> 查看详细信息**，选择 **删除** 按钮（“X”符号）。 当出现确认消息时，请确认您要删除该用户。 更改只有在 **P-0001**、**同步客户和渠道请求** 和 **1010（客户）** 作业运行后才会生效。

> [!NOTE]
> 当您从可以访问 B2B 电子商务网站的用户列表中删除用户时，对应的客户记录将从业务伙伴的客户层次结构记录中删除。 但是，客户记录本身不会从 Commerce headquarters 中删除。

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>在 B2B 电子商务网站上将现有客户作为业务合作伙伴加入

管理员可以直接在 Commerce headquarters 中加入业务合作伙伴和用户。 此功能对于在 B2B 电子商务网站上加入现有业务合作伙伴很有用。

要在 Commerce headquarters 中加入业务合作伙伴和用户，请按照下列步骤操作。

1. 创建或选择 **组织** 类型的客户添加为业务合作伙伴。
1. 创建或选择 **个人** 类型的客户添加为业务合作伙伴的管理员或用户。 确保主要电子邮件地址与客户相关联。 这些电子邮件地址用于登录网站。 

    > [!NOTE]
    > 系统必须能够为应该能够登录网站的用户找到唯一的客户记录。 如果系统在法人中发现多个客户具有相同的主要电子邮件地址，用户将无法登录网站。

1. 创建客户层次结构 ID。
1. 在 **名称** 字段中输入名称。
1. 在 **组织** 字段中，输入业务合作伙伴组织客户。
1. 在 **层次结构** 快速选项卡上，选择 **添加**。
1. 在 **姓名** 字段中，选择 **个人** 类型的客户。
1. 为应指定为管理员的客户选择 **管理员** 角色。
1. 重复此过程，将更多客户添加到层次结构中。

## <a name="additional-information"></a>其他信息

- 可以将本主题中提到的所有作业配置为以批格式按计划运行。 业务合作伙伴应该会根据需要配置批处理作业。
- 当前，只能将一个用户/客户记录指定为管理员用户，并且只能在 Commerce headquarters 中更改该角色。 没有让业务合作伙伴从 B2B 电子商务网站指定多个管理员或更改管理员的自助服务功能支持。
- 虽然可以为用户定义支出限制，但是尚未实现在订单输入过程中强制执行支出限制。
- B2B 电子商务网站上用户体验的所有业务逻辑和验证均基于映射到 Commerce headquarters 中用户的客户记录的配置。

## <a name="additional-resources"></a>其他资源

[建立 B2B 电子商务站点](set-up-b2b-site.md)

[使用客户层次结构管理 B2B 业务合作伙伴](partners-customer-hierarchies.md)

[配置 B2B 电子商务站点的客户帐户付款方式](payment-method.md)

[设置 B2B 电子商务站点的产品数量限制](quantity-limits.md)

[编号规则概览](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
