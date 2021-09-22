---
title: 采购协议最大限制对采购申请无效
description: 采购协议最大限制对采购申请无效
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
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475666"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>采购协议最大限制对采购申请无效

## <a name="symptoms"></a>故障特征

当采购申请链接到采购协议时，采购协议的最大限制对采购申请无效。 默认价格信息已正确输入，但可以在采购申请中订购超过采购协议最大限制的量。

## <a name="resolution"></a>解决方法

此行为是预期的。 由于采购申请不一定总是得到批准，因此不应在采购协议上保留数量或金额。 因此，您不会达到采购协议的最大限制。
