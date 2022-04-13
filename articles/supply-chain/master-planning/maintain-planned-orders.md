---
title: 维护计划订单
description: 本主题提供有关如何管理计划订单的信息。 介绍如何更新计划订单的状态，确定计划订单，并筛选与所选计划订单具有相同状态的计划订单。
author: t-benebo
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bf3efec234ea4d22c01e1b48b3548dad7577a2b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468571"
---
# <a name="maintain-planned-orders"></a>维护计划订单

[!include [banner](../includes/banner.md)]

本主题提供有关如何管理计划订单的信息。 介绍如何更新计划订单的状态，确定计划订单，并筛选与所选计划订单具有相同状态的计划订单。

您可以从 **主计划** 工作区、**计划订单** 列表或 **计划生产订单**、**计划采购订单** 和 **计划转移** 列表中管理计划订单。 

## <a name="planned-order-status"></a>计划订单状态
您可以使用 **状态** 字段帮助跟踪您的进度。 使用了以下值：

-   当主计划生成计划订单时，该计划订单状态为 **未处理**。
-   如果您决定不确认某一计划订单，则可以给予其状态 **已完成**。
-   如果要确认计划订单，可将状态更改为 **已审核**。 主计划会考虑状态为 **已审核** 的计划订单，所以不会在随后的主计划运行期间修改或删除这些订单。 为此，计划逻辑会在主计划期间将 **已审核** 的计划订单从旧计划版本复制到新计划版本。

## <a name="firming-planned-orders"></a>确认计划订单 
确认计划订单即创建实际订单。 这些也称为 *已下达订单* 或 *未结订单*。 确认计划订单时，该订单将移至相关模块的订单部分。

可以从 **计划订单** 页选择两个确认选项：

-   **确认** – 这将确认选择的一个或多个计划订单。
-   **全部确认** – 这将确认筛选器中的所有计划订单。 如果使用 **全部确认**，则不必选择计划订单，因为将确认筛选器中的所有计划订单。 如果要确认大量计划订单，此选项非常有用。

> [!NOTE]
> 可从 **计划订单窗体 > 视图 > 确认历史记录** 下的 **确认历史记录** 跟踪已确认的计划订单。

## <a name="parallelize-firming"></a>并行确认
如果计划同时确认大量订单，并行化运行可改善运行时间或性能。 在使用 **确认** 或 **全部确认** 确认多个计划订单时，可以使用此选项。 提供了以下参数：

-   **并行确认** – 如果设置为 **是**，则使用 **线程数** 中定义的线程数并行化确认流程。
-   **线程数** – 控制用于并行化确认流程的线程的数量。 仅当 **并行确认** 设置为 **是** 时，才显示此参数。

> [!NOTE]
> **并行确认** 选项仅在您选择了多个要确认的计划订单时显示。

## <a name="additional-resources"></a>其他资源

[主计划概览](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]