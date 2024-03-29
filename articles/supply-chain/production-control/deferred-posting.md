---
title: 在过帐到日记帐前将成品设置为实际可用
description: 当制造的物料被报告为完工入库时，它将注册为可用于进一步实际处理，并且将过帐一个或多个日记帐。 本文介绍如何通过允许消息队列中的批处理作业处理日记帐过帐来延迟日记帐过帐。
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ee767a5d7c3dca2681861802ae42d7a07217c54d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689332"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>在过帐到日记帐前将成品设置为实际可用

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

当工作人员将制造的物料报告为完工入库时，系统会将其登记为可用于进一步实际处理（如装运或储存）。 在此流程中，还将过帐一个或多个日记帐（如报告为完工入库日记帐、领料单日记帐和工艺卡日记帐）。 如果要在处理所有过帐之前使您的物料实际可用，则可以将系统设置为延迟日记帐过帐。 然后，延迟过帐由批处理作业进行管理，该作业将在系统资源允许时处理过帐。

下图显示了在有和没有延迟过帐的情况下如何调用日记帐过帐流程。

![具有和不具有延迟日记帐过帐的报告为完工入库流程。](media/deferred-posting-flowchart.png "具有和不具有延迟日记帐过帐的报告为完工入库流程")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>为您的系统开启延迟日记帐过帐

在您可以使用延迟日记帐过帐之前，必须在系统中打开它。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查此功能的状态，以及开启此功能（如果需要）。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*生产控制*
- **功能名称**：*（预览版）在过帐到日记帐前将成品设置为实际可用*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>设置“报告为完工入库”的日记帐过帐选项

工作人员可使用以下任何客户端将物料报告为完工入库：

- Web 客户端
- Warehouse Management 移动应用
- 生产车间执行界面

Web 客户端与 Warehouse Management 移动应用使用相同的过帐方法配置。 但是，必须单独配置生产车间执行界面使用的过帐方法。

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>设置 Web 客户端和 Warehouse Management 移动应用的日记帐过帐选项

在移动应用中，工作人员通过打开移动设备菜单项将物料报告为完工入库，其中 **工作创建流程** 值为 *报告为完工入库* 或 *报告为完工入库并储存*。 在 Web 客户端中，工作人员从 **所有生产订单** 列表页或 **生产订单（详细信息）** 页面将物料报告为完工入库。 您可以配置公司范围内的默认方法，也可以根据需要设置特定于仓库的覆盖。

使用以下过程配置公司范围内的默认过帐方法，以从 Web 客户端或 Warehouse Management 移动应用中将物料报告为完工入库。

1. 转到 **生产控制 \> 设置 \> 生产控制参数**。
1. 在 **日记帐** 选项卡上的 **报告为完工入库的日记帐** 部分中，将 **过帐方法** 字段设置为以下值之一：

    - *即时* - 当物料报告为完工入库时，系统将完全处理所有相关的日记帐过帐，然后再将成品标记为实际可用。
    - *延期* - 当物料报告为完工入库时，系统将成品标记为实际可用，并将日记帐过帐添加到消息队列中。 在将成品标记为实际可用之前，系统不会等到过帐被完全处理。

使用以下过程为在 **生产控制参数** 页面上配置的默认过帐方法配置特定于仓库的覆盖。

1. 转到 **仓库管理 \> 设置 \> 库存细分 \> 仓库**。
1. 选择您要设置的仓库。
1. 在操作窗格上，选择 **编辑**。
1. 在 **仓库** 快速选项卡上的 **生产订单** 部分中，将 **过帐方法** 字段设置为以下值之一：

    - *继承* - 所选仓库从 **生产控制参数** 页面继承设置。
    - *即时* - 当物料报告为完工入库时，系统将完全处理所有相关的日记帐过帐，然后再将成品标记为实际可用。
    - *延期* - 当物料报告为完工入库时，系统将成品标记为实际可用，并将日记帐过帐添加到消息队列中。 在将成品标记为实际可用之前，系统不会等到过帐被完全处理。

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>针对生产车间执行界面设置日记帐过帐选项

使用以下过程配置从生产车间执行界面将物料报告为完工入库时使用的过帐方法。

1. 转到 **生产控制 \> 设置 \> 制造执行 \> 生产订单默认值**。
1. 在 **报告为完工入库** 选项卡上的 **报告为完工入库的日记帐** 部分中，将 **过帐方法** 字段设置为以下值之一：

    - *即时* - 当物料报告为完工入库时，系统将完全处理所有相关的日记帐过帐，然后再将成品标记为实际可用。
    - *延期* - 当物料报告为完工入库时，系统将成品标记为实际可用，并将日记帐过帐添加到消息队列中。 在将成品标记为实际可用之前，系统不会等到过帐被完全处理。

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>安排消息处理器批处理作业以处理延期过帐

消息处理器批处理作业在日记帐过帐排队后负责处理它们。 若要确保处理日记帐过帐，您必须将此作业配置为按常规间隔运行。 使用以下过程设置所需的批处理作业。

1. 转到 **系统管理 \> 消息处理器 \> 消息处理器**。
1. 在 **参数** 快速选项卡上，将 **消息队列** 字段设置为 *生产*。
1. 在 **在后台运行** 快速选项卡上，将 **批处理** 选项设置为 *是*。 然后设置定期计划，并根据需要配置其他设置。 这些设置的工作方式与它们用于 Microsoft Dynamics 365 Supply Chain Management 中其他类型的[后台作业](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)时一样。

## <a name="track-the-progress-of-your-deferred-postings"></a>跟踪延期过帐的进度

延迟的日记帐过帐将作为 *消息处理器消息* 排队，一直等到 *消息处理器* 将其处理。 应设置消息处理器以作为计划的批处理作业运行。 若要查看消息处理器已处理或将要处理的延期过帐消息，请转到 **生产控制 \> 生产订单 \> 延期的生产订单过帐**。

### <a name="message-grid-columns-and-filters"></a>消息网格列和筛选器

您可以使用 **延期的生产订单过帐** 页面顶部的字段帮助查找要查找的任何特定消息。

提供以下筛选器：

- **消息类型** - 指定网格中显示的消息的类型。
- **消息状态** - 指定网格中显示的消息的状态。 存在以下状态：

    - *已排队* – 消息已准备好由消息处理器处理。
    - *已处理* – 消息已由消息处理器成功处理。
    - *已取消* - 消息在最终尝试期间无法被处理，随后被用户取消。
    - *失败* - 上次尝试期间无法处理消息。 系统将重试失败的消息三次。 然后，它将放弃并使消息处于 *失败* 状态。 请注意，在这三次尝试中的最后一次之后，您才能手动取消或编辑消息。

- **消息内容** – 此筛选器对消息内容进行全文搜索。 （消息内容未在网格中显示。）此筛选器将大多数特殊符号（例如连字符）视为空格字符，并将所有空格字符视为布尔 OR 运算符。 例如，如果您搜索等于 *USMF-123456* 的特定 `journalid` 值，系统将查找包含“USMF”或“123456”的所有消息。 在这种情况下，结果列表可能很长。 因此，最好只输入 *123456*，因为您将获得更具体的结果。

您还可以通过选择任何列标题并在下拉对话框中输入条件来对列表进行排序和筛选。

### <a name="view-the-message-log-message-content-and-details"></a>查看消息日志、消息内容和详细信息

您可以通过以下方式查找有关消息的详细信息：在网格中选择该消息，然后选择消息网格下的 **日志** 或 **原始内容** 选项卡，其中会显示每个处理事件。

**日志** 选项卡上的工具栏包括以下按钮：

- **日志** - 选择此按钮可以显示处理结果。 当消息的 **处理结果** 值为 *失败*，并且您希望了解处理失败的原因时，此按钮尤其有用。
- **捆绑** – 多个消息处理操作可以作为同一个批处理流程的一部分运行。 选择此按钮可以查看此详细数据。 例如，您可以查看是否存在需要某些消息的特定处理顺序的依赖项。

### <a name="manually-process-or-cancel-a-message"></a>手动处理或取消消息

需要时，您可以根据消息的当前状态手动处理或取消消息。 在网格中选择消息，然后在操作窗格上选择 **处理** 或 **取消**。

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>设置业务事件以为失败的处理结果发送警报

您可以设置[业务事件](../../fin-ops-core/dev-itpro/business-events/home-page.md)，以提醒您注意失败的处理结果。 转到 **系统管理 \> 设置 \> 业务事件 \> 业务事件目录**，并激活名为 *消息处理器消息已处理* 的业务事件。

作为激活流程的一部分，将提示您指定事件是特定于一个法人还是适用于所有法人。 还会提示您提供 **终结点名称** 值。 必须首先定义此值。

> [!NOTE]
> 如果将 **当业务事件发生时** 字段设置为 *Microsoft Power Automate*（比如不是 *HTTPS*），将基于 *Microsoft Power Automate* 设置在 Supply Chain Management 中自动创建 **终结点名称** 值。
