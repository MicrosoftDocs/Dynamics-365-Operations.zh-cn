---
title: 运输管理模式与方法
description: 此主题说明如何设置运输管理模式和方法。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0d41d8665252a978962bf6a2e307dce3dad64a5b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233431"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="0a521-103">运输管理模式与方法</span><span class="sxs-lookup"><span data-stu-id="0a521-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a521-104">运输管理模式表示承运人为运输交货使用的运输类型，诸如少于负荷 (LTL)、整车 (TL) 或包装。</span><span class="sxs-lookup"><span data-stu-id="0a521-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="0a521-105">运输方法表示承运人为运输交货使用的运输形式，诸如少于空运、陆运、海运或火车运输。</span><span class="sxs-lookup"><span data-stu-id="0a521-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="0a521-106">模式和运输方法在多种环境下使用。</span><span class="sxs-lookup"><span data-stu-id="0a521-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="0a521-107">路线计划中只使用模式，在设置装运承运人和承运人服务时同时使用模式和运输方法。</span><span class="sxs-lookup"><span data-stu-id="0a521-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="0a521-108">模式和运输方法之间不存在明确的关系或层次结构。</span><span class="sxs-lookup"><span data-stu-id="0a521-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="0a521-109">创建模式</span><span class="sxs-lookup"><span data-stu-id="0a521-109">Create a mode</span></span>

<span data-ttu-id="0a521-110">若要创建模式，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0a521-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="0a521-111">转到 **运输管理 \> 设置 \> 承运人 \> 方式**。</span><span class="sxs-lookup"><span data-stu-id="0a521-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="0a521-112">选择 **新建** 创建新模式。</span><span class="sxs-lookup"><span data-stu-id="0a521-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="0a521-113">为模式输入唯一的 ID 和描述名称。</span><span class="sxs-lookup"><span data-stu-id="0a521-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="0a521-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0a521-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="0a521-115">创建运输方法</span><span class="sxs-lookup"><span data-stu-id="0a521-115">Create a transportation method</span></span>

<span data-ttu-id="0a521-116">要创建运输方法，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="0a521-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="0a521-117">转到 **运输管理 \> 设置 \> 承运人 \> 运输方法**。</span><span class="sxs-lookup"><span data-stu-id="0a521-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="0a521-118">选择 **新建** 创建新的运输方法。</span><span class="sxs-lookup"><span data-stu-id="0a521-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="0a521-119">为运输方法输入唯一的 ID 和描述名称。</span><span class="sxs-lookup"><span data-stu-id="0a521-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="0a521-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0a521-120">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]