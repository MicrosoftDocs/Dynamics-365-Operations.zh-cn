---
title: 其中一行已在负荷中
description: 此页面说明您为什么收到以下错误：“其中一行已在负荷中。 无法下达到仓库”，以及如何解决问题。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475738"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>其中一行已在负荷中

## <a name="symptoms"></a>故障特征

处理负荷构建和装运时，您可能会收到以下错误消息：

> 其中一行已在负荷中。 无法下达到仓库。

如果您手动创建负荷，或者设置流程以在进行销售订单行输入之前负荷已经创建，系统将假定后续下达会手动完成，并将使用负荷中的路线和评级。

在另一个可能的场景中，您尝试对仓库执行自动下达，但是波次流程无法创建工作。 因此，仍会创建未结装运或负荷。 然后，此未结装运或负荷将阻止后续自动下达订单的尝试，直到您删除未结装运或负荷，或手动重新处理波次。

## <a name="resolution"></a>解决方法

您可以从销售订单页下达，也可以从下达销售订单页自动下达，只要在下达到仓库之前没有负荷。 负荷将在波次被处理后自动创建。
