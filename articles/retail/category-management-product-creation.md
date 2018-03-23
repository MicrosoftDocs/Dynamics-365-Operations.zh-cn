---
title: "产品类别管理"
description: "此主题介绍促销活动经理如何使用零售产品类别管理零售产品层次结构与发布的产品详细信息之间的关系。"
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: zh-cn
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="87538-103">增强的产品和类别管理</span><span class="sxs-lookup"><span data-stu-id="87538-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="87538-104">此主题介绍如何在 Dynamics 365 for Retail 中通过改进的方法管理零售产品类别和产品。</span><span class="sxs-lookup"><span data-stu-id="87538-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="87538-105">这些改进使促销活动经理可以查看零售产品层次结构与已发布的产品详细信息之间共有产品属性的结构。</span><span class="sxs-lookup"><span data-stu-id="87538-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="87538-106">若要了解如何配置零售产品类别的详细信息，请从**类别和产品管理**工作区转至**零售产品类别**，然后记下改进的**零售产品类别**页面结构。</span><span class="sxs-lookup"><span data-stu-id="87538-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![类别和产品管理工作区](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="87538-108">在以前的版本中，产品属性基于其适用范围划分为**基本产品属性**和**零售产品属性**。</span><span class="sxs-lookup"><span data-stu-id="87538-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="87538-109">**零售产品类别**按范围来说是*全局的*，也就是说，对于给定**零售产品属性**，所有法人共用一个值。</span><span class="sxs-lookup"><span data-stu-id="87538-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="87538-110">**基本产品属性**是*特定于法人的*。</span><span class="sxs-lookup"><span data-stu-id="87538-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="87538-111">换言之，对于给定**基本产品属性**，基于各个业务需求，不同法人之间的值可能不同。</span><span class="sxs-lookup"><span data-stu-id="87538-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="87538-112">在改进的零售产品类别结构中，产品属性基于其在组中的适用性分隔，以反映已发布产品详细信息窗体结构。</span><span class="sxs-lookup"><span data-stu-id="87538-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![基于适用范围为字段分组](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="87538-114">您可以在跨所有法人管理法人特定属性与针对特定法人进行管理之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="87538-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="87538-115">方法是，选择**查看/编辑所有法人**或**查看/编辑特定法人**。</span><span class="sxs-lookup"><span data-stu-id="87538-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![在单个法人与所有法人之间切换视图](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![在单个法人与所有法人之间切换视图](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="87538-118">与以前的版本相比，在新版零售产品类别结构中，促销活动经理还可以在单个类别级别再为一组产品属性定义默认值。</span><span class="sxs-lookup"><span data-stu-id="87538-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="87538-119">创建产品时，产品将基于这些默认产品属性与零售产品层次结构中单个类别之间的关联继承这些产品属性。</span><span class="sxs-lookup"><span data-stu-id="87538-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="87538-120">还可以可以对每个产品修改这些继承的产品属性，以满足单独的业务要求。</span><span class="sxs-lookup"><span data-stu-id="87538-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="87538-121">从零售产品类别窗体中选择要更新产品的属性。</span><span class="sxs-lookup"><span data-stu-id="87538-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="87538-122">可使用这个新改进的产品属性结构选择必须将哪些更新的产品属性推送到关联的产品。</span><span class="sxs-lookup"><span data-stu-id="87538-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![新改进的更新产品视图](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="87538-124">促销活动经理可以对每个产品修改这些继承的产品属性，以满足单独的业务要求。</span><span class="sxs-lookup"><span data-stu-id="87538-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


