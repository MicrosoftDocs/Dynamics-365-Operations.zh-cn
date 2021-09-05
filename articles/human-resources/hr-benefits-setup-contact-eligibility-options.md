---
title: 配置个人联系人资格选项
description: 本主题说明如何在 Microsoft Dynamics 365 Human Resources 中为个人联系人配置资格选项。
author: twheeloc
ms.date: 08/24/2021
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
ms.openlocfilehash: bd0ba4b609aaf05d37b120eaea71095a589bcc0a
ms.sourcegitcommit: 8592c661b41f9cef8b7ef2863a3b97bf49a4e6f9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/26/2021
ms.locfileid: "7423285"
---
# <a name="configure-personal-contact-eligibility-options"></a>配置个人联系人资格选项

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题将介绍如何在 Microsoft Dynamics 365 Human Resources 中配置可以在福利中使用的个人联系人的类型。 个人联系人是您的计划覆盖的个人（依赖方）或将从您的计划中受益的个人（受益人）。 依赖方通常是配偶或子女。 受益人可以是配偶、子女、信托人或父母。

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **个人联系人资格选项**。

2. 选择 **新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **资格选项** | 用于标识资格选项的唯一资格选项名称或代码。 |
   | **说明** | 资格选项的简短描述。 |
   | **联系人资格代码** | 最准确描述个人资格选项的系统代码。 您可以从以下各项中选择： <ul><li>关系</li><li>学生</li><li>超龄依赖方</li><li>超出年限的禁用依赖方</li></ul> |
   | **状态** | 资格选项的状态。 如果资格选项的状态设置为无效，那么您不能为个人联系人选择该个人联系人资格选项。 |
   | **关系** | 指定个人联系人和员工之间的关系。 仅当联系人资格代码设置为“关系”时，此字段才有效。 |
   | **帐龄** | 福利计划的合格个人联系人的最大年龄。 仅在选择关系时此字段才有效。 此年龄将与计算出的个人联系人的年龄进行比较。 计算的年龄为：（覆盖范围日期 – 个人联系人的出生日期/365）。 此数字始终是整数。 |

4. 选择 **保存**。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
