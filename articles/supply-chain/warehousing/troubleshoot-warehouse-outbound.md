---
title: 出货仓库工序疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理出货仓库工序时可能遇到的常见问题。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 56bd91d8a6fe895317021d806e180df3a2db302b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645424"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="ef7bc-103">出货仓库工序疑难解答</span><span class="sxs-lookup"><span data-stu-id="ef7bc-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef7bc-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理出货仓库工序时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="ef7bc-105">我收到以下错误消息：“销售订单无法下达。”</span><span class="sxs-lookup"><span data-stu-id="ef7bc-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ef7bc-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="ef7bc-106">Issue description</span></span>

<span data-ttu-id="ef7bc-107">出现此问题有多种原因。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="ef7bc-108">例如，订单处于信用管理暂停状态，只有为与销售订单关联的所有销售行输入有效的邮政地址，才能创建装运。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="ef7bc-109">或者，存在订单保留，要将订单下达到仓库必须对它进行处理。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="ef7bc-110">此保留可能是特定于订单的，或者可能在客户帐户上。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ef7bc-111">解决问题</span><span class="sxs-lookup"><span data-stu-id="ef7bc-111">Issue resolution</span></span>

<span data-ttu-id="ef7bc-112">在销售订单和订单行上添加或更新地址，然后将订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="ef7bc-113">仅当订单有有效的交货地址（按照 **组织管理** 模块中设置的地址格式）时，才能将订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="ef7bc-114">调查订单保留，并解决问题。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="ef7bc-115">然后从订单或客户中删除保留，将订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="ef7bc-116">我收到以下消息：“负荷 1% 的装运已确认。”</span><span class="sxs-lookup"><span data-stu-id="ef7bc-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="ef7bc-117">但是，没有过帐行。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ef7bc-118">问题描述</span><span class="sxs-lookup"><span data-stu-id="ef7bc-118">Issue description</span></span>

<span data-ttu-id="ef7bc-119">负荷上的装运已确认，但没有进一步过帐。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ef7bc-120">解决问题</span><span class="sxs-lookup"><span data-stu-id="ef7bc-120">Issue resolution</span></span>

<span data-ttu-id="ef7bc-121">装运确认不会影响过帐。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="ef7bc-122">它只是更新装运和负荷状态。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="ef7bc-123">过帐必须在单独的流程中进行。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="ef7bc-124">我收到以下错误消息：“直接交货无法为仓库 1% 执行处理，因为它启用了仓库管理。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="ef7bc-125">请指定另一个未启用仓库管理的仓库。”</span><span class="sxs-lookup"><span data-stu-id="ef7bc-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ef7bc-126">问题描述</span><span class="sxs-lookup"><span data-stu-id="ef7bc-126">Issue description</span></span>

<span data-ttu-id="ef7bc-127">物料被添加到启用了仓库管理 (WMS) 的仓库的直接交货的销售行。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="ef7bc-128">当销售行更新时，您会收到此错误消息。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="ef7bc-129">解决问题</span><span class="sxs-lookup"><span data-stu-id="ef7bc-129">Issue resolution</span></span>

<span data-ttu-id="ef7bc-130">Microsoft 已评估此问题，确定了这是一项功能限制。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="ef7bc-131">当前，WMS 不支持直接交货。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="ef7bc-132">因此，要使用直接交货，必须选择非 WMS 物料和仓库。</span><span class="sxs-lookup"><span data-stu-id="ef7bc-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
