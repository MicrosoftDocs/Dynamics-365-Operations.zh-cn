---
title: 配置工作流中的并行活动
description: 要配置并行活动，请在工作流编辑器中完成以下过程。
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dfbe78f31082ad0b1272f02e3ae9d7adbd993b1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797718"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>配置工作流中的并行活动

[!include [banner](../includes/banner.md)]

要配置并行活动，请在工作流编辑器中完成以下过程。

并行活动包括同时运行的工作流分支。

## <a name="name-a-parallel-activity"></a>对并行活动命名

按照以下步骤为并行活动输入名称。

1. 右键单击该并行活动然后单击 **属性** 打开 **属性** 窗体。
2. 在左侧窗格中，单击 **基本设置**。
3. 在 **名称** 字段中，为该并行活动输入唯一名称。
4. 单击 **关闭**。

## <a name="configure-the-branches-of-a-parallel-activity"></a>配置并行活动的分支

按照以下步骤添加和配置此并行活动的分支。

1. 双击并行活动显示并行活动的分支。
2. 要添加分支，将 **工作流元素** 区域的 **分支** 元素拖到画布上的一个插入点。 下图显示一个插入点。

    ![插入点](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > 分支的顺序并不重要，因为并行活动的所有分支同时运行。

3. 若要配置每个分支，请参阅[配置工作流中的并行分支](configure-parallel-branch-workflow.md)。
