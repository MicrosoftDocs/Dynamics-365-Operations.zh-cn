---
title: 为 4xx/5xx 状态代码错误生成自定义响应页面
description: 此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee2f74581ded6020d075377f931c465d7c89f9e5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211097"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="1933f-103">为 4xx/5xx 状态代码错误生成自定义响应页面</span><span class="sxs-lookup"><span data-stu-id="1933f-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1933f-104">此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。</span><span class="sxs-lookup"><span data-stu-id="1933f-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1933f-105">概览</span><span class="sxs-lookup"><span data-stu-id="1933f-105">Overview</span></span>

<span data-ttu-id="1933f-106">如果请求失败，服务器将发出 HTTP 状态代码错误响应。</span><span class="sxs-lookup"><span data-stu-id="1933f-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="1933f-107">如果未找到页面，将捕获并返回 404 状态代码，如果发生了服务器错误，将捕获并返回 500 状态代码。</span><span class="sxs-lookup"><span data-stu-id="1933f-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="1933f-108">在 Dynamics 365 Commerce 中，应用程序用户可为这些状态代码错误响应生成自定义状态代码错误响应页，对用户显示。</span><span class="sxs-lookup"><span data-stu-id="1933f-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="1933f-109">生成状态代码错误响应页</span><span class="sxs-lookup"><span data-stu-id="1933f-109">Build a status code error response page</span></span>

<span data-ttu-id="1933f-110">若要开始生成状态代码错误响应页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1933f-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="1933f-111">在首选 Web 浏览器中，登录到 Dynamics 365 Commerce。</span><span class="sxs-lookup"><span data-stu-id="1933f-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="1933f-112">选择要为其生成 4xx/5xx 状态代码错误响应页的站点。</span><span class="sxs-lookup"><span data-stu-id="1933f-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="1933f-113">生成模板</span><span class="sxs-lookup"><span data-stu-id="1933f-113">Build the template</span></span>

<span data-ttu-id="1933f-114">若要生成状态代码错误响应页的模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1933f-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="1933f-115">转到 **模板**。</span><span class="sxs-lookup"><span data-stu-id="1933f-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="1933f-116">选择 **新建** 以创建页面模板。</span><span class="sxs-lookup"><span data-stu-id="1933f-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="1933f-117">在 **新建模板** 对话框的 **模板名称** 下，为新模板输入名称，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1933f-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="1933f-118">基于希望状态代码错误响应页要采用的结构生成模板。</span><span class="sxs-lookup"><span data-stu-id="1933f-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="1933f-119">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="1933f-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="1933f-120">生成状态代码错误响应页</span><span class="sxs-lookup"><span data-stu-id="1933f-120">Build the status code error response page</span></span>

<span data-ttu-id="1933f-121">若要生成状态代码错误响应页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1933f-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="1933f-122">转到 **页面**。</span><span class="sxs-lookup"><span data-stu-id="1933f-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="1933f-123">选择 **新建** 创建页面。</span><span class="sxs-lookup"><span data-stu-id="1933f-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="1933f-124">在 **选择模板** 对话框中，选择一个模板，然后在 **页面名称** 下，输入状态代码错误响应页面的名称。</span><span class="sxs-lookup"><span data-stu-id="1933f-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="1933f-125">保持 **页面 URL** 字段为空。</span><span class="sxs-lookup"><span data-stu-id="1933f-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="1933f-126">生成页面。</span><span class="sxs-lookup"><span data-stu-id="1933f-126">Build the page.</span></span>
1. <span data-ttu-id="1933f-127">选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="1933f-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="1933f-128">可为 4xx 和 5xx 状态代码错误创建单独的状态代码错误响应页。</span><span class="sxs-lookup"><span data-stu-id="1933f-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="1933f-129">也可以将同一个通用状态代码错误响应页用于两个错误类别。</span><span class="sxs-lookup"><span data-stu-id="1933f-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="1933f-130">为状态代码错误响应页设置重定向。</span><span class="sxs-lookup"><span data-stu-id="1933f-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="1933f-131">若要为状态代码错误响应页设置重定向，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1933f-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="1933f-132">转到 **URL \> 新建 \> 新建别名**，然后选择之前生成的状态代码错误响应页。</span><span class="sxs-lookup"><span data-stu-id="1933f-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="1933f-133">在 **别名** 字段中，输入 **default-4xx** 或 **default-5xx**，具体取决于要为其设置重定向的状态代码错误响应页。</span><span class="sxs-lookup"><span data-stu-id="1933f-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="1933f-134">必须发布这些别名。</span><span class="sxs-lookup"><span data-stu-id="1933f-134">These aliases must be published.</span></span> <span data-ttu-id="1933f-135">否则，重定向无效。</span><span class="sxs-lookup"><span data-stu-id="1933f-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="1933f-136">选择 **确定** 提交链接。</span><span class="sxs-lookup"><span data-stu-id="1933f-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="1933f-137">如果要为两个错误类别设置一个状态代码错误响应页，请重复此过程将另一个错误类别的别名链接到同一页。</span><span class="sxs-lookup"><span data-stu-id="1933f-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1933f-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="1933f-138">Additional resources</span></span>

[<span data-ttu-id="1933f-139">使用模板</span><span class="sxs-lookup"><span data-stu-id="1933f-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="1933f-140">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="1933f-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="1933f-141">创建页面 URL</span><span class="sxs-lookup"><span data-stu-id="1933f-141">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]