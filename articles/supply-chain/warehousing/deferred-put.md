---
title: 推迟处理仓库工作
description: 本主题介绍 Dynamics 365 Supply Chain Management 中提供的用于将推迟处理仓库工作转化为放置操作的功能。
author: josaw1
manager: tfehr
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc8321c55bc867db065af0cddf356fb497a956e8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423336"
---
# <a name="deferred-processing-of-warehouse-work"></a>推迟处理仓库工作

[!include [banner](../includes/banner.md)]

本主题介绍 Dynamics 365 Supply Chain Management 中提供的用于将推迟处理仓库工作转化为放置操作的功能。

推迟处理功能让仓库工人可以在后台处理放置操作期间继续执行其他工作。 当必须处理大量工作行，并且工人可以异步处理这些工作时，推迟处理非常有用。 当服务器的处理时间临时或意外增加，并且增加的处理时间可能影响用户的生产率时，此功能也非常有用。

可使用 SysOperation 框架实现后台处理。 有关详细信息，请参阅 [SysOperation 框架概述](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview)。

## <a name="configuring-the-work-processing-policies"></a>配置工作处理策略

若要使用推迟处理，必须配置并使用工作处理策略。

策略在 **工作处理策略** 页中配置。 下表介绍该页中的字段。

| 字段                           | 说明 |
|---------------------------------|-------------|
| 工作处理策略名称     | 工作处理策略的名称。 |
| 工作订单类型                 | 应用策略的工作订单类型。 |
| 操作​                       | 使用策略处理的操作。 |
| 工作处理方法          | 用于处理工作行的方法。 如果方法设置为 **立即**，则行为类似未使用任何工作处理策略来处理行时的行为。 如果方法设置为 **推迟**，则使用的是使用批处理框架的推迟处理。 |
| 延期处理阈值   | 如果值为 **0**（零），这表示无阈值。 在这种情况下，如果可以，将使用推迟处理。 如果阈值的具体计算结果低于阈值，则使用“立即”方法。 否则，如果可以，则使用“推迟”方法。 对于与销售和运输有关的工作，计算出的阈值是正在为工作处理的关联源负荷行的数量。 对于补货工作，计算出的阈值是工作正在补货的工作行的数量。 例如，如果为销售将阈值设置为 **5**，则初始源负荷行少于五个的少量工作不使用推迟处理，但是大量工作则会使用。 仅当工作处理方法设置为 **推迟** 时，此阈值才有效。 |
| 延迟处理批处理组 |用于处理的批处理组。 |

对于延期的放置处理，支持以下工作订单类型：销售订单、转移单发放和补货。

## <a name="assigning-the-work-creation-policy"></a>分配工作创建策略

可以在仓库管理参数中分配工作创建策略。 还可以在单个仓库级别分配。 如果为仓库分配了策略，将把该策略仅应用于为这个仓库创建的工作。 如果未在仓库级别分配策略，则应用仓库管理参数中的策略。

## <a name="viewing-the-deferred-put-processing-tasks"></a>查看推迟放置处理任务

可在 **推迟放置处理任务** 页中查看推迟放置处理任务。

默认情况下，将显示 **已完成** 任务。

| 字段            | 说明 |
|------------------|-------------|
| 状态           | 任务的状态。 |
| 批处理作业状态 | 相关批处理作业的状态。 如果已处理了批处理作业，则批处理历史记录中包含批处理作业的日志和信息。 |

以下是对可能的状态的说明：

- **正在等待** – 批处理服务器正在等待处理相关批处理作业。
- **失败** – 处理已失败。 可以使用 **处理推迟的放置** 操作重新处理该任务，也可以使用 **取消推迟的放置** 操作取消该任务。
- **已完成** – 作业已完成。

## <a name="impact-on-closed-work-dates"></a>对工作关闭日期的影响

如果使用推迟的放置处理，则将工作关闭日期设置为推迟的放置处理任务的创建日期/时间。 之所以使用工作关闭日期，是因为这是放置操作完成时间的最佳估计结果。

## <a name="reprocessing-a-failed-task"></a>重新处理失败任务

可重新处理失败任务，方法是在页面中选择该任务，然后选择 **处理推迟的放置**。 重新处理与以下情况对应：用户从移动设备完成入库，就像是为立即处理设置的。

## <a name="canceling-failed-tasks"></a>取消失败任务

只有失败任务才能取消。 取消任务后，可将其分配给新用户。 也可以将任务继续分配给曾处理该工作的用户。 取消对应于以下情况：将工作带回移动设备，就像刚完成上一个领料步骤，并且工作必须完工入库。 但是，用户可以确定工作“不同”，因为该工作只有入库步骤，而位置将继续与第一位处理该工作的用户用作最终放置位置的位置对应。

取消任务后，推迟放置处理阻止原因不再阻止工作。 可以使用移动设备重新处理该任务。

取消任务后，将删除任务记录。

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>配置移动设备菜单以跳过推迟处理策略

可配置移动设备菜单项，以便不使用推迟处理策略。 然后按照不使用推迟处理策略的方式处理工作。 此功能让主管可使用其中不使用推迟放置的特定菜单项。 若要配置，请将 **推迟放置处理策略** 字段设置为 **覆盖设置并同步处理放置**。 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>不应用推迟放置处理时的限制

有几种情况即使配置了策略，也不应用推迟放置处理。 下面举了一些示例加以说明：

- 使用了手动完工。
- 将使用自动完成完成工作。
- 使用了审计模板。


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>从“出站工作监视”工作区监视推迟处理的任务

**出站工作监视** 工作区有两个磁贴，可帮助您监视推迟的放置处理任务：

- **失败推迟放置处理任务** – 此磁贴显示失败任务数量。 如果有失败任务，仓库经理必须重新处理或取消这些任务，因为不会自动重新处理。
- **等待推迟的放置处理任务** – 此磁贴显示 **正在等待** 状态超过 10 分钟的任务的数量。 如果此磁贴显示数字，可能表示批处理期间发生了问题。 可手动处理 **正在等待** 任务。 如果以后处理任务的批处理作业，就会失败，因为已经处理过了。 不会有影响。

## <a name="deleting-completed-tasks"></a>删除已完成任务

可删除已完成的推迟放置处理任务，方法是在页面中选择这些任务，然后删除。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]