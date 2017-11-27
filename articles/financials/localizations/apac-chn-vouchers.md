---
title: "中国式凭证"
description: "此主题介绍中国式凭证及其在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中的使用方法。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerVoucherType_CN, VoucherTypeWizard_CN
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261454
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8c1d1328e648c6d86fda91e19f9354ce30f9adaa
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="chinese-vouchers"></a><span data-ttu-id="6ec0c-103">中国式凭证</span><span class="sxs-lookup"><span data-stu-id="6ec0c-103">Chinese vouchers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ec0c-104">此主题介绍中国式凭证及其在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中的使用方法。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-104">This topic describes Chinese vouchers and how they are used in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="6ec0c-105">您必须为各已过帐的日志创建凭据文档。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-105">You must create a voucher document for every posted journal.</span></span> <span data-ttu-id="6ec0c-106">可以打印纸质凭证和已过帐日志。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-106">You can print a paper voucher and a posted journal.</span></span> <span data-ttu-id="6ec0c-107">根据您的需求，您可以使用凭证类型设置向导设置常用的**获取**、**付款**和**转移**凭证类型，也可以在**凭证类型设置**页面中创建新的凭证类型。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-107">Based on your requirements, you can use the Voucher type setup wizard to set up the **Get**, **Pay** and **Transfer** voucher types that are often used, or you can create new voucher types on the **Voucher type setup** page.</span></span> <span data-ttu-id="6ec0c-108">您可以使用预订凭证输入交易记录并将其分组为“收货凭证”、“付款凭证”或“转移凭证”。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-108">You can use booking vouchers to enter and group transactions into the Receipt voucher, Payment voucher, or Transfer voucher.</span></span> 

<span data-ttu-id="6ec0c-109">从每个月第一天起的持续编号规则应分配给各凭证类型。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-109">A continuous number sequence that begins from the first day of every monthly period should be assigned to each voucher type.</span></span> <span data-ttu-id="6ec0c-110">仅可以定义会计科目的中国式凭证类型。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-110">You can define a Chinese voucher type for ledger accounts only.</span></span> <span data-ttu-id="6ec0c-111">您可以将凭证类型分配给特定会计科目。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-111">You can assign the voucher types to specific ledger accounts.</span></span> <span data-ttu-id="6ec0c-112">然后，在**凭证类型设置**页面中，可以为将凭证交易记录过帐到指定会计科目定义验证规则。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-112">Then, on the **Voucher type setup** page, you can define validation rules for posting voucher transactions to the specified ledger accounts.</span></span> <span data-ttu-id="6ec0c-113">过帐凭证期间，将根据**凭证类型设置**页面中指定的规则运行验证。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-113">During voucher posting, validation is run, based on the rules that are specified on the **Voucher type setup** page.</span></span> <span data-ttu-id="6ec0c-114">如果为已选会计科目选择的凭证类型有误，将收到一条消息。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-114">You receive a message if the voucher type that is selected for the selected ledger account is incorrect.</span></span> 

<span data-ttu-id="6ec0c-115">例如，为**获取**凭证类型选择**信贷**类型的会计科目。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-115">For example, you select a ledger account of the **Credit** type for the **Get** voucher type.</span></span> <span data-ttu-id="6ec0c-116">但是，为**获取**凭证类型定义的验证规则指定会计科目必须为借方科目。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-116">However, the validation rule that you defined for the **Get** voucher type specifies that the ledger account must be a debit account.</span></span> <span data-ttu-id="6ec0c-117">在这种情况下，将收到一条消息，说明中国式凭证类型无效。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-117">In this case, you receive a message that states that the Chinese voucher type isn't valid.</span></span> <span data-ttu-id="6ec0c-118">然后可以进行相应更改，并且可以再次过帐凭证。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-118">You can then make the appropriate changes and post the voucher again.</span></span> 

<span data-ttu-id="6ec0c-119">有关详细信息，请参阅[设置中国式凭证](./tasks/set-up-chinese-vouchers.md)。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-119">For more information, see [Set up Chinese vouchers](./tasks/set-up-chinese-vouchers.md).</span></span>

## <a name="voucher-creation-methods"></a><span data-ttu-id="6ec0c-120">凭证创建方法</span><span class="sxs-lookup"><span data-stu-id="6ec0c-120">Voucher creation methods</span></span>
<span data-ttu-id="6ec0c-121">您可以在**总帐**页面中使用**简单**或**高级**方法创建凭证交易记录。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-121">You can create voucher transactions on the **General journal** page by using the **Simple** or **Advanced** method.</span></span> <span data-ttu-id="6ec0c-122">如果通过使用**简单**方法创建简单凭证类型的日记帐凭证，在所有日记帐行中选择的凭证类型应相同。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-122">If you create journal vouchers of a single voucher type by using the **Simple** method, the voucher type that is selected on all the journal lines should be the same.</span></span> <span data-ttu-id="6ec0c-123">**高级**方式可让您创建其他凭证类型的多个日志行。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-123">The **Advanced** method lets you create multiple journal lines of different voucher types.</span></span> 

## <a name="check-for-continuity-in-voucher-numbers"></a><span data-ttu-id="6ec0c-124">检查凭证号的连续性</span><span class="sxs-lookup"><span data-stu-id="6ec0c-124">Check for continuity in voucher numbers</span></span>
<span data-ttu-id="6ec0c-125">中国式凭证号应连续，并且会计期间内应该没有间隔。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-125">The Chinese voucher number should be sequential, and there should be no gaps in the fiscal period.</span></span> <span data-ttu-id="6ec0c-126">可以运行批处理确定中国式凭证号中是否有间隔。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-126">You can run a batch process to determine whether there are gaps in the Chinese voucher numbers.</span></span> <span data-ttu-id="6ec0c-127">批处理验证交易记录日期，然后为连续性对这些凭证进行重新编号。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-127">The batch process verifies the transaction dates and then renumbers the vouchers for continuity.</span></span> <span data-ttu-id="6ec0c-128">为进行跟踪，可以生成**中国式凭证连续性检查**报告。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-128">For tracking purposes, you can generate the **Chinese voucher continuity check** report.</span></span> <span data-ttu-id="6ec0c-129">此报告显示已重新编号的中国式凭证的历史记录。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-129">This report shows the history of renumbered Chinese vouchers.</span></span> <span data-ttu-id="6ec0c-130">有关详细信息，请参阅[验证凭证的连续性](./tasks/chinese-voucher-continuity-check.md)。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-130">For more information, see [Verify the continuity of vouchers](./tasks/chinese-voucher-continuity-check.md).</span></span>

## <a name="printing-a-chinese-voucher"></a><span data-ttu-id="6ec0c-131">打印中国式凭证</span><span class="sxs-lookup"><span data-stu-id="6ec0c-131">Printing a Chinese voucher</span></span>
<span data-ttu-id="6ec0c-132">可以在过帐凭证之前或之后打印中国式凭证。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-132">You can print a Chinese voucher either before or after you post the voucher.</span></span> <span data-ttu-id="6ec0c-133">在过帐之前或之后，已打印凭据显示诸如已重新编号的中国式凭证的历史记录的信息或税务信息。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-133">The printed voucher shows information such as the history of renumbered Chinese vouchers, and tax information before or after the voucher was posted.</span></span> <span data-ttu-id="6ec0c-134">在过帐之前或之后检查已打印信息以验证信息是否相同，以及信息是否正确。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-134">You can review the printed information to verify that the information is the same before and after posting, and that the information is correct.</span></span> <span data-ttu-id="6ec0c-135">例如，如果在日记帐凭证中选择销售税，最终凭证信息中将包含销售税。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-135">For example, if you select sales tax in a journal voucher, the final voucher information includes the sales tax.</span></span> <span data-ttu-id="6ec0c-136">但是，此销售税可能与日记帐中的销售税不同。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-136">However, the sales tax might differ from the sales tax that was part of the journal.</span></span> <span data-ttu-id="6ec0c-137">打印结果必须准确，并且必须与最后过帐之后生成的结果相同。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-137">The printed result must be accurate, and it must be the same as the result that is generated after the final posting.</span></span> <span data-ttu-id="6ec0c-138">因此，您可以通过日志凭据和凭据交易记录打印信息正确的中国式凭据。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-138">Therefore, you can print a Chinese voucher that has the correct information from both the journal voucher and the voucher transactions.</span></span> <span data-ttu-id="6ec0c-139">还可以在按中国式凭据和会计期间筛选信息之后，打印批处理中的中国式凭据。</span><span class="sxs-lookup"><span data-stu-id="6ec0c-139">You can also print Chinese vouchers in a batch after you filter the information by Chinese voucher type and fiscal period.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ec0c-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="6ec0c-140">Additional resources</span></span>
- [<span data-ttu-id="6ec0c-141">过帐普通日记帐的凭证</span><span class="sxs-lookup"><span data-stu-id="6ec0c-141">Post vouchers from the general journal</span></span>](./tasks/post-vouchers-general-journal.md)
- [<span data-ttu-id="6ec0c-142">过帐其他模块的凭证</span><span class="sxs-lookup"><span data-stu-id="6ec0c-142">Post vouchers from other modules</span></span>](./tasks/post-vouchers-other-modules-like-sales-invoices.md)




