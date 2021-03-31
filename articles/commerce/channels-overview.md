---
title: 渠道概览
description: 此主题概述 Microsoft Dynamics 365 Commerce 中的渠道。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8ac188832bdaeba430eed7f08e91a9c2214a0e15
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219093"
---
# <a name="channels-overview"></a><span data-ttu-id="286a0-103">渠道概览</span><span class="sxs-lookup"><span data-stu-id="286a0-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="286a0-104">此主题概述 Microsoft Dynamics 365 Commerce 中的渠道。</span><span class="sxs-lookup"><span data-stu-id="286a0-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="286a0-105">它包含有关在设置每个渠道前后必须完成的任务的信息。</span><span class="sxs-lookup"><span data-stu-id="286a0-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="286a0-106">渠道类型</span><span class="sxs-lookup"><span data-stu-id="286a0-106">Types of Channels</span></span>

<span data-ttu-id="286a0-107">Dynamics 365 Commerce 支持以下三种不同的渠道类型：零售、呼叫中心和在线渠道。</span><span class="sxs-lookup"><span data-stu-id="286a0-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="286a0-108">零售渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-108">Retail channels</span></span>

<span data-ttu-id="286a0-109">零售渠道代表标准的实体商店。</span><span class="sxs-lookup"><span data-stu-id="286a0-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="286a0-110">每个商店可以有自己的销售点 (POS) 收银机、收入帐户和支出帐户以及职员。</span><span class="sxs-lookup"><span data-stu-id="286a0-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="286a0-111">呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-111">Call center channels</span></span>

<span data-ttu-id="286a0-112">呼叫中心渠道代表呼叫中心订单和客户管理。</span><span class="sxs-lookup"><span data-stu-id="286a0-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="286a0-113">在线渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-113">Online channels</span></span>

<span data-ttu-id="286a0-114">在线渠道代表在线电子商务店面。</span><span class="sxs-lookup"><span data-stu-id="286a0-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="286a0-115">创建在线渠道后，必须使用 Microsoft Dynamics 365 Commerce 站点构建器工具或其他第三方电子商务解决方案创建站点。</span><span class="sxs-lookup"><span data-stu-id="286a0-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="286a0-116">渠道设置基础知识</span><span class="sxs-lookup"><span data-stu-id="286a0-116">Channel setup basics</span></span>

<span data-ttu-id="286a0-117">渠道设置是在 Commerce 工具中执行的。</span><span class="sxs-lookup"><span data-stu-id="286a0-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="286a0-118">每个渠道可以有自己的付款方式、价格组、产品层次结构、分类和产品集。</span><span class="sxs-lookup"><span data-stu-id="286a0-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="286a0-119">在创建渠道后，分配您希望其提供和销售的产品。</span><span class="sxs-lookup"><span data-stu-id="286a0-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="286a0-120">每种渠道类型都有可能需要配置的一组独特功能。</span><span class="sxs-lookup"><span data-stu-id="286a0-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="286a0-121">例如，零售渠道需要分配的员工、收银机和客户。</span><span class="sxs-lookup"><span data-stu-id="286a0-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="286a0-122">创建新渠道后，需要将其分配给组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="286a0-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="286a0-123">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="286a0-123">Channel setup prerequisites</span></span>

<span data-ttu-id="286a0-124">在设置渠道之前，必须根据渠道类型完成一些先决条件任务。</span><span class="sxs-lookup"><span data-stu-id="286a0-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="286a0-125">有关更多信息，请参见[渠道设置先决条件](channels-prerequisites.md)。</span><span class="sxs-lookup"><span data-stu-id="286a0-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="286a0-126">设置渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-126">Set up a channel</span></span>

<span data-ttu-id="286a0-127">完成先决条件任务后，请使用以下链接以获取详细设置说明。</span><span class="sxs-lookup"><span data-stu-id="286a0-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="286a0-128">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="286a0-129">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="286a0-130">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="286a0-131">其他资源</span><span class="sxs-lookup"><span data-stu-id="286a0-131">Additional resources</span></span>

[<span data-ttu-id="286a0-132">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="286a0-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="286a0-133">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="286a0-134">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="286a0-135">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="286a0-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="286a0-136">设置组织层次结构</span><span class="sxs-lookup"><span data-stu-id="286a0-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]