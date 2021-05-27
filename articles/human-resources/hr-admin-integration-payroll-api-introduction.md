---
title: 工资单集成 API 简介
description: 本主题介绍了 Dynamics 365 Human Resources 工资单集成 API。
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a7be5ad42642de48ffdb2731a1300a953c5ede4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022755"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="31cb8-103">工资单集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="31cb8-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="31cb8-104">本文档介绍了 Dynamics 365 Human Resources 工资单集成 API。</span><span class="sxs-lookup"><span data-stu-id="31cb8-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="31cb8-105">该 API 支持 Human Resources 与合作工资单系统之间的简化端到端集成。</span><span class="sxs-lookup"><span data-stu-id="31cb8-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="31cb8-106">集成体验始于具有员工配置文件、薪金和扣缴以及缴纳信息的 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="31cb8-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="31cb8-107">当您雇用员工并在 Human Resources 中输入所需的配置文件和付款信息时，工资单系统会提取此信息以在处理工资单时使用。</span><span class="sxs-lookup"><span data-stu-id="31cb8-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="31cb8-108">还将提取对员工或付款信息所做的任何更新，以用于以后的付款运行。</span><span class="sxs-lookup"><span data-stu-id="31cb8-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![工资单集成流](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="31cb8-110">为了支持集成，Human Resources 包括以下组件：</span><span class="sxs-lookup"><span data-stu-id="31cb8-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="31cb8-111">将员工标记为准备付款的功能</span><span class="sxs-lookup"><span data-stu-id="31cb8-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="31cb8-112">为集成应用程序开启新功能的集成 API</span><span class="sxs-lookup"><span data-stu-id="31cb8-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="31cb8-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="31cb8-113">Microsoft Dataverse</span></span>

<span data-ttu-id="31cb8-114">此 API 基于 Microsoft Dataverse（以前称为 Common Data Service）构建。</span><span class="sxs-lookup"><span data-stu-id="31cb8-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="31cb8-115">与此 API 的所有 RESTful 交互都通过使用 OData 的 Microsoft Dataverse Web API 完成。</span><span class="sxs-lookup"><span data-stu-id="31cb8-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="31cb8-116">此 API 是 Dataverse Web API 的子集。</span><span class="sxs-lookup"><span data-stu-id="31cb8-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="31cb8-117">Dataverse Web API 定义诸如身份验证、SLA、批处理、并发控制和错误处理等特征。</span><span class="sxs-lookup"><span data-stu-id="31cb8-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="31cb8-118">有关 Microsoft Dataverse Web API 的更多一般信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="31cb8-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="31cb8-119">什么是 Microsoft Dataverse？</span><span class="sxs-lookup"><span data-stu-id="31cb8-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="31cb8-120">使用 Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="31cb8-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="31cb8-121">Microsoft Dataverse 开发人员指南</span><span class="sxs-lookup"><span data-stu-id="31cb8-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="31cb8-122">本文档包含有关使用 Dataverse Web API 的详细信息和开发人员指南，包括以下主题：</span><span class="sxs-lookup"><span data-stu-id="31cb8-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="31cb8-123">使用 Web API 对 Microsoft Dataverse 进行身份验证</span><span class="sxs-lookup"><span data-stu-id="31cb8-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="31cb8-124">使用 Web API 执行操作</span><span class="sxs-lookup"><span data-stu-id="31cb8-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="31cb8-125">将 Postman 与 Web API 结合使用</span><span class="sxs-lookup"><span data-stu-id="31cb8-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="31cb8-126">使用更改跟踪将数据与外部系统同步</span><span class="sxs-lookup"><span data-stu-id="31cb8-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="31cb8-127">Dataverse 中适用于 Human Resources 的虚拟表</span><span class="sxs-lookup"><span data-stu-id="31cb8-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="31cb8-128">工资单集成 API 的终结点使用 Microsoft Dataverse 的虚拟表平台功能。</span><span class="sxs-lookup"><span data-stu-id="31cb8-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="31cb8-129">默认情况下，虚拟表及其关联的 API 终结点不针对 Human Resources 环境部署，以让组织可以确定哪些 OData 终结点将为环境公开。</span><span class="sxs-lookup"><span data-stu-id="31cb8-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="31cb8-130">要使用 API，必须为环境生成适用于 Human Resources 实体的虚拟表。</span><span class="sxs-lookup"><span data-stu-id="31cb8-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="31cb8-131">有关为 API 生成虚拟表的信息，请参阅[配置 Dataverse 虚拟表](./hr-admin-integration-common-data-service-virtual-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="31cb8-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="31cb8-132">数据模型</span><span class="sxs-lookup"><span data-stu-id="31cb8-132">Data model</span></span>

<span data-ttu-id="31cb8-133">下图说明了 API 中的关系。</span><span class="sxs-lookup"><span data-stu-id="31cb8-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="31cb8-134">若干个类型具有 Human Resources 中其他预先存在的实体的外键，这里没有说明。</span><span class="sxs-lookup"><span data-stu-id="31cb8-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="31cb8-135">本文档提供有关特定于工资单集成场景的实体的信息。</span><span class="sxs-lookup"><span data-stu-id="31cb8-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="31cb8-136">但是，适用于 Human Resources 的 Dataverse Web API 中还有很多其他实体也可能与您的集成相关。</span><span class="sxs-lookup"><span data-stu-id="31cb8-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="31cb8-137">其中某些实体在外键关系或导航属性中引用。</span><span class="sxs-lookup"><span data-stu-id="31cb8-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![工资单集成 API 数据模型](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="31cb8-139">工资单员工和相关实体</span><span class="sxs-lookup"><span data-stu-id="31cb8-139">Payroll employee and related entities</span></span>

<span data-ttu-id="31cb8-140">实体:</span><span class="sxs-lookup"><span data-stu-id="31cb8-140">Entities:</span></span>

- [<span data-ttu-id="31cb8-141">工资单员工</span><span class="sxs-lookup"><span data-stu-id="31cb8-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="31cb8-142">工资单工作人员地址</span><span class="sxs-lookup"><span data-stu-id="31cb8-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="31cb8-143">工资单固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="31cb8-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="31cb8-144">工资单职位工作</span><span class="sxs-lookup"><span data-stu-id="31cb8-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="31cb8-145">工资单职位</span><span class="sxs-lookup"><span data-stu-id="31cb8-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="31cb8-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="31cb8-146">See also</span></span>

[<span data-ttu-id="31cb8-147">生成并查看工资单实体</span><span class="sxs-lookup"><span data-stu-id="31cb8-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="31cb8-148">配置 Human Resources 参数</span><span class="sxs-lookup"><span data-stu-id="31cb8-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="31cb8-149">配置 Human Resources 共享参数</span><span class="sxs-lookup"><span data-stu-id="31cb8-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="31cb8-150">什么是 Microsoft Dataverse？</span><span class="sxs-lookup"><span data-stu-id="31cb8-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="31cb8-151">使用 Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="31cb8-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]