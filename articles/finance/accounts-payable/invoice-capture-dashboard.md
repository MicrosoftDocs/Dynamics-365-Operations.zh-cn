---
title: Invoice capture 解决方案仪表板
description: 本文介绍 Invoice capture 解决方案仪表板。
author: sunfzam
ms.date: 10/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690109"
---
# <a name="invoice-capture-solution-dashboard"></a>Invoice capture 解决方案仪表板

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

在 Invoice capture 中，仪表板包括提供已导入发票概览的图表。 这些图表可以帮助应付帐款 (AP) 经理分析发票生成流程的性能。 AP 经理可以查看发票生成流程的状态，通过应用不同的筛选器，还可以查看详细信息。

## <a name="available-charts"></a>可用图表

仪表板上有以下图表：

- **按状态列出的所有捕获的发票** – 此图表显示已捕获发票的以下状态。 通过选择状态，用户可以在详细列表中筛选捕获的发票。

    - 已捕获
    - 完成
    - 正在审核
    - 已废弃

- **捕获的发票总量** – 此图表显示按期间列出的捕获的发票数量。 用户可以使用下拉列表更改期间。
- **捕获的主要供应商的发票** – 此图表显示每个供应商的发票总数。 发票数量最多的供应商将出现在顶部。
- **每个发票的完成天数（除例外情况）** – 此图表显示捕获一个发票所需的平均天数。 此信息可以帮助 AP 经理分析在需要人工干预时处理发票的时间。 如果有上升趋势，用户可以查看流程详细信息并调整设置来帮助减少所需的天数。
- **按待处理时间列出的未完成发票** – 此图表显示未在企业资源计划 (ERP) 系统中生成已捕获发票的天数。 待处理天数越大，发票生成过程越长。 AP 经理可以向下钻取到有详细信息的已捕获发票并在 ERP 系统中生成发票。
