---
title: 收货仓库工序疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理收货仓库工序时可能遇到的常见问题。
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
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250874"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="f739f-103">收货仓库工序疑难解答</span><span class="sxs-lookup"><span data-stu-id="f739f-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f739f-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理收货仓库工序时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="f739f-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="f739f-105">我收到以下错误消息：“质检订单 %1 已生成。</span><span class="sxs-lookup"><span data-stu-id="f739f-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="f739f-106">找不到群集配置文件，请检查您的配置。”</span><span class="sxs-lookup"><span data-stu-id="f739f-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f739f-107">问题描述</span><span class="sxs-lookup"><span data-stu-id="f739f-107">Issue description</span></span>

<span data-ttu-id="f739f-108">此错误消息与打开质量管理 (QMS) 的接收流程有关。</span><span class="sxs-lookup"><span data-stu-id="f739f-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="f739f-109">根据您环境中的配置，有关生成错误消息的交易的其他详细信息可能有助于解决此问题。</span><span class="sxs-lookup"><span data-stu-id="f739f-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f739f-110">解决问题</span><span class="sxs-lookup"><span data-stu-id="f739f-110">Issue resolution</span></span>

<span data-ttu-id="f739f-111">首先，请查看[群集领料](set-up-cluster-picking.md)设置，确保正确配置了群集配置文件。</span><span class="sxs-lookup"><span data-stu-id="f739f-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="f739f-112">除非设置了群集配置文件，否则您不能使用移动设备菜单项进行群集领料。</span><span class="sxs-lookup"><span data-stu-id="f739f-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="f739f-113">根据您的环境，您可能还必须查看其他相关配置。</span><span class="sxs-lookup"><span data-stu-id="f739f-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="f739f-114">混合牌照接收不使用“贷记”以外的任何处置代码。</span><span class="sxs-lookup"><span data-stu-id="f739f-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f739f-115">问题描述</span><span class="sxs-lookup"><span data-stu-id="f739f-115">Issue description</span></span>

<span data-ttu-id="f739f-116">当处置代码的 **操作** 字段设置为 *贷记* 或 *报废* 时，您只能使用[混合牌照接收](mixed-license-plate-receiving.md)菜单项来处理退回物料。</span><span class="sxs-lookup"><span data-stu-id="f739f-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f739f-117">解决问题</span><span class="sxs-lookup"><span data-stu-id="f739f-117">Issue resolution</span></span>

<span data-ttu-id="f739f-118">Microsoft 已评估此问题，确定了这是一项功能限制。</span><span class="sxs-lookup"><span data-stu-id="f739f-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="f739f-119">当前，混合牌照接收仅支持将 **操作** 字段设置为 *贷记* 或 *报废* 的[处置代码](../service-management/set-up-disposition-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="f739f-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="f739f-120">当我运行“更新产品收货”定期任务时，未确认的采购订单会被确认。</span><span class="sxs-lookup"><span data-stu-id="f739f-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f739f-121">问题描述</span><span class="sxs-lookup"><span data-stu-id="f739f-121">Issue description</span></span>

<span data-ttu-id="f739f-122">在运行 *更新产品收货* 定期任务后，系统会自动确认库存交易状态为 *已登记* 的未确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="f739f-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f739f-123">解决问题</span><span class="sxs-lookup"><span data-stu-id="f739f-123">Issue resolution</span></span>

<span data-ttu-id="f739f-124">新的入站负荷处理功能 *负荷数量超收* 解决了这个问题。</span><span class="sxs-lookup"><span data-stu-id="f739f-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="f739f-125">要启用此功能，请转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，启用以下功能（按照它们列出的顺序）：</span><span class="sxs-lookup"><span data-stu-id="f739f-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="f739f-126">将采购订单库存交易记录与负荷相关联</span><span class="sxs-lookup"><span data-stu-id="f739f-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="f739f-127">负荷数量超收</span><span class="sxs-lookup"><span data-stu-id="f739f-127">Over receipt of load quantities</span></span>

<span data-ttu-id="f739f-128">有关详细信息，请参阅[针对采购订单过帐登记的产品数量](inbound-load-handling.md#post-registered-quantities)。</span><span class="sxs-lookup"><span data-stu-id="f739f-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]