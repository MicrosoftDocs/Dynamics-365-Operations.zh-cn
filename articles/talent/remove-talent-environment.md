---
title: "删除 Talent 环境"
description: "此主题将指导您如何删除 Microsoft Dynamics 365 for Talent 的测试驱动器或生产环境。"
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 5080f1ec182b8cbdf281967185a1afeb9887f682
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---
# <a name="remove-talent-environments"></a><span data-ttu-id="ef836-103">删除 Talent 环境</span><span class="sxs-lookup"><span data-stu-id="ef836-103">Remove Talent environments</span></span>

<span data-ttu-id="ef836-104">此主题将指导您如何删除 Microsoft Dynamics 365 for Talent 的测试驱动器或生产环境。</span><span class="sxs-lookup"><span data-stu-id="ef836-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="ef836-105">删除测试驱动器环境</span><span class="sxs-lookup"><span data-stu-id="ef836-105">Removing a test drive environment</span></span>

<span data-ttu-id="ef836-106">Talent 测试驱动器设置了 60 天的到期策略。</span><span class="sxs-lookup"><span data-stu-id="ef836-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="ef836-107">不过，测试驱动器环境的所有者可以选择通过完成以下步骤来提前结束试用。</span><span class="sxs-lookup"><span data-stu-id="ef836-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="ef836-108">导航到 [PowerApps 管理中心](https://admin.businessplatform.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="ef836-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="ef836-109">选择**环境**。</span><span class="sxs-lookup"><span data-stu-id="ef836-109">Select **Environments**.</span></span>
3. <span data-ttu-id="ef836-110">选择测试驱动器环境，其命名模式类似于这样：TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="ef836-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="ef836-111">选择**删除**并确认决定。</span><span class="sxs-lookup"><span data-stu-id="ef836-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="ef836-112">现有的测试驱动器环境将被删除。</span><span class="sxs-lookup"><span data-stu-id="ef836-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="ef836-113">在删除后，您可以注册新的测试驱动器环境。</span><span class="sxs-lookup"><span data-stu-id="ef836-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="ef836-114">删除生产环境</span><span class="sxs-lookup"><span data-stu-id="ef836-114">Removing a production environment</span></span>

<span data-ttu-id="ef836-115">此主题假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Talent。</span><span class="sxs-lookup"><span data-stu-id="ef836-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="ef836-116">因为单个 Talent 环境“包含”在单个 PowerApps 环境中，有两个选项可以考虑。</span><span class="sxs-lookup"><span data-stu-id="ef836-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="ef836-117">第一个选项是要删除整个 PowerApps 环境；第二个选项是仅删除 Talent。</span><span class="sxs-lookup"><span data-stu-id="ef836-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="ef836-118">当您创建 PowerApps 环境的目的明确是为了配置 Talent，且您刚刚开始实施或您没有任何既定的集成，这时首选第一个选项。</span><span class="sxs-lookup"><span data-stu-id="ef836-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="ef836-119">当您已建立了 PowerApps 环境并使用 PowerApps 和 Flows 中利用的富数据填充时，适用第二个选项。</span><span class="sxs-lookup"><span data-stu-id="ef836-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="ef836-120">在删除 PowerApps 环境之前，请确保其未在 Talent 范围外用于富数据集成。</span><span class="sxs-lookup"><span data-stu-id="ef836-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="ef836-121">另请注意，不能删除默认的 PowerApps 环境。</span><span class="sxs-lookup"><span data-stu-id="ef836-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="ef836-122">若要删除整个 PowerApps 环境，包括 Talent 以及关联的应用和流：</span><span class="sxs-lookup"><span data-stu-id="ef836-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="ef836-123">导航到 [PowerApps 管理中心](https://admin.businessplatform.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="ef836-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="ef836-124">选择**环境**。</span><span class="sxs-lookup"><span data-stu-id="ef836-124">Select **Environments**.</span></span>
3. <span data-ttu-id="ef836-125">选择要删除的环境。</span><span class="sxs-lookup"><span data-stu-id="ef836-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="ef836-126">选择**删除**并确认决定。</span><span class="sxs-lookup"><span data-stu-id="ef836-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="ef836-127">等待直到删除完成。</span><span class="sxs-lookup"><span data-stu-id="ef836-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="ef836-128">使用您用于订阅 Talent 的帐户登录到 [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS)。</span><span class="sxs-lookup"><span data-stu-id="ef836-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="ef836-129">选择包含环境的 Talent 项目。</span><span class="sxs-lookup"><span data-stu-id="ef836-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="ef836-130">在您的 LCS 项目中，选择 **Talent 应用管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="ef836-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="ef836-131">选择要删除的实例。</span><span class="sxs-lookup"><span data-stu-id="ef836-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="ef836-132">选择**删除实例**并确认您的决定。</span><span class="sxs-lookup"><span data-stu-id="ef836-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="ef836-133">若要从现有的 PowerApps 环境中删除 Talent 环境，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="ef836-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="ef836-134">请注意，在直接在 LCS 中支持此功能前，暂时需要 Talent DevOps 团队的支持及联系。</span><span class="sxs-lookup"><span data-stu-id="ef836-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="ef836-135">联系支持以发起删除请求。</span><span class="sxs-lookup"><span data-stu-id="ef836-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="ef836-136">支持团队将向 Talent DevOps 团队发起删除请求。</span><span class="sxs-lookup"><span data-stu-id="ef836-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="ef836-137">在收到环境已删除的消息后继续操作。</span><span class="sxs-lookup"><span data-stu-id="ef836-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="ef836-138">使用您用于订阅 Talent 的帐户登录到 LCS。</span><span class="sxs-lookup"><span data-stu-id="ef836-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="ef836-139">选择包含环境的 Talent 项目。</span><span class="sxs-lookup"><span data-stu-id="ef836-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="ef836-140">在您的 LCS 项目中，选择 **Talent 应用管理**磁贴。</span><span class="sxs-lookup"><span data-stu-id="ef836-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="ef836-141">选择要删除的实例，其应标记有部署状态**失败**。</span><span class="sxs-lookup"><span data-stu-id="ef836-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="ef836-142">选择**删除实例**并确认您的决定。</span><span class="sxs-lookup"><span data-stu-id="ef836-142">Select **Remove instance** and confirm your decision.</span></span> 


