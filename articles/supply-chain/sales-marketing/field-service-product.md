---
title: 将 Finance and Operations 中的产品同步到 Field Service 中的产品
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的产品的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 3f26240ec289f5ddcc2682e598bbf93f516b99af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "316318"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="e100f-103">将 Finance and Operations 的产品与 Field Service 的产品同步</span><span class="sxs-lookup"><span data-stu-id="e100f-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e100f-104">此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的产品的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="e100f-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e100f-105">使用的 **Field Service 产品（Fin and Ops 到 Field Service）** 模板基于“从目标客户到现金”中的**产品（Fin and Ops 到Sales）– 直接**模板。</span><span class="sxs-lookup"><span data-stu-id="e100f-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="e100f-106">有关详细信息，请参阅[产品（Fin and Ops 到Sales）– 直接](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)。</span><span class="sxs-lookup"><span data-stu-id="e100f-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="e100f-107">本主题仅介绍 **Field Service 产品（Fin and Ops 到 Field Service）** 与**产品（Fin and Ops 到Sales）– 直接**模板之间的差异。</span><span class="sxs-lookup"><span data-stu-id="e100f-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e100f-108">模板和任务</span><span class="sxs-lookup"><span data-stu-id="e100f-108">Templates and tasks</span></span>

<span data-ttu-id="e100f-109">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="e100f-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="e100f-110">Field Service 产品（Fin and Ops 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="e100f-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="e100f-111">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="e100f-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="e100f-112">产品 - 产品</span><span class="sxs-lookup"><span data-stu-id="e100f-112">Products - Products</span></span>

<span data-ttu-id="e100f-113">**Field Service 产品（Fin and Ops 到 Field Service）** 模板中包含**产品（Fin and Ops 到Sales）– 直接**模板中没有的一个映射。</span><span class="sxs-lookup"><span data-stu-id="e100f-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="e100f-114">此映射确保正确设置所需的 Field Service 特定的 **Field Service 产品类型**。</span><span class="sxs-lookup"><span data-stu-id="e100f-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="e100f-115">使用以下值映射。</span><span class="sxs-lookup"><span data-stu-id="e100f-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="e100f-116">在 Finance and Operations 中，**适售的已发布产品**数据实体的 **Field Service 产品类型**值的计算方法如下：</span><span class="sxs-lookup"><span data-stu-id="e100f-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="e100f-117">**库存：** 产品类型 = 产品和物料模型组，贮存的产品 = True</span><span class="sxs-lookup"><span data-stu-id="e100f-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="e100f-118">**非库存：** 产品类型 = 产品和物料模型组，贮存的产品 = False</span><span class="sxs-lookup"><span data-stu-id="e100f-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="e100f-119">**服务：** 产品类型 = 服务</span><span class="sxs-lookup"><span data-stu-id="e100f-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e100f-120">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="e100f-120">Template mapping in Data integration</span></span>

<span data-ttu-id="e100f-121">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="e100f-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="e100f-122">Field Service 产品（Fin and Ops 到 Field Service）：产品 - 产品</span><span class="sxs-lookup"><span data-stu-id="e100f-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="e100f-123">[![数据集成中的模板映射](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="e100f-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
