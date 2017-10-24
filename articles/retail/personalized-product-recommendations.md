---
title: "个性化产品建议概览"
description: "在 Dynamics 365 for Retail 中，可在销售点 (POS) 设备中显示产品建议。 建议是客户可能根据其购买历史记录感兴趣的商品、其愿望列表中的商品，以及其他客户在线商店和实体商店购买的商品。 对于目录丰富的零售商，建议可以帮助客户发现产品。 通过展示针对客户兴趣和购买习惯的产品，产品建议可以帮助零售商开展追加销售和交叉销售，以及增强客户的凝聚力。 在 Dynamics 365 for Retail 中，认知服务和 Microsoft Azure 机器学习为产品建议提供支持。"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d727718442f94a2a78a3864741e93439d7c36473
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="43620-107">个性化产品建议概览</span><span class="sxs-lookup"><span data-stu-id="43620-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="43620-108">此功能目前仅在沙盒和生产（高可用性）部署拓扑中可用。</span><span class="sxs-lookup"><span data-stu-id="43620-108">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="43620-109">在 Dynamics 365 for Retail 中，可在销售点 (POS) 设备中显示产品建议。</span><span class="sxs-lookup"><span data-stu-id="43620-109">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="43620-110">建议是客户可能根据其购买历史记录感兴趣的商品、其愿望列表中的商品，以及其他客户在线商店和实体商店购买的商品。</span><span class="sxs-lookup"><span data-stu-id="43620-110">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="43620-111">对于目录丰富的零售商，建议可以帮助客户发现产品。</span><span class="sxs-lookup"><span data-stu-id="43620-111">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="43620-112">通过展示针对客户兴趣和购买习惯的产品，产品建议可以帮助零售商开展追加销售和交叉销售，以及增强客户的凝聚力。</span><span class="sxs-lookup"><span data-stu-id="43620-112">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="43620-113">在 Dynamics 365 for Retail 中，认知服务和 Microsoft Azure 机器学习为产品建议提供支持。</span><span class="sxs-lookup"><span data-stu-id="43620-113">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="43620-114">方案</span><span class="sxs-lookup"><span data-stu-id="43620-114">Scenarios</span></span>
---------

<span data-ttu-id="43620-115">将为以下 POS 方案启用产品建议。</span><span class="sxs-lookup"><span data-stu-id="43620-115">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="43620-116">Cloud POS 或 Modern POS (MPOS) 中支持产品建议。</span><span class="sxs-lookup"><span data-stu-id="43620-116">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="43620-117">在**产品详细信息**页面中：</span><span class="sxs-lookup"><span data-stu-id="43620-117">On the **Product details** page:</span></span>

-   <span data-ttu-id="43620-118">如果售货员在查看跨不同渠道的早期交易记录时访问**产品详细信息**页面，建议引擎将推荐更多可能搭配购买的物料。</span><span class="sxs-lookup"><span data-stu-id="43620-118">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="43620-119">如果售货员将客户添加到交易记录，然后访问**产品详细信息**页面，建议引擎将使用该客户的交易记录历史信息提供个性化建议。</span><span class="sxs-lookup"><span data-stu-id="43620-119">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="43620-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="43620-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="43620-121">在**交易记录**页面中：</span><span class="sxs-lookup"><span data-stu-id="43620-121">On the **Transaction** page:</span></span>

-   <span data-ttu-id="43620-122">建议引擎根据购物篮中的整个物料列表推荐物料。</span><span class="sxs-lookup"><span data-stu-id="43620-122">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="43620-123">如果售货员将客户添加到交易记录，建议引擎将使用该客户的交易记录历史信息和购物篮中的物料列表提供个人建议。</span><span class="sxs-lookup"><span data-stu-id="43620-123">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="43620-124">若要在**交易记录**页面中显示建议，零售商需要更新 Dynamics 365 for Retail 中的屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="43620-124">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="43620-125">必须将**建议**控件拖到**交易记录**页面中。</span><span class="sxs-lookup"><span data-stu-id="43620-125">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="43620-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="43620-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="43620-127">在**客户详细信息**页面中：</span><span class="sxs-lookup"><span data-stu-id="43620-127">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="43620-128">建议引擎根据客户愿望列表中的用户 ID 和物料推荐物料。</span><span class="sxs-lookup"><span data-stu-id="43620-128">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="43620-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="43620-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="43620-130">配置 Dynamics 365 for Retail 以启用 POS 建议</span><span class="sxs-lookup"><span data-stu-id="43620-130">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="43620-131">若要设置产品建议，需要执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="43620-131">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="43620-132">确保已选择了正确的**法人**。</span><span class="sxs-lookup"><span data-stu-id="43620-132">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="43620-133">导航至**实体商店**，选择**零售**，然后单击**刷新**。这将使用您的操作数据库中的演示数据（或您的数据）并将其移到实体商店。</span><span class="sxs-lookup"><span data-stu-id="43620-133">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="43620-134">可选：若要在交易记录屏幕中显示建议，请转至**屏幕布局**，选择您的屏幕布局，启动**屏幕布局设计器**，然后将**建议**控件拖到所需位置。</span><span class="sxs-lookup"><span data-stu-id="43620-134">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**,and then drop the **recommendations** control where needed.</span></span>
4.  <span data-ttu-id="43620-135">转至**零售参数**，选择**机器学习**，然后在**启用 POS 建议**下选择**是**。</span><span class="sxs-lookup"><span data-stu-id="43620-135">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="43620-136">若要在 POS 中查看建议，请运行全局配置作业 **1110**。</span><span class="sxs-lookup"><span data-stu-id="43620-136">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="43620-137">若要体现对 POS 屏幕布局设计器所做更改，请运行渠道配置作业 **1070**。</span><span class="sxs-lookup"><span data-stu-id="43620-137">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="43620-138">[]()工作原理</span><span class="sxs-lookup"><span data-stu-id="43620-138">[]()How does it work?</span></span>
<span data-ttu-id="43620-139">刷新**实体商店**实体时，将执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="43620-139">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="43620-140">从 Dynamics 365 for Retail 操作数据库提取认知服务所需格式的数据并发送到实体商店。</span><span class="sxs-lookup"><span data-stu-id="43620-140">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="43620-141">Azure Data Factory (ADF) 使用这些数据清理将 Hive 脚本用作ADF 活动一部分的数据。</span><span class="sxs-lookup"><span data-stu-id="43620-141">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="43620-142">清理的数据存储在 blob 存储中。</span><span class="sxs-lookup"><span data-stu-id="43620-142">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="43620-143">认知服务 API 使用 blob 存储中的数据训练建议模型。</span><span class="sxs-lookup"><span data-stu-id="43620-143">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="43620-144">开启**启用建议**并运行配置作业时，将执行以下操作。</span><span class="sxs-lookup"><span data-stu-id="43620-144">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="43620-145">从该 API 选取模型凭据和 ID 并存储到 Dynamics 365 for Retail 操作数据库、AOS 的 web.config 和零售服务器中。</span><span class="sxs-lookup"><span data-stu-id="43620-145">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="43620-146">将模型凭据和 ID 提供给 CRT，以便可以处理联机模式下对 Cloud POS 和 MPOS 的产品建议的请求。</span><span class="sxs-lookup"><span data-stu-id="43620-146">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="43620-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="43620-147">See also</span></span>
--------

[<span data-ttu-id="43620-148">向 POS 设备上的交易记录页添加建议控件</span><span class="sxs-lookup"><span data-stu-id="43620-148">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




