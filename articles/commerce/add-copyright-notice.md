---
title: 添加版权声明
description: 此主题介绍如何向电子商务网站添加版权声明。
author: psimolin
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58c2949057ef777f706d12cee2dd3341d1a3b7e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914556"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="f28a5-103">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="f28a5-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f28a5-104">此主题介绍如何向电子商务网站添加版权声明。</span><span class="sxs-lookup"><span data-stu-id="f28a5-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f28a5-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="f28a5-105">Prerequisites</span></span>

<span data-ttu-id="f28a5-106">必须准备好以下项，才能向站点添加版权声明：</span><span class="sxs-lookup"><span data-stu-id="f28a5-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="f28a5-107">一个包含共享页脚片段的模板。</span><span class="sxs-lookup"><span data-stu-id="f28a5-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="f28a5-108">一个使用该模板的页面。</span><span class="sxs-lookup"><span data-stu-id="f28a5-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="f28a5-109">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="f28a5-109">Add a copyright notice</span></span>

<span data-ttu-id="f28a5-110">若要向使用特定模板的每个页面的底部添加版权声明，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f28a5-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="f28a5-111">转到**片段**，然后选择**新建页面片段**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="f28a5-112">在对话框中，选择**页脚**模块，然后为片段命名。</span><span class="sxs-lookup"><span data-stu-id="f28a5-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="f28a5-113">例如，输入 **Footer-Copyright**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="f28a5-114">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-114">Select **OK**.</span></span>
1. <span data-ttu-id="f28a5-115">在导航窗格中，选择**页脚**旁边的省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f28a5-116">在对话框中，选择**页脚类别**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="f28a5-117">在导航窗格中，选择**页类别脚**旁边的省略号按钮，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f28a5-118">在对话框中，选择**内容丰富块项**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="f28a5-119">在导航窗格中，选择**内容丰富块项**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="f28a5-120">在右侧的属性窗格中**段落**字段内，添加版权消息。</span><span class="sxs-lookup"><span data-stu-id="f28a5-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="f28a5-121">例如，输入 **(C) Fabrikam 2019**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="f28a5-122">选择**保存**，选择**签入**，然后选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="f28a5-123">转到**模板**，选择模板，然后选择**签出**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="f28a5-124">在**页面大纲**下，展开**正文**，然后展开**默认页面**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="f28a5-125">选择**页脚**插槽旁边的省略号按钮，然后选择**添加片段**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="f28a5-126">选择前面创建的片段，然后选择**选择**。</span><span class="sxs-lookup"><span data-stu-id="f28a5-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="f28a5-127">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="f28a5-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="f28a5-128">将在使用所选模板的所有页面的底部自动显示其中包含版权声明的页脚。</span><span class="sxs-lookup"><span data-stu-id="f28a5-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f28a5-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="f28a5-129">Additional resources</span></span>

[<span data-ttu-id="f28a5-130">添加徽标</span><span class="sxs-lookup"><span data-stu-id="f28a5-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f28a5-131">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="f28a5-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f28a5-132">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="f28a5-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f28a5-133">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="f28a5-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f28a5-134">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="f28a5-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f28a5-135">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="f28a5-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f28a5-136">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="f28a5-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

