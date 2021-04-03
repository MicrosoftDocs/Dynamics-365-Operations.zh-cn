---
title: 部分下达和部分装运疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理部分下达和部分装运时可能遇到的常见问题。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c9246376505e163a4a41bf141a98deed0fd511f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263220"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="6eb24-103">部分下达和部分装运疑难解答</span><span class="sxs-lookup"><span data-stu-id="6eb24-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6eb24-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理部分下达和部分装运时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="6eb24-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="6eb24-105">即使销售订单开票之后，销售订单的下达状态仍是“部分下达”。</span><span class="sxs-lookup"><span data-stu-id="6eb24-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6eb24-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="6eb24-106">Issue description</span></span>

<span data-ttu-id="6eb24-107">销售订单是一个交货订单，但其中的一个或多个商品有不同的交货方式。</span><span class="sxs-lookup"><span data-stu-id="6eb24-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="6eb24-108">订单开票后，其下达状态仍为 *部分下达*。</span><span class="sxs-lookup"><span data-stu-id="6eb24-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="6eb24-109">例如，一个销售订单有两个商品：一个要交货，一个要提货。</span><span class="sxs-lookup"><span data-stu-id="6eb24-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="6eb24-110">交货和提货都已完成。</span><span class="sxs-lookup"><span data-stu-id="6eb24-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="6eb24-111">因此，这两行都已开票。</span><span class="sxs-lookup"><span data-stu-id="6eb24-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="6eb24-112">但是，下达状态仍显示为 *部分下达*，这有一定误导性。</span><span class="sxs-lookup"><span data-stu-id="6eb24-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6eb24-113">解决问题</span><span class="sxs-lookup"><span data-stu-id="6eb24-113">Issue resolution</span></span>

<span data-ttu-id="6eb24-114">下达状态仅适用于物料已启用仓库管理的订单行。</span><span class="sxs-lookup"><span data-stu-id="6eb24-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="6eb24-115">因此，在这种情况下，下达状态仍为 *部分下达*。</span><span class="sxs-lookup"><span data-stu-id="6eb24-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="6eb24-116">Microsoft 已评估此问题，确定了这是一项功能限制。</span><span class="sxs-lookup"><span data-stu-id="6eb24-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="6eb24-117">可以作为装箱单和开发票流程的一部分添加扩展，来更新下达状态。</span><span class="sxs-lookup"><span data-stu-id="6eb24-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]