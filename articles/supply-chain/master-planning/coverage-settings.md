---
title: "覆盖范围设置"
description: "主计划编制使用覆盖范围设置计算物料需求。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 50f47394a4d4e95b4e158ea42a630d9e6e91f05b
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="coverage-settings"></a><span data-ttu-id="f81d8-103">覆盖范围设置</span><span class="sxs-lookup"><span data-stu-id="f81d8-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f81d8-104">主计划编制使用覆盖范围设置计算物料需求。</span><span class="sxs-lookup"><span data-stu-id="f81d8-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="f81d8-105">您可以通过以下几种方式指定覆盖范围设置：</span><span class="sxs-lookup"><span data-stu-id="f81d8-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="f81d8-106">为覆盖范围组指定覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="f81d8-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="f81d8-107">您可以创建一个覆盖范围组，它包含与该组关联的所有产品的设置。</span><span class="sxs-lookup"><span data-stu-id="f81d8-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="f81d8-108">单击**主计划 &gt; 设置 &gt; 覆盖范围 &gt; 覆盖范围组**以创建覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="f81d8-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="f81d8-109">您可以将覆盖范围组与某个产品链接。</span><span class="sxs-lookup"><span data-stu-id="f81d8-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="f81d8-110">如果链接特定于站点、仓库或产品维度，请使用**物料覆盖范围**页的**覆盖范围组**字段。</span><span class="sxs-lookup"><span data-stu-id="f81d8-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="f81d8-111">如果链接是通用的，无论产品维度如何，请使用**产品详细信息**页中**计划**快速选项卡上的**覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="f81d8-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="f81d8-112">如果您没有将某一覆盖范围组与某一产品关联，则主计划将使用在**主计划参数**页中指定的**一般覆盖范围组**作为默认覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="f81d8-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="f81d8-113">为产品指定覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="f81d8-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="f81d8-114">您可为特定产品创建覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="f81d8-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="f81d8-115">单击**产品信息管理 &gt; 产品 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="f81d8-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="f81d8-116">选择产品，在**操作窗格**上的**计划**选项卡中**覆盖范围组**中，单击**物料覆盖范围**打开**物料覆盖范围**页。</span><span class="sxs-lookup"><span data-stu-id="f81d8-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="f81d8-117">如果该产品已链接到某一覆盖范围组，则您可以使用**覆盖**字段覆盖该覆盖范围组设置。</span><span class="sxs-lookup"><span data-stu-id="f81d8-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="f81d8-118">**物料覆盖范围**页上的覆盖范围设置优先于**覆盖范围组**页上的设置。</span><span class="sxs-lookup"><span data-stu-id="f81d8-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="f81d8-119">使用向导为产品指定覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="f81d8-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="f81d8-120">该向导为设置主物料覆盖范围参数提供分步指导。</span><span class="sxs-lookup"><span data-stu-id="f81d8-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="f81d8-121">在**物料覆盖范围**页上，单击**向导**打开**物料覆盖范围向导**。</span><span class="sxs-lookup"><span data-stu-id="f81d8-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="f81d8-122">为维度组指定覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="f81d8-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="f81d8-123">单击**产品信息管理 &gt; 通用 &gt; 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="f81d8-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="f81d8-124">在**已发布产品详细信息**页上，在**常规**选项卡上，在**管理**组中，单击**存储维度组**链接。</span><span class="sxs-lookup"><span data-stu-id="f81d8-124">On the **Released product detail** page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="f81d8-125">在**存储维度组**页，选择**按维度的覆盖范围计划**字段为存储维度组中的维度创建覆盖范围设置。</span><span class="sxs-lookup"><span data-stu-id="f81d8-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="f81d8-126">所有产品维度，例如配置、颜色、尺寸、样式，必须选择**按维度的覆盖范围计划**字段。</span><span class="sxs-lookup"><span data-stu-id="f81d8-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="additional-resources"></a><span data-ttu-id="f81d8-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="f81d8-127">Additional resources</span></span>
--------

[<span data-ttu-id="f81d8-128">主计划</span><span class="sxs-lookup"><span data-stu-id="f81d8-128">Master plans</span></span>](master-plans.md)




