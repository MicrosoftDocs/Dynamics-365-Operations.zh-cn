---
title: 何时重置数据市场
description: 本主题列出了重置数据市场可能会有所改进的情况，以及重置数据市场不太可能有帮助的情况。
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71324d4aa2d20dd6ae4729412a017d130ab0144f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563721"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="d30cc-103">何时重置数据市场</span><span class="sxs-lookup"><span data-stu-id="d30cc-103">When to reset a data mart</span></span>

<span data-ttu-id="d30cc-104">重置数据市场可能很耗时。</span><span class="sxs-lookup"><span data-stu-id="d30cc-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="d30cc-105">根据具体情况，此操作可能不是所需的解决方案。</span><span class="sxs-lookup"><span data-stu-id="d30cc-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="d30cc-106">本主题列出了重置数据市场可能会有所改进的情况，以及重置数据市场不太可能有帮助的情况。</span><span class="sxs-lookup"><span data-stu-id="d30cc-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="d30cc-107">何时需要进行数据市场重置？</span><span class="sxs-lookup"><span data-stu-id="d30cc-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="d30cc-108">在重置数据市场之前，请考虑以下问题。</span><span class="sxs-lookup"><span data-stu-id="d30cc-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="d30cc-109">有一个或多个问题的回答为“是”，可能表明您的组织可以从重置数据市场中受益。</span><span class="sxs-lookup"><span data-stu-id="d30cc-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="d30cc-110">应用程序数据库已还原，但数据市场数据库未还原。</span><span class="sxs-lookup"><span data-stu-id="d30cc-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="d30cc-111">您看到一个会计期间的数据不正确，这不是报表设计问题导致的结果。</span><span class="sxs-lookup"><span data-stu-id="d30cc-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="d30cc-112">您看到一个会计期间的数据不正确，并且记录在“报表设计器”中 **集成状态** 页的“集成尝试次数”下列出（启动“报表设计器”，选择 **工具 > 集成状态**）。</span><span class="sxs-lookup"><span data-stu-id="d30cc-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="d30cc-113">您开启了一个支持事件，支持工程师已指导您在故障排除步骤中重置数据市场。</span><span class="sxs-lookup"><span data-stu-id="d30cc-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="d30cc-114">何时不适合重置数据市场？</span><span class="sxs-lookup"><span data-stu-id="d30cc-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="d30cc-115">在有些情况下，我们不建议您重置数据市场。</span><span class="sxs-lookup"><span data-stu-id="d30cc-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="d30cc-116">包括以下情况。</span><span class="sxs-lookup"><span data-stu-id="d30cc-116">These include the following.</span></span> 

- <span data-ttu-id="d30cc-117">只要不是本主题列出的原因。</span><span class="sxs-lookup"><span data-stu-id="d30cc-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="d30cc-118">您遇到与数据同步相关的性能问题。在这种情况下，重置数据市场可能无济于事。</span><span class="sxs-lookup"><span data-stu-id="d30cc-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="d30cc-119">如果您由于以下任一原因而使用定期重置模式：</span><span class="sxs-lookup"><span data-stu-id="d30cc-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="d30cc-120">**缺少数据** - 首先，消除报表设计问题和数据同步计时问题，例如，您观察到事实地图自缺少数据发布以来一直未运行。</span><span class="sxs-lookup"><span data-stu-id="d30cc-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="d30cc-121">**卡住的集成状态** - 如果集成速度慢或似乎卡住了，重置数据市场不太可能解决问题。</span><span class="sxs-lookup"><span data-stu-id="d30cc-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="d30cc-122">**尝试未成功的重置** - 如果已多次尝试完成重置，但由于缺少数据而未能成功，我们建议开启支持事件，在再次尝试重置数据市场前与支持工程师一起分析您的情况。</span><span class="sxs-lookup"><span data-stu-id="d30cc-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="d30cc-123">**过时记录** - 过时记录本身并不一定证明重置数据市场是合理的。</span><span class="sxs-lookup"><span data-stu-id="d30cc-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="d30cc-124">如果数据集较大，重置过程将需要一些时间来运行，但不太可能有改进作用。</span><span class="sxs-lookup"><span data-stu-id="d30cc-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="d30cc-125">数据市场重置不会做的事</span><span class="sxs-lookup"><span data-stu-id="d30cc-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="d30cc-126">重置仅在现有任务完成时开始。</span><span class="sxs-lookup"><span data-stu-id="d30cc-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="d30cc-127">这样可以确保不会插入旧数据。</span><span class="sxs-lookup"><span data-stu-id="d30cc-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="d30cc-128">此时，您可能会看到一条消息，如“由于有活动任务，无法处理数据市场重置。</span><span class="sxs-lookup"><span data-stu-id="d30cc-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="d30cc-129">请稍后重试。”</span><span class="sxs-lookup"><span data-stu-id="d30cc-129">Please try again later.”</span></span>
- <span data-ttu-id="d30cc-130">重置将禁用集成任务并删除所有数据市场数据。</span><span class="sxs-lookup"><span data-stu-id="d30cc-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="d30cc-131">集成将被重新启用。</span><span class="sxs-lookup"><span data-stu-id="d30cc-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="d30cc-132">以下几点指定重置数据市场 *不* 会做的两件事。</span><span class="sxs-lookup"><span data-stu-id="d30cc-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="d30cc-133">重置不会清除报表设计。</span><span class="sxs-lookup"><span data-stu-id="d30cc-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="d30cc-134">除非选择，否则重置不会清除公司数据或用户数据。</span><span class="sxs-lookup"><span data-stu-id="d30cc-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]