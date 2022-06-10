---
title: 集装箱活动实体
description: 本主题提供有关集装箱活动的信息，这些活动用于跟踪装运集装箱的进度。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 7bb2b97e8885e3b1265f0c93585873c8a64f1dfb
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813029"
---
# <a name="container-activities-entity"></a>集装箱活动实体

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

集装箱活动用于跟踪装运集装箱的进度。 为分配给创建装运集装箱时选择的行程模板的每个支线创建了记录。 在通过数据实体创建装运集装箱时也创建了记录。

通常从外部源接收有关在途装运集装箱进度的信息。 集装箱活动实体允许外部源（如货运转运商）直接更新记录。 因此，无需手动更新数据。

## <a name="container-activities-itmcontaineractivityentity"></a>集装箱活动 (ITMContainerActivityEntity)

您可以使用集装箱活动实体 (`ITMContainerActivityEntity`) 创建其他活动记录。 或者，货运转运商可以传递已确认的 **实际结束日期** 值的更新。

| Name | 映射 | 数据类型 | 键 | 强制 |
|---|---|---|---|---|
| 实际结束日期 | ITMContainerActivityTable.ActualEndDate | DateTime | 否 | 否 |
| 交货模式 | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | 否 | 否 |
| 估计结束日期 | ITMContainerActivityTable.EsimatedDate | DateTime | 否 | 否 |
| 行号 | ITMContainerActivityTable.LineNum | 数字(32, 16) | **是** | 否 |
| 备注 | ITMContainerActivityTable.Notes | nvarchar(MAX) | 否 | 否 |
| 活动 | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | 否 | **是** |
| 装运集装箱 | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **是** | **是** |
| 航行 | ITMContainerActivityTable.ShipId | Nvarchar(20) | **是** | **是** |
| 支线 | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | 否 | **是** |
| 服务提供商 | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | 否 | 否 |
| 温度 | ITMContainerActivityTable.ShipTemperature | 数字(32, 6) | 否 | 否 |
| 船舶 | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | 否 | 否 |
| 开始日期 | ITMContainerActivityTable.StartDate | DateTime | 否 | 否 |

## <a name="tracking-control"></a>跟踪控制

跟踪控制中心允许通过更新指定的目标字段来触发指定源字段的更新。 如果使用集装箱活动实体更新了源字段的值和目标字段的值，则目标字段将显示实体值。 此行为与具有 **提前期** 的 *创建类型* 值的跟踪控制记录相关。

对于具有 **状态更新** 或 *空白*（用户定义的值）的 *创建类型* 值的成本区域，系统将根据跟踪控制配置更新航行状态或目标字段。

## <a name="calculated-fields"></a>计算字段

根据其他字段的值计算了集装箱活动记录中的以下字段的值。 虽然这些计算字段未包含在数据实体中，但如果提供了计算所基于的字段，则将设置这些字段。

- **预计天数** = **估计结束日期** – **开始日期**
- **实际天数** = **实际结束日期** – **开始日期**
