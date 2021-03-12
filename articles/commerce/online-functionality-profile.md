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
ms.openlocfilehash: 1b0afeabfecb60672156692f3cd809445624020c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969968"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="4ce0c-103">创建在线功能配置文件</span><span class="sxs-lookup"><span data-stu-id="4ce0c-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4ce0c-104">本主题概述为 Microsoft Dynamics 365 Commerce 设置在线功能配置文件的过程。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4ce0c-105">概览</span><span class="sxs-lookup"><span data-stu-id="4ce0c-105">Overview</span></span>

<span data-ttu-id="4ce0c-106">在线功能配置文件提供了用于在线渠道的各种设置。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="4ce0c-107">每个在线渠道必须指定一个在线功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="4ce0c-108">创建在线功能配置文件</span><span class="sxs-lookup"><span data-stu-id="4ce0c-108">Create an online functionality profile</span></span>

<span data-ttu-id="4ce0c-109">以下过程说明了如何从 Commerce Headquarters 应用创建在线功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="4ce0c-110">在导航窗格中，转到 **模块 \> 渠道设置 \> 在线商店设置 \> 功能配置文件**。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="4ce0c-111">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4ce0c-112">在 **配置文件** 字段中，为配置文件输入 ID。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="4ce0c-113">在 **描述** 字段中，输入一个值（下面示例图像中的“冒险工作配置文件”）。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="4ce0c-114">在 **功能** 部分，根据需要修改 **购物车**、**零售客户** 或 **结帐** 设置。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="4ce0c-115">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4ce0c-116">下图显示了一个在线功能配置文件示例。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-116">The following image shows an example online functionality profile.</span></span>
  
![在线功能配置文件示例](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="4ce0c-118">函数</span><span class="sxs-lookup"><span data-stu-id="4ce0c-118">Functions</span></span>

- <span data-ttu-id="4ce0c-119">**聚合产品**：启用后，此功能允许购物车在多次添加同一商品时更新数量。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="4ce0c-120">**允许不付款结帐**：启用后，此功能可以处理添加到购物车中的商品价格为 0.00 美元的情况。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="4ce0c-121">**在异步模式下创建客户**：这是适用于第三方电子商务渠道的旧设置，不适用于 Dynamics 365 电子商务站点。</span><span class="sxs-lookup"><span data-stu-id="4ce0c-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ce0c-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="4ce0c-122">Additional resources</span></span>

[<span data-ttu-id="4ce0c-123">渠道概览</span><span class="sxs-lookup"><span data-stu-id="4ce0c-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="4ce0c-124">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="4ce0c-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="4ce0c-125">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="4ce0c-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="4ce0c-126">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="4ce0c-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="4ce0c-127">设置呼叫中心渠道</span><span class="sxs-lookup"><span data-stu-id="4ce0c-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
