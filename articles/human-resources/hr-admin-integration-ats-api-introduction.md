---
title: 申请人跟踪系统集成 API 简介
description: 本主题介绍 Dynamics 365 Human Resources 申请人跟踪系统 (ATS) 集成 API。
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c043ac9c19a810d1718f0d4907cd5e9d651d778f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055284"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="deaad-103">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="deaad-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="deaad-104">本主题介绍 Dynamics 365 Human Resources 申请人跟踪系统 (ATS) 集成 API。</span><span class="sxs-lookup"><span data-stu-id="deaad-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="deaad-105">此 API 的目的是在 Dynamics 365 Human Resources 和合作的 ATS 之间实现简化的集成。</span><span class="sxs-lookup"><span data-stu-id="deaad-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS 集成流](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="deaad-107">当招聘经理创建招聘请求时，集成体验便在 Human Resources 中开始。</span><span class="sxs-lookup"><span data-stu-id="deaad-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="deaad-108">激活请求后，ATS 会提取请求的详细信息来创建招聘项目。</span><span class="sxs-lookup"><span data-stu-id="deaad-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="deaad-109">然后，它跟随招聘管道为职位选择和雇用应聘者。</span><span class="sxs-lookup"><span data-stu-id="deaad-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="deaad-110">最后，ATS 通过将所选应聘者记录发送到 Human Resources 来完成往返集成。</span><span class="sxs-lookup"><span data-stu-id="deaad-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="deaad-111">然后，应聘者记录可以经过更多的入职验证和工作流来创建员工记录。</span><span class="sxs-lookup"><span data-stu-id="deaad-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="deaad-112">为了支持集成，Human Resources 添加了以下组件：</span><span class="sxs-lookup"><span data-stu-id="deaad-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="deaad-113">创建招聘请求的功能。</span><span class="sxs-lookup"><span data-stu-id="deaad-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="deaad-114">扩展的应聘者个人资料和相关工作流。</span><span class="sxs-lookup"><span data-stu-id="deaad-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="deaad-115">为集成应用程序开启新功能的集成 API。</span><span class="sxs-lookup"><span data-stu-id="deaad-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="deaad-116">有关设置和使用招聘请求和应聘者功能的详细信息，请参阅[招聘工作应聘者](hr-personnel-recruit.md)。</span><span class="sxs-lookup"><span data-stu-id="deaad-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="deaad-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="deaad-117">Microsoft Dataverse</span></span>

<span data-ttu-id="deaad-118">此 API 基于 Microsoft Dataverse（以前称为 Common Data Service）构建。</span><span class="sxs-lookup"><span data-stu-id="deaad-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="deaad-119">与此 API 的所有 RESTful 交互都通过使用 OData 的 Microsoft Dataverse Web API 完成。</span><span class="sxs-lookup"><span data-stu-id="deaad-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="deaad-120">此 API 是 Dataverse Web API 的子集。</span><span class="sxs-lookup"><span data-stu-id="deaad-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="deaad-121">Dataverse Web API 定义诸如身份验证、SLA、批处理、并发控制和错误处理等特征。</span><span class="sxs-lookup"><span data-stu-id="deaad-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="deaad-122">有关 Microsoft Dataverse Web API 的更多一般信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="deaad-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="deaad-123">什么是 Microsoft Dataverse？</span><span class="sxs-lookup"><span data-stu-id="deaad-123">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="deaad-124">使用 Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="deaad-124">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="deaad-125">Microsoft Dataverse 开发人员指南</span><span class="sxs-lookup"><span data-stu-id="deaad-125">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="deaad-126">以上文档包括有关使用 Dataverse Web API 的详细信息和开发人员指南，如[管理身份验证](/powerapps/developer/data-platform/webapi/authenticate-web-api)、[执行操作](/powerapps/developer/data-platform/webapi/perform-operations-web-api)、[通过 API 使用 Postman](/powerapps/developer/data-platform/webapi/use-postman-web-api) 以及通过 API [使用更改跟踪或增量令牌](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)。</span><span class="sxs-lookup"><span data-stu-id="deaad-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="deaad-127">选项集</span><span class="sxs-lookup"><span data-stu-id="deaad-127">Option sets</span></span>

<span data-ttu-id="deaad-128">本文所述的 ATS 集成 API 的数据模型包括提供与实体属性关联的枚举值的选项集。</span><span class="sxs-lookup"><span data-stu-id="deaad-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="deaad-129">有关在 Dataverse Web API 中使用选项集的详细信息，请参阅[使用 Web API 创建和更新选项集](/powerapps/developer/data-platform/webapi/create-update-optionsets)。</span><span class="sxs-lookup"><span data-stu-id="deaad-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="deaad-130">选项集将为每个 Dataverse 环境定义。</span><span class="sxs-lookup"><span data-stu-id="deaad-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="deaad-131">Dataverse 中适用于 Human Resources 的虚拟表</span><span class="sxs-lookup"><span data-stu-id="deaad-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="deaad-132">ATS 集成 API 的终结点使用 Microsoft Dataverse 的虚拟表平台功能。</span><span class="sxs-lookup"><span data-stu-id="deaad-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="deaad-133">默认情况下，虚拟表及其关联的 API 终结点不针对 Human Resources 环境部署，以让组织可以确定哪些 OData 终结点将为环境公开。</span><span class="sxs-lookup"><span data-stu-id="deaad-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="deaad-134">要使用 API，必须为环境生成适用于 Human Resources 实体的虚拟表。</span><span class="sxs-lookup"><span data-stu-id="deaad-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="deaad-135">有关为 API 生成虚拟表的信息，请参阅[配置 Dataverse 虚拟表](./hr-admin-integration-common-data-service-virtual-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="deaad-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="deaad-136">数据模型</span><span class="sxs-lookup"><span data-stu-id="deaad-136">Data model</span></span>

<span data-ttu-id="deaad-137">数据模型以两个主要实体为中心：</span><span class="sxs-lookup"><span data-stu-id="deaad-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="deaad-138">**RecruitingRequest** 表示向 ATS 发出的为一个或多个空缺职位招聘的请求。示例查询请参阅[招聘请求的查询示例](hr-admin-integration-ats-api-recruiting-request-example-query.md)。</span><span class="sxs-lookup"><span data-stu-id="deaad-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="deaad-139">**CandidateToHire** 表示接受职位聘约的应聘者的详细信息。</span><span class="sxs-lookup"><span data-stu-id="deaad-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="deaad-140">**人员** 表示作为应聘者的个人。</span><span class="sxs-lookup"><span data-stu-id="deaad-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="deaad-141">一名人员可以在公司中有多个角色，如应聘者、工作人员、员工或合同工。</span><span class="sxs-lookup"><span data-stu-id="deaad-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="deaad-142">示例查询请参阅[“可雇用的应聘者”的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)。</span><span class="sxs-lookup"><span data-stu-id="deaad-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="deaad-143">下图说明了 API 中的关系。</span><span class="sxs-lookup"><span data-stu-id="deaad-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="deaad-144">若干个类型具有 Human Resources 中其他预先存在的实体的外键，这里没有说明。</span><span class="sxs-lookup"><span data-stu-id="deaad-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="deaad-145">本文档提供有关特定于招聘集成场景的实体的信息。</span><span class="sxs-lookup"><span data-stu-id="deaad-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="deaad-146">但是，适用于 Dynamics 365 Human Resources 的 Dataverse Web API 中还有很多其他实体也可能与您的集成相关。</span><span class="sxs-lookup"><span data-stu-id="deaad-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="deaad-147">例如，您可能还需要工作人员、工作、职位或此处未定义的其他实体的详细信息。</span><span class="sxs-lookup"><span data-stu-id="deaad-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="deaad-148">这些实体中有很多在外键关系或导航属性中引用。</span><span class="sxs-lookup"><span data-stu-id="deaad-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS 集成 API 数据模型](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="deaad-150">招聘请求以及相关实体和选项集</span><span class="sxs-lookup"><span data-stu-id="deaad-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="deaad-151">示例查询：</span><span class="sxs-lookup"><span data-stu-id="deaad-151">Example query:</span></span> 

- [<span data-ttu-id="deaad-152">招聘请求的查询示例</span><span class="sxs-lookup"><span data-stu-id="deaad-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="deaad-153">实体:</span><span class="sxs-lookup"><span data-stu-id="deaad-153">Entities:</span></span>

- [<span data-ttu-id="deaad-154">招聘请求</span><span class="sxs-lookup"><span data-stu-id="deaad-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="deaad-155">招聘请求职位</span><span class="sxs-lookup"><span data-stu-id="deaad-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="deaad-156">招聘请求技能</span><span class="sxs-lookup"><span data-stu-id="deaad-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="deaad-157">招聘请求教育</span><span class="sxs-lookup"><span data-stu-id="deaad-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="deaad-158">招聘请求位置</span><span class="sxs-lookup"><span data-stu-id="deaad-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="deaad-159">选项集：</span><span class="sxs-lookup"><span data-stu-id="deaad-159">Option sets:</span></span>

- [<span data-ttu-id="deaad-160">工作免除情况</span><span class="sxs-lookup"><span data-stu-id="deaad-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="deaad-161">招聘请求职位状态</span><span class="sxs-lookup"><span data-stu-id="deaad-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="deaad-162">招聘请求状态</span><span class="sxs-lookup"><span data-stu-id="deaad-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="deaad-163">监管工作类别</span><span class="sxs-lookup"><span data-stu-id="deaad-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="deaad-164">可雇用的应聘者及相关实体和选项集</span><span class="sxs-lookup"><span data-stu-id="deaad-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="deaad-165">示例查询：</span><span class="sxs-lookup"><span data-stu-id="deaad-165">Example query:</span></span>

- [<span data-ttu-id="deaad-166">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="deaad-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="deaad-167">实体:</span><span class="sxs-lookup"><span data-stu-id="deaad-167">Entities:</span></span>

- [<span data-ttu-id="deaad-168">可雇用的应聘者</span><span class="sxs-lookup"><span data-stu-id="deaad-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="deaad-169">人员</span><span class="sxs-lookup"><span data-stu-id="deaad-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="deaad-170">人员教育</span><span class="sxs-lookup"><span data-stu-id="deaad-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="deaad-171">人员专业经验</span><span class="sxs-lookup"><span data-stu-id="deaad-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="deaad-172">人员地址</span><span class="sxs-lookup"><span data-stu-id="deaad-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="deaad-173">当事方联系人</span><span class="sxs-lookup"><span data-stu-id="deaad-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="deaad-174">人员技能</span><span class="sxs-lookup"><span data-stu-id="deaad-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="deaad-175">评级级别</span><span class="sxs-lookup"><span data-stu-id="deaad-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="deaad-176">人员证书</span><span class="sxs-lookup"><span data-stu-id="deaad-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="deaad-177">证书类型</span><span class="sxs-lookup"><span data-stu-id="deaad-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="deaad-178">人员筛选</span><span class="sxs-lookup"><span data-stu-id="deaad-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="deaad-179">筛选类型</span><span class="sxs-lookup"><span data-stu-id="deaad-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="deaad-180">人员标识号</span><span class="sxs-lookup"><span data-stu-id="deaad-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="deaad-181">选项集：</span><span class="sxs-lookup"><span data-stu-id="deaad-181">Option sets:</span></span>

- [<span data-ttu-id="deaad-182">申请人集成结果</span><span class="sxs-lookup"><span data-stu-id="deaad-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="deaad-183">空白/是/否</span><span class="sxs-lookup"><span data-stu-id="deaad-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="deaad-184">完成状态</span><span class="sxs-lookup"><span data-stu-id="deaad-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="deaad-185">联系人类型</span><span class="sxs-lookup"><span data-stu-id="deaad-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="deaad-186">教育信用基础</span><span class="sxs-lookup"><span data-stu-id="deaad-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="deaad-187">性</span><span class="sxs-lookup"><span data-stu-id="deaad-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="deaad-188">婚姻状况</span><span class="sxs-lookup"><span data-stu-id="deaad-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="deaad-189">一年中的月份</span><span class="sxs-lookup"><span data-stu-id="deaad-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="deaad-190">否/是</span><span class="sxs-lookup"><span data-stu-id="deaad-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="deaad-191">期间单位</span><span class="sxs-lookup"><span data-stu-id="deaad-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="deaad-192">筛选频率</span><span class="sxs-lookup"><span data-stu-id="deaad-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="deaad-193">筛选频率生成来源</span><span class="sxs-lookup"><span data-stu-id="deaad-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="deaad-194">技能级别类型</span><span class="sxs-lookup"><span data-stu-id="deaad-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="deaad-195">请参阅</span><span class="sxs-lookup"><span data-stu-id="deaad-195">See also</span></span>

[<span data-ttu-id="deaad-196">招聘工作应聘者</span><span class="sxs-lookup"><span data-stu-id="deaad-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="deaad-197">什么是 Microsoft Dataverse？</span><span class="sxs-lookup"><span data-stu-id="deaad-197">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="deaad-198">使用 Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="deaad-198">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="deaad-199">使用 Web API 创建和更新选项集</span><span class="sxs-lookup"><span data-stu-id="deaad-199">Create and update option sets using the Web API</span></span>](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]