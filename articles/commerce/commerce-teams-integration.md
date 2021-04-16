---
title: Dynamics 365 Commerce 和 Microsoft Teams 集成概览
description: 本主题介绍了 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成的概览。
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
ms.openlocfilehash: 3b7872757815d4eec0393e8b1c8c6ff5467e9473
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842618"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="79e6f-103">Dynamics 365 Commerce 和 Microsoft Teams 集成概览</span><span class="sxs-lookup"><span data-stu-id="79e6f-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="79e6f-104">本主题介绍了 Microsoft Dynamics 365 Commerce 和 Microsoft Teams 集成的概览。</span><span class="sxs-lookup"><span data-stu-id="79e6f-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="79e6f-105">Dynamics 365 Commerce 将与 Teams 集成，以通过同步两个应用程序之间的任务管理来帮助客户及其员工提供工作效率。</span><span class="sxs-lookup"><span data-stu-id="79e6f-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="79e6f-106">Commerce 和 Teams 集成提供的无缝任务管理使商店经理和员工可以创建任务列表，将任务分配到多个商店，并从任一应用程序跟踪跨商店的任务状态。</span><span class="sxs-lookup"><span data-stu-id="79e6f-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="79e6f-107">Commerce 和 Teams 集成从 Commerce 版本 10.0.18 版本开始可用。</span><span class="sxs-lookup"><span data-stu-id="79e6f-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="79e6f-108">主要功能</span><span class="sxs-lookup"><span data-stu-id="79e6f-108">Key features</span></span>

<span data-ttu-id="79e6f-109">以下是 Commerce 和 Microsoft Teams 集成提供的一些关键功能：</span><span class="sxs-lookup"><span data-stu-id="79e6f-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="79e6f-110">通过利用 Commerce 中明确定义的信息（例如组织结构和有关商店、工作人员、权限和业务环境的信息）预配 Teams。</span><span class="sxs-lookup"><span data-stu-id="79e6f-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="79e6f-111">在 Commerce 和 Teams 之间轻松同步正在进行的更改（例如，添加新商店或雇用新员工），但保持 Commerce 为组织结构数据的主要来源。</span><span class="sxs-lookup"><span data-stu-id="79e6f-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="79e6f-112">在 Commerce 和 Teams 之间集成任务管理，以帮助商店工作人员、商店经理、区域经理和通信经理从任一应用程序处理任务管理。</span><span class="sxs-lookup"><span data-stu-id="79e6f-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="79e6f-113">使用集成功能的先决条件</span><span class="sxs-lookup"><span data-stu-id="79e6f-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="79e6f-114">必须先满足以下先决条件，然后才能开始使用 Microsoft Teams 集成功能：</span><span class="sxs-lookup"><span data-stu-id="79e6f-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="79e6f-115">Microsoft 365 商业版标准许可证（此许可证包括 Teams。）</span><span class="sxs-lookup"><span data-stu-id="79e6f-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="79e6f-116">适用于所有商店经理和工作人员的 Azure Active Directory (Azure AD) 帐户</span><span class="sxs-lookup"><span data-stu-id="79e6f-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="79e6f-117">使用 Azure AD 身份验证配置的销售点 (POS) 系统</span><span class="sxs-lookup"><span data-stu-id="79e6f-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="79e6f-118">概念体系结构</span><span class="sxs-lookup"><span data-stu-id="79e6f-118">Conceptual architecture</span></span>

<span data-ttu-id="79e6f-119">下图显示 Dynamics 365 Commerce 和 Microsoft Teams 集成的概念体系结构，以旧金山商店为例。</span><span class="sxs-lookup"><span data-stu-id="79e6f-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="79e6f-120">Teams 和 Commerce POS 应用程序使用 Microsoft Planner 作为存储库，以便从 Teams 发布的任务显示在 POS 应用程序中，而由商店经理在 POS 应用程序中创建的临时任务显示在 Teams 中，从而在应用程序之间提供无缝的任务管理体验。</span><span class="sxs-lookup"><span data-stu-id="79e6f-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Commerce 和 Teams 集成的体系结构](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="79e6f-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="79e6f-122">Additional resources</span></span>

[<span data-ttu-id="79e6f-123">启用 Dynamics 365 Commerce 和 Microsoft Teams 集成</span><span class="sxs-lookup"><span data-stu-id="79e6f-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="79e6f-124">从 Dynamics 365 Commerce 预配 Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="79e6f-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="79e6f-125">在 Microsoft Teams 和 Dynamics 365 Commerce POS 之间同步任务管理</span><span class="sxs-lookup"><span data-stu-id="79e6f-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="79e6f-126">在 Microsoft Teams 中管理用户角色</span><span class="sxs-lookup"><span data-stu-id="79e6f-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="79e6f-127">如果 Microsoft Teams 中有预先存在的团队，映射商店和团队</span><span class="sxs-lookup"><span data-stu-id="79e6f-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="79e6f-128">Dynamics 365 Commerce 和 Microsoft Teams 集成常见问题解答</span><span class="sxs-lookup"><span data-stu-id="79e6f-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
