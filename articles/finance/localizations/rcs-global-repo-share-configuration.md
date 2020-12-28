---
title: 与外部组织共享 RCS/全局知识库中的 ER 配置
description: 此主题介绍如何直接与外部组织共享 Microsoft Regulatory Configuration Services (RCS)/全局知识库中的电子申报 (ER) 配置。
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
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
ms.openlocfilehash: 04c46824123906eccbfff18a03974c8043729e0a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440814"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="a13ce-103">直接与外部组织共享 Regulatory Configuration Services (RCS) 全局知识库中的电子申报 (ER) 配置</span><span class="sxs-lookup"><span data-stu-id="a13ce-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a13ce-104">可使用 Microsoft Regulatory Configuration Services (RCS) 共享电子申报 (ER) 配置，然后将其发布到外部组织。</span><span class="sxs-lookup"><span data-stu-id="a13ce-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="a13ce-105">以下过程介绍 RCS 用户如何与外部组织共享已在 RCS 实例中配置的 ER 配置版本。</span><span class="sxs-lookup"><span data-stu-id="a13ce-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="a13ce-106">必须先满足以下先决条件，才能完成这些过程：</span><span class="sxs-lookup"><span data-stu-id="a13ce-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="a13ce-107">访问 RCS 实例。</span><span class="sxs-lookup"><span data-stu-id="a13ce-107">Access an RCS instance.</span></span>
- <span data-ttu-id="a13ce-108">创建有效配置提供程序。</span><span class="sxs-lookup"><span data-stu-id="a13ce-108">Create an active configuration provider.</span></span> <span data-ttu-id="a13ce-109">有关详细信息，请参阅[创建配置提供程序并将其标记为有效](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)。</span><span class="sxs-lookup"><span data-stu-id="a13ce-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="a13ce-110">新建并上传 ER 配置版本。</span><span class="sxs-lookup"><span data-stu-id="a13ce-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="a13ce-111">有关详细信息，请参阅[新建和上传电子申报 (ER) 配置版本](rcs-global-repo-upload.md)。</span><span class="sxs-lookup"><span data-stu-id="a13ce-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="a13ce-112">还必须确保为公司预配 RCS 环境。</span><span class="sxs-lookup"><span data-stu-id="a13ce-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="a13ce-113">在 Finance and Operations 应用中，转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="a13ce-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="a13ce-114">如果没有为公司预配 RCS 环境，请选择 **Regulatory services – 配置外部**，然后按照说明预配一个。</span><span class="sxs-lookup"><span data-stu-id="a13ce-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="a13ce-115">如果已经为公司预配了 RCS 环境，请通过选择登录选项使用页面 URL 访问该环境。</span><span class="sxs-lookup"><span data-stu-id="a13ce-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="a13ce-116">验证要共享的配置</span><span class="sxs-lookup"><span data-stu-id="a13ce-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="a13ce-117">执行以下步骤验证是否已将要共享的配置上传到了全局知识库。</span><span class="sxs-lookup"><span data-stu-id="a13ce-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="a13ce-118">在 **电子申报** 工作区中，选择配置提供程序的 **知识库**。</span><span class="sxs-lookup"><span data-stu-id="a13ce-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![配置提供程序](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="a13ce-120">选择 **全局知识库**\>**打开**。</span><span class="sxs-lookup"><span data-stu-id="a13ce-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="a13ce-121">搜索要共享的配置。</span><span class="sxs-lookup"><span data-stu-id="a13ce-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="a13ce-122">可以使用筛选器字段缩小搜索范围。</span><span class="sxs-lookup"><span data-stu-id="a13ce-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="a13ce-123">如果在全局知识库中找不到此配置，请执行[新建和上传电子申报 (ER) 配置版本](rcs-global-repo-upload.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="a13ce-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="a13ce-124">与外部组织共享 ER 配置</span><span class="sxs-lookup"><span data-stu-id="a13ce-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="a13ce-125">在配置提供程序下创建了配置之后，可以通过使用 **全局配置知识库** 页中的 **共享对象** 快速选项卡直接与外部组织共享。</span><span class="sxs-lookup"><span data-stu-id="a13ce-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="a13ce-126">在 **电子申报** 工作区中，选择配置提供程序的 **知识库**。</span><span class="sxs-lookup"><span data-stu-id="a13ce-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="a13ce-127">选择 **全局知识库**\>**打开**。</span><span class="sxs-lookup"><span data-stu-id="a13ce-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="a13ce-128">选择要共享的配置。</span><span class="sxs-lookup"><span data-stu-id="a13ce-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="a13ce-129">在 **共享对象** 快速选项卡上，选择 **组织**。</span><span class="sxs-lookup"><span data-stu-id="a13ce-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![“共享对象”快速选项卡](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="a13ce-131">在此对话框中，输入外部组织的域名，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a13ce-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![“与外部组织共享配置版本”对话框](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="a13ce-133">将与外部组织共享配置，并在全局知识库中提供给该组织。</span><span class="sxs-lookup"><span data-stu-id="a13ce-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="a13ce-134">可以在这里将其导入到组织的 RCS 实例中或其 Finance and Operations 应用实例中。</span><span class="sxs-lookup"><span data-stu-id="a13ce-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

![与外部组织共享的配置](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_test.com)

6. <span data-ttu-id="a13ce-136">若要取消更新之前已经与外部组织共享的配置，请选择该配置，然后单击 **取消更新**，再选择 **确定**</span><span class="sxs-lookup"><span data-stu-id="a13ce-136">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>
