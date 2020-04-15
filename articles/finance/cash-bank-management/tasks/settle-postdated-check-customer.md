---
title: 结算客户的远期支票
description: 该支票由银行清算后，您可以结算过期支票。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc6f90e7adb3facdfa1facb50fecb0de4ccb04d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141572"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="2dcea-103">结算客户的远期支票</span><span class="sxs-lookup"><span data-stu-id="2dcea-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2dcea-104">该支票由银行清算后，您可以结算过期支票。</span><span class="sxs-lookup"><span data-stu-id="2dcea-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="2dcea-105">此财务交易记录也清算了过期支票的过桥科目交易记录。</span><span class="sxs-lookup"><span data-stu-id="2dcea-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="2dcea-106">在开始此任务之前，必须完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="2dcea-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="2dcea-107">设置远期支票</span><span class="sxs-lookup"><span data-stu-id="2dcea-107">Set up postdated checks</span></span>

2) <span data-ttu-id="2dcea-108">为客户登记和过帐远期支票</span><span class="sxs-lookup"><span data-stu-id="2dcea-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="2dcea-109">此任务指南的角色是出纳员。</span><span class="sxs-lookup"><span data-stu-id="2dcea-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="2dcea-110">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="2dcea-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="2dcea-111">转到“信贷和收款”>“查询和报表”>“付款”>“客户远期支票”。</span><span class="sxs-lookup"><span data-stu-id="2dcea-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="2dcea-112">单击“结算”。</span><span class="sxs-lookup"><span data-stu-id="2dcea-112">Click Settle.</span></span>
3. <span data-ttu-id="2dcea-113">单击“结算清算条目”。</span><span class="sxs-lookup"><span data-stu-id="2dcea-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="2dcea-114">结算用于支票交易记录的客户帐户。</span><span class="sxs-lookup"><span data-stu-id="2dcea-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="2dcea-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2dcea-115">Close the page.</span></span>
5. <span data-ttu-id="2dcea-116">转到“总帐”>“日记帐条目”>“普通日记帐”。</span><span class="sxs-lookup"><span data-stu-id="2dcea-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="2dcea-117">在“显示”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="2dcea-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="2dcea-118">选择或清除“仅显示用户创建的”复选框。</span><span class="sxs-lookup"><span data-stu-id="2dcea-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="2dcea-119">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="2dcea-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="2dcea-120">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="2dcea-120">Click Lines.</span></span>
10. <span data-ttu-id="2dcea-121">单击“凭证”。</span><span class="sxs-lookup"><span data-stu-id="2dcea-121">Click Voucher.</span></span>
11. <span data-ttu-id="2dcea-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="2dcea-122">Close the page.</span></span>

