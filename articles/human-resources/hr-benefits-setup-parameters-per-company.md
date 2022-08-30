---
title: 配置每个公司的福利管理参数
description: 本文介绍如何在 Microsoft Dynamics 365 Human Resources 中针对每个公司配置福利管理的参数。
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f3f8625a8ebbe6812d2f051649ff2a608ed4b54
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323889"
---
# <a name="configure-benefits-management-parameters-per-company"></a>针对每个公司配置福利管理参数


对于每个提供福利的组织，您必须配置福利确认电子邮件的设置。

## <a name="configure-confirmation-email-settings"></a>配置确认电子邮件设置

1. 在 **福利管理** 工作区中，在 **设置** 下，选择 **人力资源参数**。

2. 在 **福利管理** 选项卡上，为以下字段指定值： 

   | 字段 | 说明 |
   | --- | --- |
   | **发送确认电子邮件** | 打开此功能后，当员工从 **员工自助服务** 中的福利登记体验中签出时，将向他们发送确认电子邮件。 |
   | **确认电子邮件模板** | 选择发送登记确认时要使用的组织电子邮件模板。 如果您不选择模板，将发送以下通用电子邮件：<br><br>%EmployeeFirstName%，<br><br>恭喜! 您已成功完成福利登记。<br><br>谢谢，<br><Company/Org name> 福利。 |
   | **默认电子邮件发件人地址** | 发送确认电子邮件时要使用的电子邮件地址。 |

3. 选择 **保存**。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
