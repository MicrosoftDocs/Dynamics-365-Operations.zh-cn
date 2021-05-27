---
title: 礼品卡和贷项通知单操作无缝脱机切换
description: 此主题概述特定付款类型无缝脱机切换方面的改进。
author: rubendel
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 47867447e6d16a0fb4542c17ab184068300b2c1c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019949"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="6381f-103">礼品卡和贷项通知单操作无缝脱机切换</span><span class="sxs-lookup"><span data-stu-id="6381f-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6381f-104">如果销售点 (POS) 设备断开与渠道数据库之间的连接，收银机收到有关连接断开的警告消息之后，大多数进行中的 POS 操作和交易记录可以继续进行。</span><span class="sxs-lookup"><span data-stu-id="6381f-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="6381f-105">但是，在某些情况下，交易记录有一些元素依赖于实时服务，而在 POS 脱机时不支持这些元素。</span><span class="sxs-lookup"><span data-stu-id="6381f-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="6381f-106">本文介绍某种在这些情况下可帮助降低连接断开造成的影响的功能。</span><span class="sxs-lookup"><span data-stu-id="6381f-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="6381f-107">在脱机模式下完成礼品卡交易</span><span class="sxs-lookup"><span data-stu-id="6381f-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="6381f-108">内部礼品卡依赖于实时服务，因为礼品卡的余额必须集中存储在 Microsoft Dynamics 365 Commerce Headquarters 中。</span><span class="sxs-lookup"><span data-stu-id="6381f-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="6381f-109">为了帮助避免欺诈或其他同步问题，礼品卡添加到交易记录之后将立即被锁定。</span><span class="sxs-lookup"><span data-stu-id="6381f-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="6381f-110">锁定功能可以确保同一时刻不能在多个终端使用同一个礼品卡。</span><span class="sxs-lookup"><span data-stu-id="6381f-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="6381f-111">交易完成后，将更新并解锁该礼品卡。</span><span class="sxs-lookup"><span data-stu-id="6381f-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="6381f-112">但是，如果在礼品卡已添加到交易之后 POS 断开连接，礼品卡可能变为不可用。</span><span class="sxs-lookup"><span data-stu-id="6381f-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="6381f-113">为了帮助避免发生这种情况，Dynamics 365 Commerce 采用了一个参数，用于在 POS 脱机时完成包含礼品卡行的交易。</span><span class="sxs-lookup"><span data-stu-id="6381f-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="6381f-114">如果开启此参数，将把已强制脱机的礼品卡交易记录与脱机交易记录一起保存，并在同步脱机交易记录时间这些交易记录同步到 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="6381f-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="6381f-115">同步还将解锁礼品卡，使其可在另一台终端中使用。</span><span class="sxs-lookup"><span data-stu-id="6381f-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="6381f-116">若要在切换到脱机模式后让此功能完成礼品卡交易，请转到 **Commerce 参数** 页中的 **过帐** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6381f-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="6381f-117">在该选项卡上，找到 **礼品卡** 快速选项卡，然后将 **允许在脱机模式下完成礼品卡交易** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="6381f-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![脱机礼品卡设置](../media/gift.png)

<span data-ttu-id="6381f-119">通常将缓存 Commerce 参数。</span><span class="sxs-lookup"><span data-stu-id="6381f-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="6381f-120">因此，更新此参数的设置，并且启动了分发计划以将更改同步到渠道之后，更改可能最多需要 24 小时才会生效。</span><span class="sxs-lookup"><span data-stu-id="6381f-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="6381f-121">若要让更改立即生效，请重置 Microsoft Internet 信息服务 (IIS)。</span><span class="sxs-lookup"><span data-stu-id="6381f-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="6381f-122">在脱机模式下完成贷项通知单交易</span><span class="sxs-lookup"><span data-stu-id="6381f-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="6381f-123">和内部礼品卡一样，贷项通知单集中存储在 Commerce Headquarters 中。</span><span class="sxs-lookup"><span data-stu-id="6381f-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="6381f-124">Commerce 采用了一个参数，用于在 POS 脱机时完成贷项通知单交易。</span><span class="sxs-lookup"><span data-stu-id="6381f-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="6381f-125">此参数的工作方式类似上一节中介绍的礼品卡参数。</span><span class="sxs-lookup"><span data-stu-id="6381f-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="6381f-126">开启此参数之后，将把已被强制脱机的贷项通知单交易记录和 POS 脱机期间执行的其他交易记录一起同步回渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="6381f-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="6381f-127">若要在切换到脱机模式后让此功能完成贷项通知单交易，请转到 **Commerce 参数** 页中的 **过帐** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6381f-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="6381f-128">在该选项卡上，找到 **贷项通知单** 快速选项卡，然后将 **允许在脱机模式下完成贷项通知单交易** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="6381f-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![脱机贷项通知单设置](../media/creditmemo.png)

<span data-ttu-id="6381f-130">通常将缓存 Commerce 参数。</span><span class="sxs-lookup"><span data-stu-id="6381f-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="6381f-131">因此，更新此参数的设置，并且启动了分发计划以将更改同步到渠道之后，更改可能最多需要 24 小时才会生效。</span><span class="sxs-lookup"><span data-stu-id="6381f-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="6381f-132">若要使更改立即生效，请重置 IIS。</span><span class="sxs-lookup"><span data-stu-id="6381f-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6381f-133">相关主题</span><span class="sxs-lookup"><span data-stu-id="6381f-133">Related topics</span></span>

- [<span data-ttu-id="6381f-134">脱机销售点 (POS) 功能</span><span class="sxs-lookup"><span data-stu-id="6381f-134">Offline point of sale (POS) functionality</span></span>](../pos-offline-functionality.md)
- [<span data-ttu-id="6381f-135">销售点 (POS) 联机和脱机操作</span><span class="sxs-lookup"><span data-stu-id="6381f-135">Online and offline point of sale (POS) operations</span></span>](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]