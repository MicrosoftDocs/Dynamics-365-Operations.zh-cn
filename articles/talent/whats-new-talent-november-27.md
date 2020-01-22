---
title: Dynamics 365 Talent - Core HR（2018 年 11 月 27 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d6b5f5f7b62c400679df5eb014dee05f02e11d0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897480"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-27-2018"></a>Dynamics 365 Talent - Core HR（2018 年 11 月 27 日）中的新增功能或更改

**内部版本 8.1.2064**

此主题介绍了 Core HR 中的新增功能和更改的功能。


## <a name="changes"></a>更改

### <a name="unable-to-create-a-note-in-case-management"></a>无法在“案例管理”中创建注释

已进行了更改来解决当尝试在“案例管理”的案例日志中编辑或创建注释时出现的问题。

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>薪酬工作区中分析选项卡上拼写错误的字词 

已进行了更改来更正薪酬工作区中薪酬分析图表中“所属种族”的拼写。

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>员工自助服务工作区在用户未分配给工作人员时不显示 

已对当**员工自助服务**工作区在启动时被选择为分配给工作人员的用户的初始页面进行了更改。 在此情况下，默认仪表板将显示。

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>休假和缺勤错误：对象参考未设置为对象的实例

已对休假和缺勤进行了更改来更正在**分配给我的工作项**列表中审批休假和缺勤记录之后出现的这个错误。

### <a name="unable-to-recall-an-image-workflow"></a>无法撤消图像工作流

在撤消图像工作流后，工作流将被设置为“已取消”，现有请求可以在员工自助服务工作区删除。

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>重新雇用的员工或合同工在雇用终止后多次显示 

通过此更新，重新雇用的离职员工将只在退出列表中显示一次。 

## <a name="known-issue"></a>已知问题

- **问题**：在将新附件添加到工作人员时，**新建**和**编辑**按钮变灰。 
- **解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。 如果加载**工作人员**页面时速见表已关闭，将启用附件按钮。 （下一个平台更新中将解决这个问题。）
