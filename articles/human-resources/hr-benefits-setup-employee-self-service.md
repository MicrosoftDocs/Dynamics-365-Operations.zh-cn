---
title: 配置员工自助服务
description: 在 Microsoft Dynamics 365 Human Resources 中，您可以为员工自助服务中的顶层导航配置磁贴。
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 32981812eac3c08e1409fe5470b550e421f5d6c9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111630"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="f6e56-103">配置员工自助服务</span><span class="sxs-lookup"><span data-stu-id="f6e56-103">Configure employee self service</span></span>

<span data-ttu-id="f6e56-104">在 Microsoft Dynamics 365 Human Resources 中，您可以为员工自助服务中的顶层导航配置磁贴。</span><span class="sxs-lookup"><span data-stu-id="f6e56-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="f6e56-105">福利计划磁贴可将用户引导至他们有资格登记参加的福利计划。</span><span class="sxs-lookup"><span data-stu-id="f6e56-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="f6e56-106">设置福利计划磁贴</span><span class="sxs-lookup"><span data-stu-id="f6e56-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="f6e56-107">在 **福利管理** 工作区中，在 **设置** 下，选择 **员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="f6e56-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f6e56-108">选择 **福利计划磁贴设置** 选项卡，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f6e56-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f6e56-109">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="f6e56-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f6e56-110">字段</span><span class="sxs-lookup"><span data-stu-id="f6e56-110">Field</span></span> | <span data-ttu-id="f6e56-111">说明</span><span class="sxs-lookup"><span data-stu-id="f6e56-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f6e56-112">**磁贴 ID**</span><span class="sxs-lookup"><span data-stu-id="f6e56-112">**Tile ID**</span></span> | <span data-ttu-id="f6e56-113">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="f6e56-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f6e56-114">**磁贴标签文本**</span><span class="sxs-lookup"><span data-stu-id="f6e56-114">**Tile label text**</span></span> | <span data-ttu-id="f6e56-115">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="f6e56-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="f6e56-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="f6e56-116">**Description**</span></span> | <span data-ttu-id="f6e56-117">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="f6e56-117">A description of the tile.</span></span> |
   | <span data-ttu-id="f6e56-118">**Internet 地址**</span><span class="sxs-lookup"><span data-stu-id="f6e56-118">**Internet address**</span></span> | <span data-ttu-id="f6e56-119">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="f6e56-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f6e56-120">**磁贴大小**</span><span class="sxs-lookup"><span data-stu-id="f6e56-120">**Tile size**</span></span> | <span data-ttu-id="f6e56-121">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="f6e56-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f6e56-122">**目标**</span><span class="sxs-lookup"><span data-stu-id="f6e56-122">**Target**</span></span> | <span data-ttu-id="f6e56-123">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="f6e56-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f6e56-124">**磁贴背景图像**</span><span class="sxs-lookup"><span data-stu-id="f6e56-124">**Tile background image**</span></span> | <span data-ttu-id="f6e56-125">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="f6e56-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f6e56-126">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="f6e56-126">**Start**</span></span> | <span data-ttu-id="f6e56-127">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f6e56-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f6e56-128">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="f6e56-128">**End**</span></span> | <span data-ttu-id="f6e56-129">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f6e56-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f6e56-130">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f6e56-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="f6e56-131">设置弹性信贷计划磁贴</span><span class="sxs-lookup"><span data-stu-id="f6e56-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="f6e56-132">在 **福利管理** 工作区中，在 **设置** 下，选择 **员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="f6e56-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f6e56-133">选择 **弹性信贷计划磁贴设置** 选项卡，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f6e56-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f6e56-134">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="f6e56-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f6e56-135">字段</span><span class="sxs-lookup"><span data-stu-id="f6e56-135">Field</span></span> | <span data-ttu-id="f6e56-136">说明</span><span class="sxs-lookup"><span data-stu-id="f6e56-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f6e56-137">**磁贴 ID**</span><span class="sxs-lookup"><span data-stu-id="f6e56-137">**Tile ID**</span></span> | <span data-ttu-id="f6e56-138">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="f6e56-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f6e56-139">**磁贴标签文本**</span><span class="sxs-lookup"><span data-stu-id="f6e56-139">**Tile label text**</span></span> | <span data-ttu-id="f6e56-140">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="f6e56-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="f6e56-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="f6e56-141">**Description**</span></span> | <span data-ttu-id="f6e56-142">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="f6e56-142">A description of the tile.</span></span> |
   | <span data-ttu-id="f6e56-143">**Internet 地址**</span><span class="sxs-lookup"><span data-stu-id="f6e56-143">**Internet address**</span></span> | <span data-ttu-id="f6e56-144">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="f6e56-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f6e56-145">**磁贴大小**</span><span class="sxs-lookup"><span data-stu-id="f6e56-145">**Tile size**</span></span> | <span data-ttu-id="f6e56-146">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="f6e56-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f6e56-147">**目标**</span><span class="sxs-lookup"><span data-stu-id="f6e56-147">**Target**</span></span> | <span data-ttu-id="f6e56-148">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="f6e56-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f6e56-149">**磁贴背景图像**</span><span class="sxs-lookup"><span data-stu-id="f6e56-149">**Tile background image**</span></span> | <span data-ttu-id="f6e56-150">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="f6e56-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f6e56-151">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="f6e56-151">**Start**</span></span> | <span data-ttu-id="f6e56-152">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f6e56-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f6e56-153">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="f6e56-153">**End**</span></span> | <span data-ttu-id="f6e56-154">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f6e56-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f6e56-155">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f6e56-155">Select **Save**.</span></span>
