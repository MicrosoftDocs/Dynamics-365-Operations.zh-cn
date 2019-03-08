---
title: 管理零售产品类别和产品
description: 此主题介绍促销活动经理如何使用零售产品类别管理零售产品层次结构与发布的产品详细信息之间的关系。
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bcc5989edd9913fce414c0c24068f111d8c1aeb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "344677"
---
# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="2cb3c-103">管理零售产品类别和产品</span><span class="sxs-lookup"><span data-stu-id="2cb3c-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="2cb3c-104">此主题介绍如何在 Microsoft Dynamics 365 for Retail 中通过改进的方法管理零售产品类别和产品。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="2cb3c-105">这些改进使促销活动经理可以查看零售产品层次结构与已发布的产品详细信息之间共有的产品属性结构。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="2cb3c-106">若要了解有关如何管理零售产品类别的更多信息，请在**类别和产品管理**工作区中选择**零售产品层次结构**磁贴。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="2cb3c-107">请注意显示的**零售产品层次结构**页的增强结构。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="2cb3c-108">在以前的 Retail 版本中，产品属性基于其适用范围划分为*基本产品属性*和*零售产品属性*。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="2cb3c-109">零售产品属性的适用范围为*全局*。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="2cb3c-110">换言之，对于给定的零售产品属性，在所有法人之间共享相同的值。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="2cb3c-111">比较而言，基本产品属性是*特定于法人的*。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="2cb3c-112">换言之，对于给定基本产品属性，不同法人之间的值可能不同，具体取决于各法人各自的业务需求。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="2cb3c-113">在改进的零售产品类别结构中，产品属性基于其在组中的适用性分隔，以反映已发布产品详细信息窗体结构的结构。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![基于属性适用范围分组的字段](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="2cb3c-115">您可以在跨所有法人管理法人特定属性与针对特定法人进行管理之间进行切换。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="2cb3c-116">若要管理所有法人的属性，请选择**查看所有法人**（或 **编辑所有法人**）。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![查看/编辑所有法人](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="2cb3c-118">若要管理特定法人的属性，请选择**查看特定法人**（或**编辑特定法人**）。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![查看/编辑特定法人](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="2cb3c-120">此外，在增强的零售产品类别结构中，促销活动经理现在可以在单个类别级别再为一组产品属性定义默认值。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="2cb3c-121">然后，创建产品时，产品将根据其产品属性与零售产品层次结构中的单个类别的关联，继承这些属性的默认值。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="2cb3c-122">还可以针对每个产品修改这些继承的产品属性，以满足单独的业务要求。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="2cb3c-123">在零售产品层次结构页中选择要更新产品的属性。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="2cb3c-124">可使用这个新改进的产品属性结构选择必须将哪些更新的产品属性推送到关联的产品。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="2cb3c-125">在**零售产品层次结构**页上的操作窗格中，选择**类别**，然后选择**更新产品**以打开**更新产品**对话框。</span><span class="sxs-lookup"><span data-stu-id="2cb3c-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![“更新产品”对话框](media/NewUpdateProductsEnhancedView.PNG)
