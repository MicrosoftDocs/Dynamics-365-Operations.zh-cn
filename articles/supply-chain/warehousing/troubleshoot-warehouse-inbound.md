---
title: 收货仓库工序疑难解答
description: 此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理收货仓库工序时可能遇到的常见问题。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920979"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="30689-103">收货仓库工序疑难解答</span><span class="sxs-lookup"><span data-stu-id="30689-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30689-104">此主题介绍如何解决在 Microsoft Dynamics 365 Supply Chain Management 中处理收货仓库工序时可能遇到的常见问题。</span><span class="sxs-lookup"><span data-stu-id="30689-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="30689-105">我收到以下错误消息：“质检订单 %1 已生成。</span><span class="sxs-lookup"><span data-stu-id="30689-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="30689-106">找不到群集配置文件，请检查您的配置。”</span><span class="sxs-lookup"><span data-stu-id="30689-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="30689-107">问题描述</span><span class="sxs-lookup"><span data-stu-id="30689-107">Issue description</span></span>

<span data-ttu-id="30689-108">此错误消息与打开质量管理 (QMS) 的接收流程有关。</span><span class="sxs-lookup"><span data-stu-id="30689-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="30689-109">根据您环境中的配置，有关生成错误消息的交易的其他详细信息可能有助于解决此问题。</span><span class="sxs-lookup"><span data-stu-id="30689-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="30689-110">解决问题</span><span class="sxs-lookup"><span data-stu-id="30689-110">Issue resolution</span></span>

<span data-ttu-id="30689-111">首先，请查看[群集领料](set-up-cluster-picking.md)设置，确保正确配置了群集配置文件。</span><span class="sxs-lookup"><span data-stu-id="30689-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="30689-112">除非设置了群集配置文件，否则您不能使用移动设备菜单项进行群集领料。</span><span class="sxs-lookup"><span data-stu-id="30689-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="30689-113">根据您的环境，您可能还必须查看其他相关配置。</span><span class="sxs-lookup"><span data-stu-id="30689-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="30689-114">混合牌照接收不使用“贷记”以外的任何处置代码。</span><span class="sxs-lookup"><span data-stu-id="30689-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="30689-115">问题描述</span><span class="sxs-lookup"><span data-stu-id="30689-115">Issue description</span></span>

<span data-ttu-id="30689-116">当处置代码的 **操作** 字段设置为 *贷记* 或 *报废* 时，您只能使用[混合牌照接收](mixed-license-plate-receiving.md)菜单项来处理退回物料。</span><span class="sxs-lookup"><span data-stu-id="30689-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="30689-117">解决问题</span><span class="sxs-lookup"><span data-stu-id="30689-117">Issue resolution</span></span>

<span data-ttu-id="30689-118">Microsoft 已评估此问题，确定了这是一项功能限制。</span><span class="sxs-lookup"><span data-stu-id="30689-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="30689-119">当前，混合牌照接收仅支持将 **操作** 字段设置为 *贷记* 或 *报废* 的[处置代码](../service-management/set-up-disposition-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="30689-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="30689-120">当我运行“更新产品收货”定期任务时，未确认的采购订单会被确认。</span><span class="sxs-lookup"><span data-stu-id="30689-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="30689-121">问题描述</span><span class="sxs-lookup"><span data-stu-id="30689-121">Issue description</span></span>

<span data-ttu-id="30689-122">在运行 *更新产品收货* 定期任务后，系统会自动确认库存交易状态为 *已登记* 的未确认采购订单。</span><span class="sxs-lookup"><span data-stu-id="30689-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="30689-123">解决问题</span><span class="sxs-lookup"><span data-stu-id="30689-123">Issue resolution</span></span>

<span data-ttu-id="30689-124">新的入站负荷处理功能 *负荷数量超收* 解决了这个问题。</span><span class="sxs-lookup"><span data-stu-id="30689-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="30689-125">要启用此功能，转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区，启用以下功能（按照它们列出的顺序）：</span><span class="sxs-lookup"><span data-stu-id="30689-125">To turn on this feature, go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="30689-126">将采购订单库存交易记录与负荷相关联</span><span class="sxs-lookup"><span data-stu-id="30689-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="30689-127">负荷数量超收</span><span class="sxs-lookup"><span data-stu-id="30689-127">Over receipt of load quantities</span></span>

<span data-ttu-id="30689-128">有关详细信息，请参阅[针对采购订单过帐登记的产品数量](inbound-load-handling.md#post-registered-quantities)。</span><span class="sxs-lookup"><span data-stu-id="30689-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="30689-129">当登记入库订单时，我收到以下错误消息：“数量无效。”</span><span class="sxs-lookup"><span data-stu-id="30689-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="30689-130">问题描述</span><span class="sxs-lookup"><span data-stu-id="30689-130">Issue description</span></span>

<span data-ttu-id="30689-131">如果在用于登记入库订单的移动设备菜单项中，**牌照分组策略** 字段设置为 *用户定义*，您将收到一条错误消息（“数量无效”），并且无法完成登记。</span><span class="sxs-lookup"><span data-stu-id="30689-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="30689-132">问题原因</span><span class="sxs-lookup"><span data-stu-id="30689-132">Issue cause</span></span>

<span data-ttu-id="30689-133">当 *用户定义* 用作牌照分组策略时，系统将传入库存拆分为单独的牌照，如单位序列组所示。</span><span class="sxs-lookup"><span data-stu-id="30689-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="30689-134">如果批号或序列号用于跟踪将收货的物料，必须按登记的牌照指定每个批次或序列的数量。</span><span class="sxs-lookup"><span data-stu-id="30689-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="30689-135">如果为牌照指定的数量超过针对当前维度仍必须收货的数量，您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="30689-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="30689-136">解决问题</span><span class="sxs-lookup"><span data-stu-id="30689-136">Issue resolution</span></span>

<span data-ttu-id="30689-137">使用 **牌照分组策略** 字段设置为 *用户定义* 的移动设备菜单项登记物料时，系统可能会要求您确认或输入牌照编号、批号或序列号。</span><span class="sxs-lookup"><span data-stu-id="30689-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="30689-138">在牌照确认页面上，系统将显示为当前牌照分配的数量。</span><span class="sxs-lookup"><span data-stu-id="30689-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="30689-139">在批次或序列确认页面上，系统将显示在当前牌照上仍必须收货的数量。</span><span class="sxs-lookup"><span data-stu-id="30689-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="30689-140">它还将包含一个字段，您可以在其中输入为牌照和批号或序列号组合登记的数量。</span><span class="sxs-lookup"><span data-stu-id="30689-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="30689-141">在这种情况下，请确保为牌照登记的数量不超过仍必须收货的数量。</span><span class="sxs-lookup"><span data-stu-id="30689-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="30689-142">或者，如果在入库订单登记时生成了太多牌照，**牌照分组策略** 字段的值可以更改为 *牌照分组*，可以向物料分配新的单位序列组或者可以停用单位序列组的 **牌照分组** 选项。</span><span class="sxs-lookup"><span data-stu-id="30689-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
