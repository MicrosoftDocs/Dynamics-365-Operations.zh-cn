---
title: ATS 集成 API 的服务器到服务器身份验证
description: 本主题介绍如何针对 Dynamics 365 Human Resources 申请人跟踪系统 (ATS) 集成 API 为集成设置服务器到服务器身份验证。
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aabe2cd9fd962c8f1c5bbf7fe911e7c6ceeae082f61fc4359aaf7bf197531eff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778071"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>ATS 集成 API 的服务器到服务器身份验证

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍如何针对 Dynamics 365 Human Resources 申请人跟踪系统 (ATS) 集成 API 为应用程序集成设置服务器到服务器身份验证。 有几个需要管理的安全层，服务主体需要它们才能访问 Microsoft Dataverse 虚拟表和关联数据。 需要向用户授予对 Microsoft Power Platform 中 Dataverse 虚拟表的访问权限，以及对 Dynamics 365 Human Resources 中数据的访问权限。

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>启用对 Power Platform 中 Dataverse 虚拟表的访问权限

启用对 Power Platform 中 Dataverse 虚拟表的访问权限的第一步是针对 Dataverse 虚拟表终结点在 Power Platform 中为身份验证设置您的应用程序。 [Microsoft Dataverse 开发人员指南](/powerapps/developer/data-platform)中概述了执行此操作的步骤。

  - 对于单租户应用注册：[使用单租户服务器到服务器身份验证](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - 对于多租户应用注册：[使用多租户服务器到服务器身份验证](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>为 ATS 集成创建安全角色

创建应用程序用户后的步骤之一是将用户分配给定义应用程序对终结点具有的访问权限的安全角色。 对于单租户应用注册，这是[应用程序创建](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation)中的步骤 7；对于多租户注册，这是[为应用程序用户创建安全角色](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user)中的步骤 7。 

您向其分配应用程序用户的角色应该具有对用于 ATS 集成的数据实体的访问权限。 当前不存在，因此需要创建新安全角色。 可以按照[创建安全角色](/power-platform/admin/create-edit-security-role#create-a-security-role)中概述的步骤创建新角色。

对于新角色，必须至少向新角色的 **自定义实体** 上的以下实体分配适当的访问权限。 请注意，如果集成使用更广泛的应用程序数据，您可能需要添加其他实体。 创建新角色后，可以将其分配给应用程序用户。

  - 基本工作人员 (mshr)
  - 可雇用的应聘者 (mshr)
  - 证书能力 (mshr)
  - 证书类型 (mshr)
  - 公司
  - 薪酬工作职能 (mshr)
  - 薪酬工作类型 (mshr)
  - 国家/地区 (mshr)
  - 部门 (mshr)
  - 教育能力 (mshr)
  - 教育程度 (mshr)
  - 教育学科 (mshr)
  - 教育要求 (mshr)
  - 身份证明 (mshr)
  - 身份证明类型 (mshr)
  - 机构 (mshr)
  - 签发机构 (mshr)
  - 工作薪酬 (mshr)
  - 工作 (mshr)
  - 教育程度 (mshr)
  - 当事方联系人 (mshr)
  - 人员 (mshr)
  - 人员地址 (mshr)
  - 人员筛选 (mshr)
  - 职位类型 (mshr)
  - 职位 V2 (mshr)
  - 专业经验能力 (mshr)
  - 评级级别 (mshr)
  - 评级模型 (mshr)
  - 原因代码 (mshr)
  - 招聘请求 (mshr)
  - 招聘请求位置 (mshr)
  - 招聘请求职位 (mshr)
  - 招聘请求技能 (mshr)
  - 筛选类型 (mshr)
  - 技能能力 (mshr)
  - 技能 (mshr)
  - 标题 (mshr)
  - 退伍军人状态 (mshr)
  - 工作人员 (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>授予对 Human Resources 数据的应用程序权限

第二步是通过将它链接到 Human Resources 应用程序中的用户来确保向应用程序授予对 Human Resources 中数据的适当权限。 对于应用程序用户，在调用操作的 Dataverse 中的用户（应用）标识的上下文中完成通过 Dataverse 虚拟表的服务器到服务器调用。 然后，虚拟表适配器服务在 Human Resources 中查找关联的用户并在该用户的上下文中运行查询。 这意味着必须在 Human Resources 中创建用户并分配正确的角色，才能提供对集成应用程序所需数据的访问权限。

还需要向 Human Resources 用户分配对 Human Resources 中数据的正确权限。 **招聘应用程序** (HcmRecruitingIntegrator) 角色提供有对与招聘数据集成所需的主要实体的特权。 可以将此角色分配给 **用户** 页面中的应用程序用户以授予对数据的适当访问权限。 有关 Human Resources 安全角色的详细信息，请参阅[基于角色的安全性](/fin-ops-core/dev-itpro/sysadmin/role-based-security)。

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>设置具有适当权限的新用户

若要设置具有适当权限的新用户，请按照以下步骤操作：

  1. 在 Human Resources 中打开 **用户** 页面，然后选择 **新建**。
  2. 为新应用程序用户输入 **用户 ID** 和 **用户名**。 例如，您可以输入“RecruitingIntegration”。

      > [!NOTE]
      > 如果应用没有 Microsoft Azure Active Directory (Azure AD) 用户帐户或电子邮件地址，您可以在用户的电子邮件地址和提供商中输入“RecruitingApp”之类的内容。

  3. 在 **用户的角色** 快速选项卡上，选择 **分配角色** 操作。
  4. 在 **将角色分配给用户** 窗格中，选择 **招聘应用程序**，然后选择 **确定**。
  5. 保存新的用户记录。

### <a name="link-the-new-human-resources-user-to-the-application"></a>将新的 Human Resources 用户链接到应用程序

创建用户后，必须在 **Azure Active Directory 应用程序** 窗体中为应用程序创建一条记录，以将应用链接到 Human Resources 用户。

  1. 打开 **Azure Active Directory 应用程序** 窗体，然后选择 **新建**。
  2. 在 **客户端 ID** 字段中，输入为应用程序创建的应用程序用户的客户端 ID。
  3. 在 **名称** 字段中，输入集成应用程序的名称。
  4. 在 **用户 ID** 字段中，选择为招聘集成创建的新 Human Resources 用户。
  5. 保存新记录。

然后，应用程序将具有对 Human Resources 数据的访问权限，仅限于招聘应用程序集成所需的数据。

## <a name="see-also"></a>请参阅

[招聘工作应聘者](hr-personnel-recruit.md)<br>
[什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)<br>
[使用 Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>
[使用 Web API 创建和更新选项集](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
