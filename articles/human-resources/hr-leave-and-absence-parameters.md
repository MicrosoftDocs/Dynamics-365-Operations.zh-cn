---
title: 配置休假和缺勤参数
description: 在 Dynamics 365 Human Resources 中定义休假和缺勤的人力资源参数。
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 45f5ebfe7bd11a529e871f5fd3244577954534f5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794629"
---
# <a name="configure-leave-and-absence-parameters"></a>配置休假和缺勤参数

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

在您在 Dynamics 365 Human Resources 中设置休假和缺勤计划之前，最好先验证所有相关的人力资源参数的设置，包括：

- 休假请求的编号规则
- 家庭医疗休假法 (FMLA) 设置
- 休假和缺勤请求的员工自助服务设置
- 休假和缺勤参数

## <a name="view-and-change-human-resources-parameters"></a>查看和更改人力资源参数

1. 在 **休假和缺勤** 页面，选择 **链接** 选项卡。

2. 在 **设置** 下，选择 **人力资源参数**。

3. 在 **编号规则** 选项卡上，验证 **休假请求 ID** 的 **编号规则代码** 并根据需要进行更改。 此设置确定用于向休假请求自动分配 ID 的顺序。

4. 在 **FMLA** 选项卡上，验证 FMLA 设置并根据需要进行更改。

5. 在 **员工自助服务** 选项卡上，指示经理是否可以代表员工输入休假和缺勤请求。

7. 选择 **保存**。

>[!IMPORTANT]
>跨公司查看休假和缺勤当前处于预览状态。 您需要在 **沙盒** 环境中启用它以显示休假和缺勤的选项。 有关启用预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

## <a name="view-and-change-human-resources-shared-parameters"></a>查看和更改 Human Resources 共享参数

1. 在 **人事管理** 页面上，选择 **链接** 选项卡。

2. 在 **设置** 下，选择 **Human Resources 共享参数**。

3. 在 **高级访问** 选项卡上，针对 **启用跨公司休假查看** 选择 **是** 以允许跨公司查看休假。

4. 选择 **保存**。

## <a name="view-and-change-leave-and-absence-parameters"></a>查看和更改休假和缺勤参数

1. 在 **休假和缺勤** 页面，选择 **链接** 选项卡。

2. 在 **设置** 下，选择 **休假和缺勤参数**。

3. 在 **常规** 选项卡上，设置以下参数：
 
    - 将 **休假和缺勤单位** 设置为小时或天。 如果为天，则可以选择 **启用半天定义**，以便允许员工在休假请求中选择前半天或后半天。 

    - 选择 **服务生效日期的月份** 以设置使用服务月份的休假计划的假期额度费率生效时间。

    - 选择 **余额计算** 以显示截至今日的余额或应计期间的余额。 如果选择 **截至今日的余额**，则余额显示截止今日的所有应计、调整和请求的总计。 如果选择 **截至应计期间的余额**，则余额显示截止休假计划中的频率定义的应计期间所有应计、调整和请求的总计。 

    - 设置结转到期批处理作业的开始时间。  
    
    - 为 **允许员工购买休假** 和 **允许员工出售休假** 选择 **是**。 如果为这些选项选择 **是**，可以创建购买和出售休假策略，让员工能够提交购买和出售休假请求。

## <a name="configure-calendar-parameters"></a>配置日历参数

1. 在 **休假和缺勤** 页面，选择 **链接** 选项卡。

2. 在 **设置** 下，选择 **休假和缺勤参数**。

3. 在 **日历** 选项卡上，根据需要更改日历设置。

4. 选择 **保存**。

## <a name="see-also"></a>请参阅

- [休假和缺勤概览](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]