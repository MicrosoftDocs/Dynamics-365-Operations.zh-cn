---
title: 更改促销实体的排序顺序
description: 此主题介绍与在 Microsoft Dynamics 365 for Retail 中控制各种促销相关实体的显示顺序有关的概念。
author: ashishharchwani
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866153"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="ff856-103">更改促销实体的排序顺序</span><span class="sxs-lookup"><span data-stu-id="ff856-103">Change the sort order for merchandising entities</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ff856-104">零售商将产品发现视为所有零售渠道中的主要客户互动工具。</span><span class="sxs-lookup"><span data-stu-id="ff856-104">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span> <span data-ttu-id="ff856-105">可通过大量功能帮助客户轻松发现产品。</span><span class="sxs-lookup"><span data-stu-id="ff856-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="ff856-106">例如，可以浏览类别，进行搜索或使用筛选。</span><span class="sxs-lookup"><span data-stu-id="ff856-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="ff856-107">此主题介绍与控制各种促销相关实体的显示顺序有关的概念。</span><span class="sxs-lookup"><span data-stu-id="ff856-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="ff856-108">还介绍了如何更改排序顺序。</span><span class="sxs-lookup"><span data-stu-id="ff856-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="ff856-109">概览</span><span class="sxs-lookup"><span data-stu-id="ff856-109">Overview</span></span>

<span data-ttu-id="ff856-110">已对为促销关联的各种实体进行排序的支持进行了增强。</span><span class="sxs-lookup"><span data-stu-id="ff856-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="ff856-111">此项支持现在可以更好地适应以前要求实施合作伙伴进行扩展的现有客户方案。</span><span class="sxs-lookup"><span data-stu-id="ff856-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="ff856-112">在低于 10.0.5 的 Microsoft Dynamics 365 for Retail 版本中，导航层次结构中的类别按字母排序。</span><span class="sxs-lookup"><span data-stu-id="ff856-112">In versions of Microsoft Dynamics 365 for Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="ff856-113">促销经理可使用新的自定义排序功能为所有最终用户客户的各种促销相关实体配置排序。</span><span class="sxs-lookup"><span data-stu-id="ff856-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="ff856-114">这些客户包括总部 (HQ) 和呼叫中心。</span><span class="sxs-lookup"><span data-stu-id="ff856-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a><span data-ttu-id="ff856-115">配置零售产品层次结构中的类别的显示顺序</span><span class="sxs-lookup"><span data-stu-id="ff856-115">Configure the display order for categories in the retail product hierarchy</span></span>

<span data-ttu-id="ff856-116">必须先在环境中安装演示数据，才能完成此过程。</span><span class="sxs-lookup"><span data-stu-id="ff856-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="ff856-117">转到 **Retail \> 产品和类别 \> 零售产品层次结构**。</span><span class="sxs-lookup"><span data-stu-id="ff856-117">Go to **Retail \> Products and categories \> Retail product hierarchy**.</span></span>
2. <span data-ttu-id="ff856-118">单击**编辑类别层次结构**。</span><span class="sxs-lookup"><span data-stu-id="ff856-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="ff856-119">单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="ff856-119">Click **Edit**.</span></span>
4. <span data-ttu-id="ff856-120">在树中，展开**所有 \> 操作排序**。</span><span class="sxs-lookup"><span data-stu-id="ff856-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="ff856-121">在树中，展开**所有 \> 团队排序**。</span><span class="sxs-lookup"><span data-stu-id="ff856-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="ff856-122">在**显示顺序**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ff856-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="ff856-123">（该数字可以是负数。）</span><span class="sxs-lookup"><span data-stu-id="ff856-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="ff856-124">对要更改其顺序的其他任何类别重复步骤 4 到 6。</span><span class="sxs-lookup"><span data-stu-id="ff856-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="ff856-125">将在零售产品层次结构和按类别的已发布产品的 HQ 中体现渠道导航层次结构的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="ff856-125">The display order for the channel navigation hierarchy will be reflected in HQ for the retail product hierarchy and released products by category.</span></span>

![使用负值排序的零售产品层次结构自定义](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![基于零售产品层次结构按类别自定义排序的已发布产品](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="ff856-128">配置渠道导航层次结构中的类别的显示顺序</span><span class="sxs-lookup"><span data-stu-id="ff856-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="ff856-129">必须先在环境中安装演示数据，才能完成此过程。</span><span class="sxs-lookup"><span data-stu-id="ff856-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="ff856-130">转到**零售 \> 产品和类别 \> 渠道导航类别**。</span><span class="sxs-lookup"><span data-stu-id="ff856-130">Go to **Retail \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="ff856-131">在列表中，选择**时尚导航**层次结构。</span><span class="sxs-lookup"><span data-stu-id="ff856-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="ff856-132">单击**编辑类别层次结构**。</span><span class="sxs-lookup"><span data-stu-id="ff856-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="ff856-133">单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="ff856-133">Click **Edit**.</span></span>
5. <span data-ttu-id="ff856-134">在树中，选择**时尚 \> 女装 \> 女鞋**。</span><span class="sxs-lookup"><span data-stu-id="ff856-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="ff856-135">在**显示顺序**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ff856-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="ff856-136">在树中，选择**时尚 \> 女装 \> 上装**。</span><span class="sxs-lookup"><span data-stu-id="ff856-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="ff856-137">同样，可以为子类别定义排序顺序。</span><span class="sxs-lookup"><span data-stu-id="ff856-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="ff856-138">在树中，选择**时尚 \> 男装 \> 休闲衬衫**。</span><span class="sxs-lookup"><span data-stu-id="ff856-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="ff856-139">在**显示顺序**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ff856-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="ff856-140">在树中，选择**时尚 \> 男装 \> 外套和夹克**。</span><span class="sxs-lookup"><span data-stu-id="ff856-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="ff856-141">在**显示顺序**字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ff856-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="ff856-142">对要更改其顺序的其他任何类别重复此步骤。</span><span class="sxs-lookup"><span data-stu-id="ff856-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="ff856-143">将在 HQ、目录和零售渠道中体现渠道导航层次结构的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="ff856-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and retail channels.</span></span>

![已为渠道导航层次结构自定义排序](./media/ChannelNavCustomSorted.png)

![已基于渠道导航层次结构为目录导航层次结构自定义排序](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![具有自定义排序的类别的 POS](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="ff856-147">默认情况下，已关闭自定义排序顺序。</span><span class="sxs-lookup"><span data-stu-id="ff856-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="ff856-148">若要了解如何开启此功能和其他功能，请参阅[功能管理](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview)。</span><span class="sxs-lookup"><span data-stu-id="ff856-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
