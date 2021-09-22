---
title: 未在发票帐户中填充默认税组和现金折扣
description: 未在发票帐户中填充默认税组和默认现金折扣
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475681"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>未在发票帐户中填充默认税组和现金折扣

## <a name="symptoms"></a>故障特征

如果您使用与客户帐户不同的发票帐户，在创建采购订单时不会在发票帐户中填充默认税组和默认现金折扣。

## <a name="resolution"></a>解决方法

此为有意行为。 税组、现金折扣和其他价格信息的默认值基于客户帐户，而不是发票帐户。
