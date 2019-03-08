---
title: 定义供应商付款期限
description: 设置供应商发票的付款条款。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68c69d5be5ccbdfb17fea7c61121cbf26fee48d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "358546"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="6097b-103">定义供应商付款期限</span><span class="sxs-lookup"><span data-stu-id="6097b-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6097b-104">设置供应商发票的付款条款。</span><span class="sxs-lookup"><span data-stu-id="6097b-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="6097b-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="6097b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6097b-106">转到“应付账款”>“支付设置“>“支付条款”。</span><span class="sxs-lookup"><span data-stu-id="6097b-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="6097b-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6097b-107">Click New.</span></span>
    * <span data-ttu-id="6097b-108">“支付条款”页用于定义如何计算到期日。</span><span class="sxs-lookup"><span data-stu-id="6097b-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="6097b-109">并非用于定义如何计算现金折扣日期。</span><span class="sxs-lookup"><span data-stu-id="6097b-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="6097b-110">在“付款条款”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6097b-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="6097b-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6097b-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6097b-112">在“天数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6097b-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="6097b-113">此处输入的数字将会被添加到截止日期，或添加到“付款方式”所规定的结束日期。</span><span class="sxs-lookup"><span data-stu-id="6097b-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="6097b-114">例如，如果您选择“净额”，该数字将添加到截止日期。</span><span class="sxs-lookup"><span data-stu-id="6097b-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="6097b-115">如果您选择“本月”，将添加到当前月的最后一天来计算截止日期。</span><span class="sxs-lookup"><span data-stu-id="6097b-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="6097b-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6097b-116">Click Save.</span></span>
7. <span data-ttu-id="6097b-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6097b-117">Close the page.</span></span>
8. <span data-ttu-id="6097b-118">转到“应付账款”>“付款设置”>“现金折扣”。</span><span class="sxs-lookup"><span data-stu-id="6097b-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="6097b-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6097b-119">Click New.</span></span>
10. <span data-ttu-id="6097b-120">在“现金折扣”字段中，输入 ID。</span><span class="sxs-lookup"><span data-stu-id="6097b-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="6097b-121">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6097b-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="6097b-122">如果供应商提供了一个分层折扣，请选择当前到期日后的下一个现金折扣。</span><span class="sxs-lookup"><span data-stu-id="6097b-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="6097b-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6097b-123">Close the page.</span></span>
14. <span data-ttu-id="6097b-124">在“天数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6097b-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="6097b-125">在“天数”字段中输入的数量，将根据“净额/本月”字段中的选项，用于计算“现金折扣日期”。</span><span class="sxs-lookup"><span data-stu-id="6097b-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="6097b-126">如果选择“净额”，则数量将添加到发票日期以确定现金折扣日期。</span><span class="sxs-lookup"><span data-stu-id="6097b-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="6097b-127">如果已选择“本月数”，则该天数将添加到本月的最后日期以确定现金折扣日期。</span><span class="sxs-lookup"><span data-stu-id="6097b-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="6097b-128">在“折扣”字段中，输入现金折扣的百分比。</span><span class="sxs-lookup"><span data-stu-id="6097b-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="6097b-129">输入客户发票的现金折扣主帐户。</span><span class="sxs-lookup"><span data-stu-id="6097b-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="6097b-130">输入供应商发票的现金折扣主帐户。</span><span class="sxs-lookup"><span data-stu-id="6097b-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="6097b-131">如果将“折扣抵消帐户”设置为“使用供应商折扣的主帐号”，则应使用该“主帐号”。</span><span class="sxs-lookup"><span data-stu-id="6097b-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="6097b-132">如果该选项设置为“发票行上的帐号”，现金折扣将过帐到发票行上的资产或支出帐户。</span><span class="sxs-lookup"><span data-stu-id="6097b-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="6097b-133">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6097b-133">Click Save.</span></span>

