---
title: 定义供应商付款期限
description: 本主题说明如何设置供应商发票的付款期限。
author: abruer
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f47fc0cd67cddef3c73f9c4c6b8dd6f41bbe85ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838901"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="3897f-103">定义供应商付款期限</span><span class="sxs-lookup"><span data-stu-id="3897f-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3897f-104">本主题说明如何设置供应商发票的付款期限。</span><span class="sxs-lookup"><span data-stu-id="3897f-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="3897f-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="3897f-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3897f-106">转到 **导航窗格 > 模块 > 应付帐款 > 付款设置 > 付款期限**。</span><span class="sxs-lookup"><span data-stu-id="3897f-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="3897f-107">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3897f-107">Select **New**.</span></span> <span data-ttu-id="3897f-108">“支付条款”页用于定义如何计算到期日。</span><span class="sxs-lookup"><span data-stu-id="3897f-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="3897f-109">并非用于定义如何计算现金折扣日期。</span><span class="sxs-lookup"><span data-stu-id="3897f-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="3897f-110">在 **付款期限** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3897f-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="3897f-111">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3897f-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="3897f-112">在 **天数** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="3897f-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="3897f-113">此处输入的数字将会被添加到截止日期，或添加到“付款方式”所规定的结束日期。</span><span class="sxs-lookup"><span data-stu-id="3897f-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="3897f-114">例如，如果您选择 **净额**，该数字将添加到截止日期。</span><span class="sxs-lookup"><span data-stu-id="3897f-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="3897f-115">如果您选择 **本月**，将添加到当前月的最后一天来计算截止日期。</span><span class="sxs-lookup"><span data-stu-id="3897f-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="3897f-116">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3897f-116">Select **Save**.</span></span>
7. <span data-ttu-id="3897f-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3897f-117">Close the page.</span></span>
8. <span data-ttu-id="3897f-118">转到 **应付帐款 > 付款设置 > 现金折扣**。</span><span class="sxs-lookup"><span data-stu-id="3897f-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="3897f-119">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3897f-119">Select **New**.</span></span>
10. <span data-ttu-id="3897f-120">在 **现金折扣** 字段中，输入 ID。</span><span class="sxs-lookup"><span data-stu-id="3897f-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="3897f-121">在 **描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="3897f-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="3897f-122">如果供应商提供了一个分层折扣，请选择当前到期日后的下一个现金折扣。</span><span class="sxs-lookup"><span data-stu-id="3897f-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="3897f-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3897f-123">Close the page.</span></span>
14. <span data-ttu-id="3897f-124">在 **天数** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="3897f-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="3897f-125">在 **天数** 字段中输入的数量，将根据 **净额/本月** 字段中的选项，用于计算“现金折扣日期”。</span><span class="sxs-lookup"><span data-stu-id="3897f-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="3897f-126">如果选择 **净额**，则数量将添加到发票日期以确定现金折扣日期。</span><span class="sxs-lookup"><span data-stu-id="3897f-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="3897f-127">如果已选择 **本月数**，则该天数将添加到本月的最后日期以确定现金折扣日期。</span><span class="sxs-lookup"><span data-stu-id="3897f-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="3897f-128">在 **折扣** 字段中，输入现金折扣的百分比。</span><span class="sxs-lookup"><span data-stu-id="3897f-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="3897f-129">输入将为客户发票将现金折扣过帐到的主科目，然后输入将为供应商发票把现金折扣过帐到的主科目。</span><span class="sxs-lookup"><span data-stu-id="3897f-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="3897f-130">如果将 **折扣抵消帐户** 设置为 **使用供应商折扣的主科目**，则应使用该“主科目”。</span><span class="sxs-lookup"><span data-stu-id="3897f-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="3897f-131">如果该选项设置为 **发票行上的帐号**，现金折扣将过帐到发票行上的资产或支出帐户。</span><span class="sxs-lookup"><span data-stu-id="3897f-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="3897f-132">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3897f-132">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]