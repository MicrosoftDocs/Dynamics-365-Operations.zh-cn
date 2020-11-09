---
title: 社交共享模块
description: 此主题介绍社交共享模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022067"
---
# <a name="social-share-module"></a><span data-ttu-id="fcc1f-103">社交共享模块</span><span class="sxs-lookup"><span data-stu-id="fcc1f-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fcc1f-104">此主题介绍社交共享模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fcc1f-105">概览</span><span class="sxs-lookup"><span data-stu-id="fcc1f-105">Overview</span></span>

<span data-ttu-id="fcc1f-106">用户可通过社交共享模块在 Facebook、Twitter、Pinterest 和 LinkedIn 之类社交媒体上共享电子商务站点页面 URL。 </span><span class="sxs-lookup"><span data-stu-id="fcc1f-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="fcc1f-107">也可以通过电子邮件共享站点页面 URL。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="fcc1f-108">社交共享模块通常在产品详细信息页 (PDP) 上用于帮助用户共享产品信息。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="fcc1f-109">每个社交共享模块都是一个社交共享项模块容器。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="fcc1f-110">每个社交共享项模块配置为指向特定社交媒体站点。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="fcc1f-111">自带支持集成 Facebook、Twitter、Pinterest、LinkedIn 和电子邮件。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="fcc1f-112">当站点用户选择社交媒体符号时，将为相应的社交媒体站点启动 HTML iframe。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="fcc1f-113">在该 iframe 中，用户可以登录和发布自己正在查看的页面内容。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="fcc1f-114">每个社交媒体平台都可能跟踪 cookie，因此此模块需要用户接受 cookie 同意通知消息。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="fcc1f-115">如果不接受 cookie 同意，页面中将隐藏此模块。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="fcc1f-116">有关详细信息，请参阅 [Cookie 合规性](cookie-compliance.md)。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="fcc1f-117">下图突出显示产品详细信息页中使用的社交共享模块的示例。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![社交共享模块的示例](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="fcc1f-119">社交共享模块属性</span><span class="sxs-lookup"><span data-stu-id="fcc1f-119">Social share module properties</span></span>

| <span data-ttu-id="fcc1f-120">属性名称</span><span class="sxs-lookup"><span data-stu-id="fcc1f-120">Property name</span></span>             | <span data-ttu-id="fcc1f-121">值</span><span class="sxs-lookup"><span data-stu-id="fcc1f-121">Value</span></span>                 | <span data-ttu-id="fcc1f-122">说明</span><span class="sxs-lookup"><span data-stu-id="fcc1f-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="fcc1f-123">标题</span><span class="sxs-lookup"><span data-stu-id="fcc1f-123">Caption</span></span>                  | <span data-ttu-id="fcc1f-124">文本</span><span class="sxs-lookup"><span data-stu-id="fcc1f-124">Text</span></span> | <span data-ttu-id="fcc1f-125">此属性指定模块的标题。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="fcc1f-126">方向</span><span class="sxs-lookup"><span data-stu-id="fcc1f-126">Orientation</span></span> | <span data-ttu-id="fcc1f-127">**水平** 或 **垂直**</span><span class="sxs-lookup"><span data-stu-id="fcc1f-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="fcc1f-128">此属性定义社交共享项的布局属性。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="fcc1f-129">社交共享项模块属性</span><span class="sxs-lookup"><span data-stu-id="fcc1f-129">Social share item module properties</span></span>
| <span data-ttu-id="fcc1f-130">属性名称</span><span class="sxs-lookup"><span data-stu-id="fcc1f-130">Property name</span></span>             | <span data-ttu-id="fcc1f-131">值</span><span class="sxs-lookup"><span data-stu-id="fcc1f-131">Value</span></span>                 | <span data-ttu-id="fcc1f-132">说明</span><span class="sxs-lookup"><span data-stu-id="fcc1f-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="fcc1f-133">社交媒体</span><span class="sxs-lookup"><span data-stu-id="fcc1f-133">Social media</span></span>              | <span data-ttu-id="fcc1f-134">**Facebook** 、 **Twitter** 、 **Pinterest** 、 **LinkedIn** 、 **Mail**</span><span class="sxs-lookup"><span data-stu-id="fcc1f-134">**Facebook** , **Twitter** , **Pinterest** , **LinkedIn** , **Mail**</span></span> | <span data-ttu-id="fcc1f-135">一个带有社交媒体平台列表的下拉菜单。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="fcc1f-136">图标</span><span class="sxs-lookup"><span data-stu-id="fcc1f-136">Icon</span></span> |<span data-ttu-id="fcc1f-137">头像</span><span class="sxs-lookup"><span data-stu-id="fcc1f-137">Image</span></span>    | <span data-ttu-id="fcc1f-138">这将是将对相应社交媒体显示的图像。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="fcc1f-139">最佳实践是参阅社交媒体平台的 SDK 以获取各平台推荐各平台使用的图像。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="fcc1f-140">向购买框模块添加社交共享模块</span><span class="sxs-lookup"><span data-stu-id="fcc1f-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="fcc1f-141">若要向购买框模块添加社交共享模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="fcc1f-142">在 Fabrikam 站点中，选择 **页面** ，然后选择 **DefaultPDP** 页面打开产品详细信息页。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-142">In the Fabrikam site, select **Pages** , and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="fcc1f-143">在 **购买框(必填)** 插槽中，选择省略号 ( **...** )，然后选择 **添加模块** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-143">In the **Buybox (required)** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fcc1f-144">在 **添加模块** 对话框中，选择 **社交共享** 模块，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fcc1f-145">在 **社交共享** 插槽中，选择省略号 ( **...** )，然后选择 **添加模块** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-145">In the **Social Share** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fcc1f-146">在 **添加模块** 对话框中，选择 **SocialShare** 模块，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fcc1f-147">在 **SocialShare** 模块属性窗格中 **方向** 下，选择 **水平** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-147">In the properties pane of the **SocialShare** module, under **Orientation** , select **Horizontal**.</span></span> <span data-ttu-id="fcc1f-148">根据需要添加标题。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="fcc1f-149">在 **SocialShare** 插槽中，选择省略号 ( **...** )，然后选择 **添加模块** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-149">In the **SocialShare** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fcc1f-150">在 **添加模块** 对话框中，选择 **SocialShareItem** 模块，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fcc1f-151">在 **SocialShareItem** 模块属性窗格中的 **社交媒体** 下，选择 **Facebook** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-151">In the properties pane of the **SocialShareItem** module, under **Social Media** , select **Facebook**.</span></span>
1. <span data-ttu-id="fcc1f-152">在 **SocialShareItem** 模块属性窗格中的 **图标** 下，选择 **+ 添加图像** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-152">In the properties pane of the **SocialShareItem** module, under **Icon** , select **+ Add an image**.</span></span>
1. <span data-ttu-id="fcc1f-153">在 **媒体选择器** 对话框中，选择 Facebook 徽标图像，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="fcc1f-154">如果无 Facebook 徽标图像，请选择 **上载新媒体项** 上载一个。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="fcc1f-155">根据需要添加和配置更多 **SocialShareItem** 模块。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="fcc1f-156">选择 **保存** ，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-156">Select **Save** , and then select **Preview** to preview the page.</span></span> <span data-ttu-id="fcc1f-157">该页面将显示社交共享模块。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="fcc1f-158">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="fcc1f-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcc1f-159">其他资源</span><span class="sxs-lookup"><span data-stu-id="fcc1f-159">Additional resources</span></span>

[<span data-ttu-id="fcc1f-160">模块库概述</span><span class="sxs-lookup"><span data-stu-id="fcc1f-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fcc1f-161">购买框模块</span><span class="sxs-lookup"><span data-stu-id="fcc1f-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fcc1f-162">Cookie 合规性</span><span class="sxs-lookup"><span data-stu-id="fcc1f-162">Cookie compliance</span></span>](cookie-compliance.md)
