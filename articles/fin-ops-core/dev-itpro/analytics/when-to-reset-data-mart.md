---
title: 数据市场重置常见问题解答
description: 本主题提供有关数据市场重置的一些常见问题的解答。
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266601"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="76e05-103">数据市场重置常见问题解答</span><span class="sxs-lookup"><span data-stu-id="76e05-103">Data mart resets FAQ</span></span>

<span data-ttu-id="76e05-104">本主题提供有关数据市场重置的一些常见问题的解答。</span><span class="sxs-lookup"><span data-stu-id="76e05-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="76e05-105">数据市场的重置可能是一个耗时的流程，并且可能不是所需的解决方案，视具体情况而定。</span><span class="sxs-lookup"><span data-stu-id="76e05-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="76e05-106">因此，本主题包括有关数据市场重置可能有帮助的情况以及不太可能有帮助的情况的信息。</span><span class="sxs-lookup"><span data-stu-id="76e05-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="76e05-107">什么是数据市场重置？</span><span class="sxs-lookup"><span data-stu-id="76e05-107">What is a data mart reset?</span></span>

<span data-ttu-id="76e05-108">数据市场重置将禁用集成任务，删除所有数据市场数据，然后重新启用集成。</span><span class="sxs-lookup"><span data-stu-id="76e05-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="76e05-109">为了确保不插入旧数据，可以仅在完成现有任务后启动数据市场重置。</span><span class="sxs-lookup"><span data-stu-id="76e05-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="76e05-110">如果您在所有任务完成之前尝试重置数据市场，您可能会收到一条消息，例如“由于活动任务，无法处理数据市场重置。</span><span class="sxs-lookup"><span data-stu-id="76e05-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="76e05-111">请稍后重试。”</span><span class="sxs-lookup"><span data-stu-id="76e05-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="76e05-112">何时需要进行数据市场重置？</span><span class="sxs-lookup"><span data-stu-id="76e05-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="76e05-113">如果以下一项或多项陈述适用于您的情况，您的组织可以从数据市场重置中受益：</span><span class="sxs-lookup"><span data-stu-id="76e05-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="76e05-114">应用程序数据库已还原。</span><span class="sxs-lookup"><span data-stu-id="76e05-114">The application database was restored.</span></span>
- <span data-ttu-id="76e05-115">您打开了一个支持票证，支持工程师已指导您在故障排除步骤中重置数据市场。</span><span class="sxs-lookup"><span data-stu-id="76e05-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="76e05-116">何时进行数据市场重置不合适？</span><span class="sxs-lookup"><span data-stu-id="76e05-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="76e05-117">下面是一些不建议重置数据市场的情况：</span><span class="sxs-lookup"><span data-stu-id="76e05-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="76e05-118">您遇到与数据同步相关的性能问题。</span><span class="sxs-lookup"><span data-stu-id="76e05-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="76e05-119">您由于以下任一原因而使用定期重置模式：</span><span class="sxs-lookup"><span data-stu-id="76e05-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="76e05-120">**缺少数据** – 如果您发现缺少数据，请向 Microsoft 开具支持票证，以查看您的报表格式和可能的数据同步问题。</span><span class="sxs-lookup"><span data-stu-id="76e05-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="76e05-121">**卡住的集成状态**</span><span class="sxs-lookup"><span data-stu-id="76e05-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="76e05-122">**过时记录** – 过时记录本身并不一定证明数据市场重置是合理的。</span><span class="sxs-lookup"><span data-stu-id="76e05-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="76e05-123">如果数据集较大，重置流程将需要一些时间来运行，但不太可能有任何改进作用。</span><span class="sxs-lookup"><span data-stu-id="76e05-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="76e05-124">如果重置数据市场，是否会丢失已经设计好的报表？</span><span class="sxs-lookup"><span data-stu-id="76e05-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="76e05-125">否。</span><span class="sxs-lookup"><span data-stu-id="76e05-125">No.</span></span> <span data-ttu-id="76e05-126">您的报表存储在不受数据市场重置影响的 SQL 表中。</span><span class="sxs-lookup"><span data-stu-id="76e05-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="76e05-127">如果您担心丢失设计好的报表，可以备份不想丢失的设计。</span><span class="sxs-lookup"><span data-stu-id="76e05-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="76e05-128">若要备份设计，请打开 Report Designer，转到 **公司 \> 公司 \> 构建基块 \> 导出**。</span><span class="sxs-lookup"><span data-stu-id="76e05-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="76e05-129">是否所有用户都必须退出系统才能重置数据市场？</span><span class="sxs-lookup"><span data-stu-id="76e05-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="76e05-130">否。</span><span class="sxs-lookup"><span data-stu-id="76e05-130">No.</span></span> <span data-ttu-id="76e05-131">用户可以在数据市场重置期间在系统中继续工作。</span><span class="sxs-lookup"><span data-stu-id="76e05-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="76e05-132">但是，在重置完成之前，用户无法访问使用 Financial Reporter 创建的任何报表。</span><span class="sxs-lookup"><span data-stu-id="76e05-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
