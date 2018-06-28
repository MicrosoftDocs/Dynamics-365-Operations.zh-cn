---
title: "访问 Dynamics 365 for Talent 中的预览功能"
description: "此主题介绍管理员可如何启用预览功能，并且列出了当前可预览的功能。"
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.translationtype: HT
ms.sourcegitcommit: dc2ab66bf6e3195e1ebf394f99182f59c3ee2125
ms.openlocfilehash: 63e0a52919e12c1f497e6809244939c6047826a7
ms.contentlocale: zh-cn
ms.lasthandoff: 05/15/2018

---

# <a name="access-preview-features-in-dynamics-365-for-talent"></a>访问 Dynamics 365 for Talent 中的预览功能 

[!include[banner](../includes/banner.md)]

在持续推出产品功能时，我们希望让客户尽快体验新功能。 管理员可以在自己的环境中查看和使用预览功能。 这些功能几乎已针对普通使用准备就绪，并经过了大量测试。 我们正在征求最后一轮的客户反馈和验证，之后就会公开发布。

此主题介绍管理员可如何启用预览功能，并且列出了当前可预览的功能。 发布功能以公开推出和发布新功能以预览时，将更新此列表。 发布新功能以预览时，不提供通知。 用户只需启动即可查看这些功能。

## <a name="enable-or-disable-preview-features"></a>启用或禁用预览功能

可使用 Microsoft Dynamics 365 for Talent 管理员中心中的**预览功能**设置启用或禁用预览功能。 默认情况下，已关闭此设置。 预览功能的启用或禁用操作特定于环境。

> [!IMPORTANT]
> 通过开启**预览功能**设置，即对组织中该环境的所有用户启用了预览功能。 通过关闭此设置，即禁用了预览功能，并且您的用户不能访问这些功能。 在 Talent 中，对预览功能的支持受限。 预览功能可以使用的隐私和安全措施更少，并且 Talent 服务级别协议中不涵盖预览功能。 不应使用预览功能处理个人数据（即可能用于确认您的身份的所有信息），也不应处理其他与法律或法规遵从性要求有关的数据。

### <a name="enable-or-disable-preview-features-for-your-organization"></a>为组织启用或禁用预览功能

#### <a name="attract"></a>Attract

1. 登录 Microsoft Dynamics 365 for Talent: Attract。
2. 在右上角的**设置**菜单（齿轮符号）中，选择**管理员设置**。
3. 在**功能管理**选项卡上，选择**预览功能**旁边的选项，使其变为蓝色。
4. 刷新浏览器以开始查看新功能。 （所有已登录用户都会在下次登录时看到这些功能，这些用户也可以刷新浏览器以立即查看这些功能。）

#### <a name="core-hr"></a>Core HR

1. 登录 Talent。 将打开“核心人力资源”工作区，可在其中完成其余步骤。 
2. 选择**系统管理 \> 链接系统参数**。
3. 在**系统参数**页**预览功能**选项卡上，将**为所有用户启用预览模式**选项设置为**是**，以便启用预览功能。

> [!NOTE]
> 若要禁用预览功能，请使用相同的基本步骤。 禁用后，您的用户不能访问预览功能，并且预览功能的相关流程中可能出错。

## <a name="features-that-are-currently-in-preview"></a>当前的预览功能

### <a name="attract"></a>Attract

- **工作模板** – 现在可以创建聘用流程模板。 用户已经可以自定义特定工作的聘用流程。 但是，现在则可以为该流程创建模板，然后在创建特定工作时选择相应模板。 因此，此功能可帮助简化工作设置流程。
- **求职站点** – 现在的求职站点版本仅列举所有开放工作。 但是，以后将向该站点添加更多功能。 可以将工作标记为内部或外部。 登录该站点的内部用户将看到内部工作和外部工作。 但是，非内部用户和未登录用户只能查看外部工作。
- **工作发布** – 现在可向求职站点发布工作。
- **LinkedIn 工作发布** – 现在可向 LinkedIn 发布工作。

    > [!NOTE]
    > 只有订阅了一个或多个 LinkedIn 工作清单产品的客户才可查看发布的工作。 否则，客户只有明确搜索某个工作，才能看到该工作。 工作发布到 LinkedIn 时，存在延迟。 工作从 Attract 发布后，可能需要几小时才会显示。

- **候选人申请** – 内部候选人和外部候选人现在都可以直接从求职站点的工作页申请。
- **聘约管理** – 用户现在可通过包含占位符的模板创建录用信。 在候选人推进到聘约阶段，招聘人员和和招聘经理可使用录用工具通过模板准备候选人的正式聘约，发送聘约供内部批准，最后将聘约发给候选人签署。 将随时间向聘约工具增加大量新功能，而在我们准备好发布这些功能供预览时，将使用这些功能更新以前的功能。

### <a name="core-hr"></a>Core HR

- **开放登记** – 福利开放登记让员工可以在选择福利时获得简单的自助式体验。 人力资源 (HR) 管理员可使用易于使用的引导式解决方案针对组织和针对员工的登记体验配置福利开放登记流程。

## <a name="feedback"></a>反馈

无论反馈正面还是负面，我们都希望倾听您对使用预览功能的看法。 希望您在使用这些功能或其他功能时，定期在以下站点上发布反馈。

- [社区](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – 此站点是很好的资源，用户可在这里讨论使用案例，提问和获得社区帮助。
- 可使用以下站点提供产品观点方面的建议。 告知我们您希望在产品中看到的功能，以及您认为应对现有功能进行的任何更改。

    - [Attract 观点](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

请勿在提交反馈或产品评论时包含个人数据（可用于确认您的身份的任何信息）。 可能会对收集的信息进行更深入的分析，但在适用的隐私法律下不会用于回应申请。 在这些计划下单独收集的个人数据应遵守 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement)。

> [!TIP]
> 将本主题加入书签，并经常回访以在我们发布新预览功能后随时掌握相关数据。
