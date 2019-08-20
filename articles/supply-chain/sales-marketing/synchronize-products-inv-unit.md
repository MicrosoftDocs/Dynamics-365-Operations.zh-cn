---
title: 将具有库存单位的产品从 Finance and Operations 同步到 Field Service
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的具有库存单位的产品的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835686"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="7b70a-103">将具有库存单位的产品从 Finance and Operations 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="7b70a-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b70a-104">此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的具有库存单位的产品的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="7b70a-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="7b70a-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="7b70a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="7b70a-106">所用**具有库存单位的 Field Service 产品（Fin and Ops 到 Field Service）** 模板基于 **Field Service 产品（Fin and Ops 到 Field Service）** 模板。</span><span class="sxs-lookup"><span data-stu-id="7b70a-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="7b70a-107">有关详细信息，请参阅 [Field Service 产品（Finance and Operations 到 Field Service）](field-service-product.md)。</span><span class="sxs-lookup"><span data-stu-id="7b70a-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="7b70a-108">本主题仅介绍这两个模板之间的区别：</span><span class="sxs-lookup"><span data-stu-id="7b70a-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="7b70a-109">**具有库存单位的 Field Service 产品（Fin and Ops 到 Sales）**</span><span class="sxs-lookup"><span data-stu-id="7b70a-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="7b70a-110">**Field Service 产品（Fin and Ops 到 Field Service）**</span><span class="sxs-lookup"><span data-stu-id="7b70a-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="7b70a-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="7b70a-111">Templates and tasks</span></span>

<span data-ttu-id="7b70a-112">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="7b70a-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="7b70a-113">具有库存单位的 Field Service 产品（Fin and Ops 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="7b70a-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="7b70a-114">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="7b70a-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="7b70a-115">产品</span><span class="sxs-lookup"><span data-stu-id="7b70a-115">Products</span></span>

<span data-ttu-id="7b70a-116">**具有库存单位的 Field Service 产品（Fin and Ops 到 Field Service）** 模板包括 **Field Service 产品（Fin and Ops 到 Field Service）** 模板中不包括的一个映射。</span><span class="sxs-lookup"><span data-stu-id="7b70a-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="7b70a-117">此映射确保包括库存水平同步所需的库存单位。</span><span class="sxs-lookup"><span data-stu-id="7b70a-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b70a-118">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="7b70a-118">Template mapping in Data integration</span></span>

<span data-ttu-id="7b70a-119">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="7b70a-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="7b70a-120">具有库存单位的 Field Service 产品（Fin and Ops 到 Field Service）：产品</span><span class="sxs-lookup"><span data-stu-id="7b70a-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="7b70a-121">[![数据集成中的模板映射](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="7b70a-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
