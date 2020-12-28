---
title: Dynamics 365 Talent（2019 年 3 月 20 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a7a44e1c9d8dcb4b2cc81a682a044d26cdc1149e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460437"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-20-2019"></a>Dynamics 365 Talent（2019 年 3 月 20 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改

### <a name="setting-the-audience-on-activities"></a>为活动设置受众
现在可以为系统中的活动设置受众。 现在可以为所有应聘者、内部应聘者和外部应聘者设置与流程有关的活动（如面试、计划、反馈和 EEO）。 可以将自定义活动（如 Microsoft 窗体、YouTube 视频和 Web 内容）交付给所有应聘者、内部应聘者、外部应聘者或招聘团队。  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>改进求职站点工作发现能力：搜索引擎优化
搜索引擎爬网程序可通过此功能访问 Attract 求职站点上的工作发布并为其建立索引。 这样应聘者就可以使用常见的搜索引擎找到 Attract 求职站点上发布的工作。

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>向忘记了凭证的应聘者显示登录提示
如果应聘者在打开保存的链接或通过电子邮件收到的链接时忘记了用于申请工作的社交凭证，现在可以看到包含提供商名称和用户名（容易混淆）的提示。 这样就可以帮助他们使用正确的凭证访问自己的工作申请。

### <a name="help-internal-candidates-explore-internal-jobs"></a>帮助内部应聘者浏览内部工作
已修复了一个问题，这个问题是外部应聘者可以看到工作的招聘人员或招聘经理的姓名。 现在只有内部应聘者可以看到工作的招聘团队成员。 内部应聘者还可以更轻松地查看和申请仅限内部的工作。 当应聘者尝试访问链接以查看或申请仅限内部的工作时，将强制其使用 Azure Active Directory 凭证进行身份验证。 内部应聘者还可以联系招聘团队成员以表明对工作感兴趣或了解该工作的更多信息。 这项功能适用于仅对内部应聘者开放的所有工作。 有关详细信息，请参阅[在 Microsoft Dynamics 365 Talent - Attract 中设置求职站点](./career-site.md)。

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>指定银奖获得者以便为将来的职位指定高价值应聘者。
招聘人员和招聘经理通常会保留非常适合职位，但是由于该职位的人员已满而不能为其提供聘约的申请人的流动轮候名单。 此类申请人称为银奖获得者，他们非常宝贵，因为可以在下次开放类似职位时帮助缩短招聘时间。 Attract 现在允许招聘人员和招聘经理指定申请人列表中的银奖获得者，以便此类申请人提前进入聘约阶段。 银奖获得者指定信息不但会出现在工作的申请人列表中，还会出现在人才池视图，前提是此类申请人是招聘人员或招聘经理的任何人才池的成员。 此外，指定信息还会出现在工作历史记录中，后者是应聘者的人才池个人资料。 您可以通过请管理员使用[管理中心中的功能管理](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)开启此功能来预览此功能。

### <a name="add-applicants-to-talent-pools"></a>向人才池添加申请人
现在可以通过在申请人列表中显示新操作更轻松地向人才池添加申请人。 招聘人员或招聘经理可以通过选择 **添加到人才池** 图标在自己的人才池列表中进行选择，并且直接从工作的申请人列表向人才池添加申请人。

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>配置是否需要简历才能申请特定工作
根据客户反馈，招聘人员现在可以配置在申请特定工作时是否需要简历（上传的文件形式）。 此项设置属于申请活动，可以在招聘流程中访问。 启用后，将提示所有潜在申请人在申请此职位时上传简历。 除非上传了简历，否则不会将申请视为已完成。 这通过确保每位申请人提供足够的信息来让招聘人员为他们分门别类，从而帮助减少人才池中的干扰。

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>应聘者可以使用自己的 LinkedIn 个人资料申请工作
已经在 LinkedIn 中准备好了经过更新的最新个人资料的应聘者通过单击一次即可使用该个人资料申请工作。

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>跟踪应聘者的个人资料最初通过什么样的途径出现在系统中，以及申请人是在哪里发现所申请的工作的
现在可以通过查看申请人的 **个人资料** 页面上应聘者详细信息下的个人资料来源或人才池个人资料来了解特定应聘者的个人资料最初通过什么样的途径出现在 Attract。 同样，可以通过查看应用程序活动订阅源中 **申请活动** 内提供的申请人来源来了解任何申请人是如何发现工作的。 人才池个人资料中的工作历史记录内也提供这些信息。 招聘人员或招聘经理手动添加应聘者时，将提示他们指定申请表或申请人个人资料的来源。 当应聘者首次申请时，其个人资料来源将与其申请来源相同。 您可以通过请管理员使用[管理中心中的功能管理](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)开启此功能来预览此功能。 请注意，现有应聘者和申请人没有任何来源信息。 但是，招聘人员可以手动添加这些信息。

## <a name="changes-in-onboard"></a>Onboard 中的更改

本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改

本部分中的更改适用于内部版本号 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attract 集成为申请表引发重复记录错误
在此更新中，已修复了重复记录问题。 此问题是在 **个人管理** 工作区中出现的。

### <a name="unable-to-close-form-when-editing-name-sequence"></a>编辑名称序列时无法关闭窗体
已进行了更改，更正了在工作人员窗体中编辑名称序列时的问题。

## <a name="coming-soon"></a>即将到期

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高级薪酬安全（固定和可变）
在许多组织中，薪酬和福利经理可能只能访问特定薪酬记录。 这些记录可能是有关管理层或地区员工的记录。 通过此更改，HR 可以管理和维护组织中不同员工组的薪酬计划。 您可以为固定计划和可变计划分配安全角色，用于决定这些计划和与其有关的员工数据（例如，工资和奖金记录）的访问权限。 只有授予了访问权限的角色才能处理这些员工的薪酬。

###  <a name="email-support-for-alerts"></a>警报的电子邮件支持
安装 Finance and Operations 平台更新 24 之后，用户可创建警报规则，用于在被事件触发后自动向联系人派遣电子邮件通知。

### <a name="duplicate-employee-check-interface-changes"></a>重复员工检查：界面更改
借助此更改，输入名称字段时可检测重复项，而状态将显示找到的重复项数量。 您可以选择提供的链接以打开一个新的页面来评估是否要使用检测到的匹配项。 重复项窗体不会自动打开，以免中断数据输入。


