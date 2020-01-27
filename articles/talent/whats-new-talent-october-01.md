---
title: Dynamics 365 Talent - Core HR（2018 年 10 月 1 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
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
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f872b0907e0f48e0b734c87f0b8fb1a4cfe20cb0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896673"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-1-2018"></a>Dynamics 365 Talent: Core HR（2018 年 10 月 1 日）中的新增功能或更改

**内部版本 8.1.1035.0**

此主题介绍了 Core HR 中的新增功能和更改的功能。

## <a name="turn-off-electronic-payment-validation"></a>关闭电子付款验证

如果通过**员工自助服务**工作区 (ESS) 或直接在员工窗体上为直接存款设置付款，将进行电子付款信息验证。 此选项让您在不需要对金额和剩余数量值进行验证检查时灵活地去除验证。 如果要与具有不同要求的外部工资系统集成，此功能非常有用。

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>经理自助服务 - 通过“团队绩效目标”磁贴为团队成员添加目标

在此版本之前，经理可通过与各员工关联的绩效目标分别向员工添加目标。 通过此更新，经理可访问**团队绩效目标**磁贴并通过选择直接报告新建目标。

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>经理自助服务 - 通过“团队绩效审核”磁贴为团队成员添加审核

在此版本之前，经理可通过与各员工关联的审核分别向员工添加审核。 通过此更新，经理可访问**团队绩效审核**磁贴并通过选择直接报告新建审核。

## <a name="configure-proration-options-by-leave-plan"></a>根据离职计划配置按比例分配选项

组织根据员工加入和离开公司的时间以不同的方式奖励休假。 某些组织的员工从加入公司时即开始全额享受奖励，而其他组织的员工则按比例享受奖励。 此版本中提供了新选项，用于选择如何为加入组织的人员和离开组织的人员按比例分配奖励和进行累积。 选项包括：“按比例分配”、“完全累积”和“不累积”。

## <a name="other-changes"></a>其他更改

-   员工实体更新 - 现在可使用 Excel 加载项/数据管理更新**人员**磁贴。

-   安全更改中允许删除员工自助服务中有关付款信息的**删除**和**停用**按钮。

## <a name="known-issue"></a>已知问题

-   **问题：** 向工作人员添加新附件时，**新建**和**编辑**按钮灰显。**解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。 如果加载**工作人员**页面时速见表已关闭，将启用**附件**按钮。 （下一个平台更新中将解决这个问题。）
