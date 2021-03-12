---
title: 在 RCS 中创建 ER 配置并上传到全局知识库
description: 此主题介绍如何在 Microsoft Regulatory Configuration Services (RCS) 中创建电子申报 (ER) 配置并上传到全局知识库。
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ef12c911c8953b181db1c0eff0874a3d8cfcb3da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005740"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="c318c-103">在 Regulatory Configuration Service (RCS) 中创建 ER 配置并上传到全局知识库</span><span class="sxs-lookup"><span data-stu-id="c318c-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c318c-104">可使用 Microsoft Regulatory Configuration Services (RCS) 设计电子申报 (ER) 配置，然后发布，使其可在您的组织中使用。</span><span class="sxs-lookup"><span data-stu-id="c318c-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="c318c-105">以下过程介绍系统管理员或电子申报开发人员角色的用户如何创建已经在 RCS 实例中配置的 ER 配置的派生版本，然后将派生配置上传到全局知识库。</span><span class="sxs-lookup"><span data-stu-id="c318c-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="c318c-106">必须先满足以下先决条件，才能完成这些过程：</span><span class="sxs-lookup"><span data-stu-id="c318c-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="c318c-107">访问 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="c318c-107">Access an RCS instance.</span></span>
- <span data-ttu-id="c318c-108">创建有效配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="c318c-108">Create an active configuration provider.</span></span> <span data-ttu-id="c318c-109">有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="c318c-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="c318c-110">还必须确保为公司预配 RCS 环境。</span><span class="sxs-lookup"><span data-stu-id="c318c-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="c318c-111">在 Finance and Operations 应用中，转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="c318c-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="c318c-112">如果没有为公司预配 RCS 环境，请选择 **Regulatory services – 配置外部**，然后按照说明预配一个。</span><span class="sxs-lookup"><span data-stu-id="c318c-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="c318c-113">如果已经为公司预配了 RCS 环境，请通过选择登录选项使用页面 URL 访问该环境。</span><span class="sxs-lookup"><span data-stu-id="c318c-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="c318c-114">在 RCS 中创建配置的派生版本</span><span class="sxs-lookup"><span data-stu-id="c318c-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="c318c-115">在 **电子申报** 工作区中，验证您是否有组织的有效配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="c318c-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="c318c-116">选择 **申报配置**。</span><span class="sxs-lookup"><span data-stu-id="c318c-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="c318c-117">选择新版本的派生来源配置。</span><span class="sxs-lookup"><span data-stu-id="c318c-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="c318c-118">可以使用上面的筛选器字段缩小搜索范围。</span><span class="sxs-lookup"><span data-stu-id="c318c-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="c318c-119">选择 **创建配置** \> **从名称派生**。</span><span class="sxs-lookup"><span data-stu-id="c318c-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="c318c-120">输入名称和说明，然后选择 **创建配置** 创建新的派生版本。</span><span class="sxs-lookup"><span data-stu-id="c318c-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="c318c-121">选择新派生的配置，添加版本说明，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c318c-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="c318c-122">配置的状态将更改为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="c318c-122">The status of the configuration to is changed to **Completed**.</span></span>

![RCS 中的新配置版本](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="c318c-124">更改配置状态之后，可能会收到与相连应用程序有关的验证错误消息。</span><span class="sxs-lookup"><span data-stu-id="c318c-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="c318c-125">若要关闭验证，请在操作窗格上的 **配置** 选项卡中，选择 **用户参数**，然后将 **配置状态更改时跳过验证并重定基本值** 选项设置为 **是**</span><span class="sxs-lookup"><span data-stu-id="c318c-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="c318c-126">将配置上传到全局知识库</span><span class="sxs-lookup"><span data-stu-id="c318c-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="c318c-127">若要与组织共享新配置或派生配置，可以将其上传到全局知识库。</span><span class="sxs-lookup"><span data-stu-id="c318c-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="c318c-128">选择配置的已完成版本，然后选择 **上传到知识库中**。</span><span class="sxs-lookup"><span data-stu-id="c318c-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="c318c-129">选择 **全局 (Microsoft)** 选项，然后选择 **上传**。</span><span class="sxs-lookup"><span data-stu-id="c318c-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![“上传到知识库中”选项](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="c318c-131">在配置消息框中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="c318c-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="c318c-132">按照需要更新版本说明，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c318c-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="c318c-133">配置状态将更新为 **共享**，并将配置上传到全局知识库中。</span><span class="sxs-lookup"><span data-stu-id="c318c-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="c318c-134">可以在此处按照下面的方法进行处理：</span><span class="sxs-lookup"><span data-stu-id="c318c-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="c318c-135">将其导入到您的 Dynamics 365 实例中。</span><span class="sxs-lookup"><span data-stu-id="c318c-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="c318c-136">有关详细信息，请参阅 [(ER) 从 RCS 导入配置](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)。</span><span class="sxs-lookup"><span data-stu-id="c318c-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="c318c-137">与第三方或外部组织共享；请参阅 [RCS 与外部组织共享电子申报 (ER) 配置](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="c318c-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![全局知识库中的派生内部统计 Contoso 配置版本](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="c318c-139">从全局存储库中删除配置</span><span class="sxs-lookup"><span data-stu-id="c318c-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="c318c-140">完成以下步骤，删除您的组织创建的配置。</span><span class="sxs-lookup"><span data-stu-id="c318c-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="c318c-141">在 **电子报告** 工作区中，确认您的配置提供程序是 **活动** 的。</span><span class="sxs-lookup"><span data-stu-id="c318c-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="c318c-142">有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="c318c-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="c318c-143">在活动的配置提供程序上，选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="c318c-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="c318c-144">选择存储库类型 **全局**，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="c318c-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="c318c-145">在 **筛选器** 快速选项卡上，使用 **筛选器** 功能找到要删除的配置。</span><span class="sxs-lookup"><span data-stu-id="c318c-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="c318c-146">在 **版本** 快速选项卡上，选择要删除的配置版本，然后选择 **删除**：</span><span class="sxs-lookup"><span data-stu-id="c318c-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![从全局存储库中删除配置](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="c318c-148">在配置消息框中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="c318c-148">In the confirmation message box, select **Yes**.</span></span>

    ![删除配置版本确认消息](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="c318c-150">配置版本已删除，并显示确认消息。</span><span class="sxs-lookup"><span data-stu-id="c318c-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="c318c-151">配置只能由创建配置的配置提供程序删除。</span><span class="sxs-lookup"><span data-stu-id="c318c-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="c318c-152">如果配置已与另一个组织共享，在删除配置之前，需要取消共享配置。</span><span class="sxs-lookup"><span data-stu-id="c318c-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 
