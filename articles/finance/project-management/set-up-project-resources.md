---
title: 设置项目资源
description: 本主题提供有关设置或请求项目资源的信息。
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
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760488"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="44e23-103">设置项目资源</span><span class="sxs-lookup"><span data-stu-id="44e23-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44e23-104">您必须设置日历并将其与员工或工作人员关联。</span><span class="sxs-lookup"><span data-stu-id="44e23-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="44e23-105">该日历用于计划项目和预留给该项目的资源的工作时间。</span><span class="sxs-lookup"><span data-stu-id="44e23-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="44e23-106">在日历设置期间，项目经理可以作为资源优化的一部分执行资源均衡。</span><span class="sxs-lookup"><span data-stu-id="44e23-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="44e23-107">基于日历安排，可以对资源设定限制。</span><span class="sxs-lookup"><span data-stu-id="44e23-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="44e23-108">可以在**日历**页中设置日历。</span><span class="sxs-lookup"><span data-stu-id="44e23-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="44e23-109">将工作人员设置为项目资源时，可以从您为其设置资源的公司中工作的工作人员中进行选择。</span><span class="sxs-lookup"><span data-stu-id="44e23-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="44e23-110">或者也可以从您的组织中的其他公司中选择工作人员。</span><span class="sxs-lookup"><span data-stu-id="44e23-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="44e23-111">这些工作人员被称为内部公司资源。</span><span class="sxs-lookup"><span data-stu-id="44e23-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="44e23-112">以下过程阐述了如何将工作人员设置为贵公司中的项目资源以及如何设置内部公司项目资源。</span><span class="sxs-lookup"><span data-stu-id="44e23-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="44e23-113">将工作人员设置为项目资源</span><span class="sxs-lookup"><span data-stu-id="44e23-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="44e23-114">在**工作人员**页的**工作人员**列表内，选择您添加为项目资源的工作人员，然后打开工作人员记录。</span><span class="sxs-lookup"><span data-stu-id="44e23-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="44e23-115">在操作窗格中，选择**项目** &gt; **设置** &gt; **项目设置**。</span><span class="sxs-lookup"><span data-stu-id="44e23-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="44e23-116">选择日历，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="44e23-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="44e23-117">您还可以将资源的默认项目指定为预分配类型。</span><span class="sxs-lookup"><span data-stu-id="44e23-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="44e23-118">当资源经理或项目经理知道资源将提前处理哪些项目时，可以使用预分配。</span><span class="sxs-lookup"><span data-stu-id="44e23-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="44e23-119">预分配还可以基于项目赞助者或客户的请求。</span><span class="sxs-lookup"><span data-stu-id="44e23-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="44e23-120">要预分配一个项目，在**分配项目**页上，在**项目**选项卡上，在**其余项目**列表中，选择相应的项目。</span><span class="sxs-lookup"><span data-stu-id="44e23-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="44e23-121">设置内部公司资源</span><span class="sxs-lookup"><span data-stu-id="44e23-121">Set up an intercompany resource</span></span>

<span data-ttu-id="44e23-122">将工作人员设置为内部公司资源时，必须完成借出公司和借入公司中的设置。</span><span class="sxs-lookup"><span data-stu-id="44e23-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="44e23-123">在借出公司中</span><span class="sxs-lookup"><span data-stu-id="44e23-123">In the lending company</span></span>

1. <span data-ttu-id="44e23-124">在 Finance 中，验证已选择借出公司，然后完成上一部分“将工作人员设置为项目资源”中的过程。</span><span class="sxs-lookup"><span data-stu-id="44e23-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="44e23-125">在**内部公司会计**页，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="44e23-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="44e23-126">在**法人 ID** 字段中，选择借出公司。</span><span class="sxs-lookup"><span data-stu-id="44e23-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="44e23-127">根据需要填写其余字段，然后选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="44e23-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="44e23-128">在**转让价格**页，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="44e23-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="44e23-129">在**借入实体**字段中，选择适当的公司。</span><span class="sxs-lookup"><span data-stu-id="44e23-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="44e23-130">如果要仅借给借入公司您在此部分开始时创建的资源，请在**资源**字段中选择您创建的资源的名称。</span><span class="sxs-lookup"><span data-stu-id="44e23-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="44e23-131">如果要将公司内的所有资源都提供给借入公司，请将**资源**字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="44e23-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="44e23-132">在**项目管理与核算参数**页的**内部公司**选项卡上，将**启用公司间资源计划编制和工时单**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="44e23-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="44e23-133">在借入公司中</span><span class="sxs-lookup"><span data-stu-id="44e23-133">In the borrowing company</span></span>

- <span data-ttu-id="44e23-134">在**资源列表**页上的搜索筛选器中，输入您为借出公司创建的资源名称，以验证借入公司的资源列表中是否包含此名称。</span><span class="sxs-lookup"><span data-stu-id="44e23-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="44e23-135">请求项目资源</span><span class="sxs-lookup"><span data-stu-id="44e23-135">Request project resources</span></span>
<span data-ttu-id="44e23-136">项目资源计划功能仅支持资源经理为约定或项目分配雇用资源。</span><span class="sxs-lookup"><span data-stu-id="44e23-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="44e23-137">若要启用此功能，请完成以下任务，或验证是否已完成这些任务：</span><span class="sxs-lookup"><span data-stu-id="44e23-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="44e23-138">设置编号规则。</span><span class="sxs-lookup"><span data-stu-id="44e23-138">Set up number sequences.</span></span>
- <span data-ttu-id="44e23-139">设置项目管理与核算工作流。</span><span class="sxs-lookup"><span data-stu-id="44e23-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="44e23-140">启用资源请求工作流。</span><span class="sxs-lookup"><span data-stu-id="44e23-140">Enable resource request workflows.</span></span>

<span data-ttu-id="44e23-141">完成前面的任务后，可以根据需要完成下面的任务：</span><span class="sxs-lookup"><span data-stu-id="44e23-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="44e23-142">从软性预订雇用资源创建资源请求。</span><span class="sxs-lookup"><span data-stu-id="44e23-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="44e23-143">监控资源请求。</span><span class="sxs-lookup"><span data-stu-id="44e23-143">Monitor resource requests.</span></span>
- <span data-ttu-id="44e23-144">实施资源请求。</span><span class="sxs-lookup"><span data-stu-id="44e23-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="44e23-145">从 WBS 请求雇用资源。</span><span class="sxs-lookup"><span data-stu-id="44e23-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="44e23-146">在不请求雇用资源的情况下为项目预订资源。</span><span class="sxs-lookup"><span data-stu-id="44e23-146">Book resources to a project without having a request for a staffed resource.</span></span>
