---
title: 配置员工自助服务
description: 在 Microsoft Dynamics 365 Human Resources 中，您可以为员工自助服务中的顶层导航配置磁贴。
author: twheeloc
ms.date: 12/06/2021
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
ms.openlocfilehash: 1e0c59eb8db5a97405e87922cc65f3eb74bee48e
ms.sourcegitcommit: b101c21f972fdad2667431f712222e040cd69d43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/07/2021
ms.locfileid: "7898432"
---
# <a name="configure-employee-self-service"></a>配置员工自助服务

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

在 Microsoft Dynamics 365 Human Resources 中，您可以为 **员工自助服务** 中的顶层导航配置磁贴。 福利计划磁贴可将用户引导至他们有资格登记参加的福利计划。

## <a name="set-up-a-benefit-plans-tile"></a>设置福利计划磁贴

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **员工自助服务参数**。

2. 选择 **福利计划磁贴设置** 选项卡，然后选择 **新建**。

3. 为以下字段指定值。

   | 字段 | Description |
   | --- | --- |
   | **计划类型代码** | 在 **福利自助服务** 中选择此磁贴时显示的计划类型。 |
   | **磁贴 ID** | 磁贴的唯一标识符。 |
   | **磁贴标签文本** | **福利自助服务** 上磁贴将显示的文本。 |
   | **说明** | 磁贴的描述。 |
   | **磁贴背景图像** | 用于磁贴的图像的 URL（可选）。 |
   | **跟踪开放登记** | 选择此选项可跟踪此计划类型的开放登记进度。 例如，您可能已创建了 **计划类型 = 其他** 的计划。 这些计划可能是您不希望跟踪其登记进度的可选计划。 如果未选择此计划类型，则在 **公开登记** 选项卡上跟踪登记进度或登记完成时，将忽略此类型的计划。此设置适用于为所有期间和法人选择的计划类型。 |

4. 选择 **保存**。

## <a name="set-up-a-flex-credit-plan-tile"></a>设置弹性信贷计划磁贴

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **员工自助服务参数**。

2. 选择 **弹性信贷计划磁贴设置** 选项卡，然后选择 **新建**。

3. 为以下字段指定值。

   | 字段 | Description |
   | --- | --- |
   | **福利信贷 ID** | 在 **福利自助服务** 中选择此磁贴时将显示的弹性信贷项目计划。 |
   | **磁贴 ID** | 磁贴的唯一标识符。 |
   | **磁贴标签文本** | **福利自助服务** 上磁贴将显示的文本。 |
   | **说明** | 磁贴的描述。 |
   | **磁贴背景图像** | 用于磁贴的图像的 URL（可选）。 |
   | **跟踪开放登记** | 选择此选项可跟踪此计划类型的开放登记进度。 例如，您可能已创建了 **计划类型 = 其他** 的计划。 这些计划可能是您不希望跟踪其登记进度的可选计划。 如果未选择此计划类型，则在 **公开登记** 选项卡上跟踪登记进度或登记完成时，将忽略此类型的计划。此设置适用于为所有期间和法人选择的计划类型。 |

4. 选择 **保存**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
