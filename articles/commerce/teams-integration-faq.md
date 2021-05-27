---
title: Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答
description: 本主题提供对有关 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成的常见问题的解答。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019462"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="57474-103">Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答</span><span class="sxs-lookup"><span data-stu-id="57474-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57474-104">本主题提供对有关 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成的常见问题的解答。</span><span class="sxs-lookup"><span data-stu-id="57474-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="57474-105">当从 Commerce 预配 Teams 时，商店中的谁将成为团队的负责人？</span><span class="sxs-lookup"><span data-stu-id="57474-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="57474-106">所有商店经理都将作为负责人自动添加到相应的团队组中，以便他们可以执行诸如添加专有渠道以及添加或删除成员的操作。</span><span class="sxs-lookup"><span data-stu-id="57474-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="57474-107">如何在 Commerce Headquarters 中向员工分配“通信经理”角色？</span><span class="sxs-lookup"><span data-stu-id="57474-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="57474-108">Microsoft Teams 中的通信经理能够创建和发布任务列表。</span><span class="sxs-lookup"><span data-stu-id="57474-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="57474-109">需要成为通信经理的组织员工必须在 Commerce Headquarters 中向他们分配了“零售任务经理”角色。</span><span class="sxs-lookup"><span data-stu-id="57474-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="57474-110">若要在 Commerce Headquarters 中向员工分配零售任务经理角色，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="57474-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="57474-111">转到 **Retail 和 Commerce \> 员工 \> 用户**。</span><span class="sxs-lookup"><span data-stu-id="57474-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="57474-112">选择某一员工。</span><span class="sxs-lookup"><span data-stu-id="57474-112">Select an employee.</span></span>
1. <span data-ttu-id="57474-113">在 **用户的角色** 快速选项卡，选择 **分配角色**。</span><span class="sxs-lookup"><span data-stu-id="57474-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="57474-114">在 **将角色分配给用户** 对话框中，选择 **零售任务经理** 角色，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="57474-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="57474-115">如何使特定的组织层次结构可上传到 Microsoft Teams 中？</span><span class="sxs-lookup"><span data-stu-id="57474-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="57474-116">在 Commerce Headquarters 中，每个组织的层次结构都关联了一个或多个目的。</span><span class="sxs-lookup"><span data-stu-id="57474-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="57474-117">确保要预配到 Microsoft Teams 中的层次结构有与之关联的 **零售报告** 目的，如以下示例图像所示。</span><span class="sxs-lookup"><span data-stu-id="57474-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Commerce Headquarters 中组织层次结构目的示例](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="57474-119">如何使零售商店工作人员使用 Azure Active Directory (Azure AD) 登录到 Commerce 销售点 (POS)？</span><span class="sxs-lookup"><span data-stu-id="57474-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="57474-120">有关如何将 Commerce POS 登录体验配置为使用 Azure AD 身份验证的信息，请参阅[为 POS 登录启用 Azure Active Directory 身份验证](aad-pos-logon.md)。</span><span class="sxs-lookup"><span data-stu-id="57474-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="57474-121">如果我的组织已在 Microsoft Teams 中创建团队，如何在 Commerce Headquarters 中映射商店和相应的团队？</span><span class="sxs-lookup"><span data-stu-id="57474-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="57474-122">有关在有预先存在的团队的情况下如何映射商店和团队的信息，请参阅[如果您的组织在 Microsoft Teams 中有预先存在的团队，请映射商店和相应的团队](map-stores-existing-teams.md)。</span><span class="sxs-lookup"><span data-stu-id="57474-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="57474-123">如何清除会话存储中存储的 Microsoft Graph API 令牌？</span><span class="sxs-lookup"><span data-stu-id="57474-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="57474-124">使用 Azure Active Directory (Azure AD) 帐户登录到销售点 (POS) 的用户应从 POS 注销或关闭应用程序以清除会话存储。</span><span class="sxs-lookup"><span data-stu-id="57474-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="57474-125">建议的最佳做法是始终让商店工作人员锁定 POS 终端或在不使用终端时从会话中注销。</span><span class="sxs-lookup"><span data-stu-id="57474-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="57474-126">如果商店没有商店经理，会发生什么情况？</span><span class="sxs-lookup"><span data-stu-id="57474-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="57474-127">如果商店没有经理，将不会为商店或在 Teams 中创建团队组。</span><span class="sxs-lookup"><span data-stu-id="57474-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="57474-128">如果商店经理离开公司，会发生什么情况？</span><span class="sxs-lookup"><span data-stu-id="57474-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="57474-129">具有负责人角色的任何人都可以在 Commerce Headquarters 中添加新的商店经理，并重新预配 Teams，以便新经理在 Teams 中具有对组的必要特权。</span><span class="sxs-lookup"><span data-stu-id="57474-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="57474-130">其他资源</span><span class="sxs-lookup"><span data-stu-id="57474-130">Additional resources</span></span>

[<span data-ttu-id="57474-131">Dynamics 365 Commerce 和 Microsoft Teams 集成概览</span><span class="sxs-lookup"><span data-stu-id="57474-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="57474-132">启用 Dynamics 365 Commerce 和 Microsoft Teams 集成</span><span class="sxs-lookup"><span data-stu-id="57474-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="57474-133">从 Dynamics 365 Commerce 预配 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="57474-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="57474-134">在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理</span><span class="sxs-lookup"><span data-stu-id="57474-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="57474-135">在 Microsoft Teams 中管理用户角色</span><span class="sxs-lookup"><span data-stu-id="57474-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="57474-136">如果 Microsoft Teams 中有预先存在的团队，映射商店和团队</span><span class="sxs-lookup"><span data-stu-id="57474-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
