---
title: Dynamics 365 Human Resources 中的新增功能或更改（2020 年 2 月 7 日）
description: 本文介绍 2020 年 2 月 7 日 Microsoft Dynamics 365 Human Resources 中的新增功能或更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ca740c9b839a08bdb8b426ff191bea64febcd15
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712078"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Dynamics 365 Human Resources 中的新增功能或更改（2020 年 2 月 7 日）

本文介绍 Dynamics 365 Human Resources 中的新增功能或更改的功能。 更改适用于内部版本号 8.1.2835。 某些标题中括号内的数字是 Microsoft Dynamics Lifecycle Services (LCS) 中的支持号码。

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>如果教室是空白的，学习分析不显示课程 (388289)

现在，如果教室是空的，学习分析页面将显示课程。

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>职位查找不考虑时区 (405344)

现在，在验证职位是否空缺时，对空缺职位的查找将考虑时区。

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>提交休息时间请求后，当前余额分析视图不使用正确的当前休假余额进行更新 (409756)

现在，当前余额包括已提交的休息时间请求。

## <a name="in-preview"></a>预览模式

以下预览功能于 2020 年 2 月 3 日可用：

- **休假和缺勤预览功能** - 有关详细信息，请参阅[休假和缺勤预览功能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)。

- **福利管理预览功能** - 有关详细信息（包括已知问题），请参阅[福利管理概述](hr-benefits-management-overview.md)。

## <a name="coming-soon"></a>即将推出

### <a name="platform-update-32"></a>平台 update 32 

平台更新 32 即将推出。 [在此处发现有关平台更新 32 的详细信息](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32)。

### <a name="updated-common-data-service-solution"></a>更新的 Common Data Service 解决方案

一个新的 Common Data Service 解决方案很快将推出，其中包含以下更改：

| 说明 | 找零 |
| ----------------------------------------- | --- |
| **工作/职位**实体更改 | 添加了**薪酬区域**</br>添加了**财务维度** |
| **工作人员**实体更改 | 添加了**姓名顺序**</br>添加了**在家工作**</br>添加了**语言**</br>添加了**受聘日期**</br>添加了**周年纪念日日期**</br>添加了**原始雇用日期** |
| **雇用**实体更改 | 添加了**财务维度**</br>添加了**离职原因**</br>**转变日期**重命名为**离职日期**</br>添加了**试用日期** |
| **工作人员地址**实体更改 | 添加了**街道地址**</br>**地址行 1**、**地址行 2** 和**地址行 3** 标为弃用 |
| 新的可变薪酬设置实体 | **可变薪酬计划类型**</br>**薪酬可变计划**</br>**股份行权规则**</br>**可变薪酬计划级别** |
| 新**工作人员日历雇用**实体 | 添加了**工作日历实体** |
| 新**工资单职位详细信息**实体 | 添加了**工资单职位详细信息** |
| 新**职务**实体 | 添加了**职务**。 Human Resources 与 Common Data Service 之间的同步流程中将包含新的**职务**实体。 其最初不是从**工作职位**或**工作**实体引用的。 |

## <a name="see-also"></a>请参阅

[Human Resources 新增功能或更改](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 发布第 2 波概述](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新流程](hr-admin-setup-update-process.md)</br>
[管理功能](hr-admin-manage-features.md)