---
title: "配置工作流中的并行活动"
description: "要配置并行活动，请在工作流编辑器中完成以下过程。"
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 818fb054742b935d002a7341e54a37eca0bb4761
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>配置工作流中的并行活动

要配置并行活动，请在工作流编辑器中完成以下过程。

并行活动包括同时运行的工作流分支。

## <a name="name-a-parallel-activity"></a>对并行活动命名
按照以下步骤为并行活动输入名称。
1.  右键单击，然后单击**并行活动属性** ** **打开属性窗体。
2.  在左侧窗格中，单击**基本设置**。
3.  在“**名称**”字段中，为该并行活动输入唯一名称。
4.  单击**“关闭”**。

## <a name="configure-the-branches-of-a-parallel-activity"></a>配置并行活动的分支
按照以下步骤添加和配置此并行活动的分支。
1.  双击并行活动显示并行活动的分支。
2.  要添加分支，将“**工作流元素**”区域的“**分支**”元素拖到画布上的一个插入点。 下图显示了一个插入点。![插入点](./media/workflow_insertionpoint.gif)
    | **注意**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | 分支的顺序并不重要，因为并行活动的所有分支同时运行。 |

3.  若要配置每个分支，请参阅“[配置并行分支](http://axhelp.dynamics.com/en/wiki/configure-a-parallel-branch/)”。




