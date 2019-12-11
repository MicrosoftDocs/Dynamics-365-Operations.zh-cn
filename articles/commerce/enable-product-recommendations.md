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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770131"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="88774-103">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="88774-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="88774-104">此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。</span><span class="sxs-lookup"><span data-stu-id="88774-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="88774-105">有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="88774-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="88774-106">预检查建议</span><span class="sxs-lookup"><span data-stu-id="88774-106">Recommendations pre-check</span></span>
<span data-ttu-id="88774-107">启用之前，请注意，只有支持版本 10.0.6 的 F&O 客户才支持产品建议，并且这些产品建议已将存储迁移到使用 BDL。</span><span class="sxs-lookup"><span data-stu-id="88774-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="88774-108">此外，请确保已启用 RetailSale 度量。</span><span class="sxs-lookup"><span data-stu-id="88774-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="88774-109">若要详细了解此设置流程，请转到[此处](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)。</span><span class="sxs-lookup"><span data-stu-id="88774-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="88774-110">开启建议</span><span class="sxs-lookup"><span data-stu-id="88774-110">Turn on recommendations</span></span>

<span data-ttu-id="88774-111">若要开启产品建议，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="88774-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="88774-112">转到 **Retail** &gt; **产品建议** &gt; **建议参数**。</span><span class="sxs-lookup"><span data-stu-id="88774-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="88774-113">在零售共享参数列表中，选择**建议列表**。</span><span class="sxs-lookup"><span data-stu-id="88774-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="88774-114">将**启用建议**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="88774-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![启用产品建议](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="88774-116">此过程开始生成产品建议列表。</span><span class="sxs-lookup"><span data-stu-id="88774-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="88774-117">最多可能需要多个小时，列表才可用，并且可以在销售点 (POS) 或 Dynamics 365 for Commerce 中查看。</span><span class="sxs-lookup"><span data-stu-id="88774-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="88774-118">配置建议列表参数</span><span class="sxs-lookup"><span data-stu-id="88774-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="88774-119">默认情况下，基于 AI-ML 的产品建议列表提供建议的值。</span><span class="sxs-lookup"><span data-stu-id="88774-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="88774-120">可更改默认建议值以适合业务流程。</span><span class="sxs-lookup"><span data-stu-id="88774-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="88774-121">若要详细了解如何更改默认参数，请转到[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="88774-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="88774-122">在 POS 设备中显示建议</span><span class="sxs-lookup"><span data-stu-id="88774-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="88774-123">在后端启用建议之后，必须通过布局工具将建议面板添加到控制 POS 屏幕中。</span><span class="sxs-lookup"><span data-stu-id="88774-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="88774-124">若要了解此流程，请转到[此处](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)。</span><span class="sxs-lookup"><span data-stu-id="88774-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="88774-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="88774-125">Additional resources</span></span>

[<span data-ttu-id="88774-126">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="88774-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="88774-127">向页面添加建议列表</span><span class="sxs-lookup"><span data-stu-id="88774-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="88774-128">向 POS 设备添加建议面板</span><span class="sxs-lookup"><span data-stu-id="88774-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


