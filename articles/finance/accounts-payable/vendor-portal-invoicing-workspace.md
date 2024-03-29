---
title: 供应商协作开票工作区
description: 本文介绍如何通过供应商协作开票工作区查看供应商发票和提交发票。
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9ef4204e0be437b50af047704e07600653c877c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896541"
---
# <a name="vendor-collaboration-invoicing-workspace"></a>供应商协作开票工作区

[!include [banner](../includes/banner.md)]

本文介绍如何通过 **供应商协作开票** 工作区查看供应商发票和提交发票。

**供应商协作开票** 工作区可用于查看供应商发票信息和使用工作流功能提交发票至此系统。


## <a name="vendor-collaboration-invoicing-workspace"></a>供应商协作开票工作区

### <a name="summary-tiles"></a>汇总磁贴

**汇总** 磁贴提供了所选供应商的发票概览。 您可以按其状态查看发票。
-   草稿发票尚未提交到工作流。
-   已提交但未审核的发票为供应商已经提交，但未在应用程序中过帐的发票。
-   已审核但未付款的发票为已经过帐但尚未付清的发票。
-   已付款发票为已经在应用程序中全额付清的发票。

单击磁贴将打开 **发票列表** 页面的筛选视图。

### <a name="tabular-lists"></a>表格式列表

在 **表格式列表** 部分，发票的状态按照与汇总磁贴类似的方式分解：**草稿** 和 **已提交**、**未审核** 列表。 在 **草稿** 状态，发票可以提交到工作流或删除。 最后一个表格式列表是用来查找发票的选项。 您可以在搜索时进行筛选，以便更快地进行搜索。

### <a name="all-vendor-invoices-list-page"></a>所有供应商发票列表页

您可以在 **供应商协作发票** 列表页上查看所有已过帐和未过帐的供应商发票。 您可以使用此列表页查看发票的付款状态。 付款状态包括 **未过帐**、**未付款**、**部分支付** 和 **完全支付**。
从采购订单创建新发票

您可以通过选择 **供应商协作开票** 工作区上的 **新建** 操作创建新的供应商发票。 采购订单编号以及发票编号必须由供应商提供。 默认情况下，新发票上将显示供应商采购订单的所有行。 将供应商发票提交到工作流之前，可以编辑数量和成本信息。 提交发票前，您可以在发票上附加文件、附注、图片和 URL。

有关详细信息，请参阅[供应商与外部供应商的协作](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
