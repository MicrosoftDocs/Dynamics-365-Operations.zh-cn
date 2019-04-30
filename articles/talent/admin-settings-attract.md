---
title: Attract 中的管理员设置
description: 本主题说明如何为 Attract 中的组织和用户启用功能。
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0de215103306ef7115ba390b1b4855179979c77b
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "856362"
---
# <a name="admin-settings-in-attract"></a>Attract 中的管理员设置
[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attract 中的管理员中心包含配置设置、集成选项和 Attract 应用程序的设置选项。

## <a name="company-information"></a>公司信息

为公司输入一个显示名称，并添加公司徽标。 显示名称和徽标可以在工作职位和入职体验期间使用。

## <a name="linkedin-integration"></a>LinkedIn 集成

设置与 LinkedIn Recruiter System Connect (RSC) 的集成。 在使用您的 LinkedIn 凭据连接到 LinkedIn 后，您可以同步应聘者的 LinkedIn 个人资料、申请、面试反馈和招聘团队备注。 需要完全的 LinkedIn 招聘人员许可证。 有关 LinkedIn Recruiter 的详细信息，请参阅 [Recruiter System Connect (RSC) – 常见问题](https://www.linkedin.com/help/recruiter/answer/90483)。

## <a name="user-permissions"></a>用户权限

将角色分配给组织中的用户。 下列角色可用：**管理员**、**招聘人员**、**招聘经理**和**只读**。 有关用户权限的详细信息，请参阅 [Attract 中的安全和角色管理](./security-attract.md)。

## <a name="feature-management"></a>功能管理

因为添加了新功能，它们可以在公开预览中发布。 公开预览功能未满足所有服务要求。 接收它们，即表明您同意与外部系统共享您的数据。 您可能会发现您的组织不需要发布的所有新功能。 您可以根据您的组织的需求打开或关闭公开预览功能。

## <a name="template-management"></a>模板管理

流程模板包含应作为工作招聘流程的一部分包含的所有活动。 您的组织可以允许所有团队成员或仅管理员创建招聘流程模板。 若要允许团队成员创建他们自己的招聘流程模板，请打开“模板管理”功能。 有关流程模板的详细信息，请参阅 [Attract 中的流程模板](./process-templates-attract.md)。

## <a name="email-template-settings"></a>电子邮件模板设置

组织可以为各种场景创建电子邮件模板。 您可以选择包含在电子邮件模板中的标题图像。 选定的标题随后将显示在所有电子邮件模板中。 在模板页脚中，您可以出于宣传目的添加您的组织的隐私声明和使用条款的链接。 有关详细信息，请参阅 [Attract 中的电子邮件模板](./email-templates.md)。

## <a name="offer-process"></a>聘约流程

您可以为工作聘约配置审核流程。 例如，您可以指定在向应聘者发送聘约前是否必须对其审核。 您还可以要求审核人为其聘约决定添加注释。

两个审核工作流可用：**并行**和**顺序**。

- **并行** – 同时向所有审核人发送审核。
- **顺序** – 按照特定顺序向审核人发送审核。

您还可以配置与应聘者体验相关的选项。 例如，一个选项允许您指定应聘者能否在不进行其他讨论的情况下拒绝聘约。 如果您将**允许应聘者不进行其他讨论拒绝聘约**选项设置为**否**，**拒绝聘约**按钮将对应聘者可用。 如果将此选项设置为**是**，应聘者可以通过选择原因然后选择**拒绝聘约**来拒绝聘约。

您还可以设置并强制执行聘约的到期日期。 如果您将**所有聘约均必须设置到期日期**选项设置为**是**，聘约将在您指定的小时数或天数后过期。

有关聘约管理的详细信息，请参阅[设置聘约管理](./offer-setup.md)。
