---
title: 下达装载后立即生成领料工作
description: 如果必须在发放负荷时立即生成工作，您必须相应地配置波次模板。 此页面引导您完成这些步骤。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475706"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>下达出站装载后不立即生成领料工作

## <a name="symptoms"></a>故障特征

可使用销售订单或转移单创建出站负荷，然后将此负载下达到仓库。 但是请注意，不必生成任何领料工作。

## <a name="resolution"></a>解决方法

如果必须在发放负荷时立即生成工作，您必须相应地配置波次模板。 在波次模板上，将以下选项设置为 *是*：

- 自动波次创建
- 在发放到仓库时处理波次
- 自动发出波次
