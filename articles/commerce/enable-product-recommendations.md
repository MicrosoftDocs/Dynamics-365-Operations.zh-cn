---
title: 启用产品建议
description: 此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: d2dacd4a94f706be5aa65947c0b6a92e281733ca
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665018"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="622bd-103">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="622bd-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="622bd-104">此主题介绍如何做出基于 Microsoft Dynamics 365 Commerce 客户可用的人工智能-机器学习 (AI-ML) 的产品建议。</span><span class="sxs-lookup"><span data-stu-id="622bd-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="622bd-105">有关产品建议列表的详细信息，请参阅[产品建议概述](product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="622bd-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="622bd-106">预检查建议</span><span class="sxs-lookup"><span data-stu-id="622bd-106">Recommendations pre-check</span></span>

<span data-ttu-id="622bd-107">启用之前，请注意，仅对已将存储过渡为使用 Azure Data Lake Storage 的 Commerce 客户支持产品推荐。</span><span class="sxs-lookup"><span data-stu-id="622bd-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="622bd-108">启用建议前，必须先在后端启用以下配置：</span><span class="sxs-lookup"><span data-stu-id="622bd-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="622bd-109">确保已购买 Azure Data Lake Storage 并已在环境中成功验证。</span><span class="sxs-lookup"><span data-stu-id="622bd-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="622bd-110">有关详细信息，请参阅[确保已购买 Azure Data Lake Storage 并已在环境中成功验证](enable-ADLS-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="622bd-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="622bd-111">确保实体存储刷新已自动化。</span><span class="sxs-lookup"><span data-stu-id="622bd-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="622bd-112">有关更多信息，请参阅[确保实体存储刷新已自动化](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)。</span><span class="sxs-lookup"><span data-stu-id="622bd-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="622bd-113">确认 Azure AD 标识配置中包含建议的实体。</span><span class="sxs-lookup"><span data-stu-id="622bd-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="622bd-114">下面是有关如何执行此操作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="622bd-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="622bd-115">此外，请确保已启用 RetailSale 度量。</span><span class="sxs-lookup"><span data-stu-id="622bd-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="622bd-116">若要详细了解此设置流程，请参阅[使用度量](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)。</span><span class="sxs-lookup"><span data-stu-id="622bd-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="622bd-117">Azure AD 标识配置</span><span class="sxs-lookup"><span data-stu-id="622bd-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="622bd-118">运行服务架构 (IaaS) 配置的所有客户都需要执行此步骤。</span><span class="sxs-lookup"><span data-stu-id="622bd-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="622bd-119">对于运行 Service Fabric (SF) 的客户，此步骤应该是自动步骤，我们建议您验证配置的设置是否正确。</span><span class="sxs-lookup"><span data-stu-id="622bd-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="622bd-120">设置</span><span class="sxs-lookup"><span data-stu-id="622bd-120">Setup</span></span>

1. <span data-ttu-id="622bd-121">从后端搜索 **Azure Active Directory 应用程序**页面。</span><span class="sxs-lookup"><span data-stu-id="622bd-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="622bd-122">验证是否有“RecommendationSystemApplication-1”的条目。</span><span class="sxs-lookup"><span data-stu-id="622bd-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="622bd-123">如果该条目不存在，请添加具有以下信息的新条目：</span><span class="sxs-lookup"><span data-stu-id="622bd-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="622bd-124">**客户端 ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="622bd-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="622bd-125">**名称** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="622bd-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="622bd-126">**用户 ID** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="622bd-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="622bd-127">保存并关闭页面。</span><span class="sxs-lookup"><span data-stu-id="622bd-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="622bd-128">开启建议</span><span class="sxs-lookup"><span data-stu-id="622bd-128">Turn on recommendations</span></span>

<span data-ttu-id="622bd-129">若要开启产品建议，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="622bd-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="622bd-130">转到 **Retail 和 Commerce &gt; 产品建议 &gt; 建议参数**。</span><span class="sxs-lookup"><span data-stu-id="622bd-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="622bd-131">在共享参数列表中，选择**建议列表**。</span><span class="sxs-lookup"><span data-stu-id="622bd-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="622bd-132">将**启用建议**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="622bd-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![开启建议](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="622bd-134">此过程开始生成产品建议列表。</span><span class="sxs-lookup"><span data-stu-id="622bd-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="622bd-135">可能需要几小时，列表才可用，并且可以在销售点 (POS) 或 Dynamics 365 Commerce 中查看。</span><span class="sxs-lookup"><span data-stu-id="622bd-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="622bd-136">配置建议列表参数</span><span class="sxs-lookup"><span data-stu-id="622bd-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="622bd-137">默认情况下，基于 AI-ML 的产品建议列表提供建议的值。</span><span class="sxs-lookup"><span data-stu-id="622bd-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="622bd-138">可更改默认建议值以适合业务流程。</span><span class="sxs-lookup"><span data-stu-id="622bd-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="622bd-139">若要详细了解如何更改默认参数，请转到[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="622bd-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="622bd-140">在 POS 设备中显示建议</span><span class="sxs-lookup"><span data-stu-id="622bd-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="622bd-141">在 Commerce 后端启用建议之后，必须使用布局工具将建议面板添加到控制 POS 屏幕中。</span><span class="sxs-lookup"><span data-stu-id="622bd-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="622bd-142">要了解此过程，请参阅[向 POS 设备上的交易屏幕添加建议控件](add-recommendations-control-pos-screen.md)。</span><span class="sxs-lookup"><span data-stu-id="622bd-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="622bd-143">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="622bd-143">Enable personalized recommendations</span></span>

<span data-ttu-id="622bd-144">在 Dynamics 365 Commerce 中，零售商可以提供个性化的产品建议（也称为个性化）。</span><span class="sxs-lookup"><span data-stu-id="622bd-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="622bd-145">通过这种方式，可以将个性化的建议引入到在线和销售点的客户体验中。</span><span class="sxs-lookup"><span data-stu-id="622bd-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="622bd-146">当个性化功能打开时，系统可以将用户的购买和产品信息相关联，以生成个性化的产品建议。</span><span class="sxs-lookup"><span data-stu-id="622bd-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="622bd-147">若要详细了解个性化推荐，请参阅[启用个性化建议](personalized-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="622bd-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="622bd-148">其他资源</span><span class="sxs-lookup"><span data-stu-id="622bd-148">Additional resources</span></span>

[<span data-ttu-id="622bd-149">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="622bd-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="622bd-150">在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="622bd-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="622bd-151">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="622bd-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="622bd-152">启用“购买类似外观”建议</span><span class="sxs-lookup"><span data-stu-id="622bd-152">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="622bd-153">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="622bd-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="622bd-154">在 POS 中添加产品建议</span><span class="sxs-lookup"><span data-stu-id="622bd-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="622bd-155">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="622bd-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="622bd-156">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="622bd-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="622bd-157">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="622bd-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="622bd-158">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="622bd-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="622bd-159">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="622bd-159">Product recommendations FAQ</span></span>](faq-recommendations.md)

