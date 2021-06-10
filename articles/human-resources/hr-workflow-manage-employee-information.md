---
title: 使用工作流管理员工信息
description: 本文说明如何使用人力资源的工作流功能管理员工信息。 例如，可以将工作流与职位关联，以及配置员工更改其记录时启动的批准工作流。
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: aba7627877cd9b79dce5930e528f892e2d80baac
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058744"
---
# <a name="use-workflows-to-manage-employee-information"></a>使用工作流管理员工信息

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本文说明如何使用人力资源的工作流功能管理员工信息。 例如，可以将工作流与职位关联，以及配置员工更改其记录时启动的批准工作流。

人力资源的工作流功能提供各种工作流，用于管理人力资源活动。 此外，有许多可用选项，所以您可以修改工作流并将其与申报层次结构关联。 提供工作流是为了帮助管理对多种标准员工信息类型的更改。 您可以将工作流与职位相关联。 然后，如果员工更改其员工记录，将在保存新信息之前启动要求批准的工作流。 为以下类型的信息预定义了工作流，帮助您有效管理更改和维护员工数据的精确性：

-   标识号
-   课程
-   教育程度
-   图像
-   借出物品
-   专业经验
-   项目经验
-   技能
-   诚信职位
-   人力资源行动
-   课程登记

员工受聘、转岗或退休后，工作流中可以包含审核流程。 可以按照这种方式修订票据，或将行为的条款定义为工作流的一部分。 审核流程完成时，将完成票据或行为，而工作流将进入最后的批准步骤。

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>将工作流与职位层次结构关联
您可以将工作流与您正在配置的任何层次结构关联。 例如，如果某一职位矩阵报告层次结构关联，您可以配置一个工作流，用于将特定项目的费用发送给项目主管，而不是与该职位关联的员工的经理。 若要创建新工作流或修改现有工作流，请在 **人力资源工作流** 页上，单击 **新建**。 选择列表中的工作流来启动工作流设计器。 可以使用该设计器创建新工作流或更改现有工作流中的步骤。 更改现有工作流时，更改保存为新版本。 因此，如有必要，始终可以恢复为以前的版本。

## <a name="configure-a-human-resources-workflow"></a>配置人力资源工作流
若要配置员工请求更改其个人身份时启动的基本工作流，请执行以下步骤。

1.  在 **人力资源工作流** 页中，单击 **新建**。
2.  在可用工作流列表中，选择 **标识号**。
3.  单击 **运行** 启动工作流设计器，然后在系统提示时输入您的用户名和密码。
4.  将 **审核标识号** 元素从工作流元素列表拖到设计器画布。
5.  将审核元素连接到 **开始** 和 **完成**。
6.  双击 **审核元素**，右键单击，然后选择 **属性**。
7.  执行以下步骤添加工作项说明：
    1.  选择 **分配**，然后选择分配类型下的 **层次结构**。
    2.  在 **层次结构** 下，选择 **可配置的层次结构**。
    3.  添加停止条件，然后关闭该页。

8.  完成其他所有说明（不应存在更多警告）。
9.  单击 **保存并关闭**。 对话框打开时激活新工作流，然后选择 **激活**。
10. 转至 **人力资源** &gt; **职位** &gt; **职位层次结构类型**。
11. 选择 **矩阵**。
12. 将 **工作人员标识号** 工作流添加到列表。

## <a name="additional-resources"></a>其他资源

[查看和管理地址更改](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]