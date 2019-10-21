---
title: 为 Microsoft Dynamics 365 Talent - Attract 设置与 LinkedIn 的集成
description: 本主题说明如何为 Microsoft Dynamics 365 Talent - Attract 配置 LinkedIn 集成，以便您可以轻松地将工作从 Attract 发布到 LinkedIn，并让您的招聘人员可以将他们的招聘信息与应聘者的 LinkedIn 个人资料同步。
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
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6b86cafdf364f2de051f3d8ceab7413c2c13c3a5
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009961"
---
# <a name="set-up-linkedin-integration"></a>设置 LinkedIn 集成

[!include[banner](../includes/banner.md)]

通过配置与 Microsoft Dynamics 365 Talent: Attract 的 LinkedIn 集成，帮助您的招聘人员和招聘经理吸引顶尖人才。 通过 Attract，您可以将工作直接发布到最大的在线职业网站 LinkedIn。

您通过 Attract 发布到 LinkedIn 的工作属于 Limited Listings（有限列表），您的公司无需支付额外费用。 这些列表仅通过 LinkedIn 软件合作伙伴（如 Attract）提供。 它们不会出现在您公司的 LinkedIn 页面的**求职**面板中，因为只有付费列表出现在那里。 但会在潜在应聘者查看所有可申请工作时显示。 Limited Listings（有限列表）还显示在 LinkedIn 工作搜索中。

Attract 提供了两种与 LinkedIn 集成的方式，以帮助您从这个受欢迎的职业网站中找到应聘者：

- 将工作从 Attract 发布到 LinkedIn。
- 从 LinkedIn 为 Attract 寻求应聘者。

您可以在“管理中心”的 **LinkedIn 集成**选项卡上配置这两个选项。 要打开“管理中心”，请转到 <https://attract.talent.dynamics.com/adminsettings>。

> [!NOTE]
> 要使用 Attract 的 LinkedIn Recruiter 集成，您需要[综合招聘加载项](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)和 [LinkedIn Recruiter 许可证](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18)。 有关详细信息，请参阅[哪个 Attract 版本？](./attract-comprehensive-hiring.md)。

如果您在向 LinkedIn 发布工作时遇到问题，请参阅 [LinkedIn 集成疑难解答](./attract-troubleshoot-linkedin.md)。

有关将工作发布到 LinkedIn 的其他方式的信息，请参阅 [LinkedIn 常见问题](./attract-linkedin-faq.md)。

## <a name="configure-job-posting-to-linkedin"></a>配置 LinkedIn 工作发布

您需要一个 [LinkedIn 公司 ID](https://aka.ms/findID)，然后才能将工作从 Attract 发布到 LinkedIn。 您的 LinkedIn 公司 ID 是一串数字，用于在 LinkedIn 中唯一标识您的公司。 有关详细信息，请参阅[将您的 LinkedIn 公司 ID 与 LinkedIn Job Board 关联 - 常见问题](https://aka.ms/findID)。

Attract 将您的工作发布源发送给 LinkedIn，LinkedIn 大约每天检查一次源。 您的工作最多可能需要 48 小时发布到网站上。

发布到 LinkedIn 的工作将显示在实际的 LinkedIn 网站上。 LinkedIn 没有发布工作的测试环境。 因此，请确保您不会意外发布任何测试工作。 

1. 在右上角的**设置**菜单（齿轮符号）中，选择**管理中心**。 或者，转到 <https://attract.talent.dynamics.com/adminsettings>。
2. 选择 **LinkedIn 集成**选项卡。
3. 在**公司名称**下，输入您公司的名称，在**公司ID** 下，输入您的 LinkedIn 公司 ID。 确保公司名称与公司 LinkedIn 页面上显示的名称相匹配。 有关 LinkedIn 公司 ID 的详细信息，请参阅[将您的 LinkedIn 公司 ID 与 LinkedIn Job Board 关联 - 常见问题](https://www.linkedin.com/help/linkedin/answer/98972)。

    如果您需要更改组织的任何信息，请参阅[更改组织的地址、技术联系人等](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more)。 如果您仍有问题，请联系 [LinkedIn 支持](https://www.linkedin.com/help/linkedin)。

4. 选择**保存**。

## <a name="set-up-linkedin-recruiter-with-attract"></a>为 LinkedIn Recruiter 设置 Attract 

要允许招聘人员通过 LinkedIn Recruiter 寻找工作，您必须在 Attract 中配置与 LinkedIn Recruiter 的集成。 要完成配置过程，您必须与组织的 LinkedIn Recruiter 合同中的管理员用户合作。

1. 在右上角的**设置**菜单（齿轮符号）中，选择**管理中心**。 或者，转到 <https://attract.talent.dynamics.com/adminsettings>。
2. 选择 **LinkedIn 集成**选项卡。

    [![开始 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. 选择**连接**开始设置。 您将被引导进入 LinkedIn 登录过程。
4. 如果您在多个 LinkedIn 合同中有席位，请选择要连接到 Attract 系统的合同。 如果您只在一个 LinkedIn 合同中有席位，则可以跳过此步骤。
5. 在 **Recruiter System Connect (RSC)** 下，选择**请求**。

    [![请求 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. **Recruiter System Connect (RSC)** 设置现在应显示为**合作伙伴就绪**。 如果您在此页面上看到**通知合作伙伴**，请等待几秒钟，选择**通知合作伙伴**，然后刷新页面。 设置现在应显示为**合作伙伴就绪**。

    [![指示请求的 Attract 端已完成的 Attract 视图](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. 要完成以下步骤，您必须拥有 LinkedIn Recruiter 合同的管理员权限。

    1. 使用您的管理员帐户登录 LinkedIn，然后在右上角选择 **LinkedIn Recruiter**。 
    2. 在页面顶部的**更多**菜单中，选择**管理员设置**，然后选择 **ATS** 选项卡。
    3. 要只为一个合同启用一键导出，请启用**合同级别访问(此合同的每个席位)**。 要为整个公司启用，请启用**公司级别访问(公司的每个合同)**。

    [![从 LinkedIn Recruiter 管理员打开 Attract 集成的视图](./media/EnableRSC.png)](./media/EnableRSC.png)

8. 在“Attract 管理中心”，选择 **LinkedIn集成**选项卡。**Recruiter System Connect (RSC)** 设置现在应显示为**已启用**。

    [![LinkedIn Recruiter 集成完成](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>在 Attract 中设置“通过 LinkedIn 申请”

您可以允许应聘者使用他们的 LinkedIn 个人资料申请您的工作。 有关“通过 LinkedIn 申请”的详细信息，请参阅 [LinkedIn 的力量无处不在：通过 LinkedIn 申请](https://blog.linkedin.com/2011/07/24/apply-with-linkedin)。

此功能现在处于预览阶段。 在执行这些步骤之前，请确保已启用“通过 LinkedIn 申请”。 有关如何启用预览功能的详细信息，请参阅[访问 Talent 中的预览功能](./access-preview-feature.md)。

1. 在右上角的**设置**菜单（齿轮符号）中，选择**管理中心**。 或者，转到 <https://attract.talent.dynamics.com/adminsettings>。
2. 选择 **LinkedIn 集成**选项卡。

    [![开始 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. 在**通过 LinkedIn 申请**旁边，选择**连接**开始设置。 您将在引导下了解 LinkedIn 中此流程的其余部分。

## <a name="see-also"></a>请参阅

[LinkedIn 常见问题](./attract-linkedin-faq.md)

[将工作从 Attract 发布到外部站点](./posting-jobs-external.md)

[使用 LinkedIn Recruiter 寻求应聘者](./attract-linkedin-recruiter.md)

[创建工作](./creating-jobs-attract.md)

[LinkedIn 集成疑难解答](./attract-troubleshoot-linkedin.md)
