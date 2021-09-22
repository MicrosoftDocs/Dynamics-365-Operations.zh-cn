---
title: 0.00 可用导致无法执行库存预留
description: 您收到一个错误，说明因为库存中只有 0.00 可用，所以无法执行预留。 此问题可能是由于未结工作引起的。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475719"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>库存中 0.00 可用导致系统无法执行库存预留

## <a name="symptoms"></a>故障特征

如果系统由于没有足够的具有指定维度的库存交易而无法更新库存数量，则可能发生此问题。 您将收到以下错误消息：

> 实际现有量站点=%1、仓库=%2、库存状态=可用、批处理号=%3、所有者=%4：%5 无法预留，因为库存中只有 0.00。

## <a name="resolution"></a>解决方法

此问题可能是由于未结工作引起的。 请完成工作或在不创建工作时接收。 请确保没有库存交易在实际预留数量。 例如，这些交易可能会打开质量订单、库存锁定记录或输出订单。
