---
title: 计划优化故障排除
description: 本文介绍如何解决在使用计划优化时可能遇到的问题。
author: t-benebo
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f078fda02a11eb2073738d59b45f81698b707653
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889510"
---
# <a name="troubleshoot-planning-optimization"></a>计划优化故障排除 

[!include [banner](../../includes/banner.md)]

本文介绍如何解决在使用计划优化时可能遇到的常见问题。

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>无法完成计划优化加载项的安装

计划优化需要已启用 Lifecycle Services (LCS) 的第 2 层或更高层高可用性环境（非 OneBox 环境），并且具有 Dynamics 365 Supply Chain Management 版本 10.0.7 或更高版本。 如果尝试在 OneBox 环境中安装此加载项，将无法完成安装。

**解决方法**：取消安装，然后使用第 2 层或更高层高可用性环境（非 OneBox 环境）。

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>启用计划优化后计划批处理作业失败

启用计划优化时，将自动禁用内置主计划引擎。 如果在启用了计划优化的情况下触发了为内置 Supply Chain Management 计划引擎创建的主计划批处理作业，这些作业将失败。 可能会收到如下错误消息：*启用了计划优化时此操作触发了不支持的主计划*。

**解决方法**：取消为内置 Supply Chain Management 计划引擎创建的所有主计划批处理作业。

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>计划优化结果与之前结果不同

计划优化在某些方面与内置主计划设计不同。 这也可能是待定功能导致的。

**解决方法**：运行计划优化适应分析，然后在引用相关文档了解影响时分析结果。 有关详细信息，请参阅[计划优化拟合分析](planning-optimization-fit-analysis.md)。

## <a name="cant-enable-planning-optimization"></a>不能启用计划优化

**连接状态** 必须先为 **已连接**，然后才能将 **使用计划优化** 设置为 **是**。 有关详细信息，请参阅[开始使用计划优化](get-started.md)。

**解决方法**：确保已成功安装了计划优化加载项。

## <a name="error-message-is-shown-during-ctp"></a>CTP 期间显示错误消息

如果在已启用了计划优化的情况下从销售订单运行可承诺量 (CTP)，将收到以下错误消息：*启用了计划优化时此操作触发了不支持的主计划*。

这与为了支持生产订单时计划的待定功能有关。

**解决方法：** 启用计划优化后避免计算 CTP，直到 CTP 支持可用。

## <a name="additional-resources"></a>其他资源

[开始使用计划优化](get-started.md)

[计划优化适应分析](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]