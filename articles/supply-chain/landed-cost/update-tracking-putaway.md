---
title: 要储存的更新追踪信息
description: 本主题介绍如何设置和运行“更新储存的追踪信息”定期任务。
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d8e2a42d8e12a5a9cf18e876b6f9e45ecb877881
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500015"
---
# <a name="update-tracking-for-put-away"></a>要储存的更新追踪信息

[!include [banner](../includes/banner.md)]

*更新储存的追踪信息* 定期任务设计为作为夜间定期批处理任务运行。 它标识哪些航程已收到所有库存交易记录，哪些航程没有实际结束日期的值。 然后，它会根据需要将实际结束日期设置为当前日期。

系统为每个 *装运集装箱* 的每个行程 *支线* 创建了 *集装箱活动*。 这些值由创建航程时选择的行程模板定义。 对于每个集装箱活动记录，可以为 **开始日期**、**估计结束日期** 和 **实际结束日期** 字段设置值。 收到一段行程已开始或已完成的确认后，可以更新这些字段。

通常，与确认日期相关的信息由第三方（如货运转运商）提供，因为这些操作在 Microsoft Dynamics 365 Supply Chain Management 外部进行维护。 但是，若要跟踪货物从行程支线到达仓库这一过程（以货物存储为标志），则不需要来自第三方的信息。 因此，可以根据 Dynamics 365 Supply Chain Management 中的信息来确定跟踪。

若要设置和运行 *更新储存的追踪信息* 定期任务，请按照以下步骤操作：

1. 转到 **到岸成本 \> 定期任务 \> 更新储存的追踪信息**。
1. 在 **更新储存的追踪信息** 对话框内的 **参数** 部分中，设置以下字段：

    - **支线** - 选择要更新跟踪的行程部分的唯一标识名称/编号。 所选值必须代表航程到达仓库。
    - **活动** - 选择在所选支线期间进行的活动。 这些值是在跟踪控制中心按行程模板行分配的。

1. 要限制应包含在更新中的记录集，请在 **要包括的记录** 快速选项卡上选择 **筛选器** 按钮。 将出现一个标准查询对话框，您可以在其中定义选择条件、排序条件和联接。 这些字段的工作方式与它们用于 Supply Chain Management 中其他类型的查询时一样。 此处的字段是只读的，显示与您的查询相关的值。
1. 在 **在后台运行** 快速选项卡上，根据需要设置批处理和计划选项，就像您可能在 Supply Chain Management 中对其他类型所做的那样。
1. 选择 **确定** 以应用您的设置，并运行或计划更新。
