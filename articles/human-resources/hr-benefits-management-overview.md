---
title: 福利管理概述
description: Dynamics 365 Human Resources 中的福利管理预览功能概述。 通过易于使用的在线体验，为您的员工提供更多的福利选项。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029455"
---
# <a name="benefits-management-overview"></a>福利管理概述

[!include [banner](includes/preview-feature.md)]

为了保持竞争力，您必须提供丰富的福利，以吸引和留住最好的员工。 除了医疗和牙科保险等标准福利外，您可能还希望提供更多服务，例如收养帮助、娱乐计划和服装津贴。 Microsoft Dynamics 365 Human Resources 中的福利管理预览功能为您提供了一个灵活的解决方案，它支持多种福利选项。 Human Resources 还提供易于使用的员工体验，以展示您的服务。

- 增强的福利计划使您可以创建和管理独特的福利计划，并支持复杂的福利比率表和嵌套层。 您可以轻松创建福利计划、捆绑和自动登记规则，以提供更轻松的员工体验。

- 弹性信贷项目可让您按比例来支持退休和其他生命事件。

- 广泛的资格规则可确保您为合适的员工提供合适的福利。

- 在线福利登记为您的员工提供轻松的体验。

- 合格的生命事件处理与员工自助服务集成在一起，同时还支持未来的生命事件。

如果您想访问演示数据，您需要重新部署沙盒环境。

您可以提供直接反馈或将问题报告给：D365BenefitsPreview@microsoft.com。

## <a name="benefits-management-known-issues"></a>福利管理已知问题

### <a name="eligibility-processing"></a>资格处理

当运行使用 1-5X 薪金、薪金百分比和固定金额覆盖范围金额的福利的资格时，必须将**福利详细信息**日期设置为**工作经历**中的**员工开始日期**。 您还必须包括**工时数**、**付款频率**和**年度福利薪水金额**。 如果工作人员有固定薪酬，则输入**工时数**和**付款频率**。 将计算年度薪水金额。 如果员工是雇员，则不需要输入**工时数**。 我们建议在创建新工作人员时，首先输入固定薪酬。 要更新福利详细信息记录，导航到**工作人员 > 工作人员历史记录 > 雇用详细信息**。 将日期调整为工作人员开始日期。

### <a name="employee-self-service"></a>员工自助服务

更新人寿保险的覆盖范围金额时，不会计算员工金额。 例如，向员工提供人寿保险计划时，他们最多可以选择 50,000 美元的保额，每 1,000 美元保额费用为 0.36 美元。  当员工更新覆盖范围金额时，员工的关联成本保持为零。

对于仅允许单一选择该计划类型的福利计划，如果用户在选择计划后尝试放弃计划，将会收到错误。 例如，用户选择医疗计划并将其放在他们的购物车中。 然后，用户选择**放弃**另一个医疗计划。 用户将收到错误。

## <a name="enable-benefits-management"></a>雇用福利管理

福利管理是一项预览功能，仅在**沙盒**中可用。 这些文章介绍如何在 Human Resources 中打开预览功能。 另外还介绍在打开“福利管理”后，“福利管理”将替换或禁用 Human Resources 中的哪些现有功能。

- [管理功能](hr-admin-manage-features.md)
- [预览功能：福利管理](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>配置福利管理

在为员工创建福利计划之前，需要配置计划的选项。

- [设置福利管理参数](hr-benefits-setup-parameters.md)
- [配置资格规则和选项](hr-benefits-setup-eligibility-rules.md)
- [配置个人联系人资格选项](hr-benefits-setup-contact-eligibility-options.md)
- [创建覆盖范围选项](hr-benefits-setup-coverage-options.md)
- [设置付款频率](hr-benefits-setup-payment-frequencies.md)
- [配置生命事件类型](hr-benefits-setup-life-event-types.md)
- [创建计划类型](hr-benefits-setup-plan-types.md)
- [设置原因代码](hr-benefits-setup-reason-codes.md)
- [设置层代码](hr-benefits-setup-tier-codes.md)
- [配置比率](hr-benefits-setup-rates.md)
- [配置扣缴](hr-benefits-setup-deductions.md)
- [配置等待天数](hr-benefits-setup-waiting-days.md)
- [配置等待期间](hr-benefits-setup-waiting-periods.md)
- [设置舍入规则](hr-benefits-setup-rounding-rules.md)
- [创建雇用类别](hr-benefits-setup-employment-categories.md)
- [设置雇用类型](hr-benefits-setup-employment-types.md)
- [配置员工自助服务](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>创建福利计划

这些文章说明如何创建福利计划，包括捆绑和弹性信贷项目。

- [设置福利计划](hr-benefits-plans-setup.md)
- [创建工作人员福利计划](hr-benefits-plans-worker.md)
- [设置弹性信贷项目](hr-benefits-plans-flex-credit-programs.md)
- [配置未来的生命事件](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>处理福利计划

您需要处理一些更改以使它们生效。

- [处理登记资格](hr-benefits-process-enrollment-eligibility.md)
- [处理生命事件](hr-benefits-process-life-events.md)
- [处理生命事件更改](hr-benefits-process-life-event-changes.md)
- [处理生命事件资格](hr-benefits-process-life-event-eligibility.md)
- [处理比率更改](hr-benefits-process-rate-changes.md)

