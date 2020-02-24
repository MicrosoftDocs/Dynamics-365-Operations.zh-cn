---
title: 启用产品建议
description: 此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024948"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="0c763-103">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="0c763-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c763-104">此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。</span><span class="sxs-lookup"><span data-stu-id="0c763-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="0c763-105">有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="0c763-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="0c763-106">预检查建议</span><span class="sxs-lookup"><span data-stu-id="0c763-106">Recommendations pre-check</span></span>

<span data-ttu-id="0c763-107">启用之前，请注意，仅对已将存储过渡为使用 Azure Data Lake Storage (ADLS) 的 Commerce 客户支持产品推荐。</span><span class="sxs-lookup"><span data-stu-id="0c763-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="0c763-108">有关启用 ADLS 的步骤，请参见[如何在 Dynamics 365 环境中启用 ADLS](enable-ADLS-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="0c763-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="0c763-109">此外，请确保已启用 RetailSale 度量。</span><span class="sxs-lookup"><span data-stu-id="0c763-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="0c763-110">若要详细了解此设置流程，请转到[此处](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)。</span><span class="sxs-lookup"><span data-stu-id="0c763-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="0c763-111">开启建议</span><span class="sxs-lookup"><span data-stu-id="0c763-111">Turn on recommendations</span></span>

<span data-ttu-id="0c763-112">若要开启产品建议，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="0c763-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="0c763-113">转到 **Retail 和 Commerce &gt; 产品建议 &gt; 建议参数**。</span><span class="sxs-lookup"><span data-stu-id="0c763-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="0c763-114">在共享参数列表中，选择**建议列表**。</span><span class="sxs-lookup"><span data-stu-id="0c763-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="0c763-115">将**启用建议**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="0c763-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![启用产品建议](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="0c763-117">此过程开始生成产品建议列表。</span><span class="sxs-lookup"><span data-stu-id="0c763-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="0c763-118">最多可能需要多个小时，列表才可用，并且可以在销售点 (POS) 或 Dynamics 365 Commerce 中查看。</span><span class="sxs-lookup"><span data-stu-id="0c763-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="0c763-119">配置建议列表参数</span><span class="sxs-lookup"><span data-stu-id="0c763-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="0c763-120">默认情况下，基于 AI-ML 的产品建议列表提供建议的值。</span><span class="sxs-lookup"><span data-stu-id="0c763-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="0c763-121">可更改默认建议值以适合业务流程。</span><span class="sxs-lookup"><span data-stu-id="0c763-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="0c763-122">若要详细了解如何更改默认参数，请转到[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="0c763-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="0c763-123">在 POS 设备中显示建议</span><span class="sxs-lookup"><span data-stu-id="0c763-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="0c763-124">在 Commerce 后端启用建议之后，必须使用布局工具将建议面板添加到控制 POS 屏幕中。</span><span class="sxs-lookup"><span data-stu-id="0c763-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="0c763-125">要了解此过程，请参阅[向 POS 设备上的交易屏幕添加建议控件](add-recommendations-control-pos-screen.md)。</span><span class="sxs-lookup"><span data-stu-id="0c763-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="0c763-126">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="0c763-126">Enable personalized recommendations</span></span>

<span data-ttu-id="0c763-127">要了解有关如何接收个性化推荐的更多信息，请参见[启用个性化建议](personalized-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="0c763-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c763-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="0c763-128">Additional resources</span></span>

[<span data-ttu-id="0c763-129">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="0c763-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="0c763-130">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="0c763-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="0c763-131">向页面添加建议列表</span><span class="sxs-lookup"><span data-stu-id="0c763-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="0c763-132">向 POS 设备添加建议面板</span><span class="sxs-lookup"><span data-stu-id="0c763-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="0c763-133">产品集合模块概览</span><span class="sxs-lookup"><span data-stu-id="0c763-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="0c763-134">在 Dynamics 365 环境中启用 ADLS</span><span class="sxs-lookup"><span data-stu-id="0c763-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

