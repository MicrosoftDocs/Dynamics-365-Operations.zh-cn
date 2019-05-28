---
title: 具有 LinkedIn Recruiter 的来源添加
description: 此主题提供有关如何使用机器学习获得工作和工作应聘者推荐的信息。
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517390"
---
# <a name="sourcing-with-linkedin-recruiter"></a>具有 LinkedIn Recruiter 的来源添加
[!include[banner](../includes/banner.md)]

LinkedIn 是全世界最大的人才数据库招，通常是招聘人员用来查找、联系和为招聘人员要招聘的工作寻求候选人的主要系统。 LinkedIn Recruiter 与  Dynamics 365 for Talent: Attract 集成让用户可以更轻松地招聘并在两个系统之间保持数据同步。

> [!NOTE]
> 您需要综合招聘附件和 LinkedIn Recruiter 席位才能够使用 LinkedIn Recruiter 与 Attract 的集成。

## <a name="set-up-linkedin-recruiter-with-attract"></a>为 LinkedIn Recruiter 设置 Attract 

您必须先配置对 Attract 实例的合同级别或公司级别的访问才能够使用 LinkedIn Recruiter 功能。 若要完成配置流程，您必须与作为 LinkedIn Recruiter 合同的管理员的用户合作。 请完成以下步骤来配置 LinkedIn Recruiter 与 Attract 集成。

1.  作为管理员登录到 Attract 并转到**管理员设置**。

2.  在左窗格中，单击 **LinkedIn 集成**选项卡。

[![开始 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  单击**连接**开始设置，然后在引导下完成 LinkedIn 登录流程。

4.  如果您有多个 LinkedIn 合同的座位，选择您希望连接到 Attract 系统的合同。 如果只有一个 LinkedIn 合同的座位，则不需要此步骤。

5.  LinkedIn 小组件现在将加载您的管理员设置并显示集成列表。 在**招聘人员系统连接**下，单击**请求**。

[![请求 LinkedIn Recruiter 集成的 Attract 管理员视图](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  在从 Attract 请求集成后，集成将显示为**合作伙伴就绪**，并可以从**招聘人员管理员设置**打开。 如果您在此页面看到**通知合作伙伴**，请等待几秒，单击**通知合作伙伴**，然后刷新页面。 现在应该显示为**合作伙伴就绪**。

[![指示请求的 Attract 端已完成的 Attract 视图](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

要完成下一步，您需要有 LinkedIn Recruiter 合同的管理员权限。

7.  使用理员帐户登录到 LinkedIn 并转到右上方的 LinkedIn Recruiter。 

8. 在屏幕顶部的**更多**菜单上，单击**管理员设置**，然后单击 **ATS** 选项卡。

Attract 系统将列出，并有可以打开的两三个选项。

9. 如果要为 **ATS 内指标**和 **ATS 内模板小组件**启用一键导出，请选择**公司级别访问**。 如果您要启用所有公司级别的访问功能以及 InMail 历史记录、注释历史记录和 InMail 存根模板访问，请选择**合同级别访问**。

10. 从您的 LinkedIn Recruiter **管理员 ATS** 设置打开所需的访问级别。

[![从 LinkedIn Recruiter 管理员打开 Attract 集成的视图](./media/EnableRSC.png)](./media/EnableRSC.png)

12. 作为 Attract 管理员返回 Attract 管理员设置，选择 **LinkedIn 集成** 选项卡。现在您应会看到显示所选访问级别已打开的**已启用**的 LinkedIn 小组件加载。

[![LinkedIn Recruiter 集成完成](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>使用 LinkedIn Recruiter 功能

在 Attract 管理员启用 LinkedIn Recruiter 功能后，招聘经理和招聘人员可以进行访问。 若要使用这些功能，请在**用户设置**下连接您的 LinkedIn 帐户。 管理员和用户设置均连接后，若干功能将可用。

### <a name="in-ats-profile-widget"></a>ATS 内模板小组件

您可以在 Attract 中查看应聘者的 LinkedIn 个人资料。 在 ATS 信息与其用户的 LinkedIn 信息匹配时，LinkedIn 小组件将显示应聘者的个人资料。

若要查看个人资料，请从工作或人才池转到应聘者个人资料。 在应聘者个人资料中，请选择 **LinkedIn** 选项卡，模板小组件将加载。 您还可以从此页将应聘者保存到您的 LinkedIn Recruiter 项目。
1. 如果 LinkedIn 找到了基于电子邮件和 LinkedIn 成员 ID 的匹配项（精确匹配），应聘者的个人资料将显示。 用户仍可以选择链接/取消链接个人资料。

2. 如果 LinkedIn 根据电子邮件或成员 ID 找不到应聘者，它会显示基于应聘者姓名的可能的应聘者匹配项列表，用户可以从中选择一个并链接个人资料。  

3. 如果 LinkedIn 基于姓名找不到任何应聘者，它将返回未找到匹配项。

### <a name="1-click-export"></a>一键导出 

在 LinkedIn 中寻求应聘者时，您可以将应聘者一键导出到您当前打开的工作中。 完成以下步骤打开一键导出。 在完成这些步骤之前，请确认您被分配了工作的招聘经理或招聘人员角色，并且工作具有**应聘者**阶段。

1.  创建工作，分配适当的角色，并激活工作。

2.  在激活工作后，导航到 LinkedIn Recruiter。

3.  查找您在寻找的应聘者，并转至其个人资料。

4.  使用联系人卡片中的工作搜索框，使用在 Attract 中激活的职位或工作 ID 查找工作。 如果未找到工作，请单击**更改 ATS** 查找正确的 Attract 实例。

5. 在选择工作后，请单击**导出**。 应聘者现在被 Attract 获取。

6.  转到 Attract，打开各自的工作。 您将找到刚才在工作的**应聘者**阶段导出的应聘者。

### <a name="in-ats-indicator"></a>ATS 内指标 

使用 LinkedIn recruiter，您可以跟踪应聘者是否已申请组织内的其他工作，查看他们在不同的工作申请阶段所处的位置，并查看 LinkedIn Recruiter 中来自 Attract 的反馈和备注。

1.  打开 LinkedIn Recruiter，找到您要寻找的应聘者的个人资料。

2.  向下滚动查看应聘者个人资料的 **ATS 内**部分。

3.  您可以使用此小组件来在 LinkedIn Recruiter 视图内查看有关 Attract 中显示的应聘者的所有信息。

4.  选择**工作和状态**选项卡查看他们所属的工作、最新状态，以及他们如何在每个工作之间移动。

5.  选择**面试反馈**选项卡查看面试官在 Attract 中提交的反馈。

6.  选择**注释**选项卡查看在 Attract 中为此申请人获取的注释。

> [!NOTE]
> 如果应聘者未通过“潜在人选”阶段，应聘者和申请数据不会同步到 LinkedIn Recruiter。

### <a name="inmail-history"></a>InMail 历史记录

LinkedIn InMail 历史记录可以通过 LinkedIn Recruiter 的合同级别访问获取。 在启用后，您可以查看应聘者的整个 InMail 历史记录。 您还可以看到组织中还有哪些人与应聘者交换了 InMail，但是不能查看他们之间发送的消息。

要查看 InMail 历史记录，转到应聘者的个人资料，转到 **LinkedIn** 选项卡并滚动到页面底部查看历史记录。 如果您与应聘者之间有讨论，您可以查看 InMail 历史记录。 InMail 的消息每隔几小时与 Attract 同步一次。

### <a name="notes-history"></a>注释历史记录 

LinkedIn 注释历史记录可以通过 LinkedIn Recruiter 的合同级别访问获取。 在启用后，您可以查看组织中的不同招聘人员获取的有关该应聘者的注释。

要查看注释历史记录，转到应聘者的个人资料，转到 **LinkedIn** 选项卡并滚动到页面底部查看历史记录。 您可以从 LinkedIn Recruiter 查看有关应聘者的所有注释。

### <a name="inmail-stub-profile"></a>InMail 存根模板

InMail 存根模板可以通过 LinkedIn Recruiter 的合同级别访问获取。 如果应聘者同意与您组织中的任何用户共享其 LinkedIn 个人资料，您可以在 Attract 中跟踪该应聘者，并且新应聘者记录将为每个应聘者创建。 如果应聘者已经存在于系统中并具有电子邮件地址或已选择与招聘人员共享其地址，您可以查看应聘者的电子邮件地址。

若要查看应聘者列表，请转到**人才池**查看系统创建的 LinkedIn 人才池。 此人才池包含从 LinkedIn 收到的应聘者及其存根模板的列表，显示应聘者的名字和姓氏。 如果应聘者选择共享其电子邮件地址，该候选人的电子邮件 ID 将显示。
