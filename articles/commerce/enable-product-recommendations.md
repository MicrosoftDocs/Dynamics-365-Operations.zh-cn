---
title: 启用产品建议
description: 此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127874"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="13991-103">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="13991-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13991-104">此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。</span><span class="sxs-lookup"><span data-stu-id="13991-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="13991-105">有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="13991-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="13991-106">预检查建议</span><span class="sxs-lookup"><span data-stu-id="13991-106">Recommendations pre-check</span></span>

<span data-ttu-id="13991-107">启用之前，请注意，仅对已将存储过渡为使用 Azure Data Lake Storage (ADLS) 的 Commerce 客户支持产品推荐。</span><span class="sxs-lookup"><span data-stu-id="13991-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="13991-108">有关启用 ADLS 的步骤，请参见[如何在 Dynamics 365 环境中启用 ADLS](enable-ADLS-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="13991-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="13991-109">此外，请确保已启用 RetailSale 度量。</span><span class="sxs-lookup"><span data-stu-id="13991-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="13991-110">若要详细了解此设置流程，请转到[此处](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)。</span><span class="sxs-lookup"><span data-stu-id="13991-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="13991-111">开启建议</span><span class="sxs-lookup"><span data-stu-id="13991-111">Turn on recommendations</span></span>

<span data-ttu-id="13991-112">若要开启产品建议，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="13991-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="13991-113">转到 **Retail 和 Commerce &gt; 产品建议 &gt; 建议参数**。</span><span class="sxs-lookup"><span data-stu-id="13991-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="13991-114">在共享参数列表中，选择**建议列表**。</span><span class="sxs-lookup"><span data-stu-id="13991-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="13991-115">将**启用建议**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="13991-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![启用产品建议](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="13991-117">此过程开始生成产品建议列表。</span><span class="sxs-lookup"><span data-stu-id="13991-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="13991-118">最多可能需要多个小时，列表才可用，并且可以在销售点 (POS) 或 Dynamics 365 Commerce 中查看。</span><span class="sxs-lookup"><span data-stu-id="13991-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="13991-119">配置建议列表参数</span><span class="sxs-lookup"><span data-stu-id="13991-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="13991-120">默认情况下，基于 AI-ML 的产品建议列表提供建议的值。</span><span class="sxs-lookup"><span data-stu-id="13991-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="13991-121">可更改默认建议值以适合业务流程。</span><span class="sxs-lookup"><span data-stu-id="13991-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="13991-122">若要详细了解如何更改默认参数，请转到[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="13991-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="13991-123">在 POS 设备中显示建议</span><span class="sxs-lookup"><span data-stu-id="13991-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="13991-124">在 Commerce 后端启用建议之后，必须使用布局工具将建议面板添加到控制 POS 屏幕中。</span><span class="sxs-lookup"><span data-stu-id="13991-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="13991-125">要了解此过程，请参阅[向 POS 设备上的交易屏幕添加建议控件](add-recommendations-control-pos-screen.md)。</span><span class="sxs-lookup"><span data-stu-id="13991-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="13991-126">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="13991-126">Enable personalized recommendations</span></span>

<span data-ttu-id="13991-127">要了解有关如何接收个性化推荐的更多信息，请参见[启用个性化建议](personalized-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="13991-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13991-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="13991-128">Additional resources</span></span>

[<span data-ttu-id="13991-129">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="13991-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="13991-130">在 Dynamics 365 Commerce 环境中启用 ADLS</span><span class="sxs-lookup"><span data-stu-id="13991-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="13991-131">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="13991-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="13991-132">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="13991-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="13991-133">向电子商务站点添加建议列表</span><span class="sxs-lookup"><span data-stu-id="13991-133">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="13991-134">在 POS 中添加产品建议</span><span class="sxs-lookup"><span data-stu-id="13991-134">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="13991-135">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="13991-135">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="13991-136">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="13991-136">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="13991-137">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="13991-137">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="13991-138">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="13991-138">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="13991-139">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="13991-139">Product recommendations FAQ</span></span>](faq-recommendations.md)

