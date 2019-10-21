---
title: 访问 Microsoft Dynamics 365 Talent 中的预览功能
description: 此主题介绍管理员可如何启用 Microsoft Dynamics 365 Talent 中的预览功能，并且列出了当前可预览的功能。
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: e607c2ba4b544d60c97d98bd49b07d912d83ebc6
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008694"
---
# <a name="manage-preview-features"></a>管理预览功能

[!include[banner](../includes/banner.md)]

在持续推出适用于 Microsoft Dynamics 365 Talent 的人力资本管理 (HCM) 功能时，我们希望让客户尽快体验新功能。 管理员可以在自己的环境中查看和使用预览功能。 这些功能几乎已针对普通使用准备就绪，并经过了大量测试。 我们正在征求最后一轮的客户反馈和验证，之后就会公开发布。

此主题介绍如何启用预览功能，并且列出了当前可预览的功能。 发布功能以公开推出和发布新功能以预览时，将更新此列表。 发布新功能以预览时，不提供通知。 用户只需启动即可查看这些功能。 有关 Talent 中的新功能的详细信息，请参阅 [Dynamics 365 Talent 新增功能或更改](./whats-new.md)和 [Dynamics 365 和 Power Platform 发行说明](https://docs.microsoft.com/business-applications-release-notes)。

## <a name="enable-or-disable-preview-features"></a>启用或禁用预览功能

若要访问预览功能，必须首先在您的环境中启用。 预览功能的启用或禁用特定于环境。

> [!IMPORTANT]
> 开启**预览功能**设置时，即对组织中该环境的所有用户启用了预览功能。 关闭此设置时，即禁用了预览功能，并且您的用户不能访问这些功能。 在 Talent 中，对预览功能的支持受限。 预览功能可以使用的隐私和安全措施更少，并且 Talent 服务级别协议 (SLA) 中不涵盖预览功能。 不应使用预览功能处理个人数据（即可能用于确认您的身份的所有信息），也不应处理其他与法律或法规遵从性要求有关的数据。

### <a name="attract"></a>Attract

1. 登录到 Microsoft Dynamics 365 Talent: Attract。
2. 在右上角的**设置**菜单（齿轮符号）中，选择**管理中心**。
3. 在**功能管理**选项卡上，选择**预览功能**旁边的选项，使其变为蓝色，然后说出**打开**。

    ![启用 Attract 中的预览功能](./media/attract-enable-preview-features.png)

4. 选择或取消单个预览功能的选择。 如果不执行任何操作，则启用所有可用预览功能。
5. 刷新浏览器以开始查看新功能。 所有已登录用户都会在下次登录时看到这些功能，这些用户也可以刷新浏览器以立即查看这些功能。

> [!NOTE]
> 可能需要为某些预览功能执行更多配置。 单击预览功能旁边的链接完成该功能的设置。

### <a name="core-hr"></a>Core HR

1. 登录 Talent。
2. 选择 **系统管理**，然后选择**链接**选项卡。
3. 在**系统管理**页中的**设置**下，选择**系统参数**。
4. 在**系统参数**页中，选择**预览功能**选项卡。
5. 将**为所有用户启用预览模式**选项设置为**是**以启用预览功能。

    ![启用 Core HR 中的预览功能](./media/corehr-enable-preview-features.png)

> [!NOTE]
> 要禁用预览功能，请执行相同步骤，但将**为所有用户启用预览模式**选项设置为**否**。 禁用后，您的用户不能访问预览功能，并且预览功能的相关流程中可能出错。

### <a name="onboard"></a>入职

Microsoft Dynamics 365 Talent: Onboard 当前无预览功能。

## <a name="features-that-are-currently-in-preview"></a>当前的预览功能

### <a name="attract"></a>Attract

- [应聘者推荐](./intelligent-recommendations.md#candidate-recommendations) - 如果有超过十名应聘者有简历或完整的个人资料，与工作要求最接近的应聘者将显示在“工作”页的**要考虑的申请人**部分。
- [工作推荐](./intelligent-recommendations.md#job-recommendations) - 如果您的求职站点上发布的工作超过十个，Attract 将为应聘者提供工作推荐。
- [Broadbean 集成](./posting-jobs-external.md#post-jobs-to-broadbean) – 可将工作从 Attract 发布到 Broadbean，后者是一个外部工作发布站点。 启用此预览功能后，您必须通过输入您的 Broadbean 用户名、客户 ID 和加密标记来完成安装。
- [分析](./analytic-reports.md) - 在分析中心中，招聘团队可以查看单个工作的关键指标，以及所有工作的聚合指标。
- [EEO](./activities-attract.md) – 可通过新活动类型使用预定义的窗体从应聘者处收集平等就业机会 (EEO) 和联邦合同合规性计划办公室 (OFCCP) 数据。 不能编辑预定义的窗体。
- [应聘者建议](./intelligent-recommendations.md#prospect-recommendations) – Attract 可以检查过去的申请人和当前应聘者，以便提供非常适合您的工作的应聘者列表。
- [相关性搜索](./attract-talent-pools.md#search-and-view-candidate-profiles) – 可搜索整个应聘者数据库以查找特定技能、姓名或教育背景。 Attract 搜索整个个人资料并突出显示找到的所有匹配项。 Attract 还搜索应聘者的所有可用文档并为搜索结果智能分级。
- [活动受众](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – 可将活动（如面试、计划或反馈）的受众设置为**所有应聘者**、**内部应聘者**或**外部应聘者**。 可以将客户活动（如 YouTube 视频、Web 内容和 Microsoft 窗体）交付给所有应聘者、仅内部应聘者、仅外部应聘者或招聘团队。
- [通过 LinkedIn 申请](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – 可在 Attract 求职站点上设置选项，以便让工作应聘者使用 LinkedIn 申请。 此功能可以简化应聘者的申请流程，方法是让应聘者使用自己的 LinkedIn 个人资料在您的求职站点上自动填写申请表。
- [来源跟踪](./source-tracking.md) – Attract 跟踪应聘者申请表的来源，以便提供宝贵信息，帮助您有针对性地开展招聘工作。 您也可以在向工作或人才池添加应聘者时选择申请来源。
- [银奖获得者](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – 如果任何应聘者非常适合您的组织，但是您曾经不能为其提供当前职位的延伸聘约，则可将其指定为银奖获得者。 在您下次有类似职位时，此功能可帮助缩短您的招聘时间。

### <a name="core-hr"></a>Core HR

- [验证职位层次结构数据](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – 您可以验证管理层次结构，以查找无意中导入的任何循环引用。
- [指定休假类型的原因代码](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – 您可为休假类型指定原因代码。
- [休假请求需要原因代码](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – 除了指定休假类型的原因代码之外，您还可以要求为休假请求提供原因代码。
- [为 HR 提供休假和缺勤交易记录列表](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – 您可以查看休假和缺勤交易的列表，以便帮助提供对休假余额的见解。

### <a name="onboard"></a>入职

Onboard 当前无预览功能。

## <a name="feedback"></a>反馈

希望您提供有关以上任何预览功能的体验信息。 希望您在使用这些功能或其他功能时，定期在以下站点上发布反馈：

- [社区](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – 此站点是很好的资源，用户可在这里讨论使用案例，提问和获得社区帮助。
- 告知我们您希望在产品中看到的功能，或您认为我们应对现有功能进行的任何更改。 请在以下站点提供产品观点方面的建议：

    - [Attract 观点](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR 观点](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Onboard 观点](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

切勿在提交反馈或产品评论时包含个人数据（可用于确认您的身份的任何信息）。 可能会对收集的信息进行更深入的分析，但在适用的隐私法律下不会用于回应申请。 在这些计划下单独收集的个人数据应遵守 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement)。

> [!TIP]
> 将本主题加入书签，并经常回访以在我们发布新预览功能后随时掌握相关数据。

## <a name="see-also"></a>请参阅

- [试用或购买 Talent 应用](https://dynamics.microsoft.com/talent/overview/)
- [新增功能](./whats-new.md)
- [版本说明](https://docs.microsoft.com/business-applications-release-notes/index)
- [获取 Talent 支持](./talent-support.md)
