---
title: 在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage
description: 本主题说明如何针对 Dynamics 365 Commerce 环境启用和测试 Azure Data Lake Storage，这是启用产品推荐的先决条件。
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5887ae7983fd817a929a185327671b301808b354
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478228"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="a4ef1-103">在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="a4ef1-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4ef1-104">本主题说明如何针对 Dynamics 365 Commerce 环境启用和测试 Azure Data Lake Storage，这是启用产品推荐的先决条件。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

<span data-ttu-id="a4ef1-105">在 Dynamics 365 Commerce 解决方案中，所有产品和交易信息都在环境的实体商店中进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-105">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="a4ef1-106">为了使此数据可供其他 Dynamics 365 服务（例如数据分析、商业智能和个性化建议）访问，必须将环境连接到客户拥有的 Azure Data Lake Storage 第 2 代解决方案。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-106">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="a4ef1-107">由于在环境中配置了 Azure Data Lake Storage，因此从实体商店中镜像了所有必需的数据，同时仍受到保护并在客户的控制之下。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-107">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="a4ef1-108">如果在环境中也启用了产品推荐或个性化推荐，则将向产品推荐堆栈授予 Azure Data Lake Storage 中专用文件夹的访问权限，以检索客户的数据并基于该数据计算推荐。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-108">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a4ef1-109">先决条件</span><span class="sxs-lookup"><span data-stu-id="a4ef1-109">Prerequisites</span></span>

<span data-ttu-id="a4ef1-110">客户需要在其拥有的 Azure 订阅中配置 Azure Data Lake Storage。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-110">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="a4ef1-111">本主题不涉及购买 Azure 订阅或设置启用 Azure Data Lake Storage 的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-111">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="a4ef1-112">有关 Azure Data Lake Storage 的详细信息，请参阅 [Azure Data Lake Storage Gen2 官方文档](https://azure.microsoft.com/pricing/details/storage/data-lake)。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-112">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="a4ef1-113">配置步骤</span><span class="sxs-lookup"><span data-stu-id="a4ef1-113">Configuration steps</span></span>

<span data-ttu-id="a4ef1-114">此部分介绍在环境中启用 Azure Data Lake Storage（当其与产品建议有关时）需要执行的配置步骤。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-114">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="a4ef1-115">有关启用 Azure Data Lake Storage 需要执行的步骤的更深度概述，请参阅[将实体商店用作 Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-115">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="a4ef1-116">在环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="a4ef1-116">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="a4ef1-117">登录到环境的后台办公室门户。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="a4ef1-118">搜索 **系统参数** 并导航到 **数据连接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="a4ef1-119">将 **启用 Data Lake 集成** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="a4ef1-120">将 **缓慢更新 Data Lake** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="a4ef1-121">然后，输入以下必需信息：</span><span class="sxs-lookup"><span data-stu-id="a4ef1-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="a4ef1-122">**应用程序 ID** // **应用程序密钥** // **DNS 名称** - 需要连接到存储 ADLS 密钥的 Azure Data Lake Storage。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="a4ef1-123">**密钥名称** - 密钥名称存储在 KeyVault 中，用于通过 Azure Data Lake Storage 进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="a4ef1-124">将更改保存在页面的左上角。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="a4ef1-125">下图显示了一个 Azure Data Lake Storage 配置示例。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-125">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Azure Data Lake Storage 配置示例](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="a4ef1-127">测试 Azure Data Lake Storage 连接</span><span class="sxs-lookup"><span data-stu-id="a4ef1-127">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="a4ef1-128">使用 **测试 Azure 密钥保管库** 链接测试与 KeyVault 的连接。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="a4ef1-129">使用 **测试 Azure 存储** 链接测试与 Azure Data Lake Storage 的连接。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-129">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="a4ef1-130">如果测试失败，请仔细检查上面添加的所有 KeyVault 信息是否正确，然后重试。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="a4ef1-131">连接测试成功后，必须为实体商店启用自动刷新。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="a4ef1-132">要为实体商店启用自动刷新，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="a4ef1-133">搜索 **实体商店**。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="a4ef1-134">在左侧列表中，导航到 **RetailSales** 条目，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="a4ef1-135">确保 **启用自动刷新** 设定为 **是**，选择 **刷新**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="a4ef1-136">下图显示了启用了自动刷新的实体商店的示例。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![启用了自动刷新的实体商店示例](./media/exampleADLSConfig2.png)

<span data-ttu-id="a4ef1-138">现在为环境配置了 Azure Data Lake Storage。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-138">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="a4ef1-139">如果尚未完成，请按照以下步骤为环境[配置产品推荐和个性化设置](enable-product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="a4ef1-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4ef1-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="a4ef1-140">Additional resources</span></span>

[<span data-ttu-id="a4ef1-141">将实体商店用作 Data Lake</span><span class="sxs-lookup"><span data-stu-id="a4ef1-141">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="a4ef1-142">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="a4ef1-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a4ef1-143">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="a4ef1-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a4ef1-144">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="a4ef1-144">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a4ef1-145">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="a4ef1-145">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a4ef1-146">启用“购买类似外观”建议</span><span class="sxs-lookup"><span data-stu-id="a4ef1-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="a4ef1-147">在 POS 上添加产品建议</span><span class="sxs-lookup"><span data-stu-id="a4ef1-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a4ef1-148">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="a4ef1-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a4ef1-149">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="a4ef1-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a4ef1-150">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="a4ef1-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a4ef1-151">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="a4ef1-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a4ef1-152">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="a4ef1-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
