---
title: 在供应商设计之间切换
description: 本主题介绍如何在 Finance and Operations 应用与 Common Data Service 之间切换供应商数据集成。
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
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997544"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="d9e7e-103">在供应商设计之间切换</span><span class="sxs-lookup"><span data-stu-id="d9e7e-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="d9e7e-104">供应商数据流</span><span class="sxs-lookup"><span data-stu-id="d9e7e-104">Vendor data flow</span></span> 

<span data-ttu-id="d9e7e-105">如果您选择使用 **客户** 实体来存储 **组织** 类型的供应商，使用 **联系人** 实体来存储 **个人** 类型的供应商，请配置以下工作流。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="d9e7e-106">否则，不需要此配置。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="d9e7e-107">对“组织”类型的供应商使用扩展的供应商设计</span><span class="sxs-lookup"><span data-stu-id="d9e7e-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="d9e7e-108">**Dynamics365FinanceExtended** 解决方案包包含以下工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="d9e7e-109">您将为每个模板创建工作流。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="d9e7e-110">在“客户”实体中创建供应商</span><span class="sxs-lookup"><span data-stu-id="d9e7e-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="d9e7e-111">在“供应商”实体中创建供应商</span><span class="sxs-lookup"><span data-stu-id="d9e7e-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="d9e7e-112">在“客户”实体中更新供应商</span><span class="sxs-lookup"><span data-stu-id="d9e7e-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="d9e7e-113">在“供应商”实体中更新供应商</span><span class="sxs-lookup"><span data-stu-id="d9e7e-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="d9e7e-114">要使用工作流程模板创建新的工作流程，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="d9e7e-115">为 **供应商** 实体创建工作流程，然后选择 **在“客户”实体中创建供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="d9e7e-116">然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-116">Then select **OK**.</span></span> <span data-ttu-id="d9e7e-117">此工作流处理 **客户** 实体的供应商创建方案。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![在“客户”实体中创建供应商工作流程](media/create_process.png)

2. <span data-ttu-id="d9e7e-119">为 **供应商** 实体创建工作流程，然后选择 **在“客户”实体中更新供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="d9e7e-120">然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-120">Then select **OK**.</span></span> <span data-ttu-id="d9e7e-121">此工作流处理 **客户** 实体的供应商更新方案。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="d9e7e-122">为 **客户** 实体创建工作流程，然后选择 **在“供应商”实体中创建供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="d9e7e-123">为 **客户** 实体创建工作流程，然后选择 **在“供应商”实体中更新供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="d9e7e-124">您可以根据需要将工作流配置为实时工作流或后台工作流。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="d9e7e-125">要将工作流配置为后台工作流，请选择 **转换为后台工作流** 。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![“转换为后台工作流”按钮](media/background_workflow.png)

6. <span data-ttu-id="d9e7e-127">启用您为 **客户** 和 **供应商** 实体创建的工作流，以开始使用 **客户** 实体存储 **组织** 类型的供应商信息。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="d9e7e-128">对“个人”类型的供应商使用扩展的供应商设计</span><span class="sxs-lookup"><span data-stu-id="d9e7e-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="d9e7e-129">**Dynamics365FinanceExtended** 解决方案包包含以下工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="d9e7e-130">您将为每个模板创建工作流。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="d9e7e-131">在“供应商”实体中创建“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="d9e7e-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="d9e7e-132">在“联系人”实体中创建“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="d9e7e-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="d9e7e-133">在“联系人”实体中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="d9e7e-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="d9e7e-134">在“供应商”实体中更新“个人”类型的供应商</span><span class="sxs-lookup"><span data-stu-id="d9e7e-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="d9e7e-135">要使用工作流程模板创建新的工作流程，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="d9e7e-136">为 **供应商** 实体创建工作流程，然后选择 **在“联系人”实体中创建“个人”类型的供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="d9e7e-137">然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-137">Then select **OK**.</span></span> <span data-ttu-id="d9e7e-138">此工作流处理 **联系人** 实体的供应商创建方案。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="d9e7e-139">为 **供应商** 实体创建工作流程，然后选择 **在“联系人”实体中更新“个人”类型的供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="d9e7e-140">然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-140">Then select **OK**.</span></span> <span data-ttu-id="d9e7e-141">此工作流处理 **联系人** 实体的供应商更新方案。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="d9e7e-142">为 **联系人** 实体创建工作流程，然后选择 **在“供应商”实体中创建“个人”类型的供应商** 模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="d9e7e-143">为 **联系人** 实体创建工作流程，然后选择 **在“供应商”实体中更新“个人”类型的供应商** 工作流程模板。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="d9e7e-144">您可以根据需要将工作流配置为实时工作流或后台工作流。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="d9e7e-145">要将工作流配置为后台工作流，请选择 **转换为后台工作流** 。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="d9e7e-146">启用您在 **联系人** 和 **供应商** 实体上创建的工作流，以开始使用 **联系人** 实体存储 **个人** 类型的供应商信息。</span><span class="sxs-lookup"><span data-stu-id="d9e7e-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
