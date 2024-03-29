---
title: 部分库位周期盘点
description: 周期盘点计划指导实际盘点操作。 您可以要求仅盘点特定的产品和产品变型，无需对库位中的所有现有库存进行盘点。
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f06b39f3c2d2f5a0bdfef1da9395c71686ed46968a1143305b5a10787f7e85f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778426"
---
# <a name="partial-location-cycle-counting"></a>部分库位周期盘点

[!include [banner](../includes/banner.md)]

周期盘点计划指导实际盘点操作。 您可以要求仅盘点特定的产品和产品变型，无需对库位中的所有现有库存进行盘点。

通过使用周期盘点计划创建盘点工作，您可以指导实际盘点操作。 您可以要求仅盘点特定的产品和产品变型，无需对库位中的所有现有库存进行盘点。 通过筛选特定产品，仓库经理可以降低审核开销，避免合并错误和节省时间。

## <a name="how-to-configure-partial-location-cycle-counting"></a>如何配置部分库位周期盘点

当您对盘点操作使用仓库工作流程时，为每个库位创建一个工作标题。 当您定义周期盘点计划时，可以使用 **选择库位** 查询以限制创建的周期盘点工作。 为周期盘点计划选择产品时，可以同时选择产品和产品变型查询以细化盘点内容。

您可以将 **工作模板** 与周期盘点计划相关联，以定义创建周期盘点工作的方式。 用于盘点操作的工作模板从周期盘点计划中直接引用。

定义工作模板详细信息时，可以使用 **工作换行符** 选项以指定是否必须按照物料编号或产品变型编号对盘点工作行分组。 如果您要仅对一个库位中的特定产品盘点现有库存，则必须进行此设置。 创建的周期盘点工作行将具有您在此处定义的信息级别，并将基于此级别处理指导的盘点操作。

如果您使用 **工作换行符** 选项将周期盘点计划与工作模板相关联，则为创建的周期盘点工作选择 **部分周期盘点** 字段，并将基于工作模板的定义创建多个周期盘点工作行。

可以处理部分周期盘点工作前，您必须至少为移动设备菜单项选择 **显示物料编号** 作为周期盘点设置的一部分。 系统将要求仓库操作员仅记录与盘点行相关联的盘点信息（物料编号和产品维度）。 此盘点流程将忽略所有其他现有库存。

对于部分周期盘点流程，不会更新此库位的 **上一次周期盘点** 日期/时间，即使盘点了给定库位的所有物料也不例外。 部分周期盘点不会考虑 **周期盘点计划** 页面中的参数 **周期盘点之间的天数**。 部分周期盘点不支持同时盘点同一个库位的多个物料。 部分周期盘点功能可能导致在运行 **处理周期盘点计划** 时，多次为一个物料盘点同一个库位。 若要避免此情况，请在 **选择库位** 字段中指定筛选器。

> [!NOTE]
> 在使用部分周期盘点流程时，仓库管理移动应用不提供 **添加 LP 或物料** 按钮。

## <a name="example"></a>示例

在此示例中，仅须盘点仓库 61 中的物料编号 A0001。

1. 为周期盘点创建新的工作模板。 **工作换行符** 选项用于按物料编号对盘点工作行分组。 因此，创建的周期盘点工作的每个物料编号有多行。 您还可以按产品变型编号对行分组。
1. 创建引用新建工作模板的新周期盘点计划。 周期盘点计划包括拥有物料编号 A0001 库存的仓库 61 中的所有库位（**选择库位** 查询）。 特定产品的选择在 **周期盘点产品选择** 部分定义。
1. 您可以通过将 **空库位** 字段设置为 **排除空库位** 来为周期盘点计划选择产品。 在处理周期盘点计划时，物料编号 A0001 的部分周期盘点工作将创建。 使用用于指导的周期盘点的移动设备菜单项可以执行实际盘点流程。

## <a name="additional-resources"></a>其他资源

[周期盘点](cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]