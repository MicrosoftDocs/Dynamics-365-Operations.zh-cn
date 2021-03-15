---
title: 分类帐分配规则
description: 本文提供有关分类帐分配规则的信息。 介绍这些分配规则的各个组件和可为其使用的分配方法。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8006221c36abcc24893741458d2cf6b25a6010e6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988744"
---
# <a name="ledger-allocation-rules"></a>分类帐分配规则

[!include [banner](../includes/banner.md)]

本文提供有关分类帐分配规则的信息。 介绍这些分配规则的各个组件和可为其使用的分配方法。

分类帐分配规则用于自动计算并生成分配日记帐和科目分录，以便分配分类帐余额或固定金额。 分配方法可以是可变的，也可以是固定的。 以下分配方法可用于分类帐分配规则：

-   **基础** – 此可变方法在分配取决于实际分类帐余额时使用，基于筛选条件。 例如，可以基于每个部门的销售额相对于各部门总销售额的比例分配公司广告成本。
-   **固定百分比** 和 **固定权重**– 对于这些方法，分配百分比或权重是直接针对规则定义的。 例如，可以分配广告支出，以便部门 A 收到 70% 的广告支出，部门 B 收到 30%。
-   **平均** – 此方法将金额平均分配给每个定义的目标。 例如，如果为部门 A 和部门 B 定义了目标，则可以分配广告支出以便部门 A 和部门 B 收到 50% 的广告支出。

如果“基础”用作分配规则的分配方法，则您还必须定义单独的分类帐分配基础规则。 “处理分配请求”流程允许用户在过帐或删除已计算的分摊之前，处理分类帐分配规则和预览生成的分配日记帐分录。

## <a name="components-of-ledger-allocation-rules"></a>分类帐分配规则的组成部分
每个分配规则都具有四个组成部分：常规、来源、目标和对方。 一个附加的组成部分，即分类帐分配基础规则，在“基础”用作分配方法时是必需的。 每个组成部分都提供处理分配所需的信息的重要部分。

-   **常规** – 此组成部分是用户指定选项的位置，例如分配方法、内部公司规则设置以及规则是否处于活动状态。
-   **来源** – 此组成部分是用户为分配指定源数据的位置。 分配可以基于分类帐余额（**数据源** = **分类帐**）或固定金额（**数据源** = **固定值**）。 当 **数据源** 设置为 **分类帐** 时，必须为分类帐分配规则定义来源筛选条件（例如，对于广告支出）。
-   **目标** – 此组成部分定义应如何分配和考虑分配计算的结果。 例如，每个部门可以有一个目标行。
-   **对方** – 此组成部分定义应如何为平衡目标条目的对方条目确定主科目和维度。 通常会使用用户定义的选项，而不是给予来源的帐户和维度。 当 **数据源** 设置为 **固定值** 时，**来源** 将不能用作选项。
-   **分类帐分配基础规则** – 这些规则使用自己的源筛选条件来确定应为分配使用哪个分类帐余额（例如，每个部门的收入）。 每个分配基础规则可以用于多个分配规则。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]