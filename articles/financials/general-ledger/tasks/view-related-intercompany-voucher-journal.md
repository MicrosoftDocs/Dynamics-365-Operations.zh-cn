--- 
title: "查看日记帐中的相关内部公司凭证"
description: "在过帐内部公司交易的普通日记帐时，相关的凭证窗口显示该凭证来自其他公司。"
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, SysDataAreaSelectLookup, LedgerTransVoucher, LedgerTransRelatedVouchers
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: fe2590b43a4399c3935906c8ab67a91883bbf094
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="view-related-intercompany-voucher-from-journal"></a><span data-ttu-id="a2e0e-103">查看日记帐中的相关内部公司凭证</span><span class="sxs-lookup"><span data-stu-id="a2e0e-103">View related intercompany voucher from journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2e0e-104">在过帐内部公司交易的普通日记帐时，相关的凭证窗口显示该凭证来自其他公司。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-104">The related voucher window shows the voucher from the offset company when posting an intercompany transaction from the general journal.</span></span>


## <a name="post-an-intercompany-journal"></a><span data-ttu-id="a2e0e-105">过帐一个内部公司日记帐</span><span class="sxs-lookup"><span data-stu-id="a2e0e-105">Post an intercompany journal</span></span>
1. <span data-ttu-id="a2e0e-106">转到“普通日记帐”。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-106">Go to General journals.</span></span>
2. <span data-ttu-id="a2e0e-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-107">Click New.</span></span>
3. <span data-ttu-id="a2e0e-108">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a2e0e-109">在“名称”字段中，输入或选择内部公司日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-109">In the Name field, enter or select the intercompany journal name.</span></span>
5. <span data-ttu-id="a2e0e-110">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-110">Click Lines.</span></span>
6. <span data-ttu-id="a2e0e-111">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-111">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="a2e0e-112">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-112">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="a2e0e-113">在“描述”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-113">In the Description field, enter or select a value.</span></span>
9. <span data-ttu-id="a2e0e-114">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-114">In the Description field, type a value.</span></span>
10. <span data-ttu-id="a2e0e-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-115">Close the page.</span></span>
11. <span data-ttu-id="a2e0e-116">在“借方”字段中，输入一个数值。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-116">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="a2e0e-117">在“对方公司”字段中，键入或者选择对方公司。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-117">In the Offset company field, type or select the offset company.</span></span>
13. <span data-ttu-id="a2e0e-118">在“对方公司”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-118">In the Offset company field, enter or select a value.</span></span>
14. <span data-ttu-id="a2e0e-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-119">Close the page.</span></span>
15. <span data-ttu-id="a2e0e-120">在“抵销帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-120">In the Offset account field, specify the desired values.</span></span>
16. <span data-ttu-id="a2e0e-121">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-121">Click Post.</span></span>

## <a name="view-related-intercompany-voucher"></a><span data-ttu-id="a2e0e-122">查看相关内部公司凭证</span><span class="sxs-lookup"><span data-stu-id="a2e0e-122">View related intercompany voucher</span></span>
1. <span data-ttu-id="a2e0e-123">单击“凭证”。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-123">Click Voucher.</span></span>
2. <span data-ttu-id="a2e0e-124">单击“相关凭证”。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-124">Click Related vouchers.</span></span>
3. <span data-ttu-id="a2e0e-125">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-125">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a2e0e-126">单击“凭证”。</span><span class="sxs-lookup"><span data-stu-id="a2e0e-126">Click Voucher.</span></span>


