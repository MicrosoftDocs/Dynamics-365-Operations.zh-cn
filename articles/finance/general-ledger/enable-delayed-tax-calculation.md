---
title: 为日记帐启用延迟税金计算
description: 此主题介绍如何启用延迟税金计算功能以在有大量日记帐行时帮助提高税金计算的性能。
author: EricWang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: fddb6d3a9850b8f2f88f813f9591006637c7e535
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713125"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>为日记帐启用延迟税金计算
[!include [banner](../includes/banner.md)]


本主题说明如何延迟日记帐的销售税计算。 当日记帐行很多时，此功能有助于提高税金计算的性能。

默认情况下，每当更新与税相关的字段时，都会计算日记帐行上的销售税金额。 这些字段包括销售税组和物料销售税组的字段。 日记帐行的任何更新都会导致重新计算所有日记帐行的税额。 尽管此行为可以帮助用户实时查看税额，但是如果日记帐行的数量很大，也可能影响性能。

延迟税金计算功能使您可以延迟日记帐的税金计算，从而帮助解决性能问题。 开启此功能时，则仅当用户选择 **销售税** 或过帐日记帐时，才会计算税额。

您可以在三个级别上延迟销售税的计算：

- 法人
- 日记帐名称
- 日记帐标题

系统优先考虑日记帐标头的设置。 默认情况下，此设置来自日记帐名称。 默认情况下，创建日记帐名称时，日记帐名称的设置从 **总帐参数** 页面上的设置获取。 以下各节说明如何为法人、日记帐名称和日记帐标头打开延迟税金计算。

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>在法人级别启用延迟税金计算

1. 转到 **总帐 \> 分类帐设置 \> 总帐参数**。
2. 在 **销售税** 选项卡，在 **常规** 快速选项卡，将 **延迟税金计算** 选项设置为 **是**。

![总帐参数图像。](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>在日记帐名称级别启用延迟税金计算

1. 转到 **总帐 \> 日记帐设置 \> 日记帐名称**。
2. 在 **常规** 快速选项卡上，在 **销售税** 部分，将 **延迟税金计算** 选项设置为 **是**。

![日记帐名称图像。](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>在日记帐标头级别启用延迟税金计算

1. 转到 **总帐 \> 日记帐条目 \> 普通日记帐**。
2. 选择 **新建**。
3. 选择一个日记帐名称。
4. 在 **设置** 选项卡上，将 **延迟税金计算** 选项设置为 **是**。

![普通日记帐页面图像。](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
