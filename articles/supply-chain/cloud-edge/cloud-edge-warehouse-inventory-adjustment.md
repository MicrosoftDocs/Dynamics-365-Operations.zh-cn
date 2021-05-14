---
title: 仓库库存调整
description: 本主题提供有关使用缩放单元时仓库库存调整日记帐和处理的信息。
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938218"
---
# <a name="warehouse-inventory-adjustment"></a>仓库库存调整

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

当为[制造工作负荷](cloud-edge-workload-manufacturing.md)和[仓库管理工作负荷](cloud-edge-workload-warehousing.md)运行云和边缘缩放单元时，将使用“仓库库存调整”功能。

当工作人员使用仓库应用针对缩放单元仓库管理工作负荷进行库存调整时，必须由 **仓库库存调整日记帐** 批处理作业处理实际现有量更新，您可以转到 **仓库管理 > 定期任务 > 仓库库存调整日记** 来运行和计划此作业。

以下仓库应用工作流程当前对缩放单元工作负荷使用 **仓库库存调整日记帐**：

- 调入/调出
- 周期盘点
- 牌照加载

由于中心和缩放单元部署共享库存记录，因此在库存调整流程中将多个库存交易创建为云和边缘的一部分。

## <a name="inventory-adjustment-example"></a>库存调整示例

在此示例中，仓库工作人员已使用仓库应用登记了现有库存量的增加。

首先，缩放单元工作负荷为正实际调整创建仓库库存调整交易，然后交易将被同步到中心，致使中心现有库存量增加。

| 类型                                    | 缩放单元 | 方向 | 中心 |
|-----------------------------------------|------------|-----------|-----|
| 仓库库存调整          | +1         | ->        | +1  |

然后，中心处理盘点日记帐过帐，这通过[消息处理器消息](cloud-edge-message-processor-messages.md)接收。 这将更新其他现有库存。 为了防止重叠的现有库存，中心将在此流程中创建抵销交易，并删除与仓库库存调整有关的先前记录的现有库存量。

| 类型                                    | 缩放单元 | 方向 | 中心 |
|-----------------------------------------|------------|-----------|-----|
| 盘点                                | +1         | <-        | +1  |
| 仓库库存调整（抵销） | -1         | <-        | -1  |

缩放单元在中心创建了 **仓库库存调整日记帐** 之后，您可以查看中心作为调整流程一部分创建的 **盘点日记帐** 和 **抵销日记帐**。

您可以通过执行以下步骤在 Supply Chain Management 中查看这些日记帐条目和交易的每一个：

1. 登录到缩放单元。
1. 转到 **仓库管理 \> 定期任务 \> 仓库库存调整日记帐**。
1. 在 **仓库库存调整日记帐** 页上，找到并打开记录库存现有量更改的日记帐。 **日记帐行** 部分显示此日记帐记录的每个调整。
1. 登录到中心。
1. 转到 **仓库管理 \> 定期任务 \> 仓库库存调整日记帐**。
1. 在 **仓库库存调整日记帐** 页上，如果中心和缩放单元已同步，您应该会看到列出的相同日记帐。
1. 打开日记帐。 如果 [消息处理器消息](cloud-edge-message-processor-messages.md)已处理，您将在标头中看到指向 **盘点日记帐** 和 **抵销日记帐** 的链接。
    - **盘点日记帐** 应显示与日记帐行相同的维度值。
    - **抵销日记帐** 应显示将消除重叠的库存调整的抵销量。
    > [!NOTE]
    > 完成所有同步和处理后，**盘点日记帐** 和 **抵销日记帐** 将被同步回缩放单元。 这些内容也可以从相关的 **仓库库存调整日记帐** 页查看。
