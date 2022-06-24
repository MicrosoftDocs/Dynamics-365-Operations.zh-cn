---
title: 准备付款
description: 本文说明如何在 Dynamics 365 Human Resources 中将员工标记为准备付款。
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 81c73584e3567d620292227ce4a24c3c0945fa96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862850"
---
# <a name="ready-to-pay"></a>准备付款


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> 如果您希望将员工标记为准备付款，您必须首先在功能管理中启用 **(预览版)工资单集成** 功能。 有关启用预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

此功能使人力资源专业人员能够了解哪些员工已准备好进行工资单处理，哪些员工需要在第三方工资单提供商使用之前执行操作。

## <a name="mark-employee-as-ready-to-pay"></a>将员工标记为准备付款

收集和验证员工信息既耗时又容易出错。 通过为人力资源专业人员提供一种查看和轻松更新员工信息的方式，Dynamics 365 Human Resources 可以帮助减少准备处理工资单所花费的时间。

将员工标记为准备付款：

1. 打开 **薪酬管理**。 工作区中有两个磁贴： 
    - **员工准备付款**
    - **员工未准备好支付**
    ![薪酬管理工作区。](./media/hr-ready-to-pay-1-workspace.png)

2. 选择 **员工未准备好付款** 磁贴。

3. 选择要验证的员工。 在 **工资单** 选项卡上，在 **准备付款** 组中，选择 **验证**。
    ![验证员工。](./media/hr-ready-to-pay-2-validate.png)

4. 要查看结果，在 **工资单选项卡** 上，在 **准备付款** 组中选择 **结果**。

## <a name="validation"></a>验证

在将员工标记为准备支付之前，将验证员工个人资料的完整性。

![验证结果。](./media/hr-ready-to-pay-3-results.png)

| 验证 | 明细 |
| --- | --- |
| **地址用途参数** | 确认已选择 **使用工资单地址用途** 参数。 |
| **工资单地址** | 确认工作人员个人资料至少有一个地址具有 **工资单居住地址** 或 **工资单工作地点** 用途，以及每个用途只有一个地址。 |
| **雇用** | 确认工作人员至少有一个雇用（当前、以前或将来）。 |
| **身份证号** | 确认 **在处理工资单时使用标识类型** 字段在 **人力资源参数** 页上为 **是**，以及参数中指示的身份证明类型已在工作人员个人资料中填充。 |
| **姓名** | 确认字段 **名字** 和 **姓氏** 已填写。|
| **位置编号** | 确认工作人员已被分配职位。 |
| **出生日期** | 确认 **生日** 字段已填充。 |
| **薪酬** | 确认工作人员已在固定薪酬计划中登记。 |

如果其中一项验证失败，则无法将员工标记为准备付款。

如果 **准备付款** 字段为 **否**，则指示您必须执行操作以确保工作人员个人资料完整。 这不会停止在任何数据实体中公开的数据。 

## <a name="process-automation"></a>流程自动化

您可以使用[流程自动化](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation)自动验证所有员工。 在 **薪酬管理** 工作区中，转到 **链接**\>**参数**\>**流程自动化**。

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
