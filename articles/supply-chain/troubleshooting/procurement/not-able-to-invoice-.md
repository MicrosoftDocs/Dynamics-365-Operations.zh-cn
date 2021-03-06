---
title: 您无法为面向客户的销售订单开票
description: 启用“自动过帐发票”选项后，您无法再为原始销售订单和原始直接交货采购订单开票。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026299"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>您无法为面向客户的销售订单开票

知识库编号：4611793

## <a name="symptoms"></a>故障特征

在供应商的 **内部公司** 页上启用 **自动过帐发票** 选项后，您无法再为原始销售订单和原始直接交货采购订单开票。

## <a name="resolution"></a>解决方法

内部公司和直接交货订单发票的同步行为由[设置用于过帐内部公司订单的参数](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order)中所述的参数控制和强制执行。

设置这些参数后，必须首先为内部公司销售订单开票。 然后原始销售订单和采购订单将同步。
