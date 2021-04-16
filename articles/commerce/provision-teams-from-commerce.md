---
title: 从 Dynamics 365 Commerce 预配 Microsoft Teams
description: 本主题介绍如何使用组织数据从 Dynamics 365 Commerce 预配 Microsoft Teams。
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
ms.openlocfilehash: 96382c072e03506294d72899072a358091bda8ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842624"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="7187f-103">从 Dynamics 365 Commerce 预配 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7187f-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7187f-104">本主题介绍如何使用组织数据从 Dynamics 365 Commerce 预配 Microsoft Teams。</span><span class="sxs-lookup"><span data-stu-id="7187f-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7187f-105">如果您尚未在此处为零售商店设置团队，Dynamics 365 Commerce 将提供一种轻松方式来预配 Teams。</span><span class="sxs-lookup"><span data-stu-id="7187f-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="7187f-106">通过利用 Commerce 中要在 Teams 中使用的明确定义的信息，您可以帮助商店员工开始使用 Teams。</span><span class="sxs-lookup"><span data-stu-id="7187f-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="7187f-107">此信息包括组织层次结构、商店名称、员工信息和 Azure Active Directory (Azure AD) 帐户。</span><span class="sxs-lookup"><span data-stu-id="7187f-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="7187f-108">预配 Teams 的流程包括两个主要步骤：</span><span class="sxs-lookup"><span data-stu-id="7187f-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="7187f-109">在 Teams 中，为每个零售商店创建团队，将商店工作人员添加为适当团队的成员。</span><span class="sxs-lookup"><span data-stu-id="7187f-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="7187f-110">如果一名员工与多个零售商店相关联，则团队成员身份将反映这一事实。</span><span class="sxs-lookup"><span data-stu-id="7187f-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="7187f-111">将创建包括区域经理作为成员的通信团队，以帮助从 Teams 发布任务。</span><span class="sxs-lookup"><span data-stu-id="7187f-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="7187f-112">将您的组织层次结构从 Commerce 上传到 Teams。</span><span class="sxs-lookup"><span data-stu-id="7187f-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="7187f-113">在 Commerce Headquarters 中预配 Teams</span><span class="sxs-lookup"><span data-stu-id="7187f-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="7187f-114">在预配 Microsoft Teams 之前，完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="7187f-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="7187f-115">确认所有区域经理均已成为通信经理。</span><span class="sxs-lookup"><span data-stu-id="7187f-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="7187f-116">确认每个商店经理和工作人员的 Azure 帐户已与 Commerce Headquarters 中该经理或工作人员的工作人员记录相关联。</span><span class="sxs-lookup"><span data-stu-id="7187f-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="7187f-117">若要在 Commerce Headquarters 中预配 Teams，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7187f-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="7187f-118">转到 **Retail 和 Commerce \> 渠道设置 \> Microsoft Teams 集成配置**。</span><span class="sxs-lookup"><span data-stu-id="7187f-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="7187f-119">在操作窗格上，选择 **预配团队**。</span><span class="sxs-lookup"><span data-stu-id="7187f-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="7187f-120">将创建名为 **Teams 预配** 的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="7187f-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="7187f-121">转到 **系统管理 \> 查询 \> 批处理作业**，查找具有描述 **Teams 预配** 的最新作业。</span><span class="sxs-lookup"><span data-stu-id="7187f-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="7187f-122">等待此作业完成运行。</span><span class="sxs-lookup"><span data-stu-id="7187f-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="7187f-123">如果您的区域经理、商店经理和商店工作人员均未与 Teams 许可证相关联，您可能会收到以下错误消息：“无法为用户检索适用的 Sku 类别。”</span><span class="sxs-lookup"><span data-stu-id="7187f-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="7187f-124">若要更正此问题，请在操作窗格上选择 **同步团队和成员**。</span><span class="sxs-lookup"><span data-stu-id="7187f-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="7187f-125">在 Teams 管理中心中验证 Teams 预配</span><span class="sxs-lookup"><span data-stu-id="7187f-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="7187f-126">若要在 Microsoft Teams 管理中心中验证 Microsoft Teams 预配，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7187f-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="7187f-127">转到 [Teams 管理中心](https://admin.teams.microsoft.com/)，然后以您的电子商务租户的管理员身份登录。</span><span class="sxs-lookup"><span data-stu-id="7187f-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="7187f-128">在左侧导航窗格中，选择 **Teams** 以展开它，然后选择 **管理团队**。</span><span class="sxs-lookup"><span data-stu-id="7187f-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="7187f-129">确认已为每个 Commerce 零售商店创建了一个团队。</span><span class="sxs-lookup"><span data-stu-id="7187f-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="7187f-130">选择团队，并确认已将商店工作人员作为成员添加到该团队。</span><span class="sxs-lookup"><span data-stu-id="7187f-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="7187f-131">在左侧导航窗格中，选择 **用户**，并确认已将所有商店中的所有商店员工都添加为用户。</span><span class="sxs-lookup"><span data-stu-id="7187f-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="7187f-132">下图显示 Teams 管理中心中 **管理团队** 页面的示例。</span><span class="sxs-lookup"><span data-stu-id="7187f-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Teams 管理中心中“管理团队”页面的示例](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="7187f-134">将 Commerce 组织层次结构上传到 Teams</span><span class="sxs-lookup"><span data-stu-id="7187f-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="7187f-135">Commerce 组织层次结构可在 Microsoft Teams 中使用，以将任务发布到使用相同层次结构的全部或选定商店。</span><span class="sxs-lookup"><span data-stu-id="7187f-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="7187f-136">若要将 Commerce 组织层次结构上传到 Teams，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7187f-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="7187f-137">在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> 渠道设置 \> Microsoft Teams 集成配置**。</span><span class="sxs-lookup"><span data-stu-id="7187f-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="7187f-138">选择 **下载目标层次结构**，然后选择 **零售商店(按地区)** 以下载组织层次结构的以逗号分隔值 (CSV) 文件。</span><span class="sxs-lookup"><span data-stu-id="7187f-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="7187f-139">通过按照[安装 Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install) 中的步骤安装 Microsoft Teams PowerShell 模块。</span><span class="sxs-lookup"><span data-stu-id="7187f-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="7187f-140">当系统提示您位于 Teams PowerShell 窗口中时，使用 Azure AD 租户的管理员帐户登录。</span><span class="sxs-lookup"><span data-stu-id="7187f-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="7187f-141">按照[设置团队目标层次结构](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy)中的步骤为目标层次结构上传 CSV 文件。</span><span class="sxs-lookup"><span data-stu-id="7187f-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="7187f-142">验证组织层次结构是否已上传到 Teams</span><span class="sxs-lookup"><span data-stu-id="7187f-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="7187f-143">若要验证组织层次结构是否已上传到 Microsoft Teams，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7187f-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="7187f-144">以通信经理身份登录到 Teams。</span><span class="sxs-lookup"><span data-stu-id="7187f-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="7187f-145">在左侧导航窗格中，选择 **按 Planner 划分的任务**。</span><span class="sxs-lookup"><span data-stu-id="7187f-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="7187f-146">在 **已发布列表** 选项卡上，创建具有虚拟任务的新列表。</span><span class="sxs-lookup"><span data-stu-id="7187f-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="7187f-147">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="7187f-147">Select **Publish**.</span></span> <span data-ttu-id="7187f-148">组织层次结构应显示在 **选择要发布给的人** 对话框中，如下图中的示例所示。</span><span class="sxs-lookup"><span data-stu-id="7187f-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![“选择要发布给的人”对话框中的组织层次结构的示例](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="7187f-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="7187f-150">Additional resources</span></span>

[<span data-ttu-id="7187f-151">Dynamics 365 Commerce 和 Microsoft Teams 集成概览</span><span class="sxs-lookup"><span data-stu-id="7187f-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="7187f-152">启用 Dynamics 365 Commerce 和 Microsoft Teams 集成</span><span class="sxs-lookup"><span data-stu-id="7187f-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="7187f-153">在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理</span><span class="sxs-lookup"><span data-stu-id="7187f-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="7187f-154">在 Microsoft Teams 中管理用户角色</span><span class="sxs-lookup"><span data-stu-id="7187f-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="7187f-155">如果 Microsoft Teams 中有预先存在的团队，映射商店和团队</span><span class="sxs-lookup"><span data-stu-id="7187f-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="7187f-156">Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答</span><span class="sxs-lookup"><span data-stu-id="7187f-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
