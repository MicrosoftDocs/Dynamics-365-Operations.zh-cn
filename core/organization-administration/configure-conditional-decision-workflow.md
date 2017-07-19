---
title: "在工作流中配置有条件决策"
description: "使用以下过程配置有条件决策的属性。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c21c8e33ab3a88e1b93ca81d6f0770f1c77fe139
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>在工作流中配置有条件决策

[!include[banner](../includes/banner.md)]


使用以下过程配置有条件决策的属性。

有条件决策是工作流划分为两个分支处的点。 要配置有条件决策，在工作流编辑器中，右键单击“有条件决策”，然后单击“**属性**”以打开“**属性**”窗体。

## <a name="name-a-decision"></a>为决策命名
按照以下步骤为有条件决策输入名称。
1.  在左侧窗格中，单击**基本设置**。
2.  在“**名称**”字段中，为有条件决策输入唯一名称。

## <a name="set-conditions"></a>设置条件
系统确定使用的分支，方法是评估提交的文档以确定其是否符合特定条件。
1.  在左侧窗格中，单击**基本设置**。
2.  单击“**添加条件**”。
3.  输入条件。
4.  如果需要，输入其他条件。
5.  要验证输入的条件是否正确配置，请完成以下步骤：
    1.  单击“**测试**”以打开“**测试工作流条件**”窗体。
    2.  在该窗体的“**验证条件**”区域中选择某个记录。
    3.  单击“**测试**”。 系统对该记录进行评估，判断其是否符合您定义的条件。
    4.  单击“**确定**”或“**取消**”返回到“**属性**”窗体。






