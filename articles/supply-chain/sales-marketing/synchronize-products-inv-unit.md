---
title: 将具有库存单位的产品从 Supply Chain Management 同步到 Field Service
description: 此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的具有库存单位的产品的模板和基础任务。
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3485e4f284218924cee01e45d5248f5af1a64010
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215945"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="31b76-103">将具有库存单位的产品从 Supply Chain Management 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="31b76-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="31b76-104">此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的具有库存单位的产品的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="31b76-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="31b76-105">[![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="31b76-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="31b76-106">所用**具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）** 模板基于 **Field Service 产品（Supply Chain Management 到 Field Service）** 模板。</span><span class="sxs-lookup"><span data-stu-id="31b76-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="31b76-107">有关详细信息，请参阅[将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品](field-service-product.md)。</span><span class="sxs-lookup"><span data-stu-id="31b76-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="31b76-108">本主题仅介绍这两个模板之间的区别：</span><span class="sxs-lookup"><span data-stu-id="31b76-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="31b76-109">**具有库存单位的 Field Service 产品（Supply Chain Management 到 Sales）**</span><span class="sxs-lookup"><span data-stu-id="31b76-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="31b76-110">**Field Service 产品（Supply Chain Management 到 Field Service）**</span><span class="sxs-lookup"><span data-stu-id="31b76-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="31b76-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="31b76-111">Templates and tasks</span></span>

<span data-ttu-id="31b76-112">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="31b76-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="31b76-113">具有库存单位的 Field Service 产品（Supply Chain Management 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="31b76-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="31b76-114">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="31b76-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="31b76-115">产品</span><span class="sxs-lookup"><span data-stu-id="31b76-115">Products</span></span>

<span data-ttu-id="31b76-116">**具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）** 模板中包含 **Field Service 产品（Supply Chain Management 到 Field Service）** 模板中不包含的一个映射。</span><span class="sxs-lookup"><span data-stu-id="31b76-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="31b76-117">此映射确保包括库存水平同步所需的库存单位。</span><span class="sxs-lookup"><span data-stu-id="31b76-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="31b76-118">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="31b76-118">Template mapping in Data integration</span></span>

<span data-ttu-id="31b76-119">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="31b76-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="31b76-120">具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）：产品</span><span class="sxs-lookup"><span data-stu-id="31b76-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="31b76-121">[![数据集成中的模板映射](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="31b76-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
