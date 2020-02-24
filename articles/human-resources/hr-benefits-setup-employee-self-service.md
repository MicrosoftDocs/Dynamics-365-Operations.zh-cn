---
title: 配置员工自助服务
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008233"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="b2e79-102">配置员工自助服务</span><span class="sxs-lookup"><span data-stu-id="b2e79-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="b2e79-103">在 Microsoft Dynamics 365 Human Resources 中，您可以为员工自助服务中的顶层导航配置磁贴。</span><span class="sxs-lookup"><span data-stu-id="b2e79-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="b2e79-104">福利计划磁贴可将用户引导至他们有资格登记参加的福利计划。</span><span class="sxs-lookup"><span data-stu-id="b2e79-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="b2e79-105">设置角色中心磁贴</span><span class="sxs-lookup"><span data-stu-id="b2e79-105">Set up a role center tile</span></span>

1. <span data-ttu-id="b2e79-106">在**福利管理**工作区中，在**设置**下，选择**员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="b2e79-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="b2e79-107">选择**角色中心磁贴设置**选项卡，然后选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b2e79-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="b2e79-108">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="b2e79-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b2e79-109">字段</span><span class="sxs-lookup"><span data-stu-id="b2e79-109">Field</span></span> | <span data-ttu-id="b2e79-110">说明</span><span class="sxs-lookup"><span data-stu-id="b2e79-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b2e79-111">磁贴 ID</span><span class="sxs-lookup"><span data-stu-id="b2e79-111">Tile ID</span></span> | <span data-ttu-id="b2e79-112">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="b2e79-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="b2e79-113">磁贴标签文本</span><span class="sxs-lookup"><span data-stu-id="b2e79-113">Tile label text</span></span> | <span data-ttu-id="b2e79-114">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="b2e79-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="b2e79-115">说明</span><span class="sxs-lookup"><span data-stu-id="b2e79-115">Description</span></span> | <span data-ttu-id="b2e79-116">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="b2e79-116">A description of the tile.</span></span> |
   | <span data-ttu-id="b2e79-117">Internet 地址</span><span class="sxs-lookup"><span data-stu-id="b2e79-117">Internet address</span></span> | <span data-ttu-id="b2e79-118">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="b2e79-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="b2e79-119">磁贴大小</span><span class="sxs-lookup"><span data-stu-id="b2e79-119">Tile size</span></span> | <span data-ttu-id="b2e79-120">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="b2e79-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="b2e79-121">目标</span><span class="sxs-lookup"><span data-stu-id="b2e79-121">Target</span></span> | <span data-ttu-id="b2e79-122">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="b2e79-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="b2e79-123">磁贴背景图像</span><span class="sxs-lookup"><span data-stu-id="b2e79-123">Tile background image</span></span> | <span data-ttu-id="b2e79-124">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="b2e79-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="b2e79-125">开始日期</span><span class="sxs-lookup"><span data-stu-id="b2e79-125">Start</span></span> | <span data-ttu-id="b2e79-126">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b2e79-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="b2e79-127">结束日期</span><span class="sxs-lookup"><span data-stu-id="b2e79-127">End</span></span> | <span data-ttu-id="b2e79-128">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b2e79-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="b2e79-129">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b2e79-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="b2e79-130">设置福利计划磁贴</span><span class="sxs-lookup"><span data-stu-id="b2e79-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="b2e79-131">在**福利管理**工作区中，在**设置**下，选择**员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="b2e79-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="b2e79-132">选择**福利计划磁贴设置**选项卡，然后选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b2e79-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="b2e79-133">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="b2e79-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b2e79-134">字段</span><span class="sxs-lookup"><span data-stu-id="b2e79-134">Field</span></span> | <span data-ttu-id="b2e79-135">说明</span><span class="sxs-lookup"><span data-stu-id="b2e79-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b2e79-136">磁贴 ID</span><span class="sxs-lookup"><span data-stu-id="b2e79-136">Tile ID</span></span> | <span data-ttu-id="b2e79-137">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="b2e79-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="b2e79-138">磁贴标签文本</span><span class="sxs-lookup"><span data-stu-id="b2e79-138">Tile label text</span></span> | <span data-ttu-id="b2e79-139">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="b2e79-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="b2e79-140">说明</span><span class="sxs-lookup"><span data-stu-id="b2e79-140">Description</span></span> | <span data-ttu-id="b2e79-141">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="b2e79-141">A description of the tile.</span></span> |
   | <span data-ttu-id="b2e79-142">Internet 地址</span><span class="sxs-lookup"><span data-stu-id="b2e79-142">Internet address</span></span> | <span data-ttu-id="b2e79-143">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="b2e79-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="b2e79-144">磁贴大小</span><span class="sxs-lookup"><span data-stu-id="b2e79-144">Tile size</span></span> | <span data-ttu-id="b2e79-145">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="b2e79-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="b2e79-146">目标</span><span class="sxs-lookup"><span data-stu-id="b2e79-146">Target</span></span> | <span data-ttu-id="b2e79-147">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="b2e79-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="b2e79-148">磁贴背景图像</span><span class="sxs-lookup"><span data-stu-id="b2e79-148">Tile background image</span></span> | <span data-ttu-id="b2e79-149">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="b2e79-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="b2e79-150">开始日期</span><span class="sxs-lookup"><span data-stu-id="b2e79-150">Start</span></span> | <span data-ttu-id="b2e79-151">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b2e79-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="b2e79-152">结束日期</span><span class="sxs-lookup"><span data-stu-id="b2e79-152">End</span></span> | <span data-ttu-id="b2e79-153">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b2e79-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="b2e79-154">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b2e79-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="b2e79-155">设置弹性信贷计划磁贴</span><span class="sxs-lookup"><span data-stu-id="b2e79-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="b2e79-156">在**福利管理**工作区中，在**设置**下，选择**员工自助服务参数**。</span><span class="sxs-lookup"><span data-stu-id="b2e79-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="b2e79-157">选择**弹性信贷计划磁贴设置**选项卡，然后选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b2e79-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="b2e79-158">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="b2e79-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b2e79-159">字段</span><span class="sxs-lookup"><span data-stu-id="b2e79-159">Field</span></span> | <span data-ttu-id="b2e79-160">说明</span><span class="sxs-lookup"><span data-stu-id="b2e79-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b2e79-161">磁贴 ID</span><span class="sxs-lookup"><span data-stu-id="b2e79-161">Tile ID</span></span> | <span data-ttu-id="b2e79-162">磁贴的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="b2e79-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="b2e79-163">磁贴标签文本</span><span class="sxs-lookup"><span data-stu-id="b2e79-163">Tile label text</span></span> | <span data-ttu-id="b2e79-164">自助服务上磁贴将显示的文本。</span><span class="sxs-lookup"><span data-stu-id="b2e79-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="b2e79-165">说明</span><span class="sxs-lookup"><span data-stu-id="b2e79-165">Description</span></span> | <span data-ttu-id="b2e79-166">磁贴的描述。</span><span class="sxs-lookup"><span data-stu-id="b2e79-166">A description of the tile.</span></span> |
   | <span data-ttu-id="b2e79-167">Internet 地址</span><span class="sxs-lookup"><span data-stu-id="b2e79-167">Internet address</span></span> | <span data-ttu-id="b2e79-168">输入员工自助服务页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="b2e79-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="b2e79-169">磁贴大小</span><span class="sxs-lookup"><span data-stu-id="b2e79-169">Tile size</span></span> | <span data-ttu-id="b2e79-170">磁贴的大小：小、中或大。</span><span class="sxs-lookup"><span data-stu-id="b2e79-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="b2e79-171">目标</span><span class="sxs-lookup"><span data-stu-id="b2e79-171">Target</span></span> | <span data-ttu-id="b2e79-172">指定页面应在新窗口中打开还是在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="b2e79-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="b2e79-173">磁贴背景图像</span><span class="sxs-lookup"><span data-stu-id="b2e79-173">Tile background image</span></span> | <span data-ttu-id="b2e79-174">用于磁贴的图像的 URL（可选）。</span><span class="sxs-lookup"><span data-stu-id="b2e79-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="b2e79-175">开始日期</span><span class="sxs-lookup"><span data-stu-id="b2e79-175">Start</span></span> | <span data-ttu-id="b2e79-176">磁贴应该可用的开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b2e79-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="b2e79-177">结束日期</span><span class="sxs-lookup"><span data-stu-id="b2e79-177">End</span></span> | <span data-ttu-id="b2e79-178">磁贴应该可用的结束日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b2e79-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="b2e79-179">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b2e79-179">Select **Save**.</span></span>
