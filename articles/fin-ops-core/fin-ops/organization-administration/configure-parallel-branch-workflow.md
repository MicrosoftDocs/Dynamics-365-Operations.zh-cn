---
title: 配置工作流中的并行分支
description: 要配置并行分支，请在工作流编辑器中完成以下过程。
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b5270660f0dbe4351f0088787468a563d2f36cf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747799"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="d3c0c-103">配置工作流中的并行分支</span><span class="sxs-lookup"><span data-stu-id="d3c0c-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3c0c-104">要配置并行分支，请在工作流编辑器中完成以下过程。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="d3c0c-105">并行分支主要是在母工作流上下文中运行的工作流。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="d3c0c-106">为分支命名</span><span class="sxs-lookup"><span data-stu-id="d3c0c-106">Name a branch</span></span>

<span data-ttu-id="d3c0c-107">按照以下步骤为并行分支输入名称。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="d3c0c-108">右键单击并行分支，然后单击 **属性**。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="d3c0c-109">将显示 **属性** 窗体。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="d3c0c-110">在左侧窗格中，单击 **基本设置**。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="d3c0c-111">在 **名称** 字段中，为该并行分支输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="d3c0c-112">单击 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="d3c0c-113">设计和配置分支的元素</span><span class="sxs-lookup"><span data-stu-id="d3c0c-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="d3c0c-114">按照以下步骤可以设计和配置并行分支的元素。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="d3c0c-115">双击并行分支。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="d3c0c-116">将工作流元素拖到画布上，然后配置元素，就如您创建任何其他工作流一样。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="d3c0c-117">有关详细信息，请参阅[创建工作流概览](create-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="d3c0c-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3c0c-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="d3c0c-118">Additional resources</span></span>

[<span data-ttu-id="d3c0c-119">创建工作流概览</span><span class="sxs-lookup"><span data-stu-id="d3c0c-119">Create workflows overview</span></span>](create-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]