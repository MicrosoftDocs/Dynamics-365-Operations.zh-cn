---
title: 中国的固定资产折旧法
description: 本文描述为中国法人设置的折旧法。
author: AdamTrukawka
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: China (PRC)
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 265244
ms.search.form: AssetParameters
ms.openlocfilehash: d6d6445c60c88dbabbb48ce61324bf6f3af5b470
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284008"
---
# <a name="fixed-assets-depreciation-methods-for-china"></a>中国的固定资产折旧法

[!include [banner](../includes/banner.md)]

本文描述为中国法人设置的折旧法。

年数总和折旧法 (SYD) 是一种基于以下假设的加速折旧技术：资产越新，生产率越高，如果变旧，生产率随之下降。 SYD 法的折旧计算公式为：

> *SYD 折旧 = 折旧基数 × (剩余使用寿命/年数总和法)*

若要创建折旧模板：

1. 在 **固定资产参数** 页上，选择 **SYDM 和 DRBM** 折旧法。
2. 创建一个新折旧模板。 使用 **年数总和法** 或 **双倍余额递减法**。
3. 为该折旧法创建一个帐簿，请使用 **年数总和法** 或 **双倍余额递减法**。

有关详细信息，请参阅[设置固定资产折旧分摊](./tasks/fixed-asset-depreciation-allocation.md)。




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
