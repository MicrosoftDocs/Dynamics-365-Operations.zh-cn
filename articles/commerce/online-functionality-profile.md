---
title: 创建在线功能配置文件
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建在线功能配置文件。
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
ms.openlocfilehash: cb9d78a945132c913dcb8a5d5b41eaacd1a6db3b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477724"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="68482-103">创建在线功能配置文件</span><span class="sxs-lookup"><span data-stu-id="68482-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="68482-104">本主题概述为 Microsoft Dynamics 365 Commerce 设置在线功能配置文件的过程。</span><span class="sxs-lookup"><span data-stu-id="68482-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="68482-105">在线功能配置文件提供了用于在线渠道的各种设置。</span><span class="sxs-lookup"><span data-stu-id="68482-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="68482-106">每个在线渠道必须指定一个在线功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="68482-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="68482-107">创建在线功能配置文件</span><span class="sxs-lookup"><span data-stu-id="68482-107">Create an online functionality profile</span></span>

<span data-ttu-id="68482-108">以下过程说明了如何从 Commerce Headquarters 应用创建在线功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="68482-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="68482-109">在导航窗格中，转到 **模块 \> 渠道设置 \> 在线商店设置 \> 功能配置文件**。</span><span class="sxs-lookup"><span data-stu-id="68482-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="68482-110">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="68482-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="68482-111">在 **配置文件** 字段中，为配置文件输入 ID。</span><span class="sxs-lookup"><span data-stu-id="68482-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="68482-112">在 **描述** 字段中，输入一个值（下面示例图像中的“冒险工作配置文件”）。</span><span class="sxs-lookup"><span data-stu-id="68482-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="68482-113">在 **功能** 部分，根据需要修改 **购物车**、**零售客户** 或 **结帐** 设置。</span><span class="sxs-lookup"><span data-stu-id="68482-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="68482-114">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="68482-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="68482-115">下图显示了一个在线功能配置文件示例。</span><span class="sxs-lookup"><span data-stu-id="68482-115">The following image shows an example online functionality profile.</span></span>
  
![在线功能配置文件示例](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="68482-117">函数</span><span class="sxs-lookup"><span data-stu-id="68482-117">Functions</span></span>

- <span data-ttu-id="68482-118">**聚合产品**：启用后，此功能允许购物车在多次添加同一商品时更新数量。</span><span class="sxs-lookup"><span data-stu-id="68482-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="68482-119">**允许不付款结帐**：启用后，此功能可以处理添加到购物车中的商品价格为 0.00 美元的情况。</span><span class="sxs-lookup"><span data-stu-id="68482-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="68482-120">**在异步模式下创建客户**：这是适用于第三方电子商务渠道的旧设置，不适用于 Dynamics 365 电子商务站点。</span><span class="sxs-lookup"><span data-stu-id="68482-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68482-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="68482-121">Additional resources</span></span>

[<span data-ttu-id="68482-122">渠道概览</span><span class="sxs-lookup"><span data-stu-id="68482-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="68482-123">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="68482-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="68482-124">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="68482-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="68482-125">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="68482-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="68482-126">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="68482-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
