---
title: 销售历史记录清除性能改进
description: 本主题描述了销售历史记录清理性能改进功能以及如何启用它。
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3c8ad7b0bd46c49fc989be091f44630a6a3eebc1
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985903"
---
# <a name="sales-history-cleanup-performance-improvements"></a>销售历史记录清除性能改进

[!include [banner](../includes/banner.md)]

如果 **销售更新历史记录清理** 定期批处理作业不是经常在具有大量销售更新的环境中运行，可能会花费很长时间。 在这些情况下，*销售历史记录清理性能改进* 功能可以帮助减少运行持续时间并提高可靠性。

此功能用以下方式改进现有清理作业：

- 它将清理拆分为批处理（您可以通过自定义来更改批处理大小）。
- 它将最多运行 2 小时（您可以通过自定义来更改持续时间）。
- 在可能的情况下，它将利用数据库功能来最大程度地减少锁定争用，和避免在清理过程中加入交易表。

启用此功能后，**销售更新历史记录清理** 批处理作业（**销售和市场营销 \> 期间任务 \> 清理 \> 销售更新历史记录清理**）将像以前一样运行，但性能更好，最多运行 2 小时。 这意味着可能需要运行多次才能清理特定保留期限内的所有数据。

## <a name="turn-on-the-sales-history-cleanup-performance-improvements-feature"></a>打开销售历史记录清理性能改进功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*销售和市场营销*
- **功能名称**：*销售历史记录清理性能改进功能*
