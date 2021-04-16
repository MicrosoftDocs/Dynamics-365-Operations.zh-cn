---
title: 使用供应商协作监控托运库存
description: 此过程显示如何通过供应商协作查看有关您在客户托运中发放的物料的存货级别的信息。
author: sherry-zheng
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e397c12b9f605d1c864ce053477090ed8c1700
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839263"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>使用供应商协作监控托运库存

[!include [banner](../../includes/banner.md)]

此过程显示如何通过供应商协作查看有关您在客户托运中发放的物料的存货级别的信息。 也可以在客户接管库存的所有权时监控存货的消耗情况。 您可以在 USMF 演示数据公司中使用此过程。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="view-consumed-inventory"></a>查看消耗的库存
1. 转到“供应商协作”>“托运库存”>“从托运库存接收的产品”。
    * 此列表显示托运库存所有权从供应商更改为客户时生成的物料收货行。 可能必须向右滚动才能看到数量和其他信息。 可以使用此列表中的信息为客户生成发票。 您还可以将数据导出至 Microsoft Excel。   
2. 单击“查看采购订单”。
3. 展开“行明细”部分。
    * 此行标记为“托运”，并且标题部分显示状态为“入库”的采购订单。  
4. 关闭该页面。

## <a name="view-on-hand-inventory"></a>查看现有库存量
1. 转到“供应商协作”>“托运库存”>“现有托运库存”。
    * “现有托运库存”页面显示您在客户的仓库中拥有的存货。 可以通过单击“显示维度”选项卡显示更多维度，如站点和仓库。   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]