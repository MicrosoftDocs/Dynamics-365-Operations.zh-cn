---
title: 可以将交易记录过帐到暂停的会计科目中
description: 如果取消了产品收货，系统将允许将交易记录过帐到已暂停的会计科目中，即使主科目已暂停
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
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475736"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>可以将交易记录过帐到暂停的会计科目中

## <a name="symptoms"></a>故障特征

如果取消了产品收货，系统将允许将交易记录过帐到已暂停的会计科目中，即使主科目已暂停。

## <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 在 **应付帐款参数** 页上的 **常规** 选项卡上，确保将 **在分类帐中对产品收货过帐** 选项设置为 *是*。
1. 创建一个采购订单，并添加产品数量为 *1,000* 的订单行。
1. 确认采购订单。
1. 过帐产品收货，并检查凭证。
1. 暂停相关的主科目 *200140* 和 *140200*。
1. 取消已过帐的产品收货。
1. 请注意，可以将交易记录过帐到暂停的会计科目中。

## <a name="resolution"></a>解决方法

取消产品收货后，可以将交易记录过帐到已暂停的会计科目中，因为此行为可进行正确过帐。
