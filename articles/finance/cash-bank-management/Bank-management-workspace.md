---
title: 银行管理工作区
description: 此主题提供了有关银行管理工作区的信息。 此工作区显示与公司银行帐户关联的信息，并包括一个汇总视图和一个分析页。 汇总视图显示汇总磁贴、银行帐户信息、余额图表和关联信息。 分析页使用 Microsoft Power BI 的功能显示与银行帐户余额相关的视觉对象。
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3c5d248c5431b7a54835c699618a0a27ab760754
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260199"
---
# <a name="bank-management-workspace"></a>银行管理工作区

[!include [banner](../includes/banner.md)]

**银行管理** 工作区显示与公司银行帐户关联的信息。 该工作区包括一个 **汇总** 视图和一个 **分析** 页。 **汇总** 视图显示汇总磁贴、银行帐户信息、余额图表和关联信息。 **分析** 页使用 Microsoft Power BI 的功能显示与银行帐户余额相关的视觉对象。

## <a name="summary-view"></a>汇总视图

### <a name="summary"></a>汇总

在 **汇总** 部分中的磁贴提供您的银行帐户概览并提供最常用页面的快速访问。 银行对帐信息特定于高级银行对帐功能。 包含的信息仅适用于 **银行帐户** 页上的 **高级银行对帐** 选项设置为 **是** 的银行帐户。 从 **汇总** 部分可以导入跨所有法人的银行帐户的电子银行文件。

### <a name="bank-accounts"></a>银行帐户

法人中的每个银行帐户用 **银行帐户** 部分的一张卡表示。 显示当前余额，并且您可以钻取到构成该汇总余额金额的交易记录。 **过渡交易记录** 金额也可以让您钻取到构成该汇总金额的交易记录。 过渡交易记录是指已经使用过渡功能过帐但尚未清除的任何待定交易记录。 **待定余额** 金额是指当前余额减去过渡或待定交易记录。

卡上还显示上次对帐的银行帐户。 仅当对银行帐户启用高级银行对帐时才显示此信息。

### <a name="balance"></a>所有者权益

**余额** 图表显示在 **银行帐户** 部分选择的银行帐户的历史余额信息或法人中的所有银行帐户的历史余额信息汇总。 此信息适用于不同期间：本周、本月、本年度、过去五年以及所有期间（银行帐户的完整历史记录）。 

如果您正在查看单个银行帐户的 **余额** 图表，则以银行帐户币种显示历史余额。 如果您正在查看法人中的所有银行帐户的图表，则以记帐币种显示历史余额。

图表顶部显示上次更新数据的时间信息。 您可以按需要更新数据。

### <a name="related-information"></a>相关信息

从 **相关信息** 部分可打开 **普通日记帐** 页面以完成银行转帐。 您还可以快速打开 **银行交易记录** 和 **过渡交易** 页。

## <a name="analytics-view"></a>分析视图

**分析** 页提供有关当前公司中的银行帐户的重要指标。 页面上提供以下可视化项：

-   系统币种的银行总余额
-   按法人分类的余额
-   银行帐户币种的今日实际余额与预测余额比较
-   按银行帐户分类的余额
-   原币余额

您可以从 **现金概览–所有公司** 工作区查看跨所有公司的银行分析。 有关详细信息，请参阅[现金概览 Power BI 内容](Cash-Overview-Power-BI-content.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]