---
title: 零售价报表
description: 此主题提供可以用于查看分类产品的近期价格变更的价格报表功能的概览。
author: shajain
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 7fa2710d64d632c6e4ef376528aff8316b02a380ce7e2a976d53a3dd39375fa7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767258"
---
# <a name="retail-price-reports"></a>零售价报表

[!include [banner](includes/banner.md)]


为向客户提供有竞争力的价格，零售商通常会更改产品的价格。 店长希望能够轻松访问最近或未来的价格变更，以便他们可以计划所需资源来更新显示在商店货位上的价格标签。 使用 Retail 的版本 10.0，店长可以通过导航到 **所有商店 \> 商店 \> 价格报表** 并查看与商店关联的产品的更新价格来打开 **价格** 报表。 

若要启用价格报表，必须打开 **启用商店的价格报表** 参数。 此参数位于 **商业参数 \> 折扣 \> 杂项** 选项卡中。打开 **价格报表** 页将显示具有不同配置的对话框。 可用配置在下面列出。

| 配置 | 说明 |
|---|---|
| 开始日期/结束日期| 应该生成价格报表的日期范围。 持续时间当前限定为 7 天。 |
| 通道| 应该生成价格报表的商店。 |
| 显示具有可用库存的产品| 将此项设置为 **是** 将只显示当前在商店中有可用的实际库存的那些产品的价格。 |
| 显示变型的价格 | 将此项设置为 **是** 将显示变型以及基础产品的价格。 这应该仅在您有变型特定价格时再 **打开**，因为行数将变得非常大。 在将来的版本中，我们将启用基于维度的价格，以便店长可以选择应显示其价格的维度。 |
| 显示具有价格更改的产品 | 将此项设置为 **是** 将仅显示价格已更改的那些日期的价格。 **开始日期** 的 *前一天* 的价格将始终显示，以便店长可以轻松识别在整个所选持续时间内未更改价格的产品，并可以查看当前价格。 |

生成报表后，Excel 文件可以根据任何其他筛选需要下载。 价格报表还可以用于检查过去日期的产品的历史价格。


[!INCLUDE[footer-include](../includes/footer-banner.md)]