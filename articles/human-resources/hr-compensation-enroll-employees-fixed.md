---
title: 在固定薪酬计划中登记员工
description: 薪酬福利经理可以指派不同雇员不同的固定薪酬计划以确定其各自的基本工资。
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d611f2631a59fbe1e131e82ca9937a5adaaf2ebd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688732"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>在固定薪酬计划中登记员工


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

薪酬福利经理可以指派不同雇员不同的固定薪酬计划以确定其各自的基本工资。 此程序假设已经创建了一个有效的固定薪酬计划，且该计划的资格规定也已经设置完成。 创建此程序的演示数据公司是 USMF。 启动该程序，请转到 **人力资源** > **工作人员** > **雇员** > **薪酬** > **固定计划**。

1. 单击 **新建**。
2. 在 **操作** 字段中，选择一个“固定薪酬”操作类型 **雇用 / 再雇用**，说明雇员薪酬的变化。
3. 在列表中，单击所选行中的链接。
4. 在 **职位** 字段中，单击下拉按钮以打开查找。
5. 在列表中，单击所选行中的链接。
    * 显示的级别来自分配给 **职位** 的 **工作** 的 **薪酬** 快速选项卡 > **级别** 字段。 该工作标准必须在付给雇员薪酬之前设置。  
6. 在 **计划** 字段中，为该雇员选择“固定薪酬计划”。 **计划** 查找仅显示经过筛选后固定薪酬计划符合 **资格规则** 的员工。
7. 在列表中，找到并选择所需记录。
    * 薪酬 **生效日期** 与 **截止日期** 默认为指派工作人员职位的开始日期与结束日期。 可以根据需要更改相关日期。  
    * 如果该雇员的“固定薪酬计划”是一步计划，则选择包含相应工资标准的薪酬阶梯。 如果该雇员的固定薪酬计划是根据等级或期间设置，输入其工资标准。 该工资标准将验证该薪酬计划设置的可行性程度，以及该工作薪酬水平的最小和最大参考值。  
8. 单击 **确定**。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
