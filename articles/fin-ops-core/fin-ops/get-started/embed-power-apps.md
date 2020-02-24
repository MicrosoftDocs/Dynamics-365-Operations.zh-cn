---
title: 嵌入 Power Apps
description: 此主题描述如何将 Power Apps 嵌入到客户端以细分该产品的功能。
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 9585d5a399ebf45b0ad7640f3c4e48d8afc46cd8
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017720"
---
# <a name="embed-microsoft-power-apps"></a><span data-ttu-id="93702-103">嵌入 Microsoft Power Apps</span><span class="sxs-lookup"><span data-stu-id="93702-103">Embed Microsoft Power Apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93702-104">Finance and Operations 支持与 Microsoft Power Apps 集成，这项服务供开发人员和非技术用户为移动设备、平板电脑和 Web 构建自定义企业应用，而无需编写代码。</span><span class="sxs-lookup"><span data-stu-id="93702-104">Finance and Operations supports integration with Microsoft Power Apps, a service for developers and non-technical users to build custom business apps for mobile devices, tablets, and the web without writing code.</span></span> <span data-ttu-id="93702-105">以生，由您、您的组织或者更广泛的生态系统开发的 Power Apps 可以嵌入到 Finance and Operations 应用程序以细分产品的功能。</span><span class="sxs-lookup"><span data-stu-id="93702-105">Power Apps developed by you, your organization, or the broader ecosystem can then be embedded in Finance and Operations apps to augment the product's functionality.</span></span> <span data-ttu-id="93702-106">例如，您可以利用 Power Apps 构建应用以使用从其他系统检索的信息补充 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="93702-106">For example, you might build an app from Power Apps to supplement a Finance and Operations app with information retrieved from another system.</span></span>

<span data-ttu-id="93702-107">若要了解有关嵌入 Power Apps 的详细信息，请观看视频短片[如何嵌入 Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY)。</span><span class="sxs-lookup"><span data-stu-id="93702-107">To learn more about embedding Power Apps, watch the short [How to embed Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) video.</span></span>

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a><span data-ttu-id="93702-108">将 Power Apps 中的嵌入应用添加到页面中</span><span class="sxs-lookup"><span data-stu-id="93702-108">Adding an embedded app from Power Apps to a page</span></span>

### <a name="overview"></a><span data-ttu-id="93702-109">概览</span><span class="sxs-lookup"><span data-stu-id="93702-109">Overview</span></span>

<span data-ttu-id="93702-110">在将 Power Apps 中的应用嵌入到客户端之前，您首先需要使用所需的视觉对象和/或功能找到或构建应用。</span><span class="sxs-lookup"><span data-stu-id="93702-110">Before embedding an app fro Power Apps into the client, you first need to find or build an app with the desired visuals and/or functionality.</span></span> <span data-ttu-id="93702-111">我们在这里将不介绍构建应用的详细流程。</span><span class="sxs-lookup"><span data-stu-id="93702-111">We will not describe the detailed process for building apps here.</span></span> <span data-ttu-id="93702-112">如果您是 Power Apps 的新用户，[Power Apps 简介](https://docs.microsoft.com/powerapps/getting-started)主题是一个好的起始点。</span><span class="sxs-lookup"><span data-stu-id="93702-112">The [Introduction to Power Apps](https://docs.microsoft.com/powerapps/getting-started) topic is a good starting point if you are new to Power Apps.</span></span>

<span data-ttu-id="93702-113">当您准备嵌入特定应用时，您可以选择以下两种方式之一在页面上访问应用，选择更适合您的场景的路线。</span><span class="sxs-lookup"><span data-stu-id="93702-113">When you are ready to embed a specific app, you can choose between one of two ways of accessing the app on a page, whichever route better fits your scenario.</span></span> <span data-ttu-id="93702-114">第一种方法是通过已添加到标准操作窗格的 Power Apps 按钮。</span><span class="sxs-lookup"><span data-stu-id="93702-114">The first way is through the Power Apps button that has been added to the standard Action Pane.</span></span> <span data-ttu-id="93702-115">使用此机制添加的应用在 Power Apps 菜单按钮内将显示为菜单项。</span><span class="sxs-lookup"><span data-stu-id="93702-115">Apps added using this mechanism will appear as menu items inside the Power Apps menu button.</span></span> <span data-ttu-id="93702-116">一旦选中，这些菜单项中的每一项都将打开包含嵌入的应用的侧窗格。</span><span class="sxs-lookup"><span data-stu-id="93702-116">When selected, each of these menu items will open a side pane that contains the embedded app.</span></span> <span data-ttu-id="93702-117">或者，您可以选择直接在页面上将应用嵌入为新选项卡、快速选项卡、边栏选项卡，或者显示为工作区的新部分。</span><span class="sxs-lookup"><span data-stu-id="93702-117">Alternatively, you may choose to embed an app directly on a page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span>

<span data-ttu-id="93702-118">配置嵌入的应用时，您可以选择您希望将其作为上下文发送到应用的单个字段。</span><span class="sxs-lookup"><span data-stu-id="93702-118">When configuring your embedded app, you can select a single field that you want to send as context to the app.</span></span> <span data-ttu-id="93702-119">这允许应用基于您正在查看的数据作出响应。</span><span class="sxs-lookup"><span data-stu-id="93702-119">This allows the app to be responsive based on the data that you are currently viewing.</span></span>

### <a name="details"></a><span data-ttu-id="93702-120">明细</span><span class="sxs-lookup"><span data-stu-id="93702-120">Details</span></span>

<span data-ttu-id="93702-121">以下说明显示如何将 Power Apps 中的应用嵌入到 Web 客户端。</span><span class="sxs-lookup"><span data-stu-id="93702-121">The following instructions show how to embed an app from Power Apps into the web client.</span></span>

1. <span data-ttu-id="93702-122">转到您希望嵌入应用的页面。</span><span class="sxs-lookup"><span data-stu-id="93702-122">Go to the page where you would like to embed the app.</span></span> <span data-ttu-id="93702-123">这与包含需要作为输入传送到应用的任何数据的页面是同一页。</span><span class="sxs-lookup"><span data-stu-id="93702-123">This will be the same page that contains any data that needs to be passed to the app as as input.</span></span>
2. <span data-ttu-id="93702-124">打开**从 Power Apps 中添加应用**窗格：</span><span class="sxs-lookup"><span data-stu-id="93702-124">Open the **Add an app from Power Apps** pane:</span></span>

    - <span data-ttu-id="93702-125">单击**选项**，然后选择**个性化设置此页面**。</span><span class="sxs-lookup"><span data-stu-id="93702-125">Click **Options**, and then select **Personalize this page**.</span></span> <span data-ttu-id="93702-126">在**插入**菜单下，选择 **Power Apps**。</span><span class="sxs-lookup"><span data-stu-id="93702-126">Under the **Insert** menu, choose **Power Apps**.</span></span> <span data-ttu-id="93702-127">最后，选择要添加应用的区域。</span><span class="sxs-lookup"><span data-stu-id="93702-127">Finally, select the region where you would like to add the app.</span></span> <span data-ttu-id="93702-128">如果要在 Power Apps 菜单按钮下嵌入应用，选择操作窗格。</span><span class="sxs-lookup"><span data-stu-id="93702-128">If you want to embed the app under the Power Apps menu button, choose the Action Pane.</span></span> <span data-ttu-id="93702-129">如果要将应用直接嵌入到页面上，选择相应的选项卡、快速选项卡、边栏选项卡或部分（如果您处于工作区）。</span><span class="sxs-lookup"><span data-stu-id="93702-129">If you want to embed the app directly onto the page, choose the appropriate tab, FastTab, blade, or section (if you're on a workspace).</span></span>
    - <span data-ttu-id="93702-130">如果将使用 Power Apps 菜单按钮访问应用，您可以单击标准操作窗格中的 **Power Apps** 菜单按钮，然后选择**添加应用**。</span><span class="sxs-lookup"><span data-stu-id="93702-130">If the app will be accessed using the Power Apps menu button, you can alternatively click the **Power Apps** menu button in the standard Action Pane, and then select **Add an app**.</span></span>

3. <span data-ttu-id="93702-131">配置嵌入的应用：</span><span class="sxs-lookup"><span data-stu-id="93702-131">Configure the embedded app:</span></span>

    - <span data-ttu-id="93702-132">**名称**字段指示为将包含嵌入的应用的按钮或选项卡显示的文本。</span><span class="sxs-lookup"><span data-stu-id="93702-132">The **Name** field indicates the text shown for the button or tab that will contain the embedded app.</span></span> <span data-ttu-id="93702-133">通常，您可能要在此字段中重复应用的名称。</span><span class="sxs-lookup"><span data-stu-id="93702-133">Oftentimes, you may want to repeat the name of the app in this field.</span></span>
    - <span data-ttu-id="93702-134">**应用 ID** 是您要嵌入的应用的 GUID。</span><span class="sxs-lookup"><span data-stu-id="93702-134">**App ID** is the GUID for the app  that you want to embed.</span></span> <span data-ttu-id="93702-135">若要检索此值，在 [web.powerapps.com](https://web.powerapps.com) 上找到应用，然后在**详细信息**下找到**应用 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="93702-135">To retrieve this value, find the app on [web.powerapps.com](https://web.powerapps.com) and then locate the **App ID** field under **Details**.</span></span>
    - <span data-ttu-id="93702-136">对于**应用的输入上下文**，您可以有选择性地选择包含您要作为输入传送到应用的数据的字段。</span><span class="sxs-lookup"><span data-stu-id="93702-136">For **Input context for the app**, you can optionally select the field that contains the data that you want to pass to the app as input.</span></span> <span data-ttu-id="93702-137">请参阅本主题后面名为[构建利用 Finance and Operations 应用的数据的应用](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps)部分，了解有关应用如何访问发送自 Finance and Operations 应用的数据的详细信息。</span><span class="sxs-lookup"><span data-stu-id="93702-137">See the section later in this topic titled [Building apps that leverages data from Finance and Operations apps](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps) for details on how the app can access the data sent from Finance and Operations apps.</span></span>
    - <span data-ttu-id="93702-138">选择与您嵌入的应用类型匹配的**应用程序大小**。</span><span class="sxs-lookup"><span data-stu-id="93702-138">Choose the **Application size** that matches the type of app that you're embedding.</span></span> <span data-ttu-id="93702-139">为针对移动设备构建的应用选择**窄**，为平板电脑构建的应用选择**宽**。</span><span class="sxs-lookup"><span data-stu-id="93702-139">Select **Thin** for apps built for mobile devices, and **Wide** for apps built for tablets.</span></span> <span data-ttu-id="93702-140">这将确保为嵌入的应用分配足够的空间量。</span><span class="sxs-lookup"><span data-stu-id="93702-140">This ensures a sufficient amount of space is allotted for the embedded app.</span></span>
    - <span data-ttu-id="93702-141">**法人**快速选项卡提供选择应用可用于哪些法人的功能。</span><span class="sxs-lookup"><span data-stu-id="93702-141">The **Legal entities** FastTab provides the ability to choose which legal entities the app is available for.</span></span> <span data-ttu-id="93702-142">默认让所有法人都能访问应用。</span><span class="sxs-lookup"><span data-stu-id="93702-142">The default is to make the app accessible to all legal entities.</span></span> <span data-ttu-id="93702-143">此选项仅在[保存的视图](saved-views.md)功能已禁用时才可用。</span><span class="sxs-lookup"><span data-stu-id="93702-143">This option is only available when the [Saved views](saved-views.md) feature is disabled.</span></span> 

4. <span data-ttu-id="93702-144">在确认配置正确后，请单击**插入**在页面上嵌入 Power App。</span><span class="sxs-lookup"><span data-stu-id="93702-144">After confirming that the configuration is correct, click **Insert** to embed the Power App on the page.</span></span> <span data-ttu-id="93702-145">系统将提示您刷新浏览器以查看嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="93702-145">You will be prompted to refresh the browser in order to see the embedded app.</span></span>

## <a name="sharing-an-embedded-app"></a><span data-ttu-id="93702-146">共享嵌入的应用</span><span class="sxs-lookup"><span data-stu-id="93702-146">Sharing an embedded app</span></span>

<span data-ttu-id="93702-147">在页面上嵌入应用并确认它能够正确处理从页面传递的所有数据上下文后，您可能希望与系统中的其他用户共享此应用。</span><span class="sxs-lookup"><span data-stu-id="93702-147">After you have embedded app on a page and confirmed that it is working correctly with any data context passed from the page, you might want to share this with other users in the system.</span></span> <span data-ttu-id="93702-148">可使用本产品的个性化功能以两种不同的方法达到此目的：</span><span class="sxs-lookup"><span data-stu-id="93702-148">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="93702-149">建议的方案是通过系统管理员，因为系统管理员可以将个性化设置推送给所有用户或一小部分用户。</span><span class="sxs-lookup"><span data-stu-id="93702-149">The recommended scenario is through the system administrator, who can push a personalization to all users or a subset of users.</span></span>
- <span data-ttu-id="93702-150">也可以导出页面的个性化设置，将其发送给一位或多位用户，然后请这些用户分别导入那些更改。</span><span class="sxs-lookup"><span data-stu-id="93702-150">Alternatively, you can export your page's personalizations, send them to one or more users, and have each of those users import those changes.</span></span> <span data-ttu-id="93702-151">个性化工具栏具有允许您导出和导入个性化的操作。</span><span class="sxs-lookup"><span data-stu-id="93702-151">The personalization toolbar has actions that allow you to export and import personalizations.</span></span>

<span data-ttu-id="93702-152">有关产品中的个性化功能以及如何使用的更多详细信息，请参阅[打造个性化的用户体验](personalize-user-experience.md)。</span><span class="sxs-lookup"><span data-stu-id="93702-152">See [Personalize the user experience](personalize-user-experience.md) for more details about the personalization capabilities in the product and how to use them.</span></span>

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a><span data-ttu-id="93702-153">构建一个利用从 Finance and Operations 应用中发送的数据的应用</span><span class="sxs-lookup"><span data-stu-id="93702-153">Building an app that leverages data sent from Finance and Operations apps</span></span>

<span data-ttu-id="93702-154">从将嵌入到 Finance and Operations 应用中的 Power Apps 中构建应用的重要部分将使用该应用程序中的输入数据。</span><span class="sxs-lookup"><span data-stu-id="93702-154">An important part of building an app from Power Apps that will be embedded in a Finance and Operations app is utilizing the input data from that application.</span></span> <span data-ttu-id="93702-155">根据 Power Apps 开发经验，可以使用 Param("EntityId") 变量访问从 Finance and Operations 应用传递的输入数据。</span><span class="sxs-lookup"><span data-stu-id="93702-155">From the Power Apps development experience, the input data passed from a Finance and Operations app can be accessed using the Param("EntityId") variable.</span></span>

<span data-ttu-id="93702-156">例如，在应用的 OnStart 功能中，可以将 Finance and Operations 应用的输入数据设置为类似这样的一个变量：</span><span class="sxs-lookup"><span data-stu-id="93702-156">For example, in the OnStart function of the app, you could set the input data from Finance and Operations apps to a variable like this:</span></span>

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a><span data-ttu-id="93702-157">查看应用</span><span class="sxs-lookup"><span data-stu-id="93702-157">Viewing an app</span></span>

<span data-ttu-id="93702-158">若要查看 Finance and Operations 应用中页面上的嵌入应用，只需转到包含嵌入的应用的页面。</span><span class="sxs-lookup"><span data-stu-id="93702-158">To view an embedded app on a page in Finance and Operations apps, simply go to a page with an embedded app.</span></span> <span data-ttu-id="93702-159">回忆一下，应用可以通过标准操作窗格的 Power Apps 按钮访问，或可以在页面上直接显示为新的选项卡、快速选项卡，或在工作区显示为新部分。</span><span class="sxs-lookup"><span data-stu-id="93702-159">Recall that apps can be accessed through the Power Apps button in the standard Action Pane, or can appear directly on the page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span> <span data-ttu-id="93702-160">当用户首次尝试在页面上加载应用时，系统将提示他或她登录到以确保用户有使用应用的相应权限。</span><span class="sxs-lookup"><span data-stu-id="93702-160">When a user first attempts to load an app on a page, he or she will be prompted to sign in to ensure the user has the appropriate permissions to use the app.</span></span>

## <a name="editing-an-embedded-app"></a><span data-ttu-id="93702-161">编辑嵌入的应用</span><span class="sxs-lookup"><span data-stu-id="93702-161">Editing an embedded app</span></span>

<span data-ttu-id="93702-162">在应用嵌入到页面后，可能需要对该应用的配置作一些更改。</span><span class="sxs-lookup"><span data-stu-id="93702-162">After an app has been embedded onto a page, you may need to make some changes to the configuration of the app.</span></span> <span data-ttu-id="93702-163">例如，可能您要修改与嵌入的应用关联的标签，或者已创建新版本应用并且您需要更新应用 ID 以指向最新应用。</span><span class="sxs-lookup"><span data-stu-id="93702-163">For example, perhaps you want to modify the label associated with the embedded app or a new version of the app has been created and you need to update the App ID to point at the latest.</span></span>

<span data-ttu-id="93702-164">执行以下步骤来编辑嵌入的应用的配置：</span><span class="sxs-lookup"><span data-stu-id="93702-164">Follow these steps to edit the configuration of an embedded app:</span></span>

1. <span data-ttu-id="93702-165">转到**编辑应用**窗格。</span><span class="sxs-lookup"><span data-stu-id="93702-165">Go to the **Edit the app** pane.</span></span>

    - <span data-ttu-id="93702-166">如果嵌入的应用通过 Power Apps 菜单按钮访问，右键单击 Power Apps 菜单按钮并选择**个性化**。</span><span class="sxs-lookup"><span data-stu-id="93702-166">If the embedded app is accessed through the Power Apps menu button, right-click on the Power Apps menu button and select **Personalize**.</span></span> <span data-ttu-id="93702-167">选择您想要从**选择应用**下拉菜单配置的应用。</span><span class="sxs-lookup"><span data-stu-id="93702-167">Select the app that you want to configure from the **Select an app** drop-down menu.</span></span>
    - <span data-ttu-id="93702-168">如果嵌入的应用直接出现在页面上，选择**选项**，然后选择**个性化设置此页面**。</span><span class="sxs-lookup"><span data-stu-id="93702-168">If the embedded app appears directly on the page, select **Options**, and then select **Personalize this page**.</span></span> <span data-ttu-id="93702-169">使用**选择**工具，单击嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="93702-169">Using the **Select** tool, click the embedded app.</span></span>

2. <span data-ttu-id="93702-170">对应用配置进行需要的修改，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="93702-170">Make the needed modifications to the app configuration, and then click **Save**.</span></span>

## <a name="removing-an-app"></a><span data-ttu-id="93702-171">移除应用</span><span class="sxs-lookup"><span data-stu-id="93702-171">Removing an app</span></span>

<span data-ttu-id="93702-172">在应用嵌入到页面上后，如果需要，有两种方法可以删除它：</span><span class="sxs-lookup"><span data-stu-id="93702-172">After an app has been embedded onto a page, there are two ways to remove it if needed:</span></span>

- <span data-ttu-id="93702-173">使用此主题前面[编辑嵌入的应用](#editing-an-embedded-power-app)部分中的说明转到**编辑应用**窗格。</span><span class="sxs-lookup"><span data-stu-id="93702-173">Go to the **Edit an app** pane using the instructions from the [Editing an embedded app](#editing-an-embedded-power-app) section earlier in this topic.</span></span> <span data-ttu-id="93702-174">确认窗格显示您要删除的嵌入应用的信息，然后单击**删除**按钮。</span><span class="sxs-lookup"><span data-stu-id="93702-174">Confirm that the pane displays information for the embedded app that you would like to remove, and then click the **Delete** button.</span></span>
- <span data-ttu-id="93702-175">由于嵌入的应用保存为个性化数据，清除页面的个性化也将删除该页面上所有嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="93702-175">Because the embedded app is saved as personalization data, clearing your page's personalization will also remove any embedded apps on that page.</span></span> <span data-ttu-id="93702-176">请注意，清除页面的个性化是永久的，并且无法撤消。</span><span class="sxs-lookup"><span data-stu-id="93702-176">Note that clearing the page's personalization is permanent and cannot be undone.</span></span> <span data-ttu-id="93702-177">若要删除您的页面上的个性化设置，依次选择**选项**、**个性化设置此页面**和**清除**。</span><span class="sxs-lookup"><span data-stu-id="93702-177">To remove your personalizations on a page, select **Options**, and then **Personalize this page**, and finally the **Clear** button.</span></span> <span data-ttu-id="93702-178">刷新您的浏览器后，将删除此页之前的所有个性化设置。</span><span class="sxs-lookup"><span data-stu-id="93702-178">After refreshing your browser, all the previous personalizations for this page will be removed.</span></span> <span data-ttu-id="93702-179">请参阅[打造个性化的用户体验](personalize-user-experience.md)了解有关如何使用个性化设置优化页面的更多信息。</span><span class="sxs-lookup"><span data-stu-id="93702-179">See [Personalize the user experience](personalize-user-experience.md) for more information about how to optimize pages using personalization.</span></span>

## <a name="appendix"></a><span data-ttu-id="93702-180">附录</span><span class="sxs-lookup"><span data-stu-id="93702-180">Appendix</span></span>

### <a name="developer-control-over-where-an-app-can-be-embedded"></a><span data-ttu-id="93702-181">开发人员控制应用可以嵌入的位置</span><span class="sxs-lookup"><span data-stu-id="93702-181">Developer control over where an app can be embedded</span></span>

<span data-ttu-id="93702-182">默认情况下，用户可以在任何页面嵌入应用，要么嵌入在 Power Apps 菜单按钮下，要么作为选项卡、快速选项卡、边栏选项卡或工作区新部分直接嵌入在页面上。</span><span class="sxs-lookup"><span data-stu-id="93702-182">By default, users can embed apps on any page, either under the Power Apps menu button or directly on the page as a tab, FastTab, blade or as a new section in a workspace.</span></span> <span data-ttu-id="93702-183">但是，如果需要，开发人员还可以将此功能配置为只允许在特定页面上嵌入应用，方法如下：</span><span class="sxs-lookup"><span data-stu-id="93702-183">However, if required, developers can also configure this feature to only allow embedding of apps on certain pages by implementing the following methods:</span></span>

- <span data-ttu-id="93702-184">**isPowerAppPersonalizationEnabled** – 如果此方法为特定页面返回 false，那么 Power Apps 菜单按钮不显示，并且用户不能将应用嵌入到此页的任何位置，包括作为选项卡。</span><span class="sxs-lookup"><span data-stu-id="93702-184">**isPowerAppPersonalizationEnabled** – If this method returns false for a specific page, then the Power Apps menu button will not be shown, and users will not be able to embed apps anywhere on this page, including as a tab.</span></span>
- <span data-ttu-id="93702-185">**isPowerAppTabPersonalizationEnabled** – 如果此方法为特定页返回 false，那么用户不能直接在页面上作为选项卡、快速选项卡或全景部分嵌入应用。</span><span class="sxs-lookup"><span data-stu-id="93702-185">**isPowerAppTabPersonalizationEnabled** – If this method returns false for a specific page, then users will not be able to embed apps directly on the page as a tab, FastTab, or panorama section.</span></span> <span data-ttu-id="93702-186">如果允许在页面上嵌入，用户仍可以通过 Power Apps 菜单按钮嵌入应用。</span><span class="sxs-lookup"><span data-stu-id="93702-186">Users will still be able to embed apps through the Power Apps menu button if embedding is allowed on the page.</span></span>

<span data-ttu-id="93702-187">以下示例显示需要通过这两种方法来配置应用可以嵌入的位置的新类。</span><span class="sxs-lookup"><span data-stu-id="93702-187">The following example shows a new class with the two methods needed to configure where apps can be embedded.</span></span>

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
