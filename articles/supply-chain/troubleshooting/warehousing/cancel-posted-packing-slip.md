---
title: 装箱单从销售订单过帐后无法取消
description: 为 WMS 启用了领料和装运流程后，无法取消从销售订单过帐的装箱单。 此页面提供了一个解决方法。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475741"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>装箱单从销售订单过帐后无法取消

## <a name="symptoms"></a>故障特征

为高级仓库管理 (WMS) 启用了领料和装运流程后，无法取消从销售订单过帐的装箱单。

## <a name="resolution"></a>解决方法

要更正已启用 WMS 的物料的已过帐装箱单，必须从负荷而不是从订单进行过帐。 Microsoft 已评估此问题，确定了这是一项功能限制。  

通常，通过仓库管理流程领料和装运的销售订单可以从负荷或装运以及销售订单文档本身更新装箱单。 但是，如果从销售订单文档对销售订单进行装箱单更新，装箱单冲销仍然无法从负荷或销售订单进行。 因此，我们建议您从负荷使用装箱单过帐。 在这种情况下，将启用必须从负荷进行的冲销。
