---
title: 不能向“采购协议”页面添加“计价单位”字段
description: 当我以行视图模式打开“采购协议”页时，我无法通过在该行的概览中添加“计价单位”字段来个性化该页面
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 56d2ce94fb4b74d982cb6a052cca71c18190cd04
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475660"
---
# <a name="you-cant-add-the-price-unit-field-to-the-purchase-agreement-page"></a>不能向“采购协议”页面添加“计价单位”字段

## <a name="symptoms"></a>故障特征

当我以行视图模式打开 **采购协议** 页时，我无法通过在该行的概览中添加 **计价单位** 字段来个性化该页面。

## <a name="resolution"></a>解决方法

协议框架中的某些共享字段不能包含在个性化设置中。 由于实现了数据模型，因此会出现此限制。 因此，您无法个性化 **计价单位** 字段。
