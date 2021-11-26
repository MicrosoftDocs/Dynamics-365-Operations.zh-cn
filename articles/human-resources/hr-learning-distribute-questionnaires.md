---
title: 分发和计划调查表
description: 本主题描述如何分配您设计的调查表，以便它们可供将要完成它们的一个人或一组人使用。
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a13f699c8c0951b32f7826e8cfe8d7dcf02a7f55
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728995"
---
# <a name="distribute-and-schedule-questionnaires"></a>分发和计划调查表

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题描述如何分配您设计的调查表，以便它们可供将要完成它们的一个人或一组人使用。 

有多种方式来分配调查表：

-   将调查表标记为 **有效**。 然后，调查表可用于所有员工，除非设置调查表组来限制对它的访问。
-   向调查表组分配权限。 然后，调查表可供所选组的所有成员使用。
-   创建计划应答期。 然后，调查表只可供特定人员使用。
-   创建计划。 然后，调查表中可供多个人员使用。

## <a name="marking-a-questionnaire-as-active"></a>将调查表标记为有效

通过在 **调查表** 页上将 **有效** 字段设置为 **是**，您使调查表可供所有员工使用并完成。 调查对象可以多次完成调查表。 如果您要全年收集连续反馈，则此功能十分有用。 例如，您可以让员工使用调查表来提供有关在自助服务餐厅享用午餐服务的反馈。

## <a name="questionnaire-groups"></a>调查表组

您可以设置调查表组，然后包括调查表应分配到的调查对象。 

可以从以下页面创建调查表组：

-   **调查表组**– 只有调查表组中的个人可以完成选定的调查表组。 例如，您的预期受众是承包商，因此您可以创建特定于这些调查对象的调查表组。
-   **调查表组成员** – 您可以向调查表组添加人员。

若要将调查表组分配给某一调查表，请在 **调查表** 页上，单击 **用户权限**。 在调查表保存为有效后，调查表组的成员可以完成调查表。 如果您想要先对一组特定的人员测试某一调查表，然后再将其展开到一个更大的组，或者，如果您想要使调查表面向非常具体的受众，则此功能很有用。

## <a name="planned-answer-sessions-in-a-questionnaire"></a>调查表中的计划应答期

计划应答期是您设计并选择调查对象的调查表。 

> [!NOTE]
> 在您可以设置计划应答期之前，必须设计调查表。 

在 **计划应答期** 页上，您可为单独的员工创建计划应答期。 该页面上的列表显示所有已编制的调查表。 

计划应答期还用于 **调查表计划** 页上，在那里您可以为多人计划调查表：

-   员工
-   课程参与者
-   组织单位

每个人只能回答调查表一次。

## <a name="scheduling-a-questionnaire"></a>计划调查表

（可选）您可以为多个调查对象计划调查表。

### <a name="planning-types"></a>计划类型

如果您想要为多个调查对象安排计划的回答会话，则需要计划类型。 计划类型用于对调查表计划分类。 例如，您可能会出于以下目的计划调查表：

-   评估
-   调查
-   正在测试

您可以在 **调查表计划** 页上为调查表计划指定计划类型。

### <a name="reference-types-for-questionnaire"></a>调查表的参考类型

您可以使用参考类型输入您可以在计划调查表时选择的回应者的条件。 

使用 **参考类型** 页可以设置调查表的参考类型。 每个参考类型对应于 Microsoft Dynamics 365 Finance 中的某个表。 在您创建调查表计划时，可以指定表中记录或指定调查表将关联的一系列记录。 

例如，如果您选择“课程”表，您可以确定调查表将针对哪一个特定课程。 在您为“课程”表设置参考时，**课程** 页上的某些字段和按钮将可用。

### <a name="questionnaire-schedules"></a>调查表计划

您可以使用调查表计划基于参考类型为一组用户生成多个计划应答期。 在 **调查表计划** 页上创建计划。 选择计划类型对计划进行分类，并且选择应用于在系统中查询特定用户的参考类型。 例如，如果您将参考类型设置为“课程”表，则您可以在 **参考** 字段中选择特定课程。 

单击 **设置详细信息** 可以选择调查表和其他条件。 例如，如果调查表是对教师的评估，则指定教师的名称作为条件。 在您完成输入设置详细信息后，系统将为查询中包括的用户生成计划应答期。 

单击 **计划应答期** 可以查看计划的应答期。 然后，您可以手动创建附加计划应答期或删除尚未回答的计划应答期。 

单击 **功能** &gt; **开始** 可以使计划调查表在相关计划应答期中可供用户使用。 单击 **回答** 可以查看该调查表的已完成响应。 （可选）您可以复制调查表计划设置、计划应答期和对新计划调查表的回答。

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>告知调查对象调查表对其可用
在分发调查表时，您必须通知调查对象调查表对其可用。 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>向调查对象通知计划应答期

如果您使用计划应答期，您必须直接通知人员，例如通过电话或电子邮件地址。

### <a name="notifying-respondents-about-a-scheduling"></a>向调查对象通知相关计划

使用 **调查表计划** 页可以准备电子邮件并将其发送给分配有调查表的调查对象。 在 **员工自助服务的电子邮件** 选项卡上输入电子邮件文本。在计划开始后，单击 **功能** &gt; **发送电子邮件** 以生成电子邮件并将其发送给调查对象。 然后调查对象可以登录到该网站并完成调查表。 

> [!NOTE]
> 在您可以使用电子邮件功能之前，您的 IT 管理员必须在 **电子邮件参数** 页上输入电子邮件设置。

## <a name="ending-a-scheduled-questionnaire"></a>结束预定的调查表

您可以在所有回应者都已完成他们的分配的应答期后，结束计划的调查表。 在结束后某一计划的调查表，您不能将其设置为新计划编制。 

> [!NOTE]
>   如果一个或多个调查对象尚未完成调查表并且您仍要结束计划编制，则首先在 **计划应答期** 页上的列表中删除这些调查对象。 然后，即可结束计划。

## <a name="completing-questionnaires"></a>填写调查表

在您设计并分配某一调查表后，该调查表可由所选调查对象完成。 您可以从以下两个位置完成可供您使用的调查表：

-   在导航窗格中，单击 **调查表** &gt; **分配** &gt; **填写调查表**。
-   在员工自助服务中，单击 **要完成的调查表**。

调查表可用于网络中的所有人士，或者可用于特定的用户组或所有用户。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
