---
title: 管理评分和评价
description: 此主题介绍如何使用 Microsoft Dynamics 365 Commerce 评分和评价审查工具管理评分和评价。
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027234"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="92143-103">管理评分和评价</span><span class="sxs-lookup"><span data-stu-id="92143-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92143-104">此主题介绍如何使用 Microsoft Dynamics 365 Commerce 评分和评价审查工具管理评分和评价。</span><span class="sxs-lookup"><span data-stu-id="92143-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="92143-105">概览</span><span class="sxs-lookup"><span data-stu-id="92143-105">Overview</span></span>

<span data-ttu-id="92143-106">Dynamics 365 Commerce 使用 Microsoft Azure Cognitive Service 通过修正猥亵词自动审查评价文本。</span><span class="sxs-lookup"><span data-stu-id="92143-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="92143-107">此外，审查者还可以使用评分和评价审查工具执行以下手动任务：</span><span class="sxs-lookup"><span data-stu-id="92143-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="92143-108">通过响应或删除评级来审查评级</span><span class="sxs-lookup"><span data-stu-id="92143-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="92143-109">在客户的请求下删除客户的评价。</span><span class="sxs-lookup"><span data-stu-id="92143-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="92143-110">将所有产品的评分和评价数据批量导入 Microsoft Power BI 模板中，以便分析评分和评价的趋势。</span><span class="sxs-lookup"><span data-stu-id="92143-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="92143-111">访问评分和评价审查功能</span><span class="sxs-lookup"><span data-stu-id="92143-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="92143-112">要访问电子商务站点管理工具中的评分和评价审查功能，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="92143-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="92143-113">登录 [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com)。</span><span class="sxs-lookup"><span data-stu-id="92143-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="92143-114">打开包含要在其中初始化电子商务的环境的项目。</span><span class="sxs-lookup"><span data-stu-id="92143-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="92143-115">在**环境**部分中，选择环境。</span><span class="sxs-lookup"><span data-stu-id="92143-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="92143-116">在**环境功能**下，选择**零售管理**。</span><span class="sxs-lookup"><span data-stu-id="92143-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="92143-117">在**电子商务**选项卡上，在**链接**下，选择**电子商务站点管理工具**。</span><span class="sxs-lookup"><span data-stu-id="92143-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="92143-118">阅读评价</span><span class="sxs-lookup"><span data-stu-id="92143-118">Read a review</span></span> 

1. <span data-ttu-id="92143-119">转到**主页 \> 评价 \> 审查**。</span><span class="sxs-lookup"><span data-stu-id="92143-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="92143-120">可使用页面右上角的搜索字段按产品 ID、产品名或评价文本筛选评价。</span><span class="sxs-lookup"><span data-stu-id="92143-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="92143-121">可使用更多筛选器按期间、评分、渠道或关注状态（已撤下、已响应或已报告）限制评价。</span><span class="sxs-lookup"><span data-stu-id="92143-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![审查主页](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="92143-123">响应评价</span><span class="sxs-lookup"><span data-stu-id="92143-123">Respond to a review</span></span> 

<span data-ttu-id="92143-124">有时，购买了产品的客户会表示自己满意或不满意，或者不知道如何使用产品。</span><span class="sxs-lookup"><span data-stu-id="92143-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="92143-125">作为审查者，您可以发布对评价的响应。</span><span class="sxs-lookup"><span data-stu-id="92143-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="92143-126">此响应和评价一起在站点中显示。</span><span class="sxs-lookup"><span data-stu-id="92143-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="92143-127">若要响应评价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="92143-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="92143-128">转到**主页 \> 评价 \> 审查**。</span><span class="sxs-lookup"><span data-stu-id="92143-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="92143-129">找到并选择需要响应的评价。</span><span class="sxs-lookup"><span data-stu-id="92143-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="92143-130">在右侧的属性窗格中，选择**添加响应**。</span><span class="sxs-lookup"><span data-stu-id="92143-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="92143-131">输入响应文本和应该对响应者显示的名称。</span><span class="sxs-lookup"><span data-stu-id="92143-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="92143-132">默认响应者名称为**审查者**。</span><span class="sxs-lookup"><span data-stu-id="92143-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="92143-133">当您完成时，选择**发布响应**。</span><span class="sxs-lookup"><span data-stu-id="92143-133">When you've finished, select **Post response**.</span></span>

![响应评价](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="92143-135">撤下评价</span><span class="sxs-lookup"><span data-stu-id="92143-135">Take down a review</span></span> 

<span data-ttu-id="92143-136">有时设立了业务仲裁供审查者撤下客户评价。</span><span class="sxs-lookup"><span data-stu-id="92143-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="92143-137">若要撤下评价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="92143-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="92143-138">转到**主页 \> 评价 \> 审查**。</span><span class="sxs-lookup"><span data-stu-id="92143-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="92143-139">找到并选择必须撤下的评价。</span><span class="sxs-lookup"><span data-stu-id="92143-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="92143-140">在右侧的属性窗格中，选择撤下原因，然后选择**撤下**。</span><span class="sxs-lookup"><span data-stu-id="92143-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="92143-141">在客户的请求下删除客户的评价</span><span class="sxs-lookup"><span data-stu-id="92143-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="92143-142">有时，客户希望从电子商务网站中永久删除自己的评分和评价数据。</span><span class="sxs-lookup"><span data-stu-id="92143-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="92143-143">收到客户的删除请求的注册者可以使用评价删除功能删除客户的数据。</span><span class="sxs-lookup"><span data-stu-id="92143-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="92143-144">若要找到并删除客户的数据，审查者需要客户用于登录和提供评价的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="92143-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="92143-145">若要查找和删除客户数据，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="92143-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="92143-146">转到**主页 \> 评价 \> 删除**。</span><span class="sxs-lookup"><span data-stu-id="92143-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="92143-147">在**按电子邮件地址搜索用户**字段中，输入客户的电子邮件地址，然后选择**搜索**。</span><span class="sxs-lookup"><span data-stu-id="92143-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="92143-148">如果客户进行了任何评价活动（例如，提交评价，对另一位客户的评价是否有帮助投票，或评论了另一位客户的评价），将显示结果。</span><span class="sxs-lookup"><span data-stu-id="92143-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="92143-149">每项有一个**删除**按钮。</span><span class="sxs-lookup"><span data-stu-id="92143-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="92143-150">为必须删除的每项选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="92143-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="92143-151">提示确认时，选择**是**。</span><span class="sxs-lookup"><span data-stu-id="92143-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![删除客户数据](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="92143-153">最多可能需要七天，才会从系统中完全删除数据。</span><span class="sxs-lookup"><span data-stu-id="92143-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="92143-154">审查者应该通知客户存在此延迟。</span><span class="sxs-lookup"><span data-stu-id="92143-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="92143-155">如果改变了其帐户设置中自己的姓名，搜索结果中可能会显示多项。</span><span class="sxs-lookup"><span data-stu-id="92143-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="92143-156">在此情况下，要完全删除此客户的数据，审查者必须为各项选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="92143-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="92143-157">下载评分和评价数据</span><span class="sxs-lookup"><span data-stu-id="92143-157">Download ratings and reviews data</span></span>

<span data-ttu-id="92143-158">审查者可使用评分和评价审查工具批量导入评分和评价数据，以便分析趋势。</span><span class="sxs-lookup"><span data-stu-id="92143-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="92143-159">提供其中包含基本度量的 Power BI 模板。</span><span class="sxs-lookup"><span data-stu-id="92143-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="92143-160">审查者可使用此模板连接批量导入的数据和查看仪表板。</span><span class="sxs-lookup"><span data-stu-id="92143-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="92143-161">不必创建自定义仪表板。</span><span class="sxs-lookup"><span data-stu-id="92143-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="92143-162">审查者也可以自定义 Power BI 模板满足其具体需求。</span><span class="sxs-lookup"><span data-stu-id="92143-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="92143-163">若要下载评分和评价数据，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="92143-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="92143-164">转到**主页 \> 评价 \> 报告**。</span><span class="sxs-lookup"><span data-stu-id="92143-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="92143-165">选择**下载评价数据**使用逗号分隔的值 (CSV) 格式批量下载评分和评价数据。</span><span class="sxs-lookup"><span data-stu-id="92143-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="92143-166">查看评分和评价趋势</span><span class="sxs-lookup"><span data-stu-id="92143-166">View ratings and reviews trends</span></span>

<span data-ttu-id="92143-167">审查者可下载 Power BI 模板，以便在仪表板中查看趋势。</span><span class="sxs-lookup"><span data-stu-id="92143-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="92143-168">若要查看评分和评价趋势，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="92143-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="92143-169">转到**主页 \> 评价 \> 报告**。</span><span class="sxs-lookup"><span data-stu-id="92143-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="92143-170">选择 **PowerBI 模板**下载模板。</span><span class="sxs-lookup"><span data-stu-id="92143-170">Select **PowerBI template** to download the template.</span></span>

    ![下载 Power BI 模板](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="92143-172">使用 Power BI 应用打开下载的模板。</span><span class="sxs-lookup"><span data-stu-id="92143-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="92143-173">关闭显示的**访问 Web 内容**对话框，然后关闭显示的“刷新”错误消息。</span><span class="sxs-lookup"><span data-stu-id="92143-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="92143-174">转到**主页**，选择**编辑查询**，然后选择**数据源设置**。</span><span class="sxs-lookup"><span data-stu-id="92143-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="92143-175">在**数据源设置**对话框中，选择**更改源**。</span><span class="sxs-lookup"><span data-stu-id="92143-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="92143-176">在 **URL** 字段中，输入上一过程中下载的评价数据的路径（例如，**c:\\reviews\\ReviewsData.csv**）。</span><span class="sxs-lookup"><span data-stu-id="92143-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![“逗号分隔值”对话框中的 URL 字段](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="92143-178">选择**确定**，然后选择**应用更改**。</span><span class="sxs-lookup"><span data-stu-id="92143-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="92143-179">需要一到两分钟才能应用对数据源的更改。</span><span class="sxs-lookup"><span data-stu-id="92143-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="92143-180">选择**趋势表**显示评分和评价趋势。</span><span class="sxs-lookup"><span data-stu-id="92143-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![评分和评价趋势](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="92143-182">其他资源</span><span class="sxs-lookup"><span data-stu-id="92143-182">Additional resources</span></span>

[<span data-ttu-id="92143-183">评分和评价概览</span><span class="sxs-lookup"><span data-stu-id="92143-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="92143-184">选择使用评分和评价</span><span class="sxs-lookup"><span data-stu-id="92143-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="92143-185">配置评分和评价</span><span class="sxs-lookup"><span data-stu-id="92143-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="92143-186">在 Dynamics 365 Retail 中同步产品评分</span><span class="sxs-lookup"><span data-stu-id="92143-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
