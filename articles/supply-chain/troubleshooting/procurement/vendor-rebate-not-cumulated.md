---
title: 不会根据发票累计供应商返点
description: 不会根据发票累计供应商返点
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475731"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>不会根据发票累计供应商返点

## <a name="symptoms"></a>故障特征

如果过帐的发票具有不同的截止日期，这些发票不会反映在从它们生成的供应商返点中。

## <a name="resolution"></a>解决方法

在计算供应商返点时不考虑截止日期。 考虑自定义系统，以使截止日期和与发票的关系相对于实际的供应商返点更加明显。
