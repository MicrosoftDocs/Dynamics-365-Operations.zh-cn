---
title: Dynamics 365 Talent 的新增功能或更改（2019 年 7 月 16 日）
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6dce39bc529bf6dd6079ed900af12510c0773f9a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899074"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Dynamics 365 Talent 的新增功能或更改（2019 年 7 月 16 日）

此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改
本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。

### <a name="coming-soon-in-attract"></a>Attract 中即将推出
#### <a name="job-approvals-appear-on-the-home-page"></a>主页中显示工作审核

仪表板的**审核**部分中将显示审核。 审核人可以在**已分配给您**（其中显示工作 ID、工作头衔、其他审核人和作业的分配日期）下查看自己的审核。 提交待审核工作的用户可以在**您请求的**（其中显示仍然必须审核提交的工作的审核者）下查看自己的工作。

## <a name="changes-in-onboard"></a>Onboard 中的更改
本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。

## <a name="changes-in-core-hr"></a>Core HR 中的更改
本部分中的更改适用于内部版本号 8.1.2390。

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>现在支持自定义字段的 Common Data Service 实体

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>无法在经理自助服务中查看目标和审核

本周的更改现在允许在经理自助服务中显示和编辑跨级经理的目标和审核。

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>用户编辑目标字段后，无法关闭目标窗体

此版本更正了选择**关闭**时目标窗体未关闭的问题。

### <a name="creating-new-goals-and-saving-displays-error"></a>创建新目标和保存显示错误

此版本更正了在员工和经理自助服务中保存目标时的问题。

### <a name="unable-to-add-a-field-to-position-details"></a>无法向职位详细信息添加字段 

在此版本中，职位详细信息现在支持自定义字段。
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>无法通过数据管理设置收入代码的到期日期

更改现在允许您在数据管理中设置收入代码的到期日期。

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>新自定义字段同步不够快

本周的发布改进了自定义字段同步到 Common Data Service 的性能。

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>实体导出到数据库作业失败，并显示错误消息：“初始化字符串的格式不符合从索引 0 开始的规范。”

此版本更正了数据库批处理作业失败的问题。 要手动更新：

1. 转到**数据管理**。
2. 选择**配置实体导出到数据库功能**。
3. 在目标数据库中重新输入连接字符串，然后选择**保存**。

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>SMTP 电子邮件配置突然失败，并显示错误消息：“SMTP 服务器需要安全连接或客户端未经过身份验证。”

此版本更正了突然失败的 SMTP 电子邮件配置。 要手动更新：

1. 转到**系统管理**。
2. 选择**电子邮件参数**。
3. 选择 **SMTP 设置**。 
4. 重新输入用于 SMTP 服务器的用户名和密码，然后选择**保存**。

## <a name="in-preview"></a>预览模式

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>只有沙盒实例中才会启用预览功能

配置新的 Talent 实例时，可指定实例类型为**生产**还是**沙盒**。 **沙盒**类型的实例可用于提前测试新功能。 将把所有现有 Talent 实例更新为**生产**实例类型。 如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support)以发起更改请求。

有关如何发布更改的详细信息，请参阅[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。

### <a name="restrict-leave-types-in-time-off-requests"></a>限制请假中的休假类型

组织可以为员工提供多种不同的休假类型。 但是，可能不适合员工提交某些休假类型的请假。 可以改用 HR 管理这些休假类型。 在此版本中，可以配置员工可以提交哪些休假类型的请假。 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>在经理自助服务中查看直接报表和扩展报表的性能信息

经理可通过一个新选项查看直接报表和扩展报表的绩效。 现在，职能经理可以分配和更新绩效目标和颁发新审核。 此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。 实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。
