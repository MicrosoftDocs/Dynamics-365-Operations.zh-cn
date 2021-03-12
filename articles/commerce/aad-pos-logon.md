---
title: 对 POS 登录启用 Azure Active Directory 身份验证
description: 此主题介绍如何为 Microsoft Dynamics 365 Commerce 销售点 (POS) 配置登录体验，以便使用 Azure Active Directory 身份验证。
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982732"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="3caa8-103">对 POS 登录启用 Azure Active Directory 身份验证</span><span class="sxs-lookup"><span data-stu-id="3caa8-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="3caa8-104">许多使用 Microsoft Dynamics 365 Commerce 的客户也使用其他 Microsoft 云服务，并且可能使用 Azure Active Directory (Azure AD) 来管理这些服务的用户凭据。</span><span class="sxs-lookup"><span data-stu-id="3caa8-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="3caa8-105">在这些情况下，客户可能希望在多个应用程序中使用同一个 Azure AD 帐户。</span><span class="sxs-lookup"><span data-stu-id="3caa8-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="3caa8-106">此主题介绍如何配置 Commerce 销售点 (POS) 登录体验，以便使用 Azure AD 身份验证。</span><span class="sxs-lookup"><span data-stu-id="3caa8-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="3caa8-107">配置 Azure AD 身份验证</span><span class="sxs-lookup"><span data-stu-id="3caa8-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="3caa8-108">若要将 Azure AD 设置为商店的 POS 登录身份验证方法，必须配置商店的功能配置文件设置，然后将这些设置应用于 POS 客户端。</span><span class="sxs-lookup"><span data-stu-id="3caa8-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="3caa8-109">若要配置功能配置文件，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3caa8-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="3caa8-110">转至 **Retail 和 Commerce** \> **渠道设置** \> **POS 设置** \> **POS 配置文件** \> **功能配置文件**。</span><span class="sxs-lookup"><span data-stu-id="3caa8-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="3caa8-111">选择要更改的功能配置文件。</span><span class="sxs-lookup"><span data-stu-id="3caa8-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="3caa8-112">在 **功能** 快速选项卡上的 **POS 职员登录** 部分中，将 **登录身份验证方法** 字段的值从 **个人 ID 和密码** 更改为 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="3caa8-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="3caa8-113">默认情况下，所有功能配置文件都使用 **个人 ID 和密码** 作为 POS 身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="3caa8-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="3caa8-114">因此，如果要使用 Azure AD，必须更改 **登录身份验证方法** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="3caa8-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="3caa8-115">此更改将影响链接到所选功能配置文件的每家零售商店。</span><span class="sxs-lookup"><span data-stu-id="3caa8-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="3caa8-116">若要将这些设置应用于 POS 客户端，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3caa8-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="3caa8-117">转到 **Retail 和 Commerce** \> **Retail 和 Commerce IT** \> **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="3caa8-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="3caa8-118">运行 **1070**（**渠道配置**）配送计划。</span><span class="sxs-lookup"><span data-stu-id="3caa8-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="3caa8-119">Azure AD 身份验证需要 Internet 连接。</span><span class="sxs-lookup"><span data-stu-id="3caa8-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="3caa8-120">如果 POS 处于脱机模式，将不能工作。</span><span class="sxs-lookup"><span data-stu-id="3caa8-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="3caa8-121">目前，**经理覆盖** 功能不支持将 Azure AD 作为身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="3caa8-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="3caa8-122">即使将 Azure AD 配置为 POS 登录的身份验证方法，也需要操作员 ID 和密码。</span><span class="sxs-lookup"><span data-stu-id="3caa8-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="3caa8-123">将 Azure AD 帐户与工作人员关联</span><span class="sxs-lookup"><span data-stu-id="3caa8-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="3caa8-124">必须先将 Azure AD 帐户与商店工作人员关联，该工作人员才能使用 Azure AD 帐户登录 POS 应用程序。</span><span class="sxs-lookup"><span data-stu-id="3caa8-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="3caa8-125">若要将 Azure AD 帐户与工作人员关联，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3caa8-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="3caa8-126">转到 **Retail 和 Commerce** \> **员工** \> **工作人员**。</span><span class="sxs-lookup"><span data-stu-id="3caa8-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="3caa8-127">打开工作人员的详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="3caa8-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="3caa8-128">在操作窗格中 **Commerce** 选项卡上的 **外部标识** 组中，选择 **关联现有标识**。</span><span class="sxs-lookup"><span data-stu-id="3caa8-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="3caa8-129">在 **使用现有外部标识** 对话框中，选择 **使用电子邮件搜索**，输入 Azure AD 电子邮件地址，然后选择 **搜索**。</span><span class="sxs-lookup"><span data-stu-id="3caa8-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="3caa8-130">选择返回的 Azure AD 帐户，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3caa8-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="3caa8-131">将填写该工作人员详细信息页的 **Commerce** 选项卡中的 **别名**、**UPN** 和 **外部子标识** 字段。</span><span class="sxs-lookup"><span data-stu-id="3caa8-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="3caa8-132">更新工作记录后，例如，如果关联了新的 Azure AD 帐户，更改了密码或更新了员工通讯簿，建议您运行 **1060**（**人员**）分配计划将最新的人员信息同步到渠道。</span><span class="sxs-lookup"><span data-stu-id="3caa8-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="3caa8-133">这样，POS 应用程序可以获取正确的数据以进行用户身份验证和授权检查。</span><span class="sxs-lookup"><span data-stu-id="3caa8-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3caa8-134">其他资源</span><span class="sxs-lookup"><span data-stu-id="3caa8-134">Additional resources</span></span>

[<span data-ttu-id="3caa8-135">为 MPOS 和 Cloud POS 设置扩展登录功能</span><span class="sxs-lookup"><span data-stu-id="3caa8-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="3caa8-136">创建零售功能配置文件</span><span class="sxs-lookup"><span data-stu-id="3caa8-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="3caa8-137">配置工作人员</span><span class="sxs-lookup"><span data-stu-id="3caa8-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
