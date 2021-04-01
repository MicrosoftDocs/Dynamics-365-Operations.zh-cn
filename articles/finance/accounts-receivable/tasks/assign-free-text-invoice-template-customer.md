---
title: 向客户分配普通账单模板
description: 此任务展示的是如何将普通发票模板分配到客户。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1f87c731a603dbb3def0ebc2d2ebe54f9706053
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254099"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="7398b-103">向客户分配普通账单模板</span><span class="sxs-lookup"><span data-stu-id="7398b-103">Assign a free text invoice template to a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7398b-104">此任务展示的是如何将普通发票模板分配到客户。</span><span class="sxs-lookup"><span data-stu-id="7398b-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="7398b-105">此任务使用 USMF 演示公司，旨在为负责管理和处理应收帐款发票的用户使用。</span><span class="sxs-lookup"><span data-stu-id="7398b-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="7398b-106">在 **导航窗格** 中，转到 **模块 > 应收帐款 > 客户 > 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="7398b-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="7398b-107">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="7398b-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7398b-108">在 **操作窗格** 中，单击 **发票**。</span><span class="sxs-lookup"><span data-stu-id="7398b-108">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="7398b-109">单击 **重复发票**。</span><span class="sxs-lookup"><span data-stu-id="7398b-109">Click **Recurring invoices**.</span></span> <span data-ttu-id="7398b-110">使用此页将普通发票模板分配给客户，并指定发送给客户的频率。</span><span class="sxs-lookup"><span data-stu-id="7398b-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="7398b-111">单击 **新建** 以将新模板分配给客户。</span><span class="sxs-lookup"><span data-stu-id="7398b-111">Click **New** to assign a new template to the customer.</span></span>
6. <span data-ttu-id="7398b-112">在 **模板** 字段中，选择您要分配给客户的普通发票模板。</span><span class="sxs-lookup"><span data-stu-id="7398b-112">In the **Template** field, select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="7398b-113">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="7398b-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="7398b-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7398b-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7398b-115">在 **记帐开始日期** 字段中，输入第一张发票的生成日期。</span><span class="sxs-lookup"><span data-stu-id="7398b-115">In the **Billing start date** field, enter the date when the first invoice will be generated.</span></span>
10. <span data-ttu-id="7398b-116">在 **重复执行结束** 部分中，输入重复执行结束日期。</span><span class="sxs-lookup"><span data-stu-id="7398b-116">In the **Recurrence end** section, enter a recurring end date.</span></span>  
    * <span data-ttu-id="7398b-117">选择以下选项之一：无结束日期 - 将会无限期生成发票，直到删除来自该客户帐户的模板。</span><span class="sxs-lookup"><span data-stu-id="7398b-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>
    * <span data-ttu-id="7398b-118">计费结束日期 - 选择此选项并输入可以生成发票的最后日期。</span><span class="sxs-lookup"><span data-stu-id="7398b-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
11. <span data-ttu-id="7398b-119">在 **最大累计金额** 字段中，输入最大累计金额，达到此值后将停止生成发票。</span><span class="sxs-lookup"><span data-stu-id="7398b-119">In the **Maximum cumulative amount** field, enter the maximum cumulative amount after which invoice generation will stop.</span></span> <span data-ttu-id="7398b-120">输入使用所选模板可以达到的最大累计金额。</span><span class="sxs-lookup"><span data-stu-id="7398b-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="7398b-121">例如，若您输入 1,000.00，并在每月生成 100.00 金额的发票，则发票在生成第十个时将停止生成。</span><span class="sxs-lookup"><span data-stu-id="7398b-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
12. <span data-ttu-id="7398b-122">在 **通过使用默认值生成重复发票** 中，选择普通发票模板或客户帐户。</span><span class="sxs-lookup"><span data-stu-id="7398b-122">In the **Generate recurring invoices by using the default values from** section, select either free text invoice template or the customer account.</span></span> <span data-ttu-id="7398b-123">创建发票时，选择是否使用普通发票模板或客户帐户来确定语言、过帐模板、销售税组、物料销售税组、清单代码、交货国家/地区、币种、付款期限、付款方式、付款说明、付款计划、现金折扣、财务维度和转帐单的默认值。</span><span class="sxs-lookup"><span data-stu-id="7398b-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
13. <span data-ttu-id="7398b-124">在 **重复执行模式** 字段中，选择重复执行模式。</span><span class="sxs-lookup"><span data-stu-id="7398b-124">In the **Recurrence pattern** field, select the recurrence pattern.</span></span>
    + <span data-ttu-id="7398b-125">每日 – 选择此选项并在“每”字段中输入天数。</span><span class="sxs-lookup"><span data-stu-id="7398b-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="7398b-126">例如，如果您输入 15，将为此客户每 15 天生成一次发票。</span><span class="sxs-lookup"><span data-stu-id="7398b-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>
    + <span data-ttu-id="7398b-127">每周 - 选择此选项并在“每”字段中输入周数。</span><span class="sxs-lookup"><span data-stu-id="7398b-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="7398b-128">例如，如果您输入 2，将为此客户每两周生成一次发票。</span><span class="sxs-lookup"><span data-stu-id="7398b-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>
    + <span data-ttu-id="7398b-129">每月 - 选择此选项并在“每”字段中输入月数。</span><span class="sxs-lookup"><span data-stu-id="7398b-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="7398b-130">例如，如果您输入 6，将为此客户每六个月生成一次发票。</span><span class="sxs-lookup"><span data-stu-id="7398b-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>
    + <span data-ttu-id="7398b-131">每年 - 选择此选项并在“每”字段中输入年数。</span><span class="sxs-lookup"><span data-stu-id="7398b-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="7398b-132">例如，如果您输入 2，将为此客户每两年生成一次发票。</span><span class="sxs-lookup"><span data-stu-id="7398b-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
14. <span data-ttu-id="7398b-133">在 **每** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7398b-133">In the **Per** field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]