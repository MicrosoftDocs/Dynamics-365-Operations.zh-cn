---
title: Attract 的可扩展性
description: 此主题介绍如何使用 Microsoft Power 平台扩展 Microsoft Dynamics 365 for Talent - Attract 应用程序。
author: josaw
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c77c64070cb82180441f4b629b6884981b9b81d2
ms.sourcegitcommit: 0bd0215d0735ed47b1b8af93a80bcdbf7ca2cc49
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/08/2019
ms.locfileid: "789643"
---
# <a name="extensibility-in-attract"></a>Attract 的可扩展性

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent 在 Common Data Service (CDS) for Apps 平台基础上构建，可以使用 Microsoft Power 平台和 Common Data Service for Apps 提供的功能以各种方式扩展。 因此，您可以使用 Microsoft PowerApps 和 Microsoft Flow 来配置和个性化系统。 还可以使用 Microsoft Power BI 获取有关人员的附加分析。 此外，PowerApps 和 Web 内容 (iframe) 活动等新的自定义活动让招聘流程的适应性比以往更强。 通过使用这些活动，您可以针对您的业务需要和流程来定制招聘流程，并且可以确保招聘团队和应聘者具有无缝的自定义体验。

## <a name="extending-option-sets-in-attract"></a>扩展 Attract 中的选项集

**选项集**（选择列表）是实体中可包含的一种字段。 用于定义一组选项。 选项集在窗体中显示时，使用下拉列表控件。  在 Attract 中，有多个字段是选项集。  下面介绍的功能用于扩展选项集，从拒绝原因字段、雇佣类型字段和任职类型字段开始。   还可以为添加的选项添加本地化的显示标签。  有关详细信息，请参阅以下链接：[自定义选项集标签](https://docs.microsoft.com/en-us/poweapps/developer/common-data-service/customize-labels-suport-multiple-languages)

> [!NOTE]
> 工作发布到 LinkedIn 这一功能要求使用**工作详细信息**页中的**雇佣类型**和**任职类型**字段。 这些字段中的默认值受 LinkedIn 支持，将在发布工作时显示。 因此，如果要将工作发布到 LinkedIn，并且修改这些字段的现有选项集值，仍将发布工作，但是 LinkedIn 不会显示自定义的**雇佣类型**和**任职类型**值。  

下面列出了用于使用特定于您的业务的值更新**拒绝原因**字段的步骤。  

1. 若要扩展**拒绝原因** 选项集，请导航到 [PowerApps 管理员网站](Https://admin.powerapps.microsoft.com)。
2. 可能会提示您登录您的帐户。 提供用于登录 Dynamics 365 和/或 Office 365 的用户 ID 和密码凭证，然后单击**下一步**。
3. 在**环境**选项卡中，选择要管理的环境，然后双击以访问**详细信息**选项卡。
4. 在**详细信息**选项卡中，选择 **Dynamics 365 管理中心**。
5. 选择要修改的实例，然后选择**打开**。
6. 导航到**设置**，然后导航到**自定义项**，再选择**自定义系统**。
7. 通过选择**实体**并展开组，找到要为其扩展选项集的实体。 本示例中为**工作申请实体**。
8. 通过选择**字段**选项转至要为其扩展选项集的字段。 本示例中为 **msdyn_rejectionreason**。 双击该字段。
9. 在**选项集**字段中，选择**编辑**。
10. 选择 **+** 图标。
11. 输入一个**标签**。  （此值必须为唯一值 – 不得有重复项）。
12. 选择**保存**。
13. 选择页面顶部的**发布**。

## <a name="take-advantage-of-the-microsoft-power-platform"></a>利用 Microsoft Power Platform 

由于 Attract 的所有数据均位于 Common Data Service for Apps 中，您可以使用 Microsoft Power 平台的工具来将您的独特业务需求合并到 Attract 中。

### <a name="powerapps"></a>PowerApps

您可以使用 PowerApps 轻松构建与您的 Attract 数据连接并且使用如 Microsoft Excel 中的表达式添加逻辑的应用。 您使用 PowerApps 构建的应用可以在 Web 上以及 Apple iOS 和 Google Android 设备上运行。

例如，您可以构建让其在 Attract 中扫描简历并向应聘者发送职位的轻型应用，从而让招聘人员更加轻松地应对大学招聘会。 或者，您可以构建帮助您的组织达到合规要求的应用。 有关 PowerApps 以及如何用它来构建应用的更多信息，请参阅[将数据集成到 Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps)。

### <a name="microsoft-flow"></a>Microsoft Flow 

您可以使用 Microsoft Flow 创建在 Attract 数据基础上运行的自动化工作流。 您可以轻松连接到成百上千个热闹应用和服务，而不必编写代码。 通过在 Common Data Service for Apps 中构建与 Attract 工作、应聘者和申请实体交互的流，您可以自动执行各种操作。 例如，当应聘者接受聘约时，可以向入职团队发送通知，或可以在 Twitter 上公布新闻。 有关流的详细信息，请参阅 [Microsoft Flow 文档](https://docs.microsoft.com/en-us/flow/)。

### <a name="power-bi"></a>Power BI

Power BI 让您可以建立并查看让您更深入地了解 Attract 数据的自定义报表和仪表板。 有关 Power BI 以及如何建立交互式报表和仪表板的更多信息，请参阅 [Power BI 文档](https://docs.microsoft.com/en-us/power-bi/)。

### <a name="custom-activities"></a>自定义活动 

您可以在工作流程模板或在创建新工作时添加自定义活动，例如 PowerApps 应用和 Web 内容 (iframe) 活动。 这些活动让您可以自定义招聘流程，并将特定于您的组织的业务逻辑带入 Attract。

#### <a name="powerapps-activity"></a>PowerApps 活动 

PowerApps 活动允许工业或工作流程模板的创建者在招聘流程中嵌入 PowerApps 应用。 在创建和发布应用后，您可以在活动配置中输入其应用 ID。 通过使用 PowerApps 应用，您可以在 Common Data Service for Apps 中读取和写入数据。 您甚至可以将应用链接到流。 例如，您有一个招聘人员用来在进行电话面试时填写表单的应用。 在这种情况下，您可以将应用链接到评估申请可否在工作申请流程中继续推进的流。 此类活动只能由招聘团队的成员查看。 有关如何配置 PowerApps 活动的详细信息，请参阅 [Attract 中的活动](./activities-attract.md)。

> [!NOTE]
> PowerApps 活动仅通过综合招聘附件提供。

#### <a name="web-content-iframe-activity"></a>Web 内容 (iframe) 活动

Web 内容 (iframe) 活动允许您嵌入在招聘流程或应聘者门户构建的自定义 Web 解决方案。 您可以直接从 Common Data Service for Apps 读取和写入数据。 还可以自定义解决方案，以使它触发流或利用 Microsoft Azure 功能。 有关如何配置 Web 内容活动的详细信息，请参阅 [Attract 中的活动](./activities-attract.md)。

> [!NOTE]
> Web 内容活动仅通过综合招聘附件提供。
