---
title: 由于交易记录不足，未更新库存数量
description: 由于物料 %2 没有足够多具有指定维度的库存交易记录，因此无法更新库存数量 -1%。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475639"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>由于交易记录不足，系统无法更新库存数量

## <a name="symptoms"></a>故障特征

如果系统由于没有足够的具有指定维度的库存交易而无法更新库存数量，则可能发生此问题。 您将收到以下错误消息：

> 库存数量 -%1 由于批次 ID %12 上的物料 %2（维度为尺寸=%3、颜色=%4、附加物=%5、站点%6、仓库=%7、位置=%8、库存状态=可用、牌照=%9、引用 ID %11 的批处理号=%10）的库存交易不足无法更新。

## <a name="resolution"></a>解决方法

请确保没有库存交易在实际预留数量。 例如，这些交易可能会打开质量订单、库存锁定记录或输出订单。
