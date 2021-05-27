---
title: 何时重置数据市场
description: 本主题列出了重置数据市场可能会有所改进的情况，以及重置数据市场不太可能有帮助的情况。
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988984"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="d97a8-103">何时重置数据市场</span><span class="sxs-lookup"><span data-stu-id="d97a8-103">When to reset a data mart</span></span>

<span data-ttu-id="d97a8-104">重置数据市场可能很耗时。</span><span class="sxs-lookup"><span data-stu-id="d97a8-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="d97a8-105">根据具体情况，此操作可能不是所需的解决方案。</span><span class="sxs-lookup"><span data-stu-id="d97a8-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="d97a8-106">本主题列出了重置数据市场可能会有所改进的情况，以及重置数据市场不太可能有帮助的情况。</span><span class="sxs-lookup"><span data-stu-id="d97a8-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="d97a8-107">何时需要进行数据市场重置？</span><span class="sxs-lookup"><span data-stu-id="d97a8-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="d97a8-108">在重置数据市场之前，请考虑以下问题。</span><span class="sxs-lookup"><span data-stu-id="d97a8-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="d97a8-109">有一个或多个问题的回答为“是”，可能表明您的组织可以从重置数据市场中受益。</span><span class="sxs-lookup"><span data-stu-id="d97a8-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="d97a8-110">应用程序数据库是否已还原？</span><span class="sxs-lookup"><span data-stu-id="d97a8-110">Was the application database restored?</span></span>
- <span data-ttu-id="d97a8-111">如果您开启了一个支持事件，支持工程师是否已指导您在故障排除步骤中重置数据市场？</span><span class="sxs-lookup"><span data-stu-id="d97a8-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="d97a8-112">何时不适合重置数据市场？</span><span class="sxs-lookup"><span data-stu-id="d97a8-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="d97a8-113">在有些情况下，我们不建议您重置数据市场。</span><span class="sxs-lookup"><span data-stu-id="d97a8-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="d97a8-114">包括以下情况。</span><span class="sxs-lookup"><span data-stu-id="d97a8-114">These include the following.</span></span> 

- <span data-ttu-id="d97a8-115">您遇到与数据同步相关的性能问题。</span><span class="sxs-lookup"><span data-stu-id="d97a8-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="d97a8-116">如果您由于以下任一原因而使用定期重置模式：</span><span class="sxs-lookup"><span data-stu-id="d97a8-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="d97a8-117">**缺少数据**</span><span class="sxs-lookup"><span data-stu-id="d97a8-117">**Missing data**</span></span> 
  - <span data-ttu-id="d97a8-118">**卡住的集成状态**</span><span class="sxs-lookup"><span data-stu-id="d97a8-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="d97a8-119">**过时记录** - 过时记录本身并不一定证明重置数据市场是合理的。</span><span class="sxs-lookup"><span data-stu-id="d97a8-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="d97a8-120">如果数据集较大，重置过程将需要一些时间来运行，但不太可能有改进作用。</span><span class="sxs-lookup"><span data-stu-id="d97a8-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="d97a8-121">什么是数据市场重置？</span><span class="sxs-lookup"><span data-stu-id="d97a8-121">What is a data mart reset?</span></span>
- <span data-ttu-id="d97a8-122">重置仅在现有任务完成时开始。</span><span class="sxs-lookup"><span data-stu-id="d97a8-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="d97a8-123">这样可以确保不会插入旧数据。</span><span class="sxs-lookup"><span data-stu-id="d97a8-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="d97a8-124">此时，您可能会看到一条消息，如“由于有活动任务，无法处理数据市场重置。</span><span class="sxs-lookup"><span data-stu-id="d97a8-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="d97a8-125">请稍后重试。”</span><span class="sxs-lookup"><span data-stu-id="d97a8-125">Please try again later.”</span></span>
- <span data-ttu-id="d97a8-126">重置将禁用集成任务并删除所有数据市场数据。</span><span class="sxs-lookup"><span data-stu-id="d97a8-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="d97a8-127">集成将被重新启用。</span><span class="sxs-lookup"><span data-stu-id="d97a8-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="d97a8-128">如果重置数据市场，是否会丢失已经设计好的报表？</span><span class="sxs-lookup"><span data-stu-id="d97a8-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="d97a8-129">不会，您的报表存储在不受数据市场重置影响的 SQL 表中。</span><span class="sxs-lookup"><span data-stu-id="d97a8-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="d97a8-130">如果您担心丢失设计好的报表，可以备份不想丢失的设计。</span><span class="sxs-lookup"><span data-stu-id="d97a8-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="d97a8-131">要进行备份，请打开报表设计器，转到 **公司 > 公司 > 构建基块 > 导出**。</span><span class="sxs-lookup"><span data-stu-id="d97a8-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="d97a8-132">重置数据市场时是否有必要让所有用户都退出系统？</span><span class="sxs-lookup"><span data-stu-id="d97a8-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="d97a8-133">不需要，用户可以在数据市场重置期间在系统中继续工作。</span><span class="sxs-lookup"><span data-stu-id="d97a8-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="d97a8-134">但是，在重置完成之前，他们无法访问使用 Financial Reporter 创建的任何报表。</span><span class="sxs-lookup"><span data-stu-id="d97a8-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
