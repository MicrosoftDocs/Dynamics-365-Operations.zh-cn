---
title: "流程中的活动"
description: "本主题提供有关可用于招聘流程的活动的各个类型的信息。"
author: 
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: ccd9e2d0ff1f7fb6825c6823936b4013b3054f5d
ms.contentlocale: zh-cn
ms.lasthandoff: 10/22/2018

---

# <a name="activities-in-the-hiring-processes"></a>招聘流程中的活动

[!include[banner](../includes/banner.md)]

活动可以在 Microsoft Dynamics 365 for Talent: Attract 中作为招聘流程的一部分添加。 活动可以添加到流程模板，或者它们可以直接添加到工作中的招聘流程。 当定义工作后，会选择流程模板，模板中包含的活动将应用到工作。 如果模板没有选择，则使用默认模板。 招聘流程也可以在应用模板后在工作上修改。

> [!NOTE] 
> 流程模板随综合招聘附件提供。

## <a name="prospect-activity"></a>应聘者活动

应聘者活动控制应聘者是否可以添加到工作中。 默认情况下，应聘者可以添加到工作中。 若要关闭应聘者活动，请将**启用应聘者**选项设置为**关**。 在应聘者活动打开时，招聘经理可以添加和查看应聘者，**应聘者**选项卡显示在工作上。

## <a name="application-activity"></a>申请活动

申请活动是招聘流程模板的必要项目。 要在应聘者发送申请或被添加到申请阶段时向其发送电子邮件，请将**向应聘者发送邮件**选项设置为**开**。

## <a name="scheduler-activity"></a>计划程序活动

计划程序活动是可选的。 此活动具有两个组件：应聘者可用日期和计划。 应聘者可用日期组件允许您使用电子邮件请求应聘者的可用日期。 计划组件提供计划应聘者和招聘团队的面试的能力。 在计划活动中，可以配置以下选项：**请求应聘者可用日期**、**联机会议**和**向应聘者发送邮件**。

- 要向应聘者发送电子邮件以请求其可用日期，请将**请求应聘者可用日期**选项设置为**开**。 如果您将此选项设置为**关**，此步骤不会在工作的招聘流程中显示。
- 若要使用 Skype for Business 实时传输或进行电话会议，请将**联机会议**字段设置为 **Skype for Business**。 正确的**加入 Skype 会议**链接随后将添加到发送给面试官的面试会议请求中。
- 要向应聘者发送电子邮件以最终确定计划，请将**向应聘者发送邮件**选项设置为**开**。 如果您将此选项设置为**关**，仅当应聘者登录应聘者门户时他们才会收到面试计划。

## <a name="feedback-activity"></a>反馈活动

反馈活动是可选的。 此活动允许面试参与者为申请人输入建议。 他们还可以输入要添加的任何反馈注释。 如果打开**继承来自招聘团队的反馈参与者**选项，招聘人员、招聘经理和面试官将自动进入反馈活动。 组织可以允许面试官在提交他们自己的反馈前查看其他人员的反馈。 组织还可以允许面试官在提交反馈后编辑反馈。

## <a name="interview-activity"></a>面试活动

面试活动是可选的。 此活动具有三个组件：应聘者可用日期、计划和反馈。 应聘者可用日期组件允许您使用电子邮件请求应聘者的可用日期。 计划组件提供计划应聘者和招聘团队的面试的能力。 在计划活动中，可以配置以下选项：**请求应聘者可用日期**、**联机会议**和**向应聘者发送邮件**。

- 要向应聘者发送电子邮件以请求其可用日期，请将**请求应聘者可用日期**选项设置为**开**。 如果您将此选项设置为**关**，此步骤不会在工作的招聘流程中显示。
- 若要使用 Skype for Business 实时传输或进行电话会议，请将**联机会议**字段设置为 **Skype for Business**。 正确的**加入 Skype 会议**链接随后将添加到面试会议请求中。
- 要向应聘者发送电子邮件以最终确定计划，请将**向应聘者发送邮件**选项设置为**开**。 如果您将此选项设置为**关**，仅当应聘者登录应聘者门户时他们才会收到面试计划。

反馈组件允许人员为申请人输入建议。 他们还可以输入要添加的任何反馈注释。 如果打开**继承来自招聘团队的反馈参与者**选项，招聘人员、招聘经理和面试官将自动进入反馈组件。 组织可以允许面试官在提交他们自己的反馈前查看其他人员的反馈。 组织还可以允许面试官在提交反馈后编辑反馈。

## <a name="powerapps-activity"></a>PowerApps 活动

PowerApps 活动让您可以在招聘流程中嵌入 Microsoft PowerApps 应用。 此应用可能对所有申请人、仅内部申请人、仅外部申请人是必要的，也可能不是必要的。 如果此应用被标记为必要，则必须在推进此阶段前完成它。 如果此应用未标记为必要，此活动是可选步骤，即使未完成应用仍可以推进此阶段。

若要将 PowerApps 活动保存到招聘流程，您必须输入 PowerApps ID。 若要查找 PowerApps ID，请转到 [PowerApps](https://web.powerapps.com)，选择**应用**，然后选择**详细信息**。

如果您选择**允许为此活动添加参与者**选项，可以为使用 PowerApps 活动的申请添加其他参与者。 例如，组织为技术角色创建了作为面试问题库的 PowerApps 应用。 组织现在在招聘新的软件开发人员并向软件开发人员角色的招聘流程添加了 PowerApps 活动。 如果选择了**允许为此活动添加参与者**选项，查看软件开发人员角色申请人的招聘人员或招聘经理可以向 PowerApps 活动添加人员。 这些人员然后可以查看具有面试问题的应用。

> [!NOTE]
> PowerApps 活动仅通过综合招聘附件提供。

## <a name="youtube-activity"></a>YouTube 活动

YouTube 活动允许您作为招聘流程的一部分共享 YouTube 视频。 若要将 YouTube 活动保存到招聘流程，您必须指定 YouTube 视频的 URL。 对于 PowerApps 活动，您可以允许参与者被添加到活动。 如果您选择**仅对应聘者显示**选项，视频将仅作为应聘者体验的一部分显示。 它不会显示在 Attract 中的招聘流程中。

> [!NOTE]
> YouTube 活动仅通过综合招聘附件提供。

## <a name="web-content-activity"></a>Web 内容活动

Web 内容活动允许您在招聘流程中嵌入在线内容。 若要将 Web 内容活动保存到招聘流程，您必须指定内容的 URL。 对于 PowerApps 和 YouTube 活动，您可以允许参与者被添加到活动。 如果您选择**仅对应聘者显示**选项，内容将仅作为应聘者体验的一部分显示。 它不会显示在 Attract 中的招聘流程中。 您可以选择内容的显示尺寸。

> [!NOTE]
> Web 内容活动仅通过综合招聘附件提供。

## <a name="microsoft-forms-activity"></a>Microsoft 窗体活动

Microsoft 窗体活动让您可以在招聘流程中嵌入 Microsoft 窗体。 Microsoft 窗体允许您创建测试、调查和轮询。 若要将 Microsoft 窗体活动保存到招聘流程，您必须指定窗体的 URL。 对于 PowerApps、YouTube 和 Web 内容活动，您可以允许参与者被添加到活动。 如果您选择**仅对应聘者显示**选项，窗体将仅作为应聘者体验的一部分显示。 它不会显示在 Attract 中的招聘流程中。

在 Microsoft 窗体中，作者可以更改其设置以允许其组织外的用户对调查或测试作出响应。 在这种情况下，用户匿名提交响应。 如果要查看哪些人参与了您的调查或测试，您可以要求回应者在调查或测试中输入其姓名。

> [!NOTE]
> Microsoft 窗体活动仅通过综合招聘附件提供。

