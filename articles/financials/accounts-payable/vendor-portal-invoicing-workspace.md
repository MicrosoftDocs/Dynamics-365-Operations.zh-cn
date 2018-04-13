---
title: "供应商协作开票工作区"
description: "本主题介绍如何通过供应商协作开票工作区查看供应商发票和提交发票。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 2368fae3913f67d9d2ce0bbe6b2e0bee7968bb15
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="vendor-collaboration-invoicing-workspace"></a>供应商协作开票工作区

[!INCLUDE [banner](../includes/banner.md)]

本主题介绍如何通过供应商协作开票工作区查看供应商发票和提交发票。

**供应商协作开票**工作区可用于查看供应商发票信息和使用工作流功能提交发票至 Microsoft Dynamics 365 for Finance and Operations。


<a name="vendor-collaboration-invoicing-workspace"></a>供应商协作开票工作区
----------------------------------------

### <a name="summary-tiles"></a>汇总磁贴

**汇总**磁贴提供了所选供应商的发票概览。 您可以按其状态查看发票。
-   草稿发票尚未提交到工作流。
-   已提交但未审核的发票为供应商已经提交，但未在 Finance and Operations 中过帐的发票。
-   已审核但未付款的发票为已经在 Finance and Operations 中过帐但尚未付清的发票。
-   已付款发票为已经在 Finance and Operations 中全额付清的发票。

单击磁贴将打开“**发票列表**”页面的筛选视图。

### <a name="tabular-lists"></a>表格式列表

在“**表格式列表**”部分，发票的状态按照与汇总磁贴类似的方式分解：草稿和已提交，未审核的列表。 在“草稿”状态，发票可以提交到工作流或删除。 最后一个表格式列表是用来查找发票的选项。 您可以在搜索时进行筛选，以便更快地进行搜索。

<a name="all-vendor-invoices-list-page"></a>所有供应商发票列表页
-----------------------------

您可以在**供应商协作发票**列表页上查看所有已过帐和未过帐的供应商发票。 您可以使用此列表页查看发票的付款状态。 付款状态包括未过帐，未付款，部分支付和完全支付。
从采购订单创建新发票
--------------------------------------------

您可以通过选择“**供应商协作开票**”工作区上的“**新建**”操作创建新的供应商发票。 采购订单编号以及发票编号必须由供应商提供。 默认情况下，新发票上将显示供应商采购订单的所有行。 将供应商发票提交到工作流之前，可以编辑数量和成本信息。 提交发票前，您可以在发票上附加文件、附注、图片和 URL。



有关详细信息，请参阅[供应商与外部供应商的协作](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)




