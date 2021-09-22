---
title: 即使未生成凭证也使用产品收货凭证号
description: 即使产品收货期间未生成财务凭证，也会使用产品收货凭证号
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475682"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>即使未生成凭证也使用产品收货凭证号

## <a name="symptoms"></a>故障特征

即使产品收货期间未生成财务凭证，也会使用产品收货凭证号。

## <a name="resolution"></a>解决方法

如果物料模型组的 **产品收货上的应计负债** 选项设置为 *否*，将不会过帐到总帐。 但是，将在子分类帐中为会计目的记录物理事件，该事件需要凭证号。 此凭证号是库存交易记录中引用的凭证号。

我们建议您将 **产品收货上的应计负债** 选项设置为 *是*，如以下博客文章所述：[在产品收货时过帐杂项费用](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)。
