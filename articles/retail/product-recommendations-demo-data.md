---
title: 全渠道产品建议演示数据
description: 此文档旨在使用预填充的可自定义演示数据提供有关如何在 1 级单盒环境中利用全渠道产品建议的指导。
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225633"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="36ebc-103">全渠道产品建议演示数据</span><span class="sxs-lookup"><span data-stu-id="36ebc-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="36ebc-104">此文档旨在使用预填充的可自定义演示数据提供有关如何在 1 级单盒环境中利用全渠道产品建议的指导。</span><span class="sxs-lookup"><span data-stu-id="36ebc-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="36ebc-105">全渠道产品建议提供一组以编辑身份策划或以编程方式生成的已排序产品列表。</span><span class="sxs-lookup"><span data-stu-id="36ebc-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="36ebc-106">可以在多种方案中使用这些列表，具体取决于业务需要。</span><span class="sxs-lookup"><span data-stu-id="36ebc-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="36ebc-107">有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendaitons-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="36ebc-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="36ebc-108">对于 2 级及更高 Dynamics 环境，将根据客户数据自动计算产品建议。</span><span class="sxs-lookup"><span data-stu-id="36ebc-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="36ebc-109">使用产品建议演示数据不会禁用环境中已设置的任何产品建议解决方案和与其使用关联的任何成本。</span><span class="sxs-lookup"><span data-stu-id="36ebc-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="36ebc-110">对于 1 级环境，产品建议仅基于 csv 文件中存储的静态演示数据。</span><span class="sxs-lookup"><span data-stu-id="36ebc-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="36ebc-111">在环境中启用产品建议演示数据</span><span class="sxs-lookup"><span data-stu-id="36ebc-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="36ebc-112">客户需要将 **Dynamics 365 Commerce 预览演示扩展**部署到相应环境，这将自动启用产品建议演示数据。</span><span class="sxs-lookup"><span data-stu-id="36ebc-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="36ebc-113">默认演示数据</span><span class="sxs-lookup"><span data-stu-id="36ebc-113">Default demo data</span></span>
<span data-ttu-id="36ebc-114">每个 Onebox 类型的环境都自带一组预加载的产品建议演示数据，这些数据存储在以逗号分隔的 **‘reco_demo_data.csv’** 文件中，该文件与此文档位于 Retail Server 上的同一个文件夹中。</span><span class="sxs-lookup"><span data-stu-id="36ebc-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="36ebc-115">此数据与以下列一起结构化</span><span class="sxs-lookup"><span data-stu-id="36ebc-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="36ebc-116">列名</span><span class="sxs-lookup"><span data-stu-id="36ebc-116">Column name</span></span>         | <span data-ttu-id="36ebc-117">限定</span><span class="sxs-lookup"><span data-stu-id="36ebc-117">Mandatory</span></span>          | <span data-ttu-id="36ebc-118">说明</span><span class="sxs-lookup"><span data-stu-id="36ebc-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="36ebc-119">可能的值</span><span class="sxs-lookup"><span data-stu-id="36ebc-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="36ebc-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="36ebc-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="36ebc-122">演示数据点要生成的特定产品建议列表类型。</span><span class="sxs-lookup"><span data-stu-id="36ebc-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="36ebc-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="36ebc-123">RecoBestSelling</span></span></li><li><span data-ttu-id="36ebc-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="36ebc-124">RecoNew</span></span></li><li><span data-ttu-id="36ebc-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="36ebc-125">RecoTrending</span></span></li><li><span data-ttu-id="36ebc-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="36ebc-126">RecoCart</span></span></li><li><span data-ttu-id="36ebc-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="36ebc-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="36ebc-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="36ebc-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="36ebc-130">预期在其中出现产品建议的特定运营单位编号。</span><span class="sxs-lookup"><span data-stu-id="36ebc-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="36ebc-131">类别</span><span class="sxs-lookup"><span data-stu-id="36ebc-131">Category</span></span>            |                    |    <span data-ttu-id="36ebc-132">应该为其返回特定列表的类别。</span><span class="sxs-lookup"><span data-stu-id="36ebc-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="36ebc-133">如果不指定任何类别，则列表仅针对导航层次结构顶部。</span><span class="sxs-lookup"><span data-stu-id="36ebc-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="36ebc-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="36ebc-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="36ebc-135">对于需要种子的列表（RecoPeopleAlsoBuy 和 RecoCart），为这些列表应为其显示更多产品的产品。</span><span class="sxs-lookup"><span data-stu-id="36ebc-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="36ebc-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="36ebc-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="36ebc-138">要作为结果返回且以 **‘;’** 分隔的一个或多个产品。</span><span class="sxs-lookup"><span data-stu-id="36ebc-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="36ebc-139">自定义演示数据</span><span class="sxs-lookup"><span data-stu-id="36ebc-139">Customize demo data</span></span>
<span data-ttu-id="36ebc-140">客户可编辑包含在总部配置的任何产品和类别信息的默认演示数据。</span><span class="sxs-lookup"><span data-stu-id="36ebc-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="36ebc-141">更新 CSV 之后，返回给客户的产品建议将立即体现更改。</span><span class="sxs-lookup"><span data-stu-id="36ebc-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="36ebc-142">此扩展中包含一个数据文件，称为 RecoMockDataset.csv，供客户控制用于增强模拟建议结果的数据集。</span><span class="sxs-lookup"><span data-stu-id="36ebc-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="36ebc-143">可以使用 **ext.Recommendations.DemoFilePath** 设置通过扩展名配置来控制文件名。</span><span class="sxs-lookup"><span data-stu-id="36ebc-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="36ebc-144">这样就可以为客户提供多个可通过配置轻松切换的数据集。</span><span class="sxs-lookup"><span data-stu-id="36ebc-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="36ebc-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="36ebc-145">Additional resources</span></span>

[<span data-ttu-id="36ebc-146">产品建议概述</span><span class="sxs-lookup"><span data-stu-id="36ebc-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="36ebc-147">环境计划</span><span class="sxs-lookup"><span data-stu-id="36ebc-147">Environment planning</span></span>](environment-planning.md)
