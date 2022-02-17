---
title: Dynamics 365 Talent - Attract 和 Onboard 应用停用
description: 本主题介绍 Dynamics 365 Talent - Attract 和 Onboard 应用的停用。
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: df33f35f66e356c3c2a99f0d81ebba1d0f34b5d9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069396"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract 和 Onboard 应用停用


2019 年 12 月，我们宣布将于 2022 年 2 月 1 日停用 Dynamics 365 Talent - Attract 和 Onboard 应用，为我们的客户提供两年的计划时间。

有关这些应用停用的详细信息，请参阅：
 - [停用 Dynamics 365 Talent - Attract 和 Dynamics 365 Talent: Onboard 应用](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [使用 Dynamics 365 Human Resources 建立更成功的员工队伍](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

我们将继续支持 Dynamics 365 Human Resources，这将帮助我们的客户获得所需的劳动力见解，以在多个领域构建数据驱动的员工体验，如：

- 薪酬
- 福利
- 休假和缺勤
- 合规性
- Payroll
- 绩效反馈
- 培训与认证
- 自助服务项目

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent 应用停用常见问题

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>从 2022 年 2 月 1 日起，Dynamics 365 Talent - Attract 和 Onboard 应用有什么用户体验？

用户将无法使用这些应用程序，将被重定向到停用页面。

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>2022 年 2 月 1 日之后，客户能否继续导出 Dynamics 365 Talent - Attract 和 Onboard 应用的数据？
  
不能，2019 年 12 月已宣布停用，2022 年 2 月 1 日之前已经提供了所需的导出功能。 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>在 2022 年 2 月 1 日之后，与 Dynamics 365 Talent - Attract 和 Onboard 应用相关的客户数据是否会在 Dataverse 中删除？

不会，Dataverse 实体即使在停用后仍将保留在客户的 Microsoft Dataverse 环境中，除非 Human Capital Management Talent 解决方案被删除或卸载。

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>我知道 Talent 环境的名称。 如何在 Dataverse 中查看 Attract 和 Onboard 数据？

1.  登录到 Power Apps：https://make.powerapps.com
2.  选择要查看 Attract 和 Onboard 数据的环境。
3.  转到 **Dataverse > 表**。 
4.  在 **搜索** 中键入“msdyn_”。 如果您看到以“msdyn_”+ 表名称（示例：msdyn_candidate）开头的表列表，说明您已找到具有 Attract 和 Onboard 数据的环境。

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>我不知道 Talent 环境的名称。 如何找到具有 Dynamics 365 Talent: Attract 和 Dynamics 365 Talent: Onboard 应用程序数据的环境？

1)  登录到 Power Platform 管理中心：https://admin.powerplatform.microsoft.com/
2)  选择 **环境**。
3)  选择要评估的特定环境。
4)  选择 **资源 > Dynamics 365 应用**。
5)  如果您看到安装了 **HCM Talent** 解决方案，说明该环境中应该存储有 Attract 和 Onboard 数据。 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> **HCM Talent** 解决方案也用于 Dynamics 365 Human Resources。
