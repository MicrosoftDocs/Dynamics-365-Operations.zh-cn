---
title: 产品所有者
description: 此主题提供有关产品所有者的信息。 产品所有者是负责特定产品的一组用户。 只有该组成员可以发布这些产品。 产品所有者也可以在审核工作流中使用。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 90f5596f9b5fc45e78cc49a3309c45864e07e70b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967325"
---
# <a name="product-owners"></a><span data-ttu-id="41701-106">产品所有者</span><span class="sxs-lookup"><span data-stu-id="41701-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41701-107">产品所有者是负责特定产品的一组用户。</span><span class="sxs-lookup"><span data-stu-id="41701-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="41701-108">将产品所有者组分配给产品后，只有该组的成员可以发布该产品。</span><span class="sxs-lookup"><span data-stu-id="41701-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="41701-109">产品所有者也可以在工程更改管理中的审核工作流中使用。</span><span class="sxs-lookup"><span data-stu-id="41701-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="41701-110">产品所有者是全局设置。</span><span class="sxs-lookup"><span data-stu-id="41701-110">Product owners are global settings.</span></span> <span data-ttu-id="41701-111">因此，可用于所有法人。</span><span class="sxs-lookup"><span data-stu-id="41701-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="41701-112">创建产品所有者组</span><span class="sxs-lookup"><span data-stu-id="41701-112">Create a product owner group</span></span>

<span data-ttu-id="41701-113">若要创建产品所有者组并向其中添加成员，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="41701-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="41701-114">转到 **工程更改管理 \> 设置 \> 产品所有者**。</span><span class="sxs-lookup"><span data-stu-id="41701-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="41701-115">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="41701-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="41701-116">在 **产品所有者** 字段中，为组输入名称。</span><span class="sxs-lookup"><span data-stu-id="41701-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="41701-117">在 **名称** 字段中，输入组的描述。</span><span class="sxs-lookup"><span data-stu-id="41701-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="41701-118">在 **成员** 快速选项卡上，添加应成为组成员的工作人员。</span><span class="sxs-lookup"><span data-stu-id="41701-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="41701-119">向产品分配产品所有者</span><span class="sxs-lookup"><span data-stu-id="41701-119">Assign a product owner to a product</span></span>

<span data-ttu-id="41701-120">要向产品分配产品所有者，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="41701-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="41701-121">打开相关产品或基础产品的 **产品详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="41701-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="41701-122">在 **常规** 快速选项卡上，将 **产品所有者** 字段设置为相关产品所有者组的名称。</span><span class="sxs-lookup"><span data-stu-id="41701-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="41701-123">将产品所有者分配给产品后，只有产品所有者组的成员可以编辑 **产品所有者** 设置。</span><span class="sxs-lookup"><span data-stu-id="41701-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="41701-124">产品所有者也在 **已发布产品** 页上可见。</span><span class="sxs-lookup"><span data-stu-id="41701-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="41701-125">产品所有者和产品发布</span><span class="sxs-lookup"><span data-stu-id="41701-125">Product owners and product releases</span></span>

<span data-ttu-id="41701-126">只有产品的产品所有者组中的用户可以发布该产品。</span><span class="sxs-lookup"><span data-stu-id="41701-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="41701-127">但是，如果产品是子物料并且其父物料由父物料的所有者发布，这时会有例外。</span><span class="sxs-lookup"><span data-stu-id="41701-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="41701-128">换言之，如果该产品是另一个产品的物料清单的一部分，系统不会检查物料清单中每个物料的产品所有者。</span><span class="sxs-lookup"><span data-stu-id="41701-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="41701-129">只会检查父物料的产品所有者。</span><span class="sxs-lookup"><span data-stu-id="41701-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="41701-130">例如，产品 X 被分配到 *设计柜* 产品所有者组。</span><span class="sxs-lookup"><span data-stu-id="41701-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="41701-131">产品 X 也是产品 Y 的物料清单的一部分，后者被分配到 *设计扬声器* 产品所有者组。</span><span class="sxs-lookup"><span data-stu-id="41701-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="41701-132">如果来自 *设计扬声器* 产品所有者组的用户发布产品 Y 及其物料清单，产品 X 将与产品 Y 一起发布。</span><span class="sxs-lookup"><span data-stu-id="41701-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="41701-133">产品所有者和审核</span><span class="sxs-lookup"><span data-stu-id="41701-133">Product owners and approvals</span></span>

<span data-ttu-id="41701-134">因为产品所有者知道特定的工程更改是否会对他们的产品有所帮助，所以在工程更改管理中将它们作为审核流程的一部分包括在内通常是有意义的。</span><span class="sxs-lookup"><span data-stu-id="41701-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="41701-135">您可以通过在用于工程更改管理的工作流中将产品所有者设置为参与者提供方来实现此方法。</span><span class="sxs-lookup"><span data-stu-id="41701-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="41701-136">然后，系统将基于工程更改请求和工程更改订单中的产品在工作流中分配审核任务。</span><span class="sxs-lookup"><span data-stu-id="41701-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="41701-137">有关详细信息，请参阅[管理工程产品的更改](engineering-change-management.md)。</span><span class="sxs-lookup"><span data-stu-id="41701-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>
