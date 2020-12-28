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
ms.openlocfilehash: 911c5cc79ae359bbb77d31f366ccfeabf282a33e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423142"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="cdb9d-103">将具有库存单位的产品从 Supply Chain Management 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="cdb9d-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cdb9d-104">此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的具有库存单位的产品的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="cdb9d-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="cdb9d-105">[![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="cdb9d-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="cdb9d-106">所用 **具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）** 模板基于 **Field Service 产品（Supply Chain Management 到 Field Service）** 模板。</span><span class="sxs-lookup"><span data-stu-id="cdb9d-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="cdb9d-107">有关详细信息，请参阅[将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品](field-service-product.md)。</span><span class="sxs-lookup"><span data-stu-id="cdb9d-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="cdb9d-108">本主题仅介绍这两个模板之间的区别：</span><span class="sxs-lookup"><span data-stu-id="cdb9d-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="cdb9d-109">**具有库存单位的 Field Service 产品（Supply Chain Management 到 Sales）**</span><span class="sxs-lookup"><span data-stu-id="cdb9d-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="cdb9d-110">**Field Service 产品（Supply Chain Management 到 Field Service）**</span><span class="sxs-lookup"><span data-stu-id="cdb9d-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="cdb9d-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="cdb9d-111">Templates and tasks</span></span>

<span data-ttu-id="cdb9d-112">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="cdb9d-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="cdb9d-113">具有库存单位的 Field Service 产品（Supply Chain Management 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="cdb9d-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="cdb9d-114">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="cdb9d-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="cdb9d-115">产品</span><span class="sxs-lookup"><span data-stu-id="cdb9d-115">Products</span></span>

<span data-ttu-id="cdb9d-116">**具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）** 模板中包含 **Field Service 产品（Supply Chain Management 到 Field Service）** 模板中不包含的一个映射。</span><span class="sxs-lookup"><span data-stu-id="cdb9d-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="cdb9d-117">此映射确保包括库存水平同步所需的库存单位。</span><span class="sxs-lookup"><span data-stu-id="cdb9d-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cdb9d-118">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="cdb9d-118">Template mapping in Data integration</span></span>

<span data-ttu-id="cdb9d-119">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="cdb9d-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="cdb9d-120">具有库存单位的 Field Service 产品（Supply Chain Management 到 Field Service）：产品</span><span class="sxs-lookup"><span data-stu-id="cdb9d-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="cdb9d-121">[![数据集成中的模板映射](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="cdb9d-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
