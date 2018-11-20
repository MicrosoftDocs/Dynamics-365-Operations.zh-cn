---
title: "Attract 中的求职站点功能"
description: "本文提供 Microsoft Dynamics 365 for Talent - Attract 中面向应聘者的求职站点功能的概览。 另外还介绍如何设置此功能。"
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: zh-cn
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Attract 中的求职站点功能

[!include [banner](includes/banner.md)]

本文提供 Microsoft Dynamics 365 for Talent: Attract 中面向应聘者的求职站点功能的概览。 另外还介绍如何设置此功能。

## <a name="overview"></a>概览

Attract 为租户中的每个环境提供一个求职站点。 例如，如果组织具有开发环境和测试环境，一个求职站点为开发环境设置，另一个求职站点为测试环境设置。 各求职站点是**完全隔离**的，并且具有自己的身份验证机制。 工作和应聘者个人资料不在求职站点之间共享。

默认情况下，求职站点是公共的。 因此，应聘者可以查看标记为外部的所有工作，而不必登录。 但是，其他所有操作都需要应聘者登录。

## <a name="career-site-management"></a>求职站点管理

求职站点的以下项目由设置控制：

- **组织名称：** 组织名称显示在求职站点顶部的导航栏中。 通过选择组织名称，应聘者可以转到列出所有空缺职位的页面。
- **组织徽标：** 组织徽标的图像显示在求职站点的左上角。 通过选择徽标图像，应聘者可以转到列出所有空缺职位的页面。

若要设置组织名称和徽标值，作为管理员登录到 Attract，在**设置**菜单（齿轮符号）上选择**管理员中心**，然后选择**公司信息**选项卡。

> [!NOTE]
> 显示在求职站点的徽标图像具有固定高度 20 像素 (px)。 在管理员中心添加的图像会缩放以适应此高度。 因此，根据图像，宽度可能会变化。

## <a name="career-site-url"></a>求职站点 URL

在您首次[发布外部工作](./Creating-jobs-Attract.md#postings)时，您可以从 Attract 应用程序复制**申请**链接。 此链接的 URL 将使用以下格式：`https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

求职站点的 URL 是**申请** URL 的子字符串。 它包含公司名称的所有内容。 因此，对于前面的**申请** URL，求职站点 URL 为 `https://jobs.talent.dynamics.com/jobs/<company_name>/`。

## <a name="authentication-options"></a>身份验证选项

应聘者具有以下 Attract 求职站点登录选项：

- 个人帐户：

    - LinkedIn
    - Microsoft
    - Google
    - Facebook

- 工作或学校帐户：

    - Microsoft Azure Active Directory (Azure AD)

Azure AD 登录仅用于内部应聘者。 因此，它只对使用其公司 Azure AD 凭据的内部应聘者有效。 例如，当前是 Contoso Ltd 员工的应聘者希望申请一家不相关公司 Alpine Ski House 的工作。 在这种情况下，如果员工尝试使用其 Contoso Ltd 的 Azure AD 凭据，登录将不成功。

## <a name="create-and-maintain-a-profile"></a>创建和维护个人资料

在应聘者登录到求职站点后，他们可以在页面顶部的导航栏中选择**我的个人资料**来创建和维护其个人资料。 个人资料包括个人信息、工作经验相关信息、教育详细信息、文档、链接以及技能信息。 个人资料创建后，可用于申请应聘者感兴趣的工作。 个人资料还可以帮助 Attract 向应聘者推荐合适的工作。

## <a name="find-the-right-job"></a>查找合适的工作

在工作列表页，应聘者可以通过输入搜索词搜索特定工作。 搜索功能查找职务和工作描述中的搜索词，然后在结果中显示相关工作。 应聘者可以随时基于工作位置或工作职能筛选结果。

应聘者还可以在求职站点上查看一组推荐的工作。 向应聘者推荐的工作基于应聘者过去的申请、个人资料和简历。

> [!NOTE]
> 仅当求职站点上至少发布了 10 个工作并且应聘者已经完成了个人资料时，工作推荐才会显示。

## <a name="apply-for-jobs"></a>申请工作

应聘者找到合适的工作后，可以使用工作详细信息页面的**申请**按钮进行申请。 此时，应聘者可以创建全新的个人资料或审查现有个人资料的信息。 应聘者还可以根据需要上载简历，然后提交工作申请。

## <a name="check-application-status"></a>检查申请状态

应聘者申请一个或多个工作后，可以在页面顶部的导航栏上选择**申请**来查看其打开和关闭的申请。 在应聘者打开一个申请时，他们将看到当前阶段以及他们必须完成的任何待处理的操作项目。 例如，如果应聘者必须为面对面面试提供潜在日期，页面将显示其选项。

## <a name="internal-jobs"></a>内部工作

目前，标记为内部并发布到 Attract 求职站点的工作不出现在求职站点上。 他们只能通直接的**申请** URL（可以从 Attract 应用程序复制）访问。

