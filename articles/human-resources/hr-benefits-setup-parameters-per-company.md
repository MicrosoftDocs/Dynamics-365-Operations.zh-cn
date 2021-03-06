---
title: 针对每个公司配置福利管理参数
description: 在 Microsoft Dynamics 365 Human Resources 中针对每个公司配置福利管理的参数。
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2c564f0dfd1cbe44566269c97218450fedf2173
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057614"
---
# <a name="configure-benefits-management-parameters-per-company"></a>针对每个公司配置福利管理参数

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

对于每个提供福利的组织，您必须配置福利确认电子邮件的设置。

## <a name="configure-confirmation-email-settings"></a>配置确认电子邮件设置

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **人力资源参数**。

2. 在 **福利管理** 选项卡上，为以下字段指定值： 

   | 字段 | 说明 |
   | --- | --- |
   | **发送确认电子邮件** | 打开此功能后，当员工从员工自助服务中的福利登记体验中签出时，将向他们发送确认电子邮件。 |
   | **确认电子邮件模板** | 选择发送登记确认时要使用的组织电子邮件模板。 如果您不选择模板，将发送以下通用电子邮件：<br><br>%EmployeeFirstName%，<br><br>恭喜! 您已成功完成福利登记。<br><br>谢谢，<br><Company/Org name> 福利。 |
   | **默认电子邮件发件人地址** | 发送确认电子邮件时要使用的电子邮件地址。 |

3. 选择 **保存**。

[!INCLUDE[footer-include](../includes/footer-banner.md)]