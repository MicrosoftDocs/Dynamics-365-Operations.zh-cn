---
title: 如果 Microsoft Teams 中有预先存在的团队，映射商店和团队
description: 本主题介绍如果您的组织在 Commerce 集成之前已在 Microsoft Teams 中创建了团队，如何在 Dynamics 365 Commerce Headquarters 中映射商店和相应的团队。
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3edd176788b24a5f5246e9b7bcb3c6fbcdca2254
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842620"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="f5811-103">如果 Microsoft Teams 中有预先存在的团队，映射商店和团队</span><span class="sxs-lookup"><span data-stu-id="f5811-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f5811-104">本主题介绍如果您的组织在 Commerce 集成之前已在 Microsoft Teams 中创建了团队，如何在 Dynamics 365 Commerce Headquarters 中映射商店和相应的团队。</span><span class="sxs-lookup"><span data-stu-id="f5811-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="f5811-105">在集成 Dynamics 365 Commerce 和 Microsoft Teams 之前，您的组织可能已为部分或全部商店创建了团队。</span><span class="sxs-lookup"><span data-stu-id="f5811-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="f5811-106">如果是这种情况，若要在 Commerce POS 和 Microsoft Teams 之间建立任务同步，您必须提供 Commerce Headquarters 中商店和相应团队的映射。</span><span class="sxs-lookup"><span data-stu-id="f5811-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="f5811-107">在 Commerce Headquarters 中映射商店和相应的团队</span><span class="sxs-lookup"><span data-stu-id="f5811-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="f5811-108">若要在 Commerce Headquarters 中映射商店和相应的团队，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f5811-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f5811-109">转到 **系统管理 \> 工作区 \> 数据管理**。</span><span class="sxs-lookup"><span data-stu-id="f5811-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="f5811-110">选择 **导出**。</span><span class="sxs-lookup"><span data-stu-id="f5811-110">Select **Export**.</span></span> 
1. <span data-ttu-id="f5811-111">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f5811-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f5811-112">在 **组名称** 下，输入“导出 Teams 映射”。</span><span class="sxs-lookup"><span data-stu-id="f5811-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="f5811-113">在 **选定实体** 快速选项卡上，选择 **添加实体**。</span><span class="sxs-lookup"><span data-stu-id="f5811-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="f5811-114">将显示 **添加实体** 对话框。</span><span class="sxs-lookup"><span data-stu-id="f5811-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="f5811-115">在 **实体名称** 下拉列表中，选择 **源与团队之间的 Teams 映射**。</span><span class="sxs-lookup"><span data-stu-id="f5811-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="f5811-116">在 **目标数据格式** 下拉列表中，选择 **CSV**。</span><span class="sxs-lookup"><span data-stu-id="f5811-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="f5811-117">选择 **添加**，然后选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="f5811-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="f5811-118">在操作窗格下的左上角，选择 **立即导出**。</span><span class="sxs-lookup"><span data-stu-id="f5811-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="f5811-119">在 **实体处理状态** 下，选择 **下载文件**。</span><span class="sxs-lookup"><span data-stu-id="f5811-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="f5811-120">在导出的 CSV 文件中，输入 **SOURCETYPE**、**SOURCEID** 和 **TEAMID** 的值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f5811-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="f5811-121">对于 **SOURCETYPE**，输入“RetailStore”。</span><span class="sxs-lookup"><span data-stu-id="f5811-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="f5811-122">对于 **SOURCEID**，输入商店编号（例如，针对旧金山商店输入“000135”）。</span><span class="sxs-lookup"><span data-stu-id="f5811-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="f5811-123">您可以在 **Retail 和 Commerce \> 渠道 \> 商店** 中找到商店编号。</span><span class="sxs-lookup"><span data-stu-id="f5811-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="f5811-124">对于 **TEAMID**，输入 Microsoft Teams 中相应的团队 ID（例如，“5f8bc92b-6aa8-451e-85d1-3949c01ddc6c”）。</span><span class="sxs-lookup"><span data-stu-id="f5811-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="f5811-125">您可以在 [admin.teams.microsoft.com](https://admin.teams.microsoft.com) 中找到团队 ID 信息。</span><span class="sxs-lookup"><span data-stu-id="f5811-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="f5811-126">将 CSV 文件保存到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="f5811-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="f5811-127">转到 **系统管理 \> 工作区 \> 数据管理**，然后选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="f5811-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="f5811-128">在 **选定实体** 快速选项卡上，选择 **添加文件**。</span><span class="sxs-lookup"><span data-stu-id="f5811-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="f5811-129">将显示 **添加文件** 对话框。</span><span class="sxs-lookup"><span data-stu-id="f5811-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="f5811-130">在 **实体名称** 下拉列表中，选择 **源与团队之间的 Teams 映射**。</span><span class="sxs-lookup"><span data-stu-id="f5811-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="f5811-131">在 **源数据格式** 下拉列表中，选择 **CSV**。</span><span class="sxs-lookup"><span data-stu-id="f5811-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="f5811-132">选择 **上传和添加**，选择之前保存的 CSV 文件，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="f5811-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="f5811-133">在 **添加文件** 对话框中，选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="f5811-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="f5811-134">在操作窗格上，选择 **保存**，然后选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="f5811-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="f5811-135">以下示例图像显示了 Commerce 中的 **导出 Teams 映射** 组，其中具有 **添加实体** 元素并且导出的 CSV 文件标题突出显示。</span><span class="sxs-lookup"><span data-stu-id="f5811-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Commerce 中的导出 Teams 映射组，其中具有添加实体元素并且导出的 CSV 文件标题突出显示](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="f5811-137">完成上述步骤后，请按照[在 Microsoft Teams 和 POS 之间同步任务管理](synchronize-tasks-teams-pos.md)中的步骤同步任务管理。</span><span class="sxs-lookup"><span data-stu-id="f5811-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f5811-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="f5811-138">Additional resources</span></span>

[<span data-ttu-id="f5811-139">Dynamics 365 Commerce 和 Microsoft Teams 集成概览</span><span class="sxs-lookup"><span data-stu-id="f5811-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="f5811-140">启用 Dynamics 365 Commerce 和 Microsoft Teams 集成</span><span class="sxs-lookup"><span data-stu-id="f5811-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="f5811-141">从 Dynamics 365 Commerce 预配 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f5811-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="f5811-142">在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理</span><span class="sxs-lookup"><span data-stu-id="f5811-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="f5811-143">在 Microsoft Teams 中管理用户角色</span><span class="sxs-lookup"><span data-stu-id="f5811-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="f5811-144">Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答</span><span class="sxs-lookup"><span data-stu-id="f5811-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
