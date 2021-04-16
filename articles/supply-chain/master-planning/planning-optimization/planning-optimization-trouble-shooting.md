---
title: 计划优化故障排除
description: 本主题介绍如何解决在使用计划优化时可能遇到的问题。
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2100235fadabe6af87849aab7d9ec55d85ea66fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812875"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="22dcb-103">计划优化故障排除</span><span class="sxs-lookup"><span data-stu-id="22dcb-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22dcb-104">本主题介绍如何解决在使用计划优化时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="22dcb-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="22dcb-105">无法完成计划优化加载项的安装</span><span class="sxs-lookup"><span data-stu-id="22dcb-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="22dcb-106">计划优化需要已启用 Lifecycle Services (LCS) 的第 2 层或更高层高可用性环境（非 OneBox 环境），并且具有 Dynamics 365 Supply Chain Management 版本 10.0.7 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="22dcb-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="22dcb-107">如果尝试在 OneBox 环境中安装此加载项，将无法完成安装。</span><span class="sxs-lookup"><span data-stu-id="22dcb-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="22dcb-108">**解决方法**：取消安装，然后使用第 2 层或更高层高可用性环境（非 OneBox 环境）。</span><span class="sxs-lookup"><span data-stu-id="22dcb-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="22dcb-109">启用计划优化后计划批处理作业失败</span><span class="sxs-lookup"><span data-stu-id="22dcb-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="22dcb-110">启用计划优化时，将自动禁用内置主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="22dcb-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="22dcb-111">如果在启用了计划优化的情况下触发了为内置 Supply Chain Management 计划引擎创建的主计划批处理作业，这些作业将失败。</span><span class="sxs-lookup"><span data-stu-id="22dcb-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="22dcb-112">可能会收到如下错误消息：*启用了计划优化时此操作触发了不支持的主计划*。</span><span class="sxs-lookup"><span data-stu-id="22dcb-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="22dcb-113">**解决方法**：取消为内置 Supply Chain Management 计划引擎创建的所有主计划批处理作业。</span><span class="sxs-lookup"><span data-stu-id="22dcb-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="22dcb-114">计划优化结果与之前结果不同</span><span class="sxs-lookup"><span data-stu-id="22dcb-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="22dcb-115">计划优化在某些方面与内置主计划设计不同。</span><span class="sxs-lookup"><span data-stu-id="22dcb-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="22dcb-116">这也可能是待定功能导致的。</span><span class="sxs-lookup"><span data-stu-id="22dcb-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="22dcb-117">**解决方法**：运行计划优化适应分析，然后在引用相关文档了解影响时分析结果。</span><span class="sxs-lookup"><span data-stu-id="22dcb-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="22dcb-118">有关详细信息，请参阅[计划优化拟合分析](planning-optimization-fit-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="22dcb-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="22dcb-119">不能启用计划优化</span><span class="sxs-lookup"><span data-stu-id="22dcb-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="22dcb-120">**连接状态** 必须先为 **已连接**，然后才能将 **使用计划优化** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="22dcb-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="22dcb-121">有关详细信息，请参阅[开始使用计划优化](get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="22dcb-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="22dcb-122">**解决方法**：确保已成功安装了计划优化加载项。</span><span class="sxs-lookup"><span data-stu-id="22dcb-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="22dcb-123">CTP 期间显示错误消息</span><span class="sxs-lookup"><span data-stu-id="22dcb-123">Error message is shown during CTP</span></span>

<span data-ttu-id="22dcb-124">如果在已启用了计划优化的情况下从销售订单运行可承诺量 (CTP)，将收到以下错误消息：*启用了计划优化时此操作触发了不支持的主计划*。</span><span class="sxs-lookup"><span data-stu-id="22dcb-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="22dcb-125">这与为了支持生产订单时计划的待定功能有关。</span><span class="sxs-lookup"><span data-stu-id="22dcb-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="22dcb-126">**解决方法：** 启用计划优化后避免计算 CTP，直到 CTP 支持可用。</span><span class="sxs-lookup"><span data-stu-id="22dcb-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22dcb-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="22dcb-127">Additional resources</span></span>

[<span data-ttu-id="22dcb-128">开始使用计划优化</span><span class="sxs-lookup"><span data-stu-id="22dcb-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="22dcb-129">计划优化适应分析</span><span class="sxs-lookup"><span data-stu-id="22dcb-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]