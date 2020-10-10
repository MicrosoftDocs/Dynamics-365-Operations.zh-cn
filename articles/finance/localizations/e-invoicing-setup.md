---
title: 设置电子开票附加产品
description: 本主题说明如何在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中设置电子开票附加产品。
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 92ffd2076497325fb986478328c4b2584929881d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835912"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a><span data-ttu-id="c775c-103">设置电子开票附加产品</span><span class="sxs-lookup"><span data-stu-id="c775c-103">Set up the Electronic invoicing add-on</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c775c-104">电子开票附加产品功能设置是通过 Regulatory Configuration Services (RCS) 环境创建所需配置并将该配置发布到电子开票附加产品服务器的过程。</span><span class="sxs-lookup"><span data-stu-id="c775c-104">Electronic invoicing add-on feature setup is the process of creating the required configuration through the Regulatory Configuration Services (RCS) environment and publishing that configuration to the Electronic invoicing add-on server.</span></span> <span data-ttu-id="c775c-105">此设置使您可以创建可配置规则，以使电子开票附加产品可以通过 Internet 使用安全协议来通过 Web 服务与第三方实体进行通信和交换数据。</span><span class="sxs-lookup"><span data-stu-id="c775c-105">The setup lets you create the configurable rules that enable the Electronic invoicing add-on to use a secure protocol over the internet to communicate and exchange data with a third-party entity through web services.</span></span>

<span data-ttu-id="c775c-106">可配置性依赖电子报告 (ER) 格式配置作为构建通过数字文件发送和接收的内容的方法。</span><span class="sxs-lookup"><span data-stu-id="c775c-106">The configurability relies on the Electronic reporting (ER) format configuration as a means to build content that is sent and received through digital files.</span></span> <span data-ttu-id="c775c-107">它还依赖于通信操作的流程来向第三方 Web 服务发送请求并接收来自这些服务的响应，您无需编写代码。</span><span class="sxs-lookup"><span data-stu-id="c775c-107">It also relies on the orchestration of communication actions to send requests to and receive responses from third-party web services without requiring that you write code.</span></span>

## <a name="overview"></a><span data-ttu-id="c775c-108">概览</span><span class="sxs-lookup"><span data-stu-id="c775c-108">Overview</span></span>

<span data-ttu-id="c775c-109">“电子开票附加产品功能”是配置和发布以使用电子开票附加产品服务器的资源的通用名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-109">"The Electronic invoicing add-on feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="c775c-110">功能设置将使用 ER 配置格式来创建可配置的导出和导入文件，与使用操作和操作流来支持创建可配置规则以发送请求、导入响应和分析响应内容，以及另外一些设置相结合。</span><span class="sxs-lookup"><span data-stu-id="c775c-110">The feature setup combines, among other things, the use of ER configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

<span data-ttu-id="c775c-111">下图显示了电子开票附加产品功能的主要组件。</span><span class="sxs-lookup"><span data-stu-id="c775c-111">The following illustration shows the main components of an Electronic invoicing add-on feature.</span></span>

![电子开票附加产品功能概述](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

<span data-ttu-id="c775c-113">由于发票格式和操作流的变化，功能设置可能会因国家或地区或业务要求而异。</span><span class="sxs-lookup"><span data-stu-id="c775c-113">Because of variations in invoice formats and action flows, the feature setup might vary according to country or region, or according to business requirements.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a><span data-ttu-id="c775c-114">设置电子开票附加产品功能</span><span class="sxs-lookup"><span data-stu-id="c775c-114">Set up the Electronic invoicing add-on feature</span></span>

<span data-ttu-id="c775c-115">设置过程必须在您的 RCS 环境中完成。</span><span class="sxs-lookup"><span data-stu-id="c775c-115">The setup process must be completed in your RCS environment.</span></span> <span data-ttu-id="c775c-116">请按照以下步骤创建新的电子开票附加产品功能。</span><span class="sxs-lookup"><span data-stu-id="c775c-116">Follow these steps to create a new Electronic invoicing add-on feature.</span></span>

1. <span data-ttu-id="c775c-117">登录您的 RCS 环境。</span><span class="sxs-lookup"><span data-stu-id="c775c-117">Sign in to your RCS environment.</span></span>
2. <span data-ttu-id="c775c-118">在**全球化功能**工作区的**功能**部分，选择**电子开票附加产品**磁贴。</span><span class="sxs-lookup"><span data-stu-id="c775c-118">In the **Globalization features** workspace, in the **Features** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="c775c-119">在**电子开票附加产品功能**页上，选择**导入**从全局存储库导入 ER 数据模型配置。</span><span class="sxs-lookup"><span data-stu-id="c775c-119">On the **Electronic invoicing add-on features** page, select **Import** to import the ER data model configuration from the Global repository.</span></span>
4. <span data-ttu-id="c775c-120">选择**添加**创建电子开票附加产品功能。</span><span class="sxs-lookup"><span data-stu-id="c775c-120">Select **Add** to create an Electronic invoicing add-on feature.</span></span> <span data-ttu-id="c775c-121">您可以从头创建此功能，也可以从现有的电子开票附加产品功能派生。</span><span class="sxs-lookup"><span data-stu-id="c775c-121">You can either create the feature from the scratch or derive it from an existing Electronic invoicing add-on feature.</span></span>

    ![添加电子开票附加产品功能](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> <span data-ttu-id="c775c-123">创建新的电子开票附加产品功能时，它具有版本号，默认状态将设置为**草稿**。</span><span class="sxs-lookup"><span data-stu-id="c775c-123">When you create a new Electronic invoicing add-on feature, it has a version number, and its default status is set to **Draft**.</span></span>

### <a name="configurations"></a><span data-ttu-id="c775c-124">配置</span><span class="sxs-lookup"><span data-stu-id="c775c-124">Configurations</span></span>

<span data-ttu-id="c775c-125">配置保留转换和创建在与第三方 Web 服务通信期间将交换的文件所需的 ER 格式配置。</span><span class="sxs-lookup"><span data-stu-id="c775c-125">Configurations hold the ER format configurations that are required for transformations and to create the files that will be exchanged during the communication with third-party web services.</span></span> <span data-ttu-id="c775c-126">基于 Web 服务提供商提供的集成技术规范，电子开票附加产品功能可以具有所需的任意数量的 ER 文件格式配置。</span><span class="sxs-lookup"><span data-stu-id="c775c-126">An Electronic invoicing add-on feature can have as many ER file format configurations as are required, based on the integration technical specification that is provided by the web service provider.</span></span>

<span data-ttu-id="c775c-127">请按照以下步骤将 ER 格式添加到电子开票附加产品功能。</span><span class="sxs-lookup"><span data-stu-id="c775c-127">Follow these steps to add ER formats to the Electronic invoicing add-on feature.</span></span>

1. <span data-ttu-id="c775c-128">在**电子开票附加产品功能**页上的**配置**选项卡上，选择**添加**为电子开票附加产品功能添加 ER 文件格式配置。</span><span class="sxs-lookup"><span data-stu-id="c775c-128">On the **Electronic invoicing add-on features** page, on the **Configurations** tab, select **Add** to add ER file format configurations for the Electronic invoicing add-on feature.</span></span>

    ![添加电子开票附加产品功能配置](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > <span data-ttu-id="c775c-130">从头创建电子开票附加产品功能时，必须手动添加所有 ER 文件格式配置。</span><span class="sxs-lookup"><span data-stu-id="c775c-130">When you create an Electronic invoicing add-on feature from scratch, you must manually add all the ER file format configurations.</span></span> <span data-ttu-id="c775c-131">从现有功能派生电子开票附加产品功能时，将自动创建 ER 文件格式配置，因为它们是从原始电子开票附加产品功能继承而来的。</span><span class="sxs-lookup"><span data-stu-id="c775c-131">When you derive an Electronic invoicing add-on feature from an existing feature, the ER file format configurations are automatically created, because they are inherited from the original Electronic invoicing add-on feature.</span></span>

2. <span data-ttu-id="c775c-132">选择**编辑**打开**格式设计器**页，您可以在其中编辑 ER 文件格式配置。</span><span class="sxs-lookup"><span data-stu-id="c775c-132">Select **Edit** to open the **Format designer** page, where you can edit the ER file format configuration.</span></span>

    ![编辑电子开票附加产品功能配置](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > <span data-ttu-id="c775c-134">在编辑格式时，配置版本的状态将设置为**草稿**。</span><span class="sxs-lookup"><span data-stu-id="c775c-134">While you're editing the format, the status of the configuration version is set to **Draft**.</span></span>

3. <span data-ttu-id="c775c-135">使用**格式设计器**页更改文件格式配置。</span><span class="sxs-lookup"><span data-stu-id="c775c-135">Use the **Format designer** page to change the file format configuration.</span></span> <span data-ttu-id="c775c-136">有关详细信息，请参阅[创建电子单据配置](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration)。</span><span class="sxs-lookup"><span data-stu-id="c775c-136">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![“格式设计器”页面](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a><span data-ttu-id="c775c-138">功能设置</span><span class="sxs-lookup"><span data-stu-id="c775c-138">Feature setups</span></span>

<span data-ttu-id="c775c-139">功能设置封装第三方 Web 服务的通信和安全性规则。</span><span class="sxs-lookup"><span data-stu-id="c775c-139">Feature setups encapsulate the rules for communication and security with a third-party web service.</span></span> <span data-ttu-id="c775c-140">根据您要完成的业务规则，电子开票附加产品功能可以具有所需的任意数量的功能设置。</span><span class="sxs-lookup"><span data-stu-id="c775c-140">An Electronic invoicing add-on feature can have as many feature setups as are required, based on the business rule that you want to accomplish.</span></span>

<span data-ttu-id="c775c-141">请按照以下步骤将功能设置添加到电子开票附加产品功能。</span><span class="sxs-lookup"><span data-stu-id="c775c-141">Follow these steps to add feature setups to the Electronic invoicing add-on feature.</span></span>

1. <span data-ttu-id="c775c-142">在**电子开票附加产品功能**页上的**设置**选项卡上，选择**添加**向电子开票附加产品功能添加功能设置。</span><span class="sxs-lookup"><span data-stu-id="c775c-142">On the **Electronic invoicing add-on features** page, on the **Setups** tab, select **Add** to add feature setups to the Electronic invoicing add-on feature.</span></span>

    ![添加电子开票附加产品功能设置](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > <span data-ttu-id="c775c-144">从头创建电子开票附加产品功能时，必须手动添加所需的所有功能设置。</span><span class="sxs-lookup"><span data-stu-id="c775c-144">When you create an Electronic invoicing add-on feature from scratch, you must manually add all the feature setups that you require.</span></span> <span data-ttu-id="c775c-145">从现有功能派生电子开票附加产品功能时，将自动创建所有功能设置，因为它们是从原始电子开票附加产品功能继承而来的。</span><span class="sxs-lookup"><span data-stu-id="c775c-145">When you derive an Electronic invoicing add-on feature from an existing feature, all feature setups are automatically created, because they are inherited from the original Electronic invoicing add-on feature.</span></span>

2. <span data-ttu-id="c775c-146">选择**编辑**编辑功能版本设置。</span><span class="sxs-lookup"><span data-stu-id="c775c-146">Select **Edit** to edit the feature version setup.</span></span>

    ![编辑电子开票附加产品功能设置](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. <span data-ttu-id="c775c-148">使用**功能版本设置**页配置操作、适用性规则和变量。</span><span class="sxs-lookup"><span data-stu-id="c775c-148">Use the **Feature version setup** page to configure actions, applicability rules, and variables.</span></span>

    ![操作、适用性规则和变量](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a><span data-ttu-id="c775c-150">行动</span><span class="sxs-lookup"><span data-stu-id="c775c-150">Actions</span></span>

<span data-ttu-id="c775c-151">操作是按顺序运行的预定义操作列表。</span><span class="sxs-lookup"><span data-stu-id="c775c-151">Actions are a predefined list of operations that are run in sequential order.</span></span> <span data-ttu-id="c775c-152">此列表代表完整执行电子开票附加产品功能所需的步骤的分解。</span><span class="sxs-lookup"><span data-stu-id="c775c-152">This list represents the breakdown of the steps that are required for full execution of the Electronic invoicing add-on feature.</span></span> <span data-ttu-id="c775c-153">操作可以在同一个电子开票附加产品功能中封装双向通信：发送目标请求、接收响应和分析内容。</span><span class="sxs-lookup"><span data-stu-id="c775c-153">The actions can encapsulate, in the same Electronic invoicing add-on feature, communication in both directions: sending a request for a destination, and receiving a response and parsing its contents.</span></span>

<span data-ttu-id="c775c-154">每个操作包含一个预定义的参数列表，这些参数是操作完成目的所必需的。</span><span class="sxs-lookup"><span data-stu-id="c775c-154">Each action contains a predefined list of parameters that are required for the action to accomplish its purpose.</span></span> <span data-ttu-id="c775c-155">可以选择提供其他参数。</span><span class="sxs-lookup"><span data-stu-id="c775c-155">Additional parameters might optionally be provided.</span></span>

#### <a name="actions-fasttab"></a><span data-ttu-id="c775c-156">“操作”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="c775c-156">Actions FastTab</span></span>

<span data-ttu-id="c775c-157">在**功能版本设置**页上的**操作**选项卡上，在**操作**快速选项卡上，按照以下其中一个步骤或全部两个步骤来管理操作：</span><span class="sxs-lookup"><span data-stu-id="c775c-157">On the **Feature versions setup** page, on the **Actions** tab, on the **Actions** FastTab, follow one or both of these steps to manage actions:</span></span>

- <span data-ttu-id="c775c-158">选择**新建**或**删除**添加新操作或删除现有操作。</span><span class="sxs-lookup"><span data-stu-id="c775c-158">Select **New** or **Delete** to add new actions or delete existing actions.</span></span>
- <span data-ttu-id="c775c-159">选择**向上**或**向下**在网格中向上或向下移动选定的动作，从而更改它们的运行顺序。</span><span class="sxs-lookup"><span data-stu-id="c775c-159">Select **Up** or **Down** to move selected actions up or down in the grid and therefore change the order that they are run in.</span></span> <span data-ttu-id="c775c-160">操作从上到下按照它们在网格中出现的顺序运行。</span><span class="sxs-lookup"><span data-stu-id="c775c-160">Actions are run in the order in which they appear in the grid, from top to bottom.</span></span>

![管理操作](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

<span data-ttu-id="c775c-162">下表说明了**操作**快速选项卡上可用的字段。</span><span class="sxs-lookup"><span data-stu-id="c775c-162">The following table describes the fields that are available on the **Actions** FastTab.</span></span>

| <span data-ttu-id="c775c-163">字段</span><span class="sxs-lookup"><span data-stu-id="c775c-163">Field</span></span>        | <span data-ttu-id="c775c-164">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-164">Description</span></span> |
|--------------|-------------|
| <span data-ttu-id="c775c-165">行动</span><span class="sxs-lookup"><span data-stu-id="c775c-165">Action</span></span>       | <span data-ttu-id="c775c-166">有八个预定义操作：</span><span class="sxs-lookup"><span data-stu-id="c775c-166">There are eight predefined actions:</span></span><ul><li><span data-ttu-id="c775c-167"><strong>对文档签名</strong></span><span class="sxs-lookup"><span data-stu-id="c775c-167"><strong>Sign document</strong></span></span></li><li><span data-ttu-id="c775c-168"><strong>FileStoreActionName</strong></span><span class="sxs-lookup"><span data-stu-id="c775c-168"><strong>FileStoreActionName</strong></span></span></li><li><span data-ttu-id="c775c-169"><strong>转换文档</strong></span><span class="sxs-lookup"><span data-stu-id="c775c-169"><strong>Transform document</strong></span></span></li><li><span data-ttu-id="c775c-170"><strong>处理响应</strong></span><span class="sxs-lookup"><span data-stu-id="c775c-170"><strong>Process response</strong></span></span></li><li><span data-ttu-id="c775c-171"><strong>调用 REST Web 服务</strong></span><span class="sxs-lookup"><span data-stu-id="c775c-171"><strong>Call REST web service</strong></span></span></li><li><span data-ttu-id="c775c-172"><strong>调用墨西哥 PAC 服务</strong></span><span class="sxs-lookup"><span data-stu-id="c775c-172"><strong>Call Mexican PAC service</strong></span></span></li><li><span data-ttu-id="c775c-173"><strong>调用巴西 SEFAZ 服务</strong></span><span class="sxs-lookup"><span data-stu-id="c775c-173"><strong>Call Brazilian SEFAZ service</strong></span></span></li><li><span data-ttu-id="c775c-174"><strong>调用意大利 SDI 服务</strong></span><span class="sxs-lookup"><span data-stu-id="c775c-174"><strong>Call Italian SDI service</strong></span></span></li></ul> |
| <span data-ttu-id="c775c-175">操作名称</span><span class="sxs-lookup"><span data-stu-id="c775c-175">Action name</span></span>  | <span data-ttu-id="c775c-176">操作的名称及其执行顺序。</span><span class="sxs-lookup"><span data-stu-id="c775c-176">The name of the action and its execution order.</span></span> |
| <span data-ttu-id="c775c-177">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-177">Description</span></span>  | <span data-ttu-id="c775c-178">操作的说明。</span><span class="sxs-lookup"><span data-stu-id="c775c-178">A description of the action.</span></span> |
| <span data-ttu-id="c775c-179">启用重试</span><span class="sxs-lookup"><span data-stu-id="c775c-179">Enable retry</span></span> | <span data-ttu-id="c775c-180">选中复选框表示如果上一次尝试失败，可以重试该操作。</span><span class="sxs-lookup"><span data-stu-id="c775c-180">A selected check box indicates that the action can be retried if the previous attempt is unsuccessful.</span></span> |
| <span data-ttu-id="c775c-181">重试操作</span><span class="sxs-lookup"><span data-stu-id="c775c-181">Retry action</span></span> | <span data-ttu-id="c775c-182">重试时，从其开始重试的操作。</span><span class="sxs-lookup"><span data-stu-id="c775c-182">In the event of a retry, the action that the retry is started from.</span></span> <span data-ttu-id="c775c-183">然后重试于当前操作（包括重试）结束。</span><span class="sxs-lookup"><span data-stu-id="c775c-183">The retry then ends on the current action (inclusive retry).</span></span> <span data-ttu-id="c775c-184">对于有重试的操作，**最小退避**和**最大退避**参数指定最小重试次数和最大重试次数。</span><span class="sxs-lookup"><span data-stu-id="c775c-184">For actions that have them, the **Minimum back off** and **Maximum back off** parameters specify the minimum number and maximum number of retries.</span></span> |

#### <a name="parameters-fasttab"></a><span data-ttu-id="c775c-185">“参数”快速选项卡</span><span class="sxs-lookup"><span data-stu-id="c775c-185">Parameters FastTab</span></span>

<span data-ttu-id="c775c-186">**参数**快速选项卡列出在**操作**快速选项卡上选择的操作的参数。</span><span class="sxs-lookup"><span data-stu-id="c775c-186">The **Parameters** FastTab lists the parameters for the action that is selected on the **Actions** FastTab.</span></span>

![“参数”快速选项卡](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

<span data-ttu-id="c775c-188">下表说明了**参数**快速选项卡上可用的字段。</span><span class="sxs-lookup"><span data-stu-id="c775c-188">The following table describes the fields that are available on the **Parameters** FastTab.</span></span>

| <span data-ttu-id="c775c-189">字段</span><span class="sxs-lookup"><span data-stu-id="c775c-189">Field</span></span>       | <span data-ttu-id="c775c-190">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-190">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="c775c-191">姓名</span><span class="sxs-lookup"><span data-stu-id="c775c-191">Name</span></span>        | <span data-ttu-id="c775c-192">预定义的参数列表。</span><span class="sxs-lookup"><span data-stu-id="c775c-192">A predefined list of parameters.</span></span> <span data-ttu-id="c775c-193">有关详细信息，请参阅[按操作排列的参数列表](#list-of-parameters-by-action)一节。</span><span class="sxs-lookup"><span data-stu-id="c775c-193">For more information, see the [List of parameters by action](#list-of-parameters-by-action) section.</span></span> |
| <span data-ttu-id="c775c-194">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-194">Description</span></span> | <span data-ttu-id="c775c-195">参数的说明。</span><span class="sxs-lookup"><span data-stu-id="c775c-195">A description of the parameter.</span></span> |
| <span data-ttu-id="c775c-196">值</span><span class="sxs-lookup"><span data-stu-id="c775c-196">Value</span></span>       | <span data-ttu-id="c775c-197">参数的值。</span><span class="sxs-lookup"><span data-stu-id="c775c-197">The value of the parameter.</span></span> |

#### <a name="list-of-parameters-by-action"></a><span data-ttu-id="c775c-198">按操作排列的参数列表</span><span class="sxs-lookup"><span data-stu-id="c775c-198">List of parameters by action</span></span>

<span data-ttu-id="c775c-199">可用参数会有所不同，具体取决于在**操作**快速选项卡上选择的操作。</span><span class="sxs-lookup"><span data-stu-id="c775c-199">The available parameters vary, depending on the action that is selected on the **Actions** FastTab.</span></span>

###### <a name="action-sign-document"></a><span data-ttu-id="c775c-200">操作：对文档签名</span><span class="sxs-lookup"><span data-stu-id="c775c-200">Action: Sign document</span></span>

| <span data-ttu-id="c775c-201">参数</span><span class="sxs-lookup"><span data-stu-id="c775c-201">Parameter</span></span>                             | <span data-ttu-id="c775c-202">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-202">Description</span></span> |
|---------------------------------------|-------------|
| <span data-ttu-id="c775c-203">输入字段</span><span class="sxs-lookup"><span data-stu-id="c775c-203">Input file</span></span>                            | <span data-ttu-id="c775c-204">必须使用电子签名进行签名的输入 XML 文档文件。</span><span class="sxs-lookup"><span data-stu-id="c775c-204">The input XML document file that must be signed by using an electronic signature.</span></span> |
| <span data-ttu-id="c775c-205">证书名称</span><span class="sxs-lookup"><span data-stu-id="c775c-205">Certificate name</span></span>                      | <span data-ttu-id="c775c-206">存储中证书的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-206">The name of the certificate in storage.</span></span> |
| <span data-ttu-id="c775c-207">签名类型</span><span class="sxs-lookup"><span data-stu-id="c775c-207">Signature type</span></span>                        | <span data-ttu-id="c775c-208">要使用的签名类型。</span><span class="sxs-lookup"><span data-stu-id="c775c-208">The type of signature to use.</span></span> |
| <span data-ttu-id="c775c-209">签名方法名称</span><span class="sxs-lookup"><span data-stu-id="c775c-209">Signature method name</span></span>                 | <span data-ttu-id="c775c-210">用于生成电子签名的签名方法的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-210">The name of the signature method that is used to generate an electronic signature.</span></span> |
| <span data-ttu-id="c775c-211">摘要方法名称</span><span class="sxs-lookup"><span data-stu-id="c775c-211">Digest method name</span></span>                    | <span data-ttu-id="c775c-212">用于在数字签名中生成摘要字符串的摘要方法。</span><span class="sxs-lookup"><span data-stu-id="c775c-212">The digest method that is used to generate a digest string in the digital signature.</span></span> |
| <span data-ttu-id="c775c-213">规范化方法名称</span><span class="sxs-lookup"><span data-stu-id="c775c-213">Canonicalization method name</span></span>          | <span data-ttu-id="c775c-214">用于计算签名哈希的规范化方法。</span><span class="sxs-lookup"><span data-stu-id="c775c-214">The canonicalization method that is used to calculate the signature hash.</span></span> |
| <span data-ttu-id="c775c-215">引用属性名称</span><span class="sxs-lookup"><span data-stu-id="c775c-215">Reference attribute name</span></span>              | <span data-ttu-id="c775c-216">指示引用 ID 应该在签名元素中插入的位置的属性名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-216">The attribute name that indicates where the reference ID should be inserted in the signature element.</span></span> |
| <span data-ttu-id="c775c-217">要进行签名的元素名称</span><span class="sxs-lookup"><span data-stu-id="c775c-217">Name of element to sign</span></span>               | <span data-ttu-id="c775c-218">必须使用电子签名进行签名的文档中的 XML 元素的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-218">The name of the XML element in the document that must be signed by using an electronic signature.</span></span> <span data-ttu-id="c775c-219">如果未指定元素，将对文档的根进行签名。</span><span class="sxs-lookup"><span data-stu-id="c775c-219">If no element is specified, the root of the document is signed.</span></span> |
| <span data-ttu-id="c775c-220">插入签名的元素的名称</span><span class="sxs-lookup"><span data-stu-id="c775c-220">Name of element to insert signature</span></span>   | <span data-ttu-id="c775c-221">应在其中插入生成的数字签名的 XML 元素的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-221">The name of the XML element where a generated digital signature should be inserted.</span></span> <span data-ttu-id="c775c-222">如果未指定元素，签名将插入文档的根。</span><span class="sxs-lookup"><span data-stu-id="c775c-222">If no element is specified, the signature is inserted in the root of the document.</span></span> |
| <span data-ttu-id="c775c-223">带有摘要转换的 XLST 文件</span><span class="sxs-lookup"><span data-stu-id="c775c-223">XLST file with digest transform</span></span>       | <span data-ttu-id="c775c-224">包含用于为电子签名生成摘要字符串的摘要转换规则的可扩展样式表语言转换 (XSLT) 文件。</span><span class="sxs-lookup"><span data-stu-id="c775c-224">The Extensible Stylesheet Language Transformations (XSLT) file that contains digest transformation rules to generate the digest string for an electronic signature.</span></span> |
| <span data-ttu-id="c775c-225">插入摘要字符串的路径</span><span class="sxs-lookup"><span data-stu-id="c775c-225">Path to insert digest string</span></span>          | <span data-ttu-id="c775c-226">必须在其中插入生成的摘要字符串的位置的路径，格式为 **\<elementName\>.\<Attribute.Path\>**</span><span class="sxs-lookup"><span data-stu-id="c775c-226">The path, in **\<elementName\>.\<Attribute.Path\>**</span></span> <span data-ttu-id="c775c-227">。</span><span class="sxs-lookup"><span data-stu-id="c775c-227">format, of the location where the generated digest string must be inserted.</span></span> |
| <span data-ttu-id="c775c-228">证书编号位置</span><span class="sxs-lookup"><span data-stu-id="c775c-228">Certificate number location</span></span>           | <span data-ttu-id="c775c-229">应放置证书编号的元素和属性的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-229">The name of the element and attribute where the certificate number should be put.</span></span> |
| <span data-ttu-id="c775c-230">证书数据的位置</span><span class="sxs-lookup"><span data-stu-id="c775c-230">Location of certificate data</span></span>          | <span data-ttu-id="c775c-231">必须在其中插入证书数据 (base64) 的元素和属性的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-231">The name of the element and attribute where certificate data (base64) must be inserted.</span></span> |
| <span data-ttu-id="c775c-232">证书编号为 ASCII 格式</span><span class="sxs-lookup"><span data-stu-id="c775c-232">Certificate number is in ASCII format</span></span> | <span data-ttu-id="c775c-233">指定证书的编号是否以 ASCII 格式编码的值。</span><span class="sxs-lookup"><span data-stu-id="c775c-233">A value that specifies whether the number of the certificate is encoded in ASCII format.</span></span> |

###### <a name="action-filestoreactionname"></a><span data-ttu-id="c775c-234">操作：FileStoreActionName</span><span class="sxs-lookup"><span data-stu-id="c775c-234">Action: FileStoreActionName</span></span>

| <span data-ttu-id="c775c-235">参数</span><span class="sxs-lookup"><span data-stu-id="c775c-235">Parameter</span></span>  | <span data-ttu-id="c775c-236">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-236">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c775c-237">输入字段</span><span class="sxs-lookup"><span data-stu-id="c775c-237">Input file</span></span> | <span data-ttu-id="c775c-238">要存储的输入文件。</span><span class="sxs-lookup"><span data-stu-id="c775c-238">The input file to store.</span></span> |

###### <a name="action-transform-document"></a><span data-ttu-id="c775c-239">操作：转换文档</span><span class="sxs-lookup"><span data-stu-id="c775c-239">Action: Transform document</span></span>

| <span data-ttu-id="c775c-240">参数</span><span class="sxs-lookup"><span data-stu-id="c775c-240">Parameter</span></span>                       | <span data-ttu-id="c775c-241">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-241">Description</span></span> |
|---------------------------------|-------------|
| <span data-ttu-id="c775c-242">输入字段</span><span class="sxs-lookup"><span data-stu-id="c775c-242">Input file</span></span>                      | <span data-ttu-id="c775c-243">提供必须对操作运行的数据的源文件。</span><span class="sxs-lookup"><span data-stu-id="c775c-243">The source file that provides the data that must be run to the action.</span></span> |
| <span data-ttu-id="c775c-244">方向</span><span class="sxs-lookup"><span data-stu-id="c775c-244">Direction</span></span>                       | <span data-ttu-id="c775c-245">指示应使用导入格式还是导出格式的值。</span><span class="sxs-lookup"><span data-stu-id="c775c-245">A value that indicates whether the import format or the export format should be used.</span></span> |
| <span data-ttu-id="c775c-246">配置 ID</span><span class="sxs-lookup"><span data-stu-id="c775c-246">Configuration ID</span></span>                | <span data-ttu-id="c775c-247">应该运行的格式。</span><span class="sxs-lookup"><span data-stu-id="c775c-247">The format that should be run.</span></span> |
| <span data-ttu-id="c775c-248">配置版本</span><span class="sxs-lookup"><span data-stu-id="c775c-248">Configuration version</span></span>           | <span data-ttu-id="c775c-249">如果未指定配置版本，将使用最新版本。</span><span class="sxs-lookup"><span data-stu-id="c775c-249">If no configuration version is specified, the most recent version will be used.</span></span> |
| <span data-ttu-id="c775c-250">配置集成点</span><span class="sxs-lookup"><span data-stu-id="c775c-250">Configuration integration point</span></span> | <span data-ttu-id="c775c-251">为报告运行时提供数据的源文件。</span><span class="sxs-lookup"><span data-stu-id="c775c-251">The source file that provides data to the reporting runtime.</span></span> |

###### <a name="action-process-response"></a><span data-ttu-id="c775c-252">操作：处理响应</span><span class="sxs-lookup"><span data-stu-id="c775c-252">Action: Process response</span></span>

| <span data-ttu-id="c775c-253">参数</span><span class="sxs-lookup"><span data-stu-id="c775c-253">Parameter</span></span>                    | <span data-ttu-id="c775c-254">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-254">Description</span></span> |
|------------------------------|-------------|
| <span data-ttu-id="c775c-255">输入字段</span><span class="sxs-lookup"><span data-stu-id="c775c-255">Input file</span></span>                   | <span data-ttu-id="c775c-256">要分析的响应。</span><span class="sxs-lookup"><span data-stu-id="c775c-256">The response to analyze.</span></span> |
| <span data-ttu-id="c775c-257">报告配置列表</span><span class="sxs-lookup"><span data-stu-id="c775c-257">Reporting configuration list</span></span> | <span data-ttu-id="c775c-258">用于解析响应的配置列表。</span><span class="sxs-lookup"><span data-stu-id="c775c-258">A list of configurations that is used to parse responses.</span></span> |

###### <a name="action-call-rest-web-service"></a><span data-ttu-id="c775c-259">操作：调用 REST Web 服务</span><span class="sxs-lookup"><span data-stu-id="c775c-259">Action: Call REST web service</span></span>

| <span data-ttu-id="c775c-260">参数</span><span class="sxs-lookup"><span data-stu-id="c775c-260">Parameter</span></span>                   | <span data-ttu-id="c775c-261">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-261">Description</span></span> |
|-----------------------------|-------------|
| <span data-ttu-id="c775c-262">Web 服务 URL</span><span class="sxs-lookup"><span data-stu-id="c775c-262">Web service URL</span></span>             | <span data-ttu-id="c775c-263">请求发送到的 URL。</span><span class="sxs-lookup"><span data-stu-id="c775c-263">The URL to send requests to.</span></span> |
| <span data-ttu-id="c775c-264">Web 请求超时</span><span class="sxs-lookup"><span data-stu-id="c775c-264">Web request timeout</span></span>         | <span data-ttu-id="c775c-265">等待 Web 服务响应的最长时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="c775c-265">The maximum amount of time (in milliseconds) to wait for a web service response.</span></span> |
| <span data-ttu-id="c775c-266">请求操作类型</span><span class="sxs-lookup"><span data-stu-id="c775c-266">Request operation type</span></span>      | <span data-ttu-id="c775c-267">HTTP 请求操作的类型（例如，**GET**、**POST** 或 **DELETE**）。</span><span class="sxs-lookup"><span data-stu-id="c775c-267">The type of HTTP request operation (for example, **GET**, **POST**, or **DELETE**).</span></span> |
| <span data-ttu-id="c775c-268">证书名称</span><span class="sxs-lookup"><span data-stu-id="c775c-268">Certificate names</span></span>           | <span data-ttu-id="c775c-269">证书名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-269">The certificate names.</span></span> |
| <span data-ttu-id="c775c-270">响应正文编码</span><span class="sxs-lookup"><span data-stu-id="c775c-270">Response body encoding</span></span>      | <span data-ttu-id="c775c-271">预期的 HTTP 响应正文的编码，以可以正确解码。</span><span class="sxs-lookup"><span data-stu-id="c775c-271">The expected encoding of the HTTP response body, so that it can be decoded correctly.</span></span> |
| <span data-ttu-id="c775c-272">HTTP 请求内容类型</span><span class="sxs-lookup"><span data-stu-id="c775c-272">HTTP request content type</span></span>   | <span data-ttu-id="c775c-273">HTTP 请求内容类型标题输入。</span><span class="sxs-lookup"><span data-stu-id="c775c-273">The HTTP request content-type header input.</span></span> |
| <span data-ttu-id="c775c-274">HTTP 请求内容正文</span><span class="sxs-lookup"><span data-stu-id="c775c-274">HTTP request content body</span></span>   | <span data-ttu-id="c775c-275">HTTP 请求正文。</span><span class="sxs-lookup"><span data-stu-id="c775c-275">The HTTP request body.</span></span> <span data-ttu-id="c775c-276">（正文可以为空。）</span><span class="sxs-lookup"><span data-stu-id="c775c-276">(The body can be empty.)</span></span> |
| <span data-ttu-id="c775c-277">HTTP 参数查询值</span><span class="sxs-lookup"><span data-stu-id="c775c-277">HTTP parameter query values</span></span> | <span data-ttu-id="c775c-278">用于使用可变参数填充 URL 的参数查询值。</span><span class="sxs-lookup"><span data-stu-id="c775c-278">Parameter query values that are used to fill the URL with variable parameters.</span></span> |
| <span data-ttu-id="c775c-279">请求路由</span><span class="sxs-lookup"><span data-stu-id="c775c-279">Request route</span></span>               | <span data-ttu-id="c775c-280">HTTP 请求的路由路径。</span><span class="sxs-lookup"><span data-stu-id="c775c-280">The route path for the HTTP request.</span></span> <span data-ttu-id="c775c-281">变量参数可以用 **\{paramName\}** 表示法编写。</span><span class="sxs-lookup"><span data-stu-id="c775c-281">The variable parameters can be written in **\{paramName\}** notation.</span></span> <span data-ttu-id="c775c-282">这是一个示例：**"api/{id}/submit"**。</span><span class="sxs-lookup"><span data-stu-id="c775c-282">Here is an example: **"api/{id}/submit"**.</span></span> |
| <span data-ttu-id="c775c-283">路由参数列表</span><span class="sxs-lookup"><span data-stu-id="c775c-283">Route parameter list</span></span>        | <span data-ttu-id="c775c-284">用于将变量插入路由的路由参数（采用键值表示法）。</span><span class="sxs-lookup"><span data-stu-id="c775c-284">The route parameters, in key-value notation, that are used to insert variables into the route.</span></span> |
| <span data-ttu-id="c775c-285">自定义 HTTP 标题</span><span class="sxs-lookup"><span data-stu-id="c775c-285">Custom HTTP headers</span></span>         | <span data-ttu-id="c775c-286">要放入请求中的自定义 HTTP 标题。</span><span class="sxs-lookup"><span data-stu-id="c775c-286">The custom HTTP headers to put into the request.</span></span> |
| <span data-ttu-id="c775c-287">HTTP 请求 cookie</span><span class="sxs-lookup"><span data-stu-id="c775c-287">HTTP request cookies</span></span>        | <span data-ttu-id="c775c-288">要放入 HTTP cookie 标题请求中的 cookie（采用键值表示法）的列表。</span><span class="sxs-lookup"><span data-stu-id="c775c-288">A list of cookies, in key-value notation, to put into the HTTP cookies header request.</span></span> |
| <span data-ttu-id="c775c-289">安全协议</span><span class="sxs-lookup"><span data-stu-id="c775c-289">Security protocol</span></span>           | <span data-ttu-id="c775c-290">用于 HTTP 请求与服务器通信的安全协议。</span><span class="sxs-lookup"><span data-stu-id="c775c-290">The security protocol to use for HTTP requests to communicate with the server.</span></span> <span data-ttu-id="c775c-291">（默认情况下，使用传输层安全性 \[TLS\] 1.2。）</span><span class="sxs-lookup"><span data-stu-id="c775c-291">(By default, Transport Layer Security \[TLS\] 1.2 is used.)</span></span> |

###### <a name="action-call-mexican-pac-service"></a><span data-ttu-id="c775c-292">操作：调用墨西哥 PAC 服务</span><span class="sxs-lookup"><span data-stu-id="c775c-292">Action: Call Mexican PAC service</span></span>

| <span data-ttu-id="c775c-293">参数</span><span class="sxs-lookup"><span data-stu-id="c775c-293">Parameter</span></span>                | <span data-ttu-id="c775c-294">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-294">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="c775c-295">输入字段</span><span class="sxs-lookup"><span data-stu-id="c775c-295">Input file</span></span>               | <span data-ttu-id="c775c-296">包含将作为方法输入参数发送到 Web 服务的 XML 数据的文件。</span><span class="sxs-lookup"><span data-stu-id="c775c-296">The file that contains XML data that will be sent to the web service as a method input parameter.</span></span> |
| <span data-ttu-id="c775c-297">URL 地址</span><span class="sxs-lookup"><span data-stu-id="c775c-297">URL address</span></span>              | <span data-ttu-id="c775c-298">Web 服务地址（终结点）。</span><span class="sxs-lookup"><span data-stu-id="c775c-298">The web service address (endpoint).</span></span> |
| <span data-ttu-id="c775c-299">Web 方法（操作）名称</span><span class="sxs-lookup"><span data-stu-id="c775c-299">Web method (action) name</span></span> | <span data-ttu-id="c775c-300">必须运行的 Web 方法（操作）的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-300">The name of the web method (action) that must be run.</span></span> |
| <span data-ttu-id="c775c-301">证书</span><span class="sxs-lookup"><span data-stu-id="c775c-301">Certificates</span></span>             | <span data-ttu-id="c775c-302">Web 服务进行客户端身份验证所需的证书链。</span><span class="sxs-lookup"><span data-stu-id="c775c-302">The certificate chain that is required for client authentication by the web service.</span></span> <span data-ttu-id="c775c-303">客户端证书应该是链中的最后一个证书。</span><span class="sxs-lookup"><span data-stu-id="c775c-303">The client certificate should be the last certificate in the chain.</span></span> <span data-ttu-id="c775c-304">根证书和中间证书应该是第一个。</span><span class="sxs-lookup"><span data-stu-id="c775c-304">The root and intermediate certificates should be first.</span></span> |
| <span data-ttu-id="c775c-305">Web 请求超时</span><span class="sxs-lookup"><span data-stu-id="c775c-305">Web request timeout</span></span>      | <span data-ttu-id="c775c-306">等待 Web 服务响应的最长时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="c775c-306">The maximum amount of time (in milliseconds) to wait for a web service response.</span></span> |
| <span data-ttu-id="c775c-307">重试间隔</span><span class="sxs-lookup"><span data-stu-id="c775c-307">Retry interval</span></span>           | <span data-ttu-id="c775c-308">尝试从 Web 服务调用和接收响应之间的间隔。</span><span class="sxs-lookup"><span data-stu-id="c775c-308">The interval between attempts to call and receive a response from the web service.</span></span> <span data-ttu-id="c775c-309">如果未指定间隔，在第一个调用失败后将不进行其他重试。</span><span class="sxs-lookup"><span data-stu-id="c775c-309">If no interval is specified, no additional retries will be made after the first call is unsuccessful.</span></span> |
| <span data-ttu-id="c775c-310">重试计数</span><span class="sxs-lookup"><span data-stu-id="c775c-310">Retry count</span></span>              | <span data-ttu-id="c775c-311">从 Web 服务调用和检索响应的最大重试尝试次数。</span><span class="sxs-lookup"><span data-stu-id="c775c-311">The maximum number of retry attempts to call and retrieve a response from the web service.</span></span> |
| <span data-ttu-id="c775c-312">重试截止时间</span><span class="sxs-lookup"><span data-stu-id="c775c-312">Retry till</span></span>               | <span data-ttu-id="c775c-313">重试调用可以继续的最长时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="c775c-313">The maximum time (in milliseconds) that retry calls can continue.</span></span> |
| <span data-ttu-id="c775c-314">最小退避</span><span class="sxs-lookup"><span data-stu-id="c775c-314">Minimum back off</span></span>         | <span data-ttu-id="c775c-315">重试间隔指数计算的最小退避率。</span><span class="sxs-lookup"><span data-stu-id="c775c-315">The minimum back-off rate for exponential calculation of retry intervals.</span></span> |
| <span data-ttu-id="c775c-316">最大退避</span><span class="sxs-lookup"><span data-stu-id="c775c-316">Maximum back off</span></span>         | <span data-ttu-id="c775c-317">重试间隔指数计算的最大退避率。</span><span class="sxs-lookup"><span data-stu-id="c775c-317">The maximum back-off rate for exponential calculation of retry intervals.</span></span> |
| <span data-ttu-id="c775c-318">安全协议</span><span class="sxs-lookup"><span data-stu-id="c775c-318">Security protocol</span></span>        | <span data-ttu-id="c775c-319">用于 HTTP 请求与服务器通信的安全协议。</span><span class="sxs-lookup"><span data-stu-id="c775c-319">The security protocol to use for HTTP requests to communicate with the server.</span></span> <span data-ttu-id="c775c-320">（默认情况下，使用 TLS 1.2。）</span><span class="sxs-lookup"><span data-stu-id="c775c-320">(By default, TLS 1.2 is used.)</span></span> |

###### <a name="action-call-brazilian-sefaz-service"></a><span data-ttu-id="c775c-321">操作：调用巴西 SEFAZ 服务</span><span class="sxs-lookup"><span data-stu-id="c775c-321">Action: Call Brazilian SEFAZ service</span></span>

| <span data-ttu-id="c775c-322">参数</span><span class="sxs-lookup"><span data-stu-id="c775c-322">Parameter</span></span>                | <span data-ttu-id="c775c-323">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-323">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="c775c-324">输入字段</span><span class="sxs-lookup"><span data-stu-id="c775c-324">Input file</span></span>               | <span data-ttu-id="c775c-325">包含将作为方法输入参数发送到 Web 服务的 XML 数据的文件。</span><span class="sxs-lookup"><span data-stu-id="c775c-325">The file that contains XML data that will be sent to the web service as a method input parameter.</span></span> |
| <span data-ttu-id="c775c-326">URL 地址</span><span class="sxs-lookup"><span data-stu-id="c775c-326">URL address</span></span>              | <span data-ttu-id="c775c-327">Web 服务地址（终结点）。</span><span class="sxs-lookup"><span data-stu-id="c775c-327">The web service address (endpoint).</span></span> |
| <span data-ttu-id="c775c-328">Web 方法（操作）名称</span><span class="sxs-lookup"><span data-stu-id="c775c-328">Web method (action) name</span></span> | <span data-ttu-id="c775c-329">必须运行的 Web 方法（操作）的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-329">The name of the web method (action) that must be run.</span></span> |
| <span data-ttu-id="c775c-330">证书</span><span class="sxs-lookup"><span data-stu-id="c775c-330">Certificates</span></span>             | <span data-ttu-id="c775c-331">Web 服务进行客户端身份验证所需的证书链。</span><span class="sxs-lookup"><span data-stu-id="c775c-331">The certificate chain that is required for client authentication by the web service.</span></span> <span data-ttu-id="c775c-332">客户端证书应该是链中的最后一个证书。</span><span class="sxs-lookup"><span data-stu-id="c775c-332">The client certificate should be the last certificate in the chain.</span></span> <span data-ttu-id="c775c-333">根证书和中间证书应该是第一个。</span><span class="sxs-lookup"><span data-stu-id="c775c-333">The root and intermediate certificates should be first.</span></span> |
| <span data-ttu-id="c775c-334">Web 请求超时</span><span class="sxs-lookup"><span data-stu-id="c775c-334">Web request timeout</span></span>      | <span data-ttu-id="c775c-335">等待 Web 服务响应的最长时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="c775c-335">The maximum amount of time (in milliseconds) to wait for a web service response.</span></span> |
| <span data-ttu-id="c775c-336">重试间隔</span><span class="sxs-lookup"><span data-stu-id="c775c-336">Retry interval</span></span>           | <span data-ttu-id="c775c-337">尝试从 Web 服务调用和接收响应之间的间隔。</span><span class="sxs-lookup"><span data-stu-id="c775c-337">The interval between attempts to call and receive a response from the web service.</span></span> <span data-ttu-id="c775c-338">如果未指定间隔，在第一个调用失败后将不进行其他重试。</span><span class="sxs-lookup"><span data-stu-id="c775c-338">If no interval is specified, no additional retries will be made after the first call is unsuccessful.</span></span> |
| <span data-ttu-id="c775c-339">重试计数</span><span class="sxs-lookup"><span data-stu-id="c775c-339">Retry count</span></span>              | <span data-ttu-id="c775c-340">从 Web 服务调用和检索响应的最大重试尝试次数。</span><span class="sxs-lookup"><span data-stu-id="c775c-340">The maximum number of retry attempts to call and retrieve a response from the web service.</span></span> |
| <span data-ttu-id="c775c-341">重试截止时间</span><span class="sxs-lookup"><span data-stu-id="c775c-341">Retry till</span></span>               | <span data-ttu-id="c775c-342">重试调用可以继续的最长时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="c775c-342">The maximum time (in milliseconds) that retry calls can continue.</span></span> |
| <span data-ttu-id="c775c-343">最小退避</span><span class="sxs-lookup"><span data-stu-id="c775c-343">Minimum back off</span></span>         | <span data-ttu-id="c775c-344">重试间隔指数计算的最小退避率。</span><span class="sxs-lookup"><span data-stu-id="c775c-344">The minimum back-off rate for exponential calculation of retry intervals.</span></span> |
| <span data-ttu-id="c775c-345">最大退避</span><span class="sxs-lookup"><span data-stu-id="c775c-345">Maximum back off</span></span>         | <span data-ttu-id="c775c-346">重试间隔指数计算的最大退避率。</span><span class="sxs-lookup"><span data-stu-id="c775c-346">The maximum back-off rate for exponential calculation of retry intervals.</span></span> |
| <span data-ttu-id="c775c-347">安全协议</span><span class="sxs-lookup"><span data-stu-id="c775c-347">Security protocol</span></span>        | <span data-ttu-id="c775c-348">用于 HTTP 请求与服务器通信的安全协议。</span><span class="sxs-lookup"><span data-stu-id="c775c-348">The security protocol to use for HTTP requests to communicate with the server.</span></span> <span data-ttu-id="c775c-349">（默认情况下，使用 TLS 1.2。）</span><span class="sxs-lookup"><span data-stu-id="c775c-349">(By default, TLS 1.2 is used.)</span></span> |

###### <a name="action-call-italian-sdi-service"></a><span data-ttu-id="c775c-350">操作：调用意大利 SDI 服务</span><span class="sxs-lookup"><span data-stu-id="c775c-350">Action: Call Italian SDI service</span></span>

| <span data-ttu-id="c775c-351">参数</span><span class="sxs-lookup"><span data-stu-id="c775c-351">Parameter</span></span>                | <span data-ttu-id="c775c-352">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-352">Description</span></span> |
|--------------------------|-------------|
| <span data-ttu-id="c775c-353">输入字段</span><span class="sxs-lookup"><span data-stu-id="c775c-353">Input file</span></span>               | <span data-ttu-id="c775c-354">包含将作为方法输入参数发送到 Web 服务的 XML 数据的文件。</span><span class="sxs-lookup"><span data-stu-id="c775c-354">The file that contains XML data that will be sent to the web service as a method input parameter.</span></span> |
| <span data-ttu-id="c775c-355">URL 地址</span><span class="sxs-lookup"><span data-stu-id="c775c-355">URL address</span></span>              | <span data-ttu-id="c775c-356">Web 服务地址（终结点）。</span><span class="sxs-lookup"><span data-stu-id="c775c-356">The web service address (endpoint).</span></span> |
| <span data-ttu-id="c775c-357">Web 方法（操作）名称</span><span class="sxs-lookup"><span data-stu-id="c775c-357">Web method (action) name</span></span> | <span data-ttu-id="c775c-358">必须运行的 Web 方法（操作）的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-358">The name of the web method (action) that must be run.</span></span> |
| <span data-ttu-id="c775c-359">证书</span><span class="sxs-lookup"><span data-stu-id="c775c-359">Certificates</span></span>             | <span data-ttu-id="c775c-360">Web 服务进行客户端身份验证所需的证书链。</span><span class="sxs-lookup"><span data-stu-id="c775c-360">The certificate chain that is required for client authentication by the web service.</span></span> <span data-ttu-id="c775c-361">客户端证书应该是链中的最后一个证书。</span><span class="sxs-lookup"><span data-stu-id="c775c-361">The client certificate should be the last certificate in the chain.</span></span> <span data-ttu-id="c775c-362">根证书和中间证书应该是第一个。</span><span class="sxs-lookup"><span data-stu-id="c775c-362">The root and intermediate certificates should be first.</span></span> |
| <span data-ttu-id="c775c-363">Web 请求超时</span><span class="sxs-lookup"><span data-stu-id="c775c-363">Web request timeout</span></span>      | <span data-ttu-id="c775c-364">等待 Web 服务响应的最长时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="c775c-364">The maximum amount of time (in milliseconds) to wait for a web service response.</span></span> |
| <span data-ttu-id="c775c-365">重试间隔</span><span class="sxs-lookup"><span data-stu-id="c775c-365">Retry interval</span></span>           | <span data-ttu-id="c775c-366">尝试从 Web 服务调用和接收响应之间的间隔。</span><span class="sxs-lookup"><span data-stu-id="c775c-366">The interval between attempts to call and receive a response from the web service.</span></span> <span data-ttu-id="c775c-367">如果未指定间隔，在第一个调用失败后将不进行其他重试。</span><span class="sxs-lookup"><span data-stu-id="c775c-367">If no interval is specified, no additional retries will be made after the first call is unsuccessful.</span></span> |
| <span data-ttu-id="c775c-368">重试计数</span><span class="sxs-lookup"><span data-stu-id="c775c-368">Retry count</span></span>              | <span data-ttu-id="c775c-369">从 Web 服务调用和检索响应的最大重试尝试次数。</span><span class="sxs-lookup"><span data-stu-id="c775c-369">The maximum number of retry attempts to call and retrieve a response from the web service.</span></span> |
| <span data-ttu-id="c775c-370">重试截止时间</span><span class="sxs-lookup"><span data-stu-id="c775c-370">Retry till</span></span>               | <span data-ttu-id="c775c-371">重试调用可以继续的最长时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="c775c-371">The maximum time (in milliseconds) that retry calls can continue.</span></span> |
| <span data-ttu-id="c775c-372">最小退避</span><span class="sxs-lookup"><span data-stu-id="c775c-372">Minimum back off</span></span>         | <span data-ttu-id="c775c-373">重试间隔指数计算的最小退避率。</span><span class="sxs-lookup"><span data-stu-id="c775c-373">The minimum back-off rate for exponential calculation of retry intervals.</span></span> |
| <span data-ttu-id="c775c-374">最大退避</span><span class="sxs-lookup"><span data-stu-id="c775c-374">Maximum back off</span></span>         | <span data-ttu-id="c775c-375">重试间隔指数计算的最大退避率。</span><span class="sxs-lookup"><span data-stu-id="c775c-375">The maximum back-off rate for exponential calculation of retry intervals.</span></span> |
| <span data-ttu-id="c775c-376">安全协议</span><span class="sxs-lookup"><span data-stu-id="c775c-376">Security protocol</span></span>        | <span data-ttu-id="c775c-377">用于 HTTP 请求与服务器通信的安全协议。</span><span class="sxs-lookup"><span data-stu-id="c775c-377">The security protocol to use for HTTP requests to communicate with the server.</span></span> <span data-ttu-id="c775c-378">（默认情况下，使用 TLS 1.2。）</span><span class="sxs-lookup"><span data-stu-id="c775c-378">(By default, TLS 1.2 is used.)</span></span> |

### <a name="applicability-rules"></a><span data-ttu-id="c775c-379">适用性规则</span><span class="sxs-lookup"><span data-stu-id="c775c-379">Applicability rules</span></span>

<span data-ttu-id="c775c-380">适用性规则使您可以创建确定功能设置用法上下文的逻辑规则。</span><span class="sxs-lookup"><span data-stu-id="c775c-380">Applicability rules let you create logical rules that determine the usage context for the feature setup.</span></span> <span data-ttu-id="c775c-381">因此，所发送的要进行处理的业务文档给定的上下文与适用性规则条件之间的匹配，确定使用哪个电子开票附加产品功能来处理该提交。</span><span class="sxs-lookup"><span data-stu-id="c775c-381">Thus, the matching between the context given by the business document that is sent for processing, along with the applicability rule criteria, determine which Electronic invoicing add-on feature is used to process that submission.</span></span>

#### <a name="set-up-applicability-rules"></a><span data-ttu-id="c775c-382">设置适用性规则</span><span class="sxs-lookup"><span data-stu-id="c775c-382">Set up applicability rules</span></span>

1. <span data-ttu-id="c775c-383">在**功能版本设置**页，在**适用性规则**选项卡上，选择**新建**添加适用性规则。</span><span class="sxs-lookup"><span data-stu-id="c775c-383">On the **Feature version setup** page, on **Applicability rules** tab, select **New** to add an applicability rule.</span></span>

    ![管理适用性规则](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. <span data-ttu-id="c775c-385">在网格中，选择应分组的子句。</span><span class="sxs-lookup"><span data-stu-id="c775c-385">In the grid, select the clauses that should be grouped.</span></span>
3. <span data-ttu-id="c775c-386">选择**分组子句**。</span><span class="sxs-lookup"><span data-stu-id="c775c-386">Select **Group clause**.</span></span>

    ![分组子句](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    <span data-ttu-id="c775c-388">将子句分组后，一个新列将添加到网格中。</span><span class="sxs-lookup"><span data-stu-id="c775c-388">When clauses are grouped, a new column is added to the grid.</span></span> <span data-ttu-id="c775c-389">此列指定分组子句的逻辑运算符。</span><span class="sxs-lookup"><span data-stu-id="c775c-389">This column specifies the logical operator for the grouped clauses.</span></span>

    ![分组子句的逻辑运算符](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

<span data-ttu-id="c775c-391">若要取消对子句的分组，请选择要取消分组的分组子句，然后选择**取消子句分组**。</span><span class="sxs-lookup"><span data-stu-id="c775c-391">To ungroup clauses, select the grouped clauses to ungroup, and then select **Ungroup clause**.</span></span>

![取消子句分组](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> <span data-ttu-id="c775c-393">取消子句分组时，请始终从最内部的分组级别开始。</span><span class="sxs-lookup"><span data-stu-id="c775c-393">When you ungroup a clause, always start from the innermost grouping level.</span></span>

<span data-ttu-id="c775c-394">下表说明了**适用性规则**选项卡上可用的字段。</span><span class="sxs-lookup"><span data-stu-id="c775c-394">The following table describes the fields that are available on the **Applicability rules** tab.</span></span>

| <span data-ttu-id="c775c-395">字段</span><span class="sxs-lookup"><span data-stu-id="c775c-395">Field</span></span>         | <span data-ttu-id="c775c-396">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-396">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="c775c-397">与/或</span><span class="sxs-lookup"><span data-stu-id="c775c-397">And/or</span></span>        | <span data-ttu-id="c775c-398">逻辑运算符。</span><span class="sxs-lookup"><span data-stu-id="c775c-398">The logical operator.</span></span> |
| <span data-ttu-id="c775c-399">字段</span><span class="sxs-lookup"><span data-stu-id="c775c-399">Field</span></span>         | <span data-ttu-id="c775c-400">用于构造规则的字段。</span><span class="sxs-lookup"><span data-stu-id="c775c-400">The field to use to construct the rule.</span></span> |
| <span data-ttu-id="c775c-401">运算符类型</span><span class="sxs-lookup"><span data-stu-id="c775c-401">Operator type</span></span> | <span data-ttu-id="c775c-402">运算符的类型：</span><span class="sxs-lookup"><span data-stu-id="c775c-402">The type of operator:</span></span><ul><li><span data-ttu-id="c775c-403">相等</span><span class="sxs-lookup"><span data-stu-id="c775c-403">Equal</span></span></li><li><span data-ttu-id="c775c-404">不等于</span><span class="sxs-lookup"><span data-stu-id="c775c-404">Not equal</span></span></li><li><span data-ttu-id="c775c-405">大于/小于</span><span class="sxs-lookup"><span data-stu-id="c775c-405">Greater than/Less than</span></span></li><li><span data-ttu-id="c775c-406">大于等于/小于等于</span><span class="sxs-lookup"><span data-stu-id="c775c-406">Greater than or equal to/Less than or equal to</span></span></li><li><span data-ttu-id="c775c-407">包含</span><span class="sxs-lookup"><span data-stu-id="c775c-407">Contains</span></span></li><li><span data-ttu-id="c775c-408">开头为</span><span class="sxs-lookup"><span data-stu-id="c775c-408">Begin with</span></span></li></ul> |
| <span data-ttu-id="c775c-409">值</span><span class="sxs-lookup"><span data-stu-id="c775c-409">Value</span></span>         | <span data-ttu-id="c775c-410">规则的条件。</span><span class="sxs-lookup"><span data-stu-id="c775c-410">The criterion for the rule.</span></span> |

### <a name="variables"></a><span data-ttu-id="c775c-411">变量</span><span class="sxs-lookup"><span data-stu-id="c775c-411">Variables</span></span>

<span data-ttu-id="c775c-412">您可以创建变量，然后将它们用作特定操作的参数的输入值。</span><span class="sxs-lookup"><span data-stu-id="c775c-412">You can create variables and then use them as the input value for a parameter of a specific action.</span></span> <span data-ttu-id="c775c-413">您还可以使用它们在电子开票附加产品服务与客户端之间交换作为提交流一部分执行特定操作的结果信息。</span><span class="sxs-lookup"><span data-stu-id="c775c-413">You can also use them to exchange, between the Electronic invoicing add-on services and the client, information that is the result of execution of a specific action as part of the flow of submissions.</span></span>

#### <a name="set-up-variables"></a><span data-ttu-id="c775c-414">设置变量</span><span class="sxs-lookup"><span data-stu-id="c775c-414">Set up variables</span></span>

- <span data-ttu-id="c775c-415">在**功能版本设置**页上的**变量**选项卡上，选择**新建**或**删除**管理变量。</span><span class="sxs-lookup"><span data-stu-id="c775c-415">On the **Feature version setup** page, on the **Variables** tab, select **New** or **Delete** to manage variables.</span></span>

    ![管理变量](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

<span data-ttu-id="c775c-417">下表说明了**变量**选项卡上可用的字段。</span><span class="sxs-lookup"><span data-stu-id="c775c-417">The following table describes the fields that are available on the **Variables** tab.</span></span>

| <span data-ttu-id="c775c-418">字段</span><span class="sxs-lookup"><span data-stu-id="c775c-418">Field</span></span>       | <span data-ttu-id="c775c-419">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-419">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="c775c-420">姓名</span><span class="sxs-lookup"><span data-stu-id="c775c-420">Name</span></span>        | <span data-ttu-id="c775c-421">变量的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-421">The name of the variable.</span></span> |
| <span data-ttu-id="c775c-422">说明</span><span class="sxs-lookup"><span data-stu-id="c775c-422">Description</span></span> | <span data-ttu-id="c775c-423">变量的简要说明。</span><span class="sxs-lookup"><span data-stu-id="c775c-423">A brief description of the variable.</span></span> |
| <span data-ttu-id="c775c-424">类型</span><span class="sxs-lookup"><span data-stu-id="c775c-424">Type</span></span>        | <span data-ttu-id="c775c-425">变量的类型：</span><span class="sxs-lookup"><span data-stu-id="c775c-425">The type of variable:</span></span><ul><li><span data-ttu-id="c775c-426"><strong>常数</strong> – 变量的内容是固定的。</span><span class="sxs-lookup"><span data-stu-id="c775c-426"><strong>Constant</strong> – The content of the variable is fixed.</span></span></li><li><span data-ttu-id="c775c-427"><strong>从客户端</strong> – 变量的内容在执行提交流程期间从 Microsoft Dynamics 365 客户端获取。</span><span class="sxs-lookup"><span data-stu-id="c775c-427"><strong>From client</strong> – The content of the variable is acquired from the Microsoft Dynamics 365 client during execution of the submission process.</span></span></li><li><span data-ttu-id="c775c-428"><strong>到客户端</strong> – 变量的内容在执行提交流程期间可以供 Microsoft Dynamics 365 客户端导入。</span><span class="sxs-lookup"><span data-stu-id="c775c-428"><strong>To client</strong> – The content of the variable is made available for import by the Microsoft Dynamics 365 client during execution of the submission process.</span></span></li></ul> |
| <span data-ttu-id="c775c-429">数据类型</span><span class="sxs-lookup"><span data-stu-id="c775c-429">Data type</span></span>   | <span data-ttu-id="c775c-430">变量的数据类型：</span><span class="sxs-lookup"><span data-stu-id="c775c-430">The data type of the variable:</span></span><ul><li><span data-ttu-id="c775c-431">Boolean</span><span class="sxs-lookup"><span data-stu-id="c775c-431">Boolean</span></span></li><li><span data-ttu-id="c775c-432">日期</span><span class="sxs-lookup"><span data-stu-id="c775c-432">Date</span></span></li><li><span data-ttu-id="c775c-433">数值</span><span class="sxs-lookup"><span data-stu-id="c775c-433">Number</span></span></li><li><span data-ttu-id="c775c-434">UUID</span><span class="sxs-lookup"><span data-stu-id="c775c-434">UUID</span></span></li><li><span data-ttu-id="c775c-435">字符串</span><span class="sxs-lookup"><span data-stu-id="c775c-435">String</span></span></li><li><span data-ttu-id="c775c-436">文件</span><span class="sxs-lookup"><span data-stu-id="c775c-436">File</span></span></li></ul> |
| <span data-ttu-id="c775c-437">值</span><span class="sxs-lookup"><span data-stu-id="c775c-437">Value</span></span>       | <span data-ttu-id="c775c-438">变量的值或设置变量值的操作的名称。</span><span class="sxs-lookup"><span data-stu-id="c775c-438">The value of the variable or the name of the action that sets the value of the variable.</span></span> |

### <a name="validate-the-feature-setup"></a><span data-ttu-id="c775c-439">验证功能设置</span><span class="sxs-lookup"><span data-stu-id="c775c-439">Validate the feature setup</span></span>

- <span data-ttu-id="c775c-440">在**功能版本设置**页上的操作窗格上，选择**验证**验证功能版本设置。</span><span class="sxs-lookup"><span data-stu-id="c775c-440">On the **Feature version setup** page, on the Action Pane, select **Validate** to validate the feature version setup.</span></span>

   ![选择“验证”按钮](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

<span data-ttu-id="c775c-442">验证检查整个配置的一致性。</span><span class="sxs-lookup"><span data-stu-id="c775c-442">The validation checks the consistency of the whole configuration.</span></span> <span data-ttu-id="c775c-443">例如，如果某个操作的特定参数是强制性的，但其值仍为空白，验证会检测到这种不一致，您会收到警告。</span><span class="sxs-lookup"><span data-stu-id="c775c-443">For example, if a specific parameter for an action is mandatory but its value remains blank, the validation detects this inconsistency, and you receive a warning.</span></span>

## <a name="environments"></a><span data-ttu-id="c775c-444">环境</span><span class="sxs-lookup"><span data-stu-id="c775c-444">Environments</span></span>

<span data-ttu-id="c775c-445">电子开票附加产品环境必须与电子开票附加产品功能关联并启用。</span><span class="sxs-lookup"><span data-stu-id="c775c-445">An Electronic invoicing add-on environment must be associated with the Electronic invoicing add-on feature and enabled for it.</span></span> <span data-ttu-id="c775c-446">必须通过在组织的 RCS 帐户中配置全球化功能预先创建和发布电子开票附加产品环境。</span><span class="sxs-lookup"><span data-stu-id="c775c-446">Electronic invoicing add-on environments must be created and published in advance, through the configuration of Globalization features in your organization's RCS account.</span></span>

<span data-ttu-id="c775c-447">请按照以下步骤为电子开票附加产品功能启用电子开票附加产品环境。</span><span class="sxs-lookup"><span data-stu-id="c775c-447">Follow these steps to enable an Electronic invoicing add-on environment for the Electronic invoicing add-on feature.</span></span>

1. <span data-ttu-id="c775c-448">在**电子开票附加产品功能**页上的**环境**选项卡上，选择**启用**添加电子开票附加产品环境。</span><span class="sxs-lookup"><span data-stu-id="c775c-448">On the **Electronic invoicing add-on features** page, on the **Environments** tab, select **Enable** to add an Electronic invoicing add-on environment.</span></span>
2. <span data-ttu-id="c775c-449">在**生效开始日期**字段中，输入新环境生效的日期。</span><span class="sxs-lookup"><span data-stu-id="c775c-449">In the **Effective from** field, enter the date when the new environment becomes effective.</span></span>

![启用电子开票附加产品环境](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a><span data-ttu-id="c775c-451">组织</span><span class="sxs-lookup"><span data-stu-id="c775c-451">Organizations</span></span>

<span data-ttu-id="c775c-452">电子开票附加产品功能可以在多个组织之间共享。</span><span class="sxs-lookup"><span data-stu-id="c775c-452">The Electronic invoicing add-on feature can be shared across multiple organizations.</span></span>

- <span data-ttu-id="c775c-453">在**电子开票附加产品功能**页上的**组织**选项卡上，选择**共享**添加要与之共享电子开票附加产品功能的组织。</span><span class="sxs-lookup"><span data-stu-id="c775c-453">On the **Electronic invoicing add-on features** page, on the **Organizations** tab, select **Share with** to add the organization that you want to share the Electronic invoicing add-on feature with.</span></span>

<span data-ttu-id="c775c-454">要停止与组织共享电子开票附加产品功能，请选择**取消共享**。</span><span class="sxs-lookup"><span data-stu-id="c775c-454">To stop sharing the Electronic invoicing add-on feature with the organization, select **Unshare**.</span></span>

## <a name="versions"></a><span data-ttu-id="c775c-455">版本</span><span class="sxs-lookup"><span data-stu-id="c775c-455">Versions</span></span>

<span data-ttu-id="c775c-456">版本通过管理电子开票附加产品功能的状态来帮助控制电子开票附加产品功能的生命周期。</span><span class="sxs-lookup"><span data-stu-id="c775c-456">Versions help control the lifecycle of the Electronic invoicing add-on feature by managing its status.</span></span> <span data-ttu-id="c775c-457">您可以创建现有电子开票附加产品功能的新版本，或在完成电子开票附加产品功能的所有配置后，可以将功能的状态更改为**完成**，然后更改为**发布**。</span><span class="sxs-lookup"><span data-stu-id="c775c-457">You can create a new version of an existing Electronic invoicing add-on feature, or, when all configuration for the Electronic invoicing add-on feature is completed, you can change the feature's status to **Complete** and then to **Publish**.</span></span>

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a><span data-ttu-id="c775c-458">创建现有电子开票附加产品功能的新版本</span><span class="sxs-lookup"><span data-stu-id="c775c-458">Create a new version of an existing Electronic invoicing add-on feature</span></span>

1. <span data-ttu-id="c775c-459">在**电子开票附加产品功能**页上，在左侧的网格中，选择电子开票附加产品功能。</span><span class="sxs-lookup"><span data-stu-id="c775c-459">On the **Electronic invoicing add-on features** page, in the grid on the left, select the Electronic invoicing add-on feature.</span></span>
2. <span data-ttu-id="c775c-460">在**版本**选项卡上，选择**新建**添加电子开票附加产品功能的新版本。</span><span class="sxs-lookup"><span data-stu-id="c775c-460">On **Versions** tab, select **New** to add a new version of the Electronic invoicing add-on feature.</span></span>

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a><span data-ttu-id="c775c-461">更改电子开票附加产品功能的状态</span><span class="sxs-lookup"><span data-stu-id="c775c-461">Change the status of the Electronic invoicing add-on feature</span></span>

<span data-ttu-id="c775c-462">请按照以下步骤管理电子开票附加产品功能的生命周期。</span><span class="sxs-lookup"><span data-stu-id="c775c-462">Follow these steps to manage the lifecycle of the Electronic invoicing add-on feature.</span></span>

1. <span data-ttu-id="c775c-463">在**电子开票附加产品功能**页上，在左侧的网格中，选择电子开票附加产品功能。</span><span class="sxs-lookup"><span data-stu-id="c775c-463">On the **Electronic invoicing add-on features** page, in the grid on the left, select the Electronic invoicing add-on feature.</span></span>
2. <span data-ttu-id="c775c-464">在**版本**选项卡上，选择**更改状态**，然后将状态从**草稿**更改为**完成**。</span><span class="sxs-lookup"><span data-stu-id="c775c-464">On **Versions** tab, select **Change status**, and then change the status from **Draft** to **Complete**.</span></span>
3. <span data-ttu-id="c775c-465">系统将提示您确认要完成电子开票附加产品功能及其所有组件。</span><span class="sxs-lookup"><span data-stu-id="c775c-465">You're prompted to confirm that you want to complete the Electronic invoicing add-on feature and all its components.</span></span> <span data-ttu-id="c775c-466">选择**是**确认操作或选择**否**取消。</span><span class="sxs-lookup"><span data-stu-id="c775c-466">Select **Yes** to confirm the action or **No** to cancel it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c775c-467">当您选择**是**时，作为电子开票附加产品功能的组件的配置版本的状态会自动从**草稿**更改为**完成**。</span><span class="sxs-lookup"><span data-stu-id="c775c-467">When you select **Yes**, the status of configuration versions, which are components of the Electronic invoicing add-on feature, is automatically changed from **Draft** to **Completed**.</span></span>

4. <span data-ttu-id="c775c-468">选择**更改状态**，然后将状态从**完成**更改为**发布**。</span><span class="sxs-lookup"><span data-stu-id="c775c-468">Select **Change status**, and then change the status from **Complete** to **Publish**.</span></span>
5. <span data-ttu-id="c775c-469">系统将提示您确认要将电子开票附加产品功能及其所有组件发布到全局存储库。</span><span class="sxs-lookup"><span data-stu-id="c775c-469">You're prompted to confirm that you want to publish the Electronic invoicing add-on feature and all its components to the Global repository.</span></span> <span data-ttu-id="c775c-470">选择**是**确认操作或选择**否**取消。</span><span class="sxs-lookup"><span data-stu-id="c775c-470">Select **Yes** to confirm the action or **No** to cancel it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c775c-471">当您选择**是**时，配置版本的状态会自动从**已完成**更改为**已共享**。</span><span class="sxs-lookup"><span data-stu-id="c775c-471">When you select **Yes**, the status of configuration versions is automatically changed from **Completed** to **Shared**.</span></span>
