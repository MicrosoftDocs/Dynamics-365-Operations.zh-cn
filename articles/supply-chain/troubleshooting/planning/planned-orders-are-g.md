---
title: 主计划为虚拟产品生成计划订单
description: 主计划在运行后为虚拟产品生成了计划订单。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741996"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>主计划为虚拟产品生成计划订单

知识库编号：4614729

## <a name="symptoms"></a>故障特征

主计划在运行后为虚拟产品生成了计划订单。

## <a name="resolution"></a>解决方法

已发布产品的 **虚拟** 选项的设置确定物料清单 (BOM) 上的默认行类型。 当 **虚拟** 选项设置为 *是* 时，系统仍会为物料创建计划订单，但每个计划订单的 **直接派生要求** 选项将设置为 *是*。 因此，计划生产订单无法自行确认。 而是在确认父生产订单时，始终自动包括在内。 而且，计划虚拟订单的物料清单行将包括在父生产订单的物料清单中。
