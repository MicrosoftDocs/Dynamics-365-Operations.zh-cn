---
title: 云和边缘缩放单元的仓库订单
description: 本主题提供有关仓库订单功能的信息，它是仓库缩放单元工作负荷的一部分。
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4a77b157e9dd5ee1f551cbb59abbc89aaa28d325cc74a77e6624f25902c5b19e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731881"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>云和边缘缩放单元的仓库订单

[!include [banner](../includes/banner.md)]

> [!WARNING]
> 当使用缩放单元工作负荷时，并非所有业务功能都在公开预览版中完全受支持。 如果您使用的是缩放单元，请确保仅使用本主题明确描述为受支持的那些流程。

## <a name="what-are-warehouse-orders"></a>什么是仓库订单？

*仓库订单* 是为支持中心和缩放单元仓库部署而创建的一种订单。 当您在缩放单元上运行仓库工作负荷时，您可以使用它们来接收库存。 它们当前只能与采购订单一起使用。

仓库订单用作仓库管理处理的一部分，例如在处理入库采购订单期间使用仓库管理移动应用登记实际现有库存时。 仓库订单的创建是 *发放到仓库* 流程的一部分，可用于指定缩放单位仓库的采购订单，以及为使用仓库管理流程启用的项目。

> [!IMPORTANT]
> 仓库订单仅在将[仓库管理工作负荷用于云和边缘缩放单元](cloud-edge-workload-warehousing.md)的部署中可用。

## <a name="create-a-warehouse-order"></a>创建仓库订单

要创建仓库订单，请按照下面的步骤操作。

1. 登录到在中心运行的 Microsoft Dynamics 365 Supply Chain Management 的实例。 （在中心登录后，您必须启动 *发放到仓库* 流程。）
1. 转到 **采购 \> 采购订单 \> 所有采购订单**。
1. 在“操作窗格”上的 **仓库** 选项卡上，在 **操作** 组中，选择 **发放到仓库**。
1. 要查看相关的仓库订单行，打开相关的采购订单，在 **采购订单行** 部分选择行，然后在工具栏上选择 **仓库 \> 仓库订单行**。 要查看所有行，转到 **仓库管理 \> 查询和报表 \> 仓库订单行**。

您也可以通过转到 **仓库管理 > 发放到仓库 > 自动下达采购订单**，从批处理作业触发 *发放到仓库* 流程。 设置批处理作业时，您可以根据查询选择特定的采购订单行。 一个典型的方案是设置一个重复批处理作业，来发放所有预期在第二天到达的已确认采购订单行。

## <a name="cancel-a-warehouse-order"></a>取消仓库订单

作为 *发放到仓库* 流程的一部分，采购订单库存交易将链接到仓库订单，并被中心锁定以免更新。 如果您错误地发放到仓库，或者有其他原因要撤消仓库订单行的创建，可以请求取消仓库订单行。

要取消仓库订单行，请按照下面的步骤操作。

1. 登录到在中心运行的 Supply Chain Management 实例。
1. 转到 **仓库管理 \> 查询和报表 \> 仓库订单行**。
1. 选择相关行。
1. 在操作窗格上，选择 **取消仓库订单行**。

> [!NOTE]
> 对于任何已经在等待取消或正在缩放单元上运行工作负荷的仓库中处理的行，取消行请求都将被拒绝。

## <a name="monitor-a-warehouse-order"></a>监视仓库订单

在 **仓库订单行** 视图中，您可以通过查看 **要接收的剩余数量** 列中的值来监视入站接收的进度。 若要查看与使用仓库管理移动应用完成的工作相关的详细信息，请执行以下步骤之一。

- 转到 **仓库管理 \> 查询和报表 \> 仓库订单行**，使用筛选器查找您要查找的行。
- 转到 **采购 \> 采购订单 \> 所有采购订单**，打开相关的采购订单。 在 **采购订单行** 部分，选择一个或多个行，然后在工具栏上选择 **仓库 \> 仓库收货条目**。

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
