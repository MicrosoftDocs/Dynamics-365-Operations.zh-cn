---
title: "配置工作流中的并行活动"
description: "要配置并行活动，请在工作流编辑器中完成以下过程。"
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
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5473327c0665c9183746eb8125c7a368fbedc21e
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a><span data-ttu-id="c1174-103">配置工作流中的并行活动</span><span class="sxs-lookup"><span data-stu-id="c1174-103">Configure a parallel activity in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c1174-104">要配置并行活动，请在工作流编辑器中完成以下过程。</span><span class="sxs-lookup"><span data-stu-id="c1174-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="c1174-105">并行活动包括同时运行的工作流分支。</span><span class="sxs-lookup"><span data-stu-id="c1174-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="c1174-106">对并行活动命名</span><span class="sxs-lookup"><span data-stu-id="c1174-106">Name a parallel activity</span></span>
<span data-ttu-id="c1174-107">按照以下步骤为并行活动输入名称。</span><span class="sxs-lookup"><span data-stu-id="c1174-107">Follow these steps to enter a name for a parallel activity.</span></span>
1.  <span data-ttu-id="c1174-108">右键单击该并行活动然后单击“**属性**”打开“**属性**”窗体。</span><span class="sxs-lookup"><span data-stu-id="c1174-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2.  <span data-ttu-id="c1174-109">在左侧窗格中，单击**基本设置**。</span><span class="sxs-lookup"><span data-stu-id="c1174-109">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="c1174-110">在“**名称**”字段中，为该并行活动输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="c1174-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4.  <span data-ttu-id="c1174-111">单击**“关闭”**。</span><span class="sxs-lookup"><span data-stu-id="c1174-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="c1174-112">配置并行活动的分支</span><span class="sxs-lookup"><span data-stu-id="c1174-112">Configure the branches of a parallel activity</span></span>
<span data-ttu-id="c1174-113">按照以下步骤添加和配置此并行活动的分支。</span><span class="sxs-lookup"><span data-stu-id="c1174-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>
1.  <span data-ttu-id="c1174-114">双击并行活动显示并行活动的分支。</span><span class="sxs-lookup"><span data-stu-id="c1174-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2.  <span data-ttu-id="c1174-115">要添加分支，将“**工作流元素**”区域的“**分支**”元素拖到画布上的一个插入点。</span><span class="sxs-lookup"><span data-stu-id="c1174-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="c1174-116">下图显示了一个插入点。![插入点](./media/workflow_insertionpoint.gif)</span><span class="sxs-lookup"><span data-stu-id="c1174-116">The following figure shows an insertion point.![Insertion point](./media/workflow_insertionpoint.gif)</span></span>
    | <span data-ttu-id="c1174-117">**注意**</span><span class="sxs-lookup"><span data-stu-id="c1174-117">**Note**</span></span>                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c1174-118">分支的顺序并不重要，因为并行活动的所有分支同时运行。</span><span class="sxs-lookup"><span data-stu-id="c1174-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span> |

3.  <span data-ttu-id="c1174-119">若要配置每个分支，请参阅“[配置并行分支](configure-parallel-branch-workflow.md)”。</span><span class="sxs-lookup"><span data-stu-id="c1174-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>






