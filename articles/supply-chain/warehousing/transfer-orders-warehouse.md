---
title: 设置转移单的仓库
description: 此主题介绍如何设置转移单的仓库。
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 91db6e8f921bd674211f6d478b6d0f0a832c983c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847007"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>设置转移单的仓库 

[!include [banner](../includes/banner.md)]

您可以使用仓库级别创建支持在仓库之间转移订单的层次结构。 基于此设置，主计划编制计算单个仓库级别的物料需求，并从分配的源仓库生成计划转移单以完成订单。

1.  单击**库存管理**>“设置”>“库存细分”>“仓库”.

2.  选择您要重填物料的仓库。

3.  在**主计划**快速选项卡上，选择**重填**复选框。

4.  在**主仓库**字段中，选择要分配为重填物料仓库的仓库。 主计划编制计算选定仓库的物料转移需求并从分配的**主仓库**中生成计划转移单。
   
    > [!NOTE]
    > <P>如果您将<STRONG>重填</STRONG>复选框清除，将为选定的仓库分配一个与<STRONG>主仓库</STRONG>有关的仓库级别，但并不将<STRONG>主仓库</STRONG>设置为重填仓库。</P>

5.  关闭页面以应用新设置。


> [!TIP]
> <P>如果您要分配一个仓库用于重填，必须首先在<STRONG>库存维度组</STRONG>页面将此仓库设置为存储维度。 在此页面上，选择仓库的<STRONG>有效</STRONG>和<STRONG>按维度的覆盖范围计划</STRONG>字段。</P>

## <a name="set-up-transport-lead-time"></a>设置运输提前期

您还必须设置**运输天数**页面的仓库之间的运输提前期。 
1. 转到**库存管理 > 设置 > 配送 > 运输天数**。
2. 在**接收点**字段中，选择**仓库**。
3. 选择**装运仓库**、**接收仓库**和**运输天数**。 
4. （可选）还可以根据交货方式设置运输时间，在**每个交货模式的运输天数**选项卡下。
