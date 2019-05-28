---
title: 工作时间日历
description: 本主题介绍 Dynamics 365 for Talent -- Core HR 中的工作时间日历和如何设置日历。
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: a1e7bc0098556f42321b6a8883b59aa4fd9a8abd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517437"
---
# <a name="working-time-calendars"></a>工作时间日历

[!include [banner](includes/banner.md)]

可通过工作日历创建包含员工在组织中的工作时数和天数的日历。 缺省情况下，日历以小时或天为单位组织请假流程。 员工提交请假申请时，不必担心假日和歇业，因为会通过工作日历处理这些事宜。

## <a name="setting-up-a-working-time-calendar"></a>设置工作日历

日历中包含生成详细信息、要包含的日期和小时、日历的日期、这些日期的工作时间，以及已登记的员工。 

若要设置日历，请执行以下步骤：

1. 在**组织管理**页面上，单击**日历**。

2. 在操作窗格上，选择**新建**并输入名称和描述。

3. 选择组织的工作日，然后输入工作时间。

4. 通过使用**添加**按钮添加假日和歇业。

5. 输入假日和歇业的名称和描述，如“美国假日”或“银行日”。 输入假日和歇业的日期。 保存假日和歇业列表，然后关闭页面。

6. 从下拉菜单中选择假日和歇业列表。

7. 如果员工有非工作时间（如午餐时间或休息时间），请一并添加。 选择**非工作时间**，然后输入名称和时间范围。 关闭该页面。 

8. 单击**添加**以向日历添加非工作时间。

9. 在**天数**选项卡中，选择**生成**以生成日历中包含的天数。 输入日历的日期范围。 天数和工作时间基于生成选项下定义的工作日和时间以及所选日期生成。

10. 若要将日历分配给员工，请在操作窗格中选择**分配给员工**。 选择要为其分配该日历的员工，然后单击**分配**。

可以不为员工分配日历。 如果定义了工作日历，将从请假中自动排除休假日期。 缺省情况下，数量（以小时或天为单位）为日历中定义的工作时间。 如果没有为员工分配日历，则所有日期均可请假，而休假量不是请假的默认值。 
