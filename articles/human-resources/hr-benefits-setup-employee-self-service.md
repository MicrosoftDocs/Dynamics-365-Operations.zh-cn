---
title: 配置员工自助服务
description: 在 Microsoft Dynamics 365 Human Resources 中，您可以为员工自助服务中的顶层导航配置磁贴。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e763a09e0a0f13eb7222a6ffbcb31b6230b83f4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797927"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="5e577-103">配置员工自助服务</span><span class="sxs-lookup"><span data-stu-id="5e577-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5e577-104">在 Microsoft Dynamics 365 Human Resources 中，您可以为员工自助服务中的顶层导航配置磁贴。</span><span class="sxs-lookup"><span data-stu-id="5e577-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="5e577-105">福利计划磁贴可将用户引导至他们有资格登记参加的福利计划。</span><span class="sxs-lookup"><span data-stu-id="5e577-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="5e577-106">设置福利计划磁贴</span><span class="sxs-lookup"><span data-stu-id="5e577-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="5e577-107">在 **福利管理** 工作区中，在 **设置** 下，选择 **员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="5e577-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="5e577-108">选择 **福利计划磁贴设置** 选项卡，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5e577-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="5e577-109">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="5e577-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5e577-110">字段</span><span class="sxs-lookup"><span data-stu-id="5e577-110">Field</span></span> | <span data-ttu-id="5e577-111">说明</span><span class="sxs-lookup"><span data-stu-id="5e577-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5e577-112">**磁贴 ID**</span><span class="sxs-lookup"><span data-stu-id="5e577-112">**Tile ID**</span></span> | <span data-ttu-id="5e577-113">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="5e577-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="5e577-114">**磁贴标签文本**</span><span class="sxs-lookup"><span data-stu-id="5e577-114">**Tile label text**</span></span> | <span data-ttu-id="5e577-115">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="5e577-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="5e577-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5e577-116">**Description**</span></span> | <span data-ttu-id="5e577-117">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="5e577-117">A description of the tile.</span></span> |
   | <span data-ttu-id="5e577-118">**Internet 地址**</span><span class="sxs-lookup"><span data-stu-id="5e577-118">**Internet address**</span></span> | <span data-ttu-id="5e577-119">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="5e577-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="5e577-120">**磁贴大小**</span><span class="sxs-lookup"><span data-stu-id="5e577-120">**Tile size**</span></span> | <span data-ttu-id="5e577-121">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="5e577-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="5e577-122">**目标**</span><span class="sxs-lookup"><span data-stu-id="5e577-122">**Target**</span></span> | <span data-ttu-id="5e577-123">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="5e577-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="5e577-124">**磁贴背景图像**</span><span class="sxs-lookup"><span data-stu-id="5e577-124">**Tile background image**</span></span> | <span data-ttu-id="5e577-125">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="5e577-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="5e577-126">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="5e577-126">**Start**</span></span> | <span data-ttu-id="5e577-127">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="5e577-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="5e577-128">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="5e577-128">**End**</span></span> | <span data-ttu-id="5e577-129">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="5e577-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="5e577-130">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="5e577-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="5e577-131">设置弹性信贷计划磁贴</span><span class="sxs-lookup"><span data-stu-id="5e577-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="5e577-132">在 **福利管理** 工作区中，在 **设置** 下，选择 **员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="5e577-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="5e577-133">选择 **弹性信贷计划磁贴设置** 选项卡，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5e577-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="5e577-134">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="5e577-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5e577-135">字段</span><span class="sxs-lookup"><span data-stu-id="5e577-135">Field</span></span> | <span data-ttu-id="5e577-136">说明</span><span class="sxs-lookup"><span data-stu-id="5e577-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5e577-137">**磁贴 ID**</span><span class="sxs-lookup"><span data-stu-id="5e577-137">**Tile ID**</span></span> | <span data-ttu-id="5e577-138">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="5e577-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="5e577-139">**磁贴标签文本**</span><span class="sxs-lookup"><span data-stu-id="5e577-139">**Tile label text**</span></span> | <span data-ttu-id="5e577-140">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="5e577-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="5e577-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="5e577-141">**Description**</span></span> | <span data-ttu-id="5e577-142">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="5e577-142">A description of the tile.</span></span> |
   | <span data-ttu-id="5e577-143">**Internet 地址**</span><span class="sxs-lookup"><span data-stu-id="5e577-143">**Internet address**</span></span> | <span data-ttu-id="5e577-144">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="5e577-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="5e577-145">**磁贴大小**</span><span class="sxs-lookup"><span data-stu-id="5e577-145">**Tile size**</span></span> | <span data-ttu-id="5e577-146">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="5e577-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="5e577-147">**目标**</span><span class="sxs-lookup"><span data-stu-id="5e577-147">**Target**</span></span> | <span data-ttu-id="5e577-148">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="5e577-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="5e577-149">**磁贴背景图像**</span><span class="sxs-lookup"><span data-stu-id="5e577-149">**Tile background image**</span></span> | <span data-ttu-id="5e577-150">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="5e577-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="5e577-151">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="5e577-151">**Start**</span></span> | <span data-ttu-id="5e577-152">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="5e577-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="5e577-153">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="5e577-153">**End**</span></span> | <span data-ttu-id="5e577-154">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="5e577-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="5e577-155">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="5e577-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]