---
title: 消息处理程序消息
description: 本主题提供有关缩放单元工作负荷的消息处理器消息功能的信息。
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 76a3cc316da322c7997072c00780f2fc133bfd2a02274b1e53f5cd06cfb1277e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748851"
---
# <a name="message-processor-messages"></a>消息处理程序消息

[!include [banner](../includes/banner.md)]

当为[制造工作负荷](cloud-edge-workload-manufacturing.md)和[仓库管理工作负荷](cloud-edge-workload-warehousing.md)运行云和边缘缩放单元时，将使用消息处理器消息。

会有大量数据在中心和缩放单元部署环境之间进行交换以保持同步，但是 *消息处理器* 将仅处理其中的少数数据交换。 您可以转到 **系统管理 > 消息处理器 > 消息处理器消息** 查看消息处理器处理的消息。

## <a name="message-grid-columns-and-filters"></a>消息网格列和筛选器

您可以使用 **消息处理器消息** 页顶部的字段帮助查找要查找的任何特定消息。 这些筛选器中的大多数与消息网格中的列标题匹配。 提供以下筛选器和列标题：

- **消息类型** – 指定消息的类型。
- **消息队列** – 指定要处理其中的消息的队列的名称。 提供以下队列：
  - *缩放单元到中心*
  - *中心到仓库执行缩放单元*
  - *中心到制造执行缩放单元*
- **消息状态** – 指定消息的状态。 存在以下状态：
  - *已排队* – 消息已准备好由消息处理器处理。
  - *已处理* – 消息已由消息处理器成功处理。
  - *已取消* – 消息已处理，但处理失败。
- **消息内容** – 此筛选器对消息内容进行全文搜索。 （消息内容未在网格中显示。）此筛选器将大多数特殊符号（例如“-”）视为空格，并将所有空格字符视为布尔 OR 运算符。 T=例如，这意味着如果您搜索等于“USMF-123456”的特定 `journalid` 值，系统将查找所有包含“USMF”或“123456”的消息，这可能是一个很长的列表。 因此，最好只输入“123456”，因为这样会返回更具体的结果。

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>示例消息类型：请求库存调整财务更新

例如，*请求库存调整财务更新* 这一 **消息类型** 用于在工作人员使用仓库应用在缩放单元仓库管理工作负荷上[登记库存调整](cloud-edge-warehouse-inventory-adjustment.md)时，在中心创建和过帐盘点日记帐。 由于此特定流程源自缩放单元，因此 **消息队列** 字段将显示值 *缩放单元到中心*。

对于此消息类型，缩放单元工作负荷将消息记录为仓库应用库存调整操作的一部分。 然后，消息数据将作为用于 [Commerce data exchange 体系结构](../../commerce/commerce-architecture.md)的同一流程的一部分转移到中心。 消息将更新为 **消息状态** 显示 *已排队*。 然后，消息处理器将尝试处理消息，如果成功，会将 **消息状态** 更新为 *已处理*，如果失败，则更新为 *已取消*。

## <a name="view-the-message-log-message-content-and-details"></a>查看消息日志、消息内容和详细信息

您可以通过以下方式查找有关消息的详细信息：在网格中选择该消息，然后打开消息网格下的 **日志** 或 **消息内容** 选项卡，其中会显示每个处理事件。

**消息内容** 取决于 **消息类型**，因此具有不同的文本长度。 典型的消息内容文本将以 **{** 开头，以 **}** 结尾，中间有字段名称（如 `journalId`），后跟 **:** 和一个值（如 *USMF-123456*）。

**日志** 选项卡上的工具栏包括以下按钮：

- **日志** – 显示处理结果。 这对于理解 **处理结果** 为 *失败* 的消息为何处理失败的原因特别有用。
- **捆绑** – 多个消息处理操作可以作为同一个批处理流程的一部分运行。 选择此按钮可以查看此详细数据。 例如，您可以查看是否存在需要系统以特定顺序处理某些消息的依赖项。

## <a name="message-processor-batch-job"></a>消息处理器批处理作业

在运行云和边缘部署时，在创建新消息以进行处理时，将自动引发 *消息处理器* 批处理作业，因此，您应该无需手动计划此作业。

如有必要，您可以转到 **系统管理 > 消息处理器 > 消息处理器** 来访问此批处理作业。

## <a name="manually-process-or-cancel-a-message"></a>手动处理或取消消息

如果需要，您可以根据消息的当前状态手动处理或取消消息。 要执行此操作，在网格中选择消息，然后在操作窗格上选择 **处理** 或 **取消**

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>设置业务事件以为失败的处理结果发送警报

除了筛选 **消息状态** 值 *已取消* 来查询失败的消息外，您还可以在中心设置[业务事件](../../fin-ops-core/dev-itpro/business-events/home-page.md)，来提醒您处理结果失败。 要执行此操作，在 **业务事件目录** 页（**系统管理 > 设置 > 业务事件 > 业务事件目录**）上激活名为 *消息处理器消息已处理* 的业务事件。

作为激活流程的一部分，系统将指导您指定事件是特定于一个还是所有法人，并提供必须首先定义的 **终结点名称**。

>[!NOTE]
> 如果将 **当业务事件发生时** 设置为 *Microsoft Power Automate*（比如不是 *HTTPS*），将基于 *Microsoft Power Automate* 设置在 Supply Chain Management 中自动创建 **终结点名称**。

### <a name="microsoft-power-automate-example"></a>Microsoft Power Automate 示例

在此示例中，将 **当业务事件发生时** 与 *Microsoft Power Automate* 配合使用，来发送包含信息日志消息和超链接的电子邮件，以打开中心部署中特定失败消息的 **消息处理器消息** 页。 如果需要，您可以添加额外的逻辑来使用不同的渠道并行发送通知，并根据事件数据控制收件人。

1. 在 [Power Automate](https://preview.flow.microsoft.com) 中，为流触发器 **当业务事件发生时 - Fin & Ops App (Dynamics 365)** 创建一个新的自动化云端流，后跟 **分析 JSON** 和 **发送电子邮件** 步骤，如下图所示。

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate 自动化云端流。":::

1. 在 **当业务事件发生时** 步骤中，您可以查找或输入中心 **实例**，之后是 **类别**，然后是 **业务事件***消息处理器消息已处理*，如下图所示。

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate 当业务事件发生时步骤。":::

1. 对于 **分析 JSON** 步骤，输入定义扩展字段的 **架构**。 您可以使用 Supply Chain Management 中 **业务事件目录** 页上的 *下载架构* 选项，也可以从粘贴示例架构文本开始。 下图之后提供了此示例文本。

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate 分析 JSON步骤。":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. 在 **发送电子邮件** 步骤中，您可以选择各个字段，也可以从将电子邮件正文示例粘贴到 **正文** 字段中开始。 下图之后提供了此示例。

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate 发送电子邮件步骤。":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. 保存业务事件时，它将自动被激活，可以用作 Supply Chain Management 的一部分。
