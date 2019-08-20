---
title: 创建库位模板
description: 仓库中的每个库位都需要关联一个库位模板，用于描述库位的属性，例如，库位是否允许混合物料。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: a9e1217a1105e1d53fc937f927e066e392f1ef14
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847319"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="6e371-103">创建库位模板</span><span class="sxs-lookup"><span data-stu-id="6e371-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e371-104">仓库中的每个库位都需要关联一个库位模板，用于描述库位的属性，例如，库位是否允许混合物料。</span><span class="sxs-lookup"><span data-stu-id="6e371-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="6e371-105">在此过程中，我们将为不需要牌照控制的库位创建模板。</span><span class="sxs-lookup"><span data-stu-id="6e371-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="6e371-106">我们将启用混合物料和混合库存状态，并允许周期盘点。</span><span class="sxs-lookup"><span data-stu-id="6e371-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="6e371-107">您可以在 USMF 演示数据公司中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="6e371-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="6e371-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6e371-108">Click New.</span></span>
2. <span data-ttu-id="6e371-109">在“位置模板 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6e371-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="6e371-110">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6e371-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6e371-111">在“位置格式”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6e371-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="6e371-112">在“位置类型”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6e371-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="6e371-113">在“码头管理模板 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6e371-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="6e371-114">选择“允许混合物料”字段中的“是”。</span><span class="sxs-lookup"><span data-stu-id="6e371-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="6e371-115">选择“允许混合库存状态”字段中的“是”。</span><span class="sxs-lookup"><span data-stu-id="6e371-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="6e371-116">在“允许周期盘点”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="6e371-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="6e371-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6e371-117">Click Save.</span></span>
11. <span data-ttu-id="6e371-118">转到“仓库管理”>“设置”>“仓库”>“位置模板”。</span><span class="sxs-lookup"><span data-stu-id="6e371-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

