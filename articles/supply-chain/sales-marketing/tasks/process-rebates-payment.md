--- 
title: "处理付款返点"
description: "该过程说明如何将已批准和处理的客户返点转换到贷方通知单。"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 791ec304b9ea7c49fbea506d73c4daffd4478739
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="49f62-103">处理付款返点</span><span class="sxs-lookup"><span data-stu-id="49f62-103">Process rebates for payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49f62-104">该过程说明如何将已批准和处理的客户返点转换到贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="49f62-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="49f62-105">您可以使用 USMF 公司演示运行此指南。</span><span class="sxs-lookup"><span data-stu-id="49f62-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="49f62-106">本指南中的先决条件是拥有一个或多个状态为“标记”的要求。</span><span class="sxs-lookup"><span data-stu-id="49f62-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="49f62-107">如果您正在使用 USMF，在开始本指南之前，您应该运行“生成和处理客户返点”指南。</span><span class="sxs-lookup"><span data-stu-id="49f62-107">If you’re using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="49f62-108">将返点要求转换为贷方通知单</span><span class="sxs-lookup"><span data-stu-id="49f62-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="49f62-109">转到“所有客户”。</span><span class="sxs-lookup"><span data-stu-id="49f62-109">Go to All customers.</span></span>
2. <span data-ttu-id="49f62-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="49f62-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="49f62-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="49f62-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="49f62-112">在“操作窗格”上，单击“收款”。</span><span class="sxs-lookup"><span data-stu-id="49f62-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="49f62-113">单击“结算交易记录”。</span><span class="sxs-lookup"><span data-stu-id="49f62-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="49f62-114">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="49f62-114">Click Functions.</span></span>
7. <span data-ttu-id="49f62-115">单击“返点计划”。</span><span class="sxs-lookup"><span data-stu-id="49f62-115">Click Rebate program.</span></span>
    * <span data-ttu-id="49f62-116">“返利”页面会列示您已在客户返利工作台中处理，且状态为标记的返利要求。</span><span class="sxs-lookup"><span data-stu-id="49f62-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="49f62-117">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="49f62-117">Click Edit.</span></span>
    * <span data-ttu-id="49f62-118">根据您想要包括在贷方通知单中的要求，设置“标记”字段中的核取标志。</span><span class="sxs-lookup"><span data-stu-id="49f62-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="49f62-119">单击“功能”。</span><span class="sxs-lookup"><span data-stu-id="49f62-119">Click Functions.</span></span>
10. <span data-ttu-id="49f62-120">单击“创建贷方通知单”。</span><span class="sxs-lookup"><span data-stu-id="49f62-120">Click Create credit note.</span></span>
    * <span data-ttu-id="49f62-121">一条消息会显示，以通知您某一日记帐已过帐（这是“应收帐款参数”页中明确指出的“应收帐款耗损日记帐”)。</span><span class="sxs-lookup"><span data-stu-id="49f62-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="49f62-122">这会导致实际负债（贷方）金额被移到客户余额。</span><span class="sxs-lookup"><span data-stu-id="49f62-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="49f62-123">这意味着，客户的帐户已被记入贷方，“返点”应计项目帐户已被记入借方。</span><span class="sxs-lookup"><span data-stu-id="49f62-123">This means that the customer’s account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="49f62-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="49f62-124">Close the page.</span></span>
12. <span data-ttu-id="49f62-125">单击“取消”。</span><span class="sxs-lookup"><span data-stu-id="49f62-125">Click Cancel.</span></span>
    * <span data-ttu-id="49f62-126">这会刷新页面，以便您可以查看更新。</span><span class="sxs-lookup"><span data-stu-id="49f62-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="49f62-127">在“操作窗格”上，单击“收款”。</span><span class="sxs-lookup"><span data-stu-id="49f62-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="49f62-128">单击“结算交易记录”。</span><span class="sxs-lookup"><span data-stu-id="49f62-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="49f62-129">请注意，负数金额的交易记录（表示总返点金额，而无发票参考编号）已被添加到客户余额。</span><span class="sxs-lookup"><span data-stu-id="49f62-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="49f62-130">单击“取消”。</span><span class="sxs-lookup"><span data-stu-id="49f62-130">Click Cancel.</span></span>


