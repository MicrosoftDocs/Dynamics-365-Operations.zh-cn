---
title: 管理产品类别和产品
description: 此主题介绍促销活动经理如何使用产品类别管理商业产品层次结构与发布的产品详细信息之间的关系。
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cee79d6937afeec1e607abde49d52790c51e98a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001066"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="50f7f-103">管理产品类别和产品</span><span class="sxs-lookup"><span data-stu-id="50f7f-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="50f7f-104">此主题介绍如何在 Dynamics 365 Commerce 中通过改进的方法管理产品类别和产品。</span><span class="sxs-lookup"><span data-stu-id="50f7f-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="50f7f-105">这些改进使促销活动经理可以查看产品层次结构与已发布的产品详细信息之间共有的产品属性结构。</span><span class="sxs-lookup"><span data-stu-id="50f7f-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="50f7f-106">若要了解有关如何管理产品类别的更多信息，请在 **类别和产品管理** 工作区中选择 **商业产品层次结构** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="50f7f-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="50f7f-107">请注意显示的 **商业产品层次结构** 页的增强结构。</span><span class="sxs-lookup"><span data-stu-id="50f7f-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="50f7f-108">在以前的应用版本中，产品属性基于其适用范围划分为 *基本产品属性* 和 *零售产品属性*。</span><span class="sxs-lookup"><span data-stu-id="50f7f-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="50f7f-109">零售产品属性的适用范围为 *全局*。</span><span class="sxs-lookup"><span data-stu-id="50f7f-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="50f7f-110">换言之，对于给定的产品属性，在所有法人之间共享相同的值。</span><span class="sxs-lookup"><span data-stu-id="50f7f-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="50f7f-111">比较而言，基本产品属性是 *特定于法人的*。</span><span class="sxs-lookup"><span data-stu-id="50f7f-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="50f7f-112">换言之，对于给定基本产品属性，不同法人之间的值可能不同，具体取决于各法人各自的业务需求。</span><span class="sxs-lookup"><span data-stu-id="50f7f-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="50f7f-113">在改进的产品类别结构中，产品属性基于其在组中的适用性分隔，以反映已发布产品详细信息窗体结构的结构。</span><span class="sxs-lookup"><span data-stu-id="50f7f-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![基于属性适用范围分组的字段](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="50f7f-115">您可以在跨所有法人管理法人特定属性与针对特定法人进行管理之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="50f7f-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="50f7f-116">若要管理所有法人的属性，请选择 **查看所有法人**（或 **编辑所有法人**）。</span><span class="sxs-lookup"><span data-stu-id="50f7f-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![查看/编辑所有法人](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="50f7f-118">若要管理特定法人的属性，请选择 **查看特定法人**（或 **编辑特定法人**）。</span><span class="sxs-lookup"><span data-stu-id="50f7f-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![查看/编辑特定法人](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="50f7f-120">此外，在增强的产品类别结构中，促销活动经理现在可以在单个类别级别再为一组产品属性定义默认值。</span><span class="sxs-lookup"><span data-stu-id="50f7f-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="50f7f-121">然后，创建产品时，产品将根据其产品属性与产品层次结构中的单个类别的关联，继承这些属性的默认值。</span><span class="sxs-lookup"><span data-stu-id="50f7f-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="50f7f-122">还可以针对每个产品修改这些继承的产品属性，以满足单独的业务要求。</span><span class="sxs-lookup"><span data-stu-id="50f7f-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="50f7f-123">在商业产品层次结构页中选择要更新产品的属性。</span><span class="sxs-lookup"><span data-stu-id="50f7f-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="50f7f-124">可使用这个新改进的产品属性结构选择必须将哪些更新的产品属性推送到关联的产品。</span><span class="sxs-lookup"><span data-stu-id="50f7f-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="50f7f-125">在 **商业产品层次结构** 页上的操作窗格中，选择 **类别**，然后选择 **更新产品** 以打开 **更新产品** 对话框。</span><span class="sxs-lookup"><span data-stu-id="50f7f-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![“更新产品”对话框](media/NewUpdateProductsEnhancedView.PNG)
