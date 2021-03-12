---
title: 将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品
description: 此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的产品的模板和基础任务。
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ffa0616d51127a024bea526c5926a182c0449971
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996718"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="11607-103">将 Supply Chain Management 中的产品直接同步到 Field Service 中的产品</span><span class="sxs-lookup"><span data-stu-id="11607-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="11607-104">此主题介绍用于将产品从 Dynamics 365 Supply Chain Management 同步到 Dynamics 365 Field Service 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="11607-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="11607-105">使用的 **Field Service 产品（Supply Chain Management 到 Field Service）** 模板基于“从目标客户到现金”中的 **产品（Supply Chain Management 到 Sales）– 直接** 模板。</span><span class="sxs-lookup"><span data-stu-id="11607-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="11607-106">有关详细信息，请参阅[产品（Supply Chain Management 到 Sales）– 直接](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)。</span><span class="sxs-lookup"><span data-stu-id="11607-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="11607-107">本主题仅介绍 **Field Service 产品（Supply Chain Management 到 Field Service）** 与 **产品（Supply Chain Management 到Sales）– 直接** 模板之间的差异。</span><span class="sxs-lookup"><span data-stu-id="11607-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="11607-108">模板和任务</span><span class="sxs-lookup"><span data-stu-id="11607-108">Templates and tasks</span></span>

<span data-ttu-id="11607-109">**数据集成中的模板名称**</span><span class="sxs-lookup"><span data-stu-id="11607-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="11607-110">Field Service 产品（Supply Chain Management 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="11607-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="11607-111">**数据集成项目中的任务名称**</span><span class="sxs-lookup"><span data-stu-id="11607-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="11607-112">产品 - 产品</span><span class="sxs-lookup"><span data-stu-id="11607-112">Products - Products</span></span>

<span data-ttu-id="11607-113">**Field Service 产品（Supply Chain Management 到 Field Service）** 模板中包含 **产品（Supply Chain Management 到 Sales）– 直接** 模板中不包含的一个映射。</span><span class="sxs-lookup"><span data-stu-id="11607-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="11607-114">此映射确保正确设置所需的 Field Service 特定的 **Field Service 产品类型**。</span><span class="sxs-lookup"><span data-stu-id="11607-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="11607-115">使用以下值映射。</span><span class="sxs-lookup"><span data-stu-id="11607-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="11607-116">在 Supply Chain Management 中，**适售的已发布产品** 数据实体的 **Field Service 产品类型** 值的计算方法如下：</span><span class="sxs-lookup"><span data-stu-id="11607-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="11607-117">**库存：** 产品类型 = 产品和物料模型组，贮存的产品 = True</span><span class="sxs-lookup"><span data-stu-id="11607-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="11607-118">**非库存：** 产品类型 = 产品和物料模型组，贮存的产品 = False</span><span class="sxs-lookup"><span data-stu-id="11607-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="11607-119">**服务：** 产品类型 = 服务</span><span class="sxs-lookup"><span data-stu-id="11607-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="11607-120">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="11607-120">Template mapping in Data integration</span></span>

<span data-ttu-id="11607-121">下图显示了数据集成中的模板映射。</span><span class="sxs-lookup"><span data-stu-id="11607-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="11607-122">Field Service 产品（Supply Chain Management 到 Field Service）：产品 - 产品</span><span class="sxs-lookup"><span data-stu-id="11607-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="11607-123">[![数据集成中的模板映射](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="11607-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
