---
title: 同步内部公司费用
description: 本主题介绍了内部公司费用的同步
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 2c7f60786743cf750b2bb17ccc0dadf71d859766
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678566"
---
# <a name="synchronize-intercompany-charges"></a>同步内部公司费用

[!include [banner](../../includes/banner.md)]

费用只在内部公司销售订单和内部公司采购订单之间同步，并且同步将始终发生。

如果在内部公司采购订单或内部公司销售订单上选择了 **允许编辑价格** 字段，则可以手动将费用添加到内部公司销售订单或内部公司采购订单。 否则不能。

如果在内部公司销售订单上未选择 **允许编辑价格** 字段，则不能将费用手动添加到内部公司销售订单。

如果在内部公司采购订单上未选择 **允许编辑价格** 字段，则不能将费用添加到内部公司采购订单。

如果在内部公司采购订单和内部公司销售订单上都启动了 **允许编辑价格** 字段，则您可以手动添加费用到这两个订单。 但是，这可能导致许多费用被错误添加。

若要避免这些类型的冲突，最佳实践是允许费用添加到内部公司销售订单或内部公司采购订单，但不允许同时添加到这两者上。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
