---
title: 维护计划
description: 本主题介绍资产管理中的维护计划。
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4e9dca4b9b163e73c33ec2dc88b8aea2cecd9bef
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922198"
---
# <a name="maintenance-plans"></a>维护计划

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

维护计划定义何时对资产执行提前计划的预防性维护作业。 维护计划可以与资产、资产类型、功能位置或功能位置类型关联，但是您首先应该创建公司中要使用的维护计划。

一个维护计划中可以有多个维护计划行。 维护作业类型和间隔在维护计划行中指定。 维护计划行有两种：

- 时间  
- 计数器  

类型为“时间”的维护计划行用于基于固定时间间隔的计划性重复执行维护。 类型为“计数器”的维护计划行用于基于资产计数器登记的计划性维护或反应性维护。 一个维护计划中可以同时包含这两种类型的多个维护计划行。

>[!NOTE]
>如果没有为资产登记计数器类型的计数器值，将忽略维护计划行。

首先，为预防性维护作业创建所需维护计划，然后选择应该与每个维护计划关联的资产类型、资产、功能位置类型和功能位置。 然后，如果需要，也可以向资产或功能位置添加维护计划，此操作在**所有资产** > 选择资产 > **资产维护计划**快速选项卡中或**所有功能位置** > 选择功能位置 > **维护计划**快速选项卡中进行。

如果向资产类型或功能位置类型添加维护计划，则意味着在新建这些资产类型或功能位置类型的资产或功能位置时，将把该资产或功能位置自动添加到维护计划。 开始与维护计划关联的日期为当前日期，可能需要调整该日期。

## <a name="set-up-maintenance-plans"></a>制定维护计划

此部分介绍如何设置维护计划行，并提供其用法示例。

1. 单击**资产管理** > **设置** > **预防性维护** > **维护计划**。

2. 单击**新建**创建一个新的序列。

3. 在**维护序列**字段中插入 ID，在**名称**字段中插入名称。

4. 在**计划日期**字段中插入可以开始对维护计划进行计划的日期。 请注意，基于时间的维护计划行可能具有其他计划日期。

5. 在**有效**切换按钮中选择“是”以激活维护计划。

>[!NOTE]
>如果停用维护计划，则在运行计划维护计划作业时，不会在维护安排中创建计划过帐。

6. **容差提前天数**和**容差延后天数**字段与其中选中了**阻止维护作业重叠**复选框的维护计划行关联（请参见步骤 17）。 这些“容差”字段用于以天为单位延长间隔，而在此情况下，如果多个维护计划重叠，则在维护计划安排期间将最复杂/最大的作业创建为维护安排行，而更常见的是，维护计划安排期间忽略重叠作业。 在**容差提前天数**字段中插入天数，如“2”。

7. 如果在**容差提前天数**字段中插入了一个值，也请在**容差延后天数**字段中插入天数，如“2”。

>[!NOTE]
>此步骤和上一步骤中介绍的示例表示，如果多个维护计划行重叠，并且为一个或多个行选中**阻止维护作业重叠** ，则将维护安排行的忽略期间延长为总共五天（维护安排行的预计开始日期*加*该日期前两天*加*该日期后两天）。

8. **详细信息**快速选项卡上的**详细信息**组显示为维护计划设置的维护计划行的数量，以及与维护计划关联的资产和功能位置的数量。

9. 在**行**快速选项卡上，单击**添加时间行**或**添加资产计数器行**以创建新的维护计划行。

10. 在**工作订单描述**字段中输入行的描述。 将把此描述传输到关联的工作订单。

11. 在**维护作业类型**字段中，选择要与维护计划行关联的作业类型。

12. 在**维护作业类型变型**和**工种**字段中，根据要与维护作业类型关联的变型和工种。

13. 在**完成期限(天)** 和**完成期限(小时)** 字段中，可输入以天或小时为单位的预计结束日期。 将插入相对预计开始日期（这是创建维护安排行时计算出的）的预计结束日期。 例如，可以在**完成期限(天)** 字段中插入“7”，指示关联作业将在预计开始日期之后一周内完成。

14. 在**间隔类型**字段中，选择维护计划行中要使用的间隔类型，如“重复...”或“每隔...”。 有关间隔类型与行类型之间的关联的说明，请参见下面的[间隔类型概览](## Interval types overview)表。

15. **期间**字段仅与基于时间的行类型关联。 选择与期间频率关联的期间类型。

16. 在**期间频率**字段中，插入行应该用于计划预防性维护作业的次数。 示例：如果创建了一个类型为“计数器”的行，而您的计数器为生产数量，并且在此字段中插入数字“20000”，则每次预计再生产 20,000 个物料，都会在预防性维护安排期间新建维护序列行。

17. **阻止维护作业重叠**复选框与基于时间的行类型和基于计数器的行类型关联。 若要删除同一天创建的维护安排条目，请选中此复选框。 例如，如果已经创建了 1 个月检验行，6 个月检验行和 1 年检验行，则与此复选框有关。 对于 1 年检验，只需要完成该检验，不需要完成另外两项检验，这也符合时间范围。 若要正确设置此示例，请将 1 年检验行设置为第一个行，将 6 个月行设置为第二个行，将 1 个月行设置为第三个行，并且选中 1 个月行和 6 个月行的**阻止维护作业重叠**复选框。 这样就可以确保在到达 1 年标记时，忽略一个月检验和六个月检验，并仅为 1 年检验行创建维护安排行。

>[!NOTE]
>此步骤中介绍的示例显示，最复杂的作业（其中包含的任务数量最多，并且执行频率不高）应该始终作为第一行插入。 然后按照频率顺序将频率更高的作业作为单独行插入，并将频率最高的作业放在列表底部。

18. **计数器**字段仅与基于计数器的行类型关联。 选择行中要使用的计数器类型。 如果某个计数器类型对关联的资产无效，将忽略维护计划行。

19. **按天数计算的资产计数器时限**字段仅与基于计数器的行类型关联。 插入一个数字，用于指示完成维护计划安排后检查计数器登记时的回溯天数。 这表示回溯多久的数据（现有计数器登记）来充当计算趋势时的基础，以确定创建多少个维护安排行。

>*示例：* 如果应该每个月进行一次计数器登记，则可在此字段中插入数字“365”，因为维护计划安排始终基于过去的 12 个月，因此，基于上一年的趋势创建维护安排行。 另一方面，如果在此字段中插入“10”，则预计进行计数器登记的频率更高，如，每天一次。 这意味着在安排维护计划时，将使用过去 10 天的计数器登记充当基础来计划维护安排行。

20. **计划日期**字段仅与基于时间的行类型关联。 如果维护计划行的计划日期不是整个维护计划的日期，请在行中的**计划日期**字段中选择一个日期。

21. 在**服务级别**字段中，可选择工作订单服务级别来进一步界定维护计划行 - 用作工作订单中的服务级别。

22. 如果要在安排维护计划时根据所选维护计划行自动创建工作订单，请选中**自动创建**复选框。

23. 如果已选中了**自动创建**复选框，则可在**工作订单类型**字段中为自动创建的工作订单选择工作订单类型。 如果已选中了**自动创建**复选框，但是不在此字段中选择工作订单类型，则使用在**资产管理** > **设置** > **资产管理参数** > **工作订单**列表 > **预防性工作订单类型**字段中选择的工作订单类型。

24. 可使用**开始季节**和**结束季节**字段创建 12 个月期间内基于时间的重复性维护计划行。 *示例：* 需要在预定义的期间内每个春季为用于维护绿化区的设备服务。 在**开始季节**字段中输入要重复的期间的开始日期。

25. 在**结束季节**字段中输入要重复的期间的结束日期。

26. **生成的期间**字段中将显示要重复的当前期间。 当前期间已过去，并且开始新的年度时，将更新此字段中显示的期间，以体现重复序列中的下一年。

27. 在**资产**快速选项卡上，选择应该与维护计划关联的资产。

28. 在**资产类型**快速选项卡上，选择应该与维护计划关联的资产类型。

29. 在**功能位置**快速选项卡上，选择应该与维护计划关联的功能位置。 如果需要，可以通过选择关联的资产类型、制造商和型号来提高设置的具体程度。

30. 在**功能位置类型**快速选项卡上，选择应该与维护计划关联的功能位置类型。

>[!NOTE]
>为供应商保修涵盖的资产手动创建工作订单时，将显示一个对话框，用于提醒用户注意保修。 然后可以取消创建此工作订单。 将对自动创建的工作订单忽略检查保修关联。

## <a name="interval-types-overview"></a>间隔类型概览

| 间隔类型和描述                                                                                                                                                                                                                                                                                                                                                                                                       | 行类型：时间                                                                                                                                                                                                                                                                                                                                                           | 行类型：计数器                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **间隔类型：从计划日期开始重复** 计数从所用计划日期开始。 如果安排维护计划，将在到达间隔时创建维护安排行。                                                                                                                                                                                                                | 将使用维护计划行中的**计划日期**。 如果不在行中选择任何计划日期，则使用维护计划的**计划日期**。 示例：如果在**期间频率**字段中输入数字“3”，并且在**期间**字段中选择“是”，则每隔 3 年创建新建一次维护安排行。                             | 将使用维护计划的**计划日期**。 如果已替换了计数器，将把最近的替换日期用作计划日期。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **间隔类型：从开始日期开始重复** 从开始关联资产时的日期开始计数。 此日期在**所有资产**详细信息视图 > **资产维护计划**快速选项卡 > **开始日期**字段中或在**所有功能位置**详细信息视图 > **维护计划**快速选项卡 > **开始日期**字段中选择。 如果安排维护计划，将在到达间隔时创建维护安排行。 | 将使用资产或功能位置的维护计划行的开始日期。 如果该字段为空，则使用维护计划的**计划日期**。                                                                                                                                                                                                 | 将使用资产或功能位置的维护计划行的开始日期。 如果该字段为空，则使用维护计划的**计划日期**。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **间隔类型：从上一个工作订单开始重复** 从对采用特定维护作业类型/维护作业类型变型/工种组合的资产完成的上一个工作订单的实际结束日期和时间开始计数。 将在**所有工作订单**详细信息视图中的**实际结束时间**字段中显示该日期和时间。                                                                                                                                 | 将使用对采用该特定维护作业类型/维护作业类型变型/工种组合的资产完成的工作订单的实际结束。 如果未找到已完成的工作订单，将改用上面介绍的“从开始日期开始重复”间隔类型中使用的一个日期。                                                                                             | 将使用对资产*和*维护作业类型/维护作业类型变型/工种组合完成的工作订单的实际结束。 日期和时间。 如果工作订单中的结束日期和时间保留为空，将改用上面介绍的“从开始日期开始重复”间隔类型中使用的一个日期。                                                                                                                                                                                                                                                                                                                                                                           |
| **间隔类型：从计划日期开始一次** 请参阅上面的“从计划日期开始重复”间隔类型的描述。 唯一不同之处是，此间隔类型仅使用一次。                                                                                                                                                                                                                                                   | 请参阅上面的“从计划日期开始重复”间隔类型的描述。 此间隔通常用于一次性维护或服务作业。                                                                                                                                                                                                                             | 请参阅上面的“从计划日期开始重复”间隔类型的描述。 此间隔通常用于一次性维护或服务作业。 **注释 1：** 仅当只要执行维护或服务作业就替换计数器时，此间隔类型才相关。 如果出于某种原因在计划的间隔结束前就替换了计数器，将从替换计数器时开始为作业计算新的时间。 **注释 2：** 如果在完成维护或服务作业时替换计数器，此间隔类型将充当上面的“从计划日期开始重复”间隔类型。                                             |
| **间隔类型：从开始日期开始一次** 请参阅上面的“从开始日期开始重复”间隔类型的描述。 唯一不同之处是，此间隔类型仅使用一次。                                                                                                                                                                                                                                                 | 请参阅上面的“从开始日期开始重复”间隔类型的描述。 此间隔通常用于一次性维护或服务作业。                                                                                                                                                                                                                            | 请参阅上面的“从开始日期开始重复”间隔类型的描述。 此间隔通常用于一次性维护或服务作业。 上面的**注释 1** 也适用于此间隔类型。 **注释 3：** 如果在完成维护或服务作业时替换计数器，此间隔类型将充当上面的“从开始日期开始重复”间隔类型。                                                                                                                                                                                                                                                                                                |
| **间隔类型：达到上限时一次** 此间隔类型仅与计数器关联，用于指示为维护计划行设置的上限。 维护安排条目将采用计数器登记的预计开始日期和时间，这意味着创建的这些条目的预计开始日期等于或早于系统日期。                                                | 无                                                                                                                                                                                                                                                                                                                                                                       | 此计数器间隔指示一个上限。 如果在创建计数器登记时超过了该限制，将在安排预防性维护时创建一个维护安排行。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **间隔类型：达到下限时一次** 此间隔类型仅与计数器关联，用于指示为维护计划行设置的下限。 维护安排条目将采用计数器登记的预计开始日期和时间，这意味着创建的这些条目的预计开始日期等于或早于系统日期。                                                 | 无                                                                                                                                                                                                                                                                                                                                                                       | 此计数器间隔指示一个下限。 如果在创建计数器登记时低于该限制，将在安排预防性维护时创建一个维护安排行。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **间隔类型：从开始日期链接** 此间隔类型仅创建一次维护安排行。 一个维护计划中可以包含多个使用此间隔类型的维护计划行，并且将链接这些行。 您创建的维护计划中通常仅包含此间隔类型的行。 将通过识别具有第一个预计开始日期和时间的维护计划行来创建维护安排行。                                                                                                                                                                                                                                                                                                                                                                                           | 请参阅上面的“从开始日期开始一次”的描述。 示例：在一辆汽车的服务作业的维护计划中创建两个行：一个行基于时间且期间为 1 年，一个行基于计数器且限制为 25,000 公里。 将为首先达到的限制创建一个维护安排行。 对于此行类型，将创建期间为 1 年的行。                                                                                                                                                                                   | 请参阅上面的“从开始日期开始一次”的描述。 示例：在一辆汽车的服务作业的维护计划中创建两个行：一个行基于时间且期间为 1 年，一个行基于计数器且限制为 25,000 公里。 将为首先达到的限制创建一个维护安排行。 对于此行类型，将创建限制为 25,000 公里的行。 有关创建两个计数器行的示例：也可以设置包含两个基于计数器的链接行的维护计划，其中的第一个行的限制为生产 10,000 个物料，第二个行则与在运行 3,000 小时后需要服务的机器或工作中心关联。                                                                                                                                                           |
| **间隔类型：从最后一个工作订单链接** 每次完成工作订单，此间隔类型都将创建新的维护安排行。 一个维护计划中可以包含多个使用此间隔类型的行，并且将链接这些行。 您创建的维护计划中通常仅包含此间隔类型的维护计划行。 将通过识别具有第一个预计开始日期和时间的维护计划行来创建维护安排行。                                                                                                                                                                                                                                                                        | 此间隔类型基本充当上面的“从开始日期链接”。 唯一区别是充当间隔类型基础的日期。 所用日期是对资产*和*维护作业类型/维护作业类型变型/工种组合完成的最后一个工作订单的实际日期和时间。                                                                                                                                                                                                                                                           | 此间隔类型基本充当上面的“从开始日期链接”。 唯一区别是充当间隔类型基础的日期。 所用日期是对资产*和*维护作业类型/维护作业类型变型/工种组合完成的最后一个工作订单的实际日期和时间。                                                                                                                   |


>[!NOTE]
>为基于时间的维护计划行创建维护安排行时，预计时间始终为当天的开始时间。 对于基于计数器的维护计划行，预计时间可以是当天的任何时间。

下面是基于时间的维护计划行和基于计数器的维护计划行的设置：

**示例 1 - 基于时间的维护计划行：** 可以为润滑作业设置固定间隔，每周进行一次。 因此，请在**间隔类型**字段中选择“从计划日期开始重复”。 请参阅下图中的示例。

![图 1](media/02-preventive-maintenance.png)

**示例 2 - 基于时间的维护计划行：** 可将一个检验作业设置为一周大约执行一次。 因此，请在**间隔类型**字段中选择“从最后一个工作订单开始重复”。 请参阅下图中的示例。

![图 2](media/03-preventive-maintenance.png)

**示例 3 - 基于计数器的维护计划行：** 下图显示每次过去 250 小时都将为其创建一个新的维护安排行的小时计数器。 这个基于计数器的行的间隔类型为“从开始日期开始重复”。 开始日期是关联资产在**所有资产**详细信息视图 > **资产维护计划**快速选项卡 > **开始日期**字段中或**功能位置**详细信息视图 > **维护计划**快速选项卡 > **开始日期**字段中的开始日期。 这是*预防性*维护计划的示例，因为每次达到阈值 (+ 250) 时，都将自动创建维护安排行。

![图 3](media/04-preventive-maintenance.png)


**示例 4 - 基于计数器的维护计划行：** 下图显示用于度量制动衬块磨损情况的计数器值降低。 当为制动衬块创建低于 20 毫米的计数器登记时，将创建一个维护安排行。 这个基于计数器的行的间隔类型为“达到下限时一次”或“从上一个开始日期开始时一次”。 这是*反应式*维护计划的示例，因为在登记的度量低于 20 毫米之前，不创建维护安排行。

![图 4](media/05-preventive-maintenance.png)


**示例 5 - 基于计数器的维护计划行：** 下图显示阈值为 -18° 摄氏度的计数器。 当创建的计数器登记超过 -18° 摄氏度时，将创建一个维护安排行。 这个基于计数器的行的间隔类型为“达到上限时一次”。 这是*反应式*维护计划的示例，因为在登记的度量高于 -18° 摄氏度之前，不创建维护安排行。

![图 5](media/06-preventive-maintenance.png)

- 当您创建新资产，并且该资产使用与维护计划关联的资产类型时，将在**所有对象** > **资产维护计划**快速选项卡中自动插入该维护计划。 并且将在**维护计划**快速选项卡上的**资产类型默认**中自动插入关联的维护计划。  
- 如果在**维护计划**中添加或删除资产类型或功能位置类型，将仅在执行更改之后新建的资产上体现该更改。  
- 如果在**维护计划**中添加或删除资产或功能位置，将在**所有资产** > **资产维护计划**快速选项卡中或在**所有功能位置** > **维护计划**快速选项卡中自动更新该更改。  

下图显示**维护计划**页中“卡车维修”维护计划的一个示例。

![图 6](media/07-preventive-maintenance.png)


## <a name="add-a-maintenance-plan-to-an-asset"></a>向资产添加维护计划

1. 单击**资产管理** > **常用** > **资产** > **所有资产**或**有效资产**。

2. 选择要为其设置维护计划的资产，然后单击**编辑**。

3. 在**资产维护计划**快速选项卡上，单击**添加行**向资产添加维护计划。

4. 在**维护计划**字段中，选择相关维护计划。

5. 在**开始日期**字段中选择可以开始对预防性维护计划进行计划的日期。 

6. 单击**保存**。 将自动更新**有效**字段。

下图显示**所有资产**页中为资产设置的维护计划的一个示例。

![图 7](media/08-preventive-maintenance.png)
