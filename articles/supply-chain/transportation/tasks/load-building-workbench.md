---
title: 装载计划工作台
description: 本主题介绍如何使用负荷构建工作台。
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1ed91adba5c7accf9a18d7a754d33b2b35b848f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974214"
---
# <a name="load-building-workbench"></a><span data-ttu-id="93167-103">装载计划工作台</span><span class="sxs-lookup"><span data-stu-id="93167-103">Load building workbench</span></span>

<span data-ttu-id="93167-104">负荷构建工作台可让您在创建负荷时应用负荷构建策略。</span><span class="sxs-lookup"><span data-stu-id="93167-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="93167-105">创建负荷构建策略</span><span class="sxs-lookup"><span data-stu-id="93167-105">Create a load building strategy</span></span>

<span data-ttu-id="93167-106">使用负荷构建策略自动构建负荷。</span><span class="sxs-lookup"><span data-stu-id="93167-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="93167-107">在以下情况下，此功能可能会很有用：</span><span class="sxs-lookup"><span data-stu-id="93167-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="93167-108">如果您定期装运一组特定产品，负荷策略有助于节省时间，因为您不必每次都构建相同的负荷。</span><span class="sxs-lookup"><span data-stu-id="93167-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="93167-109">如果要避免半满负荷以最大程度地提高效率，负荷策略可以帮助尽可能多地填充每个负荷。</span><span class="sxs-lookup"><span data-stu-id="93167-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="93167-110">名为 `TMSLoadBuildingVolumeStrategy` 的负荷构建策略类提供名为 *基于体积的负荷构建策略* 的负荷构建策略。</span><span class="sxs-lookup"><span data-stu-id="93167-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="93167-111">此策略允许您在装载模板上为高度和重量指定最大值，或您可以通过输入新的值来覆盖设置。</span><span class="sxs-lookup"><span data-stu-id="93167-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="93167-112">此策略是随附开箱即用的唯一策略。</span><span class="sxs-lookup"><span data-stu-id="93167-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="93167-113">（但是，您可能有一些自定义策略。）</span><span class="sxs-lookup"><span data-stu-id="93167-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="93167-114">若要使用开箱即用的 *基于体积的负荷构建策略* 策略，请在 **负荷构建工作台** 页面（**运输管理 &gt; 计划 &gt; 负荷构建工作台**）上的 **负荷构建策略** 字段中选择它。</span><span class="sxs-lookup"><span data-stu-id="93167-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="93167-115">若要创建负荷构建策略，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="93167-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="93167-116">转到 **运输管理 &gt; 设置 &gt; 负荷构建 &gt; 负荷构建策略**。</span><span class="sxs-lookup"><span data-stu-id="93167-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="93167-117">在操作窗格上，选择 **生成类列表** 以确保您具有所有可用类的最新版本。</span><span class="sxs-lookup"><span data-stu-id="93167-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="93167-118">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="93167-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="93167-119">输入策略的唯一名称，为其选择负荷构建策略类，然后输入描述。</span><span class="sxs-lookup"><span data-stu-id="93167-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="93167-120">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="93167-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="93167-121">在操作窗格中，选择 **参数**。</span><span class="sxs-lookup"><span data-stu-id="93167-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="93167-122">在 **负荷构建策略参数** 页面上，在列表中选择 **体积容量**，然后在 **值** 字段中，输入应该应用于新负荷构建策略的负荷总体积容量的百分比。</span><span class="sxs-lookup"><span data-stu-id="93167-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="93167-123">在列表中选择 **重量容量**，然后在 **值** 字段中，输入应该应用于新负荷构建策略的负荷总重量容量的百分比。</span><span class="sxs-lookup"><span data-stu-id="93167-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="93167-124">关闭 **负荷构建策略参数** 页面。</span><span class="sxs-lookup"><span data-stu-id="93167-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="93167-125">关闭 **负荷构建策略** 页面。</span><span class="sxs-lookup"><span data-stu-id="93167-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="93167-126">现在，您可以将负荷构建策略分配给负荷构建模板。</span><span class="sxs-lookup"><span data-stu-id="93167-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="93167-127">或者，您可以直接在负荷计划工作台中使用它。</span><span class="sxs-lookup"><span data-stu-id="93167-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="93167-128">在负荷构建工作台中使用负荷构建策略</span><span class="sxs-lookup"><span data-stu-id="93167-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="93167-129">转到 **运输管理 &gt; 计划 &gt; 负荷构建工作台**。</span><span class="sxs-lookup"><span data-stu-id="93167-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="93167-130">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="93167-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="93167-131">在 **负荷构建策略** 字段中选择策略。</span><span class="sxs-lookup"><span data-stu-id="93167-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="93167-132">如果您已定义负荷构建模板并已向其分配负荷构建策略，请在操作窗格的 **管理模板** 选项卡上，选择 **应用模板**。</span><span class="sxs-lookup"><span data-stu-id="93167-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="93167-133">然后，在 **应用负荷构建模板** 下拉对话框中，在 **负荷构建模板名称** 字段中选择模板。</span><span class="sxs-lookup"><span data-stu-id="93167-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="93167-134">在 **负荷模板序列** 快速选项卡上，选择一个或多个[负荷模板](load-template.md)。</span><span class="sxs-lookup"><span data-stu-id="93167-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="93167-135">工作台将尝试按此处指定的顺序将负荷装入这些类型的容器中。</span><span class="sxs-lookup"><span data-stu-id="93167-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="93167-136">通常，应将最小的容器放在列表顶部，以确保首先选择可能的最小容器。</span><span class="sxs-lookup"><span data-stu-id="93167-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="93167-137">在操作窗格上，选择 **建议负荷**。</span><span class="sxs-lookup"><span data-stu-id="93167-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="93167-138">查看建议的负荷和建议的负荷行。</span><span class="sxs-lookup"><span data-stu-id="93167-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="93167-139">在操作窗格上，选择 **创建负荷** 以创建基于 **建议的负荷行** 快速选项卡上的源单据行的负荷。</span><span class="sxs-lookup"><span data-stu-id="93167-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="93167-140">关闭 **负荷构建工作台** 页面。</span><span class="sxs-lookup"><span data-stu-id="93167-140">Close the **Load building workbench** page.</span></span>
