---
title: 工资单职位工作
description: 本主题提供 Dynamics 365 Human Resources 中工资单职位工作实体的详细信息和示例查询。
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72f3109f5bea36a390b04b7165fc3831d777b640
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881936"
---
# <a name="payroll-position-job"></a>工资单职位工作

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题提供 Dynamics 365 Human Resources 中工资单职位工作关系实体的详细信息和示例查询。

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **工作 ID**<br>mshr_jobid<br>*字符串* | 只读<br>必填 |工作的 ID。 |
| **生效日期**<br>mshr_validto<br>*日期/时间偏移* | 只读 <br>必填 | 职位和工作关系有效的开始日期。 |
| **失效日期**<br>mshr_validto<br>*日期/时间偏移* | 只读 <br>必填 | 职位和工作关系有效的结束日期。  |
| **职位 ID**<br>mshr_positionid<br>*字符串* | 只读<br>必填 | 职位的 ID。 |
| **主要字段**<br>mshr_primaryfield<br>*字符串* | 必填<br>系统生成的 |  |
| **职位工作 ID 值**<br>_mshr_fk_positionjob_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_payrollpositionjobentity 的 mshr_PayrollPositionJobEntity |与职位关联的工作的 ID。|
| **固定薪酬计划 ID 值**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | 只读<br>必填<br>外键：mshr_payrollfixedcompensationplanentity 的 mshr_FixedCompPlan_id  | 与职位关联的固定薪酬计划的 ID。 |
| **工资单职位工作实体 ID**<br>mshr_payrollpositionjobentityid<br>*GUID* | 必填<br>系统生成。 | 系统生成的用于唯一标识工作的 GUID 值。  |

