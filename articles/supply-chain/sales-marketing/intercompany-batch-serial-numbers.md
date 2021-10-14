---
title: 内部公司批处理和序列号
description: 本主题介绍了登记内部公司订单的批号和序列号时将会发生什么情况
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4da936263bb57c24eeb7021ac61b3945bb2777fb
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548136"
---
# <a name="intercompany-batch-and-serial-numbers"></a>内部公司批处理和序列号

[!include [banner](../../includes/banner.md)]

使用序列号或批号跟踪其物料的公司还必须跟踪已领取物料的序列号和批号。 内部公司功能自动完成从一个公司到另一个公司的序列号和批号的收/发。 当您在内部公司销售订单上登记物料的批号和序列号时，可以对程序进行设置，以将这些代号自动传送到内部公司采购订单和原始销售订单。 您必须在 **内部公司** 页面上为销售订单设置相关参数：

- 如果您选择在 **采购订单策略** 页上的 **批号** 字段，则在您过帐内部公司销售订单的装箱单时，批号与内部公司采购订单行上的库存交易记录保持同步。
- 如果您选择 **序列号** 字段，则在您过帐内部公司销售订单的装箱单时，序列号与内部公司采购订单行上的库存交易记录保持同步。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
