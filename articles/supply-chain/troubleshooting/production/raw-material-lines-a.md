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
ms.openlocfilehash: f56dcf27704db5d304f002f1204631f8d389cd60bce8b3235433c0131b9473a9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744026"
---
# <a name="users-can-unpick-material-lines-for-products-that-have-been-reported-as-finished"></a>用户可以取消已报告为已完工入库的产品的材料行的领料

知识库编号：4614721

## <a name="symptoms"></a>故障特征

系统允许用户取消已报告为已完工入库的产品的原材料行的领料。

## <a name="resolution"></a>解决方法

此系统行为是有意设计的。 原材料消耗量可以调整，直到生产订单到达 *已结束* 状态。
