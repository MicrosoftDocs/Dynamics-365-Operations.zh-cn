---
title: 为日记帐启用延迟税金计算
description: 此主题介绍如何**为日记帐启用延迟税金计算**功能在有大量日记帐行时提高税金计算的性能。
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176562"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>为日记帐启用延迟税金计算
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

此主题介绍如何**为日记帐启用延迟税金计算**功能在有大量日记帐行时提高税金计算的性能。

日记帐的当前销售税计算行为在用户更新与税金有关的字段（如销售税组/物料销售税组）时实时触发。 日记帐行级别的任何更新都将重新计算所有日记帐行中的税额。 它可帮助用户查看实时计算的税额，但是如果日记帐行数量非常大，也可以导致性能问题。

此功能提供了一个选项，用于推迟税金计算以解决性能问题。 如果开启了此功能，则仅当用户单击“销售税”命令或过帐日记帐时，才会计算税额。

用户可在三个级别开启/关闭此参数：
- 按法人
- 按日记帐名称
- 按日记帐标题

系统将把日记帐标题中的参数值视为最终值。 日记帐标题中的参数值默认取自日记帐名称。 日记帐名称中的参数值默认取自创建日记帐名称时生成的分类帐参数。

如果开启此参数，将隐藏日记帐中的“实际销售税金额”和“已计算销售税金额”字段。 目标是不让用户迷惑，因为用户触发税金计算之前，这两个字段的值始终显示 0。

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>按法人启用延迟的税金计算

1. 转到**总帐 > 分类帐设置 > 总帐参数**
2. 单击**销售税**选项卡
3. 在**常规**快速选项卡下，找到参数**延迟的税金计算**，然后开启/关闭该参数

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>按日记帐名称启用延迟的税金计算

1. 转到**总帐 > 日记帐设置 > 日记帐名称**
2. 在**常规**快速选项卡下，找到参数**延迟的税金计算**，然后开启/关闭该参数

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>按日记帐启用延迟的税金计算

1. 转到**总帐 > 日记帐条目 > 普通日记帐**
2. 单击**新建**
3. 选择一个日记帐名称
4. 单击**设置**
5. 找到参数**延迟的税金计算**，然后开启/关闭该参数

![](media/delayed-tax-calculation-journal-header.png)
