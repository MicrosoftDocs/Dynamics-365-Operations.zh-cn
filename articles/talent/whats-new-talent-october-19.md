---
title: Dynamics 365 Talent - Core HR（2018 年 10 月 16 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 13e89faa3f8470125010ccdb40a6f01c0a9c4fe7
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008769"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-19-2018"></a>Dynamics 365 Talent: Core HR（2018 年 10 月 19 日）中的新增功能或更改

[!include[banner](includes/banner.md)]

**内部版本 8.1.1067**

此主题介绍了 Core HR 中的新增功能和更改的功能。

## <a name="allow-managers-to-update-time-off-requests"></a>允许经理更新休假请求

员工休假请求在通过工作流审批后可能需要更新。 在大多数情况下，经理代表员工进行这些更新。 此新功能为经理提供代表其员工更新休假或取消休假请求的能力。 此功能由**代为工作**参数控制，此参数可以在**人力资源参数**页设置。 
 
## <a name="allow-hr-to-update-time-off-requests"></a>允许人力资源更新休假请求

与上述功能类似，员工休假请求之前在通过工作流审批后可能需要由人力资源更新。 此功能为人力资源用户提供更新休假请求的能力。 此功能在**人员**工作区和**工作人员**页面使用称为**查看休假**的新选项启用。 在这些页面上，人力资源用户可以查看请求并更新休假交易记录，类似于经理执行这些操作的方式。

控制此功能的访问的安全责任是：
- 责任：维护特定工作人员休假和缺勤的流程。
- 权限：维护所有工作人员的休假和缺勤请求。

## <a name="other-changes"></a>其他更改
此版本已进行以下更新：
- 更改了工作人员招聘操作，以便操作不会再被“卡”在**工作流已完成**状态。
- 雇用记录现在可以创建，其中没有雇用开始日期。
- 在员工自助服务中显示的课程的 Dynamics 365 Talent 登记日期现在将时区偏移应用到日期。
- 使用**员工实体**可以没有任何错误地多次导入 Excel 文件。

## <a name="known-issue"></a>已知问题

- **问题**：在将新附件添加到工作人员时，**新建**和**编辑**按钮变灰。 
- **解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。 如果加载**工作人员**页面时速见表已关闭，将启用附件按钮。 （下一个平台更新中将解决这个问题。）
