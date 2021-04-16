---
title: 设置电子商务开发环境以针对 1 级零售服务器虚拟机进行调试
description: 本主题介绍如何设置电子商务开发环境以针对 1 级零售服务器虚拟机 (VM) 进行调试。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5ef286aa28ff459befb72b0178f308e5fb85ec44
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801475"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="5293a-103">设置电子商务开发环境以针对 1 级零售服务器虚拟机进行调试</span><span class="sxs-lookup"><span data-stu-id="5293a-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5293a-104">本主题介绍如何设置电子商务开发环境以针对 1 级零售服务器虚拟机 (VM) 进行调试。</span><span class="sxs-lookup"><span data-stu-id="5293a-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="5293a-105">说明</span><span class="sxs-lookup"><span data-stu-id="5293a-105">Description</span></span>

<span data-ttu-id="5293a-106">通常会为 Commerce Runtime (CRT) 和销售点 (POS) 扩展开发部署 Microsoft Dynamics 365 Commerce 1 级环境。</span><span class="sxs-lookup"><span data-stu-id="5293a-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="5293a-107">它们是独立的环境。</span><span class="sxs-lookup"><span data-stu-id="5293a-107">They are standalone environments.</span></span> <span data-ttu-id="5293a-108">由于架构具有服务型软件 (SaaS) 性质，因此它们不包含电子商务组件。</span><span class="sxs-lookup"><span data-stu-id="5293a-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="5293a-109">在某些情况下，您可能希望在 1 级环境中测试对扩展的调用，以便可以调试电子商务组件中的扩展。</span><span class="sxs-lookup"><span data-stu-id="5293a-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="5293a-110">有关一般说明，请参阅[针对 1 级商业开发环境进行调试](../e-commerce-extensibility/debug-tier-1.md)。</span><span class="sxs-lookup"><span data-stu-id="5293a-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="5293a-111">当您针对 1 级环境进行调试时，由于该站点现在会调用另一台零售服务器，因此跨服务器调用可能会导致与内容安全策略相关的各种错误。</span><span class="sxs-lookup"><span data-stu-id="5293a-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="5293a-112">下图显示了在产品详细信息页面上选择变体时可能会发生的错误的示例。</span><span class="sxs-lookup"><span data-stu-id="5293a-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![在产品详细信息页面上选择变体时出错](media/unhandled-rejection-error.jpg)

<span data-ttu-id="5293a-114">下图显示了浏览器的调试器工具（F12 开发人员工具）中类似错误的示例。</span><span class="sxs-lookup"><span data-stu-id="5293a-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="5293a-115">该错误消息提到违反内容安全策略指令。</span><span class="sxs-lookup"><span data-stu-id="5293a-115">The error message mentions violation of the content security policy directive.</span></span>

![调试器工具错误](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="5293a-117">解决方法</span><span class="sxs-lookup"><span data-stu-id="5293a-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="5293a-118">在 Commerce 站点构建器中对站点禁用内容安全策略</span><span class="sxs-lookup"><span data-stu-id="5293a-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="5293a-119">选择您正在处理的站点。</span><span class="sxs-lookup"><span data-stu-id="5293a-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="5293a-120">选择 **设置**，然后选择 **扩展**。</span><span class="sxs-lookup"><span data-stu-id="5293a-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="5293a-121">在 **内容安全策略** 选项卡上，选择 **禁用内容安全策略**。</span><span class="sxs-lookup"><span data-stu-id="5293a-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="5293a-122">选择 **保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="5293a-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="5293a-123">企业对消费者 (B2C) 登录在本地开发环境中不起作用。</span><span class="sxs-lookup"><span data-stu-id="5293a-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="5293a-124">但是，您可以根据需要使用来宾结帐或构建页面模拟来模拟用户登录。</span><span class="sxs-lookup"><span data-stu-id="5293a-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5293a-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="5293a-125">Additional resources</span></span>

[<span data-ttu-id="5293a-126">电子商务在线可扩展性开发入门</span><span class="sxs-lookup"><span data-stu-id="5293a-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="5293a-127">在电子商务站点上管理内容安全策略 (CSP)</span><span class="sxs-lookup"><span data-stu-id="5293a-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
