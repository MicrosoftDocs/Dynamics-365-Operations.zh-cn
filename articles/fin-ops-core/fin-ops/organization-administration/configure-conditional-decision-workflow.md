---
title: 配置工作流中的有条件决策
description: 使用以下过程配置有条件决策的属性。
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a593d4e188f47b73967f0c5468f7d7c3e9f64dc8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567452"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>配置工作流中的有条件决策

[!include [banner](../includes/banner.md)]

使用以下过程配置有条件决策的属性。

有条件决策是工作流划分为两个分支处的点。 要配置有条件决策，在工作流编辑器中，右键单击“有条件决策”，然后单击 **属性** 以打开 **属性** 窗体。

## <a name="name-a-decision"></a>为决策命名

按照以下步骤为有条件决策输入名称。

1. 在左侧窗格中，单击 **基本设置**。
2. 在 **名称** 字段中，为有条件决策输入唯一名称。

## <a name="set-conditions"></a>设置条件

系统确定使用的分支，方法是评估提交的文档以确定其是否符合特定条件。

1. 在左侧窗格中，单击 **基本设置**。
2. 单击 **添加条件**。
3. 输入条件。
4. 如果需要，输入其他条件。
5. 要验证输入的条件是否正确配置，请完成以下步骤：

    1. 单击 **测试** 以打开 **测试工作流条件** 窗体。
    2. 在该窗体的 **验证条件** 区域中选择某个记录。
    3. 单击 **测试**。 系统对该记录进行评估，判断其是否符合您定义的条件。
    4. 单击 **确定** 或 **取消** 返回到 **属性** 窗体。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]