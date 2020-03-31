---
title: 在 Dynamics 365 Commerce 环境中启用 ADLS
description: 本主题说明如何针对 Dynamics 365 Commerce 环境启用和测试 Azure Data Lake Storage (ADLS)，这是启用产品推荐的先决条件。
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: 553e1512ba72559923403eef741ce08222172a09
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127759"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="e7855-103">在 Dynamics 365 Commerce 环境中启用 ADLS</span><span class="sxs-lookup"><span data-stu-id="e7855-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7855-104">本主题说明如何针对 Dynamics 365 Commerce 环境启用和测试 Azure Data Lake Storage (ADLS)，这是启用产品推荐的先决条件。</span><span class="sxs-lookup"><span data-stu-id="e7855-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="e7855-105">概览</span><span class="sxs-lookup"><span data-stu-id="e7855-105">Overview</span></span>

<span data-ttu-id="e7855-106">在 Dynamics 365 Commerce 解决方案中，所有产品和交易信息都在环境的实体商店中进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="e7855-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="e7855-107">为了使此数据可供其他 Dynamics 365 服务（例如数据分析、商业智能和个性化建议）访问，必须将环境连接到客户拥有的 Azure Data Lake Storage 第 2 代 (ADLS) 解决方案。</span><span class="sxs-lookup"><span data-stu-id="e7855-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="e7855-108">由于在环境中配置了 ADLS，因此从实体商店中镜像了所有必需的数据，同时仍受到保护并在客户的控制之下。</span><span class="sxs-lookup"><span data-stu-id="e7855-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="e7855-109">如果在环境中也启用了产品推荐或个性化推荐，则将向产品推荐堆栈授予 ADLS 中专用文件夹的访问权限，以检索客户的数据并基于该数据计算推荐。</span><span class="sxs-lookup"><span data-stu-id="e7855-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e7855-110">先决条件</span><span class="sxs-lookup"><span data-stu-id="e7855-110">Prerequisites</span></span>

<span data-ttu-id="e7855-111">客户需要在其拥有的 Azure 订阅中配置 ADLS。</span><span class="sxs-lookup"><span data-stu-id="e7855-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="e7855-112">本主题不涉及购买 Azure 订阅或设置启用 ADLS 的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="e7855-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="e7855-113">有关 ADLS 的详细信息，请参阅 [ADLS 官方文档](https://azure.microsoft.com/pricing/details/storage/data-lake)。</span><span class="sxs-lookup"><span data-stu-id="e7855-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="e7855-114">配置步骤</span><span class="sxs-lookup"><span data-stu-id="e7855-114">Configuration steps</span></span>

<span data-ttu-id="e7855-115">本节介绍在环境中启用 ADLS 所需的配置步骤。</span><span class="sxs-lookup"><span data-stu-id="e7855-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="e7855-116">在环境中启用 ADLS</span><span class="sxs-lookup"><span data-stu-id="e7855-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="e7855-117">登录到环境的后台办公室门户。</span><span class="sxs-lookup"><span data-stu-id="e7855-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="e7855-118">搜索**系统参数**并导航到**数据连接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="e7855-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="e7855-119">将**启用 Data Lake 集成**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e7855-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="e7855-120">将**缓慢更新 Data Lake** 设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e7855-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="e7855-121">然后，输入以下必需信息：</span><span class="sxs-lookup"><span data-stu-id="e7855-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="e7855-122">**应用程序 ID** // **应用程序密钥** // **DNS 名称** - 需要连接到存储 ADLS 密钥的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e7855-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="e7855-123">**密钥名称** - 密钥名称存储在 KeyVault 中，用于通过 ADLS 进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="e7855-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="e7855-124">将更改保存在页面的左上角。</span><span class="sxs-lookup"><span data-stu-id="e7855-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="e7855-125">下图显示了一个 ADLS 配置示例。</span><span class="sxs-lookup"><span data-stu-id="e7855-125">The following image shows an example ADLS configuration.</span></span>

![ADLS 配置示例](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="e7855-127">测试 ADLS 连接</span><span class="sxs-lookup"><span data-stu-id="e7855-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="e7855-128">使用**测试 Azure 密钥保管库**链接测试与 KeyVault 的连接。</span><span class="sxs-lookup"><span data-stu-id="e7855-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="e7855-129">使用**测试 Azure 存储**链接测试与 ADLS 的连接。</span><span class="sxs-lookup"><span data-stu-id="e7855-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="e7855-130">如果测试失败，请仔细检查上面添加的所有 KeyVault 信息是否正确，然后重试。</span><span class="sxs-lookup"><span data-stu-id="e7855-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="e7855-131">连接测试成功后，必须为实体商店启用自动刷新。</span><span class="sxs-lookup"><span data-stu-id="e7855-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="e7855-132">要为实体商店启用自动刷新，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e7855-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="e7855-133">搜索**实体商店**。</span><span class="sxs-lookup"><span data-stu-id="e7855-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="e7855-134">在左侧列表中，导航到 **RetailSales** 条目，然后选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="e7855-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="e7855-135">确保**启用自动刷新**设定为**是**，选择**刷新**，然后选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="e7855-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="e7855-136">下图显示了启用了自动刷新的实体商店的示例。</span><span class="sxs-lookup"><span data-stu-id="e7855-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![启用了自动刷新的实体商店示例](./media/exampleADLSConfig2.png)

<span data-ttu-id="e7855-138">现在为环境配置了 ADLS。</span><span class="sxs-lookup"><span data-stu-id="e7855-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="e7855-139">如果尚未完成，请按照以下步骤为环境[配置产品推荐和个性化设置](enable-product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="e7855-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7855-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="e7855-140">Additional resources</span></span>

[<span data-ttu-id="e7855-141">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="e7855-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e7855-142">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="e7855-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="e7855-143">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="e7855-143">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="e7855-144">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="e7855-144">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="e7855-145">向电子商务站点添加建议列表</span><span class="sxs-lookup"><span data-stu-id="e7855-145">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="e7855-146">在 POS 中添加产品建议</span><span class="sxs-lookup"><span data-stu-id="e7855-146">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e7855-147">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="e7855-147">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="e7855-148">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="e7855-148">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="e7855-149">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="e7855-149">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="e7855-150">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="e7855-150">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="e7855-151">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="e7855-151">Product recommendations FAQ</span></span>](faq-recommendations.md)

