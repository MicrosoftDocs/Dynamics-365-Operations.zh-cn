---
title: Attract 中的求职站点功能
description: 本主题概述 Attract 中面向应聘者的求职站点功能。
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/13/2019
ms.locfileid: "389950"
---
# <a name="career-site-functionality-in-attract"></a>Attract 中的求职站点功能

[!include[banner](../includes/banner.md)]

本主题概述 Microsoft Dynamics 365 for Talent: Attract 中面向应聘者的求职站点功能。 另外还介绍如何设置此功能。

Attract 为租户中的每个环境提供一个求职站点。 例如，如果组织具有开发环境和测试环境，一个求职站点为开发环境设置，另一个求职站点为测试环境设置。 各求职站点是完全隔离的，并且具有自己的身份验证机制。 工作和应聘者个人资料不在求职站点之间共享。

默认情况下，求职站点是公共的。 因此，应聘者可以查看标记为外部的所有工作，而不必登录。 但是，其他所有操作都需要应聘者登录。

## <a name="career-site-management"></a>求职站点管理

若要设置以下项，作为管理员登录到 Attract，在**设置**菜单（齿轮符号）上选择**管理员中心**，然后选择**公司信息**选项卡。

-   **组织名称** - 组织名称显示在求职站点顶部的导航栏中。 通过选择组织名称，应聘者可以转到列出所有空缺职位的页面。

-   **组织徽标** - 组织徽标的图像显示在求职站点的左上角。 通过选择徽标图像，应聘者可以转到列出所有空缺职位的页面。

    >   [!NOTE] 
    >   显示在求职站点的徽标图像具有固定高度 20 像素 (px)。 在管理员中心添加的图像会缩放以适应此高度。 因此，根据图像，宽度可能会变化。
 
若要设置以下项，作为管理员登录到 Attract，在**设置**菜单上选择**管理员中心**，然后选择**求职站点管理**选项卡。

-   **搜索引擎优化** - 如果启用，可使用 Bing 和 Google 之类搜索引擎搜索 Attract 求职站点中发布的所有公开职位。

    >   [!NOTE] 
    >   开启此设置到搜索结果显示之间可能存在延迟，具体取决于所用搜索引擎。
         
## <a name="career-site-urls"></a>求职站点 URL

以下列表中包含常用求职站点 URL 及其访问方法。

-   **求职站点主页 URL** - 若要查看求职站点主页 URL，请以管理员身份登录 Attract，选择**设置**菜单中的**管理员中心**，然后选择**求职站点管理**选项卡。

-   **单个工作发布申请 URL** - 在您首次[发布外部工作](Creating-jobs-Attract.md#postings)时，您可以从 Attract 应用程序复制**申请**链接。 此链接的 URL 将使用以下格式：[https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **单个工作发布 URL** - 充当“申请 URL”的子字符串的工作发布 URL。 它包含工作编号的所有内容。 因此，对于前面的申请 URL，工作发布 URL 为 [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)。

## <a name="authentication-options"></a>身份验证选项

应聘者具有以下 Attract 求职站点登录选项：

-   个人帐户：

    -   LinkedIn

    -   Microsoft

    -   Google

    -   Facebook

-   工作或学校帐户：

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD 登录仅用于内部应聘者。 因此，它只对使用其公司 Azure AD 凭据的内部应聘者有效。 例如，当前是 Contoso Ltd 员工的应聘者希望申请一家不相关公司 Alpine Ski House 的工作。 在这种情况下，如果员工尝试使用 Contoso Ltd 的 Azure AD 凭据，登录将不成功。

## <a name="create-and-maintain-a-profile"></a>创建和维护个人资料

在应聘者登录到求职站点后，他们可以在页面顶部的导航栏中选择**我的个人资料**来创建和维护其个人资料。
个人资料包括个人信息、工作经验相关信息、教育详细信息、文档、链接以及技能信息。 个人资料创建后，可用于申请应聘者感兴趣的工作。 个人资料还可以帮助 Attract 向应聘者推荐合适的工作。

>   [!NOTE]
>   如果应聘者使用电子邮件 ID 和上面列举的一个身份验证提供商登录，该电子邮件 ID 默认为与个人资料关联的联系人电子邮件 ID。 但是，后者随时可更改，完全独立于前者。 Attract 将始终使用联系人电子邮件 ID 与您的个人资料关联来进行所有电子邮件通信。

## <a name="find-the-right-job"></a>查找合适的工作

在工作列表页，应聘者可以通过输入搜索词搜索特定工作。 搜索功能查找职务和工作描述中的搜索词，然后在结果中显示相关工作。 应聘者可以随时基于工作位置或工作职能筛选结果。

应聘者还可以在求职站点上查看一组推荐的工作。 向应聘者推荐的工作基于应聘者过去的申请、个人资料和简历。

>   [!NOTE] 
>   仅当求职站点上至少发布了 10 个工作并且应聘者已经完成了个人资料时，工作推荐才会显示。

## <a name="apply-for-jobs"></a>申请工作

应聘者找到合适的工作后，可以使用**工作详细信息**页面的**申请**按钮进行申请。 此时，应聘者可以创建新的个人资料或审查现有个人资料的信息。
应聘者还可以根据需要上载简历，然后提交工作申请。

## <a name="check-application-status"></a>检查申请状态

应聘者申请一个或多个工作后，可以在页面顶部的导航栏上选择**申请**来查看其打开和关闭的申请。 在应聘者打开一个申请时，他们将看到当前阶段以及他们必须完成的任何待处理的操作项目。 例如，如果应聘者必须为面对面面试提供潜在日期，页面将显示可用选项。

## <a name="internal-jobs"></a>内部工作

目前，标记为内部并发布到 Attract 求职站点的工作不出现在求职站点上。 只能使用直接的**申请** URL（可以从 Attract 应用程序复制）访问这些工作。
