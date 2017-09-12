---
title: "关闭应收帐款"
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
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2b2e827df0c679855af9624f8a2fb36cb23f359a
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---

# <a name="close-accounts-receivable"></a><span data-ttu-id="c61e8-102">关闭应收帐款</span><span class="sxs-lookup"><span data-stu-id="c61e8-102">Close Accounts receivable</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="c61e8-103">下表列出了支持应收帐款关帐业务流程的页面。</span><span class="sxs-lookup"><span data-stu-id="c61e8-103">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="c61e8-104">要打开该表中的一些页面，您必须输入信息或指定参数设置。</span><span class="sxs-lookup"><span data-stu-id="c61e8-104">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="c61e8-105">**业务流程组件任务**</span><span class="sxs-lookup"><span data-stu-id="c61e8-105">**Business process component task**</span></span>                   

<span data-ttu-id="c61e8-106">总帐中的结转期间</span><span class="sxs-lookup"><span data-stu-id="c61e8-106">Close periods in the general ledger</span></span>

| <span data-ttu-id="c61e8-107">页面名称</span><span class="sxs-lookup"><span data-stu-id="c61e8-107">Page name</span></span>                            | <span data-ttu-id="c61e8-108">用法</span><span class="sxs-lookup"><span data-stu-id="c61e8-108">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="c61e8-109">批处理作业</span><span class="sxs-lookup"><span data-stu-id="c61e8-109">Batch job</span></span>                             | <span data-ttu-id="c61e8-110">查看或创建批处理作业。</span><span class="sxs-lookup"><span data-stu-id="c61e8-110">View or create batch jobs.</span></span> <span data-ttu-id="c61e8-111">批处理作业可能无法完成，并且您想要确保所有过帐完成。</span><span class="sxs-lookup"><span data-stu-id="c61e8-111">Batch jobs might not be completed, and you want make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="c61e8-112">确认销售订单</span><span class="sxs-lookup"><span data-stu-id="c61e8-112">Confirm sales order</span></span>                   | <span data-ttu-id="c61e8-113">更新销售订单。</span><span class="sxs-lookup"><span data-stu-id="c61e8-113">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="c61e8-114">外币重估</span><span class="sxs-lookup"><span data-stu-id="c61e8-114">Foreign currency revaluation</span></span>          | <span data-ttu-id="c61e8-115">生成以外币更新未结客户交易记录的值的交易记录。</span><span class="sxs-lookup"><span data-stu-id="c61e8-115">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="c61e8-116">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="c61e8-116">Journal</span></span>                              | <span data-ttu-id="c61e8-117">过帐发票、付款和本票。</span><span class="sxs-lookup"><span data-stu-id="c61e8-117">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="c61e8-118">日记帐凭证</span><span class="sxs-lookup"><span data-stu-id="c61e8-118">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="c61e8-119">**付款日志** – 生成、处理和过帐付款。</span><span class="sxs-lookup"><span data-stu-id="c61e8-119">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="c61e8-120">**签发汇票日志** – 过帐汇票。</span><span class="sxs-lookup"><span data-stu-id="c61e8-120">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="c61e8-121">**拒付汇票日志** – 过帐拒付汇票。</span><span class="sxs-lookup"><span data-stu-id="c61e8-121">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="c61e8-122">**重新签发汇票日志** – 过帐重新签发汇票。</span><span class="sxs-lookup"><span data-stu-id="c61e8-122">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="c61e8-123">**汇款日志** – 过帐汇款。</span><span class="sxs-lookup"><span data-stu-id="c61e8-123">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="c61e8-124">**结算汇票日志** – 过帐已结算汇票</span><span class="sxs-lookup"><span data-stu-id="c61e8-124">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="c61e8-125">装箱单过帐</span><span class="sxs-lookup"><span data-stu-id="c61e8-125">Packing slip posting</span></span>                 | <span data-ttu-id="c61e8-126">更新销售订单的装箱单。</span><span class="sxs-lookup"><span data-stu-id="c61e8-126">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="c61e8-127">过帐普通发票</span><span class="sxs-lookup"><span data-stu-id="c61e8-127">Post free text invoice</span></span>               | <span data-ttu-id="c61e8-128">过帐普通发票。</span><span class="sxs-lookup"><span data-stu-id="c61e8-128">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="c61e8-129">过帐发票</span><span class="sxs-lookup"><span data-stu-id="c61e8-129">Posting invoice</span></span>                      | <span data-ttu-id="c61e8-130">过帐销售订单的发票。</span><span class="sxs-lookup"><span data-stu-id="c61e8-130">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="c61e8-131">过帐领料单</span><span class="sxs-lookup"><span data-stu-id="c61e8-131">Posting picking list</span></span>                 |<span data-ttu-id="c61e8-132">更新销售订单的领料单。</span><span class="sxs-lookup"><span data-stu-id="c61e8-132">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="c61e8-133">**业务流程组件任务**</span><span class="sxs-lookup"><span data-stu-id="c61e8-133">**Business process component task**</span></span>   

<span data-ttu-id="c61e8-134">创建和提交欧盟销售清单</span><span class="sxs-lookup"><span data-stu-id="c61e8-134">Create and submit the EU sales list</span></span>

| <span data-ttu-id="c61e8-135">页面名称</span><span class="sxs-lookup"><span data-stu-id="c61e8-135">Page name</span></span>                            | <span data-ttu-id="c61e8-136">用法</span><span class="sxs-lookup"><span data-stu-id="c61e8-136">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="c61e8-137">欧盟销售清单</span><span class="sxs-lookup"><span data-stu-id="c61e8-137">EU sales list</span></span>                         | <span data-ttu-id="c61e8-138">出于增值税 (VAT) 申报目的向税务主管机构申报的欧盟 (EU) 销售</span><span class="sxs-lookup"><span data-stu-id="c61e8-138">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |







