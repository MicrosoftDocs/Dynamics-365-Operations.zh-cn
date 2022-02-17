---
title: 配置等待时段
description: 在 Microsoft Dynamics 365 Human Resources 中，等待天数建立用于福利计划的里程碑。
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3df65a89ca4b18de2c823ca02fd8daa3da1e9ea6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066867"
---
# <a name="configure-waiting-periods"></a>配置等待时段


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

在 Microsoft Dynamics 365 Human Resources 中，等待天数建立用于福利计划的里程碑。 例如，从雇用日期起三个月，每个月的第一天，或六个月。   

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **等待期间**。

2. 选择 **新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **等待代码** | 等待期间的唯一标识符。 |
   | **说明** | 等待期间的描述。 |
   | **等待方法** | 从值的下拉列表中选择合适的等待方法。 选项包括 **净**、**当前月份**、**当前季度**、**当前年度** 和 **当前周**。 |
   | **月数** | 输入要加到等待方法的月数以计算等待日期。 |
   | **天数** | 输入要加到等待方法的天数以计算等待日期。 |
   | **等待天数** | 选择要用于计算等待日期的等待天数。 |

4. 选择 **保存**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
