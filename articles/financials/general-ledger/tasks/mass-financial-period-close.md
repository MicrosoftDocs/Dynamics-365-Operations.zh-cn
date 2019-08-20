---
title: 批量财务期间结帐
description: 此过程显示如何暂停期间，或一次性永久关闭一个期间或多个法人。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbe2d3f7d623384e1b356d9bb683db8046a85220
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846335"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="60758-103">批量财务期间结帐</span><span class="sxs-lookup"><span data-stu-id="60758-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60758-104">此过程显示如何暂停期间，或一次性永久关闭一个期间或多个法人。</span><span class="sxs-lookup"><span data-stu-id="60758-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="60758-105">此外，此任务将显示如何把用户组过帐限制到特定模块。</span><span class="sxs-lookup"><span data-stu-id="60758-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="60758-106">转到“总帐”>“期间结转”>“分类帐日历”。</span><span class="sxs-lookup"><span data-stu-id="60758-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="60758-107">请注意，显示的法人列表取决于该页中选择的会计日历。</span><span class="sxs-lookup"><span data-stu-id="60758-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="60758-108">将仅显示使用所选会计日历的法人。</span><span class="sxs-lookup"><span data-stu-id="60758-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="60758-109">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="60758-109">Click Edit.</span></span>
3. <span data-ttu-id="60758-110">选择要修改其状态的期间。</span><span class="sxs-lookup"><span data-stu-id="60758-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="60758-111">选择要更新其状态的法人。</span><span class="sxs-lookup"><span data-stu-id="60758-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="60758-112">可以通过选中网格左上方的复选标记快速选中所有法人。</span><span class="sxs-lookup"><span data-stu-id="60758-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="60758-113">选择“更新模块访问”以定义所选模块的过帐访问。</span><span class="sxs-lookup"><span data-stu-id="60758-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="60758-114">也可以通过编辑网格中的记录，逐一更新模块状态。</span><span class="sxs-lookup"><span data-stu-id="60758-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="60758-115">希望快速更新多个法人记录时，此按钮非常有用。</span><span class="sxs-lookup"><span data-stu-id="60758-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="60758-116">在“应用模块”中，选择要更新状态的模块。</span><span class="sxs-lookup"><span data-stu-id="60758-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="60758-117">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="60758-117">Click Select.</span></span>
7. <span data-ttu-id="60758-118">在“访问级别”中，选择“全部”、“无”或特定用户组。</span><span class="sxs-lookup"><span data-stu-id="60758-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="60758-119">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="60758-119">Click Select.</span></span>
    * <span data-ttu-id="60758-120">“所有”表示如果期间为开放状态，所有可编辑模块的用户可进行过帐。</span><span class="sxs-lookup"><span data-stu-id="60758-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="60758-121">“无”表示如果期间为开放状态，则用户不能过帐至该模块。</span><span class="sxs-lookup"><span data-stu-id="60758-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="60758-122">“特定用户组”表示如果期间为开放状态，只有组内用户能够过帐至该模块。</span><span class="sxs-lookup"><span data-stu-id="60758-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="60758-123">单击“更新”。</span><span class="sxs-lookup"><span data-stu-id="60758-123">Click Update.</span></span>
9. <span data-ttu-id="60758-124">选择另一个期间以更新状态。</span><span class="sxs-lookup"><span data-stu-id="60758-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="60758-125">选择要更新其期间状态的法人。</span><span class="sxs-lookup"><span data-stu-id="60758-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="60758-126">选择“更新期间状态”，然后将状态设置为“暂停”、“打开”或“永久关闭”。</span><span class="sxs-lookup"><span data-stu-id="60758-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="60758-127">“开放”表示期间内可进行过帐，但用户必须有访问权限。</span><span class="sxs-lookup"><span data-stu-id="60758-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="60758-128">“暂停”表示期间内不能过帐，但是可以重新打开期间。</span><span class="sxs-lookup"><span data-stu-id="60758-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="60758-129">“永久关闭”表示期间已关闭，永远不能打开。</span><span class="sxs-lookup"><span data-stu-id="60758-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="60758-130">不能过帐调整。</span><span class="sxs-lookup"><span data-stu-id="60758-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="60758-131">不建议在完成所有调整和审计前设置期间为“永久关闭”。</span><span class="sxs-lookup"><span data-stu-id="60758-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="60758-132">单击“更新”。</span><span class="sxs-lookup"><span data-stu-id="60758-132">Click Update.</span></span>

