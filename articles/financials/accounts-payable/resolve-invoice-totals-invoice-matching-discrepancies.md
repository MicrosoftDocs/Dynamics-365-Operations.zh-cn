---
title: "解决发票合计匹配期间出现的差异"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="f89c2-102">解决发票合计匹配期间出现的差异</span><span class="sxs-lookup"><span data-stu-id="f89c2-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="f89c2-103">发票合计匹配是发票匹配验证的类型之一。</span><span class="sxs-lookup"><span data-stu-id="f89c2-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="f89c2-104">要指定系统应执行发票合计匹配，请在**“应付账款参数”**页上的**“发票验证”**选项卡上，将**“匹配发票合计”**选项设置为**“是”**。</span><span class="sxs-lookup"><span data-stu-id="f89c2-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="f89c2-105">您可以使用发票合计匹配来帮助确保发票总金额与预期金额之间的差异不会超出可接受的差异。</span><span class="sxs-lookup"><span data-stu-id="f89c2-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="f89c2-106">在**“发票合计匹配详细信息”**页面上比较六项合计。</span><span class="sxs-lookup"><span data-stu-id="f89c2-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="f89c2-107">如果任一合计偏离预期的相应采购订单合计，则标记匹配差异。</span><span class="sxs-lookup"><span data-stu-id="f89c2-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="f89c2-108">要检查具有合计匹配差异的发票，请在**“供应商发票项”**工作区中，单击**“待定发票”**磁贴。</span><span class="sxs-lookup"><span data-stu-id="f89c2-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="f89c2-109">然后，在“操作”窗格的**“检查”**选项卡上，单击**“匹配详细信息”**。</span><span class="sxs-lookup"><span data-stu-id="f89c2-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="f89c2-110">如果检测到匹配差异，则发票金额旁边会显示警告图标。</span><span class="sxs-lookup"><span data-stu-id="f89c2-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="f89c2-111">您可以通过查看发票合计匹配详细信息来查看有关合计的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="f89c2-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="f89c2-112">在标识差异后，如果您认为发票上的信息不正确，则可能必须与供应商联系。</span><span class="sxs-lookup"><span data-stu-id="f89c2-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="f89c2-113">根据与供应商签订的最终协议，您随后可执行以下任一操作：</span><span class="sxs-lookup"><span data-stu-id="f89c2-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="f89c2-114">接受价格差异并过帐具有匹配差异的发票。</span><span class="sxs-lookup"><span data-stu-id="f89c2-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="f89c2-115">您的系统可能设置为在存在匹配差异的情况下要求先获得批准，然后才能过帐。</span><span class="sxs-lookup"><span data-stu-id="f89c2-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="f89c2-116">在此情况下，您必须批准匹配差异，并且可以选择性地输入批准注释。</span><span class="sxs-lookup"><span data-stu-id="f89c2-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="f89c2-117">然后，您可以选择过帐发票。</span><span class="sxs-lookup"><span data-stu-id="f89c2-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="f89c2-118">将发票金额修正为预期金额并过帐该发票。</span><span class="sxs-lookup"><span data-stu-id="f89c2-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="f89c2-119">从供应商处请求完全信用和新的纠正后的发票。</span><span class="sxs-lookup"><span data-stu-id="f89c2-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="f89c2-120">有关详细信息，请参阅[研究或解析异常](tasks/research-resolve-exceptions.md)。</span><span class="sxs-lookup"><span data-stu-id="f89c2-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



