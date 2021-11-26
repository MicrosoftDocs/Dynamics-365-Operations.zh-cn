---
title: 通过仓库管理移动应用的牌照接收
description: 本主题说明如何设置仓库管理移动应用以支持使用牌照接收流程接收实际库存。
author: perlynne
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 872a08241f3d0156d0ccf1f89443e3a894656404
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777581"
---
# <a name="license-plate-receiving-via-the-warehouse-management-mobile-app"></a>通过仓库管理移动应用的牌照接收

[!include [banner](../includes/banner.md)]

本主题说明如何设置仓库管理移动应用，以便支持使用牌照接收流程接收实际库存。

可使用此功能快速记录与发货通知 (ASN) 有关的入站库存的收货。 当使用仓库管理流程为转移单发货时，系统将自动创建 ASN。 对于采购订单流程，ASN 可以手动创建，也可以使用入站 ASN 数据实体流程自动导入。

ASN 数据将通过 *装箱结构* 链接到负荷和装运，其中的托盘（父牌照）中包含货箱（嵌套牌照）。

> [!NOTE]
> 为了在使用具有嵌套牌照的装箱结构时减少库存交易记录数量，系统记录父牌照中的实际现有库存。 为了基于装箱结构数据触发实际现有库存从父牌照到嵌套牌照的转移，移动设备必须提供基于 *打包到嵌套的牌照* 工作创建流程的菜单项。

## <a name="warehousing-mobile-device-app-processing"></a>仓库移动设备应用处理

当工作人员扫描传入的牌照 ID 时，系统会初始化牌照接收流程。 根据此信息，牌照的内容（来自 ASN 的数据）在入库台货位进行实际登记。 接下来的流程将取决于您的业务流程需求。

## <a name="work-policies"></a>工作策略

与（举例）*完工入库* 移动设备菜单项流程一样，牌照接收流程基于定义的设置支持多个工作流。

### <a name="work-policies-with-work-creation"></a>有工作创建的工作策略

当您使用创建工作的工作策略登记传入的物料时，系统会为每次登记生成并保存储存工作记录。 如果您使用 *牌照接收和储存* 工作流程，登记和储存将使用单个移动设备菜单项作为单个操作处理。 如果您使用 *牌照接收* 流程，接收和储存流程将作为两个不同的仓库操作处理，每个操作有自己的移动设备菜单项。

### <a name="work-policies-without-work-creation"></a>无工作创建的工作策略

您可以在不创建工作的情况下使用牌照接收流程。 如果您定义工作订单类型为 *转移收货* 和/或 *采购订单* 的工作策略，然后您将流程用于 *牌照接收（和储存）*，以下两个 Warehousing mobile app 流程将不会创建工作。 取而代之的是，他们只会在入站收货台的牌照上登记入站实际库存。

- *牌照接收*
- *牌照接收和储存*

> [!NOTE]
> - 您必须在 **库存货位** 部分为工作策略定义至少一个位置。 您不能为多个工作政策指定相同的位置。
> - 仓库移动设备菜单项的 **打印标签** 选项不会在不创建工作的情况下打印牌照标签。

要使此功能在您的系统上可用，您必须在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开 *牌照接收增强* 功能。

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>在不跟踪牌照的位置接收库存

即使未打开 **使用牌照跟踪**，也可以使用分配给货位模板的仓库货位。 因此，当您接收库存时，可以直接在某个位置登记现有库存量，而无需创建工作。

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>为仓库中的每个接收位置添加移动设备菜单项

*牌照接收增强* 功能使您可以通过在 Warehousing mobile app 中添加位置特定的牌照接收（和储存）菜单项，来在仓库中的任何位置接收。 以前，系统仅支持在为每个仓库定义的默认位置接收。 但是，打开此功能后，牌照接收（和储存）的移动设备菜单项现在会提供 **使用默认数据** 选项，可让您为每个菜单项选择一个自定义的“接收”位置。 （此选项已经可用于某些其他类型的菜单项。）

要使此功能在您的系统上可用，您必须在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开 *牌照接收增强* 功能。

## <a name="show-or-skip-the-receiving-summary-page"></a>显示或跳过收货摘要页

可使用 *控制是否在移动设备上显示收货摘要页* 功能在牌照接收流程中利用其他详细的仓库管理移动应用流。

开启此功能之后，牌照收货或牌照收货加入库处理的移动设备菜单项将提供 **显示收货摘要页** 设置。 此设置具有以下选项：

- **显示详细摘要** – 牌照收货期间，工作人员将看到一个额外页面，其中显示完整的 ASN 信息。
- **跳过摘要** – 工作人员将看不到完整的 ASN 信息。 仓库工作人员也将无法在接收过程中设置处置代码或添加例外。

要使此功能在您的系统上可用，必须在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开 *控制是否在移动设备上显示接收摘要页* 功能。 （从 Supply Chain Management 版本 10.0.21 开始，此功能默认开启。）

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>阻止转移单已装运牌照用于目标仓库以外的其他仓库

如果 ASN 中包含已存在的牌照 ID，并且具有的实际现有数据所在仓货位置不是牌照的登记仓货位置，则不能使用牌照接收流程。

对于中转仓库不跟踪牌照（因此也不跟踪每个牌照的实际现有库存）的转移单方案，可使用 *阻止转移单已装运牌照用于目标仓库以外的其他仓库* 功能阻止中转中的牌照的实际现有更新。

要使此功能在您的系统上可用，您必须在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开 *阻止转移单已装运牌照用于目标仓库以外的其他仓库*。

若要在此功能可用时管理功能，请执行以下步骤。

1. 转到 **仓库管理 \> 设置 \> 仓库管理参数**。
1. 在 **常规** 选项卡的 **牌照** 快速选项卡上，将 **中转仓库牌照政策** 字段设置为以下值之一：

    - **允许重复使用非跟踪牌照** – 系统的工作方式与 *阻止转移单已装运牌照用于目标仓库以外的其他仓库* 功能不可用时的工作方式相同。 此值是首先激活此功能时的默认设置。
    - **防止重复使用非跟踪牌照** – 收到转移单之前，目标仓库中仅允许与装运的牌照有关的现有更新。

## <a name="more-information"></a>更多信息

有关移动设备菜单项的详细信息，请参阅[为仓库工作设置移动设备](configure-mobile-devices-warehouse.md)。

有关 *完工入库* 生产方案的详细信息，请参阅[仓库工作策略概述](warehouse-work-policies.md)。

有关入站负荷管理的详细信息，请参阅[仓库对采购订单入站负荷的处理](inbound-load-handling.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]