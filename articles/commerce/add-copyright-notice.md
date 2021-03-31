---
title: 添加版权声明
description: 此主题介绍如何向电子商务网站添加版权声明。
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2ea04854636fdd0c2b3223bb19d5f06a19836151
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206359"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="5e510-103">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="5e510-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5e510-104">此主题介绍如何向电子商务网站添加版权声明。</span><span class="sxs-lookup"><span data-stu-id="5e510-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5e510-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="5e510-105">Prerequisites</span></span>

<span data-ttu-id="5e510-106">必须准备好以下项，才能向站点添加版权声明：</span><span class="sxs-lookup"><span data-stu-id="5e510-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="5e510-107">一个包含共享页脚片段的模板。</span><span class="sxs-lookup"><span data-stu-id="5e510-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="5e510-108">一个使用该模板的页面。</span><span class="sxs-lookup"><span data-stu-id="5e510-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="5e510-109">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="5e510-109">Add a copyright notice</span></span>

<span data-ttu-id="5e510-110">若要向使用特定模板的每个页面的底部添加版权声明，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5e510-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="5e510-111">转到 **片段**，然后选择 **新建**.</span><span class="sxs-lookup"><span data-stu-id="5e510-111">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="5e510-112">在 **新建片段** 对话框中，选择 **页脚** 模块，然后为片段命名。</span><span class="sxs-lookup"><span data-stu-id="5e510-112">In the **New fragment** dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="5e510-113">例如，输入 **Footer-Copyright**。</span><span class="sxs-lookup"><span data-stu-id="5e510-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="5e510-114">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5e510-114">Select **OK**.</span></span>
1. <span data-ttu-id="5e510-115">在导航窗格中，选择 **页脚** 旁边的省略号按钮 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="5e510-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="5e510-116">在对话框中，选择 **页脚类别**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5e510-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="5e510-117">在导航窗格中，选择 **页类别脚** 旁边的省略号按钮，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="5e510-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="5e510-118">在对话框中，选择 **文本块**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5e510-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="5e510-119">在导航窗格中，选择 **文字块**。</span><span class="sxs-lookup"><span data-stu-id="5e510-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="5e510-120">在右侧的属性窗格中 **段落** 字段内，添加版权消息。</span><span class="sxs-lookup"><span data-stu-id="5e510-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="5e510-121">例如，输入 **(C) Fabrikam 2019**。</span><span class="sxs-lookup"><span data-stu-id="5e510-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="5e510-122">选择 **保存**，选择 **完成编辑**，然后选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="5e510-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="5e510-123">转到 **模板**，选择模板，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="5e510-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="5e510-124">在 **页面大纲** 下，展开 **正文**，然后展开 **默认页面**。</span><span class="sxs-lookup"><span data-stu-id="5e510-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="5e510-125">选择 **页脚** 插槽旁边的省略号按钮，然后选择 **添加片段**。</span><span class="sxs-lookup"><span data-stu-id="5e510-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="5e510-126">选择前面创建的片段，然后选择 **选择**。</span><span class="sxs-lookup"><span data-stu-id="5e510-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="5e510-127">选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="5e510-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="5e510-128">将在使用所选模板的所有页面的底部自动显示其中包含版权声明的页脚。</span><span class="sxs-lookup"><span data-stu-id="5e510-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e510-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="5e510-129">Additional resources</span></span>

[<span data-ttu-id="5e510-130">添加徽标</span><span class="sxs-lookup"><span data-stu-id="5e510-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="5e510-131">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="5e510-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="5e510-132">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="5e510-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="5e510-133">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="5e510-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="5e510-134">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="5e510-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5e510-135">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="5e510-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="5e510-136">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="5e510-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]