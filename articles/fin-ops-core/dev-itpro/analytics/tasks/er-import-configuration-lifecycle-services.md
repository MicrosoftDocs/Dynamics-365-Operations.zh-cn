---
title: 从 Lifecycle Services 导入配置
description: 本主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 导入电子报告 (ER) 配置的新版本。
author: NickSelin
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 674d0dc02b4a53e455a15a06fdb7f24ca3036ba3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752356"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="a8305-103">从 Lifecycle Services 导入配置</span><span class="sxs-lookup"><span data-stu-id="a8305-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8305-104">此主题介绍系统管理员或电子报表开发人员角色的用户如何从 Microsoft Dynamics Lifecycle Services (LCS) 中的[项目级资产库](../../lifecycle-services/asset-library.md)导入新[电子申报 (ER) 配置](../general-electronic-reporting.md#Configuration)版本。</span><span class="sxs-lookup"><span data-stu-id="a8305-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="a8305-105">在此示例中，您将为名称为 Litware, Inc. 的示例公司选择所需的 ER 配置版本并将其导入。这些步骤可以在任何公司完成，因为这些公司共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="a8305-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="a8305-106">为了完成这些步骤，您必须首先完成[将配置上载到 Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) 中的步骤。</span><span class="sxs-lookup"><span data-stu-id="a8305-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="a8305-107">还需要 LCS 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="a8305-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="a8305-108">通过使用以下角色之一登录到应用程序：</span><span class="sxs-lookup"><span data-stu-id="a8305-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="a8305-109">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="a8305-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="a8305-110">系统管理员</span><span class="sxs-lookup"><span data-stu-id="a8305-110">System administrator</span></span>

2. <span data-ttu-id="a8305-111">转到 **组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="a8305-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="a8305-112">选择 **配置**。</span><span class="sxs-lookup"><span data-stu-id="a8305-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="a8305-113">确保当前 Dynamics 365 Finance 用户是其中包含用户希望[访问](../../lifecycle-services/asset-library.md#asset-library-support)来导入 ER 配置的资产库的 LCS 项目的成员。</span><span class="sxs-lookup"><span data-stu-id="a8305-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="a8305-114">不能从提供的域与 Finance 中使用的域不同的 ER 存储库访问 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="a8305-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="a8305-115">如果尝试访问，将显示空的 LCS 项目列表，并且您不能从 LCS 中的项目级资产库导入 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="a8305-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="a8305-116">若要从用于导入 ER 配置的 ER 存储库访问项目级资产库，请使用属于为其预配了当前 Finance 实例的租户（域）的用户的凭证登录 Finance。</span><span class="sxs-lookup"><span data-stu-id="a8305-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="a8305-117">删除数据模型配置的共享版本</span><span class="sxs-lookup"><span data-stu-id="a8305-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="a8305-118">在 **配置** 页上的配置树中，选择 **示例模型配置**。</span><span class="sxs-lookup"><span data-stu-id="a8305-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="a8305-119">在完成[将配置上载到 Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) 中的步骤时，创建了示例数据模型配置的第一个版本并发布到了 LCS。</span><span class="sxs-lookup"><span data-stu-id="a8305-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="a8305-120">在此过程中，您将删除 ER 配置的这一版本。</span><span class="sxs-lookup"><span data-stu-id="a8305-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="a8305-121">然后将在本主题后文从 LCS 导入该版本。</span><span class="sxs-lookup"><span data-stu-id="a8305-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="a8305-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a8305-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="a8305-123">对于此示例，请选择状态为 **已共享** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="a8305-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="a8305-124">此状态指示配置已发布到为 LCS。</span><span class="sxs-lookup"><span data-stu-id="a8305-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="a8305-125">选择 **更改状态**。</span><span class="sxs-lookup"><span data-stu-id="a8305-125">Select **Change status**.</span></span>
4. <span data-ttu-id="a8305-126">选择 **中断**。</span><span class="sxs-lookup"><span data-stu-id="a8305-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="a8305-127">通过将所选版本的状态从 **已共享** 更改为 **已中断**，使此版本可删除。</span><span class="sxs-lookup"><span data-stu-id="a8305-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="a8305-128">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a8305-128">Select **OK**.</span></span>
6. <span data-ttu-id="a8305-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a8305-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="a8305-130">对于此示例，请选择状态为 **中断** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="a8305-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="a8305-131">选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="a8305-131">Select **Delete**.</span></span>
8. <span data-ttu-id="a8305-132">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="a8305-132">Select **Yes**.</span></span>

    <span data-ttu-id="a8305-133">请注意，仅所选数据模型配置的草稿版本 2 现在可用。</span><span class="sxs-lookup"><span data-stu-id="a8305-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="a8305-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8305-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="a8305-135">从 LCS 导入数据模型配置的共享版本</span><span class="sxs-lookup"><span data-stu-id="a8305-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="a8305-136">转到 **组织管理 \> 工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="a8305-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="a8305-137">在 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a8305-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="a8305-138">在 **Litware, Inc.** 磁贴上，选择 **存储库**。</span><span class="sxs-lookup"><span data-stu-id="a8305-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="a8305-139">现在可以打开 Litware, Inc 配置提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="a8305-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="a8305-140">选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="a8305-140">Select **Open**.</span></span>

    <span data-ttu-id="a8305-141">对于此示例，请选择 **LCS** 存储库，然后打开。</span><span class="sxs-lookup"><span data-stu-id="a8305-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="a8305-142">必须具有该 LCS 项目和所选 ER 存储库访问的资产库的[访问权限](#accessconditions)。</span><span class="sxs-lookup"><span data-stu-id="a8305-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="a8305-143">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="a8305-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="a8305-144">对于此示例，请在版本列表中选择 **示例模型配置** 的第一个版本。</span><span class="sxs-lookup"><span data-stu-id="a8305-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="a8305-145">选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="a8305-145">Select **Import**.</span></span>
7. <span data-ttu-id="a8305-146">选择 **是** 确认从 LCS 导入所选版本。</span><span class="sxs-lookup"><span data-stu-id="a8305-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="a8305-147">将通过参考消息确认已成功导入了所选版本。</span><span class="sxs-lookup"><span data-stu-id="a8305-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="a8305-148">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8305-148">Close the page.</span></span>
9. <span data-ttu-id="a8305-149">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8305-149">Close the page.</span></span>
10. <span data-ttu-id="a8305-150">选择 **配置**。</span><span class="sxs-lookup"><span data-stu-id="a8305-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="a8305-151">在树结构中，选择 **示例模型配置**。</span><span class="sxs-lookup"><span data-stu-id="a8305-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="a8305-152">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a8305-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="a8305-153">对于此示例，请选择状态为 **已共享** 的配置版本。</span><span class="sxs-lookup"><span data-stu-id="a8305-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="a8305-154">请注意，所选数据模型配置的共享版本 1 现在也可用。</span><span class="sxs-lookup"><span data-stu-id="a8305-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]