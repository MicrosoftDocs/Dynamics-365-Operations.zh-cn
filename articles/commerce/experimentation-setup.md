---
title: 设置试验
description: 本主题介绍了如何在第三方服务中设置试验。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: dfd7b8cb13f4d69811b5a86b971fa1b57c75bd36
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234601"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="c5445-103">设置试验</span><span class="sxs-lookup"><span data-stu-id="c5445-103">Set up an experiment</span></span>

<span data-ttu-id="c5445-104">在[定义假设并确定您要使用哪些成功指标](experimentation-identify.md)后，您需要在第三方服务中设置试验。</span><span class="sxs-lookup"><span data-stu-id="c5445-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="c5445-105">下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。</span><span class="sxs-lookup"><span data-stu-id="c5445-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c5445-106">其他步骤在单独的主题中介绍。</span><span class="sxs-lookup"><span data-stu-id="c5445-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="c5445-107">[![试验用户旅程 - 设置](./media/experimentation_setup.svg)](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c5445-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="c5445-108">在第三方服务中设置试验</span><span class="sxs-lookup"><span data-stu-id="c5445-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="c5445-109">到目前为止，您应该已经选择了第三方服务来运行和监视您的试验，并设置了试验连接器。</span><span class="sxs-lookup"><span data-stu-id="c5445-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="c5445-110">这些先决条件在 [Dynamics 365 Commerce 中的试验](experimentation-overview.md)中列出。</span><span class="sxs-lookup"><span data-stu-id="c5445-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="c5445-111">请按照在第三方服务中创建试验所需的步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="c5445-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="c5445-112">如果连接器配置正确，则您在第三方服务中设置的试验的完整列表将在大约 5 分钟内显示在 Commerce 站点构建器中。</span><span class="sxs-lookup"><span data-stu-id="c5445-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="c5445-113">设置您的成功指标</span><span class="sxs-lookup"><span data-stu-id="c5445-113">Set up your success metrics</span></span>
<span data-ttu-id="c5445-114">每个试验都需要指标来度量变体的影响和验证假设。</span><span class="sxs-lookup"><span data-stu-id="c5445-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="c5445-115">请按照以下步骤使用 Dynamics 365 Commerce 中的实时遥测事件来在第三方服务中启用指标计算。</span><span class="sxs-lookup"><span data-stu-id="c5445-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c5445-116">若要设置成功指标，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c5445-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="c5445-117">在 Commerce 站点构建器中，选择左侧导航窗格中的 **页面**，然后选择要为其收集指标的页面。</span><span class="sxs-lookup"><span data-stu-id="c5445-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="c5445-118">转到您要跟踪的页面或模块的右侧属性窗格中的 **要跟踪的事件 ID** 部分。</span><span class="sxs-lookup"><span data-stu-id="c5445-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="c5445-119">选择 **查看**。</span><span class="sxs-lookup"><span data-stu-id="c5445-119">Select **View**.</span></span> <span data-ttu-id="c5445-120">显示所有事件 ID 的列表。</span><span class="sxs-lookup"><span data-stu-id="c5445-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="c5445-121">复制您要跟踪的事件，然后将事件密钥粘贴到第三方服务中的指定位置。</span><span class="sxs-lookup"><span data-stu-id="c5445-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="c5445-122">如果您需要多个事件，则一次复制一个密钥。</span><span class="sxs-lookup"><span data-stu-id="c5445-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="c5445-123">若要了解如何查看所有可用事件和属性，包括页面视图和收入跟踪，请参阅 [Commerce 组件的诊断和疑难解答事件](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="c5445-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="c5445-124">根据第三方服务的要求，采取任何其他步骤来跟踪指标。</span><span class="sxs-lookup"><span data-stu-id="c5445-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="c5445-125">上一步</span><span class="sxs-lookup"><span data-stu-id="c5445-125">Previous step</span></span>
[<span data-ttu-id="c5445-126">标识假设并确定试验指标</span><span class="sxs-lookup"><span data-stu-id="c5445-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="c5445-127">后续步骤</span><span class="sxs-lookup"><span data-stu-id="c5445-127">Next step</span></span>
[<span data-ttu-id="c5445-128">连接和编辑试验</span><span class="sxs-lookup"><span data-stu-id="c5445-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]