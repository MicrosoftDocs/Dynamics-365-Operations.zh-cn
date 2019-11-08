---
title: 维护属性类型
description: 本主题介绍如何在资产管理中创建属性类型。
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c07f303b72f286c33979181fca1592b47efa1303
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571223"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="5c4b9-103">维护属性类型</span><span class="sxs-lookup"><span data-stu-id="5c4b9-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5c4b9-104">本主题介绍如何在资产管理中创建属性类型。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="5c4b9-105">属性用于描述各种元素的属性。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="5c4b9-106">可为以下元素设置属性：</span><span class="sxs-lookup"><span data-stu-id="5c4b9-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="5c4b9-107">功能位置类型</span><span class="sxs-lookup"><span data-stu-id="5c4b9-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="5c4b9-108">功能位置</span><span class="sxs-lookup"><span data-stu-id="5c4b9-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="5c4b9-109">资产类型</span><span class="sxs-lookup"><span data-stu-id="5c4b9-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="5c4b9-110">资产</span><span class="sxs-lookup"><span data-stu-id="5c4b9-110">Assets</span></span>

<span data-ttu-id="5c4b9-111">可设置的属性取决于元素。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="5c4b9-112">例如，对于功能位置，可为位置的配置和物理大小设置属性。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="5c4b9-113">对于资产类型或资产，可设置引擎体积、功耗和最大容量负荷在不同条件下的属性。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="5c4b9-114">创建属性类型</span><span class="sxs-lookup"><span data-stu-id="5c4b9-114">Create attribute types</span></span>

<span data-ttu-id="5c4b9-115">可以创建自己的属性类型。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-115">You can create your own attribute types.</span></span> <span data-ttu-id="5c4b9-116">错误，还可以将产品维度转移到**属性类型**页。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="5c4b9-117">选择**拥有管理** \> **设置** \> **属性类型**。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="5c4b9-118">首次设置属性类型时，选择**创建产品属性**以自动转移标准产品维度。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="5c4b9-119">选择**新建**以创建新属性类型。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="5c4b9-120">在**属性类型**字段中，输入属性类型的名称。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="5c4b9-121">在**描述**字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="5c4b9-122">在**单位**字段中，根据需要选择相关属性单位。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="5c4b9-123">在**数据类型**字段中，选择单位的数据类型。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="5c4b9-124">如果数据类型选择的是**字符串**，则执行以下步骤创建属性类型的值：</span><span class="sxs-lookup"><span data-stu-id="5c4b9-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="5c4b9-125">选择属性类型，然后选择**值**。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="5c4b9-126">在**属性值**字段中，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="5c4b9-127">在**属性类型**字段中，选择一个属性类型（维度）。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="5c4b9-128">在**值**字段中，输入一个相关值。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="5c4b9-129">在**描述**字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="5c4b9-130">保存该记录。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-130">Save the record.</span></span>
    7. <span data-ttu-id="5c4b9-131">回到**属性类型**页。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="5c4b9-132">保存该记录。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-132">Save the record.</span></span>

    <span data-ttu-id="5c4b9-133">**功能位置类型**字段显示使用属性类型的功能位置的数量。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="5c4b9-134">**资产类型**字段显示正在使用功能位置的资产类型的数量。</span><span class="sxs-lookup"><span data-stu-id="5c4b9-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
