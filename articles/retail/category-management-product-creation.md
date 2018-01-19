---
title: "产品类别管理和创建"
description: "此主题描述对零售产品类别的管理体验进行的改进。 这些改进使促销活动经理在零售产品层次结构与已发布的产品详细信息之间具有相关性。"
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 2aa9f913b7faac393c4b403c6c36b99cc9acc80c
ms.contentlocale: zh-cn
ms.lasthandoff: 01/19/2018

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="81177-104">产品类别管理和创建</span><span class="sxs-lookup"><span data-stu-id="81177-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="81177-105">对零售产品类别的管理体验进行的改进使促销活动经理在零售产品层次结构与已发布的产品详细信息之间具有相关性。</span><span class="sxs-lookup"><span data-stu-id="81177-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="81177-106">若要查看这些改进，在**类别和产品管理**工作区，选择**零售产品层次结构**以打开**零售产品类别的新结构**页。</span><span class="sxs-lookup"><span data-stu-id="81177-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="81177-107">在以前的版本中，产品属性基于其适用范围划分为基本产品属性和零售产品属性。</span><span class="sxs-lookup"><span data-stu-id="81177-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="81177-108">零售产品属性为*全局*。</span><span class="sxs-lookup"><span data-stu-id="81177-108">Retail product properties were *global*.</span></span> <span data-ttu-id="81177-109">换言之，对于给定的产品属性，在所有法人之间共享相同的值。</span><span class="sxs-lookup"><span data-stu-id="81177-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="81177-110">基本产品属性是*法人 - 特定*。</span><span class="sxs-lookup"><span data-stu-id="81177-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="81177-111">换言之，基于各个业务需求，不同法人之间的给定产品属性可能不同。</span><span class="sxs-lookup"><span data-stu-id="81177-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="81177-112">通过这些改进，对于零售产品类别的产品属性，我们继续基于其在一个组中的适用性分隔字段，以反映已发布产品详细信息窗体结构。</span><span class="sxs-lookup"><span data-stu-id="81177-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="81177-113">您可以在跨所有法人管理法人特定属性与针对特定法人进行管理之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="81177-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="81177-114">只需根据需要选择**查看/编辑所有法人**或**查看/编辑特定法人**。</span><span class="sxs-lookup"><span data-stu-id="81177-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="81177-115">促销活动经理还可以在个别类别级别定义一组附加产品属性的默认值。</span><span class="sxs-lookup"><span data-stu-id="81177-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="81177-116">在产品创建时，这些属性值由产品基于其与类别之间的关联继承。</span><span class="sxs-lookup"><span data-stu-id="81177-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="81177-117">从零售产品类别窗体中选择要更新产品的属性。</span><span class="sxs-lookup"><span data-stu-id="81177-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="81177-118">您可以使用逻辑分组属性来选择应推送到关联产品的更新的产品属性。</span><span class="sxs-lookup"><span data-stu-id="81177-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="81177-119">促销活动经理可以对每个产品修改这些继承的产品属性，以满足单独的业务要求。</span><span class="sxs-lookup"><span data-stu-id="81177-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

