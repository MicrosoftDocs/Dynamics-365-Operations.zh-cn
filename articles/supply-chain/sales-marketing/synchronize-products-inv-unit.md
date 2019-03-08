---
title: 将具有库存单位的产品从 Finance and Operations 同步到 Field Service
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的具有库存单位的产品的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "359236"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c95ed-103">将具有库存单位的产品从 Finance and Operations 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="c95ed-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c95ed-104">此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的具有库存单位的产品的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="c95ed-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c95ed-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="c95ed-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="c95ed-106">使用的 **Field Service 产品（Finance and Operations 到 Field Service）** 模板基于“从目标客户到现金”中的**产品（Finance and Operations 到Sales）– 直接**模板。</span><span class="sxs-lookup"><span data-stu-id="c95ed-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="c95ed-107">有关详细信息，请参阅[产品（Finance and Operations 到 Sales）– 直接](products-template-mapping-direct.md)。</span><span class="sxs-lookup"><span data-stu-id="c95ed-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="c95ed-108">本主题仅介绍 **Field Service 产品（Finance and Operations 到 Field Service）** 与 **Field Service 产品（Finance and Operations 到Sales）– 直接**模板之间的差异。</span><span class="sxs-lookup"><span data-stu-id="c95ed-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c95ed-109">模板和任务</span><span class="sxs-lookup"><span data-stu-id="c95ed-109">Templates and tasks</span></span>

<span data-ttu-id="c95ed-110">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="c95ed-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="c95ed-111">具有库存单位的 Field Service 产品（Finance and Operations 到 Sales）</span><span class="sxs-lookup"><span data-stu-id="c95ed-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="c95ed-112">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="c95ed-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="c95ed-113">产品</span><span class="sxs-lookup"><span data-stu-id="c95ed-113">Products</span></span>

<span data-ttu-id="c95ed-114">**具有库存单位的 Field Service 产品（Finance and Operations 到 Field Service）** 模板包括 **Field Service 产品（Finance and Operations 到 Field Service）** 模板中不包括的一个映射。</span><span class="sxs-lookup"><span data-stu-id="c95ed-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="c95ed-115">此映射确保包括库存水平同步所需的库存单位。</span><span class="sxs-lookup"><span data-stu-id="c95ed-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c95ed-116">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="c95ed-116">Template mapping in Data integration</span></span>

<span data-ttu-id="c95ed-117">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="c95ed-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="c95ed-118">具有库存单位的 Field Service 产品（Finance and Operations 到 Field Service）：产品</span><span class="sxs-lookup"><span data-stu-id="c95ed-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="c95ed-119">[![数据集成中的模板映射](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="c95ed-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
