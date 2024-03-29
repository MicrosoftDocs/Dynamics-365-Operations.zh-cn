---
title: 半年折旧惯例方法
description: 本文介绍固定资产用于计算使用半年惯例的折旧的方法，即计算资产第一年到最后一年服务期间的六个月折旧。
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: fac20f7a31eca7922ed079f9554437f28448620d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879586"
---
# <a name="half-year-depreciation-convention-methodology"></a>半年折旧惯例方法

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文介绍固定资产中用于计算使用半年惯例的折旧的方法。 半年惯例计算资产第一年到最后一年服务期间的六个月折旧。 有关折旧惯例的详细信息，请参阅[折旧法和惯例](Fixed-asset-depreciation-conventions.md)。 

当您使用六个月折旧惯例时，系统使用购置年份或资产开始服务的年份，然后计算从该年开始的五年折旧，然后增加六个月。 为了阐释此过程，假设一个资产的购置价格为 50,000，服务时间为 2020 年 4 月。 再假设资产的服务寿命为五年。

第一个服务年份在 2020 年 12 月结束，这意味着资产的前五年服务寿命结束时间为 2024 年 12 月。 半年折旧惯例将向资产的寿命添加六个月，这意味着其服务将在 2025 年 6 月结束。 

> 年折旧 50,000/5 = 10,000，月折旧 10,000/12 = 833.33 <br>
> 第一年折旧 10,000/2 = 5,000，后续月折旧 5,000/9 = 555.56

   [![半年折旧惯例的折旧计划。](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

半年惯例增加的延长后折旧期的折旧分配更精确。 六个月惯例提供的折旧费用更平均，这对损益表中的报告非常有用。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
