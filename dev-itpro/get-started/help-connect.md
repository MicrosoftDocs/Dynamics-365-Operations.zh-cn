---
title: "连接帮助系统"
description: "此主题介绍 Microsoft Dynamics 365 for Finance and Operations 帮助系统的组件，并且提供如何连接它们的概览以及如何创建自定义帮助的摘要。"
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="865ef-103">连接帮助系统</span><span class="sxs-lookup"><span data-stu-id="865ef-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="865ef-104">此主题介绍 Microsoft Dynamics 365 for Finance and Operations 帮助系统的组件。</span><span class="sxs-lookup"><span data-stu-id="865ef-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="865ef-105">它提供如何连接这些组件的概览和如何创建自定义帮助的摘要。</span><span class="sxs-lookup"><span data-stu-id="865ef-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="865ef-106">帮助体系结构</span><span class="sxs-lookup"><span data-stu-id="865ef-106">Help architecture</span></span>
<span data-ttu-id="865ef-107">下图显示 Finance and Operations 帮助系统的各个部分。</span><span class="sxs-lookup"><span data-stu-id="865ef-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="865ef-108">产品内帮助系统从 Finance and Operations 站点 https://docs.microsoft.com 拉取文章，以及 Lifecycle Services (LCS) 中的业务流程建模器中存储的任务指南。</span><span class="sxs-lookup"><span data-stu-id="865ef-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="865ef-109">图形中列出的带有星号 (\*) 的功能已计划，但还不可用。</span><span class="sxs-lookup"><span data-stu-id="865ef-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="865ef-110">[![帮助体系结构](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="865ef-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="865ef-111">连接帮助系统</span><span class="sxs-lookup"><span data-stu-id="865ef-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="865ef-112">**任务指南**选项卡目前在 Microsoft Dynamics 365 for Talent 和 Microsoft Dynamics 365 for Retail 中不可用。</span><span class="sxs-lookup"><span data-stu-id="865ef-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="865ef-113">我们目前正在努力在将来的版本中启用此功能。</span><span class="sxs-lookup"><span data-stu-id="865ef-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="865ef-114">Talent 中的入门中的任务指南体验可用，以涵盖基本功能。</span><span class="sxs-lookup"><span data-stu-id="865ef-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="865ef-115">docs.microsoft.com 站点 ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) 上还提供用于 Retail 和 Talent 的过程帮助。</span><span class="sxs-lookup"><span data-stu-id="865ef-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="865ef-116">使用**系统参数**页，系统管理员连接有关实施的部分帮助系统。</span><span class="sxs-lookup"><span data-stu-id="865ef-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="865ef-117">[![具有帮助设置的系统参数窗体](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) 在**系统参数**页上，执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="865ef-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="865ef-118">首次打开**帮助**选项卡时，必须连接到 Lifecycle Services。</span><span class="sxs-lookup"><span data-stu-id="865ef-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="865ef-119">请确保单击窗体中间的链接，等待连接，关闭对话框，然后单击**确定**以转至**系统参数**页。[![连接到 LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="865ef-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="865ef-120">选择要连接到的 Lifecycle Services 项目。</span><span class="sxs-lookup"><span data-stu-id="865ef-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="865ef-121">选择要从中检索任务录制的 BPM 库（在所选项目内）。</span><span class="sxs-lookup"><span data-stu-id="865ef-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="865ef-122">对于 Finance and Operations 的 Microsoft 内容，选择 Microsoft Dynamics 365 for Finance and Operations 的 2017 年 2 月 QPC 标准库。</span><span class="sxs-lookup"><span data-stu-id="865ef-122">For Finance and Operations, for Microsoft content, select the February 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations.</span></span> 
    - <span data-ttu-id="865ef-123">对于 Retail，我们将在 7 月份发布一个库。</span><span class="sxs-lookup"><span data-stu-id="865ef-123">For Retail, we will be releasing a library in July.</span></span> 
    - <span data-ttu-id="865ef-124">您无需为 Talent 选择库，因为已经为您建立了与正确库的连接。</span><span class="sxs-lookup"><span data-stu-id="865ef-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="865ef-125">选择 BPM 库的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="865ef-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="865ef-126">它决定库中的任务录制在**“帮助”**窗格中的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="865ef-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="865ef-127">在您完成这些步骤后，您可以打开**“帮助”**窗格并单击**“任务指南”**选项卡。</span><span class="sxs-lookup"><span data-stu-id="865ef-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab.</span></span> <span data-ttu-id="865ef-128">您现在将看到应用于您当前在 Finance and Operations 中所处页面的任务指南。</span><span class="sxs-lookup"><span data-stu-id="865ef-128">You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="865ef-129">如果未找到任何任务指南，您可以输入关键字来调整搜索。</span><span class="sxs-lookup"><span data-stu-id="865ef-129">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="865ef-130">显示翻译的任务指南</span><span class="sxs-lookup"><span data-stu-id="865ef-130">Showing translated task guides</span></span>

<span data-ttu-id="865ef-131">翻译的任务指南首次随 2016 年 5 月 APQC 标准库和入门库提供。</span><span class="sxs-lookup"><span data-stu-id="865ef-131">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="865ef-132">在 Finance and Operations 中，若要查看本地化的任务指南帮助，请确保您已连接到五月库。</span><span class="sxs-lookup"><span data-stu-id="865ef-132">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="865ef-133">每个用户的任务指南的显示语言由**选项** &gt; **首选项**下的语言”设置控制。</span><span class="sxs-lookup"><span data-stu-id="865ef-133">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="865ef-134">虽然许多任务指南已被翻译了，但现在，Finance and Operations 客户端不显示翻译的任务指南名称。</span><span class="sxs-lookup"><span data-stu-id="865ef-134">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="865ef-135">此外，五月库中仅提供在 2016 年 2 月发布的任务指南的翻译。</span><span class="sxs-lookup"><span data-stu-id="865ef-135">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="865ef-136">我们将发布包含其它翻译的更新库。</span><span class="sxs-lookup"><span data-stu-id="865ef-136">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="865ef-137">如果已翻译任务指南，在您打开任务指南时，所有任务指南文本都将显示为您选择的语言。</span><span class="sxs-lookup"><span data-stu-id="865ef-137">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="865ef-138">如果尚未翻译任务指南，在您打开任务指南时，仅部分文本（控制文本）显示为您选择的语言。</span><span class="sxs-lookup"><span data-stu-id="865ef-138">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="865ef-139">创建客户帮助</span><span class="sxs-lookup"><span data-stu-id="865ef-139">Creating custom help</span></span>
<span data-ttu-id="865ef-140">您可以通过创建反映您的实施的任务录制并将其保存到 LCS 业务流程库中，为 Finance and Operations 和 Retail 创建自定义帮助。</span><span class="sxs-lookup"><span data-stu-id="865ef-140">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="865ef-141">您无法为 Talent 创建自定义任务指南。</span><span class="sxs-lookup"><span data-stu-id="865ef-141">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="865ef-142">对于合作伙伴，如果您要将一个库提升到公司库并将其包括到解决方案中，它将可供您的客户使用。</span><span class="sxs-lookup"><span data-stu-id="865ef-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="865ef-143">您还可以复制 APQC Unified 全局库，然后打开您的副本，从它打开任务录制，然后修改它们，并保存具有所做更改的录制。</span><span class="sxs-lookup"><span data-stu-id="865ef-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="865ef-144">有关详细信息，请参阅[如何创建任务录制以用作文档或培训](../user-interface/task-recorder.md)。</span><span class="sxs-lookup"><span data-stu-id="865ef-144">For more information, see [How to create a task recording to use as documentation or training](../user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="865ef-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="865ef-145">See also</span></span>
--------

[<span data-ttu-id="865ef-146">帮助概览</span><span class="sxs-lookup"><span data-stu-id="865ef-146">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="865ef-147">任务录制器概览</span><span class="sxs-lookup"><span data-stu-id="865ef-147">Task recorder overview</span></span>](../user-interface/task-recorder.md)

[<span data-ttu-id="865ef-148">如何创建任务录制以用作文档或培训</span><span class="sxs-lookup"><span data-stu-id="865ef-148">How to create a task recording to use as documentation or training</span></span>](../user-interface/task-recorder-training-docs.md)





