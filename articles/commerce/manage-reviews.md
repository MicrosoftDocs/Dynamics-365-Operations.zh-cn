---
title: 管理评分和评价
description: 本主题介绍了如何在 Microsoft Dynamics 365 Commerce 站点构建器中选择管理评分和评价。
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a70d0526fb2443605a6b11df3ee281d4dd12f1d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982558"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="70bd1-103">管理评分和评价</span><span class="sxs-lookup"><span data-stu-id="70bd1-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70bd1-104">本主题介绍了如何在 Microsoft Dynamics 365 Commerce 站点构建器中选择管理评分和评价。</span><span class="sxs-lookup"><span data-stu-id="70bd1-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="70bd1-105">概览</span><span class="sxs-lookup"><span data-stu-id="70bd1-105">Overview</span></span>

<span data-ttu-id="70bd1-106">Dynamics 365 Commerce 使用 Microsoft Azure Cognitive Service 通过修正猥亵词自动审查评价文本。</span><span class="sxs-lookup"><span data-stu-id="70bd1-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="70bd1-107">此外，审查者可以使用 Dynamics 365 Commerce 站点构建器实现以下手动任务：</span><span class="sxs-lookup"><span data-stu-id="70bd1-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="70bd1-108">通过响应或删除评级来审查评级</span><span class="sxs-lookup"><span data-stu-id="70bd1-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="70bd1-109">在客户的请求下删除客户的评价。</span><span class="sxs-lookup"><span data-stu-id="70bd1-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="70bd1-110">将所有产品的评分和评价数据批量导入 Microsoft Power BI 模板中，以便分析评分和评价的趋势。</span><span class="sxs-lookup"><span data-stu-id="70bd1-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="70bd1-111">阅读评价</span><span class="sxs-lookup"><span data-stu-id="70bd1-111">Read a review</span></span> 

<span data-ttu-id="70bd1-112">若要在 Commerce 站点构建器中阅读评价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="70bd1-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70bd1-113">转到 **主页 \> 评价 \> 审查**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="70bd1-114">可使用页面右上角的搜索字段按产品 ID、产品名或评价文本筛选评价。</span><span class="sxs-lookup"><span data-stu-id="70bd1-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="70bd1-115">可使用更多筛选器按期间、评分、渠道或关注状态（已撤下、已响应或已报告）限制评价。</span><span class="sxs-lookup"><span data-stu-id="70bd1-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![审查主页](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="70bd1-117">响应评价</span><span class="sxs-lookup"><span data-stu-id="70bd1-117">Respond to a review</span></span> 

<span data-ttu-id="70bd1-118">有时，购买了产品的客户会表示自己满意或不满意，或者不知道如何使用产品。</span><span class="sxs-lookup"><span data-stu-id="70bd1-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="70bd1-119">作为审查者，您可以发布对评价的响应。</span><span class="sxs-lookup"><span data-stu-id="70bd1-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="70bd1-120">此响应和评价一起在站点中显示。</span><span class="sxs-lookup"><span data-stu-id="70bd1-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="70bd1-121">若要在 Commerce 站点构建器中响应评价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="70bd1-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70bd1-122">转到 **主页 \> 评价 \> 审查**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="70bd1-123">找到并选择需要响应的评价。</span><span class="sxs-lookup"><span data-stu-id="70bd1-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="70bd1-124">在右侧的属性窗格中，选择 **添加响应**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="70bd1-125">输入响应文本和应该对响应者显示的名称。</span><span class="sxs-lookup"><span data-stu-id="70bd1-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="70bd1-126">默认响应者名称为 **审查者**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="70bd1-127">当您完成时，选择 **发布响应**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-127">When you've finished, select **Post response**.</span></span>

![响应评价](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="70bd1-129">撤下评价</span><span class="sxs-lookup"><span data-stu-id="70bd1-129">Take down a review</span></span> 

<span data-ttu-id="70bd1-130">有时设立了业务仲裁供审查者撤下客户评价。</span><span class="sxs-lookup"><span data-stu-id="70bd1-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="70bd1-131">若要在 Commerce 站点构建器中撤下评价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="70bd1-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70bd1-132">转到 **主页 \> 评价 \> 审查**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="70bd1-133">找到并选择必须撤下的评价。</span><span class="sxs-lookup"><span data-stu-id="70bd1-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="70bd1-134">在右侧的属性窗格中，在 **撤下评价** 下方选择撤下原因，然后选择 **撤下**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="70bd1-135">在客户的请求下删除客户的评价</span><span class="sxs-lookup"><span data-stu-id="70bd1-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="70bd1-136">有时，客户希望从电子商务网站中永久删除自己的评分和评价数据。</span><span class="sxs-lookup"><span data-stu-id="70bd1-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="70bd1-137">收到客户的删除请求的注册者可以使用评价删除功能删除客户的数据。</span><span class="sxs-lookup"><span data-stu-id="70bd1-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="70bd1-138">若要找到并删除客户的数据，审查者需要客户用于登录和提供评价的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="70bd1-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="70bd1-139">若要在 Commerce 站点构建器中查找和删除客户数据，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="70bd1-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70bd1-140">转到 **主页 \> 评价 \> 删除**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="70bd1-141">在 **按电子邮件地址搜索用户** 框中，输入客户的电子邮件地址，然后选择 **搜索**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="70bd1-142">如果客户进行了任何评价活动（例如，提交评价，对另一位客户的评价是否有帮助投票，或评论了另一位客户的评价），将显示结果。</span><span class="sxs-lookup"><span data-stu-id="70bd1-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="70bd1-143">每项有一个 **删除** 按钮。</span><span class="sxs-lookup"><span data-stu-id="70bd1-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="70bd1-144">为必须删除的每项选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="70bd1-145">提示确认时，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![删除客户数据](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="70bd1-147">最多可能需要七天，才会从系统中完全删除数据。</span><span class="sxs-lookup"><span data-stu-id="70bd1-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="70bd1-148">审查者应该通知客户存在此延迟。</span><span class="sxs-lookup"><span data-stu-id="70bd1-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="70bd1-149">如果改变了其帐户设置中自己的姓名，搜索结果中可能会显示多项。</span><span class="sxs-lookup"><span data-stu-id="70bd1-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="70bd1-150">在此情况下，要完全删除此客户的数据，审查者必须为各项选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="70bd1-151">下载评分和评价数据</span><span class="sxs-lookup"><span data-stu-id="70bd1-151">Download ratings and reviews data</span></span>

<span data-ttu-id="70bd1-152">通过 Commerce 站点构建器，审查者可以批量导入评分和评价数据，以便分析趋势。</span><span class="sxs-lookup"><span data-stu-id="70bd1-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="70bd1-153">提供其中包含基本度量的 Power BI 模板。</span><span class="sxs-lookup"><span data-stu-id="70bd1-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="70bd1-154">审查者可使用此模板连接批量导入的数据和查看仪表板。</span><span class="sxs-lookup"><span data-stu-id="70bd1-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="70bd1-155">不必创建自定义仪表板。</span><span class="sxs-lookup"><span data-stu-id="70bd1-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="70bd1-156">审查者也可以自定义 Power BI 模板满足其具体需求。</span><span class="sxs-lookup"><span data-stu-id="70bd1-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="70bd1-157">若要在 Commerce 站点构建器中下载评分和评价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="70bd1-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70bd1-158">转到 **主页 \> 评价 \> 报告**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="70bd1-159">选择 **下载评价数据** 使用逗号分隔的值 (CSV) 格式批量下载评分和评价数据。</span><span class="sxs-lookup"><span data-stu-id="70bd1-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="70bd1-160">查看评分和评价趋势</span><span class="sxs-lookup"><span data-stu-id="70bd1-160">View ratings and reviews trends</span></span>

<span data-ttu-id="70bd1-161">审查者可下载 Power BI 模板，以便在仪表板中查看趋势。</span><span class="sxs-lookup"><span data-stu-id="70bd1-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="70bd1-162">若要在 Commerce 站点构建器中查看评分和评价趋势，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="70bd1-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70bd1-163">转到 **主页 \> 评价 \> 报告**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="70bd1-164">选择 **PowerBI 模板** 下载模板。</span><span class="sxs-lookup"><span data-stu-id="70bd1-164">Select **PowerBI template** to download the template.</span></span>

    ![下载 Power BI 模板](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="70bd1-166">使用 Power BI 应用打开下载的模板。</span><span class="sxs-lookup"><span data-stu-id="70bd1-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="70bd1-167">关闭显示的 **访问 Web 内容** 对话框，然后关闭显示的“刷新”错误消息。</span><span class="sxs-lookup"><span data-stu-id="70bd1-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="70bd1-168">转到 **主页**，选择 **编辑查询**，然后选择 **数据源设置**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="70bd1-169">在 **数据源设置** 对话框中，选择 **更改源**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="70bd1-170">在 **URL** 字段中，输入上一过程中下载的评价数据的路径（例如，**c:\\reviews\\ReviewsData.csv**）。</span><span class="sxs-lookup"><span data-stu-id="70bd1-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![“逗号分隔值”对话框中的 URL 字段](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="70bd1-172">选择 **确定**，然后选择 **应用更改**。</span><span class="sxs-lookup"><span data-stu-id="70bd1-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="70bd1-173">需要一到两分钟才能应用对数据源的更改。</span><span class="sxs-lookup"><span data-stu-id="70bd1-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="70bd1-174">选择 **趋势表** 显示评分和评价趋势。</span><span class="sxs-lookup"><span data-stu-id="70bd1-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![评分和评价趋势](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="70bd1-176">其他资源</span><span class="sxs-lookup"><span data-stu-id="70bd1-176">Additional resources</span></span>

[<span data-ttu-id="70bd1-177">评分和评价概览</span><span class="sxs-lookup"><span data-stu-id="70bd1-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="70bd1-178">选择使用评分和评价</span><span class="sxs-lookup"><span data-stu-id="70bd1-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="70bd1-179">配置评分和评价</span><span class="sxs-lookup"><span data-stu-id="70bd1-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="70bd1-180">在 Dynamics 365 Retail 中同步产品评分</span><span class="sxs-lookup"><span data-stu-id="70bd1-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
