---
title: 设置资产管理移动工作区
description: 本主题介绍如何设置 Microsoft Dynamics 365 Supply Chain Management 和 Finance and Operations (Dynamics 365) 移动应用以运行资产管理移动工作区，工作人员可以使用该工作区来执行资产管理任务。
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9c2410c50b5d289792e2cc364674e1e093653590
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033195"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="d4764-103">设置资产管理移动工作区</span><span class="sxs-lookup"><span data-stu-id="d4764-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4764-104">本主题介绍如何设置 Microsoft Dynamics 365 Supply Chain Management 和 Finance and Operations (Dynamics 365) 移动应用以运行 **资产管理** 移动工作区，工作人员可以使用该工作区来执行资产管理任务。</span><span class="sxs-lookup"><span data-stu-id="d4764-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="d4764-105">在 Supply Chain Management 中设置维护工人用户</span><span class="sxs-lookup"><span data-stu-id="d4764-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="d4764-106">对于需要访问 **资产管理** 移动工作区的每个用户，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d4764-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="d4764-107">在 Supply Chain Management 中，转到 **人力资源 \> 工作人员**，确保要设置的用户存在工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="d4764-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="d4764-108">根据需要创建新的工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="d4764-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="d4764-109">转到 **资产管理 \> 设置 \> 工作人员 \> 工作人员**，确保您在上一步中确定（或创建）的工作人员记录已映射到维护工人记录。</span><span class="sxs-lookup"><span data-stu-id="d4764-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="d4764-110">根据需要创建新的维护工人记录，然后将 **工作人员** 字段设置为上一步中的工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="d4764-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="d4764-111">转到 **资产管理 \> 设置 \> 工作人员 \> 维护工人组**，确保您在上一步中确定（或创建）的维护工人记录属于该维护工人组。</span><span class="sxs-lookup"><span data-stu-id="d4764-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="d4764-112">转到 **系统管理 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="d4764-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="d4764-113">在网格中选择相关用户。</span><span class="sxs-lookup"><span data-stu-id="d4764-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="d4764-114">在 **用户详细信息** 快速选项卡上，将 **人员** 字段设置为您要与当前用户帐户关联的工作人员帐户。</span><span class="sxs-lookup"><span data-stu-id="d4764-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="d4764-115">此工作人员帐户应该是您在步骤 1 中确定（或创建）并在步骤 2 中映射到维护工人记录的工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="d4764-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="d4764-116">用户权限和安全角色应用于 **资产管理** 移动工作区的功能，就像它们会应用于 Supply Chain Management 用户界面的功能一样。</span><span class="sxs-lookup"><span data-stu-id="d4764-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="d4764-117">因此，您设置为访问 **资产管理** 移动工作区的每个用户必须具有直接在 Supply Chain Management 中直接执行类似操作所需的安全角色。</span><span class="sxs-lookup"><span data-stu-id="d4764-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="d4764-118">发布资产管理移动工作区</span><span class="sxs-lookup"><span data-stu-id="d4764-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="d4764-119">若要使资产管理功能在 Finance and Operations (Dynamics 365) 移动应用中可用，您必须发布 **资产管理** 移动工作区。</span><span class="sxs-lookup"><span data-stu-id="d4764-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="d4764-120">在 Supply Chain Management 中，选择 **设置** 按钮（右上角的齿轮符号），然后在菜单上选择 **移动应用**。</span><span class="sxs-lookup"><span data-stu-id="d4764-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="d4764-121">在 **管理移动应用** 对话框中，找到 **资产管理** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="d4764-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="d4764-122">如果它包含文本“在元数据中 - 未发布”，说明该工作区尚未发布。</span><span class="sxs-lookup"><span data-stu-id="d4764-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="d4764-123">如果它包含文本“在元数据中 - 已发布”，说明工作区已发布，您可以跳过此过程的其余部分。</span><span class="sxs-lookup"><span data-stu-id="d4764-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="d4764-124">![管理移动应用对话框](media/mobile-workspaces.png "管理移动应用对话框")</span><span class="sxs-lookup"><span data-stu-id="d4764-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="d4764-125">选择 **资产管理** 磁贴，然后在工具栏上选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="d4764-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="d4764-126">几秒钟后，您应该收到一条通知，说明工作区已成功发布。</span><span class="sxs-lookup"><span data-stu-id="d4764-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="d4764-127">此外，磁贴上的文本应会变为“在元数据中 - 已发布”。</span><span class="sxs-lookup"><span data-stu-id="d4764-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="d4764-128">安装和设置 Finance and Operations (Dynamics 365) 移动应用</span><span class="sxs-lookup"><span data-stu-id="d4764-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="d4764-129">转到以下应用商店之一，在移动设备上安装 **Microsoft Finance and Operations (Dynamics 365)** 应用：</span><span class="sxs-lookup"><span data-stu-id="d4764-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="d4764-130">对于 Google Android 设备</span><span class="sxs-lookup"><span data-stu-id="d4764-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="d4764-131">对于 Apple iOS 设备</span><span class="sxs-lookup"><span data-stu-id="d4764-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="d4764-132">打开 Finance and Operations (Dynamics 365) 应用。</span><span class="sxs-lookup"><span data-stu-id="d4764-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="d4764-133">登录页面应会出现。</span><span class="sxs-lookup"><span data-stu-id="d4764-133">The sign-in page should appear.</span></span> <span data-ttu-id="d4764-134">在 **登录** 字段中，输入您的 Supply Chain Management URL，或在 **最近环境** 列表中选择一个最近的 URL，然后点击 **连接**。</span><span class="sxs-lookup"><span data-stu-id="d4764-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="d4764-135">![登录页](media/mobile-app-sign-in.png "登录页")</span><span class="sxs-lookup"><span data-stu-id="d4764-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="d4764-136">如果系统提示您确认连接，请选中 **我知道** 复选框，然后点击 **连接**。</span><span class="sxs-lookup"><span data-stu-id="d4764-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="d4764-137">在 **选择帐户** 页上，使用您的 Microsoft 帐户登录到移动应用程序。</span><span class="sxs-lookup"><span data-stu-id="d4764-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="d4764-138">**工作区** 页将显示。</span><span class="sxs-lookup"><span data-stu-id="d4764-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="d4764-139">其中将列出您的 Supply Chain Management 实例已发布的每个移动工作区。</span><span class="sxs-lookup"><span data-stu-id="d4764-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="d4764-140">![工作区列表](media/mobile-app-workspaces.png "工作区列表")</span><span class="sxs-lookup"><span data-stu-id="d4764-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="d4764-141">如果必须更改法人（公司），请点击左上角的菜单按钮（有时称为汉堡包或汉堡包按钮），然后点击 **更改公司**。</span><span class="sxs-lookup"><span data-stu-id="d4764-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="d4764-142">![更改法人](media/mobile-app-change-comp.png "更改法人")</span><span class="sxs-lookup"><span data-stu-id="d4764-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="d4764-143">在 **工作区** 页上，选择要使用的工作区将其打开。</span><span class="sxs-lookup"><span data-stu-id="d4764-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="d4764-144">![资产管理移动工作区](media/mobile-app-asset-workspace.png "资产管理移动工作区")</span><span class="sxs-lookup"><span data-stu-id="d4764-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="d4764-145">使用资产管理移动工作区</span><span class="sxs-lookup"><span data-stu-id="d4764-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="d4764-146">有关如何使用 **资产管理** 移动工作区的详细信息，请参阅[使用资产管理移动工作区](asset-management-mobile-workspace.md)。</span><span class="sxs-lookup"><span data-stu-id="d4764-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="d4764-147">有关 Finance and Operations (Dynamics 365) 移动应用的详细信息，请参阅[移动应用主页](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md)。</span><span class="sxs-lookup"><span data-stu-id="d4764-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>
