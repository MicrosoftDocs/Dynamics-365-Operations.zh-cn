---
title: 上载配置到 Lifecycle Services
description: 本主题说明如何创建新的电子报告 (ER) 配置并将其上载到 Microsoft Dynamics Lifecycle Services (LCS)。
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270551"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="64146-103">上载配置到 Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="64146-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64146-104">此主题介绍系统管理员或电子报表开发人员角色的用户如何新建[电子申报 (ER) 配置](../general-electronic-reporting.md#Configuration)并上载到 Microsoft Dynamics Lifecycle Services (LCS) 中的[项目级资产库](../../lifecycle-services/asset-library.md)中。</span><span class="sxs-lookup"><span data-stu-id="64146-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64146-105">使用 LCS 作为 ER 配置的存储库将[弃用](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)。</span><span class="sxs-lookup"><span data-stu-id="64146-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="64146-106">有关详细信息，请参阅 [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 存储弃用](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md)。</span><span class="sxs-lookup"><span data-stu-id="64146-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="64146-107">此示例以名称为 Litware，Inc. 的示例公司为例，您将创建一个配置提供程序并将其上载到 LCS 中。这些步骤可在任何公司完成，因为公司之间共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="64146-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="64146-108">为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="64146-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="64146-109">还需要 LCS 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="64146-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="64146-110">通过使用以下角色之一登录到应用程序：</span><span class="sxs-lookup"><span data-stu-id="64146-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="64146-111">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="64146-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="64146-112">系统管理员</span><span class="sxs-lookup"><span data-stu-id="64146-112">System administrator</span></span>

2. <span data-ttu-id="64146-113">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="64146-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="64146-114">选择 **Litware, Inc.** 并将其标记为 **有效**。</span><span class="sxs-lookup"><span data-stu-id="64146-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="64146-115">选择 **配置**。</span><span class="sxs-lookup"><span data-stu-id="64146-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="64146-116">确保当前 Dynamics 365 Finance 用户是其中包含用于导入 ER 配置的[资产库](../../lifecycle-services/asset-library.md#asset-library-support)的 LCS 项目的成员。</span><span class="sxs-lookup"><span data-stu-id="64146-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="64146-117">不能从提供的域与 Finance 中使用的域不同的 ER 存储库访问 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="64146-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="64146-118">如果尝试访问，将显示空的 LCS 项目列表，并且您不能从 LCS 中的项目级资产库导入 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="64146-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="64146-119">若要从用于导入 ER 配置的 ER 存储库访问项目级资产库，请使用属于为其预配了当前 Finance 实例的租户（域）的用户的凭证登录 Finance。</span><span class="sxs-lookup"><span data-stu-id="64146-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="64146-120">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="64146-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="64146-121">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="64146-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="64146-122">在 **配置** 页面中，选择 **创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="64146-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="64146-123">在此示例中，您将创建含有电子单据的示例数据模型的配置。</span><span class="sxs-lookup"><span data-stu-id="64146-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="64146-124">此数据模型配置稍后将上载到 LCS。</span><span class="sxs-lookup"><span data-stu-id="64146-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="64146-125">在 **名称** 字段中，输入 **示例模型配置**。</span><span class="sxs-lookup"><span data-stu-id="64146-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="64146-126">在 **描述** 字段中，输入 **示例模型配置**。</span><span class="sxs-lookup"><span data-stu-id="64146-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="64146-127">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="64146-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="64146-128">选择 **模型设计器** 。</span><span class="sxs-lookup"><span data-stu-id="64146-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="64146-129">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="64146-129">Select **New**.</span></span>
8. <span data-ttu-id="64146-130">在 **名称** 字段中，输入 **入口点**。</span><span class="sxs-lookup"><span data-stu-id="64146-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="64146-131">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="64146-131">Select **Add**.</span></span>
10. <span data-ttu-id="64146-132">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="64146-132">Select **Save**.</span></span>
11. <span data-ttu-id="64146-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="64146-133">Close the page.</span></span>
12. <span data-ttu-id="64146-134">选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="64146-134">Select **Change status**.</span></span>
13. <span data-ttu-id="64146-135">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="64146-135">Select **Complete**.</span></span>
14. <span data-ttu-id="64146-136">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="64146-136">Select **OK**.</span></span>
15. <span data-ttu-id="64146-137">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="64146-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="64146-138">登记新存储库</span><span class="sxs-lookup"><span data-stu-id="64146-138">Register a new repository</span></span>

1. <span data-ttu-id="64146-139">转到 **组织管理 \> 工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="64146-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="64146-140">在 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="64146-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="64146-141">在 **Litware, Inc.** 磁贴上，选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="64146-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="64146-142">现在可以打开 Litware, Inc 配置提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="64146-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="64146-143">选择 **添加** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="64146-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="64146-144">现在可以添加新存储库。</span><span class="sxs-lookup"><span data-stu-id="64146-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="64146-145">在 **配置存储库类型** 字段中，选择 **LCS**。</span><span class="sxs-lookup"><span data-stu-id="64146-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="64146-146">选择 **创建存储库**。</span><span class="sxs-lookup"><span data-stu-id="64146-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="64146-147">在 **项目** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="64146-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="64146-148">在本示例中，选择所需 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="64146-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="64146-149">您必须有权[访问](#accessconditions)该项目。</span><span class="sxs-lookup"><span data-stu-id="64146-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="64146-150">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="64146-150">Select **OK**.</span></span>

    <span data-ttu-id="64146-151">完成新的存储库输入。</span><span class="sxs-lookup"><span data-stu-id="64146-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="64146-152">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="64146-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="64146-153">对于此示例，请选择 **LCS** 存储库记录。</span><span class="sxs-lookup"><span data-stu-id="64146-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="64146-154">请注意，当前提供商将标记注册的存储库。</span><span class="sxs-lookup"><span data-stu-id="64146-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="64146-155">换句话说，只能将该提供商负责的配置放入此存储库中，从而上载到所选 LCS 项目中。</span><span class="sxs-lookup"><span data-stu-id="64146-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="64146-156">选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="64146-156">Select **Open**.</span></span>

    <span data-ttu-id="64146-157">打开存储库查看 ER 配置列表。</span><span class="sxs-lookup"><span data-stu-id="64146-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="64146-158">如果尚未将所选项目用于共享 ER 配置，列表将为空。</span><span class="sxs-lookup"><span data-stu-id="64146-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="64146-159">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="64146-159">Close the page.</span></span>
12. <span data-ttu-id="64146-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="64146-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="64146-161">将配置上传到 LCS 中</span><span class="sxs-lookup"><span data-stu-id="64146-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="64146-162">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="64146-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="64146-163">在 **配置** 页上的配置树中，选择 **示例模型配置**。</span><span class="sxs-lookup"><span data-stu-id="64146-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="64146-164">必须选择已完成的创建的配置。</span><span class="sxs-lookup"><span data-stu-id="64146-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="64146-165">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="64146-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="64146-166">对于此示例，请选择状态为 **已完成** 的所选配置版本。</span><span class="sxs-lookup"><span data-stu-id="64146-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="64146-167">选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="64146-167">Select **Change status**.</span></span>
5. <span data-ttu-id="64146-168">选择 **共享**。</span><span class="sxs-lookup"><span data-stu-id="64146-168">Select **Share**.</span></span>

    <span data-ttu-id="64146-169">在 LCS 中发布配置时，配置的状态将从 **已完成** 变为 **已共享**。</span><span class="sxs-lookup"><span data-stu-id="64146-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="64146-170">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="64146-170">Select **OK**.</span></span>
7. <span data-ttu-id="64146-171">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="64146-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="64146-172">对于此示例，请选择状态为 **已共享** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="64146-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="64146-173">请注意，所选版本的状态已从 **已完成** 变为 **已共享**。</span><span class="sxs-lookup"><span data-stu-id="64146-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="64146-174">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="64146-174">Close the page.</span></span>
9. <span data-ttu-id="64146-175">选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="64146-175">Select **Repositories**.</span></span>

    <span data-ttu-id="64146-176">现在可以打开 Litware, Inc 配置提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="64146-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="64146-177">选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="64146-177">Select **Open**.</span></span>

    <span data-ttu-id="64146-178">对于此示例，请选择 **LCS** 存储库，然后打开。</span><span class="sxs-lookup"><span data-stu-id="64146-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="64146-179">请注意，所选配置显示为所选 LCS 项目的资产。</span><span class="sxs-lookup"><span data-stu-id="64146-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="64146-180">通过转到 <https://lcs.dynamics.com> 打开 LCS。</span><span class="sxs-lookup"><span data-stu-id="64146-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="64146-181">打开一个先前用于存储库注册的项目。</span><span class="sxs-lookup"><span data-stu-id="64146-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="64146-182">打开项目的资产库。</span><span class="sxs-lookup"><span data-stu-id="64146-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="64146-183">选择 **GER 配置** 资产类型。</span><span class="sxs-lookup"><span data-stu-id="64146-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="64146-184">应该会列出您上载的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="64146-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="64146-185">请注意，如果提供程序有权访问此 LCS 项目，上载的 LCS 配置可以导入到其他实例中。</span><span class="sxs-lookup"><span data-stu-id="64146-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
