---
title: 创建新项目
description: 本主题提供有关如何创建新项目的信息。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760483"
---
# <a name="create-a-new-project"></a><span data-ttu-id="31ce9-103">创建新项目</span><span class="sxs-lookup"><span data-stu-id="31ce9-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31ce9-104">若要创建新项目，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="31ce9-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="31ce9-105">在**项目管理**页上，选择**新项目**，并输入以下值：</span><span class="sxs-lookup"><span data-stu-id="31ce9-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="31ce9-106">**项目类型：** 时间和材料</span><span class="sxs-lookup"><span data-stu-id="31ce9-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="31ce9-107">**项目名称：** XYZ 升级第 2 阶段</span><span class="sxs-lookup"><span data-stu-id="31ce9-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="31ce9-108">**项目组：** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="31ce9-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="31ce9-109">**项目合同 ID：** 00000002</span><span class="sxs-lookup"><span data-stu-id="31ce9-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="31ce9-110">选择**创建项目**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="31ce9-111">将资源分配到项目</span><span class="sxs-lookup"><span data-stu-id="31ce9-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="31ce9-112">在**工作人员**页上的**工作人员**列表中，选择您之前为其设置能力的工作人员的记录，并打开工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="31ce9-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="31ce9-113">在操作窗格的**项目**选项卡的**设置**组中，选择**分配项目**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="31ce9-114">在**资源验证项目分配**页的**项目**选项卡的**将项目添加到所选项目**字段中，筛选 **XYZ 升级第 2 阶段**项目。</span><span class="sxs-lookup"><span data-stu-id="31ce9-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="31ce9-115">在**其余项目**窗格中，选择一个项目，然后选择箭头按钮将其添加到**所选项目**窗格中。</span><span class="sxs-lookup"><span data-stu-id="31ce9-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="31ce9-116">您也可以按自己的需要分配资源的类别。</span><span class="sxs-lookup"><span data-stu-id="31ce9-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="31ce9-117">类别类型可以是**成本**或**收入**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="31ce9-118">类别类型由您的组织确定。</span><span class="sxs-lookup"><span data-stu-id="31ce9-118">The category type is determined by your organization.</span></span> <span data-ttu-id="31ce9-119">如果没有为资源分配类别，则 Finance 查找成本和收入工时价格的默认类别。</span><span class="sxs-lookup"><span data-stu-id="31ce9-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="31ce9-120">设置项目资源和角色特征</span><span class="sxs-lookup"><span data-stu-id="31ce9-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="31ce9-121">项目经理可使用项目资源功能创建项目所需的角色。</span><span class="sxs-lookup"><span data-stu-id="31ce9-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="31ce9-122">在确认的资源在预留资源期间仍未知时可以使用角色。</span><span class="sxs-lookup"><span data-stu-id="31ce9-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="31ce9-123">角色可临时预留为计划资源，以便您可以继续项目计划阶段。</span><span class="sxs-lookup"><span data-stu-id="31ce9-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="31ce9-124">[![角色示例](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="31ce9-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="31ce9-125">**场景**：Contoso 被雇用完成具有已审核项目章节的时间和材料项目。</span><span class="sxs-lookup"><span data-stu-id="31ce9-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="31ce9-126">初级项目经理仍在完成项目的工作范围。</span><span class="sxs-lookup"><span data-stu-id="31ce9-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="31ce9-127">资源经理当前正在确定要预留的处理新项目的特定资源。</span><span class="sxs-lookup"><span data-stu-id="31ce9-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="31ce9-128">由于项目的重要性质，项目出资人请求高级项目经理作为其中一个角色。</span><span class="sxs-lookup"><span data-stu-id="31ce9-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="31ce9-129">如果初级项目经理在项目计划期间需要资源信息，资源经理必须获得新的资源并且定义定义系统中的角色。</span><span class="sxs-lookup"><span data-stu-id="31ce9-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="31ce9-130">以下步骤显示资源经理如何设置高级项目经理角色并将资源特性与其关联。</span><span class="sxs-lookup"><span data-stu-id="31ce9-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="31ce9-131">之后，角色可用于搜索符合所需的资源能力的可用资源。</span><span class="sxs-lookup"><span data-stu-id="31ce9-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="31ce9-132">在**设置角色**页上，选择**新建**，并输入以下值：</span><span class="sxs-lookup"><span data-stu-id="31ce9-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="31ce9-133">**角色 ID：** 高级项目经理</span><span class="sxs-lookup"><span data-stu-id="31ce9-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="31ce9-134">**描述：** 高级项目经理</span><span class="sxs-lookup"><span data-stu-id="31ce9-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="31ce9-135">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-135">Select **Create**.</span></span>
3. <span data-ttu-id="31ce9-136">选择**高级项目经理**角色，然后选择**配置特性**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="31ce9-137">在**特性类型**字段中，选择**技能**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="31ce9-138">在**可用特性**字段中，输入要搜索的技能。</span><span class="sxs-lookup"><span data-stu-id="31ce9-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="31ce9-139">在**特性类型**字段中，选择**证书**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="31ce9-140">在**可用特性**字段中，输入您要搜索的证书类型。</span><span class="sxs-lookup"><span data-stu-id="31ce9-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="31ce9-141">将项目资源分配到项目</span><span class="sxs-lookup"><span data-stu-id="31ce9-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="31ce9-142">在**所有项目**页上，选择 **XYZ 升级第 2 阶段**项目。</span><span class="sxs-lookup"><span data-stu-id="31ce9-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="31ce9-143">在**项目团队和计划编制**选项卡上，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="31ce9-144">在**角色**字段中，选择**团队成员**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="31ce9-145">选择**从日历预订**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="31ce9-146">在**资源可用性**页上，选择**查看设置**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="31ce9-147">在**调整视图设置**页上，输入以下值：</span><span class="sxs-lookup"><span data-stu-id="31ce9-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="31ce9-148">**日期范围视图的格式：** 天</span><span class="sxs-lookup"><span data-stu-id="31ce9-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="31ce9-149">**显示可用性描述：** 是</span><span class="sxs-lookup"><span data-stu-id="31ce9-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="31ce9-150">**显示剩余产能：** 是</span><span class="sxs-lookup"><span data-stu-id="31ce9-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="31ce9-151">在资源列表中，选择某一资源。</span><span class="sxs-lookup"><span data-stu-id="31ce9-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="31ce9-152">选择**硬性预订**和**全部产能**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="31ce9-153">将资源分配给默认角色</span><span class="sxs-lookup"><span data-stu-id="31ce9-153">Assign a resource to a default role</span></span>

<span data-ttu-id="31ce9-154">为了帮助项目或资源经理，可以进一步深化到可以预留给项目的资源。</span><span class="sxs-lookup"><span data-stu-id="31ce9-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="31ce9-155">您可以将默认值角色与现有资源或新获取的资源进行关联。</span><span class="sxs-lookup"><span data-stu-id="31ce9-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="31ce9-156">例如，如果雇用了 Daniel，所以就有了经验和技能来填补“业务分析”角色。</span><span class="sxs-lookup"><span data-stu-id="31ce9-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="31ce9-157">资源经理将该角色分配为 Daniel 的默认角色。</span><span class="sxs-lookup"><span data-stu-id="31ce9-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="31ce9-158">因此，资源经理将 Daniel 添加到可处理项目的业务分析池中。</span><span class="sxs-lookup"><span data-stu-id="31ce9-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="31ce9-159">在资源预留期间，项目经理可以筛选可参与项目的角色资源。</span><span class="sxs-lookup"><span data-stu-id="31ce9-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="31ce9-160">在履行资源期间执行多条件决定分析时，他们可以使用此信息作为一个条件。</span><span class="sxs-lookup"><span data-stu-id="31ce9-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="31ce9-161">他们还可以添加其他资源特征到筛选器来搜索具有指定项目的特定技能、教育和经验的资源。</span><span class="sxs-lookup"><span data-stu-id="31ce9-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="31ce9-162">**场景：** 已审核的项目已启动，并且高级项目经理角色在项目计划阶段预留为计划的资源。</span><span class="sxs-lookup"><span data-stu-id="31ce9-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="31ce9-163">资源经理现在已获得履行高级项目经理角色的资源。</span><span class="sxs-lookup"><span data-stu-id="31ce9-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="31ce9-164">在**资源列表**页上，选择 **Daniel Goldschmidt**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="31ce9-165">在**资源角色**页上，选择**新建**，并输入以下值：</span><span class="sxs-lookup"><span data-stu-id="31ce9-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="31ce9-166">**生效日期：** 输入当前日期。</span><span class="sxs-lookup"><span data-stu-id="31ce9-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="31ce9-167">**到期日期：** 输入**从不**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="31ce9-168">**角色：** 输入**高级项目经理**。</span><span class="sxs-lookup"><span data-stu-id="31ce9-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="31ce9-169">选择**保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="31ce9-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="31ce9-170">在**能力**选项卡上，添加 **ProjectMgmt** 技能和 **PMP** 证书。</span><span class="sxs-lookup"><span data-stu-id="31ce9-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
