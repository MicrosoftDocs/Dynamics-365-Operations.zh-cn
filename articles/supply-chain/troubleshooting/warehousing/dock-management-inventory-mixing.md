---
title: 使用码头管理配置文件时混合库存类型
description: 要让码头管理配置文件有效地管理库存的混合，必须先设置工作标题分解。 此页面介绍了方法。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475672"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>使用码头管理配置文件时正在混合库存类型

## <a name="symptoms"></a>故障特征

您正在使用 *装运合并政策*。 您已经为 *位置模板* 设置了 *码头管理配置文件*，但是在创建工作时，库存类型在最终位置混合。

## <a name="resolution"></a>解决方法

码头管理配置文件需要工作提前拆分。 换言之，码头管理配置文件预期工作标题不会有多个放置位置。

要让码头管理配置文件有效地管理库存的混合，必须设置工作标题分解。

在此示例中，我们配置了码头管理配置文件，以将 **不应混合的库存类型** 设置为 *装运 ID*，然后我们将为其设置工作标题分解：

1. 转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。
1. 选择要编辑的 **工作订单类型**（例如，*采购订单*）。
1. 选择要编辑的工作模板。
1. 在操作窗格上，选择 **编辑查询**。
1. 打开 **排序** 选项卡，添加具有以下设置的行：
    - **表** - *临时工作交易*
    - **派生表** - *临时工作交易*
    - **字段** - *装运 ID*
1. 选择 **确定**。
1. 您将返回 **工作模板** 页。 在“操作窗格”中选择 **工作标题中断**。
1. 在操作窗格上，选择 **编辑**。
1. 选中与 **字段名称** 装 *运 ID* 关联的复选框。
1. 在操作窗格上，选择 **保存**。
