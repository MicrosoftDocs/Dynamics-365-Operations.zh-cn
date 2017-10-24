---
title: "重新计算重置成本和固定资产组的保险额"
description: "本文说明更新重置成本和固定资产的保险额的流程。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 74af494f261af20d6762176d780e90b4d6644b4c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a><span data-ttu-id="7af88-103">重新计算重置成本和固定资产组的保险额</span><span class="sxs-lookup"><span data-stu-id="7af88-103">Recalculate replacement costs and insured values for fixed asset groups</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7af88-104">本文说明更新重置成本和固定资产的保险额的流程。</span><span class="sxs-lookup"><span data-stu-id="7af88-104">This article explains the process to update the replacement costs and insured values for fixed assets.</span></span>

<span data-ttu-id="7af88-105">系统可能会定期通知您，已更改固定资产的特定于重置或保险的成本。</span><span class="sxs-lookup"><span data-stu-id="7af88-105">Periodically, you might be notified that the cost to replace or insure specific fixed assets has changed.</span></span> <span data-ttu-id="7af88-106">例如，您的经理可能会通知您去年的通货膨胀率是 3%，因此，您需要将所有固定资产的重置成本增加 3%。</span><span class="sxs-lookup"><span data-stu-id="7af88-106">For example, your manager might inform you that inflation was 3 percent last year, so you need to increase the replacement cost of all fixed assets by 3 percent.</span></span> 

<span data-ttu-id="7af88-107">尽管您可以在“固定资产”窗体中编辑单独固定资产的重置成本和保险额，但您可以使用“更新重置成本和保险额”窗体一次就为资产组更新这些值。</span><span class="sxs-lookup"><span data-stu-id="7af88-107">Although you can edit the replacement cost and insured value for individual fixed assets in the Fixed assets form, you can use the Update replacement costs and insured values form to update these values for a group of assets at one time.</span></span> <span data-ttu-id="7af88-108">此信息接收了如何更新固定资产组或组中特定资产的值。</span><span class="sxs-lookup"><span data-stu-id="7af88-108">This information describes how to update values for fixed asset groups or for specific assets in the groups.</span></span>

## <a name="how-values-are-updated"></a><span data-ttu-id="7af88-109">如何更新值</span><span class="sxs-lookup"><span data-stu-id="7af88-109">How values are updated</span></span>
<span data-ttu-id="7af88-110">若要为固定资产组重新计算重置成本和保险额，您必须首先指定更改现有重置成本和保险额所采用的百分比，然后执行定期更新以实际重新计算这些值。</span><span class="sxs-lookup"><span data-stu-id="7af88-110">To recalculate replacement costs and insured values for fixed asset groups, you must first specify the percentage by which to change the existing replacement costs and insured values, and then perform the periodic update to actually recalculate the values.</span></span> <span data-ttu-id="7af88-111">在“固定资产组”窗体的“重置成本系数”和“保险额系数”字段中指定百分比。</span><span class="sxs-lookup"><span data-stu-id="7af88-111">You specify the percentage in the Replacement cost factor and Insured value factor fields in the Fixed asset groups form.</span></span> <span data-ttu-id="7af88-112">尽管您为固定资产组指定这些系数，但在您使用“更新重置成本和保险额”窗体时，可以选择只为某一组内的特定固定资产重新计算重置成本和保险额。</span><span class="sxs-lookup"><span data-stu-id="7af88-112">Although you specify these factors for the fixed asset group, when you use the Update replacement costs and insured values form, you can select to recalculate the replacement cost and insured value for only specific fixed assets in a group.</span></span> 

<span data-ttu-id="7af88-113">在您使用“更新重置成本和保险额”窗体重新计算资产的重置成本和保险额时，将使用以下公式：</span><span class="sxs-lookup"><span data-stu-id="7af88-113">When you use the Update replacement costs and insured values form to recalculate the replacement cost and insured value for the assets, the following formulas are used:</span></span>

-   <span data-ttu-id="7af88-114">\[[(资产组的重置成本系数 / 100) + 1\] \* 资产的现有重置成本</span><span class="sxs-lookup"><span data-stu-id="7af88-114">\[(Asset group's replacement cost factor / 100) + 1\] \* Asset's existing replacement cost</span></span>
-   <span data-ttu-id="7af88-115">\[[(资产组的保险额系数 / 100) + 1\] \* 资产的现有保险额</span><span class="sxs-lookup"><span data-stu-id="7af88-115">\[(Asset group's insured value factor / 100) + 1\] \* Asset's existing insured value</span></span>

> [!NOTE] 
> <span data-ttu-id="7af88-116">在您使用“更新重置成本和保险额”窗体时，将为所选资产同时更新重置成本和保险额；您不能指定只更新一个值。</span><span class="sxs-lookup"><span data-stu-id="7af88-116">When you use the Update replacement costs and insured values form, both the replacement cost and insured value are updated for the selected assets; you cannot specify that only one value be updated.</span></span> <span data-ttu-id="7af88-117">若要保持一个值不变并更新另一个值，请在“固定资产组”窗体中输入 0（零）作为系数。</span><span class="sxs-lookup"><span data-stu-id="7af88-117">To leave one value the same and update the other value, enter 0 (zero) as the factor in the Fixed asset groups form.</span></span> <span data-ttu-id="7af88-118">如果系数为零或将系数留空，将导致在更新中跳过该计算。</span><span class="sxs-lookup"><span data-stu-id="7af88-118">A zero or blank factor causes the calculation to be skipped in the update.</span></span> <span data-ttu-id="7af88-119">固定资产的帐面值和帐面净值不受定期更新的影响。</span><span class="sxs-lookup"><span data-stu-id="7af88-119">The book value and net book value of fixed assets are not affected by the periodic update.</span></span> 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a><span data-ttu-id="7af88-120">如何使用某一日期来选择要更新的物料</span><span class="sxs-lookup"><span data-stu-id="7af88-120">How to use a date to select which items to update</span></span>
<span data-ttu-id="7af88-121">默认情况下，该更新流程将更新当天尚未更新、但前几天可能已更新的所选资产。</span><span class="sxs-lookup"><span data-stu-id="7af88-121">By default, the update process updates the selected assets that have not been updated on the current day, but that might have been updated on previous days.</span></span> <span data-ttu-id="7af88-122">例如，&lt; 当前日期表示“今天之前”。</span><span class="sxs-lookup"><span data-stu-id="7af88-122">For example, &lt; current date means “before today.”</span></span> <span data-ttu-id="7af88-123">可以通过单击“选择”按钮更改“更新重置成本和保险值”窗体中的日期。</span><span class="sxs-lookup"><span data-stu-id="7af88-123">You can change the date in the Update replacement costs and insured values form by clicking the Select button.</span></span> <span data-ttu-id="7af88-124">您指定的日期条件将与该资产的最后定期更新的日期进行比较（“固定资产”窗体中的“最近期间价值/成本更新”字段）。</span><span class="sxs-lookup"><span data-stu-id="7af88-124">The date criteria that you specify is compared to the date of the last periodic update for the asset (the Last periodic value/cost update field in the Fixed assets form).</span></span> <span data-ttu-id="7af88-125">每次您成功更新某一固定资产的重置成本或保险额后，系统都将自动使用当前日期更新“最近期间价值/成本更新”字段。</span><span class="sxs-lookup"><span data-stu-id="7af88-125">Each time that you successfully update the replacement cost or insured value for a fixed asset, the Last periodic value/cost update field is automatically updated with the current date.</span></span> 

<span data-ttu-id="7af88-126">示例</span><span class="sxs-lookup"><span data-stu-id="7af88-126">Example</span></span> 

<span data-ttu-id="7af88-127">您昨天按 5% 更新了车辆、办公家具和建筑物组的重置成本，并且现在考虑准确更新这些资产。</span><span class="sxs-lookup"><span data-stu-id="7af88-127">You updated the replacement cost of the Vehicles, Office Furniture, and Buildings groups by 5 percent yesterday, and you now consider these assets to be accurately updated.</span></span> <span data-ttu-id="7af88-128">为了在今天更新所有其他固定资产时不包括这些资产，请在昨天之前的“最近期间价值/成本更新”字段中输入日期（&lt; 昨天日期），因为“车辆”、“办公家具”和“建筑物”组的最后更新发生在您输入的日期条件之外。</span><span class="sxs-lookup"><span data-stu-id="7af88-128">To exclude these assets when you update all other fixed assets today, you enter a date in the Last periodic value/cost update field that is before yesterday (&lt; yesterday's date), because the last update for the Vehicles, Office Furniture, and Buildings groups occurred outside the date criteria you entered.</span></span>

## <a name="cumulative-effect-of-each-update"></a><span data-ttu-id="7af88-129">每次更新的累积影响</span><span class="sxs-lookup"><span data-stu-id="7af88-129">Cumulative effect of each update</span></span>
<span data-ttu-id="7af88-130">每次更新都具有累积影响。</span><span class="sxs-lookup"><span data-stu-id="7af88-130">Each update has a cumulative effect.</span></span> <span data-ttu-id="7af88-131">因此，您应该仔细计划更新。</span><span class="sxs-lookup"><span data-stu-id="7af88-131">Therefore, you should plan your updates carefully.</span></span> <span data-ttu-id="7af88-132">例如，如果您在星期二将所有资产增加 3%，然后在星期五将办公家具增加 4%，办公家具将按 7.12% 的总百分比增加。</span><span class="sxs-lookup"><span data-stu-id="7af88-132">For example, if you increase all assets by 3 percent on Tuesday and then increase office furniture by 4 percent on Friday, office furniture will increase by a total of 7.12 percent.</span></span>

## <a name="scenario"></a><span data-ttu-id="7af88-133">情况</span><span class="sxs-lookup"><span data-stu-id="7af88-133">Scenario</span></span>
<span data-ttu-id="7af88-134">您的经理通知您以下固定资产变化：</span><span class="sxs-lookup"><span data-stu-id="7af88-134">Your manager notifies you of the following changes to fixed assets:</span></span>
-   <span data-ttu-id="7af88-135">将除了计算机之外的所有固定资产的重置成本增加 3.25%。</span><span class="sxs-lookup"><span data-stu-id="7af88-135">Increase the replacement cost of all fixed assets, except computers, by 3.25 percent.</span></span>
-   <span data-ttu-id="7af88-136">将所有办公家具的重置成本再增加 1%。</span><span class="sxs-lookup"><span data-stu-id="7af88-136">Increase the replacement cost of all office furniture by an additional 1 percent.</span></span>
-   <span data-ttu-id="7af88-137">将所有计算机的重置成本和保险额降低 10%。</span><span class="sxs-lookup"><span data-stu-id="7af88-137">Decrease the replacement cost and insured value of all computers by 10 percent.</span></span>

<span data-ttu-id="7af88-138">您进行了下列更改：</span><span class="sxs-lookup"><span data-stu-id="7af88-138">You make the following changes:</span></span>
1.  <span data-ttu-id="7af88-139">在“固定资产组”窗体中，为除办公家具组和计算机组之外的所有固定资产组，在“重置成本系数”字段中键入 3.25，在“保险额系数”字段中键入 0。</span><span class="sxs-lookup"><span data-stu-id="7af88-139">In the Fixed asset groups form, for all fixed asset groups except the Office Furniture group and Computers group, you type 3.25 in the Replacement cost factor field and 0 in the Insured value factor field.</span></span>
2.  <span data-ttu-id="7af88-140">对于办公家具组，您在“重置成本系数”字段中键入 4.25，在“保险额系数”字段中键入 0。</span><span class="sxs-lookup"><span data-stu-id="7af88-140">For the Office Furniture group, you type 4.25 in the Replacement cost factor field and 0 in the Insured value factor field.</span></span>
3.  <span data-ttu-id="7af88-141">对于计算机组，您在“重置成本系数”字段中键入 -10，在“保险额系数”字段中键入 -10。</span><span class="sxs-lookup"><span data-stu-id="7af88-141">For the Computers group, you type -10 in the Replacement cost factor field and -10 in the Insured value factor field.</span></span>
4.  <span data-ttu-id="7af88-142">在“更新重置成本和保险额”窗体，您单击确定执行所有固定资产的重新计算。</span><span class="sxs-lookup"><span data-stu-id="7af88-142">In the Update replacement costs and insured values form, you click OK to perform the recalculation for all fixed assets.</span></span>

<span data-ttu-id="7af88-143">下一天，您的经理通知您计算机降低了 8%，而非 10%；因此，您必须纠正重置成本和保险额。</span><span class="sxs-lookup"><span data-stu-id="7af88-143">The next day, your manager informs you that computers decreased 8 percent instead of 10 percent, so that you have to correct the replacement costs and insured values.</span></span> <span data-ttu-id="7af88-144">为了纠正此错误，您可以使用以下两种方法之一：</span><span class="sxs-lookup"><span data-stu-id="7af88-144">To fix the error, you can use either of two methods:</span></span>
-   <span data-ttu-id="7af88-145">针对“计算机”固定资产组中的每个固定资产，在“固定资产”窗体中手动更改“保险额”和“重置成本”字段。</span><span class="sxs-lookup"><span data-stu-id="7af88-145">Manually change the Insured value and Replacement cost fields in the Fixed assets form for each fixed asset in the Computers fixed asset group.</span></span> <span data-ttu-id="7af88-146">计算并手动输入这些值，就像您已按 8% 减少原始金额一样。</span><span class="sxs-lookup"><span data-stu-id="7af88-146">Calculate and manually enter the values as if you had decreased the original amount by 8 percent.</span></span> <span data-ttu-id="7af88-147">使用此方法，您不使用“更新重置成本和保险额”窗体。</span><span class="sxs-lookup"><span data-stu-id="7af88-147">By using this method, you do not use the Update replacement costs and insured values form.</span></span>
-   <span data-ttu-id="7af88-148">在“固定资产组”窗体中的“重置成本系数”和“保险额系数”字段中为计算机组输入重置成本和保险额系数。</span><span class="sxs-lookup"><span data-stu-id="7af88-148">Enter replacement cost and insured value factors for the Computers group in the Replacement cost factor and Insured value factor fields in the Fixed asset groups form.</span></span> <span data-ttu-id="7af88-149">这会将这些资产重置回其原始值（在减少 10% 之前），并且将该 8% 的减少应用于原始值。</span><span class="sxs-lookup"><span data-stu-id="7af88-149">This will both reset the assets back to their original value (before the 10 percent decrease) and apply the 8 percent decrease to the original value.</span></span> <span data-ttu-id="7af88-150">然后使用“更新重置成本和保险额”窗体根据您输入的系数重新计算这些值。</span><span class="sxs-lookup"><span data-stu-id="7af88-150">Then use the Update replacement costs and insured values form to recalculate the values, depending on the factors that you entered.</span></span>

> [!NOTE]  
> <span data-ttu-id="7af88-151">您不能通过输入正 10 的系数冲销该 -10 系数（或者系数 2，即 -10 和 -8 之间的差值），因为这些金额将不会按您的预期想法计算。</span><span class="sxs-lookup"><span data-stu-id="7af88-151">You cannot reverse the -10 factor by entering a factor of positive 10 (or a factor of 2, the difference between -10 and -8), because the amounts will not be calculated as you intend.</span></span> 






