---
title: "批次和牌照确认"
description: "此主题描述如何从移动设备设置和应用批次和牌照确认。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0444caa0f1cc176153c322b8619db65bd377ddd0
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="batch-and-license-plate-confirmation"></a>批次和牌照确认

[!include[banner](../includes/banner.md)]

批次确认允许您从移动设备确认正领取正确的批次。 在仅物料上方批次的初始领料工作上，上方批次表示高于搜索层次结构中的库位的批次范围，您必须验证领取的批次与工作行上的批次匹配。 

牌照确认允许您从移动设备确认正领取正确的牌照。 从暂存位置执行领料工作时，您必须核实已领取的牌照与该工作关联的牌照匹配。 如果通过扫描牌照启动该工作，将跳过此确认步骤。

## <a name="where-it-applies"></a>适用情况
确认在以下情况下适用：

- 批次确认适用于物料上方批次的初始领料工作。
- 确认牌照适用于从暂存位置领料。

## <a name="set-up-batch-and-license-plate-confirmation"></a>设置批次和牌照确认
您可以从移动设备菜单项配置批次和牌照确认。  
1.  从移动设备菜单项输入工作确认设置。  
2.  为批次或牌照确认选择选项。 两个选项对未启用自动确认的工作类型领料均可用。  

