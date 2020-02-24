---
title: 使用演示数据获取产品建议
description: 此文档使用预填充的可自定义演示数据提供有关如何在 1 级单盒环境中利用全渠道产品建议的指导。
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6abac72b7530dc7b82c8e95faebdce791cf7dbd1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003226"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="4c0ef-103">使用演示数据获取产品建议</span><span class="sxs-lookup"><span data-stu-id="4c0ef-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="4c0ef-104">此文档使用预填充的可自定义演示数据提供有关如何在 1 级单盒环境中利用全渠道产品建议的指导。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="4c0ef-105">全渠道产品建议提供一组以编辑身份策划或以编程方式生成的产品列表。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="4c0ef-106">可以在多种方案中使用这些列表，具体取决于业务需要。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="4c0ef-107">有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="4c0ef-108">对于 2 级及更高 Dynamics 365 环境，将根据客户数据自动计算产品建议。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="4c0ef-109">使用产品建议演示数据不会禁用环境中已设置的任何产品建议解决方案和与其使用关联的任何成本。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="4c0ef-110">对于 1 级环境，产品建议仅基于 .csv 文件中存储的静态演示数据。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="4c0ef-111">在环境中启用产品建议演示数据</span><span class="sxs-lookup"><span data-stu-id="4c0ef-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="4c0ef-112">若要启用产品建议演示日期，需要将 Dynamics 365 Commerce 预览演示扩展部署到相应环境。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="4c0ef-113">这将自动启用产品建议演示数据。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="4c0ef-114">默认演示数据</span><span class="sxs-lookup"><span data-stu-id="4c0ef-114">Default demo data</span></span>
<span data-ttu-id="4c0ef-115">每个 Onebox 类型的环境都自带一组预加载的产品建议演示数据，这些数据存储在以逗号分隔的“reco_demo_data.csv”文件中，该文件位于 Commerce Scale Unit 上。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="4c0ef-116">此数据与以下列一起结构化。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="4c0ef-117">列名</span><span class="sxs-lookup"><span data-stu-id="4c0ef-117">Column name</span></span>         | <span data-ttu-id="4c0ef-118">限定</span><span class="sxs-lookup"><span data-stu-id="4c0ef-118">Mandatory</span></span>          | <span data-ttu-id="4c0ef-119">说明</span><span class="sxs-lookup"><span data-stu-id="4c0ef-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="4c0ef-120">可能的值</span><span class="sxs-lookup"><span data-stu-id="4c0ef-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4c0ef-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="4c0ef-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="4c0ef-123">演示数据点要生成的特定产品建议列表类型。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="4c0ef-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="4c0ef-124">RecoBestSelling</span></span></li><li><span data-ttu-id="4c0ef-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="4c0ef-125">RecoNew</span></span></li><li><span data-ttu-id="4c0ef-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="4c0ef-126">RecoTrending</span></span></li><li><span data-ttu-id="4c0ef-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="4c0ef-127">RecoCart</span></span></li><li><span data-ttu-id="4c0ef-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="4c0ef-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="4c0ef-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="4c0ef-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="4c0ef-131">预期在其中出现产品建议的特定运营单位编号。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="4c0ef-132">类别</span><span class="sxs-lookup"><span data-stu-id="4c0ef-132">Category</span></span>            |                    |    <span data-ttu-id="4c0ef-133">应该为其返回特定列表的类别。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="4c0ef-134">如果不指定任何类别，则列表仅针对导航层次结构顶部。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="4c0ef-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="4c0ef-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="4c0ef-136">对于需要种子的列表（RecoPeopleAlsoBuy 和 RecoCart），为这些列表应为其显示更多产品的产品。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="4c0ef-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="4c0ef-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="4c0ef-139">要作为结果返回且以“;”分隔的一个或多个产品。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="4c0ef-140">自定义演示数据</span><span class="sxs-lookup"><span data-stu-id="4c0ef-140">Customize demo data</span></span>
<span data-ttu-id="4c0ef-141">您可编辑包含在总部配置的任何产品和类别信息的默认演示数据。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="4c0ef-142">更新 .csv 之后，返回给客户的产品建议将立即体现更改。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="4c0ef-143">此扩展中包含一个数据文件，称为 RecoMockDataset.csv，供您控制用于增强模拟建议结果的数据集。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="4c0ef-144">可以使用 **ext.Recommendations.DemoFilePath** 设置通过扩展名配置来控制文件名。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="4c0ef-145">这样就可以为您提供多个可通过配置轻松切换的数据集。</span><span class="sxs-lookup"><span data-stu-id="4c0ef-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="4c0ef-146">其他资源</span><span class="sxs-lookup"><span data-stu-id="4c0ef-146">Additional Resources</span></span>

[<span data-ttu-id="4c0ef-147">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="4c0ef-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4c0ef-148">环境计划</span><span class="sxs-lookup"><span data-stu-id="4c0ef-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
