---
title: 工资单集成 API 简介
description: 本主题介绍了 Dynamics 365 Human Resources 工资单集成 API。
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7122dc7325c7fb33c4bf90e3d1a6cf1c95bd73e72232b9060f7cc04899223765
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782699"
---
# <a name="payroll-integration-api-introduction"></a>工资单集成 API 简介

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文档介绍了 Dynamics 365 Human Resources 工资单集成 API。 该 API 支持 Human Resources 与合作工资单系统之间的简化端到端集成。 集成体验始于具有员工配置文件、薪金和扣缴以及缴纳信息的 Human Resources。 当您雇用员工并在 Human Resources 中输入所需的配置文件和付款信息时，工资单系统会提取此信息以在处理工资单时使用。 还将提取对员工或付款信息所做的任何更新，以用于以后的付款运行。

[![工资单集成流。](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

为了支持集成，Human Resources 包括以下组件：

- [将员工标记为准备付款的功能。](hr-compensation-payroll.md)
- 为集成应用程序开启新功能的集成 API。

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

此 API 基于 Microsoft Dataverse（以前称为 Common Data Service）构建。 与此 API 的所有 RESTful 交互都通过使用 OData 的 Microsoft Dataverse Web API 完成。 此 API 是 Dataverse Web API 的子集。 Dataverse Web API 定义诸如身份验证、SLA、批处理、并发控制和错误处理等特征。

有关 Microsoft Dataverse Web API 的更多一般信息，请参阅：

- [什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)
- [使用 Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse 开发人员指南](/powerapps/developer/data-platform)

本文档包含有关使用 Dataverse Web API 的详细信息和开发人员指南，包括以下主题：

- [使用 Web API 对 Microsoft Dataverse 进行身份验证](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [使用 Web API 执行操作](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [将 Postman 与 Web API 结合使用](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [使用更改跟踪将数据与外部系统同步](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Dataverse 中适用于 Human Resources 的虚拟表

工资单集成 API 的终结点使用 Microsoft Dataverse 的虚拟表平台功能。 默认情况下，虚拟表及其关联的 API 终结点不针对 Human Resources 环境部署，以让组织可以确定哪些 OData 终结点将为环境公开。 要使用 API，必须为环境生成适用于 Human Resources 实体的虚拟表。

有关为 API 生成虚拟表的信息，请参阅[配置 Dataverse 虚拟表](./hr-admin-integration-common-data-service-virtual-entities.md)。

## <a name="data-model"></a>数据模型

下图说明了 API 中的关系。 若干个类型具有 Human Resources 中其他预先存在的实体的外键，这里没有说明。 本文档提供有关特定于工资单集成场景的实体的信息。 但是，适用于 Human Resources 的 Dataverse Web API 中还有很多其他实体也可能与您的集成相关。 其中某些实体在外键关系或导航属性中引用。

[![工资单集成 API 数据模型。](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>工资单员工和相关实体

实体:

- [工资单员工](hr-admin-integration-payroll-api-payroll-employee.md)
- [工资单工作人员地址](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [工资单固定薪酬计划](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [工资单可变薪酬计划](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [工资单职位工作](hr-admin-integration-payroll-api-payroll-position-job.md)
- [工资单职位](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>请参阅

[生成并查看工资单实体](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[配置 Human Resources 参数](hr-setup-parameters.md)<br>
[配置 Human Resources 共享参数](hr-setup-shared-parameters.md)<br>
[什么是 Microsoft Dataverse？](/powerapps/maker/data-platform/data-platform-intro)<br>
[使用 Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
