---
title: 在 B2B 电子商务网站上管理业务合作伙伴用户
description: 本主题介绍管理员如何在企业到企业 (B2B) 电子商务网站上添加、编辑和删除业务合作伙伴用户。
author: josaw1
ms.date: 07/22/2021
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
ms.openlocfilehash: f6cc1d5dfeb48fd00216fc1908e9e8be24f07131b3e5f1eaeefb10396efbebc3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734935"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>在 B2B 电子商务网站上管理业务合作伙伴用户

[!include [banner](../../includes/banner.md)]

本主题介绍管理员如何在企业到企业 (B2B) 电子商务网站上添加、编辑和删除业务合作伙伴用户。

B2B 电子商务网站需要组织进行注册才能成为业务合作伙伴。 组织将注册详细信息提交到 B2B 电子商务网站后，将通过资格认证流程。 如果组织成功取得资格，将作为业务合作伙伴加入。

组织作为业务合作伙伴加入后，发起请求成为业务合作伙伴的组织用户将被识别为管理员用户，并被授予将其他授权用户加入该 B2B 电子商务网站的特权。 这些授权用户然后可以代表业务合作伙伴下订单。

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>在 Commerce headquarters 中启用 B2B 电子商务功能

Commerce headquarters 中的 B2B 电子商务功能让组织可以加入业务合作伙伴和定义管理员用户。 此功能还让管理员能够创建和管理业务合作伙伴用户和团队，并为其分配特定角色。 最后，它让业务合作伙伴用户可以创建订单模板，然后使用现有订单重新订购产品。

要在 Commerce headquarters 中启用 B2B 电子商务功能，请按照以下步骤操作。

1. 转到 **工作区 \> 功能管理**。
1. 在 **所有** 选项卡上，使用术语 **零售和商业** 对 **模块** 字段进行筛选。
1. 查找并选择名为 **启用 B2B 电子商务功能** 的功能，然后选择 **立即启用**。

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>创建编号规则并将其添加到 Commerce 共享参数

编号规则用于为需要标识符的主数据记录和交易记录生成可读的唯一标识符。 有关编号规则的详细信息，请参阅[编号规则概览](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)。

若要创建编号规则并将其添加到 Commerce headquarters 中的 Commerce 共享参数，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 编号规则 \> 编号规则**，创建一个编号规则。
1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 共享参数**，将新编号规则添加到 **客户层次结构 ID** 引用中。

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>为新业务合作伙伴设置管理员用户

潜在的业务合作伙伴可以通过站点上的链接提交加入请求，来启动 B2B 电子商务网站的加入流程。 潜在的业务合作伙伴用户选择链接后，可以提供加入和注册所需的详细信息。 提交请求后，将显示一个提交确认页面。 如果提交被批准，请求者（即发起加入请求的用户）将成为业务合作伙伴管理员用户。

要在 Commerce headquarters 中审核和设置业务合作伙伴管理员用户，请按照下列步骤操作。

1. 转到 **Retail 和 Commerce IT \> 配送计划**。
1. 运行 **P-0001** 作业，将所有业务合作伙伴的加入请求拉入 Commerce headquarters。
1. **P-0001** 作业成功运行后，转到 **Retail 和 Commerce IT \> 客户**，运行 **从异步模式同步客户和业务合作伙伴** 作业。 此作业成功运行后，加入请求将作为 Commerce headquarters 中的目标客户记录创建。 这些记录的 **类型 ID** 字段将设置为 **B2B 目标客户**。
1. 转到 **客户 \> 所有目标客户**，打开目标客户页面。
1. 选择新业务合作伙伴的目标客户记录打开目标客户详细信息页面。
1. 在 **常规** 选项卡上，选择 **转换 \> 批准/拒绝** 批准或拒绝加入请求。 当出现确认消息时，请确认您要继续流程，然后批准请求。 然后，一封电子邮件将发送到请求者的电子邮件地址，确认其组织已被批准为业务合作伙伴。

    批准请求后，目标客户记录的 **状态** 字段将设置为 **已审批**。 此外，系统中还创建了两个新的客户记录：业务合作伙伴组织的 **组织类型** 客户记录和请求者的 **个人类型** 客户记录。 还将为业务合作伙伴创建客户层次结构记录。 <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. 转到 **Retail 和 Commerce IT \> 配送计划**，运行 **1010**（**客户**）作业将新创建的客户和客户层次结构记录推送到渠道数据库。

批准请求并将客户和客户层次结构记录同步到渠道数据库后，请求者可以使用他们在提交请求时提供的电子邮件地址登录 B2B 电子商务网站。 用户可以使用注册流来定义其帐户的密码。 要将标识提供者 (Azure AD B2C) 记录链接到在注册或登录时创建的 B2B 客户记录，请按照[启用标识记录到客户帐户的自动链接](../identity-record-linking.md)中的说明操作。

## <a name="onboard-additional-business-partner-users"></a>加入其他业务合作伙伴用户

业务合作伙伴管理员用户可以根据需要将其他业务合作伙伴用户加入 B2B 电子商务网站。

要将其他业务合作伙伴用户加入 B2B 电子商务网站，请按照以下步骤操作。

1. 以管理员身份登录 B2B 电子商务网站。
1. 转到 **我的帐户 \> 组织用户 \> 查看详细信息**，选择 **添加用户**。
1. 输入所需信息，然后选择 **保存**。 新用户的状态将设置为 **待处理**。

    **P-0001** 和 **从异步模式同步客户和业务合作伙伴** 作业运行后，将在 Commerce headquarters 中为新用户创建 **个人类型** 客户记录。 此客户记录还将与相关业务合作伙伴的客户层次结构记录关联。 此外，还会向新用户的电子邮件地址发送一封电子邮件，通知他们已将其添加为业务合作伙伴组织的用户，他们现在可以登录 B2B 电子商务网站。

1. 运行 **1010**（**客户**）作业将新的业务合作伙伴用户同步到渠道数据库。

同步客户记录后，B2B 电子商务网站上的用户状态将设置为 **活动**，新用户可以使用其电子邮件地址登录 B2B 电子商务网站。 用户可以使用注册流来定义其帐户的密码。 要将标识提供者 (Azure AD B2C) 记录链接到在注册或登录时创建的 B2B 客户记录，请按照[启用标识记录到客户帐户的自动链接](../identity-record-linking.md)中的说明操作。

## <a name="edit-business-partner-user-details"></a>编辑业务合作伙伴用户详细信息

要编辑业务合作伙伴用户的详细信息，请按照下列步骤操作。

1. 以管理员身份登录 B2B 电子商务网站。
1. 转到 **我的帐户 \> 组织用户 \> 查看详细信息**，选择 **编辑** 按钮（铅笔符号），进行所需的更改，然后选择 **保存**。 更改只有在 **P-0001**、**从异步模式同步客户和业务合作伙伴** 和 **1010**（**客户**）作业运行后才会生效。

## <a name="remove-a-business-partner-user"></a>删除业务合作伙伴用户

根据需要，管理员可以从可以访问 B2B 电子商务网站的用户列表中删除业务合作伙伴组织的现有用户。

要删除业务合作伙伴用户，请按照下列步骤操作。

1. 以管理员身份登录 B2B 电子商务网站。
1. 转到 **我的帐户 \> 组织用户 \> 查看详细信息**，选择 **删除** 按钮（“X”符号）。 当出现确认消息时，请确认您要删除该用户。 更改只有在 **P-0001**、**从异步模式同步客户和业务合作伙伴** 和 **1010**（**客户**）作业运行后才会生效。

> [!NOTE]
> 当您从可以访问 B2B 电子商务网站的用户列表中删除用户时，对应的客户记录将从业务伙伴的客户层次结构记录中删除。 但是，客户记录本身不会从 Commerce headquarters 中删除。

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>在 Commerce headquarters 中加入业务合作伙伴和用户

管理员可以直接在 Commerce headquarters 中加入业务合作伙伴和用户。

要在 Commerce headquarters 中加入业务合作伙伴和用户，请按照下列步骤操作。

1. 为业务合作伙伴组织创建 **组织类型** 客户记录。
1. 为业务合作伙伴用户创建 **个人类型** 客户记录。 确保为每个客户指定了主要电子邮件地址。
1. 对于必须指定为业务合作伙伴组织管理员用户的每个 **个人类型** 客户记录，在 **零售** 快速选项卡上，将 **B2B 管理员** 选项设置为 **是**。
1. 创建客户层次结构 ID。 在 **名称** 字段中输入名称。
1. 在 **组织** 字段中，输入业务合作伙伴组织客户。
1. 选择 **添加**，然后在 **名称** 字段中选择客户。
1. 重复此过程，将其他客户添加到层次结构中。

## <a name="additional-information"></a>附加信息

- 可以将本主题中提到的所有作业配置为以批格式按计划运行。 业务合作伙伴应该会根据需要配置批处理作业。
- 当前，只能将一个用户/客户记录指定为管理员用户，并且只能在 Commerce headquarters 中更改该角色。 没有让业务合作伙伴从 B2B 电子商务网站指定多个管理员或更改管理员的自助服务功能支持。
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- 虽然可以为用户定义支出限制，但是尚未实现在订单输入过程中强制执行支出限制。
- B2B 电子商务网站上用户体验的所有业务逻辑和验证均基于映射到 Commerce headquarters 中用户的客户记录的配置。

## <a name="additional-resources"></a>其他资源

[建立 B2B 电子商务站点](set-up-b2b-site.md)

[为 B2B 组织创建组织建模层次结构](org-model.md)

[配置 B2B 电子商务站点的客户帐户付款方式](payment-method.md)

[设置 B2B 电子商务站点的产品数量限制](quantity-limits.md)

[编号规则概览](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
