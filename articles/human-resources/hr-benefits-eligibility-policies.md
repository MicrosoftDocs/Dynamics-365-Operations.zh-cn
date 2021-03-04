---
title: 福利资格策略
description: 本文提供有关福利资格策略的信息，可帮助您定义哪些人有资格享受特定福利。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: fd4def17bf60ae2812927221c45547c5ac379f2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417378"
---
# <a name="benefit-eligibility-policies"></a>福利资格政策

本文提供有关福利资格策略的信息，可帮助您定义哪些人有资格享受特定福利。

在您创建福利时，您决定哪些福利可用于哪些员工。 下表显示您可以使其用于特定员工的福利示例。

| 福利          | 福利可用于谁 |
|------------------|---------------------------------|
| 健康保险 | 所有员工                   |
| 移动电话     | 销售员工、主管人员         |
| 停车证   | 主管人员                      |

以下组件用于创建资格策略：

-   政策规则类型
-   福利资格策略

策略规则类型定义开发具体政策规则时所使用的查询参数。 在您创建政策规则类型后，您可以创建福利资格策略。 策略可以创建适用于一个或多个法人的规则集合。 在每个策略中，您可以查看您之前创建的任何福利资格策略规则类型。 

您定义策略中的规则范围。 例如，如果，您创建一个名为 **主管人员** 的福利资格政策规则类型，您可以指定在该策略中有哪些规则。 在此示例中，规则可能声明包含“主管”一词的任何职称都应包含在规则中。 在您定义规则的参数或在策略包括的规则后，可以将一个特定规则分配到福利。






[!INCLUDE[footer-include](../includes/footer-banner.md)]