---
title: 连接帮助系统
description: 此主题介绍 Finance and Operations 应用程序的“帮助”系统的组件，并且提供如何连接它们的概览以及如何创建自定义帮助的摘要。
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2955464aa8a220563db1b9ebbb348be52f520659
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812572"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="0f8c3-103">连接帮助系统</span><span class="sxs-lookup"><span data-stu-id="0f8c3-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f8c3-104">此主题介绍 Finance and Operations 应用程序（如 Dynamics 365 Finance、Supply Chain Management、Retail 和 Talent）的帮助系统组件。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Retail, and Talent.</span></span> <span data-ttu-id="0f8c3-105">它提供如何连接这些组件的概览和如何创建自定义帮助的摘要。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="0f8c3-106">帮助体系结构</span><span class="sxs-lookup"><span data-stu-id="0f8c3-106">Help architecture</span></span>

<span data-ttu-id="0f8c3-107">下图显示此帮助系统的各个部分。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="0f8c3-108">产品内帮助系统从  https://docs.microsoft.com 拉取文章，以及 Lifecycle Services (LCS) 中的业务流程建模器中存储的任务指南。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="0f8c3-109">图形中列出的带有星号 (\*) 的功能已计划，但还不可用。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="0f8c3-110">[![帮助体系结构](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="0f8c3-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="0f8c3-111">连接帮助系统</span><span class="sxs-lookup"><span data-stu-id="0f8c3-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="0f8c3-112">**任务指南**选项卡目前在 Dynamics 365 Talent 或 Retail 中不可用。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-112">The **Task guides** tab is currently not available in Dynamics 365 Talent or Retail.</span></span> <span data-ttu-id="0f8c3-113">我们目前正在努力在将来的版本中启用此功能。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="0f8c3-114">Talent 中的入门中的任务指南体验可用，以涵盖基本功能。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="0f8c3-115">docs.microsoft.com 网站中也提供了 Retail 和 Talent 的过程帮助。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-115">Procedural help is also available on the docs.microsoft.com site for both Retail and Talent.</span></span>

<span data-ttu-id="0f8c3-116">使用**系统参数**页，系统管理员连接有关实施的部分帮助系统。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="0f8c3-117">[![具有帮助设置的系统参数窗体](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="0f8c3-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="0f8c3-118">在**系统参数**页上，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0f8c3-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f8c3-119">首次打开**帮助**选项卡时，必须连接到 Lifecycle Services。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="0f8c3-120">请确保单击窗体中间的链接，等待连接，关闭对话框，单后单击**确定**以转至**系统参数**页面。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="0f8c3-121">[![连接到 LCS](./media/connect-to-lcs-crop-1024x365.png "连接到 LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="0f8c3-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="0f8c3-122">选择要连接到的 Lifecycle Services 项目。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="0f8c3-123">选择要从中检索任务录制的 BPM 库（在所选项目内）。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="0f8c3-124">选择 BPM 库的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="0f8c3-125">它决定库中的任务录制在**帮助**窗格中的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="0f8c3-126">完成这些步骤后，您可以打开**帮助**窗格并单击**任务指南**选项卡。您现在将看到适用于您当前在 Finance and Operations 应用程序中所处页面的任务指南。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="0f8c3-127">如果未找到任何任务指南，您可以输入关键字来调整搜索。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="0f8c3-128">显示翻译的任务指南</span><span class="sxs-lookup"><span data-stu-id="0f8c3-128">Showing translated task guides</span></span>

<span data-ttu-id="0f8c3-129">翻译的任务指南首次随 2016 年 5 月 APQC 标准库和入门库提供。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="0f8c3-130">在 Finance and Operations 应用程序中，若要查看本地化的任务指南帮助，请确保您已连接到五月库。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="0f8c3-131">每个用户的任务指南的显示语言由**选项** &gt; **首选项**下的语言”设置控制。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="0f8c3-132">虽然许多任务指南已被翻译了，但现在，客户端不显示翻译的任务指南名称。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="0f8c3-133">此外，五月库中仅提供在 2016 年 2 月发布的任务指南的翻译。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="0f8c3-134">我们将发布包含其它翻译的更新库。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="0f8c3-135">如果已翻译任务指南，在您打开任务指南时，所有任务指南文本都将显示为您选择的语言。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="0f8c3-136">如果尚未翻译任务指南，在您打开任务指南时，仅部分文本（控制文本）显示为您选择的语言。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="0f8c3-137">创建客户帮助</span><span class="sxs-lookup"><span data-stu-id="0f8c3-137">Creating custom help</span></span>

<span data-ttu-id="0f8c3-138">您可以使用任务指南创建自定义帮助，或者将网站连接到帮助窗格。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="0f8c3-139">使用任务指南创建定制帮助</span><span class="sxs-lookup"><span data-stu-id="0f8c3-139">Create custom help with task guides</span></span>

<span data-ttu-id="0f8c3-140">您可以通过创建反映您的实施的任务录制并将其保存到 LCS 业务流程库中，为 Finance、Supply Chain Management 和 Retail 创建自定义帮助。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-140">You can create custom help for Finance, Supply Chain Management, and Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="0f8c3-141">您无法为 Talent 创建自定义任务指南。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-141">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="0f8c3-142">对于合作伙伴，如果您要将一个库提升到公司库并将其包括到解决方案中，它将可供您的客户使用。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="0f8c3-143">您还可以复制 APQC Unified 全局库，然后打开您的副本，从它打开任务录制，然后修改它们，并保存具有所做更改的录制。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="0f8c3-144">有关详细信息，请参阅[任务录制器资源](../../dev-itpro/user-interface/task-recorder.md)。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="0f8c3-145">连接自定义站点</span><span class="sxs-lookup"><span data-stu-id="0f8c3-145">Connect a custom site</span></span>

<span data-ttu-id="0f8c3-146">Microsoft 提供了介绍如何创建自定义帮助站点并将其连接到帮助窗格的白皮书和示例代码。</span><span class="sxs-lookup"><span data-stu-id="0f8c3-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="0f8c3-147">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="0f8c3-147">For more information, see:</span></span>

- [<span data-ttu-id="0f8c3-148">为 Finance and Operations 应用程序创建自定义帮助（白皮书）</span><span class="sxs-lookup"><span data-stu-id="0f8c3-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="0f8c3-149">自定义帮助 GitHub 知识库</span><span class="sxs-lookup"><span data-stu-id="0f8c3-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="0f8c3-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="0f8c3-150">Additional resources</span></span>

[<span data-ttu-id="0f8c3-151">帮助系统</span><span class="sxs-lookup"><span data-stu-id="0f8c3-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="0f8c3-152">任务录制器资源</span><span class="sxs-lookup"><span data-stu-id="0f8c3-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="0f8c3-153">通过任务录制器创建文档或培训</span><span class="sxs-lookup"><span data-stu-id="0f8c3-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
