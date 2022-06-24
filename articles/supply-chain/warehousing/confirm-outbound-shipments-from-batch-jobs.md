---
title: 确认来自批处理作业的出站装运
description: 本文介绍如何设置自动确认准备装运负荷的出站转移单装运的批处理作业。
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875092"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>确认来自批处理作业的出站装运

[!include [banner](../includes/banner.md)]

本文介绍如何设置自动确认准备装运负荷的出站转移单装运的批处理作业。 这里介绍的批处理作业仅适用于转移单装运，不适用于销售订单。

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>打开或关闭“从批处理作业确认出站装运”功能

要使用本文中描述的功能，必须为您的系统打开 *从批处理作业确认出站装运* 功能。 从 Supply Chain Management 版本 10.0.21 开始，此功能默认开启。 从 Supply Chain Management 10.0.25 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.25，管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *从批处理作业确认出站装运* 功能来打开或关闭此功能。

## <a name="process-outbound-shipments"></a>处理出站装运

设置计划的批处理作业来为准备装运的负荷运行出站装运确认：

1. 转到 **仓库管理 \> 定期任务 \> 处理出站装运**。
1. **确认装运** 对话框将打开。 在 **要包括的记录** 快速选项卡中，选择 **筛选**。
1. 查询编辑器对话框将打开。 在 **范围** 选项卡上，添加具有以下值的行：
    - **表** - *负荷*
    - **派生表** - *负荷*
    - **字段** - *负荷状态*
    - **条件** - *已装载*
1. 选择 **确定** 返回到 **确认装运** 对话框。
1. 在 **在后台运行** 快速选项卡上，将 **批处理** 设置为 **是**。
1. 在 **在后台运行** 快速选项卡上，选择 **重复执行**。
1. **定义重复执行** 对话框将打开。 根据业务需要设置运行计划。
1. 选择 **确定** 返回到 **确认装运** 对话框。
1. 在 **确认装运** 对话框中选择 **确定**，将批处理作业添加到批处理队列中。

有关详细信息，请参阅[批处理概览](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]