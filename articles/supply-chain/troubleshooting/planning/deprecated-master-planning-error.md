---
title: 运行内置主计划引擎时收到错误
description: 当您运行已弃用的内置主计划引擎时，将收到一条错误消息。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294021"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="14eba-103">运行内置主计划引擎时收到错误</span><span class="sxs-lookup"><span data-stu-id="14eba-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="14eba-104">错误代码：ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="14eba-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="14eba-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="14eba-105">Symptoms</span></span>

<span data-ttu-id="14eba-106">当您使用已弃用的内置主计划引擎运行主计划时，将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="14eba-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="14eba-107">您收到此错误消息是因为内置主计划引擎用于计划优化所支持的方案。</span><span class="sxs-lookup"><span data-stu-id="14eba-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="14eba-108">您现在应该迁移到计划优化，因为当前的内置主计划已弃用。</span><span class="sxs-lookup"><span data-stu-id="14eba-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="14eba-109">请注意，此主计划运行已成功完成。</span><span class="sxs-lookup"><span data-stu-id="14eba-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="14eba-110">如果您的迁移非常依赖待定功能，可以请求继续使用内置主计划引擎的例外。</span><span class="sxs-lookup"><span data-stu-id="14eba-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="14eba-111">请完成以下调查表以开始使用（如果与从迁移到计划优化请求例外相关）。</span><span class="sxs-lookup"><span data-stu-id="14eba-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="14eba-112">计划优化迁移和例外调查表</span><span class="sxs-lookup"><span data-stu-id="14eba-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="14eba-113">原因</span><span class="sxs-lookup"><span data-stu-id="14eba-113">Cause</span></span>

<span data-ttu-id="14eba-114">如果您运行计划并且不使用生产控制功能，应该考虑迁移到计划优化。</span><span class="sxs-lookup"><span data-stu-id="14eba-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="14eba-115">内置主计划引擎将弃用。</span><span class="sxs-lookup"><span data-stu-id="14eba-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="14eba-116">因此，如果您想继续使用它而不会收到错误消息，则必须向 Microsoft 申请例外。</span><span class="sxs-lookup"><span data-stu-id="14eba-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="14eba-117">解决方法</span><span class="sxs-lookup"><span data-stu-id="14eba-117">Resolution</span></span>

<span data-ttu-id="14eba-118">有关如何迁移到计划优化，或如何申请例外以便可以继续改为使用弃用的内置计划引擎的详细信息，请参阅[主计划的迁移到计划优化](/dynamics365/supply-chain/master-planning/new-master-planning-engine)。</span><span class="sxs-lookup"><span data-stu-id="14eba-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
