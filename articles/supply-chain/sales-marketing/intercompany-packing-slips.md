---
title: 内部公司装箱单
description: 本文介绍如何生成和打印内部公司交易记录的装箱单
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
ms.openlocfilehash: 3516058bbf925df4b0a0c75286a3d97457cc1e69
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900845"
---
# <a name="intercompany-packing-slips"></a>内部公司装箱单

## <a name="generate-intercompany-packing-slips"></a>生成内部公司装箱单

[!include [banner](../../includes/banner.md)]

如果您使用直接交运，则当您针对内部公司销售订单生成装箱单时，会针对内部公司采购订单和原始销售订单始终自动生成装箱单。 内部公司采购订单发票基于以前已生成的内部公司采购订单装箱单。

如果您在内部公司销售订单上对装箱单进行任何更新，则这些更新将反映在内部公司采购订单和原始销售订单上。

如果您没有使用直接交运，则必须手动在内部公司销售订单、内部公司采购订单和原始销售订单上生成装箱单。

## <a name="print-intercompany-packing-slips"></a>打印内部公司装箱单

[!include [banner](../../includes/banner.md)]

如果您使用直接交运，则当您在内部公司销售订单上过帐装箱单时，可为内部公司采购订单和原始销售订单自动打印一份装箱单。

若要自动打印装箱单，请在采购订单的 **内部公司** 页面上，选择两个 **自动打印装箱单** 字段。

如果您在内部公司销售订单上对装箱单进行任何更新，则这些更新将自动反映在内部公司采购订单和原始销售订单上。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
