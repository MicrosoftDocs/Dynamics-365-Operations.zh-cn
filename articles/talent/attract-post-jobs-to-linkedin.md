---
title: 将工作从 Attract 发布到 LinkedIn
description: 本主题说明如何使用 Dynamics 365 Talent - Attract 将工作发布到 LinkedIn。
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 782a2e5de6edf0e85c4d32a0910f5f3c01981a01
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460416"
---
# <a name="post-jobs-to-linkedin-from-attract"></a>将工作从 Attract 发布到 LinkedIn

[!include [banner](includes/banner.md)]

LinkedIn 是最大的在线职业网络，让您可以访问世界顶级人才。 Microsoft Dynamics 365 Talent: Attract 通过让您将工作直接从 Attract 发布到 LinkedIn，帮助您获得所需的人才。

Attract 让您可以在 LinkedIn 中发布 Limited Listings（有限列表），无需支付额外费用。 这些列表仅通过 LinkedIn 软件合作伙伴（如 Attract）提供。 它们不会出现在您公司的 LinkedIn 页面的 **求职** 面板中，因为只有付费列表出现在那里。 但会在潜在应聘者查看所有可申请工作时显示。 Limited Listings（有限列表）还显示在 LinkedIn 工作搜索中。

在 Attract 中[创建工作](./creating-jobs-attract.md)后，您只需选择一个按钮即可将您的工作放在 LinkedIn 上数千名潜在应聘者面前。

下表显示了您可以在 LinkedIn 上执行的操作，具体取决于您的用户角色。

| 角色 | 您可以执行的操作 |
|---|---|
| 管理 | 发布、重新发布和取消发布 |
| 雇用经理 | 只读 |
| 招聘人员 | 发布、重新发布和取消发布 |
| 面试人员 | 禁止访问 |
| 只读 | 只读 |

有关 Attract 中用户角色的详细信息，请参阅 [Attract 中的安全和角色管理](./security-attract.md)。

如果您是管理员并需要有关如何使用 Attract 配置 LinkedIn 集成的更多信息，请参阅[为 Microsoft Dynamics 365 Talent - Attract 设置与 LinkedIn 的集成](./attract-admin-linkedin.md)。

发布到 LinkedIn 的工作将显示在实际的 LinkedIn 网站上。 LinkedIn 没有发布工作的测试环境。 因此，请确保您不会意外发布任何测试工作。

## <a name="post-jobs-to-linkedin"></a>将职位发布至 LinkedIn

1. 在 Attract 中，打开要发布到 LinkedIn 的工作。
2. 在 **发布** 选项卡上，选择与 LinkedIn 对应的 **立即发布** 按钮。

    [![Attract 将工作发布到 LinkedIn](./media/attract-post-job-to-linkedin.png)](./media/attract-post-job-to-linkedin.png)

3. 在 **创建“立即申请”网址** 对话框中，选择 **应聘者申请时可使用** 下的选项。 建议您选择 **Attract 中的链接**。
4. 选择 **完成**。
5. 在 **提交发布** 消息框中，选择 **确认**。

在 LinkedIn 成功完成发布后，Attract 中工作的 **发布** 部分将显示 LinkedIn 状态 **已发布**。 您的工作最多可能需要 48 小时在 LinkedIn 上显示。

当感兴趣的应聘者在您的列表旁边选择 **查看** 时，他们会看到完整的工作详细信息，以及您有关如何申请的信息。

通过 Attract 完成的所有工作发布都是 Limited Listings（有限列表）。 关 LinkedIn 上 Limited Listings（有限列表）的详细信息，请参阅 [Limited Listings（有限列表）与 Job Wrapping（工作包装）的 Premium Job Slots（高级职位空缺）](https://www.linkedin.com/help/recruiter/answer/79049)。

如果您在向 LinkedIn 发布工作时遇到问题，请参阅 [LinkedIn 和 Microsoft Dynamics 365 Talent - Attract 集成疑难解答](./attract-troubleshoot-linkedin.md)。

## <a name="see-also"></a>请参阅

[Attract 与 LinkedIn 集成的常见问题](./attract-linkedin-faq.md)

[为 Microsoft Dynamics 365 Talent - Attract 设置与 LinkedIn 的集成](./attract-admin-linkedin.md)

[在 Attract 中创建、审核和发布工作](./creating-jobs-attract.md)

[使用 LinkedIn Recruiter 寻求应聘者](./attract-linkedin-recruiter.md)

[LinkedIn 集成疑难解答](./attract-troubleshoot-linkedin.md)
