---
title: 福利管理概览
description: Dynamics 365 Human Resources 中的福利管理功能概述。 通过易于使用的在线体验，为您的员工提供更多的福利选项。
author: andreabichsel
manager: tfehr
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4ae4270f3185f8795753ecdb209515ecd6e86486
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111675"
---
# <a name="benefits-management-overview"></a>福利管理概述

为了保持竞争力，您必须提供丰富的福利，以吸引和留住最好的员工。 除了医疗和牙科保险等标准福利外，您可能还希望提供更多服务，例如收养帮助、娱乐计划和服装津贴。 Microsoft Dynamics 365 Human Resources 中的福利管理为您提供了一个灵活的解决方案，它支持多种福利选项。 Human Resources 还提供易于使用的员工体验，以展示您的服务。

- 增强的福利计划使您可以创建和管理独特的福利计划，并支持复杂的福利比率表和嵌套层。 您可以轻松创建福利计划、捆绑和自动登记规则，以提供更轻松的员工体验。

- 弹性信贷项目可让您按比例来支持退休和其他生命事件。

- 广泛的资格规则可确保您为合适的员工提供合适的福利。

- 在线福利登记为您的员工提供轻松的体验。

- 合格的生命事件处理支持未来的生命事件。

如果您想访问演示数据，您需要重新部署沙盒环境。

## <a name="enable-benefits-management"></a>雇用福利管理

本主题介绍如何在 Human Resources 中开启功能。 还介绍在打开“福利管理”后，“福利管理”将替换或禁用 Human Resources 中的哪些现有功能。

> [!IMPORTANT]
> 不能在 **生产** 环境中禁用已启用的福利管理。 建议在 **生产** 环境中启用福利管理之前，在 **沙盒** 环境中启用和测试。 旧福利功能和新福利管理功能之间差别很大，需要在投入生产之前进行更多设置和应该进行测试。

- [管理功能](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>配置员工信息

必须先提供必需信息，才能为员工登记福利。 您必须在员工的开始日期在 **固定薪酬计划** 中登记员工，并且必须在 **工作人员** 窗体的 **雇用详细信息** 中选择 **福利支付频率**。

如果您有一名员工将收到诸如佣金之类的附加报酬，您可以从员工记录添加 **福利年薪** 金额。 人力资源部门在确定覆盖范围金额时将使用 **福利年薪** 金额，而不是固定薪酬年度金额。 **福利年薪** 必须自员工的开始日期或福利期开始之日（以较早者为准）起生效。 如果同时记录了员工的固定薪酬和福利年薪金额，福利年薪将用于确定覆盖范围金额。

创建用户基于性别或年龄评定的福利计划时，必须输入员工的生日和性别以计算福利成本。

## <a name="configure-benefits-management"></a>配置福利管理

在为员工创建福利计划之前，需要配置计划的选项。

- [设置福利管理参数](hr-benefits-setup-parameters.md)
- [配置资格规则和选项](hr-benefits-setup-eligibility-rules.md)
- [配置个人联系人资格选项](hr-benefits-setup-contact-eligibility-options.md)
- [创建覆盖范围选项](hr-benefits-setup-coverage-options.md)
- [设置付款频率](hr-benefits-setup-payment-frequencies.md)
- [配置生活事件类型](hr-benefits-setup-life-event-types.md)
- [创建计划类型](hr-benefits-setup-plan-types.md)
- [设置原因代码](hr-benefits-setup-reason-codes.md)
- [设置层代码](hr-benefits-setup-tier-codes.md)
- [配置费率](hr-benefits-setup-rates.md)
- [配置扣缴](hr-benefits-setup-deductions.md)
- [配置等待天数](hr-benefits-setup-waiting-days.md)
- [配置等待时段](hr-benefits-setup-waiting-periods.md)
- [设置舍入规则](hr-benefits-setup-rounding-rules.md)
- [创建雇用类别](hr-benefits-setup-employment-categories.md)
- [设置雇用类型](hr-benefits-setup-employment-types.md)
- [配置员工自助服务](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>创建福利计划

这些文章说明如何创建福利计划，包括捆绑和弹性信贷项目。

- [设置福利计划](hr-benefits-plans-setup.md)
- [设置弹性信贷计划](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>处理福利计划

您需要处理一些更改以使它们生效。

- [处理登记资格](hr-benefits-process-enrollment-eligibility.md)
- [处理生命事件](hr-benefits-process-life-events.md)
- [处理生命事件更改](hr-benefits-process-life-event-changes.md)
- [处理生命事件资格](hr-benefits-process-life-event-eligibility.md)
- [处理比率更改](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]