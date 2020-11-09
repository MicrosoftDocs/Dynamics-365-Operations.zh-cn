---
title: 对货运进行手动对帐
description: 此过程显示如何手动对帐货运。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc4fc51955544df4d0156a4c83bcc5b5a0e13df3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016965"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="672a3-103">对货运进行手动对账</span><span class="sxs-lookup"><span data-stu-id="672a3-103">Reconcile freight manually</span></span>

<span data-ttu-id="672a3-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="672a3-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="672a3-105">此过程显示如何手动对帐货运。</span><span class="sxs-lookup"><span data-stu-id="672a3-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="672a3-106">这通常由运输协调员完成。</span><span class="sxs-lookup"><span data-stu-id="672a3-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="672a3-107">您可以在 USMF 演示数据公司中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="672a3-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="672a3-108">选择要对帐的负荷</span><span class="sxs-lookup"><span data-stu-id="672a3-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="672a3-109">转到“运输管理”>“计划”>“装载计划工作台”。</span><span class="sxs-lookup"><span data-stu-id="672a3-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="672a3-110">清除“隐藏已装运和已接收”复选框。</span><span class="sxs-lookup"><span data-stu-id="672a3-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="672a3-111">在列表中，选择负荷 ID 为 00006 的负荷。</span><span class="sxs-lookup"><span data-stu-id="672a3-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="672a3-112">创建承运人发票</span><span class="sxs-lookup"><span data-stu-id="672a3-112">Create a carrier invoice</span></span>
<span data-ttu-id="672a3-113">如果手动对帐货运，并且不自动接收承运人发票，可以基于货运帐单创建发票。</span><span class="sxs-lookup"><span data-stu-id="672a3-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="672a3-114">单击“相关信息”。</span><span class="sxs-lookup"><span data-stu-id="672a3-114">Click Related information.</span></span>
2. <span data-ttu-id="672a3-115">单击“货运帐单明细”。</span><span class="sxs-lookup"><span data-stu-id="672a3-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="672a3-116">单击“生成货运帐单发票”。</span><span class="sxs-lookup"><span data-stu-id="672a3-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="672a3-117">在“发票”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="672a3-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="672a3-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="672a3-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="672a3-119">对发票进行对帐</span><span class="sxs-lookup"><span data-stu-id="672a3-119">Reconcile the invoice</span></span>
<span data-ttu-id="672a3-120">对帐承运人发票和货运帐单时，逐行执行。</span><span class="sxs-lookup"><span data-stu-id="672a3-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="672a3-121">单击“匹配货运帐单和发票”。</span><span class="sxs-lookup"><span data-stu-id="672a3-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="672a3-122">展开“发票详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="672a3-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="672a3-123">展开“已取消匹配的货运帐单明细”部分。</span><span class="sxs-lookup"><span data-stu-id="672a3-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="672a3-124">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="672a3-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="672a3-125">单击“匹配”。</span><span class="sxs-lookup"><span data-stu-id="672a3-125">Click Match.</span></span>
6. <span data-ttu-id="672a3-126">展开“匹配的货运帐单明细”部分。</span><span class="sxs-lookup"><span data-stu-id="672a3-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="672a3-127">提交发票以供审核</span><span class="sxs-lookup"><span data-stu-id="672a3-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="672a3-128">单击“提交以供审核”。</span><span class="sxs-lookup"><span data-stu-id="672a3-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="672a3-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="672a3-129">Close the page.</span></span>
3. <span data-ttu-id="672a3-130">清除“隐藏已审核项”复选框。</span><span class="sxs-lookup"><span data-stu-id="672a3-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="672a3-131">单击“供应商发票日记帐”。</span><span class="sxs-lookup"><span data-stu-id="672a3-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="672a3-132">单击以访问“参考日记帐号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="672a3-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="672a3-133">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="672a3-133">Click Lines.</span></span>

