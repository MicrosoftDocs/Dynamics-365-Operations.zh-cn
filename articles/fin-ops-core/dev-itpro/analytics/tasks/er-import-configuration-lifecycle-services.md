---
title: ER 从 Lifecycle Services 导入配置
description: 以下步骤说明系统管理员或电子报表开发人员角色的用户可如何从 Microsoft Lifecycle Services (LCS) 导入新电子申报 (ER) 配置版本。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184822"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="4cf81-103">ER 从 Lifecycle Services 导入配置</span><span class="sxs-lookup"><span data-stu-id="4cf81-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4cf81-104">以下步骤说明系统管理员或电子报表开发人员角色的用户可如何从 Microsoft Lifecycle Services (LCS) 导入新电子申报 (ER) 配置版本。</span><span class="sxs-lookup"><span data-stu-id="4cf81-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="4cf81-105">在此示例中，您将为示例公司 Litware 公司选择所需的 ER 配置版本并将其导入。这些步骤适用于所有公司，因为这些公司共享 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="4cf81-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="4cf81-106">为了完成这些步骤，您必须首先完成“将 ER 配置上载到 Lifecycle Services”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="4cf81-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="4cf81-107">完成这些步骤还需要能够访问 LCS。</span><span class="sxs-lookup"><span data-stu-id="4cf81-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="4cf81-108">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4cf81-109">单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="4cf81-110">删除数据模型配置的共享版本</span><span class="sxs-lookup"><span data-stu-id="4cf81-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="4cf81-111">在树结构中，选择“示例模型配置”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="4cf81-112">在“将 ER 配置上载到 Lifecycle Services”过程中，示例数据模型配置的第一个版本已创建并发布到 LCS。</span><span class="sxs-lookup"><span data-stu-id="4cf81-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="4cf81-113">在此过程中，您将删除 ER 配置的这一版本。</span><span class="sxs-lookup"><span data-stu-id="4cf81-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="4cf81-114">此示例数据模型配置版本以后将从 LCS 导入。</span><span class="sxs-lookup"><span data-stu-id="4cf81-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="4cf81-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="4cf81-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4cf81-116">选择状态不为“已共享”的此配置的版本。</span><span class="sxs-lookup"><span data-stu-id="4cf81-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="4cf81-117">此状态指示配置已发布到为 LCS。</span><span class="sxs-lookup"><span data-stu-id="4cf81-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="4cf81-118">单击“更改状态”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-118">Click Change status.</span></span>
4. <span data-ttu-id="4cf81-119">单击“中断”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-119">Click Discontinue.</span></span>
    * <span data-ttu-id="4cf81-120">将所选版本的状态从“已共享”更改为“已中断”以使它可删除。</span><span class="sxs-lookup"><span data-stu-id="4cf81-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="4cf81-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-121">Click OK.</span></span>
6. <span data-ttu-id="4cf81-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="4cf81-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4cf81-123">选择状态为“已中断”的此配置的版本。</span><span class="sxs-lookup"><span data-stu-id="4cf81-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="4cf81-124">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-124">Click Delete.</span></span>
8. <span data-ttu-id="4cf81-125">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-125">Click Yes.</span></span>
    * <span data-ttu-id="4cf81-126">请注意，仅所选数据模型配置的草稿版本 2 可用。</span><span class="sxs-lookup"><span data-stu-id="4cf81-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="4cf81-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4cf81-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="4cf81-128">从 LCS 导入数据模型配置的共享版本</span><span class="sxs-lookup"><span data-stu-id="4cf81-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="4cf81-129">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4cf81-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4cf81-130">打开‘Litware 公司’</span><span class="sxs-lookup"><span data-stu-id="4cf81-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="4cf81-131">配置提供程序的存储库列表。</span><span class="sxs-lookup"><span data-stu-id="4cf81-131">configuration provider.</span></span>  
2. <span data-ttu-id="4cf81-132">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-132">Click Repositories.</span></span>
3. <span data-ttu-id="4cf81-133">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-133">Click Open.</span></span>
    * <span data-ttu-id="4cf81-134">选择 LCS 存储库然后打开它。</span><span class="sxs-lookup"><span data-stu-id="4cf81-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="4cf81-135">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4cf81-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4cf81-136">选择版本列表中“示例模型配置”的第一个版本。</span><span class="sxs-lookup"><span data-stu-id="4cf81-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="4cf81-137">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-137">Click Import.</span></span>
6. <span data-ttu-id="4cf81-138">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-138">Click Yes.</span></span>
    * <span data-ttu-id="4cf81-139">确认将所选版本从 LCS 导入。</span><span class="sxs-lookup"><span data-stu-id="4cf81-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="4cf81-140">请注意，信息消息（在窗体上方）确认所选版本导入的成功完成。</span><span class="sxs-lookup"><span data-stu-id="4cf81-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="4cf81-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4cf81-141">Close the page.</span></span>
8. <span data-ttu-id="4cf81-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4cf81-142">Close the page.</span></span>
9. <span data-ttu-id="4cf81-143">单击“配置”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-143">Click Configurations.</span></span>
10. <span data-ttu-id="4cf81-144">在树结构中，选择“示例模型配置”。</span><span class="sxs-lookup"><span data-stu-id="4cf81-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="4cf81-145">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="4cf81-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4cf81-146">选择状态为“已共享”的此配置的版本。</span><span class="sxs-lookup"><span data-stu-id="4cf81-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="4cf81-147">请注意，所选数据模型配置的共享版本 1 现在也可用。</span><span class="sxs-lookup"><span data-stu-id="4cf81-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

