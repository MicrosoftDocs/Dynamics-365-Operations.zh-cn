---
title: Regression Suite Automation Tool 设置和安装教程
description: 本主题是演示如何设置和安装 Regression Suite Automation Tool (RSAT) 的教程。
author: robinarh
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: ca1e0d61263ed19e7eab18f6ba6aec628b0295a8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568403"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="0bb3a-103">Regression Suite Automation Tool 设置和安装教程</span><span class="sxs-lookup"><span data-stu-id="0bb3a-103">Set up and install Regression suite automation tool tutorial</span></span>

<span data-ttu-id="0bb3a-104">本主题是帮助您设置和开始使用 RSAT 以及与使用 RSAT 有关的工具的教程。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="0bb3a-105">可使用 Internet 浏览器工具下载此页并以 PDF 格式保存。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-105">Use your internet browser tools to download and save this page in PDF format.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="0bb3a-106">重要概念</span><span class="sxs-lookup"><span data-stu-id="0bb3a-106">Key concepts</span></span>

- <span data-ttu-id="0bb3a-107">了解支持 Regression Suite Automation Tool (RSAT) 的各种应用程序所需的安装和先决条件设置。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="0bb3a-108">了解如何使用任务录制器功能和 Microsoft Dynamics Lifecycle Services (LCS) 与 Microsoft Azure DevOps 创建、配置、运行、调查和报告测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="0bb3a-109">让功能用户可以通过使用任务录制器录制业务任务，然后将任务录制转换为一套自动化测试，而不必编写源代码。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0bb3a-110">开始之前</span><span class="sxs-lookup"><span data-stu-id="0bb3a-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0bb3a-111">先决条件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-111">Prerequisites</span></span>

- <span data-ttu-id="0bb3a-112">此教程需要运行 Microsoft Dynamics 365 for Finance and Operations 版本 10.0（2019 年 4 月）或更高版本的环境。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="0bb3a-113">也支持运行 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 平台更新 20 (PU20) 或更高版本的客户。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="0bb3a-114">用户必须具有环境的管理员权限。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="0bb3a-115">您必须有权访问客户租户 LCS 和 Azure DevOps（以前称为 Microsoft Visual Studio Team Services \[VSTS\]）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="0bb3a-116">要创建和管理测试套件的用户必须拥有 Azure DevOps 测试计划或测试管理许可证。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="0bb3a-117">以下许可证也为您提供测试计划的访问权限：</span><span class="sxs-lookup"><span data-stu-id="0bb3a-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="0bb3a-118">Visual Studio Enterprise 许可证</span><span class="sxs-lookup"><span data-stu-id="0bb3a-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="0bb3a-119">Visual Studio Test Professional 许可证</span><span class="sxs-lookup"><span data-stu-id="0bb3a-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="0bb3a-120">MSDN 平台订户许可证</span><span class="sxs-lookup"><span data-stu-id="0bb3a-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="0bb3a-121">RSAT 必须可以通过 Web 浏览器访问测试环境。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="0bb3a-122">若要生成和编辑测试参数，必须安装 Microsoft Excel。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="0bb3a-123">配置 Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="0bb3a-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="0bb3a-124">用户资格</span><span class="sxs-lookup"><span data-stu-id="0bb3a-124">User eligibility</span></span>

<span data-ttu-id="0bb3a-125">确保在 Azure DevOps 中创建用户，并且该用户具有可访问 Azure 测试计划的订阅级别。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="0bb3a-126">仅当用户需要创建和管理测试用例，才需要 Azure DevOps 测试计划许可证号（即并非所有 RSAT 用户都需要此许可证）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="0bb3a-127">有关许可证要求的信息，请参阅[许可证要求](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements)。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="0bb3a-128">创建新 Azure DevOps 项目</span><span class="sxs-lookup"><span data-stu-id="0bb3a-128">Create a new Azure DevOps project</span></span>

<span data-ttu-id="0bb3a-129">RSAT 对测试用例使用 Azure Devops，以及测试套件管理，报告和调查测试的运行结果。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span>

> [!NOTE]
> <span data-ttu-id="0bb3a-130">可使用现有 Azure DevOps 项目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="0bb3a-131">但是，如果已设置的现有 Azure DevOps 项目具有自定义模板，则将业务流程建模器 (BPM) 的测试用例同步到 Azure DevOps 时，会收到“VSTS 同步失败”错误（请参阅[测试从 BPM 到 Azure DevOps 的同步](#test-the-synchronization-from-bpm-to-azure-devops)部分）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="0bb3a-132">如果已经为该自定义模板实施了以下最佳实践，则可以将测试用例同步到 Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="0bb3a-133">（错误消息中列出了这些最佳实践。）</span><span class="sxs-lookup"><span data-stu-id="0bb3a-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="0bb3a-134">请勿删除任何工作项类型或现成字段。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="0bb3a-135">请勿删除任何工作项类型状态。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="0bb3a-136">请勿将任何必填字段添加到工作项类型。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-136">Do not add any required fields to a work item type.</span></span>

![包含最佳实践列表的错误消息](./media/setup_rsa_tool_02.png)

<span data-ttu-id="0bb3a-138">否则，对于本教程，建议新建 Azure DevOps 项目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="0bb3a-139">有关详细信息，请参阅[使用自定义 Azure DevOps (VSTS) 流程模板同步到 BPM 时的问题](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/)。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="0bb3a-140">打开 Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`)。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="0bb3a-141">选择 Azure DevOps 页中右上角的 **创建项目**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![“创建项目”按钮](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="0bb3a-143">填写以下字段，然后选择 **创建**：</span><span class="sxs-lookup"><span data-stu-id="0bb3a-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="0bb3a-144">**项目名称**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-144">**Project name**</span></span>
    - <span data-ttu-id="0bb3a-145">**版本控制** – 选择 **Team Foundation 版本控制**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="0bb3a-146">请注意，不支持默认消息 **Git**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="0bb3a-147">**工作项流程**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-147">**Work item process**</span></span>

    ![“新建项目”对话框](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="0bb3a-149">创建个人访问令牌</span><span class="sxs-lookup"><span data-stu-id="0bb3a-149">Create a personal access token</span></span>

<span data-ttu-id="0bb3a-150">本教程中，将使用 LCS 业务流程建模器 (BPM) 创建测试用例库，并将测试用例与 Azure DevOps 同步。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="0bb3a-151">需要个人访问令牌才能将 BPM 与 Azure DevOps 同步。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="0bb3a-152">选择您的 Azure DevOps 项目的页面右上角中的配置文件图标，然后选择 **安全**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![“安全”命令](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="0bb3a-154">在左窗格中 **安全** 下，选择 **个人访问令牌**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="0bb3a-155">然后选择 **新建令牌**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-155">Then select **New Token**.</span></span>

    ![“用户”设置中“个人访问令牌”选项卡上的“新建令牌”按钮](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="0bb3a-157">填写以下字段，然后选择 **创建**：</span><span class="sxs-lookup"><span data-stu-id="0bb3a-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="0bb3a-158">**姓名**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-158">**Name**</span></span>
    - <span data-ttu-id="0bb3a-159">**到期 (UTC)** – 选择 **自定义**，然后使用日期选取器选择上一个可用日期。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="0bb3a-160">**范围** – 选择 **完全访问权限** 选项。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-160">**Scopes** – Select the **Full access** option.</span></span>

    ![“新建个人访问令牌”对话框](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="0bb3a-162">记下创建的个人访问令牌。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="0bb3a-163">后面设置 RSAT 配置时需要。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![个人访问令牌](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="0bb3a-165">配置 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="0bb3a-165">Configure the LCS project</span></span>

<span data-ttu-id="0bb3a-166">您的主测试库需要 Lifecycle Services (LCS) 项目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="0bb3a-167">LCS 业务流程建模器 (BPM) 用作您的测试用例的主库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="0bb3a-168">BPM 用于为 LCS 项目管理和分发测试库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="0bb3a-169">例如，构建测试库的 Microsoft 合作伙伴或独立软件供应商 (ISV) 将以 BPM 库的形式发布测试案例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="0bb3a-170">在 BPM 中，测试用例由业务流程组织。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="0bb3a-171">BPM 不定义测试经过的执行顺序或频率。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="0bb3a-172">这些详细信息在 Azure DevOps 中管理，如本主题后文所述。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="0bb3a-173">对于 LCS 项目，可使用现有客户实施或合作伙伴项目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="0bb3a-174">更新 LCS 语言</span><span class="sxs-lookup"><span data-stu-id="0bb3a-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="0bb3a-175">要让用户界面 (UI) 正确显示业务流程，必须将 LCS 首选语言设置为 **语言(美国)**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="0bb3a-176">转到 LCS 实施项目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="0bb3a-177">选择页面右上角的 **设置** 按钮（齿轮符号），然后选择 **语言首选项**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![更新语言首选项](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="0bb3a-179">在 **首选语言** 字段中，选择 **英语 (美国)**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![“用户设置”中的“语言首选项”选项卡](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="0bb3a-181">配置 LCS 以连接到 Azure DevOps 项目</span><span class="sxs-lookup"><span data-stu-id="0bb3a-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="0bb3a-182">如果前面新建了 Azure DevOps 项目，请配置 LCS 项目以连接到新建的这个项目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="0bb3a-183">否则，如果已将您的 LCS 项目连接到了 Azure DevOps 项目，则可继续到下一部分。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="0bb3a-184">转到 LCS 实施项目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="0bb3a-185">选择 **菜单** 按钮，然后选择 **项目设置**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![“项目设置”命令](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="0bb3a-187">在左窗格中，选择 **Visual Studio Team Services**，然后选择 **设置 Visual Studio Team Services**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![“项目设置”中的“Visual Studio Team Services”选项卡](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="0bb3a-189">在 **Azure DevOps 站点 URL** 字段中，输入 Azure DevOps 站点的 URL。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="0bb3a-190">在 **个人访问令牌** 字段中，输入之前创建的个人访问令牌。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-191">尽管 VSTS 现在称为 Azure DevOps，要将 LCS 连接到 Azure DevOps 项目，请使用原来的 URL。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="0bb3a-192">例如，本教程中使用的 Azure DevOps URL 为 `https://dev.azure.com/D365FOFastTrack/`。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="0bb3a-193">但是，下图中输入的是 `https://D365FOFastTrack.visualstudio.com/`。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![“设置 Visual Studio Team Services”中的步骤 1](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="0bb3a-195">选择 **继续**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-195">Select **Continue**.</span></span>
6. <span data-ttu-id="0bb3a-196">在 **Visual Studio Team Services 项目** 字段中，在所选站点上选择要与 LCS 项目链接的 VSTS 项目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="0bb3a-197">默认情况下，**流程模板** 字段设置为 **Agile**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="0bb3a-198">对于自定义模板，请参阅[新建 Azure DevOps 项目](#create-a-new-azure-devops-project)部分中的最佳实践指南。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="0bb3a-199">然后选择 **继续**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-199">Then select **Continue**.</span></span>

    ![“设置 Visual Studio Team Services”中的步骤 2](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="0bb3a-201">检查设置，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-201">Review your settings, and then select **Save**.</span></span>

    ![“设置 Visual Studio Team Services”中的步骤 3](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="0bb3a-203">选择 **授权** 为 LCS 授予代表您访问所配置 Azure DevOps 站点的权限，以便开启与 VSTS 集成的功能。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![“授权”按钮](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="0bb3a-205">将显示一个消息框，其中说明“您即将重定向到外部站点以授权 LCS 代表您连接到 Visual Studio Team Services。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="0bb3a-206">是否要继续？”</span><span class="sxs-lookup"><span data-stu-id="0bb3a-206">Proceed?"</span></span> <span data-ttu-id="0bb3a-207">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-207">Select **Yes**.</span></span>

    ![消息框](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="0bb3a-209">选择 **接受**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-209">Select **Accept**.</span></span>

    ![授予访问权限](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="0bb3a-211">如果已为您授予用户权限，则 UI 应该会让您回到 LCS 项目设置页。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![授权用户](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="0bb3a-213">创建新的 BPM 库</span><span class="sxs-lookup"><span data-stu-id="0bb3a-213">Create a new BPM library</span></span>

1. <span data-ttu-id="0bb3a-214">转到 LCS 实施项目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="0bb3a-215">选择 **菜单** 按钮，然后选择 **业务流程建模器**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![“业务流程建模器”命令](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="0bb3a-217">选择 **新建库**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-217">Select **New library**.</span></span>

    ![“新建库”按钮](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="0bb3a-219">在 **库名** 字段中，输入名称，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="0bb3a-220">对于本教程，请将 BPM 库命名为 **RSAT**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![“新建库”对话框](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="0bb3a-222">打开新的 **RSAT** BPM 库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="0bb3a-223">选择 **示例核心业务流程** 流程，然后选择右侧的 **编辑模式**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![“编辑模式”按钮](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="0bb3a-225">将 **名称** 字段和 **说明** 字段的值更改为 **创建产品**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="0bb3a-226">然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-226">Then select **Save**.</span></span>

    ![“名称”和“说明”字段](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="0bb3a-228">环境</span><span class="sxs-lookup"><span data-stu-id="0bb3a-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="0bb3a-229">版本要求</span><span class="sxs-lookup"><span data-stu-id="0bb3a-229">Version requirement</span></span>

<span data-ttu-id="0bb3a-230">需要运行版本 10 的测试或沙盒环境。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="0bb3a-231">也支持运行版本 7.3 平台更新 20 或更高版本的客户。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="0bb3a-232">RSAT 必须可以通过 Web 浏览器访问测试环境。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="0bb3a-233">用户条件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-233">User criteria</span></span>

<span data-ttu-id="0bb3a-234">用户必须具有此环境的管理员权限。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="0bb3a-235">设置“帮助”设置以连接 LCS</span><span class="sxs-lookup"><span data-stu-id="0bb3a-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="0bb3a-236">需要执行此步骤才能与 LCS 连接，这样就可以通过客户端将任务录制保存到 LCS 中的相应 BPM 库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="0bb3a-237">打开客户端。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-237">Open the client.</span></span>
2. <span data-ttu-id="0bb3a-238">转到 **系统管理 \> 设置 \> 系统参数**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="0bb3a-239">在 **帮助** 选项卡上的 **Lifecycle Services 帮助配置** 字段中，选择相关 LCS 项目（本教程中为 **RSAT**）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![“帮助”选项卡上的“Lifecycle Services 帮助配置”字段](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="0bb3a-241">将在相应 LCS 项目下填写 BPM 库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="0bb3a-242">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-242">Select **Save**.</span></span>
5. <span data-ttu-id="0bb3a-243">可能必须刷新浏览器才能查看更新后的帮助内容。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![有关刷新浏览器的通知](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="0bb3a-245">任务录制</span><span class="sxs-lookup"><span data-stu-id="0bb3a-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="0bb3a-246">确保在主仪表板上启动您的所有任务录制。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="0bb3a-247">让各录制简短，并注重一个业务任务，如创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="0bb3a-248">创建任务录制并保存到 BPM 库</span><span class="sxs-lookup"><span data-stu-id="0bb3a-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="0bb3a-249">创建一个相应任务录制，可将其附加到在新的 BPM 库中创建的简单业务流程。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="0bb3a-250">打开客户端。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-250">Open the client.</span></span>
2. <span data-ttu-id="0bb3a-251">在主仪表板上，选择 **设置** 按钮（齿轮符号），然后选择 **任务录制器**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![在“设置”菜单上选择“任务录制器”](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="0bb3a-253">选择 **创建录制**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-253">Select **Create recording**.</span></span>

    ![“创建录制”按钮](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="0bb3a-255">填写 **记录名称** 和 **记录说明** 字段，然后选择 **开始**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![“录制名称”和“录制说明”字段](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="0bb3a-257">录制用于创建产品的步骤。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-257">Record the steps for creating a product.</span></span> <span data-ttu-id="0bb3a-258">完成后，选择 **停止** 以停止录制。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![用于创建产品的步骤](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="0bb3a-260">选择 **保存到 Lifecycle Services**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-260">Select **Save to Lifecycle Services**.</span></span>

    ![将任务录制保存到 Lifecycle Services](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="0bb3a-262">将从 LCS 加载库信息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-262">Library information is loaded from LCS.</span></span>

    ![加载库信息](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="0bb3a-264">选择要与任务录制关联的 BPM 库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="0bb3a-265">对于本教程，请选择之前创建的 **RSAT** BPM 库及其下的 **创建产品** 业务流程。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="0bb3a-266">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-266">Then select **OK**.</span></span>

    ![将任务录制与 BPM 库和业务流程关联](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="0bb3a-268">将显示“保存到 Lifecycle Services 已成功”消息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![有关成功保存到 LCS 的消息](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="0bb3a-270">如果要在本地保存任务录制，然后通过 LCS 上载到 BPM，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0bb3a-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="0bb3a-271">完成录制后，选择 **保存到此 PC**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![保存到此 PC](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="0bb3a-273">在浏览器的通知栏中，选择 **保存** 或 **另存为**，将文件保存到您的本地计算机上。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![通知栏](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="0bb3a-275">转到 **RSAT** BPM 库，然后选择要针对其保存任务录制的业务流程。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="0bb3a-276">在 **概述** 选项卡上，选择 **上载**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-276">On the **Overview** tab, select **Upload**.</span></span>

        ![“上载”按钮](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="0bb3a-278">选择 **浏览**，然后选择之前保存的 .axtr 文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="0bb3a-279">然后选择 **上载**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-279">Then select **Upload**.</span></span>

        ![选择要上载的 .axtr 文件](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="0bb3a-281">测试从 BPM 到 Azure DevOps 的同步</span><span class="sxs-lookup"><span data-stu-id="0bb3a-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="0bb3a-282">由于已向此业务流程附加了任务录制，所以必须验证是否可使用 LCS 中的 VSTS 同步功能将业务流程和关联的任务录制（分别）作为功能和测试用例同步到 Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="0bb3a-283">Azure DevOps 中创建的相应工作项类型取决于您在按照[新建 Azure DevOps 项目](#create-a-new-azure-devops-project)部分中的说明使用 Azure DevOps 配置 LCS 项目时选择的流程模板。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="0bb3a-284">转到 BPM 库，然后打开之前创建的 **RSAT** 库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="0bb3a-285">选择省略号按钮 (**...**)，然后选择 **VSTS 同步**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![省略号菜单中的“VSTS 同步”命令](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="0bb3a-287">完成 VSTS 同步之后，左侧将显示 **要求** 选项卡，其中包含相应 Azure DevOps 工作项。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-288">Azure DevOps 中创建的工作项采用 BPM 库名称充当标题前缀。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![“要求”选项卡](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="0bb3a-290">刷新该页面。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-290">Refresh the page.</span></span>
4. <span data-ttu-id="0bb3a-291">选择省略号按钮 (**...**)。将再显示一个选项，即 **同步测试用例**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="0bb3a-292">选择此选项。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-292">Select this option.</span></span>

    ![省略号菜单中的“同步测试用例”命令](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="0bb3a-294">如果刷新页面之后 **同步测试用例** 选项不可用，请转到 BPM 的主页，然后为整个库本身选择 **同步测试用例**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="0bb3a-295">这样就可以有效地为整个库强制实施同步。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    >
    > ![为整个库选择同步测试用例](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="0bb3a-297">完成同步测试用例后，将在 **要求** 选项卡上新建一个测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![“要求”选项卡上的“新建测试用例”](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="0bb3a-299">转到 Azure DevOps 项目，然后选择 **面板 \> 工作项**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![“面板”下的“工作项”命令](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="0bb3a-301">验证是否存在通过 BPM 同步创建的工作项和测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![工作项和测试用例](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="0bb3a-303">安装和配置 RSAT</span><span class="sxs-lookup"><span data-stu-id="0bb3a-303">Install and Configure RSAT</span></span>

<span data-ttu-id="0bb3a-304">可将 RSAT 安装到运行 Windows 10 并可通过 Web 浏览器（Internet Explorer 或 Google Chrome）连接到环境的任何计算机上。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="0bb3a-305">安装此工具的新版本之前，建议卸载上一个版本。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="0bb3a-306">安装身份验证证书</span><span class="sxs-lookup"><span data-stu-id="0bb3a-306">Install an authentication certificate</span></span>

<span data-ttu-id="0bb3a-307">若要启用身份验证，必须生成证书并安装到运行 RSAT 的同一台计算机上。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="0bb3a-308">生成证书</span><span class="sxs-lookup"><span data-stu-id="0bb3a-308">Generate a certificate</span></span>

1. <span data-ttu-id="0bb3a-309">若要生成证书文件，请以管理员身份打开一个 Microsoft Windows PowerShell 窗口，然后运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="0bb3a-310">通过在 **运行** 对话框中输入 **certlm.msc** 打开证书管理器，然后在 **个人 \> 证书** 下确认创建的 **D365 Automated 测试证书** 证书。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-311">务必输入 **certlm.msc**，不要输入 **certmgr.msc**，因为证书存储在本地计算机上。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![“D365 Automated 测试证书”证书](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="0bb3a-313">右键单击证书，然后选择 **复制**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="0bb3a-314">转到 **可信根证书主管机构 \> 证书**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![“可信根证书主管机构”文件夹下的“证书”文件夹](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="0bb3a-316">在 **操作** 菜单上，选择 **粘贴** 将证书复制到 **可信根证书主管机构** 位置。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![“操作”菜单上的“粘贴”命令](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="0bb3a-318">若要获取所安装证书的指纹，但是不包含空间或特殊字符，请以管理员身份打开一个 Windows PowerShell 窗口，然后运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="0bb3a-319">保存指纹，因为后面更新应用程序对象服务器 (AOS) 的 .wif 文件和设置 RSAT 配置时需要指纹。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="0bb3a-320">将 AOS 计算机配置为信任连接</span><span class="sxs-lookup"><span data-stu-id="0bb3a-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="0bb3a-321">如果环境是二级以上环境，则必须在 wif.config 文件中为环境的 **所有** AOS 计算机更新证书指纹。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="0bb3a-322">建立与 AOS 计算机之间的远程桌面协议 (RDP) 连接。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="0bb3a-323">LCS 中的环境详细信息页中提供登录详细信息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="0bb3a-324">打开 Microsoft Internet 信息服务 (IIS)，然后在站点列表中找到 **AOSService**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![站点列表中的 AOSService](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="0bb3a-326">右键单击 **浏览** 以打开 **\<Drive\>: \\AosService\\WebRoot** 文件夹。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="0bb3a-327">找到 **wif.config** 文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-327">Find the **wif.config** file.</span></span>

    ![WebRoot 文件夹中的 Wif.config 文件](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="0bb3a-329">通过添加证书的新主管机构条目和主管机构名称，更新 **wif.config** 文件，如以下示例中所示。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="0bb3a-330">如果多个用户在使用同一个应用程序，则每个用户必须生成单独的指纹，并且必须将这些指纹全部添加到 **\<keys\>** 部分中。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="0bb3a-331">如果有多台 AOS 计算机，请对其他每台计算机重复执行步骤 3 到 4。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-332">与原来的二级环境不同，将为新的二级环境部署两个 AOS 实例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="0bb3a-333">在所有 AOS 计算机上运行 **iisreset**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-334">如果没有在一级计算机上运行 **iisreset** 的管理员权限，请在 LCS 中的“环境详细信息”页上，选择“维护 > 重新启动服务”。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="0bb3a-335">二级以上环境</span><span class="sxs-lookup"><span data-stu-id="0bb3a-335">Tier 2+ environment</span></span>

<span data-ttu-id="0bb3a-336">如果使用二级以上（标准接受度测试沙盒或更高）的环境，请在安装 RSAT 的计算机上验证或设置以下注册表设置。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="0bb3a-337">需要执行此步骤，是因为可以帮助您避免身份验证或 RSAT 连接错误。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="0bb3a-338">安装 RSAT</span><span class="sxs-lookup"><span data-stu-id="0bb3a-338">Install RSAT</span></span>

1. <span data-ttu-id="0bb3a-339">转到 <https://www.microsoft.com/download/details.aspx?id=57357>，然后选择 **下载**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="0bb3a-340">选择所有文件，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-340">Select all the files, and then select **Next**.</span></span>

    ![选择所有文件](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="0bb3a-342">双击 .msi 包运行安装程序。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="0bb3a-343">然后，在安装完成时，选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT 安装程序文件](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="0bb3a-345">安装 Selenium 和浏览器驱动程序</span><span class="sxs-lookup"><span data-stu-id="0bb3a-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="0bb3a-346">在 RSAT 的早期版本中，必须安装 Selenium 和浏览器驱动程序。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="0bb3a-347">因为这些驱动程序会自动安装，所以再也不必安装。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="0bb3a-348">首次打开 RSAT 时，将提示自动下载并安装 Selenium。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="0bb3a-349">有关详细信息，请参阅[配置 RSAT](#configure-rsat) 部分。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="0bb3a-350">将提示您自动下载并安装与 RSAT 配置中所选默认浏览器对应的浏览器驱动程序，之后才能运行测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="0bb3a-351">有关详细信息，请参阅[加载和运行测试用例](#load-and-run-test-cases)部分。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="0bb3a-352">开始使用 RSAT</span><span class="sxs-lookup"><span data-stu-id="0bb3a-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="0bb3a-353">创建测试计划和测试套件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="0bb3a-354">转到 Azure DevOps 项目，然后选择 **测试计划**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![“测试计划”命令](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="0bb3a-356">选择 **新建测试计划**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-356">Select **New Test Plan**.</span></span>

    ![“新建测试计划”按钮](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="0bb3a-358">填写 **名称** 字段，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="0bb3a-359">对于本教程，将测试计划命名为 **RSAT 测试计划**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![“新建测试计划”对话框](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="0bb3a-361">选择加号 (**+**)，然后选择 **静态套件** 在新测试计划下创建一个静态套件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="0bb3a-362">将这个新的测试套件命名为 **T01 – 制造到库存**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-363">如果希望将新测试用例从 BPM 自动提取到 RSAT 测试套件中，也可以创建基于查询的套件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![创建静态套件](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="0bb3a-365">将测试用例附加到测试套件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="0bb3a-366">选择右侧的 **添加现有** 将现有测试用例添加到测试套件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![“添加现有”按钮](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="0bb3a-368">在 **将测试用例添加到套件** 页上，选择 **运行查询**，然后选择要添加到测试套件的测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="0bb3a-369">对于本教程，请选择 **创建新产品** 测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="0bb3a-370">然后选择页面右下角的 **添加测试用例**（下图中未显示此按钮）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![“运行查询”按钮](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="0bb3a-372">将把测试用例添加到 **T01 - 制造到库存** 测试套件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![测试案例已添加到测试套件](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="0bb3a-374">配置 RSAT</span><span class="sxs-lookup"><span data-stu-id="0bb3a-374">Configure RSAT</span></span>

1. <span data-ttu-id="0bb3a-375">打开 RSAT。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-375">Open RSAT.</span></span>

    ![“RSAT”图标](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="0bb3a-377">将收到警告消息，说明“Regression Suite Automation Tool 需要 Selenium。是否要立即自动下载并安装？”。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="0bb3a-378">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-378">Select **Yes**.</span></span>

    ![Regression Suite Automation Tool 需要 Selenium 的警告消息](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="0bb3a-380">选择右上角的 **设置** 按钮（齿轮符号），然后填写显示的对话框中的以下字段：</span><span class="sxs-lookup"><span data-stu-id="0bb3a-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="0bb3a-381">**Azure DevOps Url** – 输入您的 Azure DevOps 项目的 URL，如 `https://yourAzureDevOpsUrlHere.visualStudio.com`。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="0bb3a-382">**访问令牌** – 输入用于将工具连接到 Azure DevOps 的访问令牌。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="0bb3a-383">使用本教程前面创建的个人访问令牌。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="0bb3a-384">有关详细信息，请参阅[使用个人访问令牌对访问进行身份验证](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate)。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="0bb3a-385">**项目名称** – 选择您的 Azure DevOps 项目的名称。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="0bb3a-386">**测试计划** – 选择其中包含您的测试用例的 Azure DevOps 测试计划。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="0bb3a-387">有关详细信息，请参阅[创建测试计划和测试套件](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan)。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="0bb3a-388">选择测试计划之后，选择 **测试连接** 以测试您与 Azure DevOps 之间的连接。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="0bb3a-389">**主机名** – 输入测试环境的主机名，如 **\<myaos\>.cloudax.dynamics.com**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="0bb3a-390">请勿在其中包含 **https://** 或 **http://** 前缀。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="0bb3a-391">**SOAP 主机名** – 输入测试环境的 SOAP 主机名。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="0bb3a-392">SOAP 主机名通常与主机名相同，但带有 **soap** 后缀。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="0bb3a-393">下面是示例：**\<myaos\>soap.cloudax.dynamics.com**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="0bb3a-394">请勿在其中包含 **https://** 或 **http://** 前缀。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0bb3a-395">若要查找主机名和 SOAP 主机名，请打开 IIS 管理器，右键单击 **站点 \> AOSService**，然后选择 **编辑绑定**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="0bb3a-396">**主机名** 列中的值提供主机名和 SOAP 主机名（在 URL 中，SOAP 主机名带有后缀 **soap**）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![“主机名”列中的主机名和 SOAP 主机名](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="0bb3a-398">**管理员用户名** – 输入测试环境中的管理员用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="0bb3a-399">**指纹** – 按照本教程前面的说明输入身份验证证书的指纹。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="0bb3a-400">**工作目录** – 指定用于存储测试自动化文件（如 Excel 测试数据文件）的文件夹位置。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="0bb3a-401">例如，输入或选择 **C:\\Temp\\RegressionTool**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0bb3a-402">如果文件夹名称中有空格，则执行将失败，因为找不到该文件夹。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="0bb3a-403">这是已知问题，应该会在该工具的最新版本中解决。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="0bb3a-404">**默认浏览器** – 选择 **Internet Explorer** 或 **Google Chrome**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="0bb3a-405">确保已安装相应的浏览器驱动程序。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="0bb3a-406">**测试运行超时** – 为测试运行指定超时时间段（以分钟为单位）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="0bb3a-407">超时时间段耗尽后，将关闭所有活动窗口，而暂挂的测试用例将失败。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="0bb3a-408">**测试操作超时** – 此字段控制 Finance and Operation 环境服务器请求的超时时间段（以分钟为单位）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="0bb3a-409">默认值（2 分钟）通常应该就足够。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="0bb3a-410">但是，对于较慢的环境，如果发生了与超时有关的错误，可能需要增加该值。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="0bb3a-411">**公司名称** – 输入在创建 Excel 参数文件时要用作默认公司的公司名称。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="0bb3a-412">以后可通过编辑 Excel 参数文件更改公司。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![“设置”对话框](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="0bb3a-414">选择 **应用** 以应用和保存您的设置。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="0bb3a-415">若要将当前设置保存到计算机上的配置文件，请选择 **另存为**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="0bb3a-416">若要从计算机上的配置文件还原设置，请选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="0bb3a-417">选择 **关闭** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="0bb3a-418">加载和运行测试用例</span><span class="sxs-lookup"><span data-stu-id="0bb3a-418">Load and run test cases</span></span>

1. <span data-ttu-id="0bb3a-419">选择 **加载** 从 Azure DevOps 项目加载 **RSAT 测试计划** 测试计划。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![“加载”按钮](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="0bb3a-421">从测试套件选择 **创建新产品** 测试用例，然后选择 **新建 \> 生成测试执行和参数文件**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![“新建”菜单上的“生成测试执行和参数文件”命令](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="0bb3a-423">将在您在 RSAT 配置中指定的本地文件夹（如 **C:\\Temp\\RegressionTool**）内创建 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![已创建 Excel 参数文件](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="0bb3a-425">如果要保存参数文件，请选择 **上载**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="0bb3a-426">将把选择的所有测试用例的测试自动化文件上载到 Azure DevOps 供将来使用。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="0bb3a-427">（这些文件包括 Excel 测试参数文件。）</span><span class="sxs-lookup"><span data-stu-id="0bb3a-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="0bb3a-428">这样就可以选择 **加载** 直接从 Azure DevOps 加载测试用例中的参数文件（和自动化文件）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="0bb3a-429">不必重新生成参数文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="0bb3a-430">以后要保留参数文件中的修改，不希望覆盖时，此方法会变得非常重要。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="0bb3a-431">若要验证是否已将自动化文件和参数文件保存到了 Azure DevOps，请转到 Azure DevOps 项目，选择 **面板 \> 工作项**，然后选择 **创建新产品** 测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="0bb3a-432">在 **附件** 选项卡上，应该可以看到四个文件：</span><span class="sxs-lookup"><span data-stu-id="0bb3a-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="0bb3a-433">**.cs** – C\# 自动化文件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="0bb3a-434">**.dll** – 已编译为程序集的自动化文件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="0bb3a-435">**.xlsx** – Excel 参数文件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="0bb3a-436">**.xml** – 录制文件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-436">**.xml** – Recording file</span></span>

    ![“附件”选项卡上的文件](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="0bb3a-438">选择要运行的测试用例，然后选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-439">如果浏览器使用的是 Internet Explorer，请在运行测试用例之前，确保 **Windows 显示设置 \> 比例和布局** 中的桌面分辨率设置为 **100%**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="0bb3a-440">如果无法在虚拟机 (VM) 中更改此设置，请在用于访问该 VM 的客户端（笔记本电脑）上更改。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="0bb3a-441">然后，VM 显示设置将继承这些分辨率设置。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![桌面分辨率设置为 100%](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="0bb3a-443">如果系统中未安装浏览器驱动程序，将收到警告消息，说明“此操作需要 \<browser name\> 驱动程序。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="0bb3a-444">是否要立即自动下载并安装？“</span><span class="sxs-lookup"><span data-stu-id="0bb3a-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="0bb3a-445">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-445">Select **Yes**.</span></span>

    ![Internet Explorer 的警告消息](./media/setup_rsa_tool_69.png)

    ![Chrome 的警告消息](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="0bb3a-448">如果使用 Chrome 充当浏览器和接收说明因为 Chrome 版本不正确而未创建会话的错误消息，从 <http://chromedriver.chromium.org/downloads> 将最新 Chrome 驱动程序下载到 **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** 文件夹。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Chrome 的错误消息](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="0bb3a-450">将运行测试用例，并更新 **结果** 字段。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-450">The test case is run, and the **Result** field is updated.</span></span>

    ![更新的结果字段](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="0bb3a-452">如果已按照本教程的内容进行了操作，则 **创建新产品** 测试用例将失败，因为用于创建产品的任务录制将产品名另存为了硬编码的值。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="0bb3a-453">如果重新运行同一个测试用例，则应该会收到错误消息，因为已存在该产品。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![“结果”字段已设置为“失败”](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="0bb3a-455">查看测试结果</span><span class="sxs-lookup"><span data-stu-id="0bb3a-455">View the test results</span></span>

1. <span data-ttu-id="0bb3a-456">双击失败的测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="0bb3a-457">您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-457">You receive an error message.</span></span>

    ![错误消息](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="0bb3a-459">选择 **详细信息** 以查看完整的错误消息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-459">Select **Details** to view the whole error message.</span></span>

    ![完整的错误消息](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="0bb3a-461">若要在 Azure DevOps 中查看错误消息的详细版本，请选择 **在 Azure DevOps 中打开**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="0bb3a-462">在 Azure DevOps 中，可查看测试用例的状态和详细错误消息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Azure DevOps 中的详细错误消息](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="0bb3a-464">若要直接在 Azure DevOps 项目中查看测试结果，请转到 **测试计划 \> 测试计划 \> 运行**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="0bb3a-465">双击要查看其更多详细信息的测试运行。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-465">Double-click the test run that you want to see more details for.</span></span>

    ![Azure DevOps 中的测试运行列表](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="0bb3a-467">**运行摘要** 选项卡指示测试用例失败，但是不提供实际的错误消息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="0bb3a-468">若要查看详细错误消息，请选择 **测试结果** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![“运行摘要”选项卡](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="0bb3a-470">**测试结果** 选项卡提供测试用例信息，以及结果和错误消息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![“测试结果”选项卡](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="0bb3a-472">双击相关记录以查看详细错误消息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![详细错误消息](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="0bb3a-474">本地的 **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt** 中也有所有错误消息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="0bb3a-475">也可以通过选择 **导出** 导出测试计划级结果。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![导出测试计划](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="0bb3a-477">修改 Excel 参数文件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="0bb3a-478">打开 RSAT。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-478">Open RSAT.</span></span>
2. <span data-ttu-id="0bb3a-479">选择测试用例，然后选择 **编辑** 打开 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="0bb3a-480">请注意，**EcoResProductCreate** 表中的 **产品编号** 字段为硬编码。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="0bb3a-481">必须先将此字段更新为新的产品编号，才能再次运行测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="0bb3a-482">若要为每次运行生成唯一的产品编号，同时不必每次都重新打开 Excel 参数文件并手动更新产品编号，请使用以下 Excel 公式。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="0bb3a-483">除了 **常规** 选项卡，测试用例访问的每个窗体页在 Excel 参数文件中都有一个数据选项卡。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![“产品编号”字段](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="0bb3a-485">选择 **保存**，然后关闭 Excel 工作簿。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="0bb3a-486">选择 **上载** 将 Excel 参数文件保存到 Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![上载成功消息](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="0bb3a-488">若要在特定用户上下文中运行测试用例，请在 Excel 参数文件 **常规** 选项卡上的 **测试用户** 字段中输入用户的电子邮件 ID。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="0bb3a-489">在最新 RSAT 版本中，已更新了 Excel 参数文件中的字段布局，但是概念不变。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![“测试用户”字段](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="0bb3a-491">验证结果</span><span class="sxs-lookup"><span data-stu-id="0bb3a-491">Validate the results</span></span>

- <span data-ttu-id="0bb3a-492">选择 **运行** 以重新运行测试用例，并且验证测试用例是否已通过。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="0bb3a-493">可按照[查看测试结果](#view-the-test-results)部分中的说明查看测试结果。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![“结果”字段已设置为“通过”](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="0bb3a-495">链接测试用例</span><span class="sxs-lookup"><span data-stu-id="0bb3a-495">Chaining of test cases</span></span>

<span data-ttu-id="0bb3a-496">RSAT 的一项关键功能是链接测试用例（即一个测试将值传递给其他测试这项功能）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="0bb3a-497">将根据在 Azure DevOps 测试计划中为测试用例定义的顺序运行测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="0bb3a-498">（也可以在测试工具本身中更新此顺序。）因此，如果要将变量从一个测试用例传递到另一个，则测试顺序务必正确。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="0bb3a-499">此部分中，将在第一个测试用例中创建已保存变量，创建第二个测试用例，然后将已保存变量从第一个测试用例传递到第二个测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="0bb3a-500">然后将在 RSAT 中把测试用例作为链式测试用例运行。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="0bb3a-501">修改现有任务录制以创建已保存变量</span><span class="sxs-lookup"><span data-stu-id="0bb3a-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="0bb3a-502">打开客户端。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-502">Open the client.</span></span>
2. <span data-ttu-id="0bb3a-503">选择 **设置** 按钮（齿轮符号），然后选择 **任务录制器**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="0bb3a-504">选择 **编辑录制**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-504">Select **Edit Recording**.</span></span>

    ![“编辑录制”按钮](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="0bb3a-506">选择 **从 Lifecycle Services 打开**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-506">Select **Open from Lifecycle Services**.</span></span>

    ![“从 Lifecycle Services 打开”按钮](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="0bb3a-508">选择 **选择 Lifecycle Services 库**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-508">Select **Select the Lifecycle Services library**.</span></span>

    ![“选择 Lifecycle Services 库”按钮](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="0bb3a-510">将从 LCS 加载 BPM 库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-510">BPM libraries are loaded from LCS.</span></span>

    ![加载 BPM 库](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="0bb3a-512">从 LCS 加载 BPM 库之后，选择任务录制关联的 **RSAT** BPM 库和 **创建新产品** 业务流程。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="0bb3a-513">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-513">Then select **OK**.</span></span>

    ![选择 BPM 库和业务流程](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="0bb3a-515">将在 **录制名称** 字段中输入相应任务录制的名称。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="0bb3a-516">选择 **开始**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-516">Select **Start**.</span></span>

    ![“录制名称”字段中的任务录制名称](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="0bb3a-518">转到 **产品信息管理 \> 产品**，然后选择 **新建** 打开在其中录制了原始任务录制（即 **创建产品**）的页面。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="0bb3a-519">选择 **插入步骤**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-520">将在窗格中选择的步骤 **后面** 插入新步骤。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![“插入步骤”按钮](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="0bb3a-522">右键单击 **产品编号** 字段，然后选择 **任务录制器 \> 复制**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![“复制”命令](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="0bb3a-524">将在窗格中添加一个新步骤。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-524">A new step is added in the pane.</span></span> <span data-ttu-id="0bb3a-525">记下 **产品编号** 字段中的值，因为后面需要。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![添加了新步骤](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="0bb3a-527">选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="0bb3a-528">选择 **保存到 Lifecycle Services**，然后将新任务录制与原始任务录制关联的相同 BPM 库和业务流程关联。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="0bb3a-529">有关详细信息，请参阅[创建任务录制并保存到 BPM 库](#create-a-task-recording-and-save-it-to-the-bpm-library)部分。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="0bb3a-530">转到 BPM 库，然后选择 **同步测试用例** 以按照[测试从 BPM 到 Azure DevOps 的同步](#test-the-synchronization-from-bpm-to-azure-devops)部分中的说明在 Azure DevOps 中覆盖附加到测试用例的任务录制。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="0bb3a-531">打开 RSAT，然后选择 **加载** 以重新加载测试套件中的所有测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="0bb3a-532">必须按照 [加载和运行测试用例](#load-and-run-test-cases)部分中的说明为相应测试用例重新生成自动化文件和参数文件，方法是选择测试用例，然后选择 **新建 \> 生成测试执行和参数文件**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-533">如果 Excel 参数文件未关闭，重新生成将失败。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="0bb3a-534">因此，生成新的 Excel 参数文件之前，确保关闭测试用例的 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="0bb3a-535">选择 **编辑** 打开新的 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="0bb3a-536">将在行 9 中看到新的 **已保存变量** 条目。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="0bb3a-537">此变量（即 **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**）将保存到任务录制的 XML 文件，并且可以在后续测试中使用。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![“已保存变量”条目](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="0bb3a-539">创建新的测试用例</span><span class="sxs-lookup"><span data-stu-id="0bb3a-539">Create a new test case</span></span>

1. <span data-ttu-id="0bb3a-540">转到 **RSAT** BPM 库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="0bb3a-541">选择 **示例支持业务流程** 流程，然后选择右侧的 **编辑模式**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="0bb3a-542">将 **名称** 字段和 **说明** 字段的值更改为 **发布产品**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="0bb3a-543">然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-543">Then select **Save**.</span></span>

    ![“名称”和“说明”已更改为“发布产品”](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="0bb3a-545">创建具有验证功能的新任务录制</span><span class="sxs-lookup"><span data-stu-id="0bb3a-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="0bb3a-546">创建任务录制以将之前创建的产品发布给 USRT 法人。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="0bb3a-547">有关详细信息，请参阅[创建任务录制并保存到 BPM 库](#create-a-task-recording-and-save-it-to-the-bpm-library)部分。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0bb3a-548">对于链式测试用例，我们始终建议您通过 *手动键入字段的值* 查找或筛选您需要的记录。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="0bb3a-549">这样，此工具就可以确定后续测试用例中必须对其执行操作的记录。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![具有验证功能的新任务录制](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="0bb3a-551">如上图所示，使用快速筛选器找到产品之后，选择 **发布产品** 之前，请验证 **产品编号** 字段的值以确保产品 ID 是之前创建的产品 ID。 </span><span class="sxs-lookup"><span data-stu-id="0bb3a-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="0bb3a-552">若要验证该值，请右键单击 **产品编号** 字段，然后选择 **任务录制器 \> 验证 \> 当前值**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![验证当前值](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="0bb3a-554">将任务录制保存到 BPM</span><span class="sxs-lookup"><span data-stu-id="0bb3a-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="0bb3a-555">完成任务录制后，选择 **保存到 Lifecycle Services**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![将完成的任务录制保存到 Lifecycle Services](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="0bb3a-557">将从 LCS 加载库信息。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-557">Library information is loaded from LCS.</span></span>

    ![从 LCS 加载库信息](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="0bb3a-559">选择要与任务录制关联的 BPM 库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="0bb3a-560">对于本教程，请选择之前创建的 **RSAT** BPM 库及其下的 **发布产品** 业务流程。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="0bb3a-561">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="0bb3a-562">将 BPM 同步到 Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="0bb3a-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="0bb3a-563">转到 BPM 库，然后打开 **RSAT** 库。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="0bb3a-564">选择 **VSTS 同步**，然后选择 **同步测试用例**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="0bb3a-565">有关详细信息，请参阅[测试从 BPM 到 Azure DevOps 的同步](#test-the-synchronization-from-bpm-to-azure-devops)部分。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="0bb3a-566">同步完成后，Azure DevOps 中 **面板 \> 工作项** 内将显示 **发布产品** 业务流程的新工作项和相应测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="0bb3a-567">将新测试用例添加到现有测试套件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="0bb3a-568">转到 **测试计划 \> 测试计划**，然后选择 **RSAT 测试计划** 计划。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="0bb3a-569">选择 **添加现有**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="0bb3a-570">在 **向套件添加测试用例** 页中，选择 **运行查询**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="0bb3a-571">选择为 **发布产品** 创建的新测试用例，然后选择页面右下角的 **添加测试用例**（下图中未显示此按钮）。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![“向套件添加测试用例”页](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="0bb3a-573">此测试套件现在有两个测试用例。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-573">The test suite now has two test cases.</span></span>

    ![测试套件中的两个测试用例](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="0bb3a-575">将测试用例加载到 RSAT 中</span><span class="sxs-lookup"><span data-stu-id="0bb3a-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="0bb3a-576">打开 RSAT，然后选择 **加载**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="0bb3a-577">将加载测试用例，而您会收到警告，说明“此操作将覆盖 Excel 测试数据文件，本地更改将丢失。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="0bb3a-578">是否要继续?”</span><span class="sxs-lookup"><span data-stu-id="0bb3a-578">Do you want to proceed?"</span></span> <span data-ttu-id="0bb3a-579">选择 **是** 以更新本地系统中的 Excel 参数文件，但是不更新上载到 Azure DevOps 的 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![此操作将覆盖 Excel 测试数据文件](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="0bb3a-581">将加载这两个测试用例，以及第一个测试用例的 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="0bb3a-582">因为在上一个运行中选择了 **上载**，所以将从 Azure DevOps 提取参数文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![已加载测试用例](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="0bb3a-584">仅选择第二个测试用例，然后选择 **新建 \> 生成测试执行和参数文件**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="0bb3a-585">编辑 Excel 参数文件</span><span class="sxs-lookup"><span data-stu-id="0bb3a-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="0bb3a-586">仅选择第二个测试用例，然后选择 **编辑** 打开相应 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="0bb3a-587">将已保存变量 **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**（请参阅[修改现有任务录制以创建已保存变量](#modify-an-existing-task-recording-to-create-a-saved-variable)部分）从第一个测试用例复制到使用产品编号的所有字段中。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="0bb3a-588">在此情况下，将把变量复制到 **EcoResProductListPage** 表的 **产品编号** 和 **验证产品编号** 字段中。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![“产品编号”和“验证产品编号”字段](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="0bb3a-590">只有在同一个测试运行期间才能在测试之间传递变量。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="0bb3a-591">变量的名称必须完全匹配。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="0bb3a-592">选择 **保存**，然后关闭 Excel 工作簿。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="0bb3a-593">选择 **上载** 保存对 Excel 参数文件执行的更改。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="0bb3a-594">运行链式测试用例</span><span class="sxs-lookup"><span data-stu-id="0bb3a-594">Run the chained test cases</span></span>

1. <span data-ttu-id="0bb3a-595">同时选择这两个测试用例，然后选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="0bb3a-596">验证这两个测试用例是否均已通过。</span><span class="sxs-lookup"><span data-stu-id="0bb3a-596">Verify that both test cases have passed.</span></span>

    ![两个测试用例的“结果”字段均设置为已通过](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]