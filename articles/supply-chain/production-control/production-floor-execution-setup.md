---
title: 设置设备以运行生产车间执行界面
description: 为生产车间中的每个设备设置生产车间执行界面。 公司通常以不同方式设置每个设备，具体取决于设备的用途。 例如，一家公司可能在接待区有一个设备，以供工作人员上班打卡和下班打卡，而在车间有另一个设备，以供工作人员管理作业。
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 57f09bf907407e19ae0e693de64510f7f4efbf0b
ms.sourcegitcommit: f27f5d07c040bdca1bcd616f5d3f2320d3b3337e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2020
ms.locfileid: "4423307"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a><span data-ttu-id="6cf24-105">设置设备以运行生产车间执行界面</span><span class="sxs-lookup"><span data-stu-id="6cf24-105">Set up a device to run the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6cf24-106">为生产车间中的每个设备设置生产车间执行界面。</span><span class="sxs-lookup"><span data-stu-id="6cf24-106">The production floor execution interface is set up for every device on the production floor.</span></span> <span data-ttu-id="6cf24-107">公司通常以不同方式设置每个设备，具体取决于设备的用途。</span><span class="sxs-lookup"><span data-stu-id="6cf24-107">Companies typically set up each device differently, depending on the purpose that the device serves.</span></span> <span data-ttu-id="6cf24-108">例如，一家公司可能在接待区有一个设备，以供工作人员上班打卡和下班打卡，而在车间有另一个设备，以供工作人员管理作业。</span><span class="sxs-lookup"><span data-stu-id="6cf24-108">For example, a company might have one device in the reception area, where workers clock in and clock out, and another on the shop floor, where workers manage their jobs.</span></span>

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a><span data-ttu-id="6cf24-109">为特定设备设置配置和筛选器</span><span class="sxs-lookup"><span data-stu-id="6cf24-109">Set the configuration and filters for a specific device</span></span>

<span data-ttu-id="6cf24-110">若要为设备设置配置和作业筛选器，请使用具有包括 *维护时间主管* 责任的安全角色的帐户登录到 **生产车间执行** 页面。</span><span class="sxs-lookup"><span data-stu-id="6cf24-110">To set the configuration and job filters for a device, sign in to the **Production floor execution** page by using an account that has a security role that includes the *Maintain time supervisor* duty.</span></span> <span data-ttu-id="6cf24-111">（在开箱即用的安全角色中，仅 *车间主管* 具有此责任。）然后，按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6cf24-111">(Among the out-of-box security roles, only *Shop floor supervisor* has this duty.) Then follow these steps.</span></span>

1. <span data-ttu-id="6cf24-112">转到要设置的设备，然后以车间主管的身份登录到 Microsoft Dynamics 365 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="6cf24-112">Go to the device that you want to set up, and sign in to Microsoft Dynamics 365 Supply Chain Management as a shop floor supervisor.</span></span> <span data-ttu-id="6cf24-113">（使用包括 *维护时间主管* 责任的帐户。）</span><span class="sxs-lookup"><span data-stu-id="6cf24-113">(Use an account that includes the *Maintain time supervisor* duty.)</span></span>
1. <span data-ttu-id="6cf24-114">确保为您要设置的设备提供配置。</span><span class="sxs-lookup"><span data-stu-id="6cf24-114">Make sure that a configuration is available for the device that you're setting up.</span></span> <span data-ttu-id="6cf24-115">如果尚无配置，则提供默认配置。</span><span class="sxs-lookup"><span data-stu-id="6cf24-115">If no configuration already exists, a default configuration is provided.</span></span> <span data-ttu-id="6cf24-116">有关如何设置配置的详细信息，请参阅[配置生产车间执行界面](production-floor-execution-configure.md)。</span><span class="sxs-lookup"><span data-stu-id="6cf24-116">For more information about how to set up a configuration, see [Configure the production floor execution interface](production-floor-execution-configure.md).</span></span>
1. <span data-ttu-id="6cf24-117">转到 **生产控制 \> 制造执行 \> 生产车间执行**。</span><span class="sxs-lookup"><span data-stu-id="6cf24-117">Go to **Production control \> Manufacturing execution \> Production floor execution**.</span></span>

    <span data-ttu-id="6cf24-118">如果已经在当前设备上配置了生产车间执行界面至少一次，将显示登录页面。</span><span class="sxs-lookup"><span data-stu-id="6cf24-118">If the production floor execution interface has already been configured at least one time on the current device, a sign-in page appears.</span></span> <span data-ttu-id="6cf24-119">否则，将显示欢迎页面。</span><span class="sxs-lookup"><span data-stu-id="6cf24-119">Otherwise, a welcome page appears.</span></span>

1. <span data-ttu-id="6cf24-120">在登录页面或欢迎页面上，选择 **配置**。</span><span class="sxs-lookup"><span data-stu-id="6cf24-120">On either the sign-in page or the welcome page, select **Configure**.</span></span>
1. <span data-ttu-id="6cf24-121">在列表中选择配置。</span><span class="sxs-lookup"><span data-stu-id="6cf24-121">Select a configuration in the list.</span></span>
1. <span data-ttu-id="6cf24-122">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="6cf24-122">Select **Next**.</span></span>
1. <span data-ttu-id="6cf24-123">选择一个或多个筛选器以应用于当前设备。</span><span class="sxs-lookup"><span data-stu-id="6cf24-123">Select one or more filters to apply to the current device.</span></span> <span data-ttu-id="6cf24-124">这些筛选器将有助于确保仅在设备上显示相关作业。</span><span class="sxs-lookup"><span data-stu-id="6cf24-124">These filters will help ensure that only relevant jobs are shown on the device.</span></span> <span data-ttu-id="6cf24-125">若要设置筛选器，请选择筛选器类型以打开值列表，然后选择要进行筛选的值。</span><span class="sxs-lookup"><span data-stu-id="6cf24-125">To set a filter, select the filter type to open a list of values, and then select the value to filter on.</span></span> <span data-ttu-id="6cf24-126">提供以下筛选器：</span><span class="sxs-lookup"><span data-stu-id="6cf24-126">The following filters are available:</span></span>

    - <span data-ttu-id="6cf24-127">**生产单位** – 此筛选器是最高级别的筛选器。</span><span class="sxs-lookup"><span data-stu-id="6cf24-127">**Production unit** – This filter is the highest-level filter.</span></span> <span data-ttu-id="6cf24-128">它通常是指具有多个资源组以及单独资源的大型工作区。</span><span class="sxs-lookup"><span data-stu-id="6cf24-128">It typically refers to a large work area that has several resource groups and individual resources in it.</span></span>
    - <span data-ttu-id="6cf24-129">**资源组** – 此筛选器是中等级别的筛选器。</span><span class="sxs-lookup"><span data-stu-id="6cf24-129">**Resource group** – This filter is a mid-level filter.</span></span> <span data-ttu-id="6cf24-130">它通常是指工作区的有限区域中相关资源的集合。</span><span class="sxs-lookup"><span data-stu-id="6cf24-130">It typically refers to a collection of related resources in a limited area of the workspace.</span></span> <span data-ttu-id="6cf24-131">如果首先选择 **生产单位** 筛选器，资源组列表将仅显示该单元中的组。</span><span class="sxs-lookup"><span data-stu-id="6cf24-131">If you select a **Production unit** filter first, the list of resource groups shows only groups from that unit.</span></span> <span data-ttu-id="6cf24-132">否则，它将显示所有可用的资源组。</span><span class="sxs-lookup"><span data-stu-id="6cf24-132">Otherwise, it shows all available resource groups.</span></span>
    - <span data-ttu-id="6cf24-133">**资源** – 此筛选器是最具体的筛选器。</span><span class="sxs-lookup"><span data-stu-id="6cf24-133">**Resource** – This filter is the most specific filter.</span></span> <span data-ttu-id="6cf24-134">它通常是指特定的机器或其他单个资源。</span><span class="sxs-lookup"><span data-stu-id="6cf24-134">It typically refers to a specific machine or other single resource.</span></span> <span data-ttu-id="6cf24-135">如果首先选择 **资源组** 和/或 **生产单位** 筛选器，资源列表将仅显示该组和/或该单元中的资源。</span><span class="sxs-lookup"><span data-stu-id="6cf24-135">If you select a **Resource group** and/or **Production unit** filter first, the list of resources shows only resources from that group and/or unit.</span></span> <span data-ttu-id="6cf24-136">否则，它将显示所有可用的资源。</span><span class="sxs-lookup"><span data-stu-id="6cf24-136">Otherwise, it shows all available resources.</span></span>

1. <span data-ttu-id="6cf24-137">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6cf24-137">Select **OK**.</span></span>
1. <span data-ttu-id="6cf24-138">显示登录页面，您的设备可供使用。</span><span class="sxs-lookup"><span data-stu-id="6cf24-138">The sign-in page appears, and your device is ready for use.</span></span>

## <a name="allow-a-worker-to-override-the-default-filters"></a><span data-ttu-id="6cf24-139">允许工作人员替代默认筛选器</span><span class="sxs-lookup"><span data-stu-id="6cf24-139">Allow a worker to override the default filters</span></span>

<span data-ttu-id="6cf24-140">您可以授予特定工作人员在使用的任何设备上更改筛选器设置的权限。</span><span class="sxs-lookup"><span data-stu-id="6cf24-140">You can give specific workers permission to change the filter settings on any device that they use.</span></span> <span data-ttu-id="6cf24-141">对于拥有此权限的工作人员，生产车间执行界面在 **所有作业** 和 **活动作业** 页面上提供了 **筛选器** 按钮。</span><span class="sxs-lookup"><span data-stu-id="6cf24-141">For workers who have this permission, the production floor execution interface provides a **Filter** button on the **All jobs** and **Active job** pages.</span></span>

> [!NOTE]
> <span data-ttu-id="6cf24-142">如果工作人员更改筛选器，之后将针对登录到该设备的所有用户应用新的筛选器。</span><span class="sxs-lookup"><span data-stu-id="6cf24-142">If a worker changes a filter, the new filter applies from that point forward, for all users who sign in to the device.</span></span>

<span data-ttu-id="6cf24-143">若要允许工作人员替代已为设备设置的默认作业筛选器，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="6cf24-143">To allow a worker to override the default job filters that have been set up for a device, follow these steps.</span></span>

1. <span data-ttu-id="6cf24-144">转到 **考勤管理 \> 设置 \> 时间登记工作人员**。</span><span class="sxs-lookup"><span data-stu-id="6cf24-144">Go to **Time and attendance \> Setup \> Time registration workers**.</span></span>
1. <span data-ttu-id="6cf24-145">在列表中选择一个工作人员以打开该工作人员的 **时间登记工作人员** 页面。</span><span class="sxs-lookup"><span data-stu-id="6cf24-145">Select a worker in the list to open that worker's **Time registration workers** page.</span></span>
1. <span data-ttu-id="6cf24-146">在 **时间登记** 选项卡上，将 **设置筛选器** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="6cf24-146">On the **Time registration** tab, set the **Set filters** option to *Yes*.</span></span>

## <a name="run-the-interface-in-full-screen-mode"></a><span data-ttu-id="6cf24-147">以全屏模式运行界面</span><span class="sxs-lookup"><span data-stu-id="6cf24-147">Run the interface in full-screen mode</span></span>

<span data-ttu-id="6cf24-148">通常，您将在专用于此目的的设备上运行生产车间执行界面。</span><span class="sxs-lookup"><span data-stu-id="6cf24-148">Often, you will run the production floor execution interface on a device that is used exclusively for that purpose.</span></span> <span data-ttu-id="6cf24-149">因此，在不显示任何导航和/或浏览器 Chrome 的情况下，以全屏模式运行界面可能很有意义。</span><span class="sxs-lookup"><span data-stu-id="6cf24-149">Therefore, it might make sense to run the interface in full-screen mode, without showing any navigation and/or browser chrome.</span></span>

- <span data-ttu-id="6cf24-150">若要隐藏 Supply Chain Management 中显示的导航窗格，请将以下文本添加到浏览器地址栏中的 URL 的末尾：`\&limitednav=true`。</span><span class="sxs-lookup"><span data-stu-id="6cf24-150">To hide the navigation pane that is shown in Supply Chain Management, add the following text to the end of the URL in the browser's address bar: `\&limitednav=true`.</span></span>
- <span data-ttu-id="6cf24-151">若要同时隐藏浏览器的地址栏，请使用浏览器的本机全屏模式。</span><span class="sxs-lookup"><span data-stu-id="6cf24-151">To also hide the browser's address bar, use the browser's native full-screen mode.</span></span> <span data-ttu-id="6cf24-152">（有关说明，请参阅您的浏览器的文档。）</span><span class="sxs-lookup"><span data-stu-id="6cf24-152">(For instructions, see your browser's documentation.)</span></span>

<span data-ttu-id="6cf24-153">下图的上部显示了默认情况下界面的外观。</span><span class="sxs-lookup"><span data-stu-id="6cf24-153">The upper part of the following illustration shows how the interface looks by default.</span></span> <span data-ttu-id="6cf24-154">下部显示了隐藏导航窗格时全屏模式下界面的外观。</span><span class="sxs-lookup"><span data-stu-id="6cf24-154">The lower part shows how it looks in full-screen mode when the navigation pane is hidden.</span></span>

<span data-ttu-id="6cf24-155">![标准与全屏界面](media/pfei-full-screen.png "标准与全屏界面")</span><span class="sxs-lookup"><span data-stu-id="6cf24-155">![Standard vs. full-screen interface](media/pfei-full-screen.png "Standard vs. full-screen interface")</span></span>

## <a name="extend-the-session-past-12-hours"></a><span data-ttu-id="6cf24-156">将会话延长超过 12 小时</span><span class="sxs-lookup"><span data-stu-id="6cf24-156">Extend the session past 12 hours</span></span>

<span data-ttu-id="6cf24-157">默认情况下，如果 12 个小时内没有人使用，生产车间执行界面会自动注销。</span><span class="sxs-lookup"><span data-stu-id="6cf24-157">By default, the production floor execution interface automatically signs out if nobody uses it for 12 hours.</span></span> <span data-ttu-id="6cf24-158">然后，Supply Chain Management 用户必须再次登录。</span><span class="sxs-lookup"><span data-stu-id="6cf24-158">A Supply Chain Management user must then sign in again.</span></span> <span data-ttu-id="6cf24-159">但是，您可以将超时限制最多延长 90 天。</span><span class="sxs-lookup"><span data-stu-id="6cf24-159">However, you can extend the time-out limit to up to 90 days.</span></span>

<span data-ttu-id="6cf24-160">若要延长超时限制，请登录 Supply Chain Management，然后转到 **系统管理 \> 用户 \> 会话扩展**。</span><span class="sxs-lookup"><span data-stu-id="6cf24-160">To extend the time-out limit, sign in to Supply Chain Management, and go to **System administration \> Users \> Session extensions**.</span></span> <span data-ttu-id="6cf24-161">指定用于登录设备的 Supply Chain Management 用户帐户，以及会话应保持活动状态的小时数。</span><span class="sxs-lookup"><span data-stu-id="6cf24-161">Specify the Supply Chain Management user account that is used to sign in to the device, and the number of hours that the session should stay active for.</span></span>
