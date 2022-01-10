---
title: 现有量列表页上的筛选器窗格不正常工作
description: “现有量列表”页上筛选器窗格中的筛选器没有按您预期的那样筛选结果。
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920490"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>现有量列表页上的筛选器窗格不正常工作

## <a name="symptoms"></a>故障特征

**现有量列表** 页上筛选器窗格中的筛选器没有按您预期的那样筛选结果。

## <a name="resolution"></a>解决方法

**现有量列表** 页面是从包含所有可用维度的详细现有库存量表组合而成的。 但是，此页面上的列表是一个摘要。 因此，它可能根据显示的维度通过聚合值来合并源表中的行。

在筛选器窗格中设置的筛选器将应用于源表，不应用于聚合列表。 此行为有时会产生意外结果，如[这些示例](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples)所示。

但是，[网格中提供的筛选器](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters)*应用于* 聚合列表。 这些筛选器既包括位于网格顶部的快速筛选器，也包括每个列标题的筛选器。
