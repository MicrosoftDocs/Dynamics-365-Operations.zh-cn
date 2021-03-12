---
title: 生产输出位置
description: 本主题描述用于标识生产输出位置的层次结构。
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d8d28b9670d8752c1039684551d56b1779a10b20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001591"
---
# <a name="production-output-location"></a><span data-ttu-id="4c830-103">生产输出位置</span><span class="sxs-lookup"><span data-stu-id="4c830-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c830-104">本主题描述用于标识生产输出位置的层次结构。</span><span class="sxs-lookup"><span data-stu-id="4c830-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="4c830-105">生产输出位置是成品在生产后最先存储的位置。</span><span class="sxs-lookup"><span data-stu-id="4c830-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="4c830-106">通常，此位置靠近生产成品的生产流程。</span><span class="sxs-lookup"><span data-stu-id="4c830-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="4c830-107">生产输出位置作为物料在移动到装运区域、存储位置、用于下游生产流程的生产输入位置等之前的中间存储。</span><span class="sxs-lookup"><span data-stu-id="4c830-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="4c830-108">在生产订单或批次订单上报告成品时设置默认生产输出位置。</span><span class="sxs-lookup"><span data-stu-id="4c830-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="4c830-109">以下层次结构用于标识此输出位置：</span><span class="sxs-lookup"><span data-stu-id="4c830-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="4c830-110">使用在生产订单或批次订单标题上定义的输出位置。</span><span class="sxs-lookup"><span data-stu-id="4c830-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="4c830-111">如果在那里找不到任何位置，则使用在生产工艺路线中定义的最后一个操作使用的资源上定义的输出位置。</span><span class="sxs-lookup"><span data-stu-id="4c830-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="4c830-112">如果在那里找不到任何位置，则使用资源为生产工艺路线中定义的最后一个操作使用的资源组上定义的输出位置。</span><span class="sxs-lookup"><span data-stu-id="4c830-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="4c830-113">如果在那里找不到任何位置，则使用在为生产订单定义的仓库上定义的输出位置。</span><span class="sxs-lookup"><span data-stu-id="4c830-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="4c830-114">仅对使用高级仓库流程进行设置的产品设置默认生产输出位置。</span><span class="sxs-lookup"><span data-stu-id="4c830-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="4c830-115">在此类物料报告为已完工入库时，创建 **成品储存** 或 **联产品和副产品储存** 类型的仓库工作。</span><span class="sxs-lookup"><span data-stu-id="4c830-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="4c830-116">此类型工作使用生产输出位置作为领料库位。</span><span class="sxs-lookup"><span data-stu-id="4c830-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="4c830-117">储存库位由库位指令确定。</span><span class="sxs-lookup"><span data-stu-id="4c830-117">The put-away location is determined by the location directives.</span></span>
