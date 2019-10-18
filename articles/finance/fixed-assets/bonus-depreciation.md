---
title: 额外折旧
description: 本文提供红利折旧功能的概览。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 687ba57042ad65d3a1ff4ad92f0da774c6751eac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187375"
---
# <a name="bonus-depreciation"></a>额外折旧

[!include [banner](../includes/banner.md)]

本文提供红利折旧功能的概览。

对于额外折旧，您可以在资产投入使用并开始折旧的第一年中提取额外的折旧金额。 必须在进行任何其他折旧计算前提取额外折旧。 因此，最好是在帐簿禁用“过帐到总帐”功能时使用额外折旧。 您可以使用**删除尚未过帐到总帐的交易记录**选项删除未过帐到总帐的帐簿的历史交易记录。 然后，您将来可以通过删除先前过帐的折旧交易记录在资产生命周期中容纳额外折旧。 

您可以通过使用方案过程计算额外折旧，也可以创建手动额外折旧交易记录。 如果该资产帐簿存在折旧交易记录或折旧调整交易记录，则不能创建额外折旧交易记录。

当您使用方案过程计算额外折旧时，所有现有额外折旧交易记录都包括在基础计算中。 该计算还包括您为资产手动输入的任何先前的额外折旧。 

如果某资产将进行多项额外折旧，将考虑优先级。 每此额外折旧减少了下此额外折旧的资产基础。 在额外折旧计算的资产基础中不考虑残值，而且折旧惯例不会应用于额外折旧。 

目前在美国，某些财产符合第 179 条关于财产的规定。 通过使用第 179 条扣缴，您可以撤消某项资产的全部或部分成本，直到一个限额。 您可以通过在您投入资产的那一年减少成本来恢复成本。

## <a name="example"></a>示例
以下额外折旧与资产帐簿相关联：

-   **第 179 条：** 1,000.00，优先级 1
-   **自由区**：30%，优先级 2

资产购置成本为 5,000.00。 计算额外折旧时，根据第 179 条的折旧规定，第一笔额外折旧金额为 1,000.00 美元。 

对于“自由区”折旧而言，将使用以下方法计算下一笔额外折旧金额： 

购置成本 – 1,000（第 179 条的折旧规定） x 30% = 1,200 

如果额外折旧金额大于剩余的购置成本，额外折旧金额将是额外折旧计算金额和剩余购置成本两者中较小的金额。 

如果剩余的购置成本为 0（零）或更少，将不会生成额外折旧交易记录。 

使用方案过程计算额外折旧时，将会为与资产帐簿关联的所有适用额外折旧记录创建额外折旧交易记录。 

您可以创建数量不限的额外折旧记录。 将这些记录分配给资产组帐簿后，这些记录会应用于资产帐簿。 

额外折旧作为百分比或固定金额输入。 过帐折旧方案时，额外折旧交易记录将作为不同于折旧交易记录的单独的交易记录过帐到帐簿。


