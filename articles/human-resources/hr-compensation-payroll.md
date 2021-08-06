---
title: 准备付款
description: 本主题说明如何在 Dynamics 365 Human Resources 中将员工标记为准备付款。
author: marcelbf
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f9aa9e60b51b1801c07981ad120cb77f65fee286
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/14/2021
ms.locfileid: "6560093"
---
# <a name="ready-to-pay"></a>准备付款

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> 如果您希望将员工标记为准备付款，您必须首先在功能管理中启用 **(预览版)工资单集成** 功能。 有关启用预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。

此功能使人力资源专业人员能够了解哪些员工已准备好进行工资单处理，哪些员工需要在第三方工资单提供商使用之前执行操作。

## <a name="mark-employee-as-ready-to-pay"></a>将员工标记为准备付款

收集和验证员工信息既耗时又容易出错。 通过为人力资源专业人员提供一种查看和轻松更新员工信息的方式，Dynamics 365 Human Resources 可以帮助减少准备处理工资单所花费的时间。

将员工标记为准备付款：

1. 打开 **薪酬管理**。 工作区中有两个磁贴 
    - **员工准备付款**
    - **员工未准备好支付**
    ![薪酬管理工作区。](./media/hr-ready-to-pay-1-workspace.png)

2. 选择 **员工未准备好付款** 磁贴。

3. 选择要验证的员工。 在 **工资单** 选项卡上，在 **准备付款** 组中，选择 **验证**。
    ![验证员工。](./media/hr-ready-to-pay-2-validate.png)

4. 要查看结果，在 **工资单选项卡** 上，在 **准备付款** 组中选择 **结果**。

## <a name="validation"></a>验证

在将员工标记为准备付款之前，系统将对个人资料的完整性进行基本验证。

![验证结果。](./media/hr-ready-to-pay-3-results.png)

下表提供了有关所执行的每个验证的信息。 

| 验证 | 明细 |
| --- | --- |
| 地址用途参数 | 验证参数 **使用工资单地址用途** 是否打开。 |
| 工资单地址 | 验证工作人员个人资料是否至少有一个地址具有“工资单居住地址”或“工资单工作地点”用途，以及每个用途是否只有一个地址。 |
| 雇用 | 验证工作人员是否至少有一个雇用（当前、以前或将来）。 |
| 身份证号 | 验证参数“在处理工资单时使用标识类型”是否为“是”，以及参数中指示的身份证明类型是否已在工作人员个人资料中填充。 |
| 姓名 | 验证工作人员个人资料是否有效，检查字段 **姓名** 和 **姓氏** 是否已填充。|
| 位置编号 | 验证工作人员是否已分配职位。 |
| 出生日期 | 验证工作人员个人资料是否有效，检查字段 **生日** 是否已填充。 |
| 薪酬 | 验证工作人员是否已在固定薪酬计划中登记。 |

如果其中一项验证失败，则无法将员工标记为准备付款。

如果 **准备付款** 字段为 **否**，则指示您必须执行操作以确保工作人员个人资料完整。 这不会停止在任何数据实体中公开的数据。 

## <a name="known-issues"></a>已知问题

- 您必须在功能管理中禁用 **简化的员工输入** 功能。 如果您使用此功能，薪酬管理工作区中的磁贴将无法正常工作。
- 在工作人员窗体中，**工资单选项卡** 上的 **准备付款** 组可用于任何用户角色。 

## <a name="see-also"></a>请参阅

[工资单集成 API 简介](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
