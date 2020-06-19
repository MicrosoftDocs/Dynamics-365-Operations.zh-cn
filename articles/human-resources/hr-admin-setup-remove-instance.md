---
title: 删除实例
description: 此文将指导您如何删除 Microsoft Dynamics 365 Human Resources 的测试驱动器或生产环境。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17f299f81d1326dfb06c11a6125acc54b8ef2a6e
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431191"
---
# <a name="remove-an-instance"></a><span data-ttu-id="4ce8a-103">删除实例</span><span class="sxs-lookup"><span data-stu-id="4ce8a-103">Remove an instance</span></span>

<span data-ttu-id="4ce8a-104">此文将指导您如何删除 Microsoft Dynamics 365 Human Resources 的测试驱动器或生产环境。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="4ce8a-105">删除测试驱动器环境</span><span class="sxs-lookup"><span data-stu-id="4ce8a-105">Remove a test drive environment</span></span>

<span data-ttu-id="4ce8a-106">Human Resources 测试驱动器设置了 60 天的到期策略。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="4ce8a-107">不过，测试驱动器环境的所有者可以选择通过完成以下步骤来提前结束试用。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="4ce8a-108">导航到 [Power Apps 管理中心](https://admin.businessplatform.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="4ce8a-109">选择**环境**。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-109">Select **Environments**.</span></span>
3. <span data-ttu-id="4ce8a-110">选择测试驱动器环境，其命名模式类似于这样：TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="4ce8a-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="4ce8a-111">选择**删除**并确认决定。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="4ce8a-112">现有的测试驱动器环境将被删除。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="4ce8a-113">在删除后，您可以注册新的测试驱动器环境。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="4ce8a-114">删除生产环境</span><span class="sxs-lookup"><span data-stu-id="4ce8a-114">Remove a production environment</span></span>

<span data-ttu-id="4ce8a-115">本文假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="4ce8a-116">因为单个 Human Resources 环境包含在单个 Power Apps 环境中，有两个选项可以考虑。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="4ce8a-117">第一个选项是要删除整个 Power Apps 环境；第二个选项是仅删除 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="4ce8a-118">当您创建 Power Apps 环境的目的明确是为了预配 Human Resources，且您刚刚开始实施或您没有任何既定的集成，这时首选第一个选项。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="4ce8a-119">当您已建立了 Power Apps 环境并使用 Power Apps 和 Power Automate 中利用的富数据填充时，适用第二个选项。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="4ce8a-120">在删除 Power Apps 环境之前，请确保其未在 Human Resources 范围外用于富数据集成。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="4ce8a-121">另请注意，不能删除默认的 Power Apps 环境。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="4ce8a-122">若要删除整个 Power Apps 环境，包括 Human Resources 以及关联的应用和流：</span><span class="sxs-lookup"><span data-stu-id="4ce8a-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="4ce8a-123">导航到 [Power Apps 管理中心](https://admin.businessplatform.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="4ce8a-124">选择**环境**。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-124">Select **Environments**.</span></span>
3. <span data-ttu-id="4ce8a-125">选择要删除的环境。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="4ce8a-126">选择**删除**并确认决定。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="4ce8a-127">等待直到删除完成。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="4ce8a-128">使用您用于订阅 Human Resources 的帐户登录到 [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS)。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="4ce8a-129">选择包含环境的 Human Resources 项目。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="4ce8a-130">在您的 LCS 项目中，选择 **Human Resources 应用管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="4ce8a-131">选择要删除的实例。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="4ce8a-132">选择**删除实例**并确认您的决定。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="4ce8a-133">若要从现有的 Power Apps 环境中删除 Human Resources 环境，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="4ce8a-134">请注意，在直接在 LCS 中支持此功能前，暂时需要 Human Resources DevOps 团队的支持及联系。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="4ce8a-135">联系支持以发起删除请求。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="4ce8a-136">支持团队将向 Human Resources DevOps 团队发起删除请求。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="4ce8a-137">在收到环境已删除的消息后继续操作。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="4ce8a-138">使用您用于订阅 Human Resources 的帐户登录到 LCS。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="4ce8a-139">选择包含环境的 Human Resources 项目。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="4ce8a-140">在您的 LCS 项目中，选择 **Human Resources 应用管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="4ce8a-141">选择要删除的实例，其应标记有部署状态**失败**。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="4ce8a-142">选择**删除实例**并确认您的决定。</span><span class="sxs-lookup"><span data-stu-id="4ce8a-142">Select **Remove instance** and confirm your decision.</span></span> 
