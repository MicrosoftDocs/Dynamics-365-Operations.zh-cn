---
title: Dynamics 365 Human Resources（2020 年 2 月 12 日）中的新增功能或更改
description: 本文介绍 2020 年 2 月 12 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d772361f6ff0d01fb5061b6c6d35fbf83f8378beef19225b5b5d9196dfd0a44
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759785"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Dynamics 365 Human Resources（2020 年 2 月 12 日）中的新增功能或更改

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.2867。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>现有实体 CompFixedEmpls 和 HcmPersonImage 应该从 OData 访问 (414178)

本周发布后，**CompFixedEmpls** 和 **HcmPersonImage** 实体现在已公开，可通过 ODAta 获取。

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>雇用详细信息无效后无法从 Dataverse 删除雇用 (403193)

此更改现在允许当存在无效雇用详细信息时通过 Dataverse 删除雇用。

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>课程等记工作流将状态更改为已完成，并在二次批准后出错 (409749)

课程等记工作流已更新为允许多次批准。

## <a name="in-preview"></a>预览模式

以下预览功能于 2020 年 2 月 3 日可用：

- **休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。

- **福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。

## <a name="coming-soon"></a>即将推出

### <a name="platform-update-32"></a>平台 update 32 

平台更新 32 即将推出。 [在此处发现有关平台更新 32 的详细信息](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md)。

### <a name="updated-dataverse-solution"></a>更新的 Dataverse 解决方案

一个新的 Dataverse 解决方案很快将推出，其中包含以下更改：

| 说明 | 找零 |
| ----------------------------------------- | --- |
| **工作/职位** 实体更改 | 添加了 **薪酬区域**</br>添加了 **财务维度** |
| **工作人员** 实体更改 | 添加了 **姓名顺序**</br>添加了 **在家工作**</br>添加了 **语言**</br>添加了 **受聘日期**</br>添加了 **周年纪念日日期**</br>添加了 **原始雇用日期** |
| **雇用** 实体更改 | 添加了 **财务维度**</br>添加了 **离职原因**</br>**转变日期** 重命名为 **离职日期**</br>添加了 **试用日期** |
| **工作人员地址** 实体更改 | 添加了 **街道地址**</br>**地址行 1**、**地址行 2** 和 **地址行 3** 标为弃用 |
| 新的可变薪酬设置实体 | **可变薪酬计划类型**</br>**薪酬可变计划**</br>**股份行权规则**</br>**可变薪酬计划级别** |
| 新 **工作人员日历雇用** 实体 | 添加了 **工作日历实体** |
| 新 **工资单职位详细信息** 实体 | 添加了 **工资单职位详细信息** |
| 新 **职务** 实体 | 添加了 **职务**。 Human Resources 与 Dataverse 之间的同步流程中将包含新的 **职务** 实体。 其最初不是从 **工作职位** 或 **工作** 实体引用的。 |

## <a name="see-also"></a>请参阅

[Human Resources 新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]