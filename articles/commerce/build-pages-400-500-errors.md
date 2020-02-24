---
title: 为 4xx/5xx 状态代码错误生成自定义响应页面
description: 此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4477a0a43971b5322c6acd6971cba2e79e2dc8c6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001109"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="32137-103">为 4xx/5xx 状态代码错误生成自定义响应页面</span><span class="sxs-lookup"><span data-stu-id="32137-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="32137-104">此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的制作工具为 4xx 和 5xx 状态代码错误生成自定义响应页。</span><span class="sxs-lookup"><span data-stu-id="32137-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="32137-105">概览</span><span class="sxs-lookup"><span data-stu-id="32137-105">Overview</span></span>

<span data-ttu-id="32137-106">如果请求失败，服务器将发出 HTTP 状态代码错误响应。</span><span class="sxs-lookup"><span data-stu-id="32137-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="32137-107">如果未找到页面，将捕获并返回 404 状态代码，如果发生了服务器错误，将捕获并返回 500 状态代码。</span><span class="sxs-lookup"><span data-stu-id="32137-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="32137-108">在 Dynamics 365 Commerce 中，应用程序用户可为这些状态代码错误响应生成自定义状态代码错误响应页，对用户显示。</span><span class="sxs-lookup"><span data-stu-id="32137-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="32137-109">生成状态代码错误响应页</span><span class="sxs-lookup"><span data-stu-id="32137-109">Build a status code error response page</span></span>

<span data-ttu-id="32137-110">若要开始生成状态代码错误响应页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="32137-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="32137-111">在首选 Web 浏览器中，登录到 Dynamics 365 Commerce。</span><span class="sxs-lookup"><span data-stu-id="32137-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="32137-112">选择要为其生成 4xx/5xx 状态代码错误响应页的站点。</span><span class="sxs-lookup"><span data-stu-id="32137-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="32137-113">生成模板</span><span class="sxs-lookup"><span data-stu-id="32137-113">Build the template</span></span>

<span data-ttu-id="32137-114">若要生成状态代码错误响应页的模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="32137-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="32137-115">转到**模板 \> 新建模板**。</span><span class="sxs-lookup"><span data-stu-id="32137-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="32137-116">为新模板命名。</span><span class="sxs-lookup"><span data-stu-id="32137-116">Name the new template.</span></span>
1. <span data-ttu-id="32137-117">基于希望状态代码错误响应页要采用的结构生成模板。</span><span class="sxs-lookup"><span data-stu-id="32137-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="32137-118">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="32137-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="32137-119">生成状态代码错误响应页</span><span class="sxs-lookup"><span data-stu-id="32137-119">Build the status code error response page</span></span>

<span data-ttu-id="32137-120">若要生成状态代码错误响应页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="32137-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="32137-121">转到**页面 \> 新建页面**。</span><span class="sxs-lookup"><span data-stu-id="32137-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="32137-122">为状态代码错误响应页命名，但**不**设置 **URL** 字段。</span><span class="sxs-lookup"><span data-stu-id="32137-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="32137-123">生成页面。</span><span class="sxs-lookup"><span data-stu-id="32137-123">Build the page.</span></span>
1. <span data-ttu-id="32137-124">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="32137-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="32137-125">可为 4xx 和 5xx 状态代码错误创建单独的状态代码错误响应页。</span><span class="sxs-lookup"><span data-stu-id="32137-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="32137-126">也可以将同一个通用状态代码错误响应页用于两个错误类别。</span><span class="sxs-lookup"><span data-stu-id="32137-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="32137-127">为状态代码错误响应页设置重定向。</span><span class="sxs-lookup"><span data-stu-id="32137-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="32137-128">若要为状态代码错误响应页设置重定向，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="32137-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="32137-129">转到 **URL \> 新建 \> 新建别名**，然后选择之前生成的状态代码错误响应页。</span><span class="sxs-lookup"><span data-stu-id="32137-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="32137-130">在**别名**字段中，输入 **default-4xx** 或 **default-5xx**，具体取决于要为其设置重定向的状态代码错误响应页。</span><span class="sxs-lookup"><span data-stu-id="32137-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="32137-131">必须发布这些别名。</span><span class="sxs-lookup"><span data-stu-id="32137-131">These aliases must be published.</span></span> <span data-ttu-id="32137-132">否则，重定向无效。</span><span class="sxs-lookup"><span data-stu-id="32137-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="32137-133">选择**确定**提交链接。</span><span class="sxs-lookup"><span data-stu-id="32137-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="32137-134">如果要为两个错误类别设置一个状态代码错误响应页，请重复此过程将另一个错误类别的别名链接到同一页。</span><span class="sxs-lookup"><span data-stu-id="32137-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32137-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="32137-135">Additional resources</span></span>

[<span data-ttu-id="32137-136">使用模板</span><span class="sxs-lookup"><span data-stu-id="32137-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="32137-137">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="32137-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="32137-138">创建页面 URL</span><span class="sxs-lookup"><span data-stu-id="32137-138">Create a page URL</span></span>](create-page-url.md)
