---
title: 创建销售订单行时选择了同一份贸易协议
description: 如果为给定日期定义了多份贸易协议，创建销售订单行时，将始终选择价格最低的那份。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475693"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>如果重合日期有两份贸易协议，始终选择同一份

## <a name="symptoms"></a>故障特征

如果为同一期间或重叠期间定义了两个贸易协议，每次创建包含这些物料的销售订单行时，似乎会选择同一个贸易协议。

## <a name="resolution"></a>解决方法

如果给定日期有多个贸易协议，将始终选择价格最低的贸易协议。 有关详细信息，请下载以下白皮书：[Microsoft Dynamics AX 2012 中的贸易协议](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90)。
