---
title: 嵌入第三方应用
description: 本主题说明如何嵌入第三方应用以扩展产品的功能。
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d348683e0a2ed35f26830a6ce05c0bf9ca5970bd
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944822"
---
# <a name="embed-third-party-apps"></a><span data-ttu-id="b4a16-103">嵌入第三方应用</span><span class="sxs-lookup"><span data-stu-id="b4a16-103">Embed third-party apps</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="b4a16-104">很多客户使用各种应用程序来开展业务。</span><span class="sxs-lookup"><span data-stu-id="b4a16-104">Many customers use a range of applications to run their business.</span></span> <span data-ttu-id="b4a16-105">这些应用程序中有一些是与 Finance and Operations 应用结合使用的第三方 Web 应用。</span><span class="sxs-lookup"><span data-stu-id="b4a16-105">Some of those applications are third-party web apps that work in conjunction with Finance and Operations apps.</span></span> <span data-ttu-id="b4a16-106">要提供更无缝的用户体验，您可以使用 **(预览)整页应用** 功能将那些第三方应用直接嵌入到您的 Finance and Operations 应用中（前提是第三方应用允许被嵌入）。</span><span class="sxs-lookup"><span data-stu-id="b4a16-106">To provide a more seamless user experience, you can use the **(Preview) Full page apps** feature to embed those third-party apps directly into your Finance and Operations apps (provided that the third-party apps allow themselves to be embedded).</span></span> <span data-ttu-id="b4a16-107">这样，用户可以访问所需的网站和应用，而无需切换选项卡或窗口。</span><span class="sxs-lookup"><span data-stu-id="b4a16-107">In this way, users can access the websites and apps that they require without having to switch tabs or windows.</span></span>

<span data-ttu-id="b4a16-108">您必须先在“功能管理”中打开 **(预览)整页应用** 功能，然后才能够将第三方应用嵌入产品。</span><span class="sxs-lookup"><span data-stu-id="b4a16-108">Before you can embed third-party apps into the product, you must turn on the **(Preview) Full page apps** feature in Feature management.</span></span> <span data-ttu-id="b4a16-109">然后，您可以使用以下方法之一嵌入第三方应用或网站。</span><span class="sxs-lookup"><span data-stu-id="b4a16-109">You can then use one of the following methods to embed a third-party app or website.</span></span> <span data-ttu-id="b4a16-110">这些方法类似于将 Microsoft Power Apps 中的画布应用嵌入到 Finance and Operations 应用的方法。</span><span class="sxs-lookup"><span data-stu-id="b4a16-110">These methods are analogous to the methods that are used to embed canvas apps from Microsoft Power Apps into Finance and Operations apps.</span></span>

- <span data-ttu-id="b4a16-111">将应用或网站作为新的选项卡（数据透视选项卡、快速选项卡、边栏选项卡或工作区部分）嵌入到现有页面。</span><span class="sxs-lookup"><span data-stu-id="b4a16-111">Embed the app or website on an existing page as a new tab page (pivot tab, FastTab, blade, or workspace section).</span></span>
- <span data-ttu-id="b4a16-112">从仪表板为应用或网站创建新的整页体验。</span><span class="sxs-lookup"><span data-stu-id="b4a16-112">Create a new full-page experience for the app or website from the dashboard.</span></span>

## <a name="embed-a-website-on-an-existing-page"></a><span data-ttu-id="b4a16-113">在现有页面上嵌入网站</span><span class="sxs-lookup"><span data-stu-id="b4a16-113">Embed a website on an existing page</span></span>

<span data-ttu-id="b4a16-114">如果要使用嵌入式应用补充系统中的现有页面，请使用此过程。</span><span class="sxs-lookup"><span data-stu-id="b4a16-114">Use this procedure if you want to supplement an existing page in the system with an embedded app.</span></span>

1. <span data-ttu-id="b4a16-115">打开要在其中嵌入应用的页面。</span><span class="sxs-lookup"><span data-stu-id="b4a16-115">Open the page where you want to embed the app.</span></span>
2. <span data-ttu-id="b4a16-116">打开 **添加应用** 窗格：</span><span class="sxs-lookup"><span data-stu-id="b4a16-116">Open the **Add an app** pane:</span></span>

    1. <span data-ttu-id="b4a16-117">选择 **设置**，然后选择 **个性化** 打开 **个性化** 工具栏。</span><span class="sxs-lookup"><span data-stu-id="b4a16-117">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
    2. <span data-ttu-id="b4a16-118">选择 **更多 \> 添加应用**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-118">Select **More \> Add an app**.</span></span>

3. <span data-ttu-id="b4a16-119">选择页面上要添加应用的区域。</span><span class="sxs-lookup"><span data-stu-id="b4a16-119">Select the region of the page where you want to add the app.</span></span> <span data-ttu-id="b4a16-120">此区域必须是数据透视选项卡、快速选项卡、边栏选项卡或工作区部分的 *选项卡容器*。</span><span class="sxs-lookup"><span data-stu-id="b4a16-120">This region must be a *tab container* for a pivot tab, FastTab, blade, or workspace section.</span></span>
4. <span data-ttu-id="b4a16-121">选择 **网站**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-121">Select **Website**.</span></span>
5. <span data-ttu-id="b4a16-122">配置嵌入的应用：</span><span class="sxs-lookup"><span data-stu-id="b4a16-122">Configure the embedded app:</span></span>

    - <span data-ttu-id="b4a16-123">**名称** – 输入应为包含嵌入式应用的选项卡显示的文本。</span><span class="sxs-lookup"><span data-stu-id="b4a16-123">**Name** – Enter the text that should be shown for the tab that contains the embedded app.</span></span> <span data-ttu-id="b4a16-124">通常，您会希望此文本成为应用的名称。</span><span class="sxs-lookup"><span data-stu-id="b4a16-124">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="b4a16-125">**URL** – 指定应用的位置。</span><span class="sxs-lookup"><span data-stu-id="b4a16-125">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="b4a16-126">出于安全原因，URL 必须使用安全超文本传输协议 (HTTPS)。</span><span class="sxs-lookup"><span data-stu-id="b4a16-126">For security reasons, the URL must use Hypertext Transfer Protocol Secure (HTTPS).</span></span>
    > - <span data-ttu-id="b4a16-127">必须将应用或网站配置为允许被嵌入。</span><span class="sxs-lookup"><span data-stu-id="b4a16-127">The app or website must be configured to allow itself to be embedded.</span></span>

6. <span data-ttu-id="b4a16-128">选择 **保存** 将应用嵌入页面。</span><span class="sxs-lookup"><span data-stu-id="b4a16-128">Select **Save** to embed the app on the page.</span></span> <span data-ttu-id="b4a16-129">应用将被添加为组中的最后一个选项卡或部分。</span><span class="sxs-lookup"><span data-stu-id="b4a16-129">The app is added as the last tab or section in the group.</span></span>
7. <span data-ttu-id="b4a16-130">确认应用按预期显示。</span><span class="sxs-lookup"><span data-stu-id="b4a16-130">Confirm that the app appears as expected.</span></span> <span data-ttu-id="b4a16-131">如果应用未呈现，请参阅本主题后面的[故障排除](#troubleshooting)一节。</span><span class="sxs-lookup"><span data-stu-id="b4a16-131">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>
8. <span data-ttu-id="b4a16-132">打开视图选择器，选择 **保存**（如果应用应与当前视图关联）或 **另存为**（将应用保存到其他视图）。</span><span class="sxs-lookup"><span data-stu-id="b4a16-132">Open the view selector, and select either **Save** (if the app should be associated with the current view) or **Save as** (to save the app to a different view).</span></span>

    <span data-ttu-id="b4a16-133">如果页面没有视图选择器（例如，如果页面是对话框或工作区），可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="b4a16-133">If the page doesn't have a view selector (for example, if the page is a dialog box or a workspace), you can skip this step.</span></span>

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a><span data-ttu-id="b4a16-134">从仪表板将网站嵌入为整页体验</span><span class="sxs-lookup"><span data-stu-id="b4a16-134">Embed a website as a full-page experience from the dashboard</span></span>

<span data-ttu-id="b4a16-135">如果您要嵌入的应用与现有页面不相关，或者您只想在 Finance and Operations 应用中获得该应用的整页体验，请使用此过程。</span><span class="sxs-lookup"><span data-stu-id="b4a16-135">Use this procedure if the app that you want to embed isn't related to an existing page, or if you just want a full-page experience for the app inside the Finance and Operations app.</span></span>

1. <span data-ttu-id="b4a16-136">打开仪表板。</span><span class="sxs-lookup"><span data-stu-id="b4a16-136">Open the dashboard.</span></span>
2. <span data-ttu-id="b4a16-137">选择并按住（或右键单击）页面，选择 **个性化**，然后选择 **添加页面**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-137">Select and hold (or right-click) the page, select **Personalize**, and then select **Add a page**.</span></span>
3. <span data-ttu-id="b4a16-138">在 **添加页面** 窗格中，选择 **网站**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-138">In the **Add a page** pane, select **Website**.</span></span>
4. <span data-ttu-id="b4a16-139">配置嵌入的应用：</span><span class="sxs-lookup"><span data-stu-id="b4a16-139">Configure the embedded app:</span></span>

    - <span data-ttu-id="b4a16-140">**名称** – 在仪表板上输入为嵌入的应用添加的磁贴上应显示的文本。</span><span class="sxs-lookup"><span data-stu-id="b4a16-140">**Name** – Enter the text that should be shown on the tile that is added for the embedded app on the dashboard.</span></span> <span data-ttu-id="b4a16-141">通常，您会希望此文本成为应用的名称。</span><span class="sxs-lookup"><span data-stu-id="b4a16-141">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="b4a16-142">**URL** – 指定应用的位置。</span><span class="sxs-lookup"><span data-stu-id="b4a16-142">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="b4a16-143">出于安全原因，URL 必须使用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="b4a16-143">For security reasons, the URL must use HTTPS.</span></span>
    > - <span data-ttu-id="b4a16-144">必须将应用或网站配置为允许被嵌入。</span><span class="sxs-lookup"><span data-stu-id="b4a16-144">The app or website must be configured to allow itself to be embedded.</span></span>

5. <span data-ttu-id="b4a16-145">选择 **保存** 将应用作为新磁贴添加到仪表板。</span><span class="sxs-lookup"><span data-stu-id="b4a16-145">Select **Save** to add the app to the dashboard as a new tile.</span></span>
6. <span data-ttu-id="b4a16-146">选择仪表板上的新磁贴，确认应用按预期显示。</span><span class="sxs-lookup"><span data-stu-id="b4a16-146">Select the new tile on the dashboard, and confirm that the app appears as expected.</span></span> <span data-ttu-id="b4a16-147">如果应用未呈现，请参阅本主题后面的[故障排除](#troubleshooting)一节。</span><span class="sxs-lookup"><span data-stu-id="b4a16-147">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>

## <a name="sharing-embedded-apps"></a><span data-ttu-id="b4a16-148">共享嵌入的应用</span><span class="sxs-lookup"><span data-stu-id="b4a16-148">Sharing embedded apps</span></span>

<span data-ttu-id="b4a16-149">使用上一节中介绍的方法之一嵌入应用后，您可能希望与系统中的其他用户共享视图。</span><span class="sxs-lookup"><span data-stu-id="b4a16-149">After you've embedded an app by using one of the methods that are described in the previous sections, you might want to share the view with other users in the system.</span></span> <span data-ttu-id="b4a16-150">要共享嵌入的应用，请使用以下方法之一：</span><span class="sxs-lookup"><span data-stu-id="b4a16-150">To share an embedded app, use one of the following methods:</span></span>

- <span data-ttu-id="b4a16-151">**发布视图（推荐）：** 如果嵌入的应用已保存到视图，共享应用的推荐的首选方法是将视图发布给具有适当安全角色的用户。</span><span class="sxs-lookup"><span data-stu-id="b4a16-151">**Publish the view (Recommended):** If the embedded app has been saved to a view, the recommended and preferred way to share it is to publish the view to users who have the appropriate security roles.</span></span> <span data-ttu-id="b4a16-152">然后，具有发布视图所针对的安全角色的所有用户都会在 Finance and Operations 应用中看到该应用。</span><span class="sxs-lookup"><span data-stu-id="b4a16-152">Then, all users who have the security roles that are targeted by the published view will see the app in Finance and Operations apps.</span></span> <span data-ttu-id="b4a16-153">有关如何发布视图的详细信息，请参阅[发布视图](saved-views.md#publishing-views)。</span><span class="sxs-lookup"><span data-stu-id="b4a16-153">For more information about how to publish a view, see [Publishing views](saved-views.md#publishing-views).</span></span>

    <span data-ttu-id="b4a16-154">您还可以从仪表板发布已嵌入为整页体验的应用。</span><span class="sxs-lookup"><span data-stu-id="b4a16-154">You can also publish an app that has been embedded as a full-page experience from the dashboard.</span></span> <span data-ttu-id="b4a16-155">在仪表板上，选择并按住（或右键单击）与应用关联的磁贴，选择 **个性化**，然后选择 **发布页面**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-155">On the dashboard, select and hold (or right-click) the tile that is associated with the app, select **Personalize**, and then select **Publish page**.</span></span> <span data-ttu-id="b4a16-156">当前，您只能发布给安全角色。</span><span class="sxs-lookup"><span data-stu-id="b4a16-156">Currently, you can publish only to security roles.</span></span> <span data-ttu-id="b4a16-157">但是，向法人发布的功能会在该功能正式发布之前添加。</span><span class="sxs-lookup"><span data-stu-id="b4a16-157">However, the capability to publish to legal entities will be added before the feature becomes generally available.</span></span>

- <span data-ttu-id="b4a16-158">**复制个性化：** 对于不支持视图的页面（例如，对话框或工作区），或者对于整页应用体验，您可以将个性化设置复制给适当的用户。</span><span class="sxs-lookup"><span data-stu-id="b4a16-158">**Copy the personalization:** For pages that don't support views (for example, dialog boxes or workspaces), or for the full-page app experience, you can copy the personalization to the appropriate users.</span></span> <span data-ttu-id="b4a16-159">有关详细信息，请参阅[共享个性化](personalize-user-experience.md#sharing-personalizations)。</span><span class="sxs-lookup"><span data-stu-id="b4a16-159">For more information, see [Sharing personalizations](personalize-user-experience.md#sharing-personalizations).</span></span>

## <a name="viewing-embedded-apps"></a><span data-ttu-id="b4a16-160">查看嵌入的应用</span><span class="sxs-lookup"><span data-stu-id="b4a16-160">Viewing embedded apps</span></span>

<span data-ttu-id="b4a16-161">要在 Finance and Operations 应用中的页面上查看嵌入的应用，打开包含嵌入的应用的页面。</span><span class="sxs-lookup"><span data-stu-id="b4a16-161">To view an embedded app on a page in Finance and Operations apps, open the page that has the embedded app.</span></span> <span data-ttu-id="b4a16-162">请记住，在有些页面上，可以使用标准操作窗格上的 **Power Apps** 按钮访问嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="b4a16-162">Remember that, on some pages, embedded apps can be accessed by using the **Power Apps** button on the standard Action Pane.</span></span> <span data-ttu-id="b4a16-163">或者，它们可以作为新选项卡、快速选项卡或边栏选项卡，或者工作区中的新部分直接显示在页面上。</span><span class="sxs-lookup"><span data-stu-id="b4a16-163">Alternatively, they might appear directly on the page as a new tab, FastTab, or blade, or as a new section in a workspace.</span></span>

## <a name="editing-or-removing-embedded-apps"></a><span data-ttu-id="b4a16-164">编辑或删除嵌入的应用</span><span class="sxs-lookup"><span data-stu-id="b4a16-164">Editing or removing embedded apps</span></span>

<span data-ttu-id="b4a16-165">将应用嵌入页面后，您可能必须编辑其配置（例如，更改部分标签或 URL）。</span><span class="sxs-lookup"><span data-stu-id="b4a16-165">After an app has been embedded on a page, you might have to edit its configuration (for example, by changing the section label or the URL).</span></span> <span data-ttu-id="b4a16-166">或者，您可能必须将其从页面中删除。</span><span class="sxs-lookup"><span data-stu-id="b4a16-166">Alternatively, you might have to remove it from the page.</span></span> <span data-ttu-id="b4a16-167">使用以下过程之一来编辑嵌入的应用的配置或将其完全删除。</span><span class="sxs-lookup"><span data-stu-id="b4a16-167">Use one of the following procedures to edit the configuration of an embedded app or remove it completely.</span></span>

### <a name="apps-that-are-embedded-on-existing-pages"></a><span data-ttu-id="b4a16-168">嵌入到现有页面的应用</span><span class="sxs-lookup"><span data-stu-id="b4a16-168">Apps that are embedded on existing pages</span></span>

1. <span data-ttu-id="b4a16-169">打开嵌入了应用的页面。</span><span class="sxs-lookup"><span data-stu-id="b4a16-169">Open the page where the app is embedded.</span></span>
2. <span data-ttu-id="b4a16-170">选择 **设置**，然后选择 **个性化** 打开 **个性化** 工具栏。</span><span class="sxs-lookup"><span data-stu-id="b4a16-170">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
3. <span data-ttu-id="b4a16-171">选择 **选择** 工具，然后选择嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="b4a16-171">Select the **Select** tool, and then select the embedded app.</span></span>
4. <span data-ttu-id="b4a16-172">要编辑应用，对其配置进行所需的更改，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-172">To edit the app, make the required changes to its configuration, and then select **Save**.</span></span>

    <span data-ttu-id="b4a16-173">或者，要删除应用，选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-173">Alternatively, to remove the app, select **Delete**.</span></span>

5. <span data-ttu-id="b4a16-174">重新保存或重新发布视图。</span><span class="sxs-lookup"><span data-stu-id="b4a16-174">Re-save or republish the view.</span></span> <span data-ttu-id="b4a16-175">请注意，如果您离开页面时未明确保存视图，将不会保留您在 **编辑网站** 窗格中执行的任何操作。</span><span class="sxs-lookup"><span data-stu-id="b4a16-175">Note that if you leave the page without explicitly saving the view, none of the actions that you performed in the **Edit website** pane will be maintained.</span></span>

### <a name="apps-that-are-embedded-from-the-dashboard"></a><span data-ttu-id="b4a16-176">从仪表板嵌入的应用</span><span class="sxs-lookup"><span data-stu-id="b4a16-176">Apps that are embedded from the dashboard</span></span>

1. <span data-ttu-id="b4a16-177">打开仪表板。</span><span class="sxs-lookup"><span data-stu-id="b4a16-177">Open the dashboard.</span></span>
2. <span data-ttu-id="b4a16-178">选择并按住（或右键单击）与嵌入的应用关联的磁贴，然后选择 **个性化**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-178">Select and hold (or right-click) the tile that is associated with the embedded app, and then select **Personalize**.</span></span>
3. <span data-ttu-id="b4a16-179">要编辑应用，选择 **编辑页面**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-179">To edit the app, select **Edit page**.</span></span> <span data-ttu-id="b4a16-180">在 **编辑网站** 窗格中，对应用配置进行所需的更改，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-180">In the **Edit website** pane, make the required changes to the app configuration, and then select **Save**.</span></span>

    <span data-ttu-id="b4a16-181">或者，要删除应用，选择 **删除页面**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-181">Alternatively, to remove the app, select **Remove page**.</span></span>

## <a name="appendix"></a><span data-ttu-id="b4a16-182">附录</span><span class="sxs-lookup"><span data-stu-id="b4a16-182">Appendix</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="b4a16-183">疑难解答</span><span class="sxs-lookup"><span data-stu-id="b4a16-183">Troubleshooting</span></span>

<span data-ttu-id="b4a16-184">如果将网站嵌入到 Finance and Operation 应用中后网站未正确呈现，或者如果您收到错误消息，指出 URL 被拒绝连接，说明该网站可能已配置为阻止被嵌入到 iframe 中。</span><span class="sxs-lookup"><span data-stu-id="b4a16-184">If a website isn't rendered correctly after it's embedded in a Finance and Operation app, or if you receive an error message that states that the URL was denied a connection, the website is probably configured to prevent itself from being embedded in an iframe.</span></span> <span data-ttu-id="b4a16-185">请按照以下步骤确定网站是否可以嵌入。</span><span class="sxs-lookup"><span data-stu-id="b4a16-185">Follow these steps to determine whether the website can be embedded.</span></span>

1. <span data-ttu-id="b4a16-186">打开您使用的浏览器的开发人员工具。</span><span class="sxs-lookup"><span data-stu-id="b4a16-186">Open the developer tools for the browser that you're using.</span></span>
2. <span data-ttu-id="b4a16-187">在 **网络** 选项卡上，从嵌入的站点中找到并选择响应。</span><span class="sxs-lookup"><span data-stu-id="b4a16-187">On the **Network** tab, find and select the response from the embedded site.</span></span>
3. <span data-ttu-id="b4a16-188">在 **标头** 选项卡上的 **响应标头** 下，查找 **x-frame-options**。</span><span class="sxs-lookup"><span data-stu-id="b4a16-188">On the **Headers** tab, under **Response Headers**, look for **x-frame-options**.</span></span> <span data-ttu-id="b4a16-189">如果响应标头中存在 **x-frame-options**，并且其值为 **DENY** 或 **SAMEORIGIN**，网站当前无法嵌入。</span><span class="sxs-lookup"><span data-stu-id="b4a16-189">If **x-frame-options** exists in the response headers, and has a value of **DENY** or **SAMEORIGIN**, the website can't currently be embedded.</span></span> <span data-ttu-id="b4a16-190">您必须与应用的所有者合作来将它安全地嵌入。</span><span class="sxs-lookup"><span data-stu-id="b4a16-190">You will have to work with the owner of the app to enable it to be safely embedded.</span></span>

### <a name="developer-modeling-a-website-on-a-form"></a><span data-ttu-id="b4a16-191">[开发人员] 在窗体上为网站建模</span><span class="sxs-lookup"><span data-stu-id="b4a16-191">[Developer] Modeling a website on a form</span></span>

<span data-ttu-id="b4a16-192">本主题的重点是通过个性化嵌入第三方应用或网站，但开发人员也可以使用 Visual Studio 开发体验将它们嵌入到窗体中。</span><span class="sxs-lookup"><span data-stu-id="b4a16-192">Although this topic is focused on embedding third-party apps or websites through personalization, developers can also embed them in a form by using the Visual Studio development experience.</span></span> <span data-ttu-id="b4a16-193">只需将 **WebsiteHostControl** 控件添加到窗体中。</span><span class="sxs-lookup"><span data-stu-id="b4a16-193">Just add a **WebsiteHostControl** control to the form.</span></span> <span data-ttu-id="b4a16-194">控件可用的元数据属性提供与个性化体验相同的功能。</span><span class="sxs-lookup"><span data-stu-id="b4a16-194">The metadata properties that are available for the control provide the same capabilities as the personalization experience.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
