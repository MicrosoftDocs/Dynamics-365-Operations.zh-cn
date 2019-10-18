---
title: Dynamics 365 Talent（2019 年 2 月 14 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9f3fa269217bc03a15fde6ee0fc9d0c502c17b3e
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009114"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>Dynamics 365 Talent（2019 年 2 月 14 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

此主题介绍了 Talent 中的新增功能和更改的功能。

## <a name="changes-in-attract"></a>Attract 中的更改
此版本中包含一些小缺陷修复。

## <a name="changes-in-onboarding"></a>Onboarding 中的更改
此版本中包含一些小缺陷修复。
 
## <a name="changes-in-core-hr"></a>Core HR 中的更改 
**内部版本 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>员工固定薪酬实体无法导入所有记录
通过此更改，**员工固定薪酬**实体现在可以导入所有记录。 此实体可用于为员工创建固定薪酬记录和更新现有固定薪酬记录。 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>雇佣结束日期不遵守员工的首选时区设置
创建或终止与公司之间的雇佣时，雇佣结束日期现在遵守用户的首选时区。
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>英国地址在 Analytics 中显示为瑞士东部地区地址
在此版本中，已进行了更改来更正**人员管理**的“按位置分类的人数”报告中的地址不一致。
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>终止职位时工作人员职位分配记录中不填充离职代码
已进行了更改，现在终止员工职位分配时间默认采用“离职原因”代码。

### <a name="new-entity-created-for-job-compensation-levels"></a>为工作薪酬级别创建了新实体
已经创建了一个新的数据管理框架 (DMF) 实体。 提供该实体是为了为系统中定义的每个工作创建和更新薪酬级别、市场价值和调查信息。
