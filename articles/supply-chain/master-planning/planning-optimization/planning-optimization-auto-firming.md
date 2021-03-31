---
title: 通过计划优化自动确认
description: 本主题说明如何通过计划优化使用自动确认。
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 9106137fe6dd097beea9914cdde541e581946f46
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227786"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="f1fde-103">通过计划优化自动确认</span><span class="sxs-lookup"><span data-stu-id="f1fde-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1fde-104">自动确认可以使您作为主计划流程的一部分确认（即下达）计划订单。</span><span class="sxs-lookup"><span data-stu-id="f1fde-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="f1fde-105">确认计划订单后，它们将转换为实际的采购订单、转移单或生产订单。</span><span class="sxs-lookup"><span data-stu-id="f1fde-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="f1fde-106">使用计划优化时，如果订单日期（即开始日期）在用于确认的时间范围内，在主计划运行期间将确认计划订单。</span><span class="sxs-lookup"><span data-stu-id="f1fde-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="f1fde-107">仅当物料与供应商关联时，才可自动确认计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="f1fde-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="f1fde-108">开启自动确认</span><span class="sxs-lookup"><span data-stu-id="f1fde-108">Turn on autofirming</span></span>

<span data-ttu-id="f1fde-109">若要开启自动确认，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f1fde-109">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="f1fde-110">在 **功能管理** 工作区中的 **新** 选项卡上，在列表中选择 **计划优化自动确认**。</span><span class="sxs-lookup"><span data-stu-id="f1fde-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="f1fde-111">如果该功能未出现在 **新** 选项卡上，请查看 **未启用** 和 **所有** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="f1fde-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="f1fde-112">选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="f1fde-112">Select **Enable now**.</span></span> <span data-ttu-id="f1fde-113">或者，选择 **时间表**，然后选择要启用该功能的时间。</span><span class="sxs-lookup"><span data-stu-id="f1fde-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="f1fde-114">设置确认时限</span><span class="sxs-lookup"><span data-stu-id="f1fde-114">Set up the firming time fence</span></span>

<span data-ttu-id="f1fde-115">确认时限是基于主计划运行日期向前推算的。</span><span class="sxs-lookup"><span data-stu-id="f1fde-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="f1fde-116">它由您输入的天数定义。</span><span class="sxs-lookup"><span data-stu-id="f1fde-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="f1fde-117">您可以通过以下方式控制确认时限：</span><span class="sxs-lookup"><span data-stu-id="f1fde-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="f1fde-118">要定义覆盖范围组的默认确认时限，请转到 **主计划** \> **设置** \> **覆盖范围** \> **覆盖范围组**，并选择一个覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="f1fde-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="f1fde-119">然后，在 **其他** 快速选项卡上的 **自动确认时限(天)** 字段中，输入天数。</span><span class="sxs-lookup"><span data-stu-id="f1fde-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="f1fde-120">要覆盖为特定物料的覆盖范围组定义的确认时限，请转到 **产品信息管理** \> **已发布产品**，然后从操作窗格中选择 **计划**，然后选择 **物料覆盖范围**。</span><span class="sxs-lookup"><span data-stu-id="f1fde-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="f1fde-121">然后，在 **常规** 选项卡上，选择 **覆盖时限**，然后在 **自动确认时限(天)** 字段中输入天数。</span><span class="sxs-lookup"><span data-stu-id="f1fde-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="f1fde-122">要覆盖为特定主计划的覆盖范围组和物料覆盖范围定义的确认时限，请转到 **主计划** \> **设置** \> **主计划**，然后选择一个主计划。</span><span class="sxs-lookup"><span data-stu-id="f1fde-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="f1fde-123">然后，在 **时限(天)** 快速选项卡上，将 **确认** 设置为 **是**，然后输入天数。</span><span class="sxs-lookup"><span data-stu-id="f1fde-123">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="f1fde-124">如果为使用计划优化的主计划运行打开了自动确认，自动确认流程将根据自动确认设置完成。</span><span class="sxs-lookup"><span data-stu-id="f1fde-124">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="f1fde-125">如果未启用自动确认，或者从 **净需求** 页面开始了计划，则会跳过自动确认流程。</span><span class="sxs-lookup"><span data-stu-id="f1fde-125">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="f1fde-126">计划优化与内置的 Supply Chain Management 计划引擎</span><span class="sxs-lookup"><span data-stu-id="f1fde-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="f1fde-127">计划优化和 Microsoft Dynamics 365 Supply Chain Management 中内置的计划引擎都可以用来自动确认计划订单。</span><span class="sxs-lookup"><span data-stu-id="f1fde-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="f1fde-128">不过，也存在某些重要差异。</span><span class="sxs-lookup"><span data-stu-id="f1fde-128">However, there are some important differences.</span></span> <span data-ttu-id="f1fde-129">例如，计划优化使用订单日期（即开始日期）来确定要确认的计划订单，而内置的 Supply Chain Management 计划引擎则使用需求日期（即结束日期）。</span><span class="sxs-lookup"><span data-stu-id="f1fde-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="f1fde-130">以下是区别汇总。</span><span class="sxs-lookup"><span data-stu-id="f1fde-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="f1fde-131">**计划优化**</span><span class="sxs-lookup"><span data-stu-id="f1fde-131">**Planning Optimization**</span></span>

- <span data-ttu-id="f1fde-132">自动确认基于订单日期（开始日期）。</span><span class="sxs-lookup"><span data-stu-id="f1fde-132">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="f1fde-133">由于订单日期（开始日期）触发确认，因此您不必将提前期视为确认时限的一部分。</span><span class="sxs-lookup"><span data-stu-id="f1fde-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="f1fde-134">如果要确认必须在当前一周开始的所有订单，则确认时限必须为一周。</span><span class="sxs-lookup"><span data-stu-id="f1fde-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="f1fde-135">**内置 Supply Chain Management 计划引擎**</span><span class="sxs-lookup"><span data-stu-id="f1fde-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="f1fde-136">自动确认基于需求日期（结束日期）。</span><span class="sxs-lookup"><span data-stu-id="f1fde-136">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="f1fde-137">为了帮助确保按到期时间确认订单，确认时限必须长于提前期。</span><span class="sxs-lookup"><span data-stu-id="f1fde-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="f1fde-138">如果要确认必须在当前一周开始的所有订单，则确认时限必须为提前期再加上一周时间。</span><span class="sxs-lookup"><span data-stu-id="f1fde-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]