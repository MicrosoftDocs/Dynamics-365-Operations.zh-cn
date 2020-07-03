---
title: 定义和管理福利计划
description: 人力资源提供一组工具，可使用这组工具设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员的薪酬计划。 本文章提供了有关如何设置管理福利的信息。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a7fe99d4982b8f35871b15e8049c39eb806e315c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430018"
---
# <a name="define-and-manage-a-benefits-program"></a>定义和管理福利计划

Human Resources 提供一组工具，可使用这组工具设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员的薪酬计划。 本文章提供了有关如何设置和管理福利的信息。

## <a name="benefit-setup"></a>福利设置

您必须先创建每项福利的元素，然后工作人员才能在这些福利中登记。 这些元素结合类似的福利计划并定义默认设置，如扣缴比率和核算详细信息。 许多这些设置可在工作人员随后在福利中登记时进行调整。 对于每个福利计划，组织可提供多个登记选项，或者工作人员可放弃该福利计划中的登记。 

[![福利处理流程](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>福利元素

在开始创建福利并在其中注册工作人员之前，您必须定义构成福利的元素：类型、计划和选项。

-   **类型** - 某项特定福利计划的集合，如医疗或停车。
-   **计划** - 从提供商商定的特定福利。
-   **选项** - 覆盖范围级别，例如：仅员工或员工及其配偶。

对于每种类型的福利（例如视力或护齿），组织可向其工作人员提供一个或多个计划。 对于每个计划，该组织可提供不同的选项。 例如，工作人员可以其年薪的一倍、两倍或三倍购买附加期限的人寿保险。 计划和选项的每个组合将成为工作人员可登记的福利。 

[![福利图片](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>资格
许多因素决定工作人员有资格享有雇主提供的各种类型福利。 当您在 Dynamics 365 Human Resources 中创建福利时，可以设置应用于该福利的资格类型。 

您可以向所有工作人员提供福利。 例如，某些公司向所有员工提供停车证作为附加福利。 当您创建此福利时，将资格设置为**所有工作人员均符合资格**。 

对于其他福利（例如扣押和征收税款），资格不适用。 当您创建这些类型的福利时，将资格设置为**跳过资格处理**。 

最后，福利资格可基于规则。 例如，公司向员工提供两种类型的人寿保险福利。 行政职员有资格享有一项人寿保险计划，而所有其他的全职员工则有资格享有另一项人寿保险计划。 在 Human Resources 中，您可以创建一种福利资格规则以找到所有行政职员和另一种规则以找到所有其他全职员工，然后将这些规则应用于相应的福利。

## <a name="enrollment"></a>登记
在创建了组织提供的福利并确定了资格后，您可以在福利中登记您的工作人员。 在一个流程中，您可以在福利中登记一个工作人员，也可以在一项或多项福利中登记多个工作人员。 

有时，组织会停止提供某些福利。 在这种情况下，您必须更新福利和已登记的工作人员。 大批福利到期让您可以同时更改福利或已登记该福利的工作人员的到期日期。 您还可以选择在某项福利中登记的多个工作人员，并更改该其福利覆盖的结束日期。 

同样，如果您决定提供的福利期限比原始计划期限更长，则大批福利到期也让您可以同时扩展福利和已登记该福利的工作人员的到期日期。


