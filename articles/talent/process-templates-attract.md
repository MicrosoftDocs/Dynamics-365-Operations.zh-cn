---
title: 在 Attract 中创建流程模板
description: 此主题提供有关如何在 Attract 中创建流程模板的信息。
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 2b9cac68093be65584192757229c20b1a1546342
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2019
ms.locfileid: "303417"
---
# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="90d6f-103">在 Attract 中创建流程模板</span><span class="sxs-lookup"><span data-stu-id="90d6f-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="90d6f-104">*招聘流程模板*包含应作为工作招聘流程的一部分包含的所有活动。</span><span class="sxs-lookup"><span data-stu-id="90d6f-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="90d6f-105">此主题描述 Microsoft Dynamics 365 for Talent: Attract 中的流程模板元素。</span><span class="sxs-lookup"><span data-stu-id="90d6f-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="90d6f-106">它还介绍了如何创建模板。</span><span class="sxs-lookup"><span data-stu-id="90d6f-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="90d6f-107">模板创建是 Attract 的综合招聘附件的一部分。</span><span class="sxs-lookup"><span data-stu-id="90d6f-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="90d6f-108">模板管理</span><span class="sxs-lookup"><span data-stu-id="90d6f-108">Template management</span></span>

<span data-ttu-id="90d6f-109">组织可以决定是团队成员还是只有管理员可以在 Attract 中创建流程模板。</span><span class="sxs-lookup"><span data-stu-id="90d6f-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="90d6f-110">若要配置模板管理，请转到**管理员中心** \> **模板管理**。</span><span class="sxs-lookup"><span data-stu-id="90d6f-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="90d6f-111">要允许团队成员创建自己的模板，请打开模板管理。</span><span class="sxs-lookup"><span data-stu-id="90d6f-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="90d6f-112">如果未打开模板管理，只有管理员才能创建模板。</span><span class="sxs-lookup"><span data-stu-id="90d6f-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="90d6f-113">默认模板</span><span class="sxs-lookup"><span data-stu-id="90d6f-113">Default template</span></span>

<span data-ttu-id="90d6f-114">只有管理员可以设置默认模板。</span><span class="sxs-lookup"><span data-stu-id="90d6f-114">Only admins can set the default template.</span></span> <span data-ttu-id="90d6f-115">如果创建工作时未选择模板，将使用默认模板。</span><span class="sxs-lookup"><span data-stu-id="90d6f-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="90d6f-116">若要设置默认模板，请转到**管理员中心** \> **模板管理**。</span><span class="sxs-lookup"><span data-stu-id="90d6f-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="90d6f-117">在应是默认模板的模板的卡上，选择省略号按钮 (**...**)，然后选择**设置为默认值**。</span><span class="sxs-lookup"><span data-stu-id="90d6f-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="90d6f-118">创建流程模板</span><span class="sxs-lookup"><span data-stu-id="90d6f-118">Create a process template</span></span>

<span data-ttu-id="90d6f-119">管理员、招聘人员和招聘经理可以创建流程模板。</span><span class="sxs-lookup"><span data-stu-id="90d6f-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="90d6f-120">流程模板包含*阶段*和*活动*。</span><span class="sxs-lookup"><span data-stu-id="90d6f-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="90d6f-121">阶段将一个或多个活动分组到一起。</span><span class="sxs-lookup"><span data-stu-id="90d6f-121">Stages group together one or more activities.</span></span> <span data-ttu-id="90d6f-122">默认情况下，每个流程模板具有应聘者、申请和聘约活动。</span><span class="sxs-lookup"><span data-stu-id="90d6f-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="90d6f-123">包含这些活动的阶段可以重命名。</span><span class="sxs-lookup"><span data-stu-id="90d6f-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="90d6f-124">您可以通过选择 **+ 新建阶段**来添加更多阶段。</span><span class="sxs-lookup"><span data-stu-id="90d6f-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="90d6f-125">您可以通过将活动拖动到相应的阶段或在活动列表中双击它们来将活动添加到阶段。</span><span class="sxs-lookup"><span data-stu-id="90d6f-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="90d6f-126">阶段名称对**申请状态**页上的应聘者可见。</span><span class="sxs-lookup"><span data-stu-id="90d6f-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="90d6f-127">在您为阶段选择名称时应考虑此事实。</span><span class="sxs-lookup"><span data-stu-id="90d6f-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="90d6f-128">若要了解有关活动的详细信息，请参阅 [Attract 中的招聘流程活动](./activities-attract.md)。</span><span class="sxs-lookup"><span data-stu-id="90d6f-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="90d6f-129">请执行以下步骤创建招聘流程模板。</span><span class="sxs-lookup"><span data-stu-id="90d6f-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="90d6f-130">转到**模板**。</span><span class="sxs-lookup"><span data-stu-id="90d6f-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="90d6f-131">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="90d6f-131">Select **New**.</span></span>
3. <span data-ttu-id="90d6f-132">在**模板名称**字段上，请输入模板的名称，然后选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="90d6f-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="90d6f-133">在**选择审核流程**列表中，请选择**默认**以要求审核工作。</span><span class="sxs-lookup"><span data-stu-id="90d6f-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="90d6f-134">选择启用或禁用应聘者。</span><span class="sxs-lookup"><span data-stu-id="90d6f-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="90d6f-135">可选：添加或删除阶段。</span><span class="sxs-lookup"><span data-stu-id="90d6f-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="90d6f-136">若要添加阶段，请选择 **+ 新阶段**。</span><span class="sxs-lookup"><span data-stu-id="90d6f-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="90d6f-137">若要删除阶段，将指针悬停在阶段上，然后选择出现的垃圾桶按钮。</span><span class="sxs-lookup"><span data-stu-id="90d6f-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="90d6f-138">不能删除“应聘者”、“申请”和“聘约”阶段，但可以重命名。</span><span class="sxs-lookup"><span data-stu-id="90d6f-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="90d6f-139">可选：添加或删除活动。</span><span class="sxs-lookup"><span data-stu-id="90d6f-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="90d6f-140">要添加活动，请将其从右侧的活动列表拖到相应的阶段。</span><span class="sxs-lookup"><span data-stu-id="90d6f-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="90d6f-141">或者，双击活动，然后选择要添加到的阶段。</span><span class="sxs-lookup"><span data-stu-id="90d6f-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="90d6f-142">若要删除活动，展开它，然后选择活动标题上的垃圾桶按钮。</span><span class="sxs-lookup"><span data-stu-id="90d6f-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="90d6f-143">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="90d6f-143">Select **Save**.</span></span>
