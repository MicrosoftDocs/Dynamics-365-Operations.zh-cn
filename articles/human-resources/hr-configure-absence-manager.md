---
title: 配置缺勤管理人员角色
description: 本主题说明如何设置缺勤管理人员角色以管理员工休假。
author: hasrivas
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 050874628388629569751afae201ef346af020da09c81d24a69e1a4b5eb41b6f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732337"
---
# <a name="configure-the-absence-manager-role"></a>配置缺勤管理人员角色

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

在某些组织中，人事经理可能不会管理团队的休假。 而是可能由缺勤管理人员跨多个部门和团队管理团队成员的这个流程。 缺勤管理人员能够进行以下休假管理：

- 基于替代层次结构审查和审批休假。
- 查看团队成员余额。
- 查看缺勤日历。

## <a name="turn-on-the-feature"></a>开启功能

1. 在 **系统管理** 工作区，选择 **功能管理**。

2. 在 **功能管理** 选项卡上，启用 **(预览)管理休假的缺勤管理人员** 功能。

## <a name="define-a-custom-hierarchy"></a>定义自定义层次结构

缺勤管理人员功能使用必须配置的自定义层次结构。

1. 在 **组织管理** 工作区中，选择 **职位层次结构类型**。

2. 创建名为 **休假** 的职位层次结构类型。

3. 在 **休假和缺勤** 工作区中，在 **链接** 下选择 **休假和缺勤参数**。

4. 在 **常规** 选项卡上的 **缺勤层次结构** 下拉列表中，选择您之前创建的 **休假** 层次结构类型。 对于将使用缺勤管理人员功能的每个法人，都必须完成此休假层次结构关联。

定义层次结构类型后，必须将职位层次结构下属分配给职位。

1. 在 **组织管理** 工作区中，选择 **所有职位**。

2. 选择要向其添加休假层次结构的职位。

3. 在 **关系** 选项卡上，选择 **添加**。

4. 在 **层次结构名称** 字段中，选择 **休假**。

5. 在 **直接上级职位** 字段中，选择一个职位。 在您选择职位后，将自动填充工作人员姓名。

## <a name="assign-the-absence-manager-role-to-a-user"></a>将缺勤管理人员角色分配给用户

必须向员工分配缺勤管理人员角色，他们才能够批准或拒绝休假请求。

1. 在 **系统管理员** 工作区中，选择 **链接**。

2. 在 **用户** 部分，选择 **用户** 链接。

3. 在用户列表中，选择要向其分配缺勤管理人员角色的用户。

4. 在 **用户的角色** 选项卡上，选择 **分配角色**。

5. 在列表中，选择 **缺勤管理人员** 角色。 然后选择 **确定**。

    > [!IMPORTANT]
    > 请确保已将员工角色分配给您向其分配缺勤管理人员角色的用户。 否则，该工作人员将无法使用此功能。

6. 创建休假层次结构后，您可以按照以下步骤查看层次结构：

    1. 在 **组织管理** 工作区中，选择 **职位层次结构**。
    
    2. 在 **层次结构类型** 字段中，选择 **休假**。

## <a name="absence-manager-workspace"></a>缺勤经理工作区

在 **员工自助服务** 工作区中，**休假管理** 选项卡显示在休假层次结构中被分配了缺勤管理人员的员工的缺勤信息。 缺勤管理人员可使用一些选项： 
 - 查看休息时间请求。</br>
 - 代表员工提交休假请求。</br>
 - 查看作为休假层次结构的一部分分配给他们的所有员工。</br>
 - 查看缺勤管理人员日历。</br>

在 **休假管理** 工作区上，有两个选项卡：
 - **休假请求**：此选项卡将列出缺勤管理人员可以审核的所有挂起的休假请求。 缺勤管理人员可以选择多个记录并同时对其执行操作。 如果启用跨公司休假视图，则此列表将显示他们有权访问的所有法人的挂起休假请求。 否则，它将显示当前所选法人的待定休假请求。 </br>
 - **所有员工**：此选项卡将列出在休假层次结构中分配给缺勤管理人员的所有员工。 每个员工都可以使用一些选项：
    - **请求休假** - 为所选员工提交新的休假请求。</br>
    - **休假** – 查看所选员工的余额、已批准的休假和休假请求。</br>

## <a name="approve-time-off-requests"></a>批准休假请求

缺勤管理人员可以批准或拒绝员工的休假请求。 

> [!IMPORTANT]
> 必须先将休假请求工作流配置为将休假请求工作项目分配给缺勤管理人员进行审查，然后缺勤管理人员才能够批准或拒绝休假请求。
>
> 1. 在 **人力资源工作流** 页上，选择或创建休假请求工作流。
> 2. 选择 **关联层次结构** 选项，然后在 **层次结构名称** 字段中选择 **休假**。
> 3. 更新工作流设计器中的工作流。 在 **分配类型下**，选择 **层次结构** 选项，然后在 **层次结构选择** 选项卡上选择 **可配置的层次结构**。
>
> 有关如何创建休假请求工作流的信息，请参阅[创建休假请求工作流](hr-leave-and-absence-workflow.md)。

1. 在 **员工自助服务** 工作区中，选择 **休假管理** 选项卡。

2. 在 **休假请求** 选项卡上，选择要对其执行操作的休假请求。 您可以在此列表视图中选择多个记录。

3. 使用网格顶部的操作按钮审核、拒绝或委托休假请求。 

或者，用户还可以使用左边的 **休假请求** 磁贴导航到所有休假请求工作项的列表。 

## <a name="view-time-off-in-the-calendar"></a>在日历中查看休假

缺勤管理人员角色的用户可以在日历中查看休假请求。 按照以下步骤访问休假日历。

> [!IMPORTANT]
> 系统管理员必须为缺勤管理人员日历配置视图选项。 在 **休假和缺勤参数** 页上的 **日历** 选项卡上，存在隐藏或显示生日、无详细信息缺勤、休假和待处理休假请求的选项。 还有一个选项可以按工作人员类型筛选日历视图选项。

1. 在 **员工自助服务** 工作区中，选择 **休假管理**，然后选择 **缺勤管理人员日历**。

2. 在 **日期** 字段中，输入所需日期。

3. 根据需要更新视图选项。

缺勤管理人员日历显示在休假层次结构中向缺勤管理人员报告工作的员工的所有记录。

## <a name="see-also"></a>请参阅

- [休假和缺勤概览](hr-leave-and-absence-overview.md)
- [创建休假申请工作流](hr-leave-and-absence-workflow.md)
- [查看团队和公司日历](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]