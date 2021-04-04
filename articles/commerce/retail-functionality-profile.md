---
title: 创建零售功能配置文件
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建功能配置文件。
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
ms.openlocfilehash: 14da5fd2b409790de2269036ccb941ffa6d3311c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478300"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="2799b-103">创建零售功能配置文件</span><span class="sxs-lookup"><span data-stu-id="2799b-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2799b-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="2799b-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2799b-105">Commerce 功能配置文件提供了用于在线渠道的各种设置。</span><span class="sxs-lookup"><span data-stu-id="2799b-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="2799b-106">每个渠道必须指定一个功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="2799b-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="2799b-107">创建功能配置文件</span><span class="sxs-lookup"><span data-stu-id="2799b-107">Create a functionality profile</span></span>

<span data-ttu-id="2799b-108">若要创建功能配置文件，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2799b-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="2799b-109">在导航窗格中，转到 **模块 \> 渠道设置 \> POS 配置文件 \> 功能配置文件**。</span><span class="sxs-lookup"><span data-stu-id="2799b-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="2799b-110">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="2799b-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2799b-111">在 **配置文件** 字段中，输入配置文件的 ID（下面示例图像中的“FN006”）。</span><span class="sxs-lookup"><span data-stu-id="2799b-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="2799b-112">在 **描述** 字段中，输入一个值（下面示例图像中的“冒险工作配置文件”）。</span><span class="sxs-lookup"><span data-stu-id="2799b-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="2799b-113">在 **常规** 部分中，为 **ISO** 区域设置选择国家/地区。</span><span class="sxs-lookup"><span data-stu-id="2799b-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="2799b-114">在 **常规** 部分中，根据需要修改其他设置。</span><span class="sxs-lookup"><span data-stu-id="2799b-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="2799b-115">在 **常规** 部分中，为电子邮件收据选择 **收据配置文件 ID**。</span><span class="sxs-lookup"><span data-stu-id="2799b-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="2799b-116">在 **功能** 部分中，根据需要修改设置。</span><span class="sxs-lookup"><span data-stu-id="2799b-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="2799b-117">在 **金额** 部分中，根据需要修改设置。</span><span class="sxs-lookup"><span data-stu-id="2799b-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="2799b-118">在 **信息代码** 部分中，根据需要修改设置。</span><span class="sxs-lookup"><span data-stu-id="2799b-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="2799b-119">在 **收据编号** 部分中，根据需要修改设置。</span><span class="sxs-lookup"><span data-stu-id="2799b-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="2799b-120">下图显示了一个功能配置文件示例。</span><span class="sxs-lookup"><span data-stu-id="2799b-120">The following image shows an example functionality profile.</span></span>
  
![功能配置文件示例](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="2799b-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="2799b-122">Additional resources</span></span>

[<span data-ttu-id="2799b-123">信息代码和信息代码组</span><span class="sxs-lookup"><span data-stu-id="2799b-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="2799b-124">新建通讯簿</span><span class="sxs-lookup"><span data-stu-id="2799b-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="2799b-125">屏幕布局概览</span><span class="sxs-lookup"><span data-stu-id="2799b-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="2799b-126">配置并安装 Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="2799b-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
