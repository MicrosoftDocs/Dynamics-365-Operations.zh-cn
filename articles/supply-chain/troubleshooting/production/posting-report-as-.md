---
title: 过帐完工入库日记帐时出错
description: 当您过帐完工入库日记帐时，您收到一条错误消息，指出无法减少订购的已订购数量。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 50a11aba46519a3a81c313aa1f685d45dcf35f64b50bc921d93968efab13b7b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750922"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>过帐完工入库日记帐时出错

知识库编号：4612891

## <a name="symptoms"></a>故障特征

当您过帐 **完工入库** 日记帐时，发生错误，您收到以下错误信息：

> 不能减少订购数量，因为状态为“已订购”的未结库存交易记录不足。 物料已购买、已接收或已登记。

仅当在 **完工入库** 日记帐的第一行上设置了 **残次数量** 字段并且在最后一行设置了 **完好数量** 字段时，才会发生此错误。 如果在最后一行设置了 **残次数量** 字段，则不会发生错误。

## <a name="resolution"></a>解决方法

要防止发生此错误，打开 **生产控制参数** 页，然后在 **常规** 选项卡上，将 **增加剩余数量(含残次数量)** 选项设置为 *是*。
