---
title: 结算供应商的远期支票
description: 在支票过期银行清算之后，如果银行已清算支票交易记录，签发一张远期支票给供应商进行结算。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08cf4ec805e632470ef778f31beb87597e0ca096
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976183"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="f7817-103">结算供应商的远期支票</span><span class="sxs-lookup"><span data-stu-id="f7817-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7817-104">在支票过期银行清算之后，如果银行已清算支票交易记录，签发一张远期支票给供应商进行结算。</span><span class="sxs-lookup"><span data-stu-id="f7817-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="f7817-105">在开始这步之前请完成以下过程。</span><span class="sxs-lookup"><span data-stu-id="f7817-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="f7817-106">设置远期支票</span><span class="sxs-lookup"><span data-stu-id="f7817-106">Set up postdated checks</span></span>

2) <span data-ttu-id="f7817-107">为供应商登记和过帐远期支票</span><span class="sxs-lookup"><span data-stu-id="f7817-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="f7817-108">本过程由财务主管完成。</span><span class="sxs-lookup"><span data-stu-id="f7817-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="f7817-109">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="f7817-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="f7817-110">转到“应付帐款”>“付款”>“供应商远期支票”。</span><span class="sxs-lookup"><span data-stu-id="f7817-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="f7817-111">单击“结算”。</span><span class="sxs-lookup"><span data-stu-id="f7817-111">Click Settle.</span></span>
3. <span data-ttu-id="f7817-112">单击“结算清算条目”。</span><span class="sxs-lookup"><span data-stu-id="f7817-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="f7817-113">结算供应商帐户的支票交易记录。</span><span class="sxs-lookup"><span data-stu-id="f7817-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="f7817-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7817-114">Close the page.</span></span>
5. <span data-ttu-id="f7817-115">转到“总帐”>“日记帐条目”>“普通日记帐”。</span><span class="sxs-lookup"><span data-stu-id="f7817-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="f7817-116">在“显示”字段中，选择“全部”。</span><span class="sxs-lookup"><span data-stu-id="f7817-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="f7817-117">选择或清除“仅显示用户创建的”复选框。</span><span class="sxs-lookup"><span data-stu-id="f7817-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="f7817-118">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f7817-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f7817-119">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="f7817-119">Click Lines.</span></span>
10. <span data-ttu-id="f7817-120">单击“凭证”。</span><span class="sxs-lookup"><span data-stu-id="f7817-120">Click Voucher.</span></span>
11. <span data-ttu-id="f7817-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f7817-121">Close the page.</span></span>

