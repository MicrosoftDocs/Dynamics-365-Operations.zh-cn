---
title: 开始使用成本核算服务（私人预览版）
description: 本主题提供成本核算服务的许可详细信息和安装说明。
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: a82af9e8ec1806f470103897389d0316d33a4a06
ms.sourcegitcommit: 7fec9dc5297ed6e687d4a0dff099922d59d6a830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372728"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="1b86c-103">开始使用成本核算服务（私人预览版）</span><span class="sxs-lookup"><span data-stu-id="1b86c-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="1b86c-104">本主题中介绍的功能作为专用预览版的一部分提供。</span><span class="sxs-lookup"><span data-stu-id="1b86c-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="1b86c-105">本主题的内容及所介绍的功能可能会发生变化。</span><span class="sxs-lookup"><span data-stu-id="1b86c-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="1b86c-106">有关预览版的详细信息，请参阅[一个版本服务更新常见问题](../../fin-ops-core/fin-ops/get-started/one-version.md)。</span><span class="sxs-lookup"><span data-stu-id="1b86c-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="1b86c-107">成本核算服务使您可以在已设置的成本核算分类帐中执行多个库存核算。</span><span class="sxs-lookup"><span data-stu-id="1b86c-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="1b86c-108">您将每个成本核算分类帐与一个*惯例*关联。</span><span class="sxs-lookup"><span data-stu-id="1b86c-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="1b86c-109">惯例是以下几种会计政策的集合：</span><span class="sxs-lookup"><span data-stu-id="1b86c-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="1b86c-110">成本对象</span><span class="sxs-lookup"><span data-stu-id="1b86c-110">Cost object</span></span>
- <span data-ttu-id="1b86c-111">输入度量依据</span><span class="sxs-lookup"><span data-stu-id="1b86c-111">Input measurement basis</span></span>
- <span data-ttu-id="1b86c-112">成本流假设</span><span class="sxs-lookup"><span data-stu-id="1b86c-112">Cost flow assumption</span></span>
- <span data-ttu-id="1b86c-113">成本元素</span><span class="sxs-lookup"><span data-stu-id="1b86c-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="1b86c-114">即使您打开了成本核算服务，仍然可以照常在 Microsoft Dynamics 365 Supply Chain Management 中执行库存核算。</span><span class="sxs-lookup"><span data-stu-id="1b86c-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="1b86c-115">成本核算服务是一个加载项。</span><span class="sxs-lookup"><span data-stu-id="1b86c-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="1b86c-116">要使其功能可用，必须从 Microsoft Dynamics Lifecycle Services (LCS) 进行安装。</span><span class="sxs-lookup"><span data-stu-id="1b86c-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="1b86c-117">因此，您可以选择在测试环境中对其进行评估，然后再将其打开用于生产环境。</span><span class="sxs-lookup"><span data-stu-id="1b86c-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="1b86c-118">成本核算服务当前不支持 Dynamics 365 Supply Chain Management 内置的所有成本管理功能。</span><span class="sxs-lookup"><span data-stu-id="1b86c-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1b86c-119">因此，重要的是要评估当前可用的功能集是否满足您的要求。</span><span class="sxs-lookup"><span data-stu-id="1b86c-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="1b86c-120">如何获取成本核算服务（私人预览版）</span><span class="sxs-lookup"><span data-stu-id="1b86c-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b86c-121">若要使用成本核算服务，您必须具有启用 LCS 的高可用性环境（不是 OneBox 环境），并且您必须运行 Dynamics 365 Supply Chain Management 版本 10.0.11 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="1b86c-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="1b86c-122">若要注册成本核算服务私人预览版，请通过电子邮件向[成本核算服务（私人预览版）](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29)发送 LCS 环境 ID。</span><span class="sxs-lookup"><span data-stu-id="1b86c-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="1b86c-123">批准您参加此计划之后，我们将向您发送跟进电子邮件，其中包含成本核算服务测试密钥。</span><span class="sxs-lookup"><span data-stu-id="1b86c-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="1b86c-124">收到测试密钥之后，您可以继续[安装加载项](#install)。</span><span class="sxs-lookup"><span data-stu-id="1b86c-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="1b86c-125">许可授权</span><span class="sxs-lookup"><span data-stu-id="1b86c-125">Licensing</span></span>

<span data-ttu-id="1b86c-126">成本核算服务与可用于 Supply Chain Management 的库存核算标准功能一起获得许可。</span><span class="sxs-lookup"><span data-stu-id="1b86c-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="1b86c-127">您无需购买其他许可证即可使用成本核算服务。</span><span class="sxs-lookup"><span data-stu-id="1b86c-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="1b86c-128">安装加载项</span><span class="sxs-lookup"><span data-stu-id="1b86c-128">Install the add-in</span></span>

<span data-ttu-id="1b86c-129">要使用成本核算服务，请按照以下过程中的说明安装用于 Supply Chain Management 的成本核算服务加载项。</span><span class="sxs-lookup"><span data-stu-id="1b86c-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="1b86c-130">[注册](#sign-up)成本核算服务（私人预览版）。</span><span class="sxs-lookup"><span data-stu-id="1b86c-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="1b86c-131">登录 LCS。</span><span class="sxs-lookup"><span data-stu-id="1b86c-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="1b86c-132">转到**预览功能管理**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="1b86c-133">选择加号 (**+**)。</span><span class="sxs-lookup"><span data-stu-id="1b86c-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="1b86c-134">在**代码**字段中，输入您的成本核算服务的加载项测试密钥。</span><span class="sxs-lookup"><span data-stu-id="1b86c-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="1b86c-135">（您应该已经通过电子邮件收到了密钥。）</span><span class="sxs-lookup"><span data-stu-id="1b86c-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="1b86c-136">选择**解锁**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="1b86c-137">打开要在其中添加服务的 LCS 环境。</span><span class="sxs-lookup"><span data-stu-id="1b86c-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="1b86c-138">转到**完整详细信息**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="1b86c-139">向下滚动到**环境加载项**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="1b86c-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="1b86c-140">选择**安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="1b86c-141">选择**成本核算服务**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="1b86c-142">按照安装指南操作，并同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="1b86c-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="1b86c-143">选择**安装**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-143">Select **Install**.</span></span>

1. <span data-ttu-id="1b86c-144">在**环境加载项**快速选项卡上，您应该会看到正在安装成本核算服务。</span><span class="sxs-lookup"><span data-stu-id="1b86c-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="1b86c-145">几分钟后，状态应从**正在安装**变为**已安装**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="1b86c-146">（您可能必须刷新页面才能看到此改变。）此时，成本核算服务已经可以使用。</span><span class="sxs-lookup"><span data-stu-id="1b86c-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="1b86c-147">设置集成</span><span class="sxs-lookup"><span data-stu-id="1b86c-147">Set up the integration</span></span>

<span data-ttu-id="1b86c-148">要设置成本核算服务与 Dynamics 365 Supply Chain Management 之间的集成：</span><span class="sxs-lookup"><span data-stu-id="1b86c-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="1b86c-149">转到**系统管理 > 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="1b86c-150">选择**检查更新**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="1b86c-151">打开**所有**选项卡，搜索名为*成本核算服务*的功能。</span><span class="sxs-lookup"><span data-stu-id="1b86c-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="1b86c-152">选择**立即启用**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="1b86c-153">转到**成本管理 > 成本核算服务 > 设置 > 成本核算服务参数 > 集成参数**。</span><span class="sxs-lookup"><span data-stu-id="1b86c-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="1b86c-154">在**应用程序 ID** 字段中，输入以下代码：</span><span class="sxs-lookup"><span data-stu-id="1b86c-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="1b86c-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="1b86c-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="1b86c-156">在**数据服务终结点**字段中，输入以下 URL：</span><span class="sxs-lookup"><span data-stu-id="1b86c-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="1b86c-157">在**成本核算服务终结点**字段中，输入以下 URL：</span><span class="sxs-lookup"><span data-stu-id="1b86c-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="1b86c-158">成本核算服务现在可以使用了。</span><span class="sxs-lookup"><span data-stu-id="1b86c-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="1b86c-159">相关资源</span><span class="sxs-lookup"><span data-stu-id="1b86c-159">Related resources</span></span>

[<span data-ttu-id="1b86c-160">成本核算服务主页</span><span class="sxs-lookup"><span data-stu-id="1b86c-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
