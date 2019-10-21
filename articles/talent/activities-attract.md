---
title: Microsoft Dynamics 365 Talent - Attract 中的流程中的活动
description: 本主题提供有关可在 Microsoft Dynamics 365 Talent - Attract 中的招聘流程中使用的各类活动的信息。
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
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
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2e40250bb801f6222d16400b2698e5b0df47a404
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008677"
---
# <a name="activities-in-hiring-processes"></a>招聘流程中的活动

[!include[banner](../includes/banner.md)]

活动可以在 Microsoft Dynamics 365 Talent: Attract 中作为招聘流程的一部分添加。 活动可以添加到流程模板，或者它们可以直接添加到工作中的招聘流程。 当定义工作后，会选择流程模板，模板中包含的活动将应用到工作。 如果模板没有选择，则使用默认模板。 招聘流程也可以在应用模板后在工作上修改。

> [!NOTE] 
> 流程模板随综合招聘附件提供。 有关详细信息，请参阅 [Attract 综合招聘加载项功能](./attract-comprehensive-hiring.md)。

## <a name="prospect-activity"></a>应聘者活动

应聘者活动控制应聘者是否可以添加到工作中。 默认情况下，应聘者可以添加到工作中。 若要关闭应聘者活动，请将**启用应聘者**选项设置为**关**。 在应聘者活动打开时，招聘经理可以添加和查看应聘者，**应聘者**选项卡显示在工作上。

> [!NOTE]
> 要允许从 LinkedIn 将应聘者添加到工作，您必须将**启用应聘者**选项设置为**开**。

## <a name="application-activity"></a>申请活动

申请活动是招聘流程模板的必要项目。 要在应聘者发送申请或被添加到申请阶段时向其发送电子邮件，请将**向应聘者发送邮件**选项设置为**开**。

## <a name="interview-schedule-and-feedback-activity"></a>面试时间表和反馈活动

此活动具有三个组件：应聘者可用日期请求、计划和反馈。 如果您希望作为流程的一部分包含候选人可用日期请求、计划和反馈，而不是作为招聘流程的一部分单独使用它们，应在工作模板中使用面试活动。 有关详细信息，请参阅[面试计划和反馈](interview-scheduling-feedback.md)。

## <a name="powerapps-activity"></a>PowerApps 活动

PowerApps 活动让您可以在招聘流程中嵌入 Microsoft PowerApps 应用。 此应用可能对所有申请人、仅内部申请人、仅外部申请人是必要的，也可能不是必要的。 如果此应用被标记为必要，则必须在推进此阶段前完成它。 **JobApplicationStatus** 字段只有在设置为**已完成**时，才会被视为已完成。 此字段位于 JobApplicationActivity 实体中，因此 PowerApps 应用需要先更新此字段，才能推进此阶段。 如果此应用未标记为必要，此活动是可选步骤，即使未完成应用仍可以推进此阶段。

若要将 PowerApps 活动保存到招聘流程，您必须输入 PowerApps ID。 若要查找 PowerApps ID，请转到 [PowerApps](https://web.powerapps.com)，选择**应用**，然后选择**详细信息**。

默认情况下，招聘经理、招聘人员及其委托人可使用 PowerApps 活动。 如果您选择**允许为此活动添加参与者**选项，可以为使用 PowerApps 活动的申请添加更多来自招聘团队的参与者。 例如，组织为技术角色创建了作为面试问题库的 PowerApps 应用。 组织现在在招聘新的软件开发人员并向软件开发人员角色的招聘流程添加了 PowerApps 活动。 如果选择了**允许为此活动添加参与者**选项，查看软件开发人员角色申请人的招聘人员或招聘经理可以向 PowerApps 活动添加面试官。 这些人员然后可以查看具有面试问题的应用。

> [!NOTE]
> PowerApps 活动仅通过综合招聘附件提供。 有关详细信息，请参阅 [Attract 综合招聘加载项功能](./attract-comprehensive-hiring.md)。

## <a name="youtube-activity"></a>YouTube 活动

YouTube 活动允许您作为招聘流程的一部分共享 YouTube 视频。 若要将 YouTube 活动保存到招聘流程，您必须指定 YouTube 视频的 URL。 可选择向**招聘团队**、**仅限内部应聘者**、**仅限外部应聘者**或**所有应聘者**显示内容。 与 PowerApps 活动一样，您可以允许将招聘团队参与者添加到活动。 如果选择对应聘者显示内容，视频将仅作为应聘者体验的一部分显示，不会在招聘过程中显示。

> [!NOTE]
> YouTube 活动仅通过综合招聘附件提供。 有关详细信息，请参阅 [Attract 综合招聘加载项功能](./attract-comprehensive-hiring.md)。

## <a name="web-content-activity"></a>Web 内容活动

Web 内容活动允许您在招聘流程中嵌入在线内容。 若要将 Web 内容活动保存到招聘流程，您必须指定内容的 URL。 可选择向**招聘团队**、**仅限内部应聘者**、**仅限外部应聘者**或**所有应聘者**显示内容。 与 PowerApps 和 YouTube 活动一样，您可以允许将招聘团队参与者添加到活动。 如果选择对应聘者显示内容，Web 内容将仅作为应聘者体验的一部分显示，不会在招聘过程中显示。 您可以选择内容的显示尺寸。

> [!NOTE]
> Web 内容活动仅通过综合招聘附件提供。 有关详细信息，请参阅 [Attract 综合招聘加载项功能](./attract-comprehensive-hiring.md)。

## <a name="microsoft-forms-activity"></a>Microsoft 窗体活动

Microsoft 窗体活动让您可以在招聘流程中嵌入 Microsoft 窗体活动。 Microsoft 窗体允许您创建测试、调查和轮询。 若要将 Microsoft 窗体活动保存到招聘流程，您必须指定窗体的 URL。 可选择向**招聘团队**、**仅限内部应聘者**、**仅限外部应聘者**或**所有应聘者**显示内容。 与 PowerApps、YouTube 和 Web 内容活动一样，您可以允许将招聘团队参与者添加到活动。 如果选择对应聘者显示内容，窗体将仅作为应聘者体验的一部分显示，不会在招聘流程中显示。

在 Microsoft 窗体中，作者可以更改其设置以允许其组织外的用户对调查或测试作出响应。 在这种情况下，用户匿名提交响应。 如果要查看哪些人参与了您的调查或测试，您可以要求回应者在调查或测试中输入其姓名。

> [!NOTE]
> Microsoft 窗体活动仅通过综合招聘附件提供。 有关详细信息，请参阅 [Attract 综合招聘加载项功能](./attract-comprehensive-hiring.md)。

## <a name="offer-activity"></a>聘约活动

招聘流程模板需要聘约活动。 若要使用集成的聘约管理应用，请将**在准备聘约上启动聘约管理应用**设置为**开**。 如果此设置为关闭，聘约应用中将不显示应聘者，所以您必须手动跟踪应聘者的聘约活动更新。 若要定义招聘经理是否可在聘约应用中为应聘者准备聘约，请将**招聘经理可以准备聘约**设置为**开**。 如果工作与多个职位关联，可决定是否要为同一个职位编号准备多个聘约。 如果要允许每个工作的每个职位仅允许一个聘约，请将**允许在工作内重复使用职位**设置为**关**。

> [!NOTE]
> 集成的聘约管理应用仅通过综合招聘加载项提供。 有关详细信息，请参阅 [Attract 综合招聘加载项功能](./attract-comprehensive-hiring.md)。


