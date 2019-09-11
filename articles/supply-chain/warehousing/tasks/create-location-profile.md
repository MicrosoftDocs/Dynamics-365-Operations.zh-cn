---
title: 创建库位模板
description: 本主题说明如何在 Dynamics 365 for Finance and Operations 中创建库位模板。
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46aa1001c21ae39c158062444303ca02c0f41a45
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866971"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="1e7fd-103">创建库位模板</span><span class="sxs-lookup"><span data-stu-id="1e7fd-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e7fd-104">本主题说明如何在 Dynamics 365 for Finance and Operations 中创建库位模板。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-104">This topic explains how to create a location profile in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1e7fd-105">仓库中的每个库位都需要关联一个库位模板，用于描述库位的属性，例如，库位是否允许混合物料。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="1e7fd-106">在此过程中，我们将为不需要牌照控制的库位创建模板。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-106">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="1e7fd-107">我们将启用混合物料和混合库存状态，并允许周期盘点。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-107">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="1e7fd-108">您可以在 USMF 演示数据公司中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="1e7fd-109">在导航窗格中，转到**模块 > 仓库管理 > 设置 > 仓库 > 库位模板**。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="1e7fd-110">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-110">Select **New**.</span></span>
3. <span data-ttu-id="1e7fd-111">在**库位模板 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="1e7fd-112">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="1e7fd-113">在**位置格式**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="1e7fd-114">在**位置类型**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="1e7fd-115">在**码头管理模板 ID** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="1e7fd-116">选择**允许混合物料**字段中的**是**。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="1e7fd-117">选择**允许混合库存状态**字段中的**是**。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="1e7fd-118">在**允许周期盘点**字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="1e7fd-119">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="1e7fd-119">Select **Save**.</span></span>

