---
title: 客户拥有资产维护工作的计费
description: 本主题说明如何创建、处理以及为完成的客户拥有资产维护工作计费。
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131833"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="89265-103">客户拥有资产维护工作的计费</span><span class="sxs-lookup"><span data-stu-id="89265-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89265-104">*工作订单计费* 功能让您可以创建、处理和为完成的客户拥有资产维护工作计费。</span><span class="sxs-lookup"><span data-stu-id="89265-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="89265-105">此功能让您可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="89265-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="89265-106">将客户连接到他们拥有的资产。</span><span class="sxs-lookup"><span data-stu-id="89265-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="89265-107">在创建工作订单时选择客户并查看该客户拥有的资产。</span><span class="sxs-lookup"><span data-stu-id="89265-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="89265-108">为每个客户设置父项目。</span><span class="sxs-lookup"><span data-stu-id="89265-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="89265-109">根据工作订单登记工时、物料、支出和费用，然后为客户创建发票方案。</span><span class="sxs-lookup"><span data-stu-id="89265-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="89265-110">此外，此功能还提供以下功能：</span><span class="sxs-lookup"><span data-stu-id="89265-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="89265-111">客户父项目的项目合同将自动复制到相关的工作订单项目。</span><span class="sxs-lookup"><span data-stu-id="89265-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="89265-112">资产管理现在可以在工作订单预测和工作订单日记帐上使用 *费用* 项目交易类型。</span><span class="sxs-lookup"><span data-stu-id="89265-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="89265-113">开启客户计费功能</span><span class="sxs-lookup"><span data-stu-id="89265-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="89265-114">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="89265-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="89265-115">管理员可以使用[功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="89265-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="89265-116">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="89265-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="89265-117">**模块**：*项目管理和会计*</span><span class="sxs-lookup"><span data-stu-id="89265-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="89265-118">**功能名称**：*工作订单计费*</span><span class="sxs-lookup"><span data-stu-id="89265-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="89265-119">示例场景</span><span class="sxs-lookup"><span data-stu-id="89265-119">Example scenario</span></span>

<span data-ttu-id="89265-120">若要了解此功能的工作原理，请完成以下示例场景。</span><span class="sxs-lookup"><span data-stu-id="89265-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="89265-121">若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="89265-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="89265-122">开始前，必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="89265-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="89265-123">使用生产系统时，也可以将此场景用作使用此功能的指导。</span><span class="sxs-lookup"><span data-stu-id="89265-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="89265-124">但是，在此情况下，必须替换为您自己的值，而您可能会缺少标准演示数据提供的某些类型的必需记录。</span><span class="sxs-lookup"><span data-stu-id="89265-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="89265-125">步骤 1：为客户创建新的项目合同</span><span class="sxs-lookup"><span data-stu-id="89265-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="89265-126">转到 **项目管理和会计 \> 项目 \> 项目合同**。</span><span class="sxs-lookup"><span data-stu-id="89265-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="89265-127">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="89265-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="89265-128">在 **新建项目合同** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="89265-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="89265-129">**名称**：*Pelican 批发*</span><span class="sxs-lookup"><span data-stu-id="89265-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="89265-130">**融资类型**：*客户*</span><span class="sxs-lookup"><span data-stu-id="89265-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="89265-131">**融资来源**：*US-013*（*Pelican 批发*）</span><span class="sxs-lookup"><span data-stu-id="89265-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="89265-132">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89265-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="89265-133">步骤 2：为客户创建新的父项目</span><span class="sxs-lookup"><span data-stu-id="89265-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="89265-134">您在此处创建的父项目将在为客户创建工作订单时使用。</span><span class="sxs-lookup"><span data-stu-id="89265-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="89265-135">转到 **项目管理和会计 \> 项目 \> 所有项目**。</span><span class="sxs-lookup"><span data-stu-id="89265-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="89265-136">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="89265-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="89265-137">在 **新建项目** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="89265-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="89265-138">**项目类型**：*时间和材料*</span><span class="sxs-lookup"><span data-stu-id="89265-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="89265-139">**项目名称**：*Pelican 批发工作订单*</span><span class="sxs-lookup"><span data-stu-id="89265-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="89265-140">**项目组**：*TM*</span><span class="sxs-lookup"><span data-stu-id="89265-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="89265-141">**项目合同 ID**：*Pelican 批发*（您之前创建的合同）</span><span class="sxs-lookup"><span data-stu-id="89265-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="89265-142">**开始日期：** 选择今天的日期。</span><span class="sxs-lookup"><span data-stu-id="89265-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="89265-143">选择 **创建项目**。</span><span class="sxs-lookup"><span data-stu-id="89265-143">Select **Create project**.</span></span>
1. <span data-ttu-id="89265-144">新项目将打开。</span><span class="sxs-lookup"><span data-stu-id="89265-144">The new project is opened.</span></span> <span data-ttu-id="89265-145">记下 **项目 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="89265-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="89265-146">您稍后必须输入此值。</span><span class="sxs-lookup"><span data-stu-id="89265-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="89265-147">步骤 3：在资产管理中创建新的工作订单类型</span><span class="sxs-lookup"><span data-stu-id="89265-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="89265-148">转到 **资产管理 \> 设置 \> 工作订单 \> 工作订单类型**。</span><span class="sxs-lookup"><span data-stu-id="89265-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="89265-149">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="89265-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="89265-150">新记录将添加到列表中。</span><span class="sxs-lookup"><span data-stu-id="89265-150">A new record is added to the list.</span></span> <span data-ttu-id="89265-151">为它设置以下值：</span><span class="sxs-lookup"><span data-stu-id="89265-151">Set the following values for it:</span></span>

    - <span data-ttu-id="89265-152">**工作订单类型**：*服务*</span><span class="sxs-lookup"><span data-stu-id="89265-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="89265-153">**名称**：*服务工作订单*</span><span class="sxs-lookup"><span data-stu-id="89265-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="89265-154">**工作订单生命周期状态**：*标准*</span><span class="sxs-lookup"><span data-stu-id="89265-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="89265-155">步骤 4：将客户帐户链接到父项目</span><span class="sxs-lookup"><span data-stu-id="89265-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="89265-156">现在，您必须在资产管理中的项目设置中将客户帐户链接到父项目。</span><span class="sxs-lookup"><span data-stu-id="89265-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="89265-157">转到 **资产管理 \> 设置 \> 工作订单 \> 项目设置**。</span><span class="sxs-lookup"><span data-stu-id="89265-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="89265-158">在 **父项目** 选项卡中，选择 **添加** 添加一行。</span><span class="sxs-lookup"><span data-stu-id="89265-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="89265-159">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="89265-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89265-160">**客户帐户**：*US-013* (*Pelican 批发*)</span><span class="sxs-lookup"><span data-stu-id="89265-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="89265-161">**项目 ID：** 输入您之前记下的项目 ID。</span><span class="sxs-lookup"><span data-stu-id="89265-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="89265-162">步骤 5：将项目组和类型链接到工作订单项目</span><span class="sxs-lookup"><span data-stu-id="89265-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="89265-163">您应该仍然在 **项目设置** 页（**资产管理 \> 设置 \> 工作订单 \> 项目设置**）。</span><span class="sxs-lookup"><span data-stu-id="89265-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="89265-164">在 **项目组** 选项卡中，选择 **添加** 添加一行。</span><span class="sxs-lookup"><span data-stu-id="89265-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="89265-165">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="89265-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="89265-166">**工作订单类型**：*服务*（您之前创建的工作订单类型）</span><span class="sxs-lookup"><span data-stu-id="89265-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="89265-167">**项目组**：*TM*</span><span class="sxs-lookup"><span data-stu-id="89265-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="89265-168">工作订单项目上的项目合同始终从父项目继承。</span><span class="sxs-lookup"><span data-stu-id="89265-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="89265-169">步骤 6：将资产链接到客户 ID</span><span class="sxs-lookup"><span data-stu-id="89265-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="89265-170">转到 **资产管理 \> 资产 \> 有效资产**。</span><span class="sxs-lookup"><span data-stu-id="89265-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="89265-171">在 **筛选器** 字段中，输入 *VE-102*，然后选择按 **资产** 筛选。</span><span class="sxs-lookup"><span data-stu-id="89265-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="89265-172">选择资产以打开其设置。</span><span class="sxs-lookup"><span data-stu-id="89265-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="89265-173">在 **客户** 快速选项卡上，将 **客户帐户** 字段设置为 *US-013* (*Pelican 批发*)。</span><span class="sxs-lookup"><span data-stu-id="89265-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="89265-174">**名称** 字段将自动更新为 *Pelican 批发*。</span><span class="sxs-lookup"><span data-stu-id="89265-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="89265-175">步骤 7：在资产上创建新工作订单</span><span class="sxs-lookup"><span data-stu-id="89265-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="89265-176">转到 **资产管理 \> 工作订单 \> 有效工作订单**。</span><span class="sxs-lookup"><span data-stu-id="89265-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="89265-177">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="89265-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="89265-178">在 **创建工作订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="89265-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="89265-179">**工作订单类型**：*服务*</span><span class="sxs-lookup"><span data-stu-id="89265-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="89265-180">**描述**：*维修卡车*</span><span class="sxs-lookup"><span data-stu-id="89265-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="89265-181">**客户帐户**：*US-013* (*Pelican 批发*)</span><span class="sxs-lookup"><span data-stu-id="89265-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="89265-182">**资产**：*VE-102*</span><span class="sxs-lookup"><span data-stu-id="89265-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="89265-183">查找仅显示链接到所选客户帐户的资产。</span><span class="sxs-lookup"><span data-stu-id="89265-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="89265-184">**维护作业类型**：*维修*</span><span class="sxs-lookup"><span data-stu-id="89265-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="89265-185">**贸易**：*机械*</span><span class="sxs-lookup"><span data-stu-id="89265-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="89265-186">**服务级别**：*4*</span><span class="sxs-lookup"><span data-stu-id="89265-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="89265-187">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89265-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="89265-188">步骤 8：查看工作订单并开始处理</span><span class="sxs-lookup"><span data-stu-id="89265-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="89265-189">在本节中，您将处理上一节中创建的工作订单。</span><span class="sxs-lookup"><span data-stu-id="89265-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="89265-190">按照下列步骤验证父项目是否是 *Pelican 批发工作订单* 项目：</span><span class="sxs-lookup"><span data-stu-id="89265-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="89265-191">在 **工作订单维护作业** 部分，选择一行。</span><span class="sxs-lookup"><span data-stu-id="89265-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="89265-192">在 **行详细信息** 快速选项卡上，检查 **项目 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="89265-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="89265-193">它应该是 *\<Parent-Project-ID\>-\<Project-ID\>* 形式的带连字符的数字。</span><span class="sxs-lookup"><span data-stu-id="89265-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="89265-194">此值是一个链接。</span><span class="sxs-lookup"><span data-stu-id="89265-194">This value is a link.</span></span>
    1. <span data-ttu-id="89265-195">选择项目 ID 链接可以打开一个页面，您可以在其中查看父项目和项目名称。</span><span class="sxs-lookup"><span data-stu-id="89265-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="89265-196">在操作窗格的 **工作订单** 选项卡上，在 **生命周期状态** 组中，选择 **更新工作订单状态**。</span><span class="sxs-lookup"><span data-stu-id="89265-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="89265-197">在 **更新工作订单状态** 对话框中的 **选择** 列中，选中 **生命周期状态** 字段设置为 *进行中* 的行的复选框。</span><span class="sxs-lookup"><span data-stu-id="89265-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="89265-198">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89265-198">Select **OK**.</span></span>
1. <span data-ttu-id="89265-199">在 **生命周期状态: 进行中** 对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="89265-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="89265-200">步骤 9：发布在工作订单上花费的工时并创建新发票方案</span><span class="sxs-lookup"><span data-stu-id="89265-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="89265-201">在本节中，您将继续处理在上一节中处理的工作订单。</span><span class="sxs-lookup"><span data-stu-id="89265-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="89265-202">在操作窗格上，在 **工作订单** 选项卡的 **项目** 组中，选择 **日记帐**。</span><span class="sxs-lookup"><span data-stu-id="89265-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="89265-203">**工作订单日记帐** 页将出现。</span><span class="sxs-lookup"><span data-stu-id="89265-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="89265-204">在这里，您可以登记您在工作订单上花费的时间。</span><span class="sxs-lookup"><span data-stu-id="89265-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="89265-205">在 **工时** 快速选项卡中，选择 **添加行**。</span><span class="sxs-lookup"><span data-stu-id="89265-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="89265-206">在新行上，将 **工时** 字段设置为 *4*。</span><span class="sxs-lookup"><span data-stu-id="89265-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="89265-207">在操作窗格上，选择 **过帐日记帐**。</span><span class="sxs-lookup"><span data-stu-id="89265-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="89265-208">关闭 **工作订单日记帐** 页以返回到工作订单。</span><span class="sxs-lookup"><span data-stu-id="89265-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="89265-209">在操作窗格上的 **开票** 选项卡中，选择 **新建发票方案**。</span><span class="sxs-lookup"><span data-stu-id="89265-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="89265-210">在 **创建发票方案** 对话框中的 **项目交易** 部分，为要开票的每一行选中 **选择** 复选框。</span><span class="sxs-lookup"><span data-stu-id="89265-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="89265-211">选择 **确定** 关闭对话框，查看新发票方案。</span><span class="sxs-lookup"><span data-stu-id="89265-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>
