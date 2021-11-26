---
title: 创建休假请求工作流
description: 在 Dynamics 365 Human Resources 中创建休假和缺勤请求工作流以一致地管理休假请求。
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8030e568ac8ef47d8383f09e06ce02a62947698
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728630"
---
# <a name="create-a-leave-request-workflow"></a>创建休假请求工作流

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您可以在 Dynamics 365 Human Resources 中创建工作流来一致地管理休假和缺勤请求。 **休假和缺勤** 工作流可让您：

- 定义任务
- 确定谁必须完成任务
- 指定谁可以批准或拒绝请求

## <a name="create-a-leave-and-absence-request-workflow"></a>创建休假和缺勤请求工作流

1. 在 **休假和缺勤** 页面，选择 **链接** 选项卡。

2. 在 **设置** 下，选择 **人力资源工作流**。

3. 选择 **新建**，然后选择 **休假和缺勤请求**。 

4. 当 **打开此文件?** 消息框出现时，选择 **打开** 并使用您的公司凭据登录。

5. 使用工作流编辑器为休假请求创建工作流。 有关使用工作流的详细信息，请参阅[创建工作流概述](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>休假和缺勤请求工作流数据元素

您可以使用以下数据元素在工作流中为休假和缺勤请求创建条件或自动审批：

- **金额**
- **注释**
- **公司**
- **创建人**
- **创建日期和时间**
- **结束日期**
- **休假类型**
- **修改者**
- **修改日期和时间**
- **原因代码**
- **请求 ID**
- **开始日期**
- **状态** 
- **提交日期**
- **提交者**
- **由人力资源部门提交**
- **由经理提交**
- **作为代表提交**
- **工作线程**
- **工作人员类型**

这些示例说明如何使用以下数据元素创建不同类型的工作流条件：

- 在条件语句中使用 **原因代码** 将病假请求和原因代码 **外科** 一起发送给 HR 审批，同时将所有其他原因代码发送给经理。 有关条件语句的更多信息，请参阅[配置工作流中的条件判定](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md)。 

- 在自动操作中使用 **由人力资源部门提交** 和 **由经理提交**，以自动批准这些角色代表员工提交的休假请求。 有关自动操作的更多信息，请参阅[配置工作流中的批准流程](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md)。

- 在条件语句或自动操作中使用 **休假类型**，以控制工作流如何传送特定休假类型的请求。

## <a name="see-also"></a>请参阅

- [休假和缺勤概览](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
