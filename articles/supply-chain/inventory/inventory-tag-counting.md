---
title: 库存标签盘点
description: 此主题提供有关您用于将仓库的实际内容与现有库存量进行比较的标签盘点的信息。
author: MarkusFogelberg
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99d2dadf7d49a37b5f06bf08ece5454bf742d5dc6ab001402ace3097d5ec96b6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735199"
---
# <a name="inventory-tag-counting"></a>库存标签盘点

[!include [banner](../includes/banner.md)]

此主题提供有关您用于将仓库的实际内容与现有库存量进行比较的标签盘点的信息。

通过在 **标签盘点** 页上创建行，您将在每个库存物料上放置一个标签编号（如从 1 到 500 的数字）。 在盘点期间，您应在相应标签上输入物料编号和数量。 此标签随后可用作标签盘点日记帐中的输入的基础。 过帐标签盘点日记帐后，将在 **盘点** 页上创建一个新的盘点日记帐。 新日记帐基于您创建的标签盘点日记帐行。 要按特定库存维度对物料进行标签盘点，请在创建标签盘点日记帐时在 **显示维度** 页上选择维度。 例如，要盘点特定仓库中的物料，请选中 **仓库** 复选框。 如果选择了 **库存和仓库管理参数** 页上的 **盘点期间锁定物料** 滑块，则在盘点期间无法实际更新物料。 但是，标签盘点日记帐中的物料在盘点期间不会锁定。 在将标签盘点行过帐并转移到盘点日记帐之前不会创建库存交易记录。 如果随机输入了标签并且您希望标识缺失的标签，请单击 **标签** 列标题以按标签为行排序。

## <a name="additional-resources"></a>其他资源

[周期盘点](../warehousing/cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]