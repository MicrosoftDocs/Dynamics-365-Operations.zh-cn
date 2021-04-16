---
title: 为 4xx/5xx 状态代码错误生成自定义响应页面
description: 此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799632"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="5ad92-103">为 4xx/5xx 状态代码错误生成自定义响应页面</span><span class="sxs-lookup"><span data-stu-id="5ad92-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5ad92-104">此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。</span><span class="sxs-lookup"><span data-stu-id="5ad92-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5ad92-105">如果请求失败，服务器将发出 HTTP 状态代码错误响应。</span><span class="sxs-lookup"><span data-stu-id="5ad92-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="5ad92-106">如果未找到页面，将捕获并返回 404 状态代码，如果发生了服务器错误，将捕获并返回 500 状态代码。</span><span class="sxs-lookup"><span data-stu-id="5ad92-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="5ad92-107">在 Dynamics 365 Commerce 中，应用程序用户可为这些状态代码错误响应生成自定义状态代码错误响应页，对用户显示。</span><span class="sxs-lookup"><span data-stu-id="5ad92-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="5ad92-108">生成状态代码错误响应页</span><span class="sxs-lookup"><span data-stu-id="5ad92-108">Build a status code error response page</span></span>

<span data-ttu-id="5ad92-109">若要开始生成状态代码错误响应页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5ad92-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5ad92-110">在首选 Web 浏览器中，登录到 Dynamics 365 Commerce。</span><span class="sxs-lookup"><span data-stu-id="5ad92-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="5ad92-111">选择要为其生成 4xx/5xx 状态代码错误响应页的站点。</span><span class="sxs-lookup"><span data-stu-id="5ad92-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="5ad92-112">生成模板</span><span class="sxs-lookup"><span data-stu-id="5ad92-112">Build the template</span></span>

<span data-ttu-id="5ad92-113">若要生成状态代码错误响应页的模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5ad92-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5ad92-114">转到 **模板**。</span><span class="sxs-lookup"><span data-stu-id="5ad92-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="5ad92-115">选择 **新建** 以创建页面模板。</span><span class="sxs-lookup"><span data-stu-id="5ad92-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="5ad92-116">在 **新建模板** 对话框的 **模板名称** 下，为新模板输入名称，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5ad92-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="5ad92-117">基于希望状态代码错误响应页要采用的结构生成模板。</span><span class="sxs-lookup"><span data-stu-id="5ad92-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="5ad92-118">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="5ad92-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="5ad92-119">生成状态代码错误响应页</span><span class="sxs-lookup"><span data-stu-id="5ad92-119">Build the status code error response page</span></span>

<span data-ttu-id="5ad92-120">若要生成状态代码错误响应页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5ad92-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5ad92-121">转到 **页面**。</span><span class="sxs-lookup"><span data-stu-id="5ad92-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="5ad92-122">选择 **新建** 创建页面。</span><span class="sxs-lookup"><span data-stu-id="5ad92-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="5ad92-123">在 **选择模板** 对话框中，选择一个模板，然后在 **页面名称** 下，输入状态代码错误响应页面的名称。</span><span class="sxs-lookup"><span data-stu-id="5ad92-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="5ad92-124">保持 **页面 URL** 字段为空。</span><span class="sxs-lookup"><span data-stu-id="5ad92-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="5ad92-125">生成页面。</span><span class="sxs-lookup"><span data-stu-id="5ad92-125">Build the page.</span></span>
1. <span data-ttu-id="5ad92-126">选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="5ad92-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="5ad92-127">可为 4xx 和 5xx 状态代码错误创建单独的状态代码错误响应页。</span><span class="sxs-lookup"><span data-stu-id="5ad92-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="5ad92-128">也可以将同一个通用状态代码错误响应页用于两个错误类别。</span><span class="sxs-lookup"><span data-stu-id="5ad92-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="5ad92-129">为状态代码错误响应页设置重定向。</span><span class="sxs-lookup"><span data-stu-id="5ad92-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="5ad92-130">若要为状态代码错误响应页设置重定向，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5ad92-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5ad92-131">转到 **URL \> 新建 \> 新建别名**，然后选择之前生成的状态代码错误响应页。</span><span class="sxs-lookup"><span data-stu-id="5ad92-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="5ad92-132">在 **别名** 字段中，输入 **default-4xx** 或 **default-5xx**，具体取决于要为其设置重定向的状态代码错误响应页。</span><span class="sxs-lookup"><span data-stu-id="5ad92-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="5ad92-133">必须发布这些别名。</span><span class="sxs-lookup"><span data-stu-id="5ad92-133">These aliases must be published.</span></span> <span data-ttu-id="5ad92-134">否则，重定向无效。</span><span class="sxs-lookup"><span data-stu-id="5ad92-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="5ad92-135">选择 **确定** 提交链接。</span><span class="sxs-lookup"><span data-stu-id="5ad92-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="5ad92-136">如果要为两个错误类别设置一个状态代码错误响应页，请重复此过程将另一个错误类别的别名链接到同一页。</span><span class="sxs-lookup"><span data-stu-id="5ad92-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ad92-137">其他资源</span><span class="sxs-lookup"><span data-stu-id="5ad92-137">Additional resources</span></span>

[<span data-ttu-id="5ad92-138">使用模板</span><span class="sxs-lookup"><span data-stu-id="5ad92-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="5ad92-139">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="5ad92-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="5ad92-140">创建页面 URL</span><span class="sxs-lookup"><span data-stu-id="5ad92-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
