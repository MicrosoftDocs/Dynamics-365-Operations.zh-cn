---
title: 无法在销售报价行中设置服务物料数量
description: 处理销售报价单时，不能为充当服务物料的产品设置销售数量，因为没有实际物料要盘点。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475729"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>无法更改销售报价单行中的服务物料的销售数量

## <a name="symptoms"></a>故障特征

如果您尝试在销售报价单行上为 *服务* 类型的物料设置销售数量（**SalesQty** 字段），您将收到以下消息：

> 不允许更新“数量”字段”。

## <a name="cause"></a>原因

这是有意行为。 您不能为属于服务物料的产品设置销售数量。 例如，如果您提供安装物料的服务，那么记录数量是没有意义的，因为没有实际物料要盘点。 只有服务。
