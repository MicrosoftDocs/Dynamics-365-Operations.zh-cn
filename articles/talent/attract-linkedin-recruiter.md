---
title: 在 Microsoft Dynamics 365 Talent - Attract 中使用 LinkedIn Recruiter 寻求应聘者
description: 使用 Microsoft Dynamics 365 Talent - Attract 提供的 LinkedIn 集成通过 LinkedIn Recruiter 寻求应聘者。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 366dc2be6e35098dba4b26a34bb75a84913549f5
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008562"
---
# <a name="source-candidates-with-linkedin-recruiter"></a>使用 LinkedIn Recruiter 搜寻候选人
[!include[banner](../includes/banner.md)]

LinkedIn 是世界上最大的在线职业网络，让您可以访问世界顶级人才。 Microsoft Dynamics 365 Talent: Attract 让您可以直接从 LinkedIn 中寻求应聘者。 因此，找到填补空缺职位所需的人才比以往任何时候都更容易。 通过 Attract 设置与 LinkedIn 的连接后，您可以查看适合您的职位的潜在的 LinkedIn 应聘者，而且只需点击一下即可将其导出到 Attract。

如果您似乎没有此功能，请与您的管理员联系。您的管理员必须[设置与 LinkedIn 的集成](./attract-admin-linkedin.md)，您才可以从 Attract 利用 LinkedIn Recruiter。 然后，您可以设置与 LinkedIn Recruiter 的连接并开始查找应聘者。

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>设置与 LinkedIn Recruiter 的连接

您必须先设置与 LinkedIn Recruiter 的连接，然后才能够开始通过 Attract 使用 LinkedIn Recruiter。 要执行此步骤，您需要有 LinkedIn Recruiter 凭据。

1. 选择页面右上角的**设置**按钮（齿轮图标）。
2. 选择**用户设置**。
3. 在**连接**选项卡上，选择 **LinkedIn** 旁边的**连接**。 请按照 LinkedIn 提供的说明进行操作。

    ![[从 Attract 设置与 LinkedIn Recruiter 的连接](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>在 Attract 中查看 LinkedIn 应聘者

在您连接到 LinkedIn Recruiter 后，您可以在 Attract 中查看应聘者的 LinkedIn 个人资料。

1. 在 Attract 中，在左侧选择**职位**或**人才池**，然后选择申请人。

    ![[在 Attract 中查看 LinkedIn 应聘者](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. 在应聘者的个人资料中，选择 **LinkedIn** 选项卡。您可以查看应聘者的个人资料，以及 InMail 历史记录和 LinkedIn 注释历史记录。

从这里，您可以将应聘者保存到 LinkedIn Recruiter 项目，发送 inMail，或使用 Update Me 在 LinkedIn Recruiter 中设置预警。

> [!NOTE]
> 当应聘者的 Attract 信息与 LinkedIn 信息匹配时，应聘者的 LinkedIn 个人资料将显示在 Attract 中。 以下是使用的匹配规则：
> 
> 1. 如果电子邮件地址和 LinkedIn 会员 ID 在 Attract 和 LinkedIn 中匹配，则会显示应聘者的个人资料。 应聘者仍然可以选择从 Attract 链接或取消链接他们的 LinkedIn 个人资料。
> 2. 如果电子邮件地址或 LinkedIn 会员 ID 不匹配，您会看到可能的应聘者的列表。 然后，您可以在列表中选择应聘者并链接个人资料。
> 3. 如果没有合适的匹配，则会通知您未找到匹配项。

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a>点击一下将 LinkedIn 应聘者导出到 Attract

当您在 LinkedIn Recruiter 中查看应聘者时，您可以将他们导出到您当前在 Attract 中开启的职位中。 对于此步骤，您需要 Attract 中的招聘人员或招聘经理权限。 有关 Attract 中角色的详细信息，请参阅 [Attract 中的安全和角色管理](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract)。

您还必须确保该职位具有“应聘者”阶段。 有关详细信息，请参阅[应聘者活动](./activities-attract.md#prospect-activity)。

1. 在 Attract 中，创建职位、分配适当的角色并激活职位。
2. 在 LinkedIn Recruiter 中，为职位查找合适的应聘者，然后转到应聘者的个人资料。
3. 在联系人卡片的职位搜索框中，使用在 Attract 中激活的职称或职位 ID 查找职位。 如果找不到职位，请选择**更改 ATS** 查找正确的 Attract 实例。
4. 选择职位，然后选择**导出**。
5. 在 Attract 中，打开职位。 导出的应聘者将显示在职位的**应聘者**选项卡上。

## <a name="view-attract-information-in-linkedin-recruiter"></a>在 LinkedIn Recruiter 中查看 Attract 信息

在 LinkedIn Recruiter 中，您可以跟踪应聘者是否申请了您组织的其他职位，查看应聘者在职位申请各个阶段的位置，以及从 Attract 查看反馈和备注。

1. 打开 LinkedIn Recruiter，选择应聘者个人资料。
2. 悬停在 **ATS 内**上。
3. 选择以下任一选项来查看 Attract 中存储的应聘者信息：

    - **工作和状态** – 查看应聘者所属的工作、最新状态，以及应聘者在每个工作中的进度。
    - **面试反馈** – 查看面试官在 Attract 中提交的反馈。
    - **注释** – 查看在 Attract 中为该应聘者输入的所有注释。

    ![[从 LinkedIn Recruiter 查看 Attract 信息](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> 如果应聘者未通过“应聘者”阶段，应聘者和申请数据不会同步到 LinkedIn Recruiter。

## <a name="view-linkedin-talent-pools"></a>查看 LinkedIn 人才池

如果应聘者同意与您组织中的任何用户共享其 LinkedIn 个人资料，将在 Attract 中创建新应聘者记录。 这些应聘者随后将出现在系统创建的 LinkedIn 人才池中。

1. 在 Attract 中，在左侧选择**人才池**。
2. 选择 LinkedIn 人才池。 您将看到来自 LinkedIn 的应聘者及其存根个人资料的列表。 存根个人资料包含应聘者的名字、姓氏和电子邮件地址（如果应聘者选择共享）。

## <a name="see-also"></a>请参阅

[LinkedIn 常见问题](./attract-linkedin-faq.md)

[设置与 LinkedIn 的集成](./attract-admin-linkedin.md)

[创建工作](./creating-jobs-attract.md)

[将工作从 Attract 发布到 LinkedIn](./attract-post-jobs-to-linkedin.md)

[LinkedIn 集成疑难解答](./attract-troubleshoot-linkedin.md)
