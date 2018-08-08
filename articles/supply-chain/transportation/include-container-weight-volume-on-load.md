---
title: "包括容器重量和负荷的体积"
description: "此主题描述如何设置和应用要包括容器重量和负荷的体积的功能。"
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: adbaa379889d373d597b2f6882b78f82bd71ae57
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="eb26b-103">包括容器重量和负荷的体积</span><span class="sxs-lookup"><span data-stu-id="eb26b-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb26b-104">用于包括容器重量和负荷的体积的功能明确表示容器的总重量和体积以及进入负荷的物料。</span><span class="sxs-lookup"><span data-stu-id="eb26b-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="eb26b-105">负荷包含单个或多个装运，这些装运包含属于单个或多个销售订单的独特物料。</span><span class="sxs-lookup"><span data-stu-id="eb26b-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="eb26b-106">这些物料存储在容器中，且容器加载在负荷上。</span><span class="sxs-lookup"><span data-stu-id="eb26b-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="eb26b-107">位于容器外的物料也可以成为负荷的一部分。</span><span class="sxs-lookup"><span data-stu-id="eb26b-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="eb26b-108">基于这些条件，系统通过考虑容器和物料的重量和体积来计算负荷上的重量和体积的值。</span><span class="sxs-lookup"><span data-stu-id="eb26b-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="eb26b-109">如果计算的值不准确，您可以通过输入负荷上的重量和体积的实际值来进行调整。</span><span class="sxs-lookup"><span data-stu-id="eb26b-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="eb26b-110">重量和体积的值在运输管理流程中使用。</span><span class="sxs-lookup"><span data-stu-id="eb26b-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="eb26b-111">例如，这些值在费率路线工作台中使用，帮助定义负荷的费率和路线，且用于运输支付方式和驾驶员签入。</span><span class="sxs-lookup"><span data-stu-id="eb26b-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="eb26b-112">适用情况</span><span class="sxs-lookup"><span data-stu-id="eb26b-112">Where it applies</span></span>

<span data-ttu-id="eb26b-113">用于包括容器重量和负荷的体积的功能在运输管理流程中应用，如费率路线工作台、运输支付方式和驾驶员签入。</span><span class="sxs-lookup"><span data-stu-id="eb26b-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="eb26b-114">如何设置</span><span class="sxs-lookup"><span data-stu-id="eb26b-114">How it is set up</span></span>

<span data-ttu-id="eb26b-115">应为负荷考虑的容器的数量基于容器的重量和体积以及使用的容器的百分比进行计算。</span><span class="sxs-lookup"><span data-stu-id="eb26b-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="eb26b-116">若要设置容器的重量和体积，请单击**仓库管理** \> **设置** \> **容器** \> **容器类型**。</span><span class="sxs-lookup"><span data-stu-id="eb26b-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="eb26b-117">若要设置容器利用率百分比，请单击**仓库管理** \> **设置** \> **容器** \> **容器组**，然后在**容器利用率百分比**字段中输入一个值。</span><span class="sxs-lookup"><span data-stu-id="eb26b-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>

