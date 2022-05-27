---
title: 处理登记资格
description: 本主题介绍如何运行登记资格流程。
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78a7de6dbb8d8ed13392eb7eb9aa02b15db2e009
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693162"
---
# <a name="process-enrollment-eligibility"></a>处理登记资格


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍如何运行登记资格流程。

1. 在 **福利管理** 工作区中，在 **处理** 下，选择 **登记资格处理**。

2. 在 **运行福利登记资格流程** 对话框中，为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **登记期间** | 要处理其间的登记资格的登记期间。 |
   | **法人** | 要为其处理登记资格的法人。 |
   | **工作线程** | 要为其处理登记资格的工作人员。 如果将此字段留为空白，将处理所有工作人员的登记资格。 |
   | **福利计划** | 要为其处理登记资格的福利计划。

3. 如果要在后台运行此流程，请选择 **在后台运行** 并执行以下任务：

   1. 输入流程的信息。

   2. 要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。

   3. 要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。

   4. 选择 **确定**。 流程将使用您设置的参数运行。

4. 选择 **确定**。

## <a name="view-process-results"></a>查看流程结果

本主题介绍如何查看资格流程结果。

1.  在 **福利管理** 工作区中，在 **处理** 下，选择 **流程结果**。

2.  在 **流程结果** 页面中，指定了以下字段：

   | 字段 | 说明 |
   | --- | --- |
   | **流程 ID** | 工作人员、法人和运行的流程的组合的唯一 ID。 |
   | **进程类型** | 这用于标识运行的流程。 例如：登记。 |
   | **时间戳** | 资格流程的运行时间。 |
   | **法人** | 登记流程中指定的法人。 |
   | **工作线程** | 处理的工作人员。 |
   | **计划 | 尝试的登记所属福利计划。 |
   | **资格规则** | 处理的资格规则。 如果在运行资格前遇到了错误，此字段将为空。 例如，如果尚未为某个工作人员定义薪酬，将不会运行资格流程，并且此字段将保留为空。 |
   | **结果状态** | 将为“合格”或“不合格”。 如果工作人员不满足资格规则条件，工作人员缺少必需信息（如付款频率或固定薪酬），或福利计划中缺少的信息导致无法登记工作人员，结果状态将为“不合格”。 |
   | **结果消息** | 指示工作人员为何不符合福利计划的资格或是否通过了资格规则。 |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
