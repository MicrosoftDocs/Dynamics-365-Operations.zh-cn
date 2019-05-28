---
title: 预警的批处理
description: 此主题提供有关在 Microsoft Dynamics 365 for Finance and Operations 中批处理预警的信息。
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 482cf30b4f82e8801ebc12e3925c1efb09f7eb1e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546977"
---
# <a name="batch-processing-of-alerts"></a>预警的批处理

[!include [banner](../includes/banner.md)]

预警由 Microsoft Dynamics 365 for Finance and Operations 中的批处理功能来处理。 您必须首先设置批处理，然后才可以发出预警。

Finance and Operations 支持两个事件类型：

- 由基于更改的事件而触发的事件。 这些事件也称作创建/删除和更新事件。
- 按到期日期触发的事件。

您可以为各个事件类型设置批处理。
        
## <a name="batch-processing-for-change-based-events"></a>基于变化的事件的批处理

Finance and Operations 读取自上次批处理运行以来出现的所有基于变化的事件。 基于变化的事件包括更新字段、删除记录和创建记录。 这些事件与预警规则中设置的条件进行比较。 事件与规则中的条件匹配时，批处理将生成预警。

### <a name="frequency-for-change-based-events"></a>基于变化的事件的频率

对于基于变化的事件，您可以设置一个批处理作业，在系统记录某事件后立即触发对该事件的处理。 如果您设置批处理作业以更高的频率重复，用户将在更改后很快收到其预警。 但是，批处理的高频率可能冲销对系统性能的影响。

另一方面，在系统负载过低时，重复频率过低、安排的时间较短的批处理作业可能有助于提高系统性能。 但是，批处理的频率过低可能不能及时满足用户对预警的需求。

因此，在为基于变化的事件设置批处理频率时，既要考虑预警的及时性，又要考虑整个系统的性能。 当创建预警规则的用户增多时，这些注意事项的相关性就会升高。 频率不影响必须处理的事件的数量。 但是，如果创建规则的用户越多，必须执行的支票就越多。 这类数据交换可能会影响系统性能。

#### <a name="the-risks-of-low-batch-frequency"></a>低批处理频率的风险

如果为基于变化的事件的批处理设置了低频率，则与预警规则中的条件相关的数据可能在批处理执行前就已变化。 因此，您可能错过预警。

例如，当事件为**客户联系信息更改**且条件为**客户 = BB** 时，设置预警规则以触发预警。 换言之，当客户 BB 的客户联系人更改时，事件就被记录下来。 但是，对批处理系统进行设置，以便批处理出现的频率小于数据输入出现的频率。 如果事件处理之前客户名称从 **BB** 更改为 **AA**，那么数据库中的数据不再符合规则（**客户= BB**）中的条件。 因此，最后在事件处理时，不会生成任何预警。

### <a name="set-up-processing-for-change-based-alerts"></a>设置基于变化的预警的处理

1. 转到**系统管理** &gt; **定期任务** &gt; **预警** &gt; **基于变化的预警**。
2. 在**基于变化的预警**对话框中，输入相应的信息。

## <a name="batch-processing-for-due-date-events"></a>到期日期事件的批处理

Finance and Operations 会检测到所有由到期日期导致的事件，并将这些事件与预警规则中设置的条件进行比较。 批处理在事件与规则中的条件匹配时生成预警。

### <a name="frequency-for-due-date-events"></a>到期日期事件的频率

对于到期日期事件，您最好将批处理作业设置为在一天中的晚上或其他具体时间运行，以便平衡系统负荷。 我们建议您设置批处理作业，以使其每天至少运行一次。 如果应尽可能早地发送预警，将批处理设置为在系统日期变化后立即进行。 如果希望为在批处理作业已处理预警后发生的到期日期事件生成预警，则可以在同一天再次运行该批处理作业。

例如，批处理作业已按特殊日旁运行。 然后，您可以创建具有到期日期的采购订单，该日期应在同一天触发预警。 要在该天接收预警，必须在创建采购订单后再次运行批处理作业。 不过，如果当天未再次运行该批处理作业，则第二天的批处理作业就会删除前几天未处理的任何到期日期事件。

> [!NOTE]
> 即使在批处理运行的频率超过一天一次时，也不会为同一到期日期事件和条件重复预警。 仅当日期因系统在上次批处理作业运行后发生了更改而到期时，才会为之生成预警。

### <a name="batch-processing-window"></a>批处理时间范围

公司中预警规则的处理停止原因可有很多种。 这些原因包括假期、系统错误，或者阻止批处理作业在一段时间内运行的其他问题。

为了防止到期日期预警因为批处理作业数天未运行而过时，您可以设置批处理窗口。 批处理窗口可以用于阻止批处理作业在指定的运行天数内运行。

如果设置批处理窗口，预警在预警规则处理时发送，即使预警超过了到期日期条件中定义的时间限制。 只要由此时间限制和批处理窗口定义的期间未超过，预警就会继续被发送。 但是，当由时间限制和批处理窗口定义的期间超过时，不再发送预警。

### <a name="set-up-processing-for-due-date-alerts"></a>设置到期日期预警的处理

1. 转到**系统管理** &gt; **定期任务** &gt; **预警** &gt; **到期日期预警**。
2. 在**到期日期预警**对话框中，输入相应的信息。
