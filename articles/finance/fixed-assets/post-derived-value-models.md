---
title: 使用衍生帐簿过帐
description: 本文介绍如何使用衍生帐簿。
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0270ad1e66193832fb1139fca4439b36b5ffb84
ms.sourcegitcommit: dca54dd3afc7c94795d89c63050b105df2c48e3f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2022
ms.locfileid: "9682849"
---
# <a name="post-with-derived-books"></a>使用衍生帐簿过帐

[!include [banner](../includes/banner.md)]

本文介绍如何使用衍生帐簿。

当您为一个包含衍生帐簿的帐簿过帐交易记录时，衍生帐簿交易记录将自动从日志、采购订单或普通发票过帐。 但是，如果您在固定资产日记帐中准备主要帐簿交易记录，则可以在过帐衍生交易记录的金额前查看和修改这些金额。
-   某些帐户（如增值税和客户或供应商帐户）只通过主要帐簿过帐的方式更新一次。 衍生帐簿交易记录将被过帐到在“固定资产过帐模板”页中为衍生帐簿定义的帐户。
-   购置通常用作衍生帐簿的交易记录类型。 如果固定资产从购置之日起就应用帐簿和衍生帐簿，就使用此类型。
-   也可以为交易记录类型应用其他值。 例如，如果主要帐簿和衍生帐簿在销售或处置方面具有相同的间隔，则设置衍生帐簿时可以使用所有固定资产交易记录类型。

> [!WARNING]
> 衍生帐簿中已过帐的折旧金额应与主要帐簿中已过帐的金额相等。 如果帐簿之间的折旧方法不同，则使用衍生流程将不应生成折旧交易记录。 

## <a name="example"></a>示例 
以下信息描述如何设置具有衍生帐簿功能的购置交易记录。

1.  在“帐簿”页面上创建帐簿。
    -   用于核算的帐簿：VM 1，当前过帐层
    -   用于纳税目的的帐簿：VM 2，税过帐层。

2.  在 VM 1 上，单击“派生帐簿”选项卡，并在“帐簿”字段选择 VM 2，在“交易记录类型”字段选择“购置”。

然后，可将帐簿附加到特定的固定资产。 

当固定资产的购置使用帐簿 VM 1 过帐时，该购置不仅在 VM 1 中过帐，而且在衍生帐簿 VM 2 中过帐。 两种固定资产帐簿的状态将更新为“未完成”。

> [!NOTE]                                                                                                         
> 如果不使用衍生帐簿，则必须在帐簿 VM 1 和帐簿 VM 2 中都对固定资产购置过帐。

有关详细信息，请参阅[衍生帐簿](derived-books.md)。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
