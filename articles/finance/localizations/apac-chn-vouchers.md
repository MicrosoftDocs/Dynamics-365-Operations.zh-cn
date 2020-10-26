---
title: 中国式凭证
description: 此主题描述中国式凭证，以及如何在 Microsoft Dynamics 365 Finance 中使用它们。
author: anasyash
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerVoucherType_CN, VoucherTypeWizard_CN
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 261454
ms.search.region: China (PRC)
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2f3a4ef5a7cf8e6f745f4eec7821f359e4e49dc1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987503"
---
# <a name="chinese-vouchers"></a><span data-ttu-id="8a088-103">中国式凭证</span><span class="sxs-lookup"><span data-stu-id="8a088-103">Chinese vouchers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a088-104">此主题描述中国式凭证，以及如何使用它们。</span><span class="sxs-lookup"><span data-stu-id="8a088-104">This topic describes Chinese vouchers and how they are used.</span></span>

<span data-ttu-id="8a088-105">您必须为各已过帐的日志创建凭据文档。</span><span class="sxs-lookup"><span data-stu-id="8a088-105">You must create a voucher document for every posted journal.</span></span> <span data-ttu-id="8a088-106">可以打印纸质凭证和已过帐日志。</span><span class="sxs-lookup"><span data-stu-id="8a088-106">You can print a paper voucher and a posted journal.</span></span> <span data-ttu-id="8a088-107">根据您的需求，您可以使用凭证类型设置向导设置常用的**获取**、**付款**和**转移**凭证类型，也可以在**凭证类型设置**页面中创建新的凭证类型。</span><span class="sxs-lookup"><span data-stu-id="8a088-107">Based on your requirements, you can use the Voucher type setup wizard to set up the **Get**, **Pay** and **Transfer** voucher types that are often used, or you can create new voucher types on the **Voucher type setup** page.</span></span> <span data-ttu-id="8a088-108">您可以使用预订凭证输入交易记录并将其分组为“收货凭证”、“付款凭证”或“转移凭证”。</span><span class="sxs-lookup"><span data-stu-id="8a088-108">You can use booking vouchers to enter and group transactions into the Receipt voucher, Payment voucher, or Transfer voucher.</span></span> 

<span data-ttu-id="8a088-109">从每个月第一天起的持续编号规则应分配给各凭证类型。</span><span class="sxs-lookup"><span data-stu-id="8a088-109">A continuous number sequence that begins from the first day of every monthly period should be assigned to each voucher type.</span></span> <span data-ttu-id="8a088-110">在**凭证类型设置**页面中，可以为将凭证交易记录过帐到指定会计科目定义验证规则。</span><span class="sxs-lookup"><span data-stu-id="8a088-110">On the **Voucher type setup** page, you can define validation rules for posting voucher transactions to the specified accounts.</span></span> <span data-ttu-id="8a088-111">过帐凭证期间，将根据**凭证类型设置**页面中指定的规则运行验证。</span><span class="sxs-lookup"><span data-stu-id="8a088-111">During voucher posting, validation is run, based on the rules that are specified on the **Voucher type setup** page.</span></span> <span data-ttu-id="8a088-112">如果为单据选择的凭证类型有误，将收到一条消息。</span><span class="sxs-lookup"><span data-stu-id="8a088-112">You receive a message if the voucher type that is selected for the document is incorrect.</span></span> 

<span data-ttu-id="8a088-113">例如，为**获取**凭证类型选择**信贷**类型的会计科目。</span><span class="sxs-lookup"><span data-stu-id="8a088-113">For example, you select a ledger account of the **Credit** type for the **Get** voucher type.</span></span> <span data-ttu-id="8a088-114">但是，为**获取**凭证类型定义的验证规则指定会计科目必须为借方科目。</span><span class="sxs-lookup"><span data-stu-id="8a088-114">However, the validation rule that you defined for the **Get** voucher type specifies that the ledger account must be a debit account.</span></span> <span data-ttu-id="8a088-115">在这种情况下，将收到一条消息，说明中国式凭证类型无效。</span><span class="sxs-lookup"><span data-stu-id="8a088-115">In this case, you receive a message that states that the Chinese voucher type isn't valid.</span></span> <span data-ttu-id="8a088-116">然后可以进行相应更改，并且可以再次过帐凭证。</span><span class="sxs-lookup"><span data-stu-id="8a088-116">You can then make the appropriate changes and post the voucher again.</span></span> 

<span data-ttu-id="8a088-117">有关详细信息，请参阅[设置中国式凭证](./tasks/set-up-chinese-vouchers.md)。</span><span class="sxs-lookup"><span data-stu-id="8a088-117">For more information, see [Set up Chinese vouchers](./tasks/set-up-chinese-vouchers.md).</span></span>

## <a name="voucher-creation-methods"></a><span data-ttu-id="8a088-118">凭证创建方法</span><span class="sxs-lookup"><span data-stu-id="8a088-118">Voucher creation methods</span></span>
<span data-ttu-id="8a088-119">您可以在**总帐**页面中使用**简单**或**高级**方法创建凭证交易记录。</span><span class="sxs-lookup"><span data-stu-id="8a088-119">You can create voucher transactions on the **General journal** page by using the **Simple** or **Advanced** method.</span></span> <span data-ttu-id="8a088-120">如果通过使用**简单**方法创建简单凭证类型的日记帐凭证，在所有日记帐行中选择的凭证类型应相同。</span><span class="sxs-lookup"><span data-stu-id="8a088-120">If you create journal vouchers of a single voucher type by using the **Simple** method, the voucher type that is selected on all the journal lines should be the same.</span></span> <span data-ttu-id="8a088-121">**高级**方式可让您创建其他凭证类型的多个日志行。</span><span class="sxs-lookup"><span data-stu-id="8a088-121">The **Advanced** method lets you create multiple journal lines of different voucher types.</span></span> 

## <a name="check-for-continuity-in-voucher-numbers"></a><span data-ttu-id="8a088-122">检查凭证号的连续性</span><span class="sxs-lookup"><span data-stu-id="8a088-122">Check for continuity in voucher numbers</span></span>
<span data-ttu-id="8a088-123">中国式凭证号应连续，并且会计期间内应该没有间隔。</span><span class="sxs-lookup"><span data-stu-id="8a088-123">The Chinese voucher number should be sequential, and there should be no gaps in the fiscal period.</span></span> <span data-ttu-id="8a088-124">可以运行批处理确定中国式凭证号中是否有间隔。</span><span class="sxs-lookup"><span data-stu-id="8a088-124">You can run a batch process to determine whether there are gaps in the Chinese voucher numbers.</span></span> <span data-ttu-id="8a088-125">批处理验证交易记录日期，然后为连续性对这些凭证进行重新编号。</span><span class="sxs-lookup"><span data-stu-id="8a088-125">The batch process verifies the transaction dates and then renumbers the vouchers for continuity.</span></span> <span data-ttu-id="8a088-126">为进行跟踪，可以生成**中国式凭证连续性检查**报告。</span><span class="sxs-lookup"><span data-stu-id="8a088-126">For tracking purposes, you can generate the **Chinese voucher continuity check** report.</span></span> <span data-ttu-id="8a088-127">此报告显示已重新编号的中国式凭证的历史记录。</span><span class="sxs-lookup"><span data-stu-id="8a088-127">This report shows the history of renumbered Chinese vouchers.</span></span> <span data-ttu-id="8a088-128">有关详细信息，请参阅[中国式凭证连续性检查](./tasks/chinese-voucher-continuity-check.md)。</span><span class="sxs-lookup"><span data-stu-id="8a088-128">For more information, see [Chinese voucher continuity check](./tasks/chinese-voucher-continuity-check.md).</span></span>

## <a name="printing-a-chinese-voucher"></a><span data-ttu-id="8a088-129">打印中国式凭证</span><span class="sxs-lookup"><span data-stu-id="8a088-129">Printing a Chinese voucher</span></span>
<span data-ttu-id="8a088-130">可以在过帐凭证之前或之后打印中国式凭证。</span><span class="sxs-lookup"><span data-stu-id="8a088-130">You can print a Chinese voucher either before or after you post the voucher.</span></span> <span data-ttu-id="8a088-131">在过帐之前或之后，已打印凭据显示诸如已重新编号的中国式凭证的历史记录的信息或税务信息。</span><span class="sxs-lookup"><span data-stu-id="8a088-131">The printed voucher shows information such as the history of renumbered Chinese vouchers, and tax information before or after the voucher was posted.</span></span> <span data-ttu-id="8a088-132">在过帐之前或之后检查已打印信息以验证信息是否相同，以及信息是否正确。</span><span class="sxs-lookup"><span data-stu-id="8a088-132">You can review the printed information to verify that the information is the same before and after posting, and that the information is correct.</span></span> <span data-ttu-id="8a088-133">例如，如果在日记帐凭证中选择销售税，最终凭证信息中将包含销售税。</span><span class="sxs-lookup"><span data-stu-id="8a088-133">For example, if you select sales tax in a journal voucher, the final voucher information includes the sales tax.</span></span> <span data-ttu-id="8a088-134">但是，此销售税可能与日记帐中的销售税不同。</span><span class="sxs-lookup"><span data-stu-id="8a088-134">However, the sales tax might differ from the sales tax that was part of the journal.</span></span> <span data-ttu-id="8a088-135">打印结果必须准确，并且必须与最后过帐之后生成的结果相同。</span><span class="sxs-lookup"><span data-stu-id="8a088-135">The printed result must be accurate, and it must be the same as the result that is generated after the final posting.</span></span> <span data-ttu-id="8a088-136">因此，您可以通过日志凭据和凭据交易记录打印信息正确的中国式凭据。</span><span class="sxs-lookup"><span data-stu-id="8a088-136">Therefore, you can print a Chinese voucher that has the correct information from both the journal voucher and the voucher transactions.</span></span> <span data-ttu-id="8a088-137">还可以在按中国式凭据和会计期间筛选信息之后，打印批处理中的中国式凭据。</span><span class="sxs-lookup"><span data-stu-id="8a088-137">You can also print Chinese vouchers in a batch after you filter the information by Chinese voucher type and fiscal period.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a088-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="8a088-138">Additional resources</span></span>
- [<span data-ttu-id="8a088-139">过帐普通日记帐的凭证</span><span class="sxs-lookup"><span data-stu-id="8a088-139">Post vouchers from the general journal</span></span>](./tasks/post-vouchers-general-journal.md)
- [<span data-ttu-id="8a088-140">从其他模块（如销售发票）过帐凭证</span><span class="sxs-lookup"><span data-stu-id="8a088-140">Post vouchers from other modules, like sales invoices</span></span>](./tasks/post-vouchers-other-modules-like-sales-invoices.md)



