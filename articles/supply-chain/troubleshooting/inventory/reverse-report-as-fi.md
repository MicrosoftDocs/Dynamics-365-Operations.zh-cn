---
title: 报告为完工入库撤销会创建意外的未结交易
description: 带有标记的报告为完工入库撤销会创建一个未结交易，其中的已冲销数量与已冲销交易具有相同的库存维度。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026315"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>报告为完工入库撤销会创建意外的未结交易

知识库编号：4612469

## <a name="symptoms"></a>故障特征

如果您撤销带有标记的报告为完工入库，系统会创建一个未结交易，其中的已冲销数量与已冲销的交易具有相同的库存维度。

## <a name="resolution"></a>解决方法

当您撤销报告为完工入库操作时，库存维度会从生产日记帐初始化。 因此，它会获得批处理号。 由于有标记，销售订单交易将继承此批处理号。

维度可以在报告为完工入库过帐时重置。
