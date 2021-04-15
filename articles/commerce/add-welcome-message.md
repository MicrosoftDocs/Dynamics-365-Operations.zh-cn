---
title: 添加欢迎消息
description: 此主题介绍如何向 Microsoft Dynamics 365 Commerce 网站添加欢迎消息。
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797375"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="2635d-103">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="2635d-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2635d-104">此主题介绍如何向 Microsoft Dynamics 365 Commerce 网站添加欢迎消息。</span><span class="sxs-lookup"><span data-stu-id="2635d-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="2635d-105">电子商务网站中的欢迎消息可告知访问者正在开展的销售、站点新闻或是否提供应季商品。</span><span class="sxs-lookup"><span data-stu-id="2635d-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="2635d-106">欢迎消息使用预警模块设置。</span><span class="sxs-lookup"><span data-stu-id="2635d-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="2635d-107">应该将预警模块添加到页眉片段的 **错误/信息消息** 插槽中。</span><span class="sxs-lookup"><span data-stu-id="2635d-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="2635d-108">可使用预警模块指定显示的文本、文本元素和对齐方式。</span><span class="sxs-lookup"><span data-stu-id="2635d-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="2635d-109">还可以用于指定站点访问者是否可忽略消息。</span><span class="sxs-lookup"><span data-stu-id="2635d-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="2635d-110">欢迎消息添加到共享页眉片段之后，将在使用以下模板的每个页面中显示：使用这个共享页眉片段的模板。</span><span class="sxs-lookup"><span data-stu-id="2635d-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="2635d-111">若要向站点添加欢迎消息，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2635d-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="2635d-112">在 Commerce 站点构建器中，转到您的站点。</span><span class="sxs-lookup"><span data-stu-id="2635d-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="2635d-113">选择 **片段**。</span><span class="sxs-lookup"><span data-stu-id="2635d-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="2635d-114">选择要将消息添加到的页眉片段。</span><span class="sxs-lookup"><span data-stu-id="2635d-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="2635d-115">在大纲树中，展开 **错误/信息消息**。</span><span class="sxs-lookup"><span data-stu-id="2635d-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="2635d-116">选择预警模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2635d-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="2635d-117">如果还没有预警模块，首先选择 **错误/信息消息** 旁边的省略号按钮 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="2635d-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="2635d-118">在右侧的属性窗格中 **数据** 选项卡上，选择 **添加数据源**，然后选择 **内容**。</span><span class="sxs-lookup"><span data-stu-id="2635d-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="2635d-119">在 **输入文本** 字段中，输入欢迎消息的文本。</span><span class="sxs-lookup"><span data-stu-id="2635d-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="2635d-120">选择 **保存**，选择 **完成编辑** 签入页眉片段，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="2635d-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="2635d-121">现在将在使用所选页眉片段的每个站点页顶部显示欢迎消息。</span><span class="sxs-lookup"><span data-stu-id="2635d-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2635d-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="2635d-122">Additional resources</span></span>

[<span data-ttu-id="2635d-123">添加徽标</span><span class="sxs-lookup"><span data-stu-id="2635d-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2635d-124">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="2635d-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2635d-125">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="2635d-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2635d-126">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="2635d-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2635d-127">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="2635d-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2635d-128">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="2635d-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="2635d-129">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="2635d-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
