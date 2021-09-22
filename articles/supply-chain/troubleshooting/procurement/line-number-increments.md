---
title: 导入的采购订单显示的行号不正确
description: 通过数据管理导入采购订单时，采购订单行号不遵循系统参数中定义的增量
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475643"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>导入的采购订单显示的行号不正确

## <a name="symptoms"></a>故障特征

默认情况下，通过 *采购订单行 V2* 数据实体导入的采购订单行的自动生成的行号不使用系统参数中指定的系统行号增量。 如果您手动创建采购订单并通过用户界面 (UI) 添加行，行号会正确递增。 但是，如果您使用数据管理框架 (DMF)，则不会正确递增。

发生此问题的原因是，当您通过 DMF 导入行时，如果在导入的实体中尚未分配行号，系统将使用 DMF 的方法进行分配。 该方法始终将行号加 1。

## <a name="workaround"></a>解决方法

导入采购订单行时，请确保已在数据实体行号字段中提供了所需的行号。 在这种情况下，DMF 不会覆盖行号。
