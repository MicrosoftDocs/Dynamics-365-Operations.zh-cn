---
title: 配置等待时段
description: 在 Microsoft Dynamics 365 Human Resources 中，等待天数建立用于福利计划的里程碑。
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
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
ms.openlocfilehash: 07ceed65a0346912d4be012a5cec502b0f0a6149
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111556"
---
# <a name="configure-waiting-periods"></a>配置等待时段

在 Microsoft Dynamics 365 Human Resources 中，等待天数建立用于福利计划的里程碑。 例如，从雇用日期起三个月，每个月的第一天，或六个月。   

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **等待期间**。

2. 选择 **新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **等待代码** | 等待期间的唯一标识符。 |
   | **说明** | 等待期间的描述。 |
   | **等待方法** | 从值的下拉列表中选择合适的等待方法。 选项包括“净”、“当前月份”、“当前季度”、“当前年度”和“当前周”。 |
   | **月数** | 输入要加到等待方法的月数以计算等待日期。 |
   | **天数** | 输入要加到等待方法的天数以计算等待日期。 |
   | **等待天数** | 选择要用于计算等待日期的等待天数。 |

4. 选择 **保存**。
