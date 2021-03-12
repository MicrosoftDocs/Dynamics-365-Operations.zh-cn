---
title: 在供应商设计之间切换
description: 本主题介绍如何在 Finance and Operations 应用与 Dataverse 之间切换供应商数据集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: d2c22123d5f05945b34eb107c5b912852aec387a
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744457"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="30a58-103">在供应商设计之间切换</span><span class="sxs-lookup"><span data-stu-id="30a58-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="30a58-104">供应商数据流</span><span class="sxs-lookup"><span data-stu-id="30a58-104">Vendor data flow</span></span> 

<span data-ttu-id="30a58-105">如果您选择使用 **客户** 表来存储 **组织** 类型的供应商，使用 **联系人** 表来存储 **个人** 类型的供应商，请配置以下工作流。</span><span class="sxs-lookup"><span data-stu-id="30a58-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="30a58-106">否则，不需要此配置。</span><span class="sxs-lookup"><span data-stu-id="30a58-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="30a58-107">对“组织”类型的供应商使用扩展的供应商设计</span><span class="sxs-lookup"><span data-stu-id="30a58-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="30a58-108">**Dynamics365FinanceExtended** 解决方案包包含以下工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="30a58-109">您将为每个模板创建工作流。</span><span class="sxs-lookup"><span data-stu-id="30a58-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="30a58-110">在“客户”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="30a58-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="30a58-111">在“供应商”表中创建供应商</span><span class="sxs-lookup"><span data-stu-id="30a58-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="30a58-112">在“客户”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="30a58-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="30a58-113">在“供应商”表中更新供应商</span><span class="sxs-lookup"><span data-stu-id="30a58-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="30a58-114">要使用工作流程模板创建新的工作流程，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="30a58-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="30a58-115">为 **供应商** 表创建工作流程，然后选择 **在“客户”表中创建供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="30a58-116">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="30a58-116">Then select **OK**.</span></span> <span data-ttu-id="30a58-117">此工作流处理 **客户** 表的供应商创建方案。</span><span class="sxs-lookup"><span data-stu-id="30a58-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![在“客户”表中创建供应商工作流程](media/create_process.png)

2. <span data-ttu-id="30a58-119">为 **供应商** 表创建工作流程，然后选择 **在“客户”表中更新供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="30a58-120">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="30a58-120">Then select **OK**.</span></span> <span data-ttu-id="30a58-121">此工作流处理 **客户** 表的供应商更新方案。</span><span class="sxs-lookup"><span data-stu-id="30a58-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="30a58-122">为 **客户** 表创建工作流程，然后选择 **在“供应商”表中创建供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="30a58-123">为 **客户** 表创建工作流程，然后选择 **在“供应商”表中更新供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="30a58-124">您可以根据需要将工作流配置为实时工作流或后台工作流。</span><span class="sxs-lookup"><span data-stu-id="30a58-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="30a58-125">要将工作流配置为后台工作流，请选择 **转换为后台工作流**。</span><span class="sxs-lookup"><span data-stu-id="30a58-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![“转换为后台工作流”按钮](media/background_workflow.png)

6. <span data-ttu-id="30a58-127">启用您为 **客户** 和 **供应商** 表创建的工作流，以开始使用 **客户** 表存储 **组织** 类型的供应商信息。</span><span class="sxs-lookup"><span data-stu-id="30a58-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="30a58-128">对“个人”类型的供应商使用扩展的供应商设计</span><span class="sxs-lookup"><span data-stu-id="30a58-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="30a58-129">**Dynamics365FinanceExtended** 解决方案包包含以下工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="30a58-130">您将为每个模板创建工作流。</span><span class="sxs-lookup"><span data-stu-id="30a58-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="30a58-131">在“供应商”表中创建“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="30a58-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="30a58-132">在“联系人”表中创建“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="30a58-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="30a58-133">在“联系人”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="30a58-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="30a58-134">在“供应商”表中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="30a58-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="30a58-135">要使用工作流程模板创建新的工作流程，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="30a58-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="30a58-136">为 **供应商** 表创建工作流程，然后选择 **在“联系人”表中创建“个人”类型的供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="30a58-137">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="30a58-137">Then select **OK**.</span></span> <span data-ttu-id="30a58-138">此工作流处理 **联系人** 表的供应商创建方案。</span><span class="sxs-lookup"><span data-stu-id="30a58-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="30a58-139">为 **供应商** 表创建工作流程，然后选择 **在“联系人”表中更新“个人”类型的供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="30a58-140">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="30a58-140">Then select **OK**.</span></span> <span data-ttu-id="30a58-141">此工作流处理 **联系人** 表的供应商更新方案。</span><span class="sxs-lookup"><span data-stu-id="30a58-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="30a58-142">为 **联系人** 表创建工作流程，然后选择 **在“供应商”表中创建“个人”类型的供应商** 模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="30a58-143">为 **联系人** 表创建工作流程，然后选择 **在“供应商”表中更新“个人”类型的供应商** 模板。</span><span class="sxs-lookup"><span data-stu-id="30a58-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="30a58-144">您可以根据需要将工作流配置为实时工作流或后台工作流。</span><span class="sxs-lookup"><span data-stu-id="30a58-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="30a58-145">要将工作流配置为后台工作流，请选择 **转换为后台工作流**。</span><span class="sxs-lookup"><span data-stu-id="30a58-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="30a58-146">启用您在 **联系人** 和 **供应商** 表上创建的工作流，以开始使用 **联系人** 表存储 **个人** 类型的供应商信息。</span><span class="sxs-lookup"><span data-stu-id="30a58-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>
