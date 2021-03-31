---
title: 通过提领看板补货
description: 此主题介绍如何使用提领看板进行物料补货用于制造活动。
author: johanhoffmann
manager: tfehr
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07d83e64bcd206ecedc38fa884b5864d1fbd8f68
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216779"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>通过提领看板补货

[!include [banner](../includes/banner.md)]

此主题介绍如何使用提领看板进行物料补货用于制造活动。

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>使用提领看板进行物料补货的工作流
-------------------------------------------------------------------

提领看板可用于将单个物料的看板在仓库和使用物料的生产库位之间移动。 提领看板支持基于提取的物料补货解决方案，其中要求通过提取信号触发特定需求的供应。 

以下方案显示提取信号触发看板的创建以对生产流程进行物料补货的基于提取的补货系统。 

[![提取信号触发看板的创建以对生产流程进行物料补货](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  提领看板
2.  看板“源”库位和用于仓库工作的入库库位
3.  看板“至”库位和生产输入库位
4.  制造流程
5.  仓库看板领料工作
6.  仓库原材料库位
7.  物料仓库
8.  制造仓库

在此方案中，制造流程 (4) 使用来自制造仓库 (8) 的生产输入库位 (3) 的物料。 使用物料处理单元（看板）时，其登记为空。 为物料来源创建补货信号，且创建新看板 (1)。 在这种情况下，物料来源包括物料仓库 (7) 中的库位。 看板物料领料并入库到相同仓库的库位 (2)。 领取物料后，可以准备从库位 2 转移到制造仓库 (8) 中的生产输入库位 (3)。

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>为提领看板配置仓库看板领料工作

要启用提领看板的原材料领取，则为 **看板领料** 工作订单类型配置波次模板、工作模板和库位指令。 此工作订单类型不仅支持提领看板的领料流程。 它还支持制造看板的领料流程。 但是，您可以通过界定波次模板、工作模板和库位指令的方式为每种看板类型配置单独的领料流程。 要界定波次模板、工作模板和库位指令，请在这些实体的查询中对该活动类型（**流程** 或 **转移**）设置条件

## <a name="configure-the-withdrawal-kanban"></a>配置提领看板

用于提领看板的转移活动配置为精益生产流中激活的活动计划的一部分。 作为配置转移活动的一部分，您指定转移的“自”和“到”库位。 配置转移活动后，您可以将其分配到 **提领** 类型的看板规则。 看板规则设定提领看板的策略和配置。 看板的数量定义看板在转移流程期间携带多少个物料处理单元。 选择固定补货策略时使用固定看板数量。 此数量定义为了防止存货或版本存货在需求源被耗尽所需的看板数量。 固定数量可以基于实际需求、历史需求和服务级别进行计算。 以下两个方案介绍如何管理使用提领看板的物料补货。

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>方案 1：使用固定提领看板对生产输入库位补货

制造流程使用来自生产仓库中的生产输入库位的已购买的原材料。 收到供应商提供的原材料后，存储到物料仓库的库位中。 由于对物料的需求在一段时间内被视为稳定，因为设置为在固定数量看板流中供应生产。 在生产输入库位使用看板时，将登记空信号，并在流中添加一个相同类型的新看板。 

空信号可以配置为在完成看板时自动发生。 或者，空信号可以设置为从看板转移面板或手持设备上的菜单提供的手动交互。 看板转移面板是管理看板生命周期中的所有活动的工作区。 

创建看板后，原材料的波次行被添加到物料仓库的看板波次。 在看板转移面板的领料单部分，可以监控从波次创建到工作创建的物料和相关仓库流程的状态，直到物料在“转移自”库位中现有且已准备好随时被转移到生产输入库位。 可以从看板转移模板或从手持设备的菜单完成看板。 

在此方案中，物料仓库中的领料单被作为一个活动进行处理。 物料仓库与生产仓库之间的转移活动被作为一个单独的活动进行处理。 此方法可能很有用，例如如果两个仓库之间的实际距离较大时。 在这种情况下，看板转移活动可以表示卡车负荷。 

如果仓库库位与生产输入库位之间的距离较短，则将转移活动包括在领料流程中可能更有效。 物料领料后，可以直接入库到生产输入库位。 为了支持此流程，您将转移活动配置为处理提领看板的领料工作时自动完成。

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>方案 2：处理看板领料工作时自动完成转移活动

在以下方案中，提领看板的转移活动配置为在同一仓库的两个库位之间转移。 提领看板的转移活动设置为自动完成。 

[![处理看板领料工作时自动完成转移活动](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  原材料和生产的共享仓库
2.  原材料的仓库库位
3.  看板“源”库位和用于仓库工作的入库库位
4.  提领看板
5.  生产输入地点
6.  制造流程

在生产输入库位使用看板后，看板报告为空，并在流中添加一个新看板。 创建看板后，在看板波次中添加一个波次行。 处理看板波次后，创建看板领料的仓库工作。 仓库工作人员处理看板领料工作，并按照工作的指示在仓库库位中领取看板物料。 在此仓库工作人员确认领料后，看板自动完成，并指导仓库工作人员将物料入库到生产输入库位。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]