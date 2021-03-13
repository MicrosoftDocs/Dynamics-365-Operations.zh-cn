---
title: 将现有活动添加到生产流版本
description: 创建生产流的新版本时，可以选择将为较低版本创建的活动添加到新版本。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff549fd6ed526eefc5514ce2013cc31a700510f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006933"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="d42ba-103">将现有活动添加到生产流版本</span><span class="sxs-lookup"><span data-stu-id="d42ba-103">Add an existing activity to a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d42ba-104">创建生产流的新版本时，可以选择将为较低版本创建的活动添加到新版本。</span><span class="sxs-lookup"><span data-stu-id="d42ba-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="d42ba-105">此过程显示如何在不复制活动的情况下，为现有生产流创建新版本。</span><span class="sxs-lookup"><span data-stu-id="d42ba-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="d42ba-106">在下一步中，将现有活动添加到新版本。</span><span class="sxs-lookup"><span data-stu-id="d42ba-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="d42ba-107">此任务需要已创建了版本和活动的生产流。</span><span class="sxs-lookup"><span data-stu-id="d42ba-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="d42ba-108">创建新的生产流版本</span><span class="sxs-lookup"><span data-stu-id="d42ba-108">Create a new production flow version</span></span>
1. <span data-ttu-id="d42ba-109">转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。</span><span class="sxs-lookup"><span data-stu-id="d42ba-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d42ba-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d42ba-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d42ba-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d42ba-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d42ba-112">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="d42ba-112">Click Edit.</span></span>
5. <span data-ttu-id="d42ba-113">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="d42ba-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="d42ba-114">在“到期日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="d42ba-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="d42ba-115">请注意，创建新生产流版本之前，务必检查有效版本的到期日期和时间。</span><span class="sxs-lookup"><span data-stu-id="d42ba-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="d42ba-116">将使用有效开始日期创建新版本，用于连接到所选版本的到期日期。</span><span class="sxs-lookup"><span data-stu-id="d42ba-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="d42ba-117">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="d42ba-117">Click Add.</span></span>
8. <span data-ttu-id="d42ba-118">在“复制自版本”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="d42ba-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="d42ba-119">如果复制的版本的大多数活动将替换为新活动，则选择“否”将从空版本开始。</span><span class="sxs-lookup"><span data-stu-id="d42ba-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="d42ba-120">将未更改的活动手动添加到活动窗体中“添加现有功能”内。</span><span class="sxs-lookup"><span data-stu-id="d42ba-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="d42ba-121">在“重复看板规则”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="d42ba-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="d42ba-122">如果活动未复制到新版本，则不能在创建新版本时复制看板规则。</span><span class="sxs-lookup"><span data-stu-id="d42ba-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="d42ba-123">相反，您以后将在看板规则窗体中使用创建替换看板功能，以便将原来的生产流版本的看板规则替换为使用新版本的活动的看板规则。</span><span class="sxs-lookup"><span data-stu-id="d42ba-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="d42ba-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d42ba-124">Click OK.</span></span>
11. <span data-ttu-id="d42ba-125">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d42ba-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="d42ba-126">添加现有活动</span><span class="sxs-lookup"><span data-stu-id="d42ba-126">Add an existing activity</span></span>
1. <span data-ttu-id="d42ba-127">单击“活动”。</span><span class="sxs-lookup"><span data-stu-id="d42ba-127">Click Activities.</span></span>
2. <span data-ttu-id="d42ba-128">单击“添加现有”打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d42ba-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="d42ba-129">找到并选择要添加到新生产流版本的现有活动。</span><span class="sxs-lookup"><span data-stu-id="d42ba-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="d42ba-130">请注意，此列表为此生产流的所有以前版本显示为此生产流已创建的所有活动。</span><span class="sxs-lookup"><span data-stu-id="d42ba-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="d42ba-131">在“活动”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d42ba-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="d42ba-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d42ba-132">Click OK.</span></span>

