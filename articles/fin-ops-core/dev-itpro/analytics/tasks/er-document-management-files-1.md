---
title: ER 在格式输出中使用票据管理文件（第 1 部分 - 准备数据模型）
description: 以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b82b1719990caeb1b383ab806a3e09a4c4a6e41a
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026126"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="e55bb-103">ER 在格式输出中使用票据管理文件（第 1 部分 - 准备数据模型）</span><span class="sxs-lookup"><span data-stu-id="e55bb-103">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e55bb-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便在 ER 输出中使用票据管理文件（附件）。</span><span class="sxs-lookup"><span data-stu-id="e55bb-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="e55bb-105">这些步骤可以在任何公司执行。</span><span class="sxs-lookup"><span data-stu-id="e55bb-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="e55bb-106">为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="e55bb-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="e55bb-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="e55bb-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="e55bb-108">访问 Microsoft 提供的配置列表</span><span class="sxs-lookup"><span data-stu-id="e55bb-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="e55bb-109">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e55bb-110">确保“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="e55bb-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="e55bb-111">提供程序可用且标记为有效。</span><span class="sxs-lookup"><span data-stu-id="e55bb-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="e55bb-112">选择“Litware 公司”</span><span class="sxs-lookup"><span data-stu-id="e55bb-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="e55bb-113">提供程序。</span><span class="sxs-lookup"><span data-stu-id="e55bb-113">provider.</span></span>
3. <span data-ttu-id="e55bb-114">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-114">Click Repositories.</span></span>
    * <span data-ttu-id="e55bb-115">如果已存在“运营资源”类型的存储库，请跳过当前子任务的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="e55bb-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="e55bb-116">单击“添加”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="e55bb-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="e55bb-117">在“配置存储库类型”字段中，输入“运营资源”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="e55bb-118">单击“创建存储库”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-118">Click Create repository.</span></span>
7. <span data-ttu-id="e55bb-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="e55bb-120">获取 Microsoft 提供的客户发票模型配置</span><span class="sxs-lookup"><span data-stu-id="e55bb-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="e55bb-121">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-121">Click Show filters.</span></span>
2. <span data-ttu-id="e55bb-122">应用下面的筛选器：在“名称”字段中输入以“开头为”筛选器运算符开始的“运营资源”筛选器值；在“描述”字段中输入以“开头为”筛选器运算符开始的筛选器值</span><span class="sxs-lookup"><span data-stu-id="e55bb-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="e55bb-123">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-123">Click Show filters.</span></span>
4. <span data-ttu-id="e55bb-124">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-124">Click Open.</span></span>
5. <span data-ttu-id="e55bb-125">在树中，选择“客户发票模型”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="e55bb-126">选择模型配置“客户发票模型”将其导入。</span><span class="sxs-lookup"><span data-stu-id="e55bb-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="e55bb-127">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-127">Click Import.</span></span>
    * <span data-ttu-id="e55bb-128">单击所选配置版本 1 的“导入”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="e55bb-129">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-129">Click Yes.</span></span>
8. <span data-ttu-id="e55bb-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e55bb-130">Close the page.</span></span>
9. <span data-ttu-id="e55bb-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="e55bb-131">Close the page.</span></span>
10. <span data-ttu-id="e55bb-132">单击“申报配置”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="e55bb-133">在树中，选择“客户发票模型”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="e55bb-134">创建衍生模型以支持访问票据管理文件。</span><span class="sxs-lookup"><span data-stu-id="e55bb-134">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="e55bb-135">您将创建自己的客户发票模型配置，该配置派生自 Microsoft 提供的配置。</span><span class="sxs-lookup"><span data-stu-id="e55bb-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="e55bb-136">您将使用此配置实施对票据管理文件的访问，并将其提供给您将基于此模型创建的电子票据。</span><span class="sxs-lookup"><span data-stu-id="e55bb-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="e55bb-137">单击“创建配置”，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="e55bb-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="e55bb-138">在"新建"字段中，输入“从以下名称派生：客户发票模型，Microsoft”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="e55bb-139">在“名称”字段中，键入“客户发票模型（自定义）”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="e55bb-140">客户发票模型（自定义）</span><span class="sxs-lookup"><span data-stu-id="e55bb-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="e55bb-141">单击“创建配置”。</span><span class="sxs-lookup"><span data-stu-id="e55bb-141">Click Create configuration.</span></span>

