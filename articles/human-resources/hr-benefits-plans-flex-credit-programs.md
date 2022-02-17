---
title: 设置弹性信贷项目
description: 您可以在 Microsoft Dynamics 365 Human Resources 中使用弹性信贷项目来根据预先确定的弹性信贷数量为员工登记福利。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8f28e3fb603fde2c19669e9936ea0bdcfc866d0e
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065910"
---
# <a name="set-up-flex-credit-programs"></a>设置弹性信贷项目


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您可以在 Microsoft Dynamics 365 Human Resources 中使用弹性信贷项目来根据预先确定的弹性信贷数量为员工登记福利。 员工可以选择如何分配其弹性信贷。 例如，如果员工在配偶的健康保险计划中受保，他们可能希望将原本用于健康保险的信贷额用于其他福利。 

1. 在 **福利管理** 工作区中，在 **计划** 下，选择 **弹性信贷项目**。

2. 选择 **新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **福利信贷 ID** | 弹性信贷项目的唯一标识符。 |
   | **说明** | 弹性信贷项目的描述。 | 
   | **开始日期** | 弹性信贷项目生效的日期。 |
   | **截止日期** | 弹性信贷项目的结束日期。 您可以保留默认值 (12/31/2154) 来指示弹性信贷项目没有计划的到期时间。 |
   | **信贷值总计** | 每位员工必须为自己的福利使用的信贷数量。 |
   | **按比例分配规则** | 用于在弹性信贷期间的中间雇用员工时按比例分配弹性信贷的规则。 </br></br><ul><li>**无** – 如果员工在弹性信贷项目期间开始后被雇用，将不会获得弹性信贷。</li><li>**完整信贷** – 无论员工何时被雇用，员工都会获得全额的弹性信贷。</li><li>**按比例分配** – 员工将根据他们的开始日期获得按比例分配的弹性信贷额。</li></ul> |
   | **弹性信贷按比例分配公式** | 用于为弹性信贷项目福利期间的中间雇用的员工按比例分配弹性信贷的规则。 按比例分配基于雇用开始日期。 仅当您在 **按比例分配规则** 字段中选择 **按比例分配** 时，才使用此字段。 </br></br><ul><li>**每日** – 按比例分配员工按天级别获得的弹性信贷数量。 弹性信贷的总数除以期间内的天数。 例如，如果您的福利期间为 400 天，系统会将弹性信贷的总数除以 400，来计算员工每天收到的弹性信贷的数量。</li><li>**当前月份** – 按比例分配员工按月级别将获得的弹性信贷的数量，舍入到当前月份。 弹性信贷的总数除以期间内的月数。 例如，如果您的福利期间为 15 个月，系统会将弹性信贷的总数除以 15，来计算员工每月收到的弹性信贷的数量。</li><li>**下月** – 按比例分配员工按月级别将获得的弹性信贷的数量，舍入到下一个月。 弹性信贷的总数除以期间内的月数。 例如，如果您的福利期间为 15 个月，系统会将弹性信贷的总数除以 15，来计算员工每月收到的弹性信贷的数量。</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
