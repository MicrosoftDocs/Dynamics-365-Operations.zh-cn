---
title: 配置 Human Resources 参数
description: 本主题说明如何在 Dynamics 365 Human Resources 中设置特定于公司的参数。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c4c93e3d2644a380e3d5d2247961a8b6fb34568
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052401"
---
# <a name="configure-human-resources-parameters"></a>配置 Human Resources 参数

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

某些人力资源参数的设置在公司间共享，而其他参数设置是特定于公司的。 本主题说明如何设置特定于公司的人力资源参数。

提供了两个页面来设置人力资源参数。 对于跨公司共享的参数，您可使用 **人力资源共享参数** 页。 对于特定于公司的参数（换句话说，这些设置将应用于单个公司），您可使用 **人力资源参数** 页。

![转到“人力资源参数”](./media/hr-employee-self-service-human-resources-parameters.png)

在 **人力资源参数** 页上，设置在 6 个选项卡之间分配：

- **常规**
- **招聘**（此选项卡不包括在 Dynamics 365 Human Resources 中）
- **薪酬**
- **编号规则**
- **FMLA**
- **员工自助服务**
- **经理自助服务**
- **福利管理**
- **休假和缺勤**
- **付款方式**

每个选项卡均包含与单个公司有关的信息。

## <a name="general"></a>常规

**常规** 选项卡上的设置定义有关缺勤、伤害和疾病以及新的雇用的信息的外观。 此选项卡上的设置还定义在您工作时显示的某些默认条目。 具体来说，此选项卡可让您：

- 选择要应用于未结的缺勤事务的颜色
- 指定用于报表的样式表
- 启用培训课程和缺勤登记之间的集成
- 选择用于控制此集成的缺勤代码。
- 指出保留伤害和疾病案例事件的时间。
- 指定雇用新工作人员时显示的默认标识号。

![常规选项卡](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>招聘

**招聘** 选项卡上的设置定义用于自动发送给申请人的通信的文档类型。 您还可以指出用于主动提供的申请的招聘项目。

为招聘项目帐龄定义的期间确定包含在 **招聘管理** 工作区中的 **帐龄项目** 磁贴上的招聘项目。 为申请截止日期警告定义的期间用于显示接近其在 **招聘** 工作区中的 **接近申请截止日期** 磁贴上的申请截止日期的招聘项目。

有关招聘的详细信息，请参阅[招聘工作应聘者](hr-personnel-recruit.md)。

## <a name="compensation"></a>薪酬

在 Dynamics 365 Finance 中，**薪酬** 选项卡上的设置定义用户是否必须确认是希望保存固定薪酬计划的信息还是可变薪酬计划的信息。 如果您选择 **启用保存验证**，当用户关闭与薪酬相关的页面时，他们将收到一条消息，询问是否需要保存记录。 薪酬管理中的某些页面不允许用户删除信息。 通过提示用户验证是否要保存信息，您也许能够限制可保存但稍后无法删除的信息量。 如果清除 **启用保存验证**，将立即保存记录（可能在用户准备就绪之前）。 如果您使用绩效管理，则也可使用 **薪酬** 选项卡来选择要使用的评级模型，而不是选择在对绩效进行评级时分配给薪酬计划的模型。

在 Human Resources 中，您可以使用 **薪酬** 选项卡选择限制对薪酬计划的访问和设置默认货币。

有关薪酬的详细信息，请参阅[薪酬计划概述](hr-compensation-overview.md)。

![“薪酬”选项卡](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>编号规则

**编号规则** 选项卡上的设置确定用于为 Human Resources 中的项目自动分配 ID 的序列，如：

- 申请表
- 缺勤登记
- 薪酬流程结果
- 案例编号
- 课程
- 课程安排

要维护编号规则引用和代码，可使用 **编号规则** 列表页（选择 **组织管理 > 编号规则 > 编号规则**）。

有关详细信息，请参阅[编号规则概述](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)。

> [!NOTE]
> 工作的小时数不能超过 1,250，雇用时长不能超过 12 个月。 这些最大值符合美国的联邦法律。

![“编号规则”选项卡](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

在 FMLA 选项卡上，设置 FMLA 资格要求和 FMLA 权利时数。 有关详细信息，请参阅[配置休假和缺勤参数](hr-leave-and-absence-parameters.md)。

![FMLA 选项卡](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>员工自助服务

**员工自助服务** 选项卡上的设置会影响员工自助服务对员工的显示方式。 在此选项卡上，您可以：

- 为员工自助服务工作区输入名称
- 选择经理可以为员工输入的信息
- 为员工添加有用的链接
- 限制员工添加或编辑业务联系人详细信息。 有关详细信息，请参阅[限制对个人信息的编辑](hr-employee-self-service-restrict-editing.md)。

有关设置员工自助服务的详细信息，请参阅[员工和经理自助服务概述](hr-employee-manager-self-service-overview.md)。

![员工自助服务选项卡](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>经理自助服务

**经理自助服务** 选项卡上的设置会影响经理在经理自助服务中看到的内容。 在此选项卡上，您可以配置以下选项：

- 即将过期的记录的范围
- 经理可以在即将过期的记录中查看的信息
- 经理是否可以查看间接下属空缺职位
- 正离职的工作人员视图
- 对经理有用的链接

有关设置经理自助服务的详细信息，请参阅[员工和经理自助服务概述](hr-employee-manager-self-service-overview.md)。

![经理自助服务选项卡](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>福利管理

在“福利管理”选项卡上，您可以为“福利管理”配置电子邮件选项。 有关设置和使用福利管理的信息，请参阅[福利管理概述](hr-benefits-management-overview.md)。

![福利管理选项卡](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>休假和缺勤

有关设置和使用休假和缺勤的信息，请参阅[休假和缺勤概述](hr-leave-and-absence-overview.md)。

## <a name="payment-methods"></a>付款方式

在 **付款方式** 选项卡上，您可以选择组织支持的付款方式。 有关配置薪酬的详细信息，请参阅[薪酬计划概述](hr-compensation-overview.md)。

![付款方式选项卡](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]