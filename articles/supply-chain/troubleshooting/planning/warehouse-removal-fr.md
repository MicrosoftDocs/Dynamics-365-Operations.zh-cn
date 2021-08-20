---
title: 您无法从预测行中删除仓库需求预测维度
description: 您无法从预测行中删除仓库需求预测维度。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 96af593d2e8a738258fe614f0f252620cb48c5f19eeb4425c9659ee6f9cd8c0c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741205"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>您无法从预测行中删除仓库需求预测维度

知识库编号：4614408

## <a name="symptoms"></a>故障特征

当未在 **需求预测参数** 页的 **预测维度** 选项卡上分配 **仓库** 维度时，会发生此问题。 不过，**仓库** 列在 **需求预测** 页显示（**主计划 \> 预测 \> 手动预测实体 \> 需求预测行**）。

## <a name="resolution"></a>解决方法

**需求预测参数** 页的 **预测维度** 选项卡上的设置不会影响 **需求预测** 页。 它们控制在调整后的需求预测中生成和显示的基准预测。 但是，它们不控制“实际”需求预测所需的维度。 通过对 **调整后的需求预测** 页上显示的记录授权，您可以将它们转换为预测模型的“实际”预测条目。 然后可以将该模型用于主计划。

在 **需求预测** 页上，需求预测行上显示的“实际”预测的维度是库存维度的一部分。 （此行为类似于销售订单行的行为。）如果未将系统设置为将 **仓库** 用作必需的库存维度，您可以自定义此页面来隐藏列。
