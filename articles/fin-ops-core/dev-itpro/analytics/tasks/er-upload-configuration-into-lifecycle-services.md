---
title: 上载配置到 Lifecycle Services
description: 此主题介绍系统管理员或电子报表开发人员角色的用户如何新建电子申报 (ER) 配置并上载到 Microsoft Dynamics Lifecycle Services (LCS) 中。
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ebafb52882fd33f4f0ef140c5d23d3288af97a2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684155"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="3eb22-103">上载配置到 Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="3eb22-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3eb22-104">此主题介绍系统管理员或电子报表开发人员角色的用户如何新建[电子申报 (ER) 配置](../general-electronic-reporting.md#Configuration)并上载到 Microsoft Dynamics Lifecycle Services (LCS) 中的[项目级资产库](../../lifecycle-services/asset-library.md)中。</span><span class="sxs-lookup"><span data-stu-id="3eb22-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="3eb22-105">此示例以名称为 Litware，Inc. 的示例公司为例，您将创建一个配置提供程序并将其上载到 LCS 中。这些步骤可在任何公司完成，因为公司之间共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="3eb22-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="3eb22-106">为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="3eb22-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="3eb22-107">还需要 LCS 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="3eb22-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="3eb22-108">通过使用以下角色之一登录到应用程序：</span><span class="sxs-lookup"><span data-stu-id="3eb22-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="3eb22-109">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="3eb22-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="3eb22-110">系统管理员</span><span class="sxs-lookup"><span data-stu-id="3eb22-110">System administrator</span></span>

2. <span data-ttu-id="3eb22-111">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="3eb22-112">选择 **Litware, Inc.** 并将其标记为 **有效**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="3eb22-113">选择 **配置**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="3eb22-114">确保当前 Dynamics 365 Finance 用户是其中包含用于导入 ER 配置的[资产库](../../lifecycle-services/asset-library.md#asset-library-support)的 LCS 项目的成员。</span><span class="sxs-lookup"><span data-stu-id="3eb22-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="3eb22-115">不能从提供的域与 Finance 中使用的域不同的 ER 存储库访问 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="3eb22-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="3eb22-116">如果尝试访问，将显示空的 LCS 项目列表，并且您不能从 LCS 中的项目级资产库导入 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="3eb22-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="3eb22-117">若要从用于导入 ER 配置的 ER 存储库访问项目级资产库，请使用属于为其预配了当前 Finance 实例的租户（域）的用户的凭证登录 Finance。</span><span class="sxs-lookup"><span data-stu-id="3eb22-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="3eb22-118">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="3eb22-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="3eb22-119">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="3eb22-120">在 **配置** 页面中，选择 **创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="3eb22-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="3eb22-121">在此示例中，您将创建含有电子单据的示例数据模型的配置。</span><span class="sxs-lookup"><span data-stu-id="3eb22-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="3eb22-122">此数据模型配置稍后将上载到 LCS。</span><span class="sxs-lookup"><span data-stu-id="3eb22-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="3eb22-123">在 **名称** 字段中，输入 **示例模型配置**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="3eb22-124">在 **描述** 字段中，输入 **示例模型配置**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="3eb22-125">选择 **创建配置**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="3eb22-126">选择 **模型设计器** 。</span><span class="sxs-lookup"><span data-stu-id="3eb22-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="3eb22-127">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-127">Select **New**.</span></span>
8. <span data-ttu-id="3eb22-128">在 **名称** 字段中，输入 **入口点**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="3eb22-129">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-129">Select **Add**.</span></span>
10. <span data-ttu-id="3eb22-130">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-130">Select **Save**.</span></span>
11. <span data-ttu-id="3eb22-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3eb22-131">Close the page.</span></span>
12. <span data-ttu-id="3eb22-132">选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-132">Select **Change status**.</span></span>
13. <span data-ttu-id="3eb22-133">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-133">Select **Complete**.</span></span>
14. <span data-ttu-id="3eb22-134">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-134">Select **OK**.</span></span>
15. <span data-ttu-id="3eb22-135">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3eb22-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="3eb22-136">登记新存储库</span><span class="sxs-lookup"><span data-stu-id="3eb22-136">Register a new repository</span></span>

1. <span data-ttu-id="3eb22-137">转到 **组织管理 \> 工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="3eb22-138">在 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="3eb22-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="3eb22-139">在 **Litware, Inc.** 磁贴上，选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="3eb22-140">现在可以打开 Litware, Inc 配置提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="3eb22-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="3eb22-141">选择 **添加** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="3eb22-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="3eb22-142">现在可以添加新存储库。</span><span class="sxs-lookup"><span data-stu-id="3eb22-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="3eb22-143">在 **配置存储库类型** 字段中，选择 **LCS**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="3eb22-144">选择 **创建存储库**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="3eb22-145">在 **项目** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="3eb22-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="3eb22-146">在本示例中，选择所需 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="3eb22-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="3eb22-147">您必须有权[访问](#accessconditions)该项目。</span><span class="sxs-lookup"><span data-stu-id="3eb22-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="3eb22-148">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-148">Select **OK**.</span></span>

    <span data-ttu-id="3eb22-149">完成新的存储库输入。</span><span class="sxs-lookup"><span data-stu-id="3eb22-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="3eb22-150">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="3eb22-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="3eb22-151">对于此示例，请选择 **LCS** 存储库记录。</span><span class="sxs-lookup"><span data-stu-id="3eb22-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="3eb22-152">请注意，当前提供商将标记注册的存储库。</span><span class="sxs-lookup"><span data-stu-id="3eb22-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="3eb22-153">换句话说，只能将该提供商负责的配置放入此存储库中，从而上载到所选 LCS 项目中。</span><span class="sxs-lookup"><span data-stu-id="3eb22-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="3eb22-154">选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-154">Select **Open**.</span></span>

    <span data-ttu-id="3eb22-155">打开存储库查看 ER 配置列表。</span><span class="sxs-lookup"><span data-stu-id="3eb22-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="3eb22-156">如果尚未将所选项目用于共享 ER 配置，列表将为空。</span><span class="sxs-lookup"><span data-stu-id="3eb22-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="3eb22-157">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3eb22-157">Close the page.</span></span>
12. <span data-ttu-id="3eb22-158">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3eb22-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="3eb22-159">将配置上传到 LCS 中</span><span class="sxs-lookup"><span data-stu-id="3eb22-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="3eb22-160">转到 **组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="3eb22-161">在 **配置** 页上的配置树中，选择 **示例模型配置**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="3eb22-162">必须选择已完成的创建的配置。</span><span class="sxs-lookup"><span data-stu-id="3eb22-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="3eb22-163">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="3eb22-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3eb22-164">对于此示例，请选择状态为 **已完成** 的所选配置版本。</span><span class="sxs-lookup"><span data-stu-id="3eb22-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="3eb22-165">选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-165">Select **Change status**.</span></span>
5. <span data-ttu-id="3eb22-166">选择 **共享**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-166">Select **Share**.</span></span>

    <span data-ttu-id="3eb22-167">在 LCS 中发布配置时，配置的状态将从 **已完成** 变为 **已共享**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="3eb22-168">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-168">Select **OK**.</span></span>
7. <span data-ttu-id="3eb22-169">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="3eb22-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3eb22-170">对于此示例，请选择状态为 **已共享** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="3eb22-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="3eb22-171">请注意，所选版本的状态已从 **已完成** 变为 **已共享**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="3eb22-172">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="3eb22-172">Close the page.</span></span>
9. <span data-ttu-id="3eb22-173">选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-173">Select **Repositories**.</span></span>

    <span data-ttu-id="3eb22-174">现在可以打开 Litware, Inc 配置提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="3eb22-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="3eb22-175">选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="3eb22-175">Select **Open**.</span></span>

    <span data-ttu-id="3eb22-176">对于此示例，请选择 **LCS** 存储库，然后打开。</span><span class="sxs-lookup"><span data-stu-id="3eb22-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="3eb22-177">请注意，所选配置显示为所选 LCS 项目的资产。</span><span class="sxs-lookup"><span data-stu-id="3eb22-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="3eb22-178">通过转到 <https://lcs.dynamics.com> 打开 LCS。</span><span class="sxs-lookup"><span data-stu-id="3eb22-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="3eb22-179">打开一个先前用于存储库注册的项目。</span><span class="sxs-lookup"><span data-stu-id="3eb22-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="3eb22-180">打开项目的资产库。</span><span class="sxs-lookup"><span data-stu-id="3eb22-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="3eb22-181">选择 **GER 配置** 资产类型。</span><span class="sxs-lookup"><span data-stu-id="3eb22-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="3eb22-182">应该会列出您上载的 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="3eb22-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="3eb22-183">请注意，如果提供程序有权访问此 LCS 项目，上载的 LCS 配置可以导入到其他实例中。</span><span class="sxs-lookup"><span data-stu-id="3eb22-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>
