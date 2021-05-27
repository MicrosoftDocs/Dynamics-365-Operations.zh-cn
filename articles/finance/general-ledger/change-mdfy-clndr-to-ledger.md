---
title: 更改或重新分配分类帐日历
description: 本主题介绍了如何更改当前分配到分类帐的日历，以及如何向分类帐分配新日历。
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039942"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="1fcd8-103">更改或重新分配分类帐日历</span><span class="sxs-lookup"><span data-stu-id="1fcd8-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1fcd8-104">本主题介绍了如何更改当前分配到分类帐的日历，以及如何向分类帐分配新日历。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="1fcd8-105">问题</span><span class="sxs-lookup"><span data-stu-id="1fcd8-105">Issue</span></span>

<span data-ttu-id="1fcd8-106">有时，公司必须更改分配到分类帐的现有日历或者分配新日历。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="1fcd8-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="1fcd8-107">Resolution</span></span>

<span data-ttu-id="1fcd8-108">有两种更改或重新分配分类帐日历的方案。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="1fcd8-109">第一种方案涉及更改已分配到分类帐的现有日历。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="1fcd8-110">第二种方案涉及创建新日历并将其分配到分类帐。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="1fcd8-111">这两种更改方法都可以随时执行，或者在将交易记录过帐到分类帐之后执行。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="1fcd8-112">更改现有的会计日历</span><span class="sxs-lookup"><span data-stu-id="1fcd8-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="1fcd8-113">要更改已分配到分类帐的现有日历，请转到 **总帐 \> 分类帐设置 \> 分类帐**，然后选择会计日历的链接以打开 **分类帐日历** 页面。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="1fcd8-114">可以对日历进行的更改存在限制。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="1fcd8-115">例如，您可以更改年份中 *期间* 的开始日期和结束日期，但不能更改日历中 *年份* 的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="1fcd8-116">要更改年份中的期间，请选择适当的日历和年份。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="1fcd8-117">首先，使用 **删除期间** 按钮删除部分或全部现有的工作期间。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="1fcd8-118">可以删除除第一个工作期间之外的所有其他工作期间。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="1fcd8-119">然后，使用 **拆分期间** 按钮并通过输入下一个期间的适当开始日期，来将剩余的一个或多个期间拆分为多个新期间。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="1fcd8-120">在更改日历中的期间之后，必须在日历所分配到的每个法人（公司）中运行 **重新计算分类帐期间** 流程。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="1fcd8-121">尽管没有警告消息提醒您完成此步骤，但需要执行重新计算流程才能更新分配到总帐中每个已过帐交易记录的期间。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="1fcd8-122">要运行重新计算流程，请选择每个公司的 **分类帐设置** 页面上的 **重新计算分类帐期间**。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="1fcd8-123">如果未运行重新计算流程，则期间中可能会错误地包含试算平衡表或财务报表上的交易记录余额。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="1fcd8-124">在此情况下，您可以随时通过运行重新计算流程来更正余额。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="1fcd8-125">分配新的会计日历</span><span class="sxs-lookup"><span data-stu-id="1fcd8-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="1fcd8-126">要分配新的会计日历，请转到 **总帐 \> 分类帐设置 \> 分类帐**，然后选择 **编辑** 使 **分类帐** 页面进入编辑模式。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="1fcd8-127">然后，在 **会计日历** 字段中，选择新的会计日历。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="1fcd8-128">更改分类帐的会计日历后，必须运行 **重新计算分类帐期间**。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="1fcd8-129">当您为分类帐分配新的会计日历时，将出现一条消息提醒您完成此步骤。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="1fcd8-130">尽管该消息似乎说明重新计算流程为可选操作，但事实并非如此。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="1fcd8-131">需要更新分配给总帐中每个已过帐交易记录的期间。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="1fcd8-132">要运行重新计算流程，请选择 **分类帐设置** 页面上的 **重新计算分类帐期间**。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="1fcd8-133">如果未运行重新计算流程，则期间中可能会错误地包含试算平衡表或财务报表上的交易记录余额。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="1fcd8-134">在此情况下，您可以随时通过运行重新计算流程来更正余额。</span><span class="sxs-lookup"><span data-stu-id="1fcd8-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
