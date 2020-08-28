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
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998ee559a092c4acd34a6df05e893bdbf4289099
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698307"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="78ad3-103">配置工作流中的并行活动</span><span class="sxs-lookup"><span data-stu-id="78ad3-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78ad3-104">要配置并行活动，请在工作流编辑器中完成以下过程。</span><span class="sxs-lookup"><span data-stu-id="78ad3-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="78ad3-105">并行活动包括同时运行的工作流分支。</span><span class="sxs-lookup"><span data-stu-id="78ad3-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="78ad3-106">对并行活动命名</span><span class="sxs-lookup"><span data-stu-id="78ad3-106">Name a parallel activity</span></span>

<span data-ttu-id="78ad3-107">按照以下步骤为并行活动输入名称。</span><span class="sxs-lookup"><span data-stu-id="78ad3-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="78ad3-108">右键单击该并行活动然后单击**属性**打开**属性**窗体。</span><span class="sxs-lookup"><span data-stu-id="78ad3-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="78ad3-109">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="78ad3-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="78ad3-110">在**名称**字段中，为该并行活动输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="78ad3-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="78ad3-111">单击**关闭**。</span><span class="sxs-lookup"><span data-stu-id="78ad3-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="78ad3-112">配置并行活动的分支</span><span class="sxs-lookup"><span data-stu-id="78ad3-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="78ad3-113">按照以下步骤添加和配置此并行活动的分支。</span><span class="sxs-lookup"><span data-stu-id="78ad3-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="78ad3-114">双击并行活动显示并行活动的分支。</span><span class="sxs-lookup"><span data-stu-id="78ad3-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="78ad3-115">要添加分支，将**工作流元素**区域的**分支**元素拖到画布上的一个插入点。</span><span class="sxs-lookup"><span data-stu-id="78ad3-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="78ad3-116">下图显示一个插入点。</span><span class="sxs-lookup"><span data-stu-id="78ad3-116">The following figure shows an insertion point.</span></span>

    ![插入点](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="78ad3-118">分支的顺序并不重要，因为并行活动的所有分支同时运行。</span><span class="sxs-lookup"><span data-stu-id="78ad3-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="78ad3-119">若要配置每个分支，请参阅[配置工作流中的并行分支](configure-parallel-branch-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="78ad3-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
