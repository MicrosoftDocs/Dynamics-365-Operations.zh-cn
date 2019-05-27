---
title: 嵌入 PowerApps 应用程序
description: 此主题描述如何将 PowerApps 嵌入到 Finance and Operations 客户端以细分该产品的功能。
author: jasongre
manager: AnnBe
ms.date: 09/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 262d34cbc50251595d22c27387fbd3f1045d1fbb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552780"
---
# <a name="embed-powerapps-apps"></a><span data-ttu-id="f263f-103">嵌入 PowerApps 应用</span><span class="sxs-lookup"><span data-stu-id="f263f-103">Embed PowerApps apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f263f-104">在平台更新 14 中，Microsoft Dynamics 365 for Finance and Operations 支持与 Microsoft PowerApps 集成，这是一项面向为移动设备、平板电脑和 Web 构建自定义企业应用、而无需编写代码的开发人员和非技术用户的服务。</span><span class="sxs-lookup"><span data-stu-id="f263f-104">In Platform update 14, Microsoft Dynamics 365 for Finance and Operations supports integration with Microsoft PowerApps, a service for developers and non-technical users to build custom business apps for mobile devices, tablets, and the web without writing code.</span></span> <span data-ttu-id="f263f-105">由您、您的组织或者更广泛的生态系统开发的 PowerApps 反之可以嵌入到 Finance and Operations 客户端以细分产品的功能。</span><span class="sxs-lookup"><span data-stu-id="f263f-105">PowerApps developed by you, your organization, or the broader ecosystem can then be embedded in the Finance and Operations client to augment the product's functionality.</span></span> <span data-ttu-id="f263f-106">例如，您可以构建 PowerApp 来使用从其他系统检索的信息补充 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="f263f-106">For example, you might build a PowerApp to supplement Finance and Operations with information retrieved from another system.</span></span>

<span data-ttu-id="f263f-107">若要了解有关嵌入 PowerApp 的详细信息，请观看视频短片[如何在 Dynamics 365 for Finance and Operations 中嵌入 PowerApps](https://www.youtube.com/watch?v=x3qyA1bH-NY)。</span><span class="sxs-lookup"><span data-stu-id="f263f-107">To learn more about embedding PowerApps, watch the short [How to embed PowerApps in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=x3qyA1bH-NY) video.</span></span>

## <a name="adding-an-embedded-powerapp-to-a-page"></a><span data-ttu-id="f263f-108">将嵌入的 PowerApp 添加到页面</span><span class="sxs-lookup"><span data-stu-id="f263f-108">Adding an embedded PowerApp to a page</span></span>

### <a name="overview"></a><span data-ttu-id="f263f-109">概览</span><span class="sxs-lookup"><span data-stu-id="f263f-109">Overview</span></span>

<span data-ttu-id="f263f-110">在将 PowerApp 嵌入到 Finance and Operations 客户端之前，您首先需要使用所需的视觉对象和/或功能找到或构建 PowerApp。</span><span class="sxs-lookup"><span data-stu-id="f263f-110">Before embedding a PowerApp into the Finance and Operations client, you first need to find or build a PowerApp with the desired visuals and/or functionality.</span></span> <span data-ttu-id="f263f-111">我们在这里不介绍构建 PowerApp 的详细流程。</span><span class="sxs-lookup"><span data-stu-id="f263f-111">We will not describe the detailed process for building a PowerApp here.</span></span> <span data-ttu-id="f263f-112">如果您是 PowerApps 的新用户，[PowerApps 简介](https://docs.microsoft.com/powerapps/getting-started)主题是一个好的起始点。</span><span class="sxs-lookup"><span data-stu-id="f263f-112">The [Introduction to PowerApps](https://docs.microsoft.com/powerapps/getting-started) topic is a good starting point if you are new to PowerApps.</span></span>

<span data-ttu-id="f263f-113">当您准备嵌入特定 PowerApp 时，您可以选择以下两种方式之一在页面上访问 PowerApp，选择更适合您的场景的路线。</span><span class="sxs-lookup"><span data-stu-id="f263f-113">When you are ready to embed a specific PowerApp, you can choose between one of two ways of accessing the PowerApp on a page, whichever route better fits your scenario.</span></span> <span data-ttu-id="f263f-114">第一种方法是通过已添加到标准操作窗格的 PowerApps 按钮。</span><span class="sxs-lookup"><span data-stu-id="f263f-114">The first way is through the PowerApps button that has been added to the standard Action Pane.</span></span> <span data-ttu-id="f263f-115">使用此机制添加的 PowerApps 在 PowerApps 菜单按钮内将显示为菜单项。</span><span class="sxs-lookup"><span data-stu-id="f263f-115">PowerApps added using this mechanism will appear as menu items inside the PowerApps menu button.</span></span> <span data-ttu-id="f263f-116">一旦选中，这些菜单项中的每一项都将打开包含嵌入的 PowerApp 的侧窗格。</span><span class="sxs-lookup"><span data-stu-id="f263f-116">When selected, each of these menu items will open a side pane that contains the embedded PowerApp.</span></span> <span data-ttu-id="f263f-117">或者，您可以选择直接在页面上将 PowerApp 显示为新选项卡、快速选项卡、边栏选项卡，或者显示为工作区的新部分。</span><span class="sxs-lookup"><span data-stu-id="f263f-117">Alternatively, you may choose to show a PowerApp directly on a page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span>

<span data-ttu-id="f263f-118">在 Finance and Operations 中配置嵌入的 PowerApp 时，您可以选择您希望将其作为输入发送到 PowerApp 的单个字段。</span><span class="sxs-lookup"><span data-stu-id="f263f-118">When configuring your embedded PowerApp in Finance and Operations, you can select a single field that you want to send as input to the PowerApp.</span></span> <span data-ttu-id="f263f-119">这允许 PowerApp 基于您在 Finance and Operations 中正在查看的数据作出响应。</span><span class="sxs-lookup"><span data-stu-id="f263f-119">This allows the PowerApp to be responsive based on the data that you are currently viewing in Finance and Operations.</span></span>

### <a name="details"></a><span data-ttu-id="f263f-120">明细</span><span class="sxs-lookup"><span data-stu-id="f263f-120">Details</span></span>

<span data-ttu-id="f263f-121">以下说明显示如何将 PowerApp 嵌入到 Finance and Operations Web 客户端。</span><span class="sxs-lookup"><span data-stu-id="f263f-121">The following instructions show how to embed a PowerApp into the Finance and Operations web client.</span></span>

1. <span data-ttu-id="f263f-122">转到您希望嵌入 PowerApp 的页面。</span><span class="sxs-lookup"><span data-stu-id="f263f-122">Go to the page where you would like to embed the PowerApp.</span></span> <span data-ttu-id="f263f-123">这与包含需要作为输入传送到 PowerApp 的任何数据的页面是同一页。</span><span class="sxs-lookup"><span data-stu-id="f263f-123">This will be the same page that contains any data that needs to be passed to the PowerApp as input.</span></span>
2. <span data-ttu-id="f263f-124">打开**插入 PowerApp** 窗格：</span><span class="sxs-lookup"><span data-stu-id="f263f-124">Open the **Insert a PowerApp** pane:</span></span>

    - <span data-ttu-id="f263f-125">单击**选项**，然后选择**个性化设置此窗体**。</span><span class="sxs-lookup"><span data-stu-id="f263f-125">Click **Options**, and then select **Personalize this form**.</span></span> <span data-ttu-id="f263f-126">在**插入**菜单下，选择 **PowerApp**。</span><span class="sxs-lookup"><span data-stu-id="f263f-126">Under the **Insert** menu, choose **PowerApp**.</span></span> <span data-ttu-id="f263f-127">最后，选择要添加 PowerApp 的区域。</span><span class="sxs-lookup"><span data-stu-id="f263f-127">Finally, select the region where you would like to add the PowerApp.</span></span> <span data-ttu-id="f263f-128">如果要在 PowerApp 菜单按钮下嵌入 PowerApps，选择操作窗格。</span><span class="sxs-lookup"><span data-stu-id="f263f-128">If you want to embed the PowerApp under the PowerApps menu button, choose the Action Pane.</span></span> <span data-ttu-id="f263f-129">如果要将 PowerApp 直接嵌入到页面上，选择相应的选项卡、快速选项卡、边栏选项卡或部分（如果您处于工作区）。</span><span class="sxs-lookup"><span data-stu-id="f263f-129">If you want to embed the PowerApp directly onto the page, choose the appropriate tab, FastTab, blade, or section (if you're on a workspace).</span></span>
    - <span data-ttu-id="f263f-130">如果将使用 PowerApps 菜单按钮访问 PowerApp，您可以单击标准操作窗格中的 **PowerApps** 菜单按钮，然后选择**插入 PowerApp**。</span><span class="sxs-lookup"><span data-stu-id="f263f-130">If the PowerApp will be accessed using the PowerApps menu button, you can alternatively click the **PowerApps** menu button in the standard Action Pane, and then select **Insert a PowerApp**.</span></span>

3. <span data-ttu-id="f263f-131">配置嵌入的 PowerApp：</span><span class="sxs-lookup"><span data-stu-id="f263f-131">Configure the embedded PowerApp:</span></span>

    - <span data-ttu-id="f263f-132">**名称**字段指示为要包含嵌入的 PowerApp 的按钮或选项卡显示的文本。</span><span class="sxs-lookup"><span data-stu-id="f263f-132">The **Name** field indicates the text shown for the button or tab that will contain the embedded PowerApp.</span></span> <span data-ttu-id="f263f-133">通常，您可能要在此字段中重复 PowerApp 的名称。</span><span class="sxs-lookup"><span data-stu-id="f263f-133">Oftentimes, you may want to repeat the name of the PowerApp in this field.</span></span>
    - <span data-ttu-id="f263f-134">**应用 ID** 是您要嵌入的 PowerApp 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f263f-134">**App ID** is the GUID for the PowerApp that you want to embed.</span></span> <span data-ttu-id="f263f-135">若要检索此值，在 [web.powerapps.com](https://web.powerapps.com) 上找到 PowerApp，然后在**详细信息**下找到**应用 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="f263f-135">To retrieve this value, find the PowerApp on [web.powerapps.com](https://web.powerapps.com) and then locate the **App ID** field under **Details**.</span></span>
    - <span data-ttu-id="f263f-136">对于 **PowerApp 的输入数据**，您可以有选择性地选择包含您要作为输入传送到 PowerApp 的数据的字段。</span><span class="sxs-lookup"><span data-stu-id="f263f-136">For **Input data for the PowerApp**, you can optionally select the field that contains the data that you want to pass to the PowerApp as input.</span></span> <span data-ttu-id="f263f-137">请参阅本主题后面名为[构建利用 Finance and Operations 的数据的 PowerApp](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) 部分，了解有关 PowerApp 如何访问发送自 Finance and Operations 的数据的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f263f-137">See the section later in this topic titled [Building a PowerApp that leverages data from Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) for details on how the PowerApp can access the data sent from Finance and Operations.</span></span>
    - <span data-ttu-id="f263f-138">选择与您嵌入的 PowerApp 类型匹配的**应用程序大小**。</span><span class="sxs-lookup"><span data-stu-id="f263f-138">Choose the **Application size** that matches the type of PowerApp that you're embedding.</span></span> <span data-ttu-id="f263f-139">为针对移动设备构建的 PowerApps 选择**窄**，为平板电脑构建的 PowerApps 选择**宽**。</span><span class="sxs-lookup"><span data-stu-id="f263f-139">Select **Thin** for PowerApps built for mobile devices, and **Wide** for PowerApps built for tablets.</span></span> <span data-ttu-id="f263f-140">这将确保为嵌入的 PowerApp 分配足够的空间量。</span><span class="sxs-lookup"><span data-stu-id="f263f-140">This ensures a sufficient amount of space is allotted for the embedded PowerApp.</span></span>
    - <span data-ttu-id="f263f-141">**法人**快速选项卡提供选择 PowerApp 可用于哪些法人的功能。</span><span class="sxs-lookup"><span data-stu-id="f263f-141">The **Legal entities** FastTab provides the ability to choose which legal entities the PowerApp is available for.</span></span> <span data-ttu-id="f263f-142">默认显示所有法人中的 PowerApp。</span><span class="sxs-lookup"><span data-stu-id="f263f-142">The default is to show the PowerApp in all legal entities.</span></span>

4. <span data-ttu-id="f263f-143">在确认配置正确后，请单击**插入**在页面上嵌入 PowerApp。</span><span class="sxs-lookup"><span data-stu-id="f263f-143">After confirming that the configuration is correct, click **Insert** to embed the PowerApp on the page.</span></span> <span data-ttu-id="f263f-144">系统将提示您刷新浏览器以查看嵌入的 PowerApp。</span><span class="sxs-lookup"><span data-stu-id="f263f-144">You will be prompted to refresh the browser in order to see the embedded PowerApp.</span></span>

## <a name="sharing-an-embedded-powerapp"></a><span data-ttu-id="f263f-145">共享嵌入的 PowerApp</span><span class="sxs-lookup"><span data-stu-id="f263f-145">Sharing an embedded PowerApp</span></span>

<span data-ttu-id="f263f-146">在页面上嵌入 PowerApp 并确认它能够正确处理从页面传递的所有数据上下文后，您可能希望与系统中的其他用户共享此嵌入的 PowerApp。</span><span class="sxs-lookup"><span data-stu-id="f263f-146">After you have embedded a PowerApp on a page and confirmed that it is working correctly with any data context passed from the page, you might want to share this embedded PowerApp with other users in the system.</span></span> <span data-ttu-id="f263f-147">可使用本产品的个性化功能以两种不同的方法达到此目的：</span><span class="sxs-lookup"><span data-stu-id="f263f-147">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="f263f-148">建议的方案是通过系统管理员，因为系统管理员可以将个性化设置推送给所有用户或一小部分用户。</span><span class="sxs-lookup"><span data-stu-id="f263f-148">The recommended scenario is through the system administrator, who can push a personalization to all users or a subset of users.</span></span>
- <span data-ttu-id="f263f-149">也可以导出页面的个性化设置，将其发送给一位或多位用户，然后请这些用户分别导入那些更改。</span><span class="sxs-lookup"><span data-stu-id="f263f-149">Alternatively, you can export your page's personalizations, send them to one or more users, and have each of those users import those changes.</span></span> <span data-ttu-id="f263f-150">可使用个性化工具栏上的管理选项导出和导入个性化设置。</span><span class="sxs-lookup"><span data-stu-id="f263f-150">The Manage option on the personalization toolbar enables you to export and import personalizations.</span></span>

<span data-ttu-id="f263f-151">有关产品中的个性化功能以及如何使用的更多详细信息，请参阅[打造个性化的用户体验](personalize-user-experience.md)。</span><span class="sxs-lookup"><span data-stu-id="f263f-151">See [Personalize the user experience](personalize-user-experience.md) for more details about the personalization capabilities in the product and how to use them.</span></span>

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a><span data-ttu-id="f263f-152">构建利用发送自 Finance and Operations 的数据的 PowerApp</span><span class="sxs-lookup"><span data-stu-id="f263f-152">Building a PowerApp that leverages data sent from Finance and Operations</span></span>

<span data-ttu-id="f263f-153">构建将嵌入到 Finance and Operations 的 PowerApp 的一个重要部分是使用 Finance and Operations 的输入数据。</span><span class="sxs-lookup"><span data-stu-id="f263f-153">An important part of building a PowerApp that will be embedded in Finance and Operations is utilizing the input data from Finance and Operations.</span></span> <span data-ttu-id="f263f-154">在 PowerApp 内，该输入数据可以使用 Param("EntityId") 变量访问。</span><span class="sxs-lookup"><span data-stu-id="f263f-154">Inside the PowerApp, that input data can be accessed using the Param("EntityId") variable.</span></span>

<span data-ttu-id="f263f-155">例如，在 PowerApp 的 OnStart 功能中，可以将 Finance and Operations 的输入数据设置为类似这样的一个变量：</span><span class="sxs-lookup"><span data-stu-id="f263f-155">For example, in the OnStart function of the PowerApp, you could set the input data from Finance and Operations to a variable like this:</span></span>

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a><span data-ttu-id="f263f-156">查看嵌入的 PowerApp</span><span class="sxs-lookup"><span data-stu-id="f263f-156">Viewing an embedded PowerApp</span></span>

<span data-ttu-id="f263f-157">若要查看 Finance and Operations 中页面上的嵌入 PowerApp，只需转到包含嵌入的 PowerApp 的页面。</span><span class="sxs-lookup"><span data-stu-id="f263f-157">To view an embedded PowerApp on a page in Finance and Operations, simply go to a page with an embedded PowerApp.</span></span> <span data-ttu-id="f263f-158">回忆一下，PowerApps 可以通过标准操作窗格的 PowerApps 按钮访问，或可以在页面上直接显示为新的选项卡、快速选项卡，或在工作区显示为新部分。</span><span class="sxs-lookup"><span data-stu-id="f263f-158">Recall that PowerApps can be accessed through the PowerApps button in the standard Action Pane, or can appear directly on the page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span> <span data-ttu-id="f263f-159">当用户首次尝试在页面上加载 PowerApp 时，系统将提示他或她登录到 PowerApps 以确保用户有使用 PowerApp 的相应权限。</span><span class="sxs-lookup"><span data-stu-id="f263f-159">When a user first attempts to load a PowerApp on a page, he or she will be prompted to sign in to PowerApps to ensure the user has the approrpiate permissions to use the PowerApp.</span></span>

## <a name="editing-an-embedded-powerapp"></a><span data-ttu-id="f263f-160">编辑嵌入的 PowerApp</span><span class="sxs-lookup"><span data-stu-id="f263f-160">Editing an embedded PowerApp</span></span>

<span data-ttu-id="f263f-161">在 PowerApp 嵌入到页面后，可能需要对该 PowerApp 的配置作一些更改。</span><span class="sxs-lookup"><span data-stu-id="f263f-161">After a PowerApp has been embedded onto a page, you may need to make some changes to the configuration of that PowerApp.</span></span> <span data-ttu-id="f263f-162">例如，可能您要修改与嵌入的 PowerApp 或创建的新版本 PowerApp 关联的标签，并且您需要更新应用 ID 以指示最新的 PowerApp。</span><span class="sxs-lookup"><span data-stu-id="f263f-162">For example, perhaps you want to modify the label associated with the embedded PowerApp or a new version of a PowerApp has been created and you need to update the App ID to point at the latest PowerApp.</span></span>

<span data-ttu-id="f263f-163">执行以下步骤来编辑嵌入的 PowerApp 的配置：</span><span class="sxs-lookup"><span data-stu-id="f263f-163">Follow these steps to edit the configuration of an embedded PowerApp:</span></span>

1. <span data-ttu-id="f263f-164">转到**编辑 PowerApp** 窗格。</span><span class="sxs-lookup"><span data-stu-id="f263f-164">Go to the **Edit a PowerApp** pane.</span></span>

    - <span data-ttu-id="f263f-165">如果嵌入的 PowerApp 通过 PowerApps 菜单按钮访问，右键单击 PowerApps 菜单按钮并选择**个性化**。</span><span class="sxs-lookup"><span data-stu-id="f263f-165">If the embedded PowerApp is accessed through the PowerApps menu button, right-click on the PowerApps menu button and select **Personalize**.</span></span> <span data-ttu-id="f263f-166">选择您想要从**选择 PowerApp** 下拉菜单配置的 PowerApp。</span><span class="sxs-lookup"><span data-stu-id="f263f-166">Select the PowerApp that you want to configure from the **Select PowerApp** drop-down menu.</span></span>
    - <span data-ttu-id="f263f-167">如果嵌入的 PowerApp 直接出现在页面上，选择**选项**，然后选择**个性化设置此窗体**。</span><span class="sxs-lookup"><span data-stu-id="f263f-167">If the embedded PowerApp appears directly on the page, select **Options**, and then select **Personalize this form**.</span></span> <span data-ttu-id="f263f-168">使用**选择**工具，单击嵌入的 PowerApp。</span><span class="sxs-lookup"><span data-stu-id="f263f-168">Using the **Select** tool, click the embedded PowerApp.</span></span>

2. <span data-ttu-id="f263f-169">对 PowerApps 配置进行需要的修改，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="f263f-169">Make the needed modifications to the PowerApps configuration, and then click **Save**.</span></span>

## <a name="removing-an-embedded-powerapp"></a><span data-ttu-id="f263f-170">删除嵌入的 PowerApp</span><span class="sxs-lookup"><span data-stu-id="f263f-170">Removing an embedded PowerApp</span></span>

<span data-ttu-id="f263f-171">在 PowerApp 嵌入到页面上后，如果需要，有两种方法可以删除它：</span><span class="sxs-lookup"><span data-stu-id="f263f-171">After a PowerApp has been embedded onto a page, there are two ways to remove it if needed:</span></span>

- <span data-ttu-id="f263f-172">使用此主题前面[编辑嵌入的 PowerApp](#editing-an-embedded-powerapp) 部分的说明转到**编辑 PowerApp** 窗格。</span><span class="sxs-lookup"><span data-stu-id="f263f-172">Go to the **Edit a PowerApp** pane using the instructions from the [Editing an embedded PowerApp](#editing-an-embedded-powerapp) section earlier in this topic.</span></span> <span data-ttu-id="f263f-173">确认窗格显示您要删除的嵌入 PowerApp 的信息，然后单击**删除**按钮。</span><span class="sxs-lookup"><span data-stu-id="f263f-173">Confirm that the pane displays information for the embedded PowerApp that you would like to remove, and then click the **Delete** button.</span></span>
- <span data-ttu-id="f263f-174">由于嵌入的 PowerApp 保存为个性化数据，清除页面的个性化也将删除该页面上所有嵌入的 PowerApps。</span><span class="sxs-lookup"><span data-stu-id="f263f-174">Because an embedded PowerApp is saved as personalization data, clearing your page's personalization will also remove any embedded PowerApps on that page.</span></span> <span data-ttu-id="f263f-175">请注意，清除页面的个性化是永久的，并且无法撤消。</span><span class="sxs-lookup"><span data-stu-id="f263f-175">Note that clearing the page's personalization is permanent and cannot be undone.</span></span> <span data-ttu-id="f263f-176">若要删除您的页面上的个性化设置，选择**选项**，然后单击**个性化设置此窗体**。</span><span class="sxs-lookup"><span data-stu-id="f263f-176">To remove your personalizations on a page, select **Options** and then click **Personalize this form**.</span></span> <span data-ttu-id="f263f-177">在**管理**菜单下，选择**清除**按钮。</span><span class="sxs-lookup"><span data-stu-id="f263f-177">Under the **Manage** menu, select the **Clear** button.</span></span> <span data-ttu-id="f263f-178">刷新您的浏览器后，将删除此页之前的所有个性化设置。</span><span class="sxs-lookup"><span data-stu-id="f263f-178">After refreshing your browser, all the previous personalizations for this page will be removed.</span></span> <span data-ttu-id="f263f-179">请参阅[打造个性化的用户体验](personalize-user-experience.md)了解有关如何使用个性化设置优化页面的更多信息。</span><span class="sxs-lookup"><span data-stu-id="f263f-179">See [Personalization the user experience](personalize-user-experience.md) for more information about how to optimize pages using personalization.</span></span>

## <a name="appendix"></a><span data-ttu-id="f263f-180">附录</span><span class="sxs-lookup"><span data-stu-id="f263f-180">Appendix</span></span>

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a><span data-ttu-id="f263f-181">开发人员控制 PowerApp 可以嵌入的位置</span><span class="sxs-lookup"><span data-stu-id="f263f-181">Developer control over where a PowerApp can be embedded</span></span>

<span data-ttu-id="f263f-182">默认情况下，用户可以在任何页面嵌入 PowerApps，在 PowerApps 菜单按钮下，或直接在页面上作为选项卡、快速选项卡、边栏选项卡，或作为工作区的新部分。</span><span class="sxs-lookup"><span data-stu-id="f263f-182">By default, users can embed PowerApps on any page, either under the PowerApps menu button or directly on the page as a tab, FastTab, blade or as a new section in a workspace.</span></span> <span data-ttu-id="f263f-183">但是，如果需要，开发人员还可以将此功能配置为只允许在特定页面上嵌入 PowerApps，方法如下：</span><span class="sxs-lookup"><span data-stu-id="f263f-183">However, if required, developers can also configure this feature to only allow embedding of PowerApps on certain pages by implementing the following methods:</span></span>

- <span data-ttu-id="f263f-184">**isPowerAppPersonalizationEnabled** – 如果此方法为特定页面返回 false，那么 PowerApps 菜单按钮不显示，并且用户不能将 PowerApps 嵌入到此页的任何位置，包括作为选项卡。</span><span class="sxs-lookup"><span data-stu-id="f263f-184">**isPowerAppPersonalizationEnabled** – If this method returns false for a specific page, then the PowerApps menu button will not be shown, and users will not be able to embed PowerApps anywhere on this page, including as a tab.</span></span>
- <span data-ttu-id="f263f-185">**isPowerAppTabPersonalizationEnabled** – 如果此方法为特定页返回 false，那么用户不能直接在页面上作为选项卡、快速选项卡或全景部分嵌入 PowerApps。</span><span class="sxs-lookup"><span data-stu-id="f263f-185">**isPowerAppTabPersonalizationEnabled** – If this method returns false for a specific page, then users will not be able to embed PowerApps directly on the page as a tab, FastTab, or panorama section.</span></span> <span data-ttu-id="f263f-186">如果允许在页面上嵌入，用户仍可以通过 PowerApps 菜单按钮嵌入 PowerApps。</span><span class="sxs-lookup"><span data-stu-id="f263f-186">Users will still be able to embed PowerApps through the PowerApps menu button if embedding is allowed on the page.</span></span>

<span data-ttu-id="f263f-187">以下示例显示需要通过这两种方法来配置 PowerApps 可以嵌入的位置的新类。</span><span class="sxs-lookup"><span data-stu-id="f263f-187">The following example shows a new class with the two methods needed to configure where PowerApps can be embedded.</span></span>

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return true;
    }
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return true;
    }
}
```
