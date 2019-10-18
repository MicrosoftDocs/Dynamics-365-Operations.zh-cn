---
title: ER 上载配置到 Lifecycle Services
description: 以下步骤说明属于系统管理员或电子报表开发人员用户如何创建新电子申报 (ER) 配置并将其上载到 Microsoft Lifecycle Services (LCS)。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 980ce00ae702ea0a3394efa15419e0f7b7dc2530
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182201"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="8b95a-103">ER 上载配置到 Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="8b95a-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b95a-104">以下步骤说明属于系统管理员或电子报表开发人员用户如何创建新电子申报 (ER) 配置并将其上载到 Microsoft Lifecycle Services (LCS)。</span><span class="sxs-lookup"><span data-stu-id="8b95a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="8b95a-105">此示例以示例公司 Litware，Inc. 为例，您将创建一个配置提供程序并将其上载到 LCS。这些步骤可在任何公司执行，因为公司之间共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="8b95a-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="8b95a-106">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="8b95a-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="8b95a-107">完成这些步骤还需要能够访问 LCS。</span><span class="sxs-lookup"><span data-stu-id="8b95a-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="8b95a-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8b95a-109">选择“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="8b95a-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="8b95a-110">并设置为活动状态。</span><span class="sxs-lookup"><span data-stu-id="8b95a-110">and set it as active.</span></span>
3. <span data-ttu-id="8b95a-111">单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="8b95a-112">创建新的数据模型配置</span><span class="sxs-lookup"><span data-stu-id="8b95a-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="8b95a-113">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="8b95a-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="8b95a-114">您将创建含有电子单据的示例数据模型的配置。</span><span class="sxs-lookup"><span data-stu-id="8b95a-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="8b95a-115">此数据模型配置稍后将上载到 LCS。</span><span class="sxs-lookup"><span data-stu-id="8b95a-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="8b95a-116">在“名称”字段中，键入“示例模型配置”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="8b95a-117">示例模型配置</span><span class="sxs-lookup"><span data-stu-id="8b95a-117">Sample model configuration</span></span>  
3. <span data-ttu-id="8b95a-118">在“描述”字段中，键入“示例模型配置”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="8b95a-119">示例模型配置</span><span class="sxs-lookup"><span data-stu-id="8b95a-119">Sample model configuration</span></span>  
4. <span data-ttu-id="8b95a-120">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-120">Click Create configuration.</span></span>
5. <span data-ttu-id="8b95a-121">单击“模型设计器”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-121">Click Model designer.</span></span>
6. <span data-ttu-id="8b95a-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-122">Click New.</span></span>
7. <span data-ttu-id="8b95a-123">在“名称”字段中，键入“入口点”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="8b95a-124">入口点</span><span class="sxs-lookup"><span data-stu-id="8b95a-124">Entry point</span></span>  
8. <span data-ttu-id="8b95a-125">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-125">Click Add.</span></span>
9. <span data-ttu-id="8b95a-126">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-126">Click Save.</span></span>
10. <span data-ttu-id="8b95a-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b95a-127">Close the page.</span></span>
11. <span data-ttu-id="8b95a-128">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-128">Click Change status.</span></span>
12. <span data-ttu-id="8b95a-129">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-129">Click Complete.</span></span>
13. <span data-ttu-id="8b95a-130">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="8b95a-131">登记新存储库</span><span class="sxs-lookup"><span data-stu-id="8b95a-131">Register a new  repository</span></span>
1. <span data-ttu-id="8b95a-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b95a-132">Close the page.</span></span>
2. <span data-ttu-id="8b95a-133">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-133">Click Repositories.</span></span>
    * <span data-ttu-id="8b95a-134">这使您打开 Litware, Inc 配置提供程序的 存储库列表。</span><span class="sxs-lookup"><span data-stu-id="8b95a-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="8b95a-135">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="8b95a-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="8b95a-136">这允许您添加新的存储库。</span><span class="sxs-lookup"><span data-stu-id="8b95a-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="8b95a-137">在“配置存储库类型”字段中，选择 LCS。</span><span class="sxs-lookup"><span data-stu-id="8b95a-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="8b95a-138">单击“创建存储库”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-138">Click Create repository.</span></span>
6. <span data-ttu-id="8b95a-139">在“项目”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8b95a-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="8b95a-140">选择所需的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="8b95a-140">Select the desired LCS project.</span></span> <span data-ttu-id="8b95a-141">您必须有权访问该项目。</span><span class="sxs-lookup"><span data-stu-id="8b95a-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="8b95a-142">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-142">Click OK.</span></span>
    * <span data-ttu-id="8b95a-143">完成新的存储库输入。</span><span class="sxs-lookup"><span data-stu-id="8b95a-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="8b95a-144">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8b95a-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8b95a-145">选择 LCS 存储库记录。</span><span class="sxs-lookup"><span data-stu-id="8b95a-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="8b95a-146">请注意，登记的存储库由当前提供程序标记，这意味着该提供程序拥有的唯一配置可放置到此存储库中，因此，可上载到所选 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="8b95a-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="8b95a-147">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-147">Click Open.</span></span>
    * <span data-ttu-id="8b95a-148">打开存储库查看 ER 配置列表。</span><span class="sxs-lookup"><span data-stu-id="8b95a-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="8b95a-149">如果此项目没有用于 ER 配置共享，其将为空。</span><span class="sxs-lookup"><span data-stu-id="8b95a-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="8b95a-150">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b95a-150">Close the page.</span></span>
11. <span data-ttu-id="8b95a-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b95a-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="8b95a-152">上载配置到 LCS</span><span class="sxs-lookup"><span data-stu-id="8b95a-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="8b95a-153">单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-153">Click Configurations.</span></span>
2. <span data-ttu-id="8b95a-154">在树结构中，选择“示例模型配置”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="8b95a-155">选择已完成的创建的配置。</span><span class="sxs-lookup"><span data-stu-id="8b95a-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="8b95a-156">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="8b95a-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8b95a-157">选择状态为“已完成”的所选配置的版本。</span><span class="sxs-lookup"><span data-stu-id="8b95a-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="8b95a-158">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-158">Click Change status.</span></span>
5. <span data-ttu-id="8b95a-159">单击“共享”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-159">Click Share.</span></span>
    * <span data-ttu-id="8b95a-160">当在 LCS 中发布时，配置状态将从“已完成”更改为“已共享”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="8b95a-161">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-161">Click OK.</span></span>
7. <span data-ttu-id="8b95a-162">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="8b95a-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8b95a-163">选择状态为“已共享”的配置版本。</span><span class="sxs-lookup"><span data-stu-id="8b95a-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="8b95a-164">请注意，所选版本的状态已从“已完成”更改为“已共享”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="8b95a-165">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b95a-165">Close the page.</span></span>
9. <span data-ttu-id="8b95a-166">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-166">Click Repositories.</span></span>
    * <span data-ttu-id="8b95a-167">这使您打开 Litware, Inc 配置提供程序的 存储库列表。</span><span class="sxs-lookup"><span data-stu-id="8b95a-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="8b95a-168">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="8b95a-168">Click Open.</span></span>
    * <span data-ttu-id="8b95a-169">选择 LCS 存储库然后打开它。</span><span class="sxs-lookup"><span data-stu-id="8b95a-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="8b95a-170">请注意，所选配置显示为所选 LCS 项目的资产。</span><span class="sxs-lookup"><span data-stu-id="8b95a-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="8b95a-171">使用 https://lcs.dynamics.com 打开 LCS。</span><span class="sxs-lookup"><span data-stu-id="8b95a-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="8b95a-172">打开之前用于存储库登记的项目，打开此项目的“资产库”，然后展开“GER 配置”资产类型 – 上载的的 ER 配置将可用。</span><span class="sxs-lookup"><span data-stu-id="8b95a-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="8b95a-173">请注意，如果提供程序有权访问此 LCS 项目，上载的 LCS 配置可以导入到其他实例。</span><span class="sxs-lookup"><span data-stu-id="8b95a-173">Note that the uploaded LCS configuration can be imported to another instance if providers have access to this LCS project.</span></span>  

