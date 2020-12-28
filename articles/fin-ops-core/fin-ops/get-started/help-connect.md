---
title: 配置 Finance and Operations 应用的帮助体验
description: 此主题介绍某些 Microsoft Dynamics 365 应用的帮助系统组件。 还介绍如何连接这些应用和提供有关自定义帮助创建流程的摘要。
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0495bbc008ed1760b98c2c1ace63fc4a8b1ab5cc
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694413"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="92a23-104">配置 Finance and Operations 应用的帮助体验</span><span class="sxs-lookup"><span data-stu-id="92a23-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92a23-105">在此主题中，将概述 Finance and Operations 应用（如 Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce 和 Dynamics 365 Human Resources）的帮助系统组件。</span><span class="sxs-lookup"><span data-stu-id="92a23-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="92a23-106">此主题还介绍如何连接这些组件和提供有关自定义帮助创建流程的摘要。</span><span class="sxs-lookup"><span data-stu-id="92a23-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="92a23-107">帮助体系结构</span><span class="sxs-lookup"><span data-stu-id="92a23-107">Help architecture</span></span>

<span data-ttu-id="92a23-108">Finance and Operations 应用中包含已发布到 [https://docs.microsoft.com/dynamics365](/dynamics365/) 站点的概念性概述和其他主题。</span><span class="sxs-lookup"><span data-stu-id="92a23-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="92a23-109">然后，可从产品内的 **帮助** 窗格访问此内容。</span><span class="sxs-lookup"><span data-stu-id="92a23-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="92a23-110">下图显示此帮助系统的各个部分。</span><span class="sxs-lookup"><span data-stu-id="92a23-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="92a23-111">[![帮助体系结构](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="92a23-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="92a23-112">产品内帮助系统从 docs.microsoft.com 和其他相连网站提取文章。</span><span class="sxs-lookup"><span data-stu-id="92a23-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="92a23-113">还提取 Microsoft Dynamics Lifecycle Services (LCS) 中的业务流程建模器 (BPM) 内存储的任务指南。</span><span class="sxs-lookup"><span data-stu-id="92a23-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="92a23-114">添加任务指南</span><span class="sxs-lookup"><span data-stu-id="92a23-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="92a23-115">Human Resources 或 Commerce 中现在无 **任务指南** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="92a23-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="92a23-116">但是，Human Resources 中的入门中的任务指南体验可用，以涵盖基本功能。</span><span class="sxs-lookup"><span data-stu-id="92a23-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="92a23-117">[https://docs.microsoft.com/dynamics365](/dynamics365/) 站点中提供 Human Resources 和 Commerce 的过程帮助。</span><span class="sxs-lookup"><span data-stu-id="92a23-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="92a23-118">系统管理员可在 **系统参数** 页中配置对实施的相关任务指南库的访问。</span><span class="sxs-lookup"><span data-stu-id="92a23-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="92a23-119">若要配置帮助，必须通过使用与部署应用的租户相同的租户中的帐户登录。</span><span class="sxs-lookup"><span data-stu-id="92a23-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="92a23-120">不能从本地虚拟硬盘 (VHD) 上正在运行的应用实例访问 LCS 库。</span><span class="sxs-lookup"><span data-stu-id="92a23-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="92a23-121">[![具有帮助设置的系统参数窗体](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="92a23-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="92a23-122">若要配置解决方案的任务指南，请在 **系统参数** 页中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="92a23-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92a23-123">首次打开 **帮助** 选项卡时，必须连接到 Lifecycle Services。</span><span class="sxs-lookup"><span data-stu-id="92a23-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="92a23-124">请确保选择窗体中间的链接，等待连接，关闭对话框，单后选择 **确定** 以转至 **系统参数** 页面。</span><span class="sxs-lookup"><span data-stu-id="92a23-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="92a23-125">[![连接到 LCS](./media/connect-to-lcs-crop-1024x365.png "连接到 LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="92a23-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="92a23-126">选择要连接到的 Lifecycle Services 项目。</span><span class="sxs-lookup"><span data-stu-id="92a23-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="92a23-127">选择要从中检索任务录制的 BPM 库（在所选项目内）。</span><span class="sxs-lookup"><span data-stu-id="92a23-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="92a23-128">选择 BPM 库的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="92a23-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="92a23-129">此显示顺序定义库中的任务录制在 **帮助** 窗格中的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="92a23-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="92a23-130">完成这些步骤后，您可以打开 **帮助** 窗格并选择 **任务指南** 选项卡。您现在将看到适用于您当前在 Finance and Operations 应用中所处页面的任务指南。</span><span class="sxs-lookup"><span data-stu-id="92a23-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="92a23-131">如果未找到任何任务指南，您可以输入关键字来调整搜索。</span><span class="sxs-lookup"><span data-stu-id="92a23-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="92a23-132">显示翻译的任务指南</span><span class="sxs-lookup"><span data-stu-id="92a23-132">Showing translated task guides</span></span>

<span data-ttu-id="92a23-133">翻译的任务指南首次随 2016 年 5 月 APQC 标准库和入门库发布。</span><span class="sxs-lookup"><span data-stu-id="92a23-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="92a23-134">若要查看已本地化的任务指南帮助，请确保您的 Dynamics 365 解决方案已连接到 2016 年 5 月库。</span><span class="sxs-lookup"><span data-stu-id="92a23-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="92a23-135">用户可通过更改 **选项** &gt; **首选项** 下的语言设置，更改用于显示任务指南的语言。</span><span class="sxs-lookup"><span data-stu-id="92a23-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="92a23-136">虽然许多任务指南已被翻译了，但是客户端现在不显示翻译的任务指南名称。</span><span class="sxs-lookup"><span data-stu-id="92a23-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="92a23-137">此外，在 2016 年 5 月库中仅提供在 2016 年 2 月发布的任务指南的翻译。</span><span class="sxs-lookup"><span data-stu-id="92a23-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="92a23-138">Microsoft 将发布包含其它翻译的更新库。</span><span class="sxs-lookup"><span data-stu-id="92a23-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="92a23-139">如果已翻译任务指南，在您打开任务指南时，所有任务指南文本都将显示为您选择的语言。</span><span class="sxs-lookup"><span data-stu-id="92a23-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="92a23-140">如果尚未翻译任务指南，在您打开任务指南时，仅部分文本（控制文本）显示为您选择的语言。</span><span class="sxs-lookup"><span data-stu-id="92a23-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="92a23-141">添加自定义帮助</span><span class="sxs-lookup"><span data-stu-id="92a23-141">Adding custom Help</span></span>

<span data-ttu-id="92a23-142">您可以使用任务指南创建自定义帮助，也可以将自定义帮助网站连接到 **帮助** 窗格。</span><span class="sxs-lookup"><span data-stu-id="92a23-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="92a23-143">使用任务指南创建自定义帮助</span><span class="sxs-lookup"><span data-stu-id="92a23-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="92a23-144">您可以通过创建反映您的实施的任务录制并将其保存到 LCS 中的业务流程库，为支持的应用创建自定义帮助。</span><span class="sxs-lookup"><span data-stu-id="92a23-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="92a23-145">您无法为 Human Resources 创建自定义任务指南。</span><span class="sxs-lookup"><span data-stu-id="92a23-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="92a23-146">如果您是合作伙伴，并且您要将一个库提升到公司库并将其包括到解决方案中，它将可供您的客户使用。</span><span class="sxs-lookup"><span data-stu-id="92a23-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="92a23-147">您还可以复制 APQC Unified 库，然后打开副本中的任务录制，进行编辑，再保存所做更改。</span><span class="sxs-lookup"><span data-stu-id="92a23-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="92a23-148">有关详细信息，请参阅[任务录制器资源](../../dev-itpro/user-interface/task-recorder.md)。</span><span class="sxs-lookup"><span data-stu-id="92a23-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="92a23-149">连接自定义帮助站点</span><span class="sxs-lookup"><span data-stu-id="92a23-149">Connect a custom Help site</span></span>

<span data-ttu-id="92a23-150">Finance and Operations 应用很少以现成格式使用。</span><span class="sxs-lookup"><span data-stu-id="92a23-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="92a23-151">相反，将自定义并扩展此解决方案以满足组织的需要。</span><span class="sxs-lookup"><span data-stu-id="92a23-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="92a23-152">还可以自定义和扩展帮助体验。</span><span class="sxs-lookup"><span data-stu-id="92a23-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="92a23-153">例如，可以向产品内 **帮助** 窗格添加自定义帮助。</span><span class="sxs-lookup"><span data-stu-id="92a23-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="92a23-154">Microsoft 提供了工具提示，以帮助您开发自定义帮助和将其连接到 **帮助** 窗格。</span><span class="sxs-lookup"><span data-stu-id="92a23-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="92a23-155">有关如何设置连接到 **帮助** 窗格的自定义帮助解决方案的信息，请参阅[自定义帮助概述](../../dev-itpro/help/custom-help-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="92a23-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="92a23-156">如果要与 Microsoft 合作处理用于自定义帮助的工具和流程，请填写 [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback) 中的表单。</span><span class="sxs-lookup"><span data-stu-id="92a23-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="92a23-157">请参阅</span><span class="sxs-lookup"><span data-stu-id="92a23-157">See also</span></span>

[<span data-ttu-id="92a23-158">帮助系统</span><span class="sxs-lookup"><span data-stu-id="92a23-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="92a23-159">自定义帮助概述</span><span class="sxs-lookup"><span data-stu-id="92a23-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="92a23-160">任务录制器资源</span><span class="sxs-lookup"><span data-stu-id="92a23-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="92a23-161">通过任务录制器创建文档或培训</span><span class="sxs-lookup"><span data-stu-id="92a23-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="92a23-162">自定义帮助 GitHub 知识库</span><span class="sxs-lookup"><span data-stu-id="92a23-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  
