---
title: 在 RCS 中创建 ER 配置并上传到全局知识库
description: 此主题介绍如何在 Microsoft Regulatory Configuration Services (RCS) 中创建电子申报 (ER) 配置并上传到全局知识库。
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371233"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="f7da8-103">在 Regulatory Configuration Service (RCS) 中创建 ER 配置并上传到全局知识库</span><span class="sxs-lookup"><span data-stu-id="f7da8-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7da8-104">可使用 Microsoft Regulatory Configuration Services (RCS) 设计电子申报 (ER) 配置，然后发布，使其可在您的组织中使用。</span><span class="sxs-lookup"><span data-stu-id="f7da8-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="f7da8-105">以下过程介绍系统管理员或电子申报开发人员角色的用户如何创建已经在 RCS 实例中配置的 ER 配置的派生版本，然后将派生配置上传到全局知识库。</span><span class="sxs-lookup"><span data-stu-id="f7da8-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="f7da8-106">必须先满足以下先决条件，才能完成这些过程：</span><span class="sxs-lookup"><span data-stu-id="f7da8-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="f7da8-107">访问 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="f7da8-107">Access an RCS instance.</span></span>
- <span data-ttu-id="f7da8-108">创建有效配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="f7da8-108">Create an active configuration provider.</span></span> <span data-ttu-id="f7da8-109">有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="f7da8-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="f7da8-110">还必须确保为公司预配 RCS 环境。</span><span class="sxs-lookup"><span data-stu-id="f7da8-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="f7da8-111">在 Finance and Operations 应用中，转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="f7da8-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f7da8-112">如果没有为公司预配 RCS 环境，请选择 **Regulatory services – 配置外部**，然后按照说明预配一个。</span><span class="sxs-lookup"><span data-stu-id="f7da8-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="f7da8-113">如果已经为公司预配了 RCS 环境，请通过选择登录选项使用页面 URL 访问该环境。</span><span class="sxs-lookup"><span data-stu-id="f7da8-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="f7da8-114">在 RCS 中创建配置的派生版本</span><span class="sxs-lookup"><span data-stu-id="f7da8-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="f7da8-115">在**电子申报**工作区中，验证您是否有组织的有效配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="f7da8-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="f7da8-116">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="f7da8-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="f7da8-117">选择新版本的派生来源配置。</span><span class="sxs-lookup"><span data-stu-id="f7da8-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="f7da8-118">可以使用上面的筛选器字段缩小搜索范围。</span><span class="sxs-lookup"><span data-stu-id="f7da8-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="f7da8-119">选择**创建配置** \> **从名称派生**。</span><span class="sxs-lookup"><span data-stu-id="f7da8-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="f7da8-120">输入名称和说明，然后选择**创建配置**创建新的派生版本。</span><span class="sxs-lookup"><span data-stu-id="f7da8-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="f7da8-121">选择新派生的配置，添加版本说明，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f7da8-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="f7da8-122">配置的状态将更改为**已完成**。</span><span class="sxs-lookup"><span data-stu-id="f7da8-122">The status of the configuration to is changed to **Completed**.</span></span>

![RCS 中的新配置版本](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="f7da8-124">更改配置状态之后，可能会收到与相连应用程序有关的验证错误消息。</span><span class="sxs-lookup"><span data-stu-id="f7da8-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="f7da8-125">若要关闭验证，请在操作窗格上的**配置**选项卡中，选择**用户参数**，然后将**配置状态更改时跳过验证并重定基本值**选项设置为**是**</span><span class="sxs-lookup"><span data-stu-id="f7da8-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="f7da8-126">将配置上传到全局知识库</span><span class="sxs-lookup"><span data-stu-id="f7da8-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="f7da8-127">若要与组织共享新配置或派生配置，可以将其上传到全局知识库。</span><span class="sxs-lookup"><span data-stu-id="f7da8-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="f7da8-128">选择配置的已完成版本，然后选择**上传到知识库中**。</span><span class="sxs-lookup"><span data-stu-id="f7da8-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="f7da8-129">选择**全局 (Microsoft)** 选项，然后选择**上传**。</span><span class="sxs-lookup"><span data-stu-id="f7da8-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![“上传到知识库中”选项](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="f7da8-131">在配置消息框中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="f7da8-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="f7da8-132">按照需要更新版本说明，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="f7da8-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="f7da8-133">配置状态将更新为**共享**，并将配置上传到全局知识库中。</span><span class="sxs-lookup"><span data-stu-id="f7da8-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="f7da8-134">可以在此处按照下面的方法进行处理：</span><span class="sxs-lookup"><span data-stu-id="f7da8-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="f7da8-135">将其导入到您的 Dynamics 365 实例中。</span><span class="sxs-lookup"><span data-stu-id="f7da8-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="f7da8-136">有关详细信息，请参阅 [(ER) 从 RCS 导入配置](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)。</span><span class="sxs-lookup"><span data-stu-id="f7da8-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="f7da8-137">与第三方或外部组织共享；请参阅 [RCS 与外部组织共享电子申报 (ER) 配置](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="f7da8-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![全局知识库中的派生内部统计 Contoso 配置版本](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
