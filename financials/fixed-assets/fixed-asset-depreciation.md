---
title: "固定资产折旧"
description: "文本提供固定资产折旧的概览。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a7f27847832e7c4814f1dc5982b6352c2ba98741
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-asset-depreciation"></a>固定资产折旧

[!include[banner](../includes/banner.md)]


文本提供固定资产折旧的概览。

折旧是一种期间交易记录，通常会减少资产负债表中固定资产的价值，并且在损益科目中作为支出计费。 因此，主科目通常用于将折旧定期贷计到资产负债表中。 对方科目是会计科目表中的损益部分中的科目。

## <a name="depreciation-adjustment"></a>折旧调整
通常，只有对已过帐折旧交易记录的更正作为“折旧调整”过帐。 因此，主科目和对方科目都同折旧科目一样进行设置。 折旧调整可以是正金额或负金额，但“主科目”（作为资产负债表科目）和“对方科目”（通常作为损益科目）的功能保持相同。

## <a name="extraordinary-depreciation"></a>特别折旧
特殊折旧类似于基本折旧。 因此，主科目用于将折旧金额贷计到资产负债表中以及减少固定资产的值。 对方科目是损益科目，折旧计算为会计期间作为支出计费。 

特殊折旧在工作方式上与基本折旧不同。 通过将“特殊折旧”作为单独的交易记录类型，您可以采用与基本折旧不同的方式，过帐和报告特殊折旧。

## <a name="special-depreciation-allowance"></a>特殊折旧补偿
您可以在资产投入使用并开始折旧的第一年使用特殊折旧补偿提取额外折旧金额。 必须在进行任何其他折旧计算前提取特殊折旧补偿。 因为特殊折旧补偿通常会在固定资产使用年限的后期才会知晓，因此最好是对不过帐到总帐的帐簿使用这种折旧类型。 您可以使用“删除尚未过帐到总帐的交易记录”定期功能删除这些帐簿的历史交易记录。 然后您可以删除固定资产帐簿的折旧历史记录，在特殊折旧补偿已知时进行过帐，再过帐当年的剩余折旧交易记录。 

您可以创建任意数量的特殊折旧补偿记录。 将这些记录分配给资产组帐簿后，这些记录会应用于资产帐簿。 

特殊折旧补偿作为百分比或固定金额输入。 过帐折旧方案时，特殊折旧补偿交易记录会作为不同于折旧交易记录的交易记录过帐到帐簿。

## <a name="depreciation-calendars"></a>折旧年份：日历
每个帐簿都有在折旧固定资产时使用的日历。 默认情况下，如果您未在帐簿上指示日历，帐簿将使用分类帐会计日历。 如果帐簿的关联折旧模板使用会计折旧年度，您必须为该帐簿选择会计日历。 

您可以在总帐中使用“**会计日历**”页创建共享日历。

有关详细信息，请参阅[折旧法和惯例](depreciation-methods-conventions.md)。




