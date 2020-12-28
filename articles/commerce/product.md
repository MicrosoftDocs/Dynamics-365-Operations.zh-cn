---
title: 在 POS 中添加产品建议
description: 本主题介绍如何在销售点 (POS) 设备上使用产品建议。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7afe9225b8fc966ca154a5eb7421e8d4cc7c3023
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410596"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="48a92-103">在 POS 中添加产品建议</span><span class="sxs-lookup"><span data-stu-id="48a92-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="48a92-104">产品建议的核心是一个革命性的业务应用程序，该应用程序适用于所有商务领域，可以带来丰富、参与度高、度身定制的产品发现体验。</span><span class="sxs-lookup"><span data-stu-id="48a92-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="48a92-105">若要在 POS 上实施此功能，请执行[如何向 POS 设备添加建议](add-recommendations-control-pos-screen.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="48a92-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="48a92-106">有关产品建议功能的详细信息，请参阅[产品建议概述](../commerce/product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="48a92-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="48a92-107">方案</span><span class="sxs-lookup"><span data-stu-id="48a92-107">Scenarios</span></span>

<span data-ttu-id="48a92-108">将为以下 POS 方案启用产品建议。</span><span class="sxs-lookup"><span data-stu-id="48a92-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="48a92-109">Cloud POS 或 Modern POS (MPOS) 中支持产品建议。</span><span class="sxs-lookup"><span data-stu-id="48a92-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="48a92-110">在 **产品详细信息** 页面中：</span><span class="sxs-lookup"><span data-stu-id="48a92-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="48a92-111">如果售货员在查看跨不同渠道的早期交易记录时访问 **产品详细信息** 页面，建议服务将推荐更多可能搭配购买的物料。</span><span class="sxs-lookup"><span data-stu-id="48a92-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="48a92-112">[![有关“产品详细信息”页的建议](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="48a92-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="48a92-113">在 **交易记录** 页面中：</span><span class="sxs-lookup"><span data-stu-id="48a92-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="48a92-114">建议引擎根据购物车中经常一起购买的物料的完整列表推荐物料。</span><span class="sxs-lookup"><span data-stu-id="48a92-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="48a92-115">若要在 **交易记录** 页面中显示建议，零售商需要更新 Dynamics 365 Commerce 中的屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="48a92-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="48a92-116">必须将 **建议** 控件拖到 **交易记录** 页面中。</span><span class="sxs-lookup"><span data-stu-id="48a92-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="48a92-117">[![有关“交易记录”页的建议](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="48a92-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="48a92-118">配置 Commerce 以启用 POS 建议</span><span class="sxs-lookup"><span data-stu-id="48a92-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="48a92-119">要设置产品建议，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="48a92-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="48a92-120">确保设备已更新为 **10.0.6 build**。</span><span class="sxs-lookup"><span data-stu-id="48a92-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="48a92-121">按照有关如何为企业[启用产品建议](../commerce/enable-product-recommendations.md)的说明操作。</span><span class="sxs-lookup"><span data-stu-id="48a92-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="48a92-122">可选：若要在交易记录屏幕中显示建议，请转至 **屏幕布局**，选择您的屏幕布局，启动 **屏幕布局设计器**，然后将 **建议** 控件拖到所需位置。</span><span class="sxs-lookup"><span data-stu-id="48a92-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="48a92-123">转至 **商业参数**，选择 **机器学习**，然后在 **启用 POS 建议** 下选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="48a92-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="48a92-124">若要在 POS 中查看建议，请运行全局配置作业 **1110**。</span><span class="sxs-lookup"><span data-stu-id="48a92-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="48a92-125">若要体现对 POS 屏幕布局设计器所做更改，请运行渠道配置作业 **1070**。</span><span class="sxs-lookup"><span data-stu-id="48a92-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="48a92-126">排除您已启用了产品建议时遇到的问题</span><span class="sxs-lookup"><span data-stu-id="48a92-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="48a92-127">导航到 **商业参数** \> **建议列表** \> **禁用产品建议**，然后运行 **全局配置作业 \[9999\]**。</span><span class="sxs-lookup"><span data-stu-id="48a92-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="48a92-128">如果使用 **屏幕布局设计器** 为交易记录屏幕添加了 **建议控件**，请将其一并移除。</span><span class="sxs-lookup"><span data-stu-id="48a92-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="48a92-129">如果还有其他问题，请参阅[产品建议常见问题](../commerce/faq-recommendations.md)获取详细信息。</span><span class="sxs-lookup"><span data-stu-id="48a92-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48a92-130">其他资源</span><span class="sxs-lookup"><span data-stu-id="48a92-130">Additional resources</span></span>

[<span data-ttu-id="48a92-131">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="48a92-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="48a92-132">在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="48a92-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="48a92-133">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="48a92-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="48a92-134">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="48a92-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="48a92-135">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="48a92-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="48a92-136">启用“购买类似外观”建议</span><span class="sxs-lookup"><span data-stu-id="48a92-136">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="48a92-137">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="48a92-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="48a92-138">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="48a92-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="48a92-139">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="48a92-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="48a92-140">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="48a92-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="48a92-141">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="48a92-141">Product recommendations FAQ</span></span>](faq-recommendations.md)
