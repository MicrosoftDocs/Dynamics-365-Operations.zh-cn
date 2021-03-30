---
title: 扩展现有库存量数据实体
description: 本主题提供了一个示例，演示如何向 INVENTORSITEONHANDENTITY 和 INVENTWAREHOUSEONHANDENTITY 视图添加扩展字段，以使现有库存量数据实体的功能可以使用扩展。
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0f48e424a9ab3349d3c114ecbd01424005b9a9c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219333"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="b1304-103">扩展现有库存量数据实体</span><span class="sxs-lookup"><span data-stu-id="b1304-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1304-104">Microsoft Dynamics 365 Supply Chain Management 提供[可扩展性](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md)功能，让您可以[通过扩展将字段添加到表中](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="b1304-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md).</span></span> <span data-ttu-id="b1304-105">本主题提供了一个示例，演示如何向 `INVENTORSITEONHANDENTITY` 和 `INVENTWAREHOUSEONHANDENTITY` 视图添加扩展字段，以使现有库存量数据实体的功能可以使用扩展。</span><span class="sxs-lookup"><span data-stu-id="b1304-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="b1304-106">有关数据实体的详细信息，请参阅[数据管理概述](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="b1304-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b1304-107">以下是包含一部分现有库存量数据实体的列表：</span><span class="sxs-lookup"><span data-stu-id="b1304-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="b1304-108">按站点分类的现有库存</span><span class="sxs-lookup"><span data-stu-id="b1304-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="b1304-109">按站点分类的现有库存 V2</span><span class="sxs-lookup"><span data-stu-id="b1304-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="b1304-110">现有库存(按仓库分类)</span><span class="sxs-lookup"><span data-stu-id="b1304-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="b1304-111">按仓库分类的现有库存量 v2</span><span class="sxs-lookup"><span data-stu-id="b1304-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="b1304-112">在将字段添加到 `inventSiteOnHandView` 视图使用的表中之后，必须同步引擎，以正确识别扩展。</span><span class="sxs-lookup"><span data-stu-id="b1304-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="b1304-113">通过添加扩展字段来扩展 `InventSiteOnHandView` 视图。</span><span class="sxs-lookup"><span data-stu-id="b1304-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="b1304-114">使用扩展字段扩展 `InventSiteOnHandAggregatedView` 视图。</span><span class="sxs-lookup"><span data-stu-id="b1304-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="b1304-115">通过修改 `getExtensionFields()` 方法来扩展 `InventSiteOnHandAggregatedViewBuilder` viewBuilder 类。</span><span class="sxs-lookup"><span data-stu-id="b1304-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="b1304-116">这样，您可以在运行 viewBuilder 同步时将旧视图字段映射到新视图字段。</span><span class="sxs-lookup"><span data-stu-id="b1304-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="b1304-117">例如，您通过扩展将以下四个字段添加到了 `InventTable` 表中：</span><span class="sxs-lookup"><span data-stu-id="b1304-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="b1304-118">自定义字段 1</span><span class="sxs-lookup"><span data-stu-id="b1304-118">Custom field 1</span></span>
- <span data-ttu-id="b1304-119">自定义字段 2</span><span class="sxs-lookup"><span data-stu-id="b1304-119">Custom field 2</span></span>
- <span data-ttu-id="b1304-120">自定义字段 3</span><span class="sxs-lookup"><span data-stu-id="b1304-120">Custom field 3</span></span>
- <span data-ttu-id="b1304-121">自定义字段 4</span><span class="sxs-lookup"><span data-stu-id="b1304-121">Custom field 4</span></span>

<span data-ttu-id="b1304-122">在这种情况下，您必须按照以下方式修改 `getExtensionFields()` 方法。</span><span class="sxs-lookup"><span data-stu-id="b1304-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="b1304-123">完成这些步骤后，您可以通过添加新字段来扩展按站点分类的现有库存量和按仓库数据实体分类的现有库存量。</span><span class="sxs-lookup"><span data-stu-id="b1304-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="b1304-124">这样，您可以确保在使用这些数据实体的数据迁移期间扩展字段会被识别出并包含。</span><span class="sxs-lookup"><span data-stu-id="b1304-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]