---
title: 启用 Dynamics 365 Commerce 和 Microsoft Teams 集成
description: 本主题介绍如何启用 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成。
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
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019827"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="71e2f-103">启用 Dynamics 365 Commerce 和 Microsoft Teams 集成</span><span class="sxs-lookup"><span data-stu-id="71e2f-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71e2f-104">本主题介绍如何启用 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成。</span><span class="sxs-lookup"><span data-stu-id="71e2f-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="71e2f-105">若要为 Teams 预配 Dynamics 365 Commerce 中的信息并在 Teams 和销售点 (POS) 应用程序之间同步任务管理功能，您必须在 Commerce Headquarters 中启用集成功能。</span><span class="sxs-lookup"><span data-stu-id="71e2f-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="71e2f-106">启用 Teams 集成，即表示您同意与 Teams 共享数据。</span><span class="sxs-lookup"><span data-stu-id="71e2f-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="71e2f-107">与 Teams 共享的数据可能与您的 Commerce 数据位于不同的国家/地区，并且可能受不同的合规性标准约束。</span><span class="sxs-lookup"><span data-stu-id="71e2f-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="71e2f-108">有关详细信息，请参阅 [Microsoft 信任中心](https://www.microsoft.com/trust-center)。</span><span class="sxs-lookup"><span data-stu-id="71e2f-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="71e2f-109">有关 Microsoft 隐私策略的信息，请参阅 [Microsoft 隐私声明](https://aka.ms/privacy)。</span><span class="sxs-lookup"><span data-stu-id="71e2f-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="71e2f-110">启用 Teams 集成</span><span class="sxs-lookup"><span data-stu-id="71e2f-110">Enable Teams integration</span></span>

<span data-ttu-id="71e2f-111">必须先在 Azure 门户中使用您的租户注册 Teams 应用程序，然后才能启用 Microsoft Teams 与 Commerce 的集成。</span><span class="sxs-lookup"><span data-stu-id="71e2f-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="71e2f-112">若要在 Azure 门户中使用您的租户注册 Teams 应用程序，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="71e2f-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="71e2f-113">按照[快速入门：在 Microsoft 身份平台中注册应用](/azure/active-directory/develop/quickstart-register-app)中的步骤操作，以在 Azure 门户中使用您的租户注册 Teams 应用程序。</span><span class="sxs-lookup"><span data-stu-id="71e2f-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="71e2f-114">复制已注册应用的 **概述** 页面中的 **应用程序（客户端）ID** 值。</span><span class="sxs-lookup"><span data-stu-id="71e2f-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="71e2f-115">您将使用该值在 Commerce Headquarters 中启用 Teams 集成。</span><span class="sxs-lookup"><span data-stu-id="71e2f-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="71e2f-116">复制您在步骤 1 中[添加证书](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)时输入的证书值。</span><span class="sxs-lookup"><span data-stu-id="71e2f-116">Copy the certificate value that was entered when you [added a certificate](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="71e2f-117">该证书也称为公钥或应用程序密钥。</span><span class="sxs-lookup"><span data-stu-id="71e2f-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="71e2f-118">您将使用该值在 Commerce Headquarters 中启用 Teams 集成。</span><span class="sxs-lookup"><span data-stu-id="71e2f-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="71e2f-119">若要在 Commerce Headquarters 中启用 Teams 集成，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="71e2f-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="71e2f-120">转到 **Retail 和 Commerce \> 渠道设置 \> Microsoft Teams 集成配置**。</span><span class="sxs-lookup"><span data-stu-id="71e2f-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="71e2f-121">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="71e2f-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="71e2f-122">将 **启用 Microsoft Teams 集成** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="71e2f-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="71e2f-123">在 **应用程序 ID** 和 **应用程序密钥** 字段中，输入您在 Azure 门户中注册 Teams 应用程序时获取的值。</span><span class="sxs-lookup"><span data-stu-id="71e2f-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="71e2f-124">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="71e2f-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="71e2f-125">下图显示在 Commerce Headquarters 中配置 Teams 集成的示例。</span><span class="sxs-lookup"><span data-stu-id="71e2f-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Commerce Headquarters 中的 Teams 集成配置](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="71e2f-127">禁用 Teams 集成</span><span class="sxs-lookup"><span data-stu-id="71e2f-127">Disable Teams integration</span></span>

<span data-ttu-id="71e2f-128">若要在 Commerce Headquarters 中禁用 Microsoft Teams 集成，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="71e2f-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="71e2f-129">转到 **Retail 和 Commerce \> 渠道设置 \> Microsoft Teams 集成配置**。</span><span class="sxs-lookup"><span data-stu-id="71e2f-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="71e2f-130">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="71e2f-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="71e2f-131">将 **启用 Microsoft Teams 集成** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="71e2f-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="71e2f-132">清除 **应用程序 ID** 和 **应用程序密钥** 字段中的值。</span><span class="sxs-lookup"><span data-stu-id="71e2f-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="71e2f-133">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="71e2f-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="71e2f-134">禁用 Teams 与 Commerce 的集成后，POS 终端将不再显示从 Teams 应用程序发布的任务。</span><span class="sxs-lookup"><span data-stu-id="71e2f-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71e2f-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="71e2f-135">Additional resources</span></span>

[<span data-ttu-id="71e2f-136">Dynamics 365 Commerce 和 Microsoft Teams 集成概览</span><span class="sxs-lookup"><span data-stu-id="71e2f-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="71e2f-137">从 Dynamics 365 Commerce 预配 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="71e2f-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="71e2f-138">在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理</span><span class="sxs-lookup"><span data-stu-id="71e2f-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="71e2f-139">在 Microsoft Teams 中管理用户角色</span><span class="sxs-lookup"><span data-stu-id="71e2f-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="71e2f-140">如果 Microsoft Teams 中有预先存在的团队，映射商店和团队</span><span class="sxs-lookup"><span data-stu-id="71e2f-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="71e2f-141">Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答</span><span class="sxs-lookup"><span data-stu-id="71e2f-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)