---
title: Regulatory Configuration Services (RCS) - 全球化功能
description: 此主题介绍如何使用 Microsoft Regulatory Configuration Services (RCS) 和全局知识库创建和使用全球化功能。
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: ae46dab5250fbe8096f43e420cb7ef33a5862af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440662"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="18c14-103">Regulatory Configuration Services (RCS) - 全球化功能</span><span class="sxs-lookup"><span data-stu-id="18c14-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18c14-104">您可以使用 Microsoft Regulatory Configuration Services (RCS) 创建可以在全球化服务（如电子开票服务）中使用的全球化功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="18c14-105">RCS 使您可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="18c14-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="18c14-106">定义相关的功能组件。</span><span class="sxs-lookup"><span data-stu-id="18c14-106">Define related components of a feature.</span></span>
- <span data-ttu-id="18c14-107">通过功能状态管理功能生命周期。</span><span class="sxs-lookup"><span data-stu-id="18c14-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="18c14-108">使功能可用于定义的环境。</span><span class="sxs-lookup"><span data-stu-id="18c14-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="18c14-109">与其他组织共享功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="18c14-110">以下过程说明 RCS 中的用户如何添加全球化功能和相关组件、更新功能的状态，以及提供功能以可以在全球化服务中使用它。</span><span class="sxs-lookup"><span data-stu-id="18c14-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="18c14-111">在完成这些过程之前，您必须完成与以下任务相关的步骤：</span><span class="sxs-lookup"><span data-stu-id="18c14-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="18c14-112">访问 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="18c14-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="18c14-113">创建和激活配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="18c14-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="18c14-114">有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="18c14-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="18c14-115">在您的 Finance and Operations 应用实例中，按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="18c14-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="18c14-116">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="18c14-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="18c14-117">如果没有为公司预配 RCS 环境，请选择 **Regulatory services – 配置**，然后按照说明预配一个。</span><span class="sxs-lookup"><span data-stu-id="18c14-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="18c14-118">如果已经为公司预配了 RCS 环境，请通过选择登录选项使用页面 URL 访问该环境。</span><span class="sxs-lookup"><span data-stu-id="18c14-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="18c14-119">开启全球化功能</span><span class="sxs-lookup"><span data-stu-id="18c14-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="18c14-120">在您的 RCS 实例中，选择 **功能管理** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="18c14-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="18c14-121">在 **功能管理** 工作区，在列表中选择 **全球化功能**，然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="18c14-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![“功能管理”中的“全球化功能”](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="18c14-123">全球化功能</span><span class="sxs-lookup"><span data-stu-id="18c14-123">Globalization features</span></span>

<span data-ttu-id="18c14-124">要使用全球化功能，必须首先从全局知识库导入它并为此功能创建一个您自己的版本。</span><span class="sxs-lookup"><span data-stu-id="18c14-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="18c14-125">有两种添加全球化功能的方法：</span><span class="sxs-lookup"><span data-stu-id="18c14-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="18c14-126">添加基于已发布或共享的现有功能的派生功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="18c14-127">添加您从头开始创建的新功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="18c14-128">访问全球化功能</span><span class="sxs-lookup"><span data-stu-id="18c14-128">Access Globalization features</span></span>

1. <span data-ttu-id="18c14-129">如本主题前面所述，确保在“功能管理”中启用了 **全球化功能** 功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="18c14-130">打开新的 **全球化功能** 工作区，然后在 **功能** 下，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="18c14-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![全局功能工作区](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="18c14-132">**电子开票功能** 页面将打开。</span><span class="sxs-lookup"><span data-stu-id="18c14-132">The **e-Invoicing Features** page is opened.</span></span>

    ![电子开票功能页面](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="18c14-134">添加派生的全球化功能</span><span class="sxs-lookup"><span data-stu-id="18c14-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="18c14-135">您可以通过从已发布或共享的现有功能派生全球化功能来添加新的全球化功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="18c14-136">选择 **导入** 打开 **从全局知识库导入功能** 页面。</span><span class="sxs-lookup"><span data-stu-id="18c14-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![“从全局知识库导入功能”页面](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="18c14-138">选择 **同步** 获取最新功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="18c14-139">同步的列表包含由于 Microsoft 已发布或由于另一个配置提供程序已与您共享而可用的功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![同步的功能列表](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="18c14-141">在此列表中，选择要导入的功能，然后选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="18c14-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="18c14-142">成功导入所选功能后，您会收到一条消息。</span><span class="sxs-lookup"><span data-stu-id="18c14-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![导入成功消息](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="18c14-144">选择 **添加**，然后在下拉对话框中选择 **基于现有版本** 选项。</span><span class="sxs-lookup"><span data-stu-id="18c14-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="18c14-145">为功能输入名称和描述。</span><span class="sxs-lookup"><span data-stu-id="18c14-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="18c14-146">在可用功能列表中，选择功能的基本版本，然后选择 **创建功能**。</span><span class="sxs-lookup"><span data-stu-id="18c14-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![添加派生功能](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="18c14-148">您添加的功能将创建，状态为 **草稿**。</span><span class="sxs-lookup"><span data-stu-id="18c14-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![具有“草稿”状态的派生功能](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="18c14-150">查看功能组件确定是否需要更新：</span><span class="sxs-lookup"><span data-stu-id="18c14-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="18c14-151">如果需要自定义电子报告 (ER) 格式及其与功能版本的格式映射的绑定，请查看配置。</span><span class="sxs-lookup"><span data-stu-id="18c14-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="18c14-152">如果需要针对功能版本自定义 **操作** 选项卡、**适用性规则** 选项卡或 **变量** 选项卡，请查看设置。</span><span class="sxs-lookup"><span data-stu-id="18c14-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="18c14-153">在 **版本** 选项卡上，选择 **生效开始** 日期，如果 **描述** 字段为空，请输入描述。</span><span class="sxs-lookup"><span data-stu-id="18c14-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="18c14-154">选择 **更改状态** 完成功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="18c14-155">完整的功能可以为特定环境提供，以便可以在全球化服务中使用它们，也可以将其发布到全局知识库。</span><span class="sxs-lookup"><span data-stu-id="18c14-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="18c14-156">**功能版本状态** 值为 **已发布** 的功能可以与外部组织共享。</span><span class="sxs-lookup"><span data-stu-id="18c14-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="18c14-157">添加新的全球化功能</span><span class="sxs-lookup"><span data-stu-id="18c14-157">Add a new Globalization feature</span></span>

<span data-ttu-id="18c14-158">您可以通过从头开始创建来添加新的全球化功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="18c14-159">在 **从全局知识库导入功能** 页面上，选择 **添加**，然后在下拉对话框中选择 **新功能** 选项。</span><span class="sxs-lookup"><span data-stu-id="18c14-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="18c14-160">为功能输入名称和描述。</span><span class="sxs-lookup"><span data-stu-id="18c14-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="18c14-161">选择 **创建功能**。</span><span class="sxs-lookup"><span data-stu-id="18c14-161">Select **Create feature**.</span></span>

    ![添加新功能](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="18c14-163">在 **版本** 选项卡上，选择 **生效开始** 日期，然后选择 **更改状态** 完成功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="18c14-164">完整的功能可以为特定环境提供，以便可以在全球化服务中使用它们，也可以将其发布到全局知识库。</span><span class="sxs-lookup"><span data-stu-id="18c14-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="18c14-165">**功能版本状态** 值为 **已发布** 的功能可以与外部组织共享。</span><span class="sxs-lookup"><span data-stu-id="18c14-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="18c14-166">功能组件概览</span><span class="sxs-lookup"><span data-stu-id="18c14-166">Feature component overview</span></span>

<span data-ttu-id="18c14-167">全球化功能包含多个组件：</span><span class="sxs-lookup"><span data-stu-id="18c14-167">Globalization features have several components:</span></span>

- <span data-ttu-id="18c14-168">**版本** – 此组件支持功能生命周期管理，并允许用户管理功能的不同版本的状态。</span><span class="sxs-lookup"><span data-stu-id="18c14-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="18c14-169">**配置** – 此组件使用户可以管理、查看和编辑相关的电子报告格式和格式映射。</span><span class="sxs-lookup"><span data-stu-id="18c14-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="18c14-170">**设置** – 此组件使全球化服务（如电子开票服务）的用户可以管理相关功能版本的设置。</span><span class="sxs-lookup"><span data-stu-id="18c14-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="18c14-171">因此，它支持通信和响应规则的灵活构造。</span><span class="sxs-lookup"><span data-stu-id="18c14-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="18c14-172">**环境** – 此组件使全球化服务（如电子开票服务）的用户可以管理使用功能版本设置的环境，并可以向将有权访问该环境的用户授予授权。</span><span class="sxs-lookup"><span data-stu-id="18c14-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="18c14-173">**组织** – 此组件使用户可以与外部组织共享功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="18c14-174">配置功能组件</span><span class="sxs-lookup"><span data-stu-id="18c14-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="18c14-175">版本和状态</span><span class="sxs-lookup"><span data-stu-id="18c14-175">Version and status</span></span>

<span data-ttu-id="18c14-176">版本用于管理全球化功能生命周期。</span><span class="sxs-lookup"><span data-stu-id="18c14-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="18c14-177">状态可以在 **版本** 选项卡上的 **状态** 字段中更改。以下状态可用：</span><span class="sxs-lookup"><span data-stu-id="18c14-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="18c14-178">**草稿** – 功能仅在此状态下可以编辑。</span><span class="sxs-lookup"><span data-stu-id="18c14-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="18c14-179">**完成** – 功能及所有相关组件已结束（完成），无法进行编辑。</span><span class="sxs-lookup"><span data-stu-id="18c14-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="18c14-180">**已发布** – 功能及所有相关组件已发布到全局存储库。</span><span class="sxs-lookup"><span data-stu-id="18c14-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="18c14-181">**已共享** – 功能及所有相关组件已与外部组织共享。</span><span class="sxs-lookup"><span data-stu-id="18c14-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="18c14-182">**已启用** – 功能及所有相关组件已启用，可以在全球化服务（如电子开票服务）中使用。</span><span class="sxs-lookup"><span data-stu-id="18c14-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="18c14-183">功能必须在其中某些状态中顺序移动。</span><span class="sxs-lookup"><span data-stu-id="18c14-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="18c14-184">因此，可能并非每个状态在每个生命周期阶段都可用。</span><span class="sxs-lookup"><span data-stu-id="18c14-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="18c14-185">配置</span><span class="sxs-lookup"><span data-stu-id="18c14-185">Configurations</span></span>

<span data-ttu-id="18c14-186">以下操作可用于配置：</span><span class="sxs-lookup"><span data-stu-id="18c14-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="18c14-187">**查看** – 查看不需要任何更新的基础功能配置。</span><span class="sxs-lookup"><span data-stu-id="18c14-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="18c14-188">**编辑** – 创建所选配置的草稿版本，以便您可以在格式设计器中编辑格式或格式映射。</span><span class="sxs-lookup"><span data-stu-id="18c14-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="18c14-189">**删除** – 从功能中删除所选配置。</span><span class="sxs-lookup"><span data-stu-id="18c14-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="18c14-190">**重定基本版本** – 重新设定功能的基本版本。</span><span class="sxs-lookup"><span data-stu-id="18c14-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="18c14-191">有关详细信息，请参阅本主题后面的[重新设定派生的全球化功能的基本版本](#rebase)一节。</span><span class="sxs-lookup"><span data-stu-id="18c14-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="18c14-192">设置</span><span class="sxs-lookup"><span data-stu-id="18c14-192">Setups</span></span>

<span data-ttu-id="18c14-193">以下操作可用于功能设置：</span><span class="sxs-lookup"><span data-stu-id="18c14-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="18c14-194">**添加** – 创建新的功能设置。</span><span class="sxs-lookup"><span data-stu-id="18c14-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="18c14-195">此功能设置可以从现有功能设置派生，也可以从头创建。</span><span class="sxs-lookup"><span data-stu-id="18c14-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="18c14-196">**删除** – 删除所选的功能设置。</span><span class="sxs-lookup"><span data-stu-id="18c14-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="18c14-197">**查看** – 查看不需要任何更改的基础功能设置。</span><span class="sxs-lookup"><span data-stu-id="18c14-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="18c14-198">**编辑** – 创建、删除或修改功能设置的三个主要组件的属性：</span><span class="sxs-lookup"><span data-stu-id="18c14-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="18c14-199">操作及其参数</span><span class="sxs-lookup"><span data-stu-id="18c14-199">Actions and their parameters</span></span>
    - <span data-ttu-id="18c14-200">适用性规则</span><span class="sxs-lookup"><span data-stu-id="18c14-200">Applicability rules</span></span>
    - <span data-ttu-id="18c14-201">变量</span><span class="sxs-lookup"><span data-stu-id="18c14-201">Variables</span></span>

![功能版本设置页面](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="18c14-203">环境</span><span class="sxs-lookup"><span data-stu-id="18c14-203">Environments</span></span>

<span data-ttu-id="18c14-204">以下操作可用于环境：</span><span class="sxs-lookup"><span data-stu-id="18c14-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="18c14-205">**启用** – 为所选的功能版本，选择已发布的环境，并选择它应该可用的 **生效开始** 日期。</span><span class="sxs-lookup"><span data-stu-id="18c14-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="18c14-206">有关详细信息，请参阅本主题后面的[为启用配置环境](#configureenvironment)一节。</span><span class="sxs-lookup"><span data-stu-id="18c14-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="18c14-207">**取消** – 删除用于功能设置的环境。</span><span class="sxs-lookup"><span data-stu-id="18c14-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="18c14-208">组织</span><span class="sxs-lookup"><span data-stu-id="18c14-208">Organizations</span></span>

<span data-ttu-id="18c14-209">请按照以下步骤与外部组织共享全球化功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="18c14-210">在 **电子开票功能** 页面，选择功能和要共享的功能版本。</span><span class="sxs-lookup"><span data-stu-id="18c14-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="18c14-211">在 **组织** 选项卡上，选择 **共享**，然后在下拉对话框中输入组织的域名。</span><span class="sxs-lookup"><span data-stu-id="18c14-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="18c14-212">选择 **共享**。</span><span class="sxs-lookup"><span data-stu-id="18c14-212">Select **Share**.</span></span>

    ![与组织共享功能](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="18c14-214">功能将与所选组织共享，并在全局知识库中提供给该组织。</span><span class="sxs-lookup"><span data-stu-id="18c14-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="18c14-215">从那里，功能可以导入到组织的 RCS 或 Dynamics 365 Finance 实例以使它可以使用。</span><span class="sxs-lookup"><span data-stu-id="18c14-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="18c14-216">重新设定派生的全球化功能的基本版本</span><span class="sxs-lookup"><span data-stu-id="18c14-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="18c14-217">您可以将派生的全球化功能重新设定为新的或更新的基本功能版本。</span><span class="sxs-lookup"><span data-stu-id="18c14-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="18c14-218">这样，基本版本中发生的更改可以自动更新。</span><span class="sxs-lookup"><span data-stu-id="18c14-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="18c14-219">更新的基本功能版本由原始配置提供程序创建，然后发布或共享。</span><span class="sxs-lookup"><span data-stu-id="18c14-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![更新的基本功能版本](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="18c14-221">例如，如果要重新设定所创建功能的派生版本的基本版本，请首先通过从全局知识库导入该功能的最新版本来获取最新版本。</span><span class="sxs-lookup"><span data-stu-id="18c14-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="18c14-222">在 **电子开票功能** 页面，选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="18c14-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="18c14-223">选择 **同步** 获取最新功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="18c14-224">在功能列表中，选择要导入的功能，然后选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="18c14-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![导入功能的最新版本](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="18c14-226">在功能列表中，选择要重定基本版本的功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="18c14-227">在 **版本** 选项卡上，选择 **新建** 创建草稿版本。</span><span class="sxs-lookup"><span data-stu-id="18c14-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![新的草稿版本已创建](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="18c14-229">选择 **重定基本版本**。</span><span class="sxs-lookup"><span data-stu-id="18c14-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="18c14-230">在 **重定基本版本** 对话框中，选择要重定的最新的功能版本。</span><span class="sxs-lookup"><span data-stu-id="18c14-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![“重定基本版本”对话框](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="18c14-232">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="18c14-232">Select **OK**.</span></span>
9. <span data-ttu-id="18c14-233">查看功能组件，并进行所需的更改。</span><span class="sxs-lookup"><span data-stu-id="18c14-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="18c14-234">选择 **更改状态** 完成已重定基本版本的功能。</span><span class="sxs-lookup"><span data-stu-id="18c14-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="18c14-235">重定基本版本完成后，您可以执行其他操作。</span><span class="sxs-lookup"><span data-stu-id="18c14-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="18c14-236">例如，您可以发布功能并在全球化服务中提供它供其他用户使用。</span><span class="sxs-lookup"><span data-stu-id="18c14-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![功能状态更新为“已完成”](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="18c14-238">配置全球化功能的环境</span><span class="sxs-lookup"><span data-stu-id="18c14-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="18c14-239">全球化服务的用户可以通过管理环境来设置全球化功能，并向将有权访问环境的其他用户授予授权。</span><span class="sxs-lookup"><span data-stu-id="18c14-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="18c14-240">在 **全球化功能** 工作区，在 **环境** 下，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="18c14-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![全球化功能工作区](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="18c14-242">选择 **密钥保管库参数**，然后选择 **新建** 创建一个 Azure Key Vault 密钥。</span><span class="sxs-lookup"><span data-stu-id="18c14-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="18c14-243">为密钥保管库输入名称和描述，然后在 **密钥保管库 URI** 字段中，输入用于标识 Azure 中的密钥保管库资源的 URL。</span><span class="sxs-lookup"><span data-stu-id="18c14-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="18c14-244">在 **证书** 快速选项卡上，选择 **添加** 以添加证书，并为每个证书输入名称和描述。</span><span class="sxs-lookup"><span data-stu-id="18c14-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![证书已添加](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="18c14-246">选择 **新建** 创建新环境。</span><span class="sxs-lookup"><span data-stu-id="18c14-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="18c14-247">输入名称、描述和存储所需的共享访问签名令牌密钥。</span><span class="sxs-lookup"><span data-stu-id="18c14-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="18c14-248">在 **用户** 快速选项卡上，选择 **新** 添加将有权访问此环境的用户。</span><span class="sxs-lookup"><span data-stu-id="18c14-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="18c14-249">输入用户的用户 ID 和电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="18c14-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="18c14-250">重复执行步骤 7 和 8 添加更多用户。</span><span class="sxs-lookup"><span data-stu-id="18c14-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="18c14-251">选择 **发布** 发布环境。</span><span class="sxs-lookup"><span data-stu-id="18c14-251">Select **Publish** to publish the environment.</span></span>

    ![已发布的环境](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
