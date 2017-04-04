---
title: "定义和管理的个获益计划"
description: "人力资源提供一组工具，可使用这组工具设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员的薪酬计划。 本文章提供了有关如何设置管理福利的信息。"
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>定义和管理的个获益计划

人力资源提供一组工具，可使用这组工具设置和维护组织提供或为其工作人员处理的福利、扣缴和工作人员的薪酬计划。 此主题提供的信息介绍如何设置管理福利。

<a name="benefit-setup"></a>福利设置
-------------

您必须先创建每项福利的元素，然后工作人员才能在这些福利中登记。 这些元素结合类似的福利计划并定义默认设置，如扣缴比率和核算详细信息。 许多这些设置可在工作人员随后在福利中登记时进行调整。 对于每个福利计划，组织可提供多个登记选项，或者工作人员可放弃该福利计划中的登记。 

[] (![福利流程。/media/benefit 流程 flow1.png)](。/media/benefit 流程 flow1.png)

## <a name="benefit-elements"></a>福利元素
在您开始创建福利并将工作人员登记在其中之前，您必须定义组成福利的元素：类型、计划和选项。

-   **类型** - 某项特定福利计划的集合，如医疗或停车。
-   **计划** - 从提供商商定的特定福利。
-   **选项** - 覆盖范围级别，例如：仅员工或员工及其配偶。

对于每种类型的福利（例如视力或护齿），组织可向其工作人员提供一个或多个计划。 对于每个计划，该组织可提供不同的选项。 例如，工作人员可以其年薪的一倍、两倍或三倍购买附加期限的人寿保险。 计划和选项的每个组合将成为工作人员可登记的福利。 

[] (![福利图片。/media/benefit-pic.png)](。/media/benefit-pic.png)

## <a name="eligibility"></a>资格
许多因素决定工作人员有资格享有雇主提供的各种类型福利。 当您在 Microsoft Dynamics 365 中创建一福利的工序时，可以设置适用于该资格的福利类型。 

您可以对所有应用可用工作人员。 例如，某些公司向所有员工提供停车通过为附加福利。 当您创建此福利时，将资格设置为**“所有工作人员均符合资格”**。 

对于其他福利，例如税、征收和，资格不适用。 福利，您乳清您创建了这些类型设置资格**请跳过资格**流程。 

最后，福利资格可以基于规则的。 例如，公司向员工提供赔偿金生命保险保险的两个种类型。 管理员工有资格享受的生命保险，计划，而有些全职员工有资格享受其他生命保险计划。 在工序的 Dynamics 365，您可以创建一福利资格规则找到所有员工和管理其他规则找到其他全职员工，然后应用这些规则与相应的福利。

## <a name="enrollment"></a>登记
在创建了组织提供的福利并确定了资格后，您可以在福利中登记您的工作人员。 在一个流程中，您可以在福利中登记一个工作人员，也可以在一项或多项福利中登记多个工作人员。 

有时，组织会停止提供某些福利。 在这种情况下，必须更新登记的福利和工作人员。 质量福利到期可以同时更改某一福利和工作人员登记该福利的到期日期。 您还可以选择在某项福利中登记的多个工作人员，并更改该其福利覆盖的结束日期。 

同样，如果您决定提供的福利期限比原始计划期限更长，则大批福利到期也让您可以同时扩展福利和已登记该福利的工作人员的到期日期。

<a name="see-also"></a>请参阅
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


