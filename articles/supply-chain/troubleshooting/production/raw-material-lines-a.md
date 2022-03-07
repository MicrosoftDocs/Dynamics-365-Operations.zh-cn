---
title: 用户可以取消已报告为已完工入库的产品的材料行的领料
description: 系统允许用户取消已报告为已完工入库的产品的原材料行的领料。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5a4e2ffd24904f822f4993525cc196a050db1ba4
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026291"
---
# <a name="users-can-unpick-material-lines-for-products-that-have-been-reported-as-finished"></a>用户可以取消已报告为已完工入库的产品的材料行的领料

知识库编号：4614721

## <a name="symptoms"></a>故障特征

系统允许用户取消已报告为已完工入库的产品的原材料行的领料。

## <a name="resolution"></a>解决方法

此系统行为是有意设计的。 原材料消耗量可以调整，直到生产订单到达 *已结束* 状态。
