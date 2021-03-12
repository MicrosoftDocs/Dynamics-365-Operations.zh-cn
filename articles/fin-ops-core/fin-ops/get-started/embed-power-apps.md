---
title: 从 Power Apps 嵌入画布应用
description: 此主题说明如何将 Microsoft Power Apps 中的画布应用嵌入到客户端以细分该产品的功能。
author: jasongre
manager: AnnBe
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: fbdd4dd1bb0b850319b12e55b0e68d6fdc516ad6
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798369"
---
# <a name="embed-canvas-apps-from-power-apps"></a><span data-ttu-id="93c49-103">从 Power Apps 嵌入画布应用</span><span class="sxs-lookup"><span data-stu-id="93c49-103">Embed canvas apps from Power Apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93c49-104">Microsoft Power Apps 是一项服务，让开发人员和非技术用户无需编写代码即可为移动设备、平板电脑和 Web 构建自定义业务应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-104">Microsoft Power Apps is a service that lets developers and non-technical users build custom business apps for mobile devices, tablets, and the web without writing code.</span></span> <span data-ttu-id="93c49-105">Finance and Operations 应用支持与 Power Apps 集成。</span><span class="sxs-lookup"><span data-stu-id="93c49-105">Finance and Operations apps support integration with Power Apps.</span></span> <span data-ttu-id="93c49-106">您、您的组织或更广泛的生态系统开发的画布应用可以嵌入到 Finance and Operations 应用中来细分产品的功能。</span><span class="sxs-lookup"><span data-stu-id="93c49-106">Canvas apps that you, your organization, or the broader ecosystem develop can be embedded into Finance and Operations apps to augment the product's functionality.</span></span> <span data-ttu-id="93c49-107">例如，您可以利用 Power Apps 构建画布应用以使用从其他系统检索的信息补充 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-107">For example, you might build a canvas app from Power Apps to supplement a Finance and Operations app with information that is retrieved from another system.</span></span>

<span data-ttu-id="93c49-108">若要了解有关嵌入 Power Apps 的详细信息，请观看视频短片[如何嵌入 Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY)。</span><span class="sxs-lookup"><span data-stu-id="93c49-108">To learn more about embedding Power Apps, watch the short [How to embed Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) video.</span></span>

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a><span data-ttu-id="93c49-109">将 Power Apps 中的嵌入画布应用添加到页面中</span><span class="sxs-lookup"><span data-stu-id="93c49-109">Adding an embedded canvas app from Power Apps to a page</span></span>

### <a name="overview"></a><span data-ttu-id="93c49-110">概览</span><span class="sxs-lookup"><span data-stu-id="93c49-110">Overview</span></span>

<span data-ttu-id="93c49-111">将画布应用从 Power Apps 嵌入到客户端之前，必须找到或构建具有所需视觉效果或功能的应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-111">Before you embed a canvas app from Power Apps into the client, you must find or build an app that has the desired visuals or functionality.</span></span> <span data-ttu-id="93c49-112">本主题不包括对构建应用的流程的详细描述。</span><span class="sxs-lookup"><span data-stu-id="93c49-112">This topic doesn't include a detailed description of the process for building apps.</span></span> <span data-ttu-id="93c49-113">如果您不熟悉 Power Apps，请参阅 [Power Apps 文档](https://docs.microsoft.com/powerapps/)。</span><span class="sxs-lookup"><span data-stu-id="93c49-113">If you're new to Power Apps, see the [Power Apps documentation](https://docs.microsoft.com/powerapps/).</span></span>

<span data-ttu-id="93c49-114">准备嵌入应用时，有两种方法可以访问页面上的特定画布应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-114">There are two ways to access a specific canvas app on a page when you're ready to embed the app.</span></span> <span data-ttu-id="93c49-115">您可以选择更适合您的情况的方法。</span><span class="sxs-lookup"><span data-stu-id="93c49-115">You can choose whichever approach fits your scenario better.</span></span> <span data-ttu-id="93c49-116">第一种方法使用已添加到标准操作窗格的 **Power Apps** 按钮。</span><span class="sxs-lookup"><span data-stu-id="93c49-116">The first approach uses the **Power Apps** button that has been added to the standard Action Pane.</span></span> <span data-ttu-id="93c49-117">通过此方法添加的应用显示为 **Power Apps** 菜单按钮上的项目。</span><span class="sxs-lookup"><span data-stu-id="93c49-117">Apps that you add by using this approach appear as items on the **Power Apps** menu button.</span></span> <span data-ttu-id="93c49-118">选择其中一项时，将出现一个包含嵌入的应用的侧窗格。</span><span class="sxs-lookup"><span data-stu-id="93c49-118">When you select one of these items, a side pane that contains the embedded app appears.</span></span> <span data-ttu-id="93c49-119">或者，您可以直接在页面上将应用嵌入为新选项卡、快速选项卡或边栏选项卡，或者显示为工作区的新部分。</span><span class="sxs-lookup"><span data-stu-id="93c49-119">Alternatively, you can embed an app directly on a page as a new tab, FastTab, or blade, or as a new section in a workspace.</span></span>

<span data-ttu-id="93c49-120">配置嵌入的画布应用时，您可以选择您希望将其作为上下文发送到应用的单个字段。</span><span class="sxs-lookup"><span data-stu-id="93c49-120">When you configure your embedded canvas app, you can select a single field that you want to send as context to the app.</span></span> <span data-ttu-id="93c49-121">此步骤使应用可以根据您当前正在查看的数据作出响应。</span><span class="sxs-lookup"><span data-stu-id="93c49-121">This step enables the app to be responsive, based on the data that you're currently viewing.</span></span>

> [!NOTE]
> <span data-ttu-id="93c49-122">您目前无法使用此机制来嵌入建模的应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-122">You can't currently use this mechanism to embed modeled apps.</span></span>  

### <a name="details"></a><span data-ttu-id="93c49-123">明细</span><span class="sxs-lookup"><span data-stu-id="93c49-123">Details</span></span>

<span data-ttu-id="93c49-124">以下过程显示了如何将 Power Apps 中的画布应用嵌入到 Web 客户端。</span><span class="sxs-lookup"><span data-stu-id="93c49-124">The following procedure shows how to embed a canvas app from Power Apps into the web client.</span></span>

1. <span data-ttu-id="93c49-125">转到您要嵌入画布应用的页面。</span><span class="sxs-lookup"><span data-stu-id="93c49-125">Go to the page where you want to embed the canvas app.</span></span> <span data-ttu-id="93c49-126">此页面将是包含必须作为输入传递到应用的数据的页面。</span><span class="sxs-lookup"><span data-stu-id="93c49-126">This page will be the page that contains data that must be passed to the app as input.</span></span>
2. <span data-ttu-id="93c49-127">打开 **从 Power Apps 中添加应用** 窗格：</span><span class="sxs-lookup"><span data-stu-id="93c49-127">Open the **Add an app from Power Apps** pane:</span></span>

    - <span data-ttu-id="93c49-128">单击 **选项**，然后选择 **个性化设置此页面**。</span><span class="sxs-lookup"><span data-stu-id="93c49-128">Click **Options**, and then select **Personalize this page**.</span></span> <span data-ttu-id="93c49-129">在 **插入** 菜单下，选择 **Power Apps**。</span><span class="sxs-lookup"><span data-stu-id="93c49-129">Under the **Insert** menu, choose **Power Apps**.</span></span> <span data-ttu-id="93c49-130">最后，选择要添加应用的区域。</span><span class="sxs-lookup"><span data-stu-id="93c49-130">Finally, select the region where you would like to add the app.</span></span> <span data-ttu-id="93c49-131">如果要在 Power Apps 菜单按钮下嵌入应用，选择操作窗格。</span><span class="sxs-lookup"><span data-stu-id="93c49-131">If you want to embed the app under the Power Apps menu button, choose the Action Pane.</span></span> <span data-ttu-id="93c49-132">如果要将应用直接嵌入到页面上，选择相应的选项卡、快速选项卡、边栏选项卡或部分（如果您处于工作区）。</span><span class="sxs-lookup"><span data-stu-id="93c49-132">If you want to embed the app directly onto the page, choose the appropriate tab, FastTab, blade, or section (if you're on a workspace).</span></span>
    - <span data-ttu-id="93c49-133">如果将使用 Power Apps 菜单按钮访问应用，您可以单击标准操作窗格中的 **Power Apps** 菜单按钮，然后选择 **添加应用**。</span><span class="sxs-lookup"><span data-stu-id="93c49-133">If the app will be accessed using the Power Apps menu button, you can alternatively click the **Power Apps** menu button in the standard Action Pane, and then select **Add an app**.</span></span>

3. <span data-ttu-id="93c49-134">配置嵌入的应用：</span><span class="sxs-lookup"><span data-stu-id="93c49-134">Configure the embedded app:</span></span>

    - <span data-ttu-id="93c49-135">**名称** 字段指示为将包含嵌入的应用的按钮或选项卡显示的文本。</span><span class="sxs-lookup"><span data-stu-id="93c49-135">The **Name** field indicates the text shown for the button or tab that will contain the embedded app.</span></span> <span data-ttu-id="93c49-136">通常，您可能要在此字段中重复应用的名称。</span><span class="sxs-lookup"><span data-stu-id="93c49-136">Oftentimes, you may want to repeat the name of the app in this field.</span></span>
    - <span data-ttu-id="93c49-137">**应用 ID** 字段表示要嵌入的画布应用的全局唯一标识符 (GUID)。</span><span class="sxs-lookup"><span data-stu-id="93c49-137">The **App ID** field indicates the globally unique identifier (GUID) for the canvas app that you want to embed.</span></span> <span data-ttu-id="93c49-138">若要检索此值，在 [make.powerapps.com](https://make.powerapps.com) 上找到应用，然后在 **详细信息** 下查找 **应用 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="93c49-138">To retrieve this value, find the app on [make.powerapps.com](https://make.powerapps.com), and then look in the **App ID** field under **Details**.</span></span>
    - <span data-ttu-id="93c49-139">对于 **应用的输入上下文**，您可以有选择性地选择包含您要作为输入传送到应用的数据的字段。</span><span class="sxs-lookup"><span data-stu-id="93c49-139">For **Input context for the app**, you can optionally select the field that contains the data that you want to pass to the app as input.</span></span> <span data-ttu-id="93c49-140">请参阅本主题后面名为[构建利用从 Finance and Operations 应用发送的数据的应用](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps)部分，了解有关应用如何访问发送自 Finance and Operations 应用的数据的详细信息。</span><span class="sxs-lookup"><span data-stu-id="93c49-140">See the section later in this topic titled [Building an app that leverages data sent from Finance and Operations apps](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) for details on how the app can access the data sent from Finance and Operations apps.</span></span>
    - <span data-ttu-id="93c49-141">选择与您嵌入的应用类型匹配的 **应用程序大小**。</span><span class="sxs-lookup"><span data-stu-id="93c49-141">Choose the **Application size** that matches the type of app that you're embedding.</span></span> <span data-ttu-id="93c49-142">为针对移动设备构建的应用选择 **窄**，为平板电脑构建的应用选择 **宽**。</span><span class="sxs-lookup"><span data-stu-id="93c49-142">Select **Thin** for apps built for mobile devices, and **Wide** for apps built for tablets.</span></span> <span data-ttu-id="93c49-143">这将确保为嵌入的应用分配足够的空间量。</span><span class="sxs-lookup"><span data-stu-id="93c49-143">This ensures a sufficient amount of space is allotted for the embedded app.</span></span>
    - <span data-ttu-id="93c49-144">**法人** 快速选项卡提供选择应用可用于哪些法人的功能。</span><span class="sxs-lookup"><span data-stu-id="93c49-144">The **Legal entities** FastTab provides the ability to choose which legal entities the app is available for.</span></span> <span data-ttu-id="93c49-145">默认让所有法人都能访问应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-145">The default is to make the app accessible to all legal entities.</span></span> <span data-ttu-id="93c49-146">此选项仅在[保存的视图](saved-views.md)功能已禁用时才可用。</span><span class="sxs-lookup"><span data-stu-id="93c49-146">This option is only available when the [Saved views](saved-views.md) feature is disabled.</span></span> 

4. <span data-ttu-id="93c49-147">在确认配置正确后，请单击 **插入** 在页面上嵌入 Power App。</span><span class="sxs-lookup"><span data-stu-id="93c49-147">After confirming that the configuration is correct, click **Insert** to embed the Power App on the page.</span></span> <span data-ttu-id="93c49-148">系统将提示您刷新浏览器以查看嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-148">You will be prompted to refresh the browser in order to see the embedded app.</span></span>

## <a name="sharing-an-embedded-app"></a><span data-ttu-id="93c49-149">共享嵌入的应用</span><span class="sxs-lookup"><span data-stu-id="93c49-149">Sharing an embedded app</span></span>

<span data-ttu-id="93c49-150">在将画布应用嵌入页面并确认此应用能够正确处理从该页面传递的任何数据上下文后，您可能希望与系统中的其他用户共享此应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-150">After you've embedded a canvas app on a page and confirmed that it's working correctly with any data context that is passed from that page, you might want to share the app with other users in the system.</span></span> <span data-ttu-id="93c49-151">要共享嵌入的画布应用，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="93c49-151">To share an embedded canvas app, follow these steps.</span></span>

1. <span data-ttu-id="93c49-152">与适当的用户[共享画布应用](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app)，以便他们可以在 Power Apps 中访问此应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-152">[Share the canvas app](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) with the appropriate users, so that they can access the app in Power Apps.</span></span> 

2. <span data-ttu-id="93c49-153">确保目标用户具有适当的个性化设置，以便在这些用户查看页面时显示嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-153">Make sure that the targeted users have the appropriate personalizations, so that the embedded app appears when those users view the page.</span></span> <span data-ttu-id="93c49-154">您可以使用以下两种方法之一：</span><span class="sxs-lookup"><span data-stu-id="93c49-154">You can use either of the following approaches:</span></span>

    - <span data-ttu-id="93c49-155">推荐：使用[已保存视图](saved-views.md)功能创建和发布包含嵌入应用的视图。</span><span class="sxs-lookup"><span data-stu-id="93c49-155">Recommended: Use the [Saved views](saved-views.md) feature to create and publish a view that includes the embedded app.</span></span> <span data-ttu-id="93c49-156">此方法可以确保具有发布视图所针对的安全角色的所有用户都会在 Finance and Operations 应用中看到该应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-156">This approach ensures that all users who have the security roles that are targeted by the published view will see the app in Finance and Operations apps.</span></span> 
    - <span data-ttu-id="93c49-157">如果未启用“已保存视图”功能，您可以让系统管理员将包括嵌入应用的个性化设置推送给所有用户或部分用户。</span><span class="sxs-lookup"><span data-stu-id="93c49-157">If you don't have the Saved views feature turned on, you can have the system admin push a personalization that includes the embedded app to all users or a subset of users.</span></span> <span data-ttu-id="93c49-158">或者，您可以导出页面的个性化设置，然后将其发送给一个或多个用户。</span><span class="sxs-lookup"><span data-stu-id="93c49-158">Alternatively, you can export your page's personalizations, and send them to one or more users.</span></span> <span data-ttu-id="93c49-159">这些用户中的每一个都可以导入个性化设置。</span><span class="sxs-lookup"><span data-stu-id="93c49-159">Each of those users can then import the personalizations.</span></span> <span data-ttu-id="93c49-160">个性化工具栏具有让您可以导出和导入个性化设置的操作。</span><span class="sxs-lookup"><span data-stu-id="93c49-160">The personalization toolbar has actions that let you export and import personalizations.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="93c49-161">如果画布应用已与外部用户共享，这些用户将不能在 Finance and Operations 应用内使用嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-161">If the canvas app has been shared with external users, those users can't use the embedded app inside Finance and Operations apps.</span></span> <span data-ttu-id="93c49-162">不过，他们可以直接在 Power Apps 内访问该应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-162">However, they can access the app directly inside Power Apps.</span></span> <span data-ttu-id="93c49-163">外部用户包括来宾和不属于在其中部署了 Finance and Operations 应用的 Microsoft 365 Azure Directory 目录的用户。</span><span class="sxs-lookup"><span data-stu-id="93c49-163">External users include guests and users who don't belong to the Microsoft 365 Azure Directory where the Finance and Operations app is deployed.</span></span>

<span data-ttu-id="93c49-164">有关产品中的个性化功能以及如何使用的更多详细信息，请参阅[打造个性化的用户体验](personalize-user-experience.md)。</span><span class="sxs-lookup"><span data-stu-id="93c49-164">See [Personalize the user experience](personalize-user-experience.md) for more details about the personalization capabilities in the product and how to use them.</span></span>

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a><span data-ttu-id="93c49-165">构建使用从 Finance and Operations 应用发送的数据的画布应用</span><span class="sxs-lookup"><span data-stu-id="93c49-165">Building a canvas app that uses data that is sent from Finance and Operations apps</span></span>

<span data-ttu-id="93c49-166">当您构建将嵌入到 Finance and Operations 应用中的画布应用时，此流程的一个重要部分是使用来自该 Finance and Operations 应用的输入数据。</span><span class="sxs-lookup"><span data-stu-id="93c49-166">When you build a canvas app that will be embedded in a Finance and Operations app, one important part of the process is to use the input data from that Finance and Operations app.</span></span> <span data-ttu-id="93c49-167">根据 Power Apps 开发经验，可以使用 **Param("EntityId")** 变量访问从 Finance and Operations 应用传递的输入数据。</span><span class="sxs-lookup"><span data-stu-id="93c49-167">From the Power Apps development experience, the input data that is passed from a Finance and Operations app can be accessed by using the **Param("EntityId")** variable.</span></span>

<span data-ttu-id="93c49-168">例如，在应用的 OnStart 功能中，可以将 Finance and Operations 应用的输入数据设置为类似这样的一个变量：</span><span class="sxs-lookup"><span data-stu-id="93c49-168">For example, in the OnStart function of the app, you could set the input data from Finance and Operations apps to a variable like this:</span></span>

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a><span data-ttu-id="93c49-169">查看画布应用</span><span class="sxs-lookup"><span data-stu-id="93c49-169">Viewing a canvas app</span></span>

<span data-ttu-id="93c49-170">若要查看 Finance and Operations 应用中页面上的嵌入画布应用，只需转到包含嵌入的应用的页面。</span><span class="sxs-lookup"><span data-stu-id="93c49-170">To view an embedded canvas app on a page in Finance and Operations apps, just go to a page that has an embedded app.</span></span> <span data-ttu-id="93c49-171">请记住，可以使用标准操作窗格上的 **Power Apps** 按钮来访问应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-171">Remember that apps can be accessed by using the **Power Apps** button on the standard Action Pane.</span></span> <span data-ttu-id="93c49-172">或者，它们可以作为新选项卡、快速选项卡或边栏选项卡或作为工作区中的新部分直接显示在页面上。</span><span class="sxs-lookup"><span data-stu-id="93c49-172">Alternatively, they can appear directly on the page as a new tab, or FastTab, or blade, or as a new section in a workspace.</span></span> <span data-ttu-id="93c49-173">当用户首次尝试在页面上加载应用时，将提示他们登录。</span><span class="sxs-lookup"><span data-stu-id="93c49-173">When users first try to load an app on a page, they will be prompted to sign in.</span></span> <span data-ttu-id="93c49-174">此步骤可确保用户具有使用该应用的适当权限。</span><span class="sxs-lookup"><span data-stu-id="93c49-174">This step ensures that the users have the appropriate permissions to use the app.</span></span>

## <a name="editing-an-embedded-app"></a><span data-ttu-id="93c49-175">编辑嵌入的应用</span><span class="sxs-lookup"><span data-stu-id="93c49-175">Editing an embedded app</span></span>

<span data-ttu-id="93c49-176">在应用嵌入到页面后，可能需要对该应用的配置作一些更改。</span><span class="sxs-lookup"><span data-stu-id="93c49-176">After an app has been embedded onto a page, you may need to make some changes to the configuration of the app.</span></span> <span data-ttu-id="93c49-177">例如，可能您要修改与嵌入的应用关联的标签，或者已创建新版本应用并且您需要更新应用 ID 以指向最新应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-177">For example, perhaps you want to modify the label associated with the embedded app or a new version of the app has been created and you need to update the App ID to point at the latest.</span></span>

<span data-ttu-id="93c49-178">执行以下步骤来编辑嵌入的应用的配置：</span><span class="sxs-lookup"><span data-stu-id="93c49-178">Follow these steps to edit the configuration of an embedded app:</span></span>

1. <span data-ttu-id="93c49-179">转到 **编辑应用** 窗格。</span><span class="sxs-lookup"><span data-stu-id="93c49-179">Go to the **Edit the app** pane.</span></span>

    - <span data-ttu-id="93c49-180">如果嵌入的应用通过 Power Apps 菜单按钮访问，右键单击 Power Apps 菜单按钮并选择 **个性化**。</span><span class="sxs-lookup"><span data-stu-id="93c49-180">If the embedded app is accessed through the Power Apps menu button, right-click on the Power Apps menu button and select **Personalize**.</span></span> <span data-ttu-id="93c49-181">选择您想要从 **选择应用** 下拉菜单配置的应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-181">Select the app that you want to configure from the **Select an app** drop-down menu.</span></span>
    - <span data-ttu-id="93c49-182">如果嵌入的应用直接出现在页面上，选择 **选项**，然后选择 **个性化设置此页面**。</span><span class="sxs-lookup"><span data-stu-id="93c49-182">If the embedded app appears directly on the page, select **Options**, and then select **Personalize this page**.</span></span> <span data-ttu-id="93c49-183">使用 **选择** 工具，单击嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-183">Using the **Select** tool, click the embedded app.</span></span>

2. <span data-ttu-id="93c49-184">对应用配置进行需要的修改，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="93c49-184">Make the needed modifications to the app configuration, and then click **Save**.</span></span>

## <a name="removing-an-app"></a><span data-ttu-id="93c49-185">移除应用</span><span class="sxs-lookup"><span data-stu-id="93c49-185">Removing an app</span></span>

<span data-ttu-id="93c49-186">在应用嵌入到页面上后，如果需要，有两种方法可以删除它：</span><span class="sxs-lookup"><span data-stu-id="93c49-186">After an app has been embedded onto a page, there are two ways to remove it if needed:</span></span>

- <span data-ttu-id="93c49-187">使用此主题前面 [编辑嵌入的应用](#editing-an-embedded-app)部分中的说明转到 **编辑应用** 窗格。</span><span class="sxs-lookup"><span data-stu-id="93c49-187">Go to the **Edit an app** pane using the instructions from the [Editing an embedded app](#editing-an-embedded-app) section earlier in this topic.</span></span> <span data-ttu-id="93c49-188">确认窗格显示您要删除的嵌入应用的信息，然后单击 **删除** 按钮。</span><span class="sxs-lookup"><span data-stu-id="93c49-188">Confirm that the pane displays information for the embedded app that you would like to remove, and then click the **Delete** button.</span></span>
- <span data-ttu-id="93c49-189">由于嵌入的应用保存为个性化数据，清除页面的个性化也将删除该页面上所有嵌入的应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-189">Because the embedded app is saved as personalization data, clearing your page's personalization will also remove any embedded apps on that page.</span></span> <span data-ttu-id="93c49-190">请注意，清除页面的个性化是永久的，并且无法撤消。</span><span class="sxs-lookup"><span data-stu-id="93c49-190">Note that clearing the page's personalization is permanent and cannot be undone.</span></span> <span data-ttu-id="93c49-191">若要删除您的页面上的个性化设置，依次选择 **选项**、**个性化设置此页面** 和 **清除**。</span><span class="sxs-lookup"><span data-stu-id="93c49-191">To remove your personalizations on a page, select **Options**, and then **Personalize this page**, and finally the **Clear** button.</span></span> <span data-ttu-id="93c49-192">刷新您的浏览器后，将删除此页之前的所有个性化设置。</span><span class="sxs-lookup"><span data-stu-id="93c49-192">After refreshing your browser, all the previous personalizations for this page will be removed.</span></span> <span data-ttu-id="93c49-193">请参阅[打造个性化的用户体验](personalize-user-experience.md)了解有关如何使用个性化设置优化页面的更多信息。</span><span class="sxs-lookup"><span data-stu-id="93c49-193">See [Personalize the user experience](personalize-user-experience.md) for more information about how to optimize pages using personalization.</span></span>

## <a name="appendix"></a><span data-ttu-id="93c49-194">附录</span><span class="sxs-lookup"><span data-stu-id="93c49-194">Appendix</span></span>

### <a name="developer-specifying-where-an-app-can-be-embedded"></a><span data-ttu-id="93c49-195">[开发人员]指定应用可以嵌入的位置</span><span class="sxs-lookup"><span data-stu-id="93c49-195">[Developer] Specifying where an app can be embedded</span></span>

<span data-ttu-id="93c49-196">默认情况下，用户可以在任何页面嵌入应用，要么嵌入在 Power Apps 菜单按钮下，要么作为选项卡、快速选项卡、边栏选项卡或工作区新部分直接嵌入在页面上。</span><span class="sxs-lookup"><span data-stu-id="93c49-196">By default, users can embed apps on any page, either under the Power Apps menu button or directly on the page as a tab, FastTab, blade or as a new section in a workspace.</span></span> <span data-ttu-id="93c49-197">但是，如果需要，开发人员还可以将此功能配置为只允许在特定页面上嵌入应用，方法如下：</span><span class="sxs-lookup"><span data-stu-id="93c49-197">However, if required, developers can also configure this feature to only allow embedding of apps on certain pages by implementing the following methods:</span></span>

- <span data-ttu-id="93c49-198">**isPowerAppPersonalizationEnabled** – 如果此方法为特定页面返回 false，那么 Power Apps 菜单按钮不显示，并且用户不能将应用嵌入到此页的任何位置，包括作为选项卡。</span><span class="sxs-lookup"><span data-stu-id="93c49-198">**isPowerAppPersonalizationEnabled** – If this method returns false for a specific page, then the Power Apps menu button will not be shown, and users will not be able to embed apps anywhere on this page, including as a tab.</span></span>
- <span data-ttu-id="93c49-199">**isPowerAppTabPersonalizationEnabled** – 如果此方法为特定页返回 false，那么用户不能直接在页面上作为选项卡、快速选项卡或全景部分嵌入应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-199">**isPowerAppTabPersonalizationEnabled** – If this method returns false for a specific page, then users will not be able to embed apps directly on the page as a tab, FastTab, or panorama section.</span></span> <span data-ttu-id="93c49-200">如果允许在页面上嵌入，用户仍可以通过 Power Apps 菜单按钮嵌入应用。</span><span class="sxs-lookup"><span data-stu-id="93c49-200">Users will still be able to embed apps through the Power Apps menu button if embedding is allowed on the page.</span></span>

<span data-ttu-id="93c49-201">以下示例显示需要通过这两种方法来配置应用可以嵌入的位置的新类。</span><span class="sxs-lookup"><span data-stu-id="93c49-201">The following example shows a new class with the two methods needed to configure where apps can be embedded.</span></span>

```powerapps
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
