---
title: "派生的具有帐簿过帐"
description: "本文介绍如何使用衍生帐簿。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: ca077727910059878fb16a3f78c5b9133c6c741f
ms.lasthandoff: 03/31/2017


---

# <a name="post-with-derived-books"></a>派生的具有帐簿过帐

本文介绍如何使用衍生帐簿。

当您为一个包含衍生帐簿的帐簿过帐交易记录时，衍生帐簿交易记录将自动从日志、采购订单或普通发票过帐。 但是，如果您在固定资产日记帐中准备主要帐簿交易记录，则可以在过帐衍生交易记录的金额前查看和修改这些金额。
-   某些帐户（如增值税和客户或供应商帐户）只通过主要帐簿过帐的方式更新一次。 衍生帐簿交易记录将被过帐到在“固定资产过帐模板”页中为衍生帐簿定义的帐户。
-   购置通常用作衍生帐簿的交易记录类型。 如果固定资产从购置之日起就应用帐簿和衍生帐簿，就使用此类型。
-   也可以为交易记录类型应用其他值。 例如，如果主要帐簿和衍生帐簿在销售或处置方面具有相同的间隔，则设置衍生帐簿时可以使用所有固定资产交易记录类型。

> [!WARNING]
> 衍生帐簿中已过帐的折旧金额应与主要帐簿中已过帐的金额相等。 如果帐簿之间的折旧方法不同，则使用衍生流程将不应生成折旧交易记录。 |

## <a name="example"></a>示例 
以下信息描述如何设置具有衍生帐簿功能的购置交易记录。

1.  在“帐簿”页面上创建帐簿。
    -   用于核算的帐簿：VM 1，当前过帐层
    -   用于纳税目的的帐簿：VM 2，税过帐层。

2.  在 VM 1 上，单击“衍生帐簿”选项卡。 在“帐簿”字段中选择 VM 2，在“交易记录类型”字段中选择“购置”。

然后，可将帐簿附加到特定的固定资产。 

在购置使用帐簿 VM 1 的固定资产过帐时，该购置不仅在 VM 1，派生的，而且在帐簿 VM 2。 两固定资产帐簿状态更新未结。

> [!NOTE]                                                                                                         
> 如果不使用衍生帐簿，则必须在帐簿 VM 1 和帐簿 VM 2 中都对固定资产购置过帐。

有关详细信息，请参阅 books.md 的 [] ("派生") 派生的帐簿


