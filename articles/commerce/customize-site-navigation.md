---
title: 自定义站点导航
description: 此主题介绍如何创建自定义的在线导航层次结构，以便组织产品以在 Microsoft Dynamics 365 Commerce 站点中进行浏览。
author: bicyclingfool
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ae7696dcb5cdd99cd46b89ed1de1b03c16146e2d
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269651"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="3d1cd-103">自定义站点导航</span><span class="sxs-lookup"><span data-stu-id="3d1cd-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3d1cd-104">此主题介绍如何创建自定义的在线导航层次结构，以便组织产品以在 Microsoft Dynamics 365 Commerce 站点中进行浏览。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="3d1cd-105">概览</span><span class="sxs-lookup"><span data-stu-id="3d1cd-105">Overview</span></span>

<span data-ttu-id="3d1cd-106">客户通常可使用在线店面通过浏览产品类别发现和浏览产品。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="3d1cd-107">此功能通常在页面顶部的选项卡或左侧导航栏中提供。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="3d1cd-108">在 Dynamics 365 Commerce 中，可创建和管理类别导航的分层结构和各类别中包含的产品。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="3d1cd-109">创建渠道导航层次结构</span><span class="sxs-lookup"><span data-stu-id="3d1cd-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="3d1cd-110">若要创建渠道导航层次结构，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="3d1cd-111">转至 **Retail 和 Commerce \> 产品和类别 \> 类别和产品管理**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="3d1cd-112">选择**类别层次结构**，然后选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="3d1cd-113">为层次结构命名。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d1cd-114">您创建的最高级别类别是根类别节点。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="3d1cd-115">不会在您的站点中显示。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-115">It won't be shown on your site.</span></span> <span data-ttu-id="3d1cd-116">若要创建其中的站点上显示一个顶级节点的类别层次结构，请创建类别作为根类别的子代并为其命名。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="3d1cd-117">选择**新建类别节点**，然后为类别命名。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="3d1cd-118">根据需要继续创建同级类别和子类别。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="3d1cd-119">现在可将产品分配给顶级类别下创建的每个类别。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="3d1cd-120">自定义类别顺序</span><span class="sxs-lookup"><span data-stu-id="3d1cd-120">Customize the order of categories</span></span>

<span data-ttu-id="3d1cd-121">默认情况下，您的站点中按字母顺序显示您定义的类别。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="3d1cd-122">但是，也可以自定义类别的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="3d1cd-123">分配某个类别层次机构类型</span><span class="sxs-lookup"><span data-stu-id="3d1cd-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="3d1cd-124">转至 **Retail 和 Commerce \> 产品和类别 \> 类别和产品管理**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="3d1cd-125">选择**类别层次结构**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="3d1cd-126">在操作窗格中**类别层次结构**选项卡上的**设置**组中，选择**关联层次结构类型**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="3d1cd-127">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-127">Select **New**.</span></span>
1. <span data-ttu-id="3d1cd-128">在**类别层次结构类型**字段中，选择**渠道导航层次结构**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="3d1cd-129">在**类别层次结构**字段中，选择前面创建的渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="3d1cd-130">发布新的或更新后的导航层次结构</span><span class="sxs-lookup"><span data-stu-id="3d1cd-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="3d1cd-131">若要使导航层次结构可供在线店面使用，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="3d1cd-132">转到 **Retail 和 Commerce \> 渠道设置 \> 渠道类别和产品属性**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="3d1cd-133">在左侧树中，选择您的在线商店。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="3d1cd-134">选择**发布渠道更新**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="3d1cd-135">转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="3d1cd-136">在列表中，找到并选择**作业 1040**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="3d1cd-137">选择**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-137">Select **Run now**.</span></span>
1. <span data-ttu-id="3d1cd-138">对作业 1070 和 1150 重复执行步骤 5 和 6。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="3d1cd-139">在站点中显示类别</span><span class="sxs-lookup"><span data-stu-id="3d1cd-139">Show categories on your site</span></span>

<span data-ttu-id="3d1cd-140">若要在在线店面中显示类别层次结构，必须在模板或片段中的相应位置添加导航菜单模块。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="3d1cd-141">然后，如果已将导航层次结构发布到站点绑定到的渠道，导航菜单模块将显示您的导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="3d1cd-142">用户可使用商店入门套件中包含的导航菜单模块仅导航到没有子类别的类别。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="3d1cd-143">如果客户应该可以导航到有子类别的类别，则必须自定义导航菜单模块。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="3d1cd-144">添加自定义导航选项</span><span class="sxs-lookup"><span data-stu-id="3d1cd-144">Add custom navigation options</span></span>

<span data-ttu-id="3d1cd-145">在导航菜单中，可添加不属于产品类别层次结构的导航选项。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="3d1cd-146">例如，可在产品类别列表结尾添加指向为站点生成的联系页的**联系我们**项。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="3d1cd-147">若要向导航菜单添加自定义导航选项，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="3d1cd-148">在要自定义的模板或片段中，选择导航菜单模块。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="3d1cd-149">在属性窗格中的**数据**选项卡上，选择**添加项**以创建新的内容管理系统 (CMS) 导航项。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="3d1cd-150">输入链接文本和 URL。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="3d1cd-151">重复执行步骤 2 和 3 以添加更多自定义导航选项。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="3d1cd-152">完成后，选择**保存**以保存模板或片段，然后选择**完成编辑**将其签入。</span><span class="sxs-lookup"><span data-stu-id="3d1cd-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d1cd-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="3d1cd-153">Additional resources</span></span>

[<span data-ttu-id="3d1cd-154">模板和布局概览</span><span class="sxs-lookup"><span data-stu-id="3d1cd-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="3d1cd-155">使用模板</span><span class="sxs-lookup"><span data-stu-id="3d1cd-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="3d1cd-156">使用预设布局</span><span class="sxs-lookup"><span data-stu-id="3d1cd-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="3d1cd-157">使用片段</span><span class="sxs-lookup"><span data-stu-id="3d1cd-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="3d1cd-158">使用模块</span><span class="sxs-lookup"><span data-stu-id="3d1cd-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="3d1cd-159">创建页面 URL</span><span class="sxs-lookup"><span data-stu-id="3d1cd-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="3d1cd-160">使用发布组</span><span class="sxs-lookup"><span data-stu-id="3d1cd-160">Work with publish groups</span></span>](publish-groups.md)
