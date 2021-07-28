---
title: 申请人跟踪系统集成 API 简介
description: 本主题介绍 Dynamics 365 Human Resources 申请人跟踪系统 (ATS) 集成 API。
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5038a1a1b3fa4c32f54ea87b03f886504e0b004f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357380"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>申请人跟踪系统集成 API 简介

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 申请人跟踪系统 (ATS) 集成 API。 此 API 的目的是在 Dynamics 365 Human Resources 和合作的 ATS 之间实现简化的集成。

![ATS 集成流。](media/hr-admin-integration-ats-api-introduction-flow.png)

当招聘经理创建招聘请求时，集成体验便在 Human Resources 中开始。 激活请求后，ATS 会提取请求的详细信息来创建招聘项目。 然后，它跟随招聘管道为职位选择和雇用应聘者。 最后，ATS 通过将所选应聘者记录发送到 Human Resources 来完成往返集成。 然后，应聘者记录可以经过更多的入职验证和工作流来创建员工记录。

为了支持集成，Human Resources 添加了以下组件：

1.  创建招聘请求的功能。
2.  扩展的应聘者个人资料和相关工作流。
3.  为集成应用程序开启新功能的集成 API。

有关设置和使用招聘请求和应聘者功能的详细信息，请参阅[招聘工作应聘者](hr-personnel-recruit.md)。

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

此 API 基于 Microsoft Dataverse（以前称为 Common Data Service）构建。 与此 API 的所有 RESTful 交互都通过使用 OData 的 Microsoft Dataverse Web API 完成。 此 API 是 Dataverse Web API 的子集。 Dataverse Web API 定义诸如身份验证、SLA、批处理、并发控制和错误处理等特征。

有关 Microsoft Dataverse Web API 的更多一般信息，请参阅：

- [什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)
- [使用 Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse 开发人员指南](/powerapps/developer/data-platform)

以上文档包括有关使用 Dataverse Web API 的详细信息和开发人员指南，如[管理身份验证](/powerapps/developer/data-platform/webapi/authenticate-web-api)、[执行操作](/powerapps/developer/data-platform/webapi/perform-operations-web-api)、[通过 API 使用 Postman](/powerapps/developer/data-platform/webapi/use-postman-web-api) 以及通过 API [使用更改跟踪或增量令牌](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)。

### <a name="option-sets"></a>选项集

本文所述的 ATS 集成 API 的数据模型包括提供与实体属性关联的枚举值的选项集。 有关在 Dataverse Web API 中使用选项集的详细信息，请参阅[使用 Web API 创建和更新选项集](/powerapps/developer/data-platform/webapi/create-update-optionsets)。 选项集将为每个 Dataverse 环境定义。

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Dataverse 中适用于 Human Resources 的虚拟表

ATS 集成 API 的终结点使用 Microsoft Dataverse 的虚拟表平台功能。 默认情况下，虚拟表及其关联的 API 终结点不针对 Human Resources 环境部署，以让组织可以确定哪些 OData 终结点将为环境公开。 要使用 API，必须为环境生成适用于 Human Resources 实体的虚拟表。 

有关为 API 生成虚拟表的信息，请参阅[配置 Dataverse 虚拟表](./hr-admin-integration-common-data-service-virtual-entities.md)。

## <a name="data-model"></a>数据模型

数据模型以两个主要实体为中心：

- **RecruitingRequest** 表示向 ATS 发出的为一个或多个空缺职位招聘的请求。示例查询请参阅[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)。
- **CandidateToHire** 表示接受职位聘约的应聘者的详细信息。 **人员** 表示作为应聘者的个人。 一名人员可以在公司中有多个角色，如应聘者、工作人员、员工或合同工。 示例查询请参阅[“可雇用的应聘者”的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)。

下图说明了 API 中的关系。 若干个类型具有 Human Resources 中其他预先存在的实体的外键，这里没有说明。 本文档提供有关特定于招聘集成场景的实体的信息。 但是，适用于 Dynamics 365 Human Resources 的 Dataverse Web API 中还有很多其他实体也可能与您的集成相关。 例如，您可能还需要工作人员、工作、职位或此处未定义的其他实体的详细信息。 这些实体中有很多在外键关系或导航属性中引用。

![ATS 集成 API 数据模型。](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>招聘请求以及相关实体和选项集

示例查询： 

- [招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)

实体:

- [招聘请求](hr-admin-integration-ats-api-recruiting-request.md)
- [招聘请求职位](hr-admin-integration-ats-api-recruiting-request-position.md)
- [招聘请求技能](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [招聘请求教育](hr-admin-integration-ats-api-recruiting-request-education.md)
- [招聘请求位置](hr-admin-integration-ats-api-recruiting-request-location.md)

选项集：

- [工作免除情况](hr-admin-integration-ats-api-job-exempt-status.md)
- [招聘请求职位状态](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [招聘请求状态](hr-admin-integration-ats-api-recruiting-request-status.md)
- [监管工作类别](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>可雇用的应聘者及相关实体和选项集

示例查询：

- [可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

实体:

- [可雇用的应聘者](hr-admin-integration-ats-api-candidate-to-hire.md)
- [人员](hr-admin-integration-ats-api-person.md)
- [人员教育](hr-admin-integration-ats-api-person-education.md)
- [人员专业经验](hr-admin-integration-ats-api-person-professional-experience.md)
- [人员地址](hr-admin-integration-ats-api-person-address.md)
- [当事方联系人](hr-admin-integration-ats-api-party-contact.md)
- [人员技能](hr-admin-integration-ats-api-person-skill.md)
- [评级级别](hr-admin-integration-ats-api-rating-level.md)
- [人员证书](hr-admin-integration-ats-api-person-certificate.md)
- [证书类型](hr-admin-integration-ats-api-certificate-type.md)
- [人员筛选](hr-admin-integration-ats-api-person-screening.md)
- [筛选类型](hr-admin-integration-ats-api-screening-types.md)
- [人员标识号](hr-admin-integration-ats-api-person-identification-number.md)

选项集：

- [申请人集成结果](hr-admin-integration-ats-api-applicant-integration-result.md)
- [空白/是/否](hr-admin-integration-ats-api-blank-yes-no.md)
- [完成状态](hr-admin-integration-ats-api-completion-status.md)
- [联系人类型](hr-admin-integration-ats-api-contact-type.md)
- [教育信用基础](hr-admin-integration-ats-api-education-credit-basis.md)
- [性](hr-admin-integration-ats-api-gender.md)
- [婚姻状况](hr-admin-integration-ats-api-marital-status.md)
- [一年中的月份](hr-admin-integration-ats-api-months-of-year.md)
- [否/是](hr-admin-integration-ats-api-no-yes.md)
- [期间单位](hr-admin-integration-ats-api-period-unit.md)
- [筛选频率](hr-admin-integration-ats-api-screening-frequency.md)
- [筛选频率生成来源](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [技能级别类型](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>请参阅

[招聘工作应聘者](hr-personnel-recruit.md)<br>
[什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)<br>
[使用 Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>
[使用 Web API 创建和更新选项集](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]