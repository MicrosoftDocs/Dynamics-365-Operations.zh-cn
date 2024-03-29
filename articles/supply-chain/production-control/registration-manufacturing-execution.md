---
title: 制造执行的登记
description: 本文描述您需要理解才能配置和使用制造执行的重要概念和术语。
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c43a9d847045f2c029f232d6317268d91ee0129a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907194"
---
# <a name="registration-for-manufacturing-execution"></a>制造执行的登记

[!include [banner](../includes/banner.md)]

本文描述您需要理解才能配置和使用制造执行的重要概念和术语。 

制造执行主要由制造公司使用。 工作人员可以使用 **作业登记** 页登记生产作业上的时间和物料消耗。 审核所有登记，随后将它们转移到相关模块。 持续审核和庄毅登记允许经理轻松跟踪生产订单的实际成本。

## <a name="manufacturing-execution-and-registration-terminology"></a>制造执行和登记术语
下表包含与制造执行和相关登记任务的相关的术语。

| 术语                          | 说明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 制造执行       | 用于登记时间、材料消耗、生产作业成本、项目和间接活动的功能。 在制造执行登记客户端中执行登记。                                                                                                                                                                                                                                                                                                                                                                                                   |
| 作业单列表                      | 在 **作业登记** 页中，工作人员显示它们必须在机器等特定资源上执行的作业的列表。 工作人员可以在作业列表中的每个作业或任务上登记时间和物料消耗。                                                                                                                                                                                                                                                                                                                                                                           |
| 作业捆绑                  | 如果工作人员在 **作业登记** 页中同时开始不止一个作业，这将被称作捆绑作业。 可以通过使用分配参数按不同的方法将在捆绑的作业上花费的时间分配到各个作业。                                                                                                                                                                                                                                                                                                                                                         |
| 指导/助手登记 | 工作人员可以作为某一资源的助手登记，并可创建多个工作人员在同一生产作业上工作的小团队。 工作人员作为助手所连接到的资源被称为指导。 只有指导资源必须进行登记。 所有助手自动获取相同的登记。 例如，如果作为指导的机器功能和作为此机器的助手登记的工作人员可以在 **作业登记** 页中进行登记，那么机器和作为助手连接的工作人员将接收相同的登记。 |
| 间接活动             | 未直接与生产作业或项目相关的活动或任务，如部门会议、清洗工作或车间作业上的维修作业。 工作人员可以按照登记生产作业和项目的方法对间接活动进行登记。                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>制造执行中的登记
工作人员可以在生产作业上执行的工作的制造执行中进行各种类型的登记。 根据系统设置，工作人员可能还能够对项目活动以及工间休息、缺勤和间接活动等非生产任务进行登记。 以下是登记类型：

-   **上班打卡/下班打卡**（时间和出勤可用）– 工作人员在到达工作地点时上班打卡，在离开回家时下班打卡。
-   **在生成作业上登记** – 工作人员可以对显示在作业列表中的生产作业上进行登记，如开始作业和报告作业反馈。 工作人员可以同时开始多个作业。 这称为捆绑作业。
-   **在库存上登记** – 工作人员可以对用于不与生产作业直接相关的车间作业上的材料进行登记。 示例包括油脂、润滑剂，或其他用于使机械运行的材料。 在库存日志中执行登记。
-   **对项目进行登记**（时间和出勤可用）– 工作人员可以对出现在其工作列表中的项目或项目活动的起始和完成工作等进行登记。
-   **登记项目费用和项目物料**（时间和出勤可用）– 工作人员可以登记与某一项目费用日记帐的项目关联的费用（支出），如里程和过桥费。 工作人员还可以登记项目的物料消耗量。 这可以在项目物料日记帐中执行。
-   **作为另一个工作人员的助手登记** – 如果两个或多个工人在生产作业或项目上一起工作，那么工作人员可作为机器的助手或另一个工作人员的助手进行登记，然后该工作人员将作为指导。 如果需要，指导可以选择其他工作人员作为指导。
-   **登记缺勤**（时间和出勤可用）– 工作人员可以登记设置的各种考勤代码的时间。 如果工作人员迟到、在工作日期间要求缺席或比预期的标准工作时间模板早离开，可以指示缺勤。
-   **登记工间休息**（时间和出勤可用）– 在工作日，工作人员可以登记自己将离开其工作站进行休息。 可以设置许多工间休息类型。 当工作人员返回并重新登录时，系统将登记该工作人员已返回，同时工间休息登记停止。
-   **登记间接活动**（时间和出勤可用）– 间接活动是工作人员可能在工作日期间参与的非生产活动，例如部门会议、团队会议或在车间执行的维护作业。 工作人员可以在已设置的间接活动上进行登记。
-   **登记加班时间**（时间和出勤可用）– 被要求长时间工作的工作人员可以选择额外工时是否登记为弹性工作时间或加班时间。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]