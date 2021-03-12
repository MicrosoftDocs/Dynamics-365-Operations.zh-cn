---
title: 承运人组
description: 本主题介绍如何设置承运人组的数据。
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 14a2f4c7d8d053ffd7b4b5d090113e1d9c3294c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974102"
---
# <a name="carrier-groups"></a><span data-ttu-id="8bdf7-103">承运人组</span><span class="sxs-lookup"><span data-stu-id="8bdf7-103">Carrier groups</span></span>

<span data-ttu-id="8bdf7-104">承运人组是装运承运人和承运人服务的集合。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="8bdf7-105">每个承运人组都为包含的装运承运人和承运人服务指定了优先顺序。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="8bdf7-106">当同一路线细分存在多个装运承运人和承运人服务时，您可以在路线计划或路线指南中指定承运人组，而不是特定的装运承运人和承运人服务。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="8bdf7-107">创建承运人组</span><span class="sxs-lookup"><span data-stu-id="8bdf7-107">Create a carrier group</span></span>

1. <span data-ttu-id="8bdf7-108">转到 **运输管理 &gt; 设置 &gt; 承运人 &gt; 承运人组**。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="8bdf7-109">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-109">Select **New**.</span></span>
1. <span data-ttu-id="8bdf7-110">在 **承运人组** 字段中，输入组的唯一标识符 (ID)。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="8bdf7-111">在 **名称** 字段中，输入组的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="8bdf7-112">在 **详细信息** 快速选项卡上，添加一行，并为其选择装运承运人和承运人服务。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="8bdf7-113">重复此步骤，直到您为组添加了所需数量的承运人。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="8bdf7-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8bdf7-114">Close the page.</span></span>
