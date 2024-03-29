---
title: 未雇用的工作人员
description: 您的组织中没有未来、当前或历史雇用的工作人员会出现在“未雇用工作人员”页面上。
author: twheeloc
ms.date: 11/03/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3b2d5d470e780c708941fd3d08eae1a042b4c03
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689794"
---
# <a name="workers-without-employment"></a>未雇用的工作人员


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您的组织中没有未来、当前或历史雇用的工作人员会出现在 **未雇用工作人员** 页面上。 当您导入没有雇用记录的工作人员时，或者通过 **工作人员 \> 雇用历史记录** 删除工作人员的雇用时，会出现此类型的工作人员。

默认情况下，**未雇用工作人员** 页面对以下角色可用：

- 人力资源助理
- 人力资源经理
- 招聘人员
- 薪酬福利经理
- 工资管理员
- 工资经理
- 培训经理

在 **未雇用工作人员** 列表中，您可以删除列出的个人。 默认情况下，此特权被授予“人力资源助理”角色。 您可以通过以下步骤将此特权授予其他角色：

1. 选择 **系统管理**，然后选择 **安全配置**。

2. 在 **特权** 选项卡中，筛选 **特权** 列表以 **维护工作人员**。

   [![筛选特权列表。](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. 在 **参考** 列中，选择 **显示菜单项**。

4. 在 **显示菜单项** 中，选择 **HcmWorkersWithoutEmployment**。

   [![选择窗体。](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. 将 **删除** 权限设置为 **授权**。

6. 选择 **已取消发布的对象** 选项卡。

7. 选择 **全部发布**。

   [![发布更改。](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
