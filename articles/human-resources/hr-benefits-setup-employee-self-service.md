---
title: 配置员工自助服务
description: 在 Microsoft Dynamics 365 Human Resources 中，您可以为员工自助服务中的顶层导航配置磁贴。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092652"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="982e0-103">配置员工自助服务</span><span class="sxs-lookup"><span data-stu-id="982e0-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="982e0-104">在 Microsoft Dynamics 365 Human Resources 中，您可以为员工自助服务中的顶层导航配置磁贴。</span><span class="sxs-lookup"><span data-stu-id="982e0-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="982e0-105">福利计划磁贴可将用户引导至他们有资格登记参加的福利计划。</span><span class="sxs-lookup"><span data-stu-id="982e0-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="982e0-106">设置角色中心磁贴</span><span class="sxs-lookup"><span data-stu-id="982e0-106">Set up a role center tile</span></span>

1. <span data-ttu-id="982e0-107">在**福利管理**工作区中，在**设置**下，选择**员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="982e0-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="982e0-108">选择**角色中心磁贴设置**选项卡，然后选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="982e0-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="982e0-109">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="982e0-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="982e0-110">字段</span><span class="sxs-lookup"><span data-stu-id="982e0-110">Field</span></span> | <span data-ttu-id="982e0-111">说明</span><span class="sxs-lookup"><span data-stu-id="982e0-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="982e0-112">磁贴 ID</span><span class="sxs-lookup"><span data-stu-id="982e0-112">Tile ID</span></span> | <span data-ttu-id="982e0-113">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="982e0-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="982e0-114">磁贴标签文本</span><span class="sxs-lookup"><span data-stu-id="982e0-114">Tile label text</span></span> | <span data-ttu-id="982e0-115">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="982e0-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="982e0-116">说明</span><span class="sxs-lookup"><span data-stu-id="982e0-116">Description</span></span> | <span data-ttu-id="982e0-117">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="982e0-117">A description of the tile.</span></span> |
   | <span data-ttu-id="982e0-118">Internet 地址</span><span class="sxs-lookup"><span data-stu-id="982e0-118">Internet address</span></span> | <span data-ttu-id="982e0-119">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="982e0-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="982e0-120">磁贴大小</span><span class="sxs-lookup"><span data-stu-id="982e0-120">Tile size</span></span> | <span data-ttu-id="982e0-121">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="982e0-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="982e0-122">目标</span><span class="sxs-lookup"><span data-stu-id="982e0-122">Target</span></span> | <span data-ttu-id="982e0-123">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="982e0-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="982e0-124">磁贴背景图像</span><span class="sxs-lookup"><span data-stu-id="982e0-124">Tile background image</span></span> | <span data-ttu-id="982e0-125">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="982e0-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="982e0-126">开始日期</span><span class="sxs-lookup"><span data-stu-id="982e0-126">Start</span></span> | <span data-ttu-id="982e0-127">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="982e0-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="982e0-128">结束日期</span><span class="sxs-lookup"><span data-stu-id="982e0-128">End</span></span> | <span data-ttu-id="982e0-129">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="982e0-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="982e0-130">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="982e0-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="982e0-131">设置福利计划磁贴</span><span class="sxs-lookup"><span data-stu-id="982e0-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="982e0-132">在**福利管理**工作区中，在**设置**下，选择**员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="982e0-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="982e0-133">选择**福利计划磁贴设置**选项卡，然后选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="982e0-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="982e0-134">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="982e0-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="982e0-135">字段</span><span class="sxs-lookup"><span data-stu-id="982e0-135">Field</span></span> | <span data-ttu-id="982e0-136">说明</span><span class="sxs-lookup"><span data-stu-id="982e0-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="982e0-137">磁贴 ID</span><span class="sxs-lookup"><span data-stu-id="982e0-137">Tile ID</span></span> | <span data-ttu-id="982e0-138">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="982e0-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="982e0-139">磁贴标签文本</span><span class="sxs-lookup"><span data-stu-id="982e0-139">Tile label text</span></span> | <span data-ttu-id="982e0-140">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="982e0-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="982e0-141">说明</span><span class="sxs-lookup"><span data-stu-id="982e0-141">Description</span></span> | <span data-ttu-id="982e0-142">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="982e0-142">A description of the tile.</span></span> |
   | <span data-ttu-id="982e0-143">Internet 地址</span><span class="sxs-lookup"><span data-stu-id="982e0-143">Internet address</span></span> | <span data-ttu-id="982e0-144">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="982e0-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="982e0-145">磁贴大小</span><span class="sxs-lookup"><span data-stu-id="982e0-145">Tile size</span></span> | <span data-ttu-id="982e0-146">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="982e0-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="982e0-147">目标</span><span class="sxs-lookup"><span data-stu-id="982e0-147">Target</span></span> | <span data-ttu-id="982e0-148">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="982e0-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="982e0-149">磁贴背景图像</span><span class="sxs-lookup"><span data-stu-id="982e0-149">Tile background image</span></span> | <span data-ttu-id="982e0-150">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="982e0-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="982e0-151">开始日期</span><span class="sxs-lookup"><span data-stu-id="982e0-151">Start</span></span> | <span data-ttu-id="982e0-152">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="982e0-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="982e0-153">结束日期</span><span class="sxs-lookup"><span data-stu-id="982e0-153">End</span></span> | <span data-ttu-id="982e0-154">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="982e0-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="982e0-155">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="982e0-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="982e0-156">设置弹性信贷计划磁贴</span><span class="sxs-lookup"><span data-stu-id="982e0-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="982e0-157">在**福利管理**工作区中，在**设置**下，选择**员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="982e0-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="982e0-158">选择**弹性信贷计划磁贴设置**选项卡，然后选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="982e0-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="982e0-159">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="982e0-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="982e0-160">字段</span><span class="sxs-lookup"><span data-stu-id="982e0-160">Field</span></span> | <span data-ttu-id="982e0-161">说明</span><span class="sxs-lookup"><span data-stu-id="982e0-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="982e0-162">磁贴 ID</span><span class="sxs-lookup"><span data-stu-id="982e0-162">Tile ID</span></span> | <span data-ttu-id="982e0-163">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="982e0-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="982e0-164">磁贴标签文本</span><span class="sxs-lookup"><span data-stu-id="982e0-164">Tile label text</span></span> | <span data-ttu-id="982e0-165">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="982e0-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="982e0-166">说明</span><span class="sxs-lookup"><span data-stu-id="982e0-166">Description</span></span> | <span data-ttu-id="982e0-167">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="982e0-167">A description of the tile.</span></span> |
   | <span data-ttu-id="982e0-168">Internet 地址</span><span class="sxs-lookup"><span data-stu-id="982e0-168">Internet address</span></span> | <span data-ttu-id="982e0-169">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="982e0-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="982e0-170">磁贴大小</span><span class="sxs-lookup"><span data-stu-id="982e0-170">Tile size</span></span> | <span data-ttu-id="982e0-171">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="982e0-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="982e0-172">目标</span><span class="sxs-lookup"><span data-stu-id="982e0-172">Target</span></span> | <span data-ttu-id="982e0-173">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="982e0-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="982e0-174">磁贴背景图像</span><span class="sxs-lookup"><span data-stu-id="982e0-174">Tile background image</span></span> | <span data-ttu-id="982e0-175">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="982e0-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="982e0-176">开始日期</span><span class="sxs-lookup"><span data-stu-id="982e0-176">Start</span></span> | <span data-ttu-id="982e0-177">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="982e0-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="982e0-178">结束日期</span><span class="sxs-lookup"><span data-stu-id="982e0-178">End</span></span> | <span data-ttu-id="982e0-179">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="982e0-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="982e0-180">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="982e0-180">Select **Save**.</span></span>