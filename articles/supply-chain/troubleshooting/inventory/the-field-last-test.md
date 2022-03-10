---
title: 创建多个质检订单时，“上次测试日期”字段不更新
description: 创建多个质检订单时，“上次测试日期”字段不更新。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742020"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>创建多个质检订单时，“上次测试日期”字段不更新

知识库编号：4612803

## <a name="symptoms"></a>故障特征

创建多个质检订单时，**上次测试日期** 字段不更新。

## <a name="resolution"></a>解决方法

此系统行为是有意设计的。 上次测试日期与质检订单不相关。 它存储首次购买或制造成品的日期。 此日期用于计算保质期建议日期。
