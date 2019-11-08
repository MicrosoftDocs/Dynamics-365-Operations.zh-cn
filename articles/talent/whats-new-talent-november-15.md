---
title: Dynamics 365 Talent - Core HR（2018 年 11 月 15 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a571568850a675f3472f2b62df33c0c35d905af0
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551372"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a>Dynamics 365 Talent - Core HR（2018 年 11 月 15 日）中的新增功能或更改

[!include [banner](includes/banner.md)]

**内部版本 8.1.2045**

此主题介绍了 Core HR 中的新增功能和更改的功能。

## <a name="other-changesfixes"></a>其他更改/修复

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>无法将员工的当前职位更改为将来的空缺职位

已进行了更改来在职位仅在未来可用时启用职位转移。 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>职位在创建新员工时不显示

已经进行了更改来在 Talent 中招聘新员工时显示可用于分配的所有空缺职位。 这包括历史职位或被设置了将来日期的职位。 职位现在将根据雇用开始日期正确显示。 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>终止雇用日期基于用户设置显示

已对以往员工列表进行了更改来解释在查看终止雇用日期时员工首选时区的任何时区偏移。

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>分配给我的工作项链接不显示正确信息

通过此更改，导航到列表中各个工作项的详细信息将显示所选项目的正确信息。 此问题只在高级安全选项中出现。


## <a name="known-issue"></a>已知问题

- **问题**：在将新附件添加到工作人员时，**新建**和**编辑**按钮变灰。 
- **解决方法：** 打开附件页面之前，确保已关闭**工作人员**页面中的速见表。 如果加载**工作人员**页面时速见表已关闭，将启用附件按钮。 （下一个平台更新中将解决这个问题。）
