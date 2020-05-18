---
title: 通过 Warehouse 应用进行的牌照收货
description: 此主题介绍如何设置 Warehousing 应用以支持使用牌照收货流程接收实际库存。
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346368"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>通过 Warehouse 应用进行的牌照收货

此主题介绍如何设置 Warehousing 应用，以便支持使用牌照收货流程接收实际库存。

可使用此功能快速记录与发货通知 (ASN) 有关的入站库存的收货。 当使用仓库管理流程为转移单发货时，系统将自动创建 ASN。 对于采购订单流程，ASN 可以手动创建，也可以使用入站 ASN 数据实体流程自动导入。

ASN 数据将通过*装箱结构*链接到负荷和装运，其中的托盘（父牌照）中包含货箱（嵌套牌照）。

> [!NOTE]
> 为了在使用具有嵌套牌照的装箱结构时减少库存交易记录数量，系统记录父牌照中的实际现有库存。 为了基于装箱结构数据触发实际现有库存从父牌照到嵌套牌照的转移，移动设备必须提供基于*打包到嵌套的牌照*工作创建流程的菜单项。

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>显示或跳过收货摘要页

可使用*控制是否在移动设备上显示收货摘要页*功能在牌照收货流程中利用更详细的 Warehouse 应用流程。

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在**功能管理**工作区中，此功能按照下面的方式列出：

- **模块**：*仓库管理*
- **功能名称**：*控制是否在移动设备上显示收货摘要页*

开启此功能之后，牌照收货或牌照收货加入库处理的移动设备菜单项将提供**显示收货摘要页**设置。 此设置具有以下选项：

- **显示详细摘要** – 牌照收货期间，工作人员将看到一个额外页面，其中显示完整的 ASN 信息。
- **跳过摘要** – 工作人员将看不到完整的 ASN 信息。 仓库工作人员也将无法在接收过程中设置处置代码或添加例外。

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>阻止转移单已装运牌照用于目标仓库以外的其他仓库

如果 ASN 中包含已存在的牌照 ID，并且具有的实际现有数据所在仓库位置不是牌照的登记仓库位置，则不能使用牌照收货流程。

对于中转仓库不跟踪牌照（因此也不跟踪每个牌照的实际现有库存）的转移单方案，可使用*阻止转移单已装运牌照用于目标仓库以外的其他仓库*功能阻止中转中的牌照的实际现有更新。

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在**功能管理**工作区中，此功能按照下面的方式列出：

- **模块**：*仓库管理*
- **功能名称**：*阻止转移单已装运牌照用于目标仓库以外的其他仓库*

若要在此功能可用时管理功能，请执行以下步骤。

1. 转到**仓库管理 \> 设置 \> 仓库管理参数**。
1. 在**常规**选项卡的**牌照**快速选项卡上，将**中转仓库牌照政策**字段设置为以下值之一：

    - **允许重复使用非跟踪牌照** – 系统的工作方式与*阻止转移单已装运牌照用于目标仓库以外的其他仓库*功能不可用时的工作方式相同。 此值是首先激活此功能时的默认设置。
    - **防止重复使用非跟踪牌照** – 收到转移单之前，目标仓库中仅允许与装运的牌照有关的现有更新。

## <a name="more-information"></a>更多信息

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

有关移动设备菜单项的详细信息，请参阅[为仓库工作设置移动设备](configure-mobile-devices-warehouse.md)。
