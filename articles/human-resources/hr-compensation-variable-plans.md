---
title: 创建可变薪酬计划
description: 本文介绍在使用可变薪酬和在可变薪酬计划中登记员工前必须设置的组件。
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan, HcmCompensationWorkspace
audience: Application User
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f2f51a095a23b651dca645b14e652519f20037e2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070549"
---
# <a name="create-variable-compensation-plans"></a>创建可变薪酬计划


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

可变薪酬构成员工的非常规薪酬，例如奖金或股票奖励。 本文说明如何设置可变薪酬所需的组件并在可变薪酬计划中登记员工。

员工的可变薪酬金额计算可以基于若干因素，例如员工的绩效、员工的薪酬级别以及部门的绩效。

## <a name="variable-compensation-components"></a>可变薪酬组件
### <a name="create-compensation-types"></a>创建薪酬类型

**可变薪酬类型** 为必需组件。 **可变薪酬类型** 描述您的组织奖励的可变薪酬。 它们还可以指定薪酬是现金或是非货币形式，如股票。

### <a name="describe-vesting-rules"></a>介绍股份行权规则

公司可以有选择地设置 **股份行权规则**。 **股份行权规则** 描述如何随着时间的推移分配可变奖励。 例如，股份行权规则可能规定，未来四个年度员工每年将得到总奖励的 25%。 股份行权规则仅供参考。

## <a name="variable-compensation-plans"></a>可变薪酬计划
**可变薪酬计划** 包含规则、计算方法和登记员工的可变薪酬计算的默认值。 在您创建某一可变薪酬计划时，必须设置可变薪酬类型。 可变薪酬类型确定系统将计算币种金额还是单位数量作为奖励。 

**限制对所选角色的访问** 参数将对薪酬计划的访问权限限制为在 Human Resources 中分配给该计划的所选安全角色。 例如，当您创建面向高管并且不应对所有 HR 特定角色可见的薪酬计划时，您可以使用此参数限制对这些薪酬计划的访问权限。 

还必须设置计算方法：

-   **时间点** – 可变奖励的计算基于员工在特定日期的固定薪酬。 该日期在处理新薪酬金额时的流程事件中指定。
-   **组合** – 奖励金额基于员工在流程事件中周期开始日期和周期结束日期之间的每个固定薪酬付薪比率而计算。 然后合计费率以确定最终奖励。 例如，在周期中，员工转岗到具有不同付薪比率的不同职位。 在这种情况下，可变奖励为员工具有每个付薪比率的时间长度进行调整。

可变奖励金额可以基于员工定期基本收入或固定数量的单位。

-   选择 **基数百分比** 选项可输入默认百分比，并指定基数是否应为员工的固定付薪比率或员工薪酬l级别的控制点。 薪酬级别在员工工作中设置。 薪酬结构的一个参考点可以在固定薪酬计划中设置为控制点。 将使用来自员工工作的薪酬级别，并将其与在员工固定薪酬计划中列出的控制点相互参考，以查找员工薪酬级别的控制点金额。 控制点金额（而不是员工的固定付薪比率）然后将用作奖励基础。
-   选择 **单位数量** 选项输入默认的单位数量，每单位的值和单位值的币种，如果薪酬计划用于非现金奖励（例如，价值 40 美元的 200 个存货单位），或者只是单位数量，如果薪酬计划用于现金奖励。 对于现金奖励，该员工将收到指定的用于固定薪酬计划的币种的单位数量（例如，1 美元 500 个单位）。 该一对一关系控制可用于指示单位数量和单位值之间是否存在直接的一对一映射。 在通过使用单位数量创建一个基于现金的计划的可变薪酬计划时，此选项将被自动锁定为 **是**，并且单位值是 **1.0000**。

**雇用规则** 设置指定是否所有员工均应接收相同的增加，而与其雇用日期无关（**雇用规则**  =  **无**），还是基于员工在周期内被雇用的时长，员工应接收奖励百分比（**雇用规则**  =  **百分比**）。 

**杠杆** 基于员工部门的绩效调整员工的奖励。 绩效指标可以在 **部门** 页上为每个部门设置，在 **相关窗体** &gt; **薪酬** &gt; **绩效** 下。 该部门的员工获得的奖励取决于 **实现的目标的百分比** 字段的值，此值指示部门的绩效：

-   如果部门的绩效是 100%，该部门员工的奖励由在 **100% 时的付出比率** 字段中设置的百分比作为考虑因素。
-   如果部门的绩效超过 100%，系统会将在 **高于目标时按 1%** 字段中设置的百分比加到在 **100% 时的付出比率** 字段中设置的百分比，直到达到在 **允许的最高付出比率** 字段中设置的值。
-   如果部门的绩效少于 100%，系统会将在 **低于目标时按 1%** 字段中设置的百分比从在 **100% 时的付出比率** 字段中设置的百分比中减去，直到达到在 **允许的最低付出比率** 字段中设置的值。

可以在阈值百分比中设置 **容差级别**，以便当杠杆导致百分比超过阈值百分比时显示警告消息。 

默认情况下，在员工职位中设置的部门用于员工奖励。 不过，某些员工的奖励可能取决于多个部门的绩效。 在这种情况下，不同部门和分配给每个部门的奖励的百分比可以在员工的可变薪酬登记中设置。 有关详细信息，请参阅随后的“可变薪酬登记”部分。 

杠杆仅用于在薪酬流程运行时选择 **绩效付薪体系** 的情况。 

**级别覆盖** 选项卡可以基于员工的薪酬级别覆盖奖励的值默认百分比或单位数量。 如果在可变薪酬计划中登记的员工的 **启用级别覆盖** 设置为 **是**，会将员工工作中的级别与级别替代表进行比较来确定该级别的百分比或单位数量。 。如果该级别在级别覆盖表中未找到，将使用 **常规** 选项卡的默认百分比或单位数量。 百分比和单位数量也可以在可变薪酬计划的员工登记中被覆盖。

## <a name="variable-compensation-enrollment"></a>可变薪酬登记
### <a name="determine-who-is-eligible-for-the-plan"></a>确定谁适用于计划

在您准备好在可变薪酬计划中登记员工时，第一步是确定适用于在计划中指定的薪酬的员工。 除非您确定资格，否则您无法将计划分配到任何员工。 若要设置资格，请打开 **资格规则** 页以创建您的计划的新资格规则，然后定义员工必须满足才有资格享受薪酬计划的条件。 您可以按部门、工会、薪酬区域（位置）、工作、工作职能、工作类型和/或薪酬级别限制资格。 只有当员工满足在资格规则中设置的 **所有** 条件时，他们才能在薪酬计划中登记。 

**注意：** 资格规则确定固定薪酬计划和可变薪酬计划的资格。 资格规则在工作、职位和员工记录中使用以下字段来确定某员工是否有资格享受薪酬计划：

- 在 **工作** 页上：
  -   **工作** 字段
  -   **工作分类** 选项卡上的 **职能** 和 **工作类型** 字段
  -   **薪酬** 选项卡上的 **级别** 字段
- 在 **职位** 页上：**部门** 和 **薪酬区域** 字段
- 在 <strong>员工</strong>页上：*<strong><em>工作人员</em></strong>* 选项卡上<strong>个人信息</strong> &gt; <strong>工会</strong>下的有关与员工关联的工会的信息

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>启用可变薪酬计划登记

在 **可变薪酬计划** 页上，设置 **启用登记** 选项为 **是** 可允许有资格的员工在计划中登记。

### <a name="enroll-the-employee"></a>登记员工

您现在可以在可变薪酬计划中登记员工。 若要登记某一员工，请转到 **员工** 页，然后选择该员工。 然后，在操作窗格中单击 **薪酬** &gt; **可变计划登记**。 

**注意：** 在可变薪酬计划中 **登记** 必须设置为 **是**。 **计划** 字段只显示员工有资格享受的计划，基于为这些计划设置的资格规则。 如果资格规则没有为计划设置，将没有员工适用于该计划。 

确保正确设置 **生效日期** 字段。 如果可变薪酬计划使用 **组合** 计算方法，该登记的生效日期可能在员工奖励的计算时考虑。 

您可以使用 **覆盖** 选项卡覆盖员工的特定值。 例如，如果在计划中 **雇用规则** 设置为 **百分比**，并且在计算员工的雇用百分比时应使用不同的雇用日期，您可以在 **雇用规则日期** 字段中设置雇用日期。 您还可以根据计划的设置替代特定员工的 **奖励百分比** 值或 **单位数量** 值。 这些值将作为计划中雇用规则、绩效系数和其他设置考虑的因素。 

**组织覆盖** 用于基于一个或多个部门的绩效确定员工的奖励。 在部门之间分摊的百分比总计应等于 100。 员工的个人绩效也会考虑在内。 这些设置仅用于在薪酬流程运行时选择 **绩效付薪体系** 的情况。





[!INCLUDE[footer-include](../includes/footer-banner.md)]
