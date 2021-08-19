---
title: 物料不能包含物料清单或配方
description: 当您尝试确认订单时，将在物料验证期间收到一条错误消息。 它指出物料不能包含物料清单 (BOM) 或配方。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730098"
---
# <a name="item-cant-have-a-bom-or-formula"></a>物料不能包含物料清单或配方

错误代码：PRO2614

## <a name="symptoms"></a>故障特征

当您尝试确认订单时，将在物料验证期间收到以下错误消息：

> 物料不能包含物料清单或配方

## <a name="resolution"></a>解决方法

具有物料清单 (BOM) 或配方的物料必须属于 *计划物料*、*物料清单* 或 *配方* 类型。 若要更改物料的类型，请按照以下步骤操作。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 打开相关产品。
1. 在 **工程师** 快速选项卡上，将 **生产类型** 字段设置为 *计划物料*、*物料清单* 或 *配方*。
