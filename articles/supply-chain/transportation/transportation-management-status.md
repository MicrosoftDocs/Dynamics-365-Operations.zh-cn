---
title: 运输管理状态
description: 此主题说明如何创建运输状态并将该状态映射到承运人状态。
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3a2b9e50dddf0f015cdd3f16d6d93fcc03d464d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807600"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="175ab-103">运输管理状态</span><span class="sxs-lookup"><span data-stu-id="175ab-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="175ab-104">为运输状态设置主代码以解释装运承运人提供的代码。</span><span class="sxs-lookup"><span data-stu-id="175ab-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="175ab-105">这样，您可以与装运承运人集成以提供状态。</span><span class="sxs-lookup"><span data-stu-id="175ab-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="175ab-106">为运输主状态代码提供的运输状态可帮助您跟踪装载、装运或集装箱状态。</span><span class="sxs-lookup"><span data-stu-id="175ab-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="175ab-107">负荷、装运或集装箱的特定运输状态只能通过数据集成来更新，不能通过用户界面手动更新。</span><span class="sxs-lookup"><span data-stu-id="175ab-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="175ab-108">创建运输状态</span><span class="sxs-lookup"><span data-stu-id="175ab-108">Create a transportation status</span></span>

<span data-ttu-id="175ab-109">要创建运输状态，请按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="175ab-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="175ab-110">转到 **运输管理 \> 设置 \> 运输状态主数据**。</span><span class="sxs-lookup"><span data-stu-id="175ab-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="175ab-111">选择 **新建** 创建运输状态主数据。</span><span class="sxs-lookup"><span data-stu-id="175ab-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="175ab-112">在 **运输状态主数据** 字段中，为运输状态输入唯一代码。</span><span class="sxs-lookup"><span data-stu-id="175ab-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="175ab-113">在 **运输类型** 字段中，选择 *装运承运人* 或 *枢纽* 作为运输类型。</span><span class="sxs-lookup"><span data-stu-id="175ab-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="175ab-114">输入名称和运输状态。</span><span class="sxs-lookup"><span data-stu-id="175ab-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="175ab-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="175ab-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="175ab-116">将运输状态映射到承运人状态</span><span class="sxs-lookup"><span data-stu-id="175ab-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="175ab-117">要将运输状态映射到承运人状态，请按照下列步骤操作：</span><span class="sxs-lookup"><span data-stu-id="175ab-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="175ab-118">转到 **运输管理 \> 设置 \> 承运人 \> 承运人运输状态**。</span><span class="sxs-lookup"><span data-stu-id="175ab-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="175ab-119">选择 **新建** 将装运承运人的代码映射到运输类型主代码。</span><span class="sxs-lookup"><span data-stu-id="175ab-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="175ab-120">为装运承运人和承运人服务选择唯一的 ID。</span><span class="sxs-lookup"><span data-stu-id="175ab-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="175ab-121">选择要映射到所选装运承运人代码的运输状态代码。</span><span class="sxs-lookup"><span data-stu-id="175ab-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="175ab-122">输入装运承运人使用的外部代码。</span><span class="sxs-lookup"><span data-stu-id="175ab-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="175ab-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="175ab-123">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]