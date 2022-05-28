---
title: 员工使用员工自助服务选择计划（可选）
description: 本主题介绍员工如何选择或更新福利。
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 68aa401487a74b9fcd186ec6cbdb268cdb41168c
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743477"
---
# <a name="employees-select-plans-by-using-employee-self-service-optional"></a>员工使用员工自助服务选择计划（可选）


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

当新员工被雇用或发生生活事件时，员工可以在开放登记期间使用 **员工自助服务** 选择或更新他们的福利。

要访问福利进行登记，员工需要转到 **员工自助服务**，然后在 **福利** 磁贴上选择 **福利自助服务**。

在 **福利自助服务** 页面上，福利计划按计划类型分组。 要查看计划类型中的福利计划，员工在 **员工福利** 页面上选择一个磁贴。 员工将只看到他们有资格享受的福利。

> [!IMPORTANT]
> 必须先进行配置，计划类型才会在 **员工自助服务** 中显示。 有关详细信息，请参阅[配置员工自助服务](/dynamics365/human-resources/hr-benefits-setup-employee-self-service)。

根据计划类型，可以选择一项或多项福利进行登记。 例如，医疗计划类型可能被配置为将员工限制为一个医疗计划。 人寿保险计划类型可能允许员工选择多个人寿保险计划。

在员工决定登记哪个计划后，他们可能需要选择依赖方。 如果员工选择了 **员工 +1**、**员工 + 子女** 或 **家庭** 覆盖范围选项，则必须选择依赖方。 有关覆盖范围选项的详细信息，请参阅[创建覆盖范围选项](/dynamics365/human-resources/hr-benefits-setup-coverage-options)。

要选择福利计划，员工需要选择省略号按钮 (**...**) 或 **添加到购物车**。 员工将所有福利选择添加到购物车后，选择 **查看购物车**。 然后，员工会进入 **计划** 页面，在那里他们可以查看他们选择和放弃的福利计划。

员工必须先选择 **我同意** 选项，然后才能选择 **结帐** 按钮。 出现在 **我同意** 选项右侧的声明可以在 **人力资源共享参数** 页面的 **福利管理** 选项卡上进行自定义。

当员工使用 **员工自助服务** 确认他们的福利计划选择时，这些选择会被记录并显示在 **工作人员福利计划** 和 **工作人员福利计划批量更新** 页。

员工选择计划后，福利的状态将显示为 **已选择**。 当员工在 **福利自助服务** 页面选择 **结帐** 时，**结帐** 选项将被选中。

> [!IMPORTANT]
> 要完成登记，福利管理员必须为每个选定的员工福利选择 **确认**。 可以在 **工作人员福利计划** 或 **工作人员福利计划批量更新** 页面上完成确认。
>

员工无需使用 **员工自助服务** 选择福利。 可以在 **工作人员福利计划** 或 **工作人员福利计划批量更新** 页面上代表员工选择福利。 在福利管理员确认之前，不会完成员工在这些福利中的登记。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
