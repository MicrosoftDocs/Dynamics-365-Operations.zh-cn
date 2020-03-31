---
title: 设置分类
description: 本主题介绍 Dynamics 365 Commerce 中的分类并说明如何设置分类。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26614d319453041177e8072793f09f52ebfd51fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021761"
---
# <a name="set-up-assortments"></a><span data-ttu-id="c8fdd-103">设置分类</span><span class="sxs-lookup"><span data-stu-id="c8fdd-103">Set up assortments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8fdd-104">本主题介绍 Dynamics 365 Commerce 中的分类并说明如何设置分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-104">This article describes what an assortment is and explains how to set up assortments in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c8fdd-105">分类是您分配给商业渠道相关产品的集合，例如实体商店或在线商店。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-105">An assortment is a collection of related products that you assign to a commerce channel, such as a brick-and-mortar store or an online store.</span></span> <span data-ttu-id="c8fdd-106">您使用分类标识每个商店中可用的产品。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-106">You use assortments to identify the products that are available in each store.</span></span> <span data-ttu-id="c8fdd-107">分类可以包括产品的类别。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-107">An assortment can include categories of products.</span></span> <span data-ttu-id="c8fdd-108">因此，分配给包括在此分类中特定类别的所有产品。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-108">Therefore, all products that are assigned to a specific category are included in the assortment.</span></span> <span data-ttu-id="c8fdd-109">分类还可以包括特定产品和产品的特定款式。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-109">An assortment can also include specific products and specific variants of products.</span></span> <span data-ttu-id="c8fdd-110">通过设置分类，可以同时将上千种产品以商店需要的任意组合分配到您的渠道。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-110">By setting up an assortment, you can assign thousands of products to your channels at that same time, in any combination that your stores require.</span></span> <span data-ttu-id="c8fdd-111">如果您需要可以设置多个产品分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-111">You can set up as many product assortments as you require.</span></span> <span data-ttu-id="c8fdd-112">每个产品可以包括在一个或多个分类中，并且每个分类可以分配给一个或多个渠道。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-112">Each product can be included in one or more assortments, and each assortment can be assigned to one or more channels.</span></span> <span data-ttu-id="c8fdd-113">例如，您可以定义包含基本产品组的一个分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-113">For example, you define one assortment that includes a base set of products.</span></span> <span data-ttu-id="c8fdd-114">所有商店接收此分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-114">All stores receive this assortment.</span></span> <span data-ttu-id="c8fdd-115">然后定义另一个分类，其中仅包括大型体育设备。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-115">You then define another assortment that includes only large sporting equipment.</span></span> <span data-ttu-id="c8fdd-116">只有您的更大商店接收此分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-116">Only your larger stores receive this assortment.</span></span> <span data-ttu-id="c8fdd-117">下图显示如何分配产品给分类，并且这些分类如何可分配给渠道。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-117">The following diagram shows how products can be assigned to assortments, and how those assortments can be assigned to channels.</span></span>

![产品分类关系](./media/assortments_relationship.gif)

## <a name="prerequisites"></a><span data-ttu-id="c8fdd-119">先决条件</span><span class="sxs-lookup"><span data-stu-id="c8fdd-119">Prerequisites</span></span>

<span data-ttu-id="c8fdd-120">在您可以设置分类和将其分配给渠道前，必须完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-120">Before you can set up an assortment and assign it to a commerce channel, you must complete the following tasks.</span></span>

| <span data-ttu-id="c8fdd-121">任务</span><span class="sxs-lookup"><span data-stu-id="c8fdd-121">Task</span></span>                              | <span data-ttu-id="c8fdd-122">说明</span><span class="sxs-lookup"><span data-stu-id="c8fdd-122">Description</span></span> |
|-----------------------------------|-------------|
| <span data-ttu-id="c8fdd-123">设置渠道。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-123">Set up a channel.</span></span>          | <span data-ttu-id="c8fdd-124">渠道表示实体商店、在线商店或在线市场。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-124">Channels represent a brick-and-mortar store, an online store, or an online marketplace.</span></span> <span data-ttu-id="c8fdd-125">您必须至少设置一个渠道和配置商店的选项。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-125">You must set up at least one channel and configure the options for the store.</span></span> <span data-ttu-id="c8fdd-126">分类分配给商店标识特定商店持有的产品。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-126">Assortments are assigned to stores to identify the products that a particular store carries.</span></span> |
| <span data-ttu-id="c8fdd-127">创建组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-127">Create an organization hierarchy.</span></span> | <span data-ttu-id="c8fdd-128">在为组织设置商业渠道后，必须配置组织渠道以表示渠道的组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-128">After you set up the commerce channels for your organization, you must configure an organization hierarchy that represents the organizational structure of your channels.</span></span> <span data-ttu-id="c8fdd-129">组织层次结构可用于分类、补货和报告。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-129">An organization hierarchy can be used for assortments, replenishment, and reporting.</span></span> <span data-ttu-id="c8fdd-130">通过添加渠道到您的组织层次结构，可以分配分类到商店的组。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-130">By adding your channels to an organization hierarchy, you can assign assortments to groups of stores.</span></span> <span data-ttu-id="c8fdd-131">不必单独逐一分配此分类到每个商店，您将此分类分配到高级组织节点。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-131">Instead of assigning the assortment individually to each store, you assign the assortment to the high-level organization node.</span></span> <span data-ttu-id="c8fdd-132">然后，新的渠道添加到高级组织节点时，该渠道自动继承分配给级别较高的组织节点的所有分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-132">Then, whenever a new channel is added to the high-level organization node, that channel automatically inherits any assortments that were assigned to the higher-level organization node.</span></span> <span data-ttu-id="c8fdd-133">您只能将分类分配到包括在分配有**商业分类**目标的组织层次结构中的渠道。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-133">You can assign assortments only to channels that are included in an organization hierarchy that is assigned the **Commerce assortment** purpose.</span></span> |
| <span data-ttu-id="c8fdd-134">定义产品。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-134">Define products.</span></span>                  | <span data-ttu-id="c8fdd-135">在可以将产品添加到分类之前，必须将它们添加到 Commerce 中。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-135">Before you can add products to an assortment, you must add them in Commerce.</span></span> <span data-ttu-id="c8fdd-136">您可以手动添加产品，或也可以从供应商导入它们。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-136">You can add products manually, or you can import them from a vendor.</span></span> <span data-ttu-id="c8fdd-137">在您添加产品后，您必须发放到法人。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-137">After you add the products, you must release them to a legal entity.</span></span> <span data-ttu-id="c8fdd-138">只有已发放给法人的产品才能提供给您的渠道。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-138">Only products that have been released to a legal entity can be made available to your channels.</span></span> <span data-ttu-id="c8fdd-139">尚未下达到法人的产品可以添加到分类和可以审核的分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-139">Products that haven't yet been released to a legal entity can be added to an assortment, and the assortment can be approved.</span></span> <span data-ttu-id="c8fdd-140">但是，直到产品已发放到法人，渠道才可以使用这些产品。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-140">However, until the products have been released to a legal entity, they can't be made available to the channels.</span></span> |
| <span data-ttu-id="c8fdd-141">设置类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-141">Set up a category hierarchy.</span></span>      | <span data-ttu-id="c8fdd-142">在您创建商业产品时，可以使用类别层次结构功能对其进行分组和分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-142">When you create your commerce products, you can group and categorize them by using the category hierarchy feature.</span></span> <span data-ttu-id="c8fdd-143">您可以创建一个核心层次结构，以对通过渠道分发的所有产品进行分组和分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-143">You can create one core hierarchy to group and categorize all products that you distribute through your channels.</span></span> <span data-ttu-id="c8fdd-144">您还可以创建进行分组或分类您的专用产品的单独的类别补货层次结构，例如促销或分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-144">You can also create separate, supplemental category hierarchies to group or categorize your products for special purposes, such as promotions or assortments.</span></span> <span data-ttu-id="c8fdd-145">通过使用类别层次结构，则可以分配在特定类别的所有产品到分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-145">By using category hierarchies, you can assign all the products in a specific category to an assortment.</span></span> <span data-ttu-id="c8fdd-146">所有自动添加到类别的产品包括在此分类中。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-146">Any products that are added to the category that is included in the assortment are automatically included in the assortment.</span></span> <span data-ttu-id="c8fdd-147">然后，下次运行商业分类计划程序时，分类分配到的渠道可以使用这些产品。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-147">Then, the next time that the commerce assortment scheduler is run, these products become available to the channels that the assortment is assigned to.</span></span> |

## <a name="setting-up-an-assortment"></a><span data-ttu-id="c8fdd-148">设置分类</span><span class="sxs-lookup"><span data-stu-id="c8fdd-148">Setting up an assortment</span></span>

<span data-ttu-id="c8fdd-149">在您完成先决条件后，您可以创建分类并将其分配给您的渠道。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-149">After you complete the prerequisites, you can create an assortment and assign it to your channels.</span></span> <span data-ttu-id="c8fdd-150">若要设置分类，必须完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-150">To set up an assortment, you must complete the following tasks.</span></span>

1. <span data-ttu-id="c8fdd-151">创建新的分类或者复制现有的分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-151">Create a new assortment, or copy an existing assortment.</span></span>
2. <span data-ttu-id="c8fdd-152">选择渠道或此分类应用于的渠道的更高级别组。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-152">Select the channels or the high-level groups of channels that the assortment applies to.</span></span>
3. <span data-ttu-id="c8fdd-153">添加产品类别、单独的产品或产品变型到此分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-153">Add product categories, individual products, or product variants to the assortment.</span></span> <span data-ttu-id="c8fdd-154">您在特定类别可以包括所有产品，或可以从包括在分类的类别中排除所选的产品。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-154">You can include all products in a specific category, or you can exclude selected products from a category that is included in the assortment.</span></span>
4. <span data-ttu-id="c8fdd-155">发布分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-155">Publish the assortment.</span></span> <span data-ttu-id="c8fdd-156">在发布分类时，将自动运行分类计划程序。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-156">When you publish an assortment, the assortment scheduler is automatically run.</span></span> <span data-ttu-id="c8fdd-157">此过程生成产品列表。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-157">This process generates the list of products.</span></span> <span data-ttu-id="c8fdd-158">在此过程完成后，产品分类分配到的渠道可以使用这些产品。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-158">When this process is completed, the products become available to the channels that the product assortment is assigned to.</span></span> <span data-ttu-id="c8fdd-159">如果对已发布的分类或该分类所分配到的渠道进行了更改，则必须更新该分类。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-159">If changes are made to an assortment that has been published, or to the channels that the assortment is assigned to, the assortment must be updated.</span></span> <span data-ttu-id="c8fdd-160">若要在完成更改后更新此分类，您可以批处理作业形式运行分类计划程序。</span><span class="sxs-lookup"><span data-stu-id="c8fdd-160">To update the assortment when changes are made, you can run the assortment scheduler as a batch job.</span></span>