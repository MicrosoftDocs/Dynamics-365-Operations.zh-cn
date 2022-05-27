---
title: 处理生活事件更改
description: 本主题介绍如何在 Microsoft Dynamics 365 Human Resources 中处理生活事件更改。
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f43ee914bb57b14969b6d729218accbd1009d67a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691769"
---
# <a name="process-life-event-changes"></a>处理生活事件更改


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

在 Microsoft Dynamics 365 Human Resources 中处理生活事件更改以进行两项生活事件更改：

- 生日更改
- 资格规则覆盖到期更改 

1. 在 **福利管理** 工作区中，在 **处理** 下，选择 **生活事件更改处理**。

2. 在 **运行生活事件更改流程** 对话框中，为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | 登记期间 | 要处理其间的生活事件更改的登记期间。 |
   | 法人 | 要为其处理生活事件更改的法人。 |

3. 如果要在后台运行此流程，请选择 **在后台运行** 并执行以下任务：

   1. 输入流程的信息。

   2. 要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。

   3. 要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。

   4. 选择 **确定**。 流程将使用您设置的参数运行。

4. 选择 **确定**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
