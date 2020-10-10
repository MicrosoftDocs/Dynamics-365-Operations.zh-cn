---
title: 选择退出个性化产品建议
description: 本主题说明如何在 Microsoft Dynamics 365 Commerce 中让客户选择不接收个性化建议。
author: bebeale
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6a64b45e1326673dd84c3c705491c9c100cdd069
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817515"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="d438e-103">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="d438e-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d438e-104">本主题说明如何在 Microsoft Dynamics 365 Commerce 中让客户选择不接收个性化建议。</span><span class="sxs-lookup"><span data-stu-id="d438e-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d438e-105">概览</span><span class="sxs-lookup"><span data-stu-id="d438e-105">Overview</span></span>

<span data-ttu-id="d438e-106">在创建帐户期间，会自动将新客户设置为接收个性化建议。</span><span class="sxs-lookup"><span data-stu-id="d438e-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="d438e-107">但是，Dynamics 365 Commerce 为零售商提供了各种方式，可以让用户可以选择不接收这些建议并限制其对个人数据的处理。</span><span class="sxs-lookup"><span data-stu-id="d438e-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="d438e-108">选择不接收个性化建议的经过身份验证的用户会立即无法查看个性化列表。</span><span class="sxs-lookup"><span data-stu-id="d438e-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="d438e-109">而且，将从个性化建议模型中删除为个性化收集的所有个人数据。</span><span class="sxs-lookup"><span data-stu-id="d438e-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="d438e-110">有关个性化产品建议的详细信息，请参阅[启用个性化建议](personalized-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="d438e-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="d438e-111">零售商实现退出体验的方法</span><span class="sxs-lookup"><span data-stu-id="d438e-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="d438e-112">零售商可以通过三种方法实现退出体验。</span><span class="sxs-lookup"><span data-stu-id="d438e-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="d438e-113">代表用户退出</span><span class="sxs-lookup"><span data-stu-id="d438e-113">Opting out on behalf of users</span></span>

<span data-ttu-id="d438e-114">在 Commerce 后端的“帐户管理”中，零售商可以代表用户选择退出。</span><span class="sxs-lookup"><span data-stu-id="d438e-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="d438e-115">在后端主页上搜索**所有客户**。</span><span class="sxs-lookup"><span data-stu-id="d438e-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="d438e-116">搜索并选择一个客户，然后选择**零售**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="d438e-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![“零售”快速选项卡](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="d438e-118">在**隐私**下，将**禁用个性化设置**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="d438e-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![隐私设置](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="d438e-120">选择**保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="d438e-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="d438e-121">基于模块的退出体验</span><span class="sxs-lookup"><span data-stu-id="d438e-121">Module-based opt-out experience</span></span>

<span data-ttu-id="d438e-122">零售商可以让经过身份验证的用户自己选择退出个性化建议。</span><span class="sxs-lookup"><span data-stu-id="d438e-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="d438e-123">要提供这种退出体验，请将用户退出模块添加到客户帐户的个人资料页面。</span><span class="sxs-lookup"><span data-stu-id="d438e-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="d438e-124">自定义扩展</span><span class="sxs-lookup"><span data-stu-id="d438e-124">Custom extensions</span></span>

<span data-ttu-id="d438e-125">零售商可以创建自己的扩展来管理用户的退出体验。</span><span class="sxs-lookup"><span data-stu-id="d438e-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="d438e-126">有关详细信息，请参阅[调用 Retail Server API](e-commerce-extensibility/call-retail-server-apis.md) 和[在线渠道可扩展性](e-commerce-extensibility/overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d438e-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="d438e-127">代表经过身份验证的用户获取个性化建议数据的数字副本</span><span class="sxs-lookup"><span data-stu-id="d438e-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="d438e-128">客户可能希望获取其个人数据的数字副本，并且还希望查看其建议结果的导出视图。</span><span class="sxs-lookup"><span data-stu-id="d438e-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="d438e-129">如果客户请求此信息，零售商必须创建一个自定义的扩展，来调用 Retail Server 应用程序编程接口 (API)，以基于客户的客户 ID 从**为您推荐**列表中查询完整结果。</span><span class="sxs-lookup"><span data-stu-id="d438e-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="d438e-130">然后可以将结果以逗号分隔值 (CSV) 格式导出并与客户共享。</span><span class="sxs-lookup"><span data-stu-id="d438e-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="d438e-131">以下示例显示零售商如何完成此任务。</span><span class="sxs-lookup"><span data-stu-id="d438e-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="d438e-132">零售商创建自定义扩展来代表用户提取个人建议数据。</span><span class="sxs-lookup"><span data-stu-id="d438e-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="d438e-133">有关如何创建模块、克隆现有模块，调用 Retail Server API 和调用数据操作的信息，请参阅[在线渠道可扩展性](e-commerce-extensibility/overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d438e-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="d438e-134">自定义扩展对 **get-recommendations** 核心数据操作进行调用，然后根据列表的要求将所需信息传递给它。</span><span class="sxs-lookup"><span data-stu-id="d438e-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="d438e-135">如果是**为您推荐**列表，扩展必须将正确的列表名称和客户 ID 传递给此数据操作。</span><span class="sxs-lookup"><span data-stu-id="d438e-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="d438e-136">创建自定义扩展的一种方法是克隆现有的用于返回建议结果的产品集合模块。</span><span class="sxs-lookup"><span data-stu-id="d438e-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="d438e-137">通过克隆此现有模块，零售商可以修改现有代码并添加新按钮，以将建议结果导出到 CSV 文件。</span><span class="sxs-lookup"><span data-stu-id="d438e-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="d438e-138">有关详细信息，请参阅[克隆模块库模块](e-commerce-extensibility/clone-starter-module.md)和[产品集合模块](product-collection-module-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d438e-138">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="d438e-139">有关 Retail Server API 库的完整视图，请参见 [Retail Server 客户和用户 API](dev-itpro/retail-server-customer-consumer-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d438e-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="d438e-140">创建自定义扩展后，零售商可以根据经过身份验证的用户的唯一客户 ID 导出所有建议结果的 CSV 文件。</span><span class="sxs-lookup"><span data-stu-id="d438e-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="d438e-141">零售商可以与经过身份验证的用户共享导出的包含建议产品完整的个性化列表的 CSV 文件。</span><span class="sxs-lookup"><span data-stu-id="d438e-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d438e-142">其他资源</span><span class="sxs-lookup"><span data-stu-id="d438e-142">Additional resources</span></span>

[<span data-ttu-id="d438e-143">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="d438e-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d438e-144">在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="d438e-144">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d438e-145">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="d438e-145">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d438e-146">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="d438e-146">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d438e-147">启用“购买类似外观”建议</span><span class="sxs-lookup"><span data-stu-id="d438e-147">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="d438e-148">在 POS 上添加产品建议</span><span class="sxs-lookup"><span data-stu-id="d438e-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d438e-149">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="d438e-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d438e-150">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="d438e-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d438e-151">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="d438e-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d438e-152">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="d438e-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d438e-153">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="d438e-153">Product recommendations FAQ</span></span>](faq-recommendations.md)
