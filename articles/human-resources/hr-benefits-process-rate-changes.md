---
title: 处理比率更改
description: 处理当新的或现有的福利计划的资格规则设置发生更改时，Microsoft Dynamics 365 Human Resources 中的福利比率更改。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5cfecc4da90b4fb39bdece38095f3b25023e4cae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055692"
---
# <a name="process-rate-changes"></a>处理比率更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

处理当新的或现有的福利计划的资格规则设置发生更改时，Microsoft Dynamics 365 Human Resources 中的福利比率更改。 如果创建了新的资格规则并将其分配给计划，这将提示系统重新运行工作人员资格，以根据新的资格选项检查工作人员现在是否有资格享受计划。 

1. 在 **福利管理** 工作区中，在 **处理** 下，选择 **比率更改更新处理**。

2. 在 **运行福利比率更新流程** 对话框中，为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **登记期间** | 要处理其间的比率更改的登记期间。 |

3. 如果要在后台运行此流程，请选择 **在后台运行** 并执行以下任务：

   1. 输入流程的信息。

   2. 要设置重复性作业，请选择 **重复**，输入重复信息，然后选择 **确定**。

   3. 要设置作业预警，请选择 **预警**，选择要接收的预警，然后选择 **确定**。

   4. 选择 **确定**。 流程将使用您设置的参数运行。

4. 选择 **确定**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]