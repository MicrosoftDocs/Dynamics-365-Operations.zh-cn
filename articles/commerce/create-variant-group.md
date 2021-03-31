---
title: 创建变型组
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中为产品创建尺寸、样式或颜色变型组。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4c34aca043f10fef38f186800c429cac36c41ce7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207839"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="051e2-103">创建款式组</span><span class="sxs-lookup"><span data-stu-id="051e2-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="051e2-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中为产品创建尺寸、样式或颜色变型组。</span><span class="sxs-lookup"><span data-stu-id="051e2-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="051e2-105">概览</span><span class="sxs-lookup"><span data-stu-id="051e2-105">Overview</span></span>

<span data-ttu-id="051e2-106">Dynamics 365 Commerce 支持产品的多种变型。</span><span class="sxs-lookup"><span data-stu-id="051e2-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="051e2-107">最好是为不同的产品类别设置变型。</span><span class="sxs-lookup"><span data-stu-id="051e2-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="051e2-108">例如，可以为尺寸特小、较小、中等、较大和特大的 T 恤创建尺寸组，或者可以创建颜色组以包括产品的所有可用颜色。</span><span class="sxs-lookup"><span data-stu-id="051e2-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="051e2-109">添加产品之前，应添加变型组。</span><span class="sxs-lookup"><span data-stu-id="051e2-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="051e2-110">在本主题中，将创建并配置一个尺寸组。</span><span class="sxs-lookup"><span data-stu-id="051e2-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="051e2-111">类似的过程可用于添加和配置样式组和颜色组。</span><span class="sxs-lookup"><span data-stu-id="051e2-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="051e2-112">创建大小组</span><span class="sxs-lookup"><span data-stu-id="051e2-112">Create a size group</span></span>

<span data-ttu-id="051e2-113">要创建一个大小组，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="051e2-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="051e2-114">在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 变型组 \> 大小组**。</span><span class="sxs-lookup"><span data-stu-id="051e2-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="051e2-115">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="051e2-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="051e2-116">在 **大小组** 框中，输入大小组的名称。</span><span class="sxs-lookup"><span data-stu-id="051e2-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="051e2-117">在 **描述** 框中，输入适当的描述。</span><span class="sxs-lookup"><span data-stu-id="051e2-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="051e2-118">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="051e2-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="051e2-119">将属性添加到大小组</span><span class="sxs-lookup"><span data-stu-id="051e2-119">Add attributes to the size group</span></span>

<span data-ttu-id="051e2-120">若要将属性添加到大小组，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="051e2-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="051e2-121">在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 变型组 \> 大小组**。</span><span class="sxs-lookup"><span data-stu-id="051e2-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="051e2-122">在导航窗格中，选择一个大小组。</span><span class="sxs-lookup"><span data-stu-id="051e2-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="051e2-123">在 **大小组行** 下面，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="051e2-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="051e2-124">在 **大小** 框中，输入代表大小的字符串（例如“XL”）。</span><span class="sxs-lookup"><span data-stu-id="051e2-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="051e2-125">在 **大小名称** 框中，输入大小的名称（例如“特大号”）。</span><span class="sxs-lookup"><span data-stu-id="051e2-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="051e2-126">在 **补货重量** 框中，输入代表补货重量的数字。</span><span class="sxs-lookup"><span data-stu-id="051e2-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="051e2-127">在 **条码中的编号** 框中，输入代表条码的数字。</span><span class="sxs-lookup"><span data-stu-id="051e2-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="051e2-128">在 **显示顺序** 框中，输入代表显示顺序的数字。</span><span class="sxs-lookup"><span data-stu-id="051e2-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="051e2-129">添加完大小后，在操作窗格上选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="051e2-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="051e2-130">下图显示了“休闲衬衫尺寸”的大小组的示例。</span><span class="sxs-lookup"><span data-stu-id="051e2-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![创建大小组](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="051e2-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="051e2-132">Additional resources</span></span>

[<span data-ttu-id="051e2-133">产品信息概览</span><span class="sxs-lookup"><span data-stu-id="051e2-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="051e2-134">设置零售产品</span><span class="sxs-lookup"><span data-stu-id="051e2-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="051e2-135">产品维度</span><span class="sxs-lookup"><span data-stu-id="051e2-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]