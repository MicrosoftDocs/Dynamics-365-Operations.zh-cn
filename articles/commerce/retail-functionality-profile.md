---
title: 创建零售功能配置文件
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建零售功能配置文件。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002835"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="c4da3-103">创建零售功能配置文件</span><span class="sxs-lookup"><span data-stu-id="c4da3-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c4da3-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建零售功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4da3-104">This topic describes how to create a retail functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c4da3-105">概览</span><span class="sxs-lookup"><span data-stu-id="c4da3-105">Overview</span></span>

<span data-ttu-id="c4da3-106">零售功能配置文件提供了用于在线渠道的各种设置。</span><span class="sxs-lookup"><span data-stu-id="c4da3-106">The retail functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="c4da3-107">每个零售渠道必须指定一个零售功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="c4da3-107">Each retail channel must specify a retail functionality profile.</span></span>

## <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="c4da3-108">创建零售功能配置文件</span><span class="sxs-lookup"><span data-stu-id="c4da3-108">Create a retail functionality profile</span></span>

<span data-ttu-id="c4da3-109">若要创建零售功能配置文件，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c4da3-109">To create a retail functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="c4da3-110">在导航窗格中，转到**模块 \> 渠道设置 \> POS 配置文件 \> 功能配置文件**。</span><span class="sxs-lookup"><span data-stu-id="c4da3-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="c4da3-111">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="c4da3-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c4da3-112">在**配置文件**字段中，输入配置文件的 ID（下面示例图像中的“FN006”）。</span><span class="sxs-lookup"><span data-stu-id="c4da3-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="c4da3-113">在**描述**字段中，输入一个值（下面示例图像中的“冒险工作配置文件”）。</span><span class="sxs-lookup"><span data-stu-id="c4da3-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="c4da3-114">在**常规**部分中，为 **ISO** 区域设置选择国家/地区。</span><span class="sxs-lookup"><span data-stu-id="c4da3-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="c4da3-115">在**常规**部分中，根据需要修改其他设置。</span><span class="sxs-lookup"><span data-stu-id="c4da3-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="c4da3-116">在**常规**部分中，为电子邮件收据选择**收据配置文件 ID**。</span><span class="sxs-lookup"><span data-stu-id="c4da3-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="c4da3-117">在**功能**部分中，根据需要修改设置。</span><span class="sxs-lookup"><span data-stu-id="c4da3-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="c4da3-118">在**金额**部分中，根据需要修改设置。</span><span class="sxs-lookup"><span data-stu-id="c4da3-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="c4da3-119">在**信息代码**部分中，根据需要修改设置。</span><span class="sxs-lookup"><span data-stu-id="c4da3-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="c4da3-120">在**收据编号**部分中，根据需要修改设置。</span><span class="sxs-lookup"><span data-stu-id="c4da3-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="c4da3-121">下图显示了一个零售功能配置文件示例。</span><span class="sxs-lookup"><span data-stu-id="c4da3-121">The following image shows an example retail functionality profile.</span></span>
  
![零售功能配置文件示例](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="c4da3-123">其他资源</span><span class="sxs-lookup"><span data-stu-id="c4da3-123">Additional resources</span></span>

[<span data-ttu-id="c4da3-124">信息代码和信息代码组</span><span class="sxs-lookup"><span data-stu-id="c4da3-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="c4da3-125">新建通讯簿</span><span class="sxs-lookup"><span data-stu-id="c4da3-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="c4da3-126">屏幕布局概览</span><span class="sxs-lookup"><span data-stu-id="c4da3-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="c4da3-127">配置并安装 Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="c4da3-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
