---
title: 波次执行通知
description: 本主题介绍波次执行通知并说明如何进行设置。
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 0a61aff10234f40f14d603852be30fec3ba83647
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838074"
---
# <a name="wave-execution-notifications"></a>波次执行通知

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

*波次执行通知* 功能使用业务事件和操作中心来提供与波次执行相关的通知。 它使您可以指定生成通知的事件类型、生成通知的仓库以及接收通知的用户。

导航栏右侧的 **显示消息** 按钮（铃铛符号）指示操作中心消息何时对当前用户可用。 用户可以选择 **显示消息** 按钮以打开操作中心并查看消息。

运行业务流程时，将发生业务事件。 业务流程由任务组成。 在业务流程中，参与其中的用户将执行业务操作以完成这些任务。 业务事件提供一种机制，使外部系统可以从 Finance and Operations 应用程序中接收通知。 这样，系统可以执行业务操作以响应业务事件。 有关详细信息，请参阅[业务事件概述](../../fin-ops-core/dev-itpro/business-events/home-page.md)。

## <a name="turn-on-the-wave-execution-notifications-feature"></a>打开波次执行通知功能

*波次执行通知* 功能只有在系统中打开之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。 在那里，此功能以以下方式列出：

- **模块**：*仓库管理*
- **功能名称**：*波次执行通知*

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>场景：将波次批处理执行通知发送到操作中心

此场景显示通过操作中心将有关波次批处理执行错误的通知发送给特定角色的端到端流。

### <a name="make-demo-data-available"></a>提供演示数据

要采取此方案，必须安装演示数据，并且必须选择 **USMF** 法人。

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>确保在批处理模式下运行波次

1. 转到 **仓库管理 \> 设置 \> 仓库管理参数**。
1. 在 **波次处理** 快速选项卡上，将 **批量处理波次** 选项设置为 *是*。

> [!NOTE]
> 如果要禁用波次批处理执行通知，请将 **禁用波次处理批处理通知** 选项设置为 *是*。

### <a name="configure-a-wave-notification-policy"></a>配置波次通知策略

波次通知策略定义发送的通知类型和收到通知的用户。

1. 转到 **仓库管理 \> 设置 \> 波次 \> 波次通知策略**。
1. 创建一个具有以下设置的记录：

    - **波次通知策略**：*24BatchError*
    - **描述**：*仓库 24 波次批处理错误*
    - **发送以下通知**：*仅错误*
    - **目标角色**：*系统管理员*

        > [!NOTE]
        > 由于此场景使用演示数据，因此为简单起见，选择 *系统管理员* 角色。 由于您以系统管理员用户身份登录，因此您将收到通知。 但实际上，您通常应该选择一个更具体的角色（例如 *仓库经理*）来通知波次批处理执行错误。

1. 在操作窗格上，选择 **保存**。

### <a name="configure-a-wave-template"></a>配置波次模板

波次模板使您可以将波次方法的特定实例链接到相应的波次标签模板。

1. 转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。
1. 在列表窗格中，将 **波次模板类型** 字段设置为 *装运*，然后为仓库 24 选择 *24 装运默认* 波次模板。
1. 在 **常规** 快速选项卡上，将 **波次通知策略** 字段设置为 *24BatchError*。

### <a name="configure-a-work-template"></a>配置工作模板

在波次执行期间使用工作模板生成工作。 对于这种情况，波次执行应触发错误。 通过将工作模板查询设置为使用不存在的仓库，您将确保波次执行失败并因此发送通知。

1. 转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。
1. 在列表窗格中，将 **工作模板类型** 字段设置为 *销售订单*，然后为仓库 24 选择 *24 SO 阶段* 工作模板。
1. 在操作窗格上，选择 **编辑查询**。
1. 在查询编辑器对话框中，在 **范围** 选项卡上，编辑以下行（或添加行，如果不存在）：

    - **表**：*临时工作事务*
    - **派生表**：*临时工作事务*
    - **字段**：*仓库*
    - **标准：** 将值从 *24* 更改为 *错误*。

1. 选择 **确定**，然后确认更改。

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>创建销售订单并将其下达到仓库

1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。
1. 创建具有以下设置的销售订单：

    - **客户帐户**：*US-001*
    - **仓库**：*24*

1. 在 **销售订单行** 快速选项卡上，添加具有以下设置的销售订单行：

    - **物料编号：***A0001*
    - **数量：** *10*

    > [!NOTE]
    > 这些物料和数量仅是示例。 指定的仓库必须包含足够的存货。

1. 在 **销售订单行** 快速选项卡上仍选择新行时，在工具栏上选择 **库存 \> 预留**。
1. 在 **预留** 页的操作窗格中，选择 **预留批次**。 然后关闭页面。
1. 在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。

### <a name="notifications-from-wave-batch-job-execution"></a>来自波次批处理作业执行的通知

根据业务事件的设置，您最终将收到有关波次执行失败的通知。 操作中心消息将类似于以下示例，并将包括指向失败波次的链接。

> **波次执行期间出错**  
> 执行波次 USMF-000000001 时出错。  
> 最新消息：没有为波次 USMF-000000001 创建任何工作。
>
> **状态**  
> 可用
>
> 打开波次详细信息

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
