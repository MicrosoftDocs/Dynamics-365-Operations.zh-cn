---
title: 物料处理设备接口 (MHAX)
description: 本主题介绍如何设置物料处理设备接口 (MHAX)，让您可以连接到外部物理物料处理 (MH) 系统。
author: Mirzaab
manager: tfehr
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ea021529d7417fb3170c859c7fffcb2cfd23a43f
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571834"
---
# <a name="material-handling-equipment-interface-mhax"></a>物料处理设备接口 (MHAX)

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

您可以使用 *物料处理设备接口* (MHAX) 将外部物理物料处理 (MH) 系统连接到由 Microsoft Dynamics 365 Supply Chain Management 中的高级仓库管理 (WMS) 管理的仓库。 WMS 和 MH 系统之间的接口由两个队列组成：一个队列是出站事件（从 WMS 到 MH），另一个队列是入站事件（从 MH 到 WMS）。 WMS 系统基于在各个工作创建和执行流程中创建的工作行生成出站事件。 然后，MH 系统会定期在 WMS 系统中轮询新事件并处理响应。 MH 系统按照工作说明完成事件处理后，将发送入站事件，如工作行完成和领料短缺。

下图显示了使用 MHAX 集成时的各个元素以及流程发生的顺序。

![MHAX 组件和交互](media/mhax-components.png "MHAX 组件和交互")

这是前图中所示的交互的说明：

1. 在工作创建或工作执行期间，将在出站队列中创建出站事件。
2. MH 设备连接到 MH 设备服务，轮询与之相关的任何新事件，并处理这些事件。
3. 当 MH 设备准备好进行报告时，它将再次连接到服务并提交入站事件。 这些事件将立即由队列处理器处理。
4. 基于入站事件数据，队列处理器可以运行现有工作，对其进行修改或创建新工作。

## <a name="turn-on-the-mhax-feature"></a>开启 MHAX 功能

必须同时打开 MHAX 的功能和配置密钥，然后才能够使用 MHAX 功能。

1. 转到 **系统管理 \> 工作区 \> 功能管理**。
2. 在 **[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** 工作区中，打开名为 *物料处理设备接口* 的功能。
3. 将您的系统置于维护模式下，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。
4. 转到 **系统管理 \> 设置 \> 许可证配置**。
5. 展开 **贸易 \> 仓库和运输管理**，然后选中 **物料处理设备接口** 复选框。
6. 关闭维护模式，如[维护模式](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)中所述。

## <a name="set-mhax-parameters"></a>设置 MHAX 参数

您必须在 **物料处理设备接口参数** 页上设置一些常规参数才能配置此功能。

1. 转到 **物料处理设备接口 \> 设置 \> 物料处理设备接口参数**。
2. 在 **常规** 选项卡上，设置以下字段：

    - **用户 ID** – 选择一个工作人员。 此工作人员将用于运行通过入站队列处理的所有工作操作（领料和放置）。
    - **启用传入消息 ID** – 当此选项设置为 *是* 时，如果收到重复的传入消息 ID，该消息将被拒绝，并显示一条错误消息，指出该消息已存在。 当此选项设置为 *否* 时，将允许重复的传入消息 ID。

3. 在 **编号规则** 选项卡上，选择应用于为入站队列项、出站队列项和工作行对生成唯一 ID 的系统范围的编号规则。

## <a name="outbound-events"></a>出站事件

在工作创建或工作执行期间的特定点，系统将确定是否必须生成要发送到 MH 系统的出站事件。 如果在仓库处理期间为特定点配置了预订，系统将根据预订的设置生成事件。

### <a name="structure-of-outbound-events"></a>出站事件的结构

每个出站事件由出站队列 ID 唯一标识。 出站交易类型确定事件的类型。 仓库和生成事件的预订的 ID 也会在事件中记录。

为了将数据传送到 MH 系统，出站事件包含 10 个数据字段（**data01** 到 **data10**）。 这些数据字段与现有数据库字段具有一对一 (1:1) 映射。 具体而言，它们是从工作行表和工作标题表中的字段提取的。 这些字段可以自由选择。 您在创建预订时设置它们。

除了与现有数据库字段有 1:1 映射的 10 个数据字段外，事件还可以包含称为 *有效负载* 的额外数据字段。 此字段的内容由称为 *有效负载生成器* 的自定义 X++ 代码生成。 应使用的任何有效负载生成器在预订中设置。

为确保 MH 系统仅一次即可接收每个出站队列 ID，状态字段用于指定事件是否已准备好发送到外部系统或是否已经发送。

### <a name="outbound-queue-subscriptions"></a>出站队列预订

在生成任何事件之前，必须设置预订来告知 MHAX 功能是否以及如何生成事件。 生成的事件由预订标识符标记。 因此，多个 MH 系统可以连接到同一个 WMS 系统，但它们的事件保持分开。 当轮询 MHAX 服务查询新事件时，预订是检索事件的可用选项之一。

要创建预订，转到 **物料处理设备接口 \> 设置 \> 预订**。 对于每个预订，以下参数可用：

- **预订 ID** – 标识预订的唯一名称。
- **描述** – 预订的自由文本描述。
- **仓库** – 应按其筛选事件的特定仓库。
- **出站交易类型** – 预订应包含的事件类型。
- **有效负载生成器** – 可选代码扩展，可以在出站事件的 **有效负载** 字段中输入其他信息。

查询可以与每个预订关联。 此查询筛选工作行和标题来进一步限制将使用预订生成事件的工作。 要将查询添加到预订，在 **预订** 页上选中相关预订的 **运行查询** 复选框，然后在操作窗格上选择 **编辑查询**。 标准 Supply Chain Management 查询编辑器将出现。

此外，预订还包括一个 *预订映射*，可根据需要将工作标题或工作行中的字段映射到出站事件的 10 个空闲数据字段的其中一部分或全部。 要将信息返回到 MHAX 服务，通常会包含工作行记录 ID 或 *工作行对 ID*。 （工作行对 ID 是一个新属性，让系统可以使用单个退回命令处理领料和放置行。）其余字段取决于用例。 本主题后面提供了一些示例。

要设置预订映射，在 **预订** 页上选择相关的预订，然后在操作窗格上选择 **预订映射**。 在在出现的 **预订映射** 对话框中，您可以根据需要为每个可用数据字段分配表和字段。

### <a name="outbound-event-types"></a>出站事件类型

本节介绍各个可用的事件类型。 （事件类型也称为 *交易类型*。）另外还说明了每个事件类型是何时在 WMS 系统中创建的。

#### <a name="work-creation-events"></a>工作创作事件

工作创建事件在应用程序生成工作后创建。 此行为适用于大多数类型的工作创建流程，尤其是创建领料和补货工作。 通常，如果工作是在 *未结* 状态下创建的，这表明该工作已准备就绪，可以由工作人员运行，工作创建事件将生成。 此外，还会为基本移动工作（不是通过模板工作移动）生成工作创建事件，即使该工作没有作为未结工作创建。

此行为的一个明显例外是周期盘点工作，它当前不受支持。 MH 系统中的存货盘点不在 MHAX 范围内，盘点结果必须导入库存盘点日记帐。

创建工作后，MHAX 服务将处理所生成的工作行，并为每个工作标题的所有生成的工作行分配工作行对 ID。 目的是将所有领料工作行与连续的放置分组到一个工作行对 ID 下。 （这些组对应于工作模板中的领料/放置对。）通过这种方式，可以使用一个 ID 来报告所有相关领料和放置行的工作完成。 分组流程从第一行开始，然后以相同的 ID 继续，直到遇到连续的放置/领料工作行对。 运行的 ID 将被分配到该对的放置行。 然后，新 ID 将用于之后该对的领料行。 此流程将一直持续到处理完所有属于工作标题的行为止。

作为工作创建事件的一项特殊功能，如果在工作标题上将 **锁定波次** 选项设置为 *是*，生成的事件的状态将为 *锁定*，而不是用于将它们发送到 MH 系统的通常的 *就绪* 状态。 工作标题上的 **锁定波次** 标记表示工作标题尚未准备好供工作人员运行，可能是由于补货工作未完成。 清除 **锁定波次** 标记后，已生成的事件将被解除锁定，可供 MH 系统从队列中检索。

#### <a name="work-initiation-events"></a>工作启动事件

工作启动事件在工作状态在工作更新期间从 *未结* 变为 *进行中* 时触发。

#### <a name="work-completion-events"></a>工作完成事件

工作完成事件在工作状态在工作更新期间从 *进行中* 变为 *已关闭* 时触发。

#### <a name="work-cancellation-events"></a>工作取消事件

工作取消事件在工作状态在工作更新期间从 *已取消* 以外的任何状态变为 *已取消* 时触发。 此外，与工作标题相关的所有其他事件将被从所有预订的队列中删除。 这样，将阻止外部系统处理不需要的事件。

#### <a name="pickput-completion-events"></a>领料/放置完成事件

领料/放置完成事件在领料/放置行的状态在工作行更新期间从 *进行中* 变为 *已关闭* 时触发。

### <a name="monitor-the-outbound-queue"></a>监视出站队列

要查看您的出站队列，请转到 **物料处理设备接口 \> 通用 \> 出站队列**。 **出站队列** 页列出每个出站队列项及其状态。 选择一个队列项来查看其详细信息。 这些详细信息包括项目的交易类型、它使用的预订，以及每个数据字段的值（**data01** 到 **data10**）和有效负载。

### <a name="clean-up-the-outbound-queue"></a>清理出站队列

最终，您的出站队列将开始充满已发送的队列项。 要删除这些项目，请转到 **物料处理设备接口 \> 定期任务 \> 清理 \> 出站队列清理**。

## <a name="inbound-events"></a>入站事件

本节介绍 MH 系统可以向 WMS 系统报告的各个类型的入站事件。 另外还说明了数据必须由 MH 系统提供，以及每个入站事件在 WMS 系统中的作用。

### <a name="structure-of-inbound-events"></a>入站事件的结构

提交入站事件时，外部系统必须提供入站交易类型以及最多 10 个参数（**data01** 到 **data10**）。 可选验证可以确保 MHAX 服务没有多次收到同一个入站事件。 要启用此验证，每个入站事件必须具有唯一的消息 ID。 如果收到重复的消息 ID，并且在 **物料处理设备接口参数** 页上 **启用入站消息 ID** 选项设置为 *是*，该消息将被拒绝。 错误消息将指出该消息已经存在。

除了传入数据字段外，系统还为事件分配唯一的入站队列 ID。

### <a name="inbound-event-types"></a>入站事件类型

本节介绍受支持的入站事件类型（交易类型）以及必须为要处理的事件提供的数据。

#### <a name="work-confirm-events"></a>工作确认事件

工作确认事件需要传入数据字段包括以下信息：

- **data01** – 工作行对 ID。
- **data02** – 工作行记录 ID（`RecId` 值）。

    > [!NOTE]
    > **data01** 字段 *或* 者 **data02** 字段的 *其中一个* 必须存在。

- **data03** – 从其领料的牌照的 ID。
- **data04** – 工作标题的目标牌照 ID。

如果提供了工作行对 ID，将按顺序运行由工作行对 ID 标记、状态为 *未结* 或 *进行中* 的所有领料、放置或自定义工作行。 如果提供了工作行记录 ID（`RecId` 值），工作行必须是状态为 *未结* 或 *进行中* 的领料、放置或自定义工作行。

牌照控制的位置的领料行需要 **data03** 指定应从其领料的牌照，不论行是使用工作行记录 ID 还是工作行对 ID 标记。 **data04** 字段必须指定领料的工作标题的目标牌照。

放置行不接受其他信息。 它们仅基于当前工作行的位置和工作的目标牌照运行。 如果必须在其他位置进行放置，请按照本主题后面[替代事件](#override-events)一节中的介绍更改工作行的位置。

自定义工作行在入站事件中不需要或支持任何其他信息。

#### <a name="short-pick-events"></a>领料短缺事件

领料短缺事件需要传入数据字段包括以下信息：

- **data02** – 工作记录 ID（`RecId` 值）。
- **data03** – 从其领料的牌照的 ID。
- **data04** – 要领料的数量。
- **data05** – 领料短缺异常代码。
- **data06** – 工作标题的目标牌照 ID。

> [!NOTE]
> **data01** 字段不用于领料短缺事件。

此事件类似于工作确认事件，但仅应用于领料行。

#### <a name="override-events"></a><a id="override-events"></a>替代事件

替代事件需要传入数据字段包括以下信息：

- **data01** – 工作记录 ID（`RecId` 值）。
- **data02** – 新位置 ID。

工作行的状态必须为 *未结* 或 *进行中*，并且新位置必须存在。

#### <a name="license-plate-receipt-events"></a>牌照接收事件

牌照接收事件需要传入数据字段包括以下信息：

- **data01** – 要接收的入站牌照的 ID。

系统基于作为 **data01** 字段的值传入的牌照执行牌照接收操作。

### <a name="monitor-the-inbound-queue"></a>监视入站队列

要查看您的入站队列，请转到 **物料处理设备接口 \> 通用 \> 入站队列**。 **入站队列** 页列出每个入站队列项及其状态。 选择一个队列项来查看其详细信息。 这些详细信息包括项目的交易类型、消息 ID，以及每个数据字段的值（**data01** 到 **data10**）。

如果在处理入站事件时发生错误或其他类型的日志项，您可以通过在操作窗格上选择 **错误日志** 来检查日志。

### <a name="inbound-event-processing"></a>入站事件处理

入站事件首先写入到数据库，然后立即（同步）运行。 如果在处理过程中发生错误，事件仍会写入到队列，但状态将设置为 *出错*。 MHAX 服务将错误消息返回到 MH 系统，并将错误日志存储在入站事件记录中供以后调查。

如果错误条件已修复，状态为 *出错* 的事件可以在以后重新处理。 要重新处理，请按照下列步骤之一操作：

- 转到 **物料处理设备接口 \> 通用 \> 入站队列**。 选择相关的入站队列，然后在操作窗格上选择 **重新处理**。
- 转到 **物料处理设备接口 \> 通用 \> 重新处理出错的入站队列**。 将出现一个标准批处理作业对话框。 在那里，您可以设置记录筛选器，并计划或运行批处理作业来重新处理队列。

所有工作操作（领料和放置）均使用在 **物料处理设备接口参数** 页上的 **用户 ID** 字段中选择的工作人员运行。

### <a name="clean-up-the-inbound-queue"></a>清理入站队列

最终，您的入站队列将开始充满已处理的队列项。 要删除这些项目，请转到 **物料处理设备接口 \> 定期任务 \> 清理 \> 入站队列清理**。

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>使用队列管理器快速概览

要快速概览与入站和出站队列相关的所有活动，请转到 **物料处理设备接口 \> 工作区 \> 队列管理器**。 **队列管理器** 页提供了一组选项卡和磁贴，可用于监视和浏览队列。 另外还提供指向本主题中提到的其他大多数页面的有用链接。

## <a name="connect-to-the-mhax-service"></a>连接到 MHAX 服务

MHAX 作为自定义服务实现。 因此，可以通过 SOAP 和 REST 调用对其进行访问。 以下是 SOAP 和 REST 终结点的地址：

- **SOAP：**`https://base_environment_URL/soap/services/WMHEServices`
- **REST：**`https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>从出站队列检索消息

要从出站队列检索消息，请使用以下方法之一：

- 使用 `readOutboundSubscriptionQueue` 根据预订 ID 检索事件。
- 使用 `readOutboundWarehouseQueue` 根据事件类型和仓库 ID 跨多个预订检索事件。