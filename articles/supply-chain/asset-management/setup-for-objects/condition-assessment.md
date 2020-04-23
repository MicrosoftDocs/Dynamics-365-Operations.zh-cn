---
title: 条件评估
description: 本主题介绍如何在资产管理中为资产创建条件评估模板和登记。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2694b3ee51e2619a94e7ea2f4039fb52adddbbc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208907"
---
# <a name="condition-assessment"></a><span data-ttu-id="954fc-103">条件评估</span><span class="sxs-lookup"><span data-stu-id="954fc-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="954fc-104">本主题介绍如何在资产管理中为资产创建条件评估模板和登记。</span><span class="sxs-lookup"><span data-stu-id="954fc-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="954fc-105">条件评估定期执行，主要目的是为资产创建和维护条件数据。</span><span class="sxs-lookup"><span data-stu-id="954fc-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="954fc-106">从预防性维护角度来看，监视当前条件和剩余寿命之类关键信息至关重要。</span><span class="sxs-lookup"><span data-stu-id="954fc-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="954fc-107">此外，如果定期执行评估，就可以监控和比较工厂内的机器条件。</span><span class="sxs-lookup"><span data-stu-id="954fc-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="954fc-108">条件评估可用于度量和监控设备的各种条件。</span><span class="sxs-lookup"><span data-stu-id="954fc-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="954fc-109">示例：可以度量机器的振动。</span><span class="sxs-lookup"><span data-stu-id="954fc-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="954fc-110">在资产管理中为各种设备登记了振动度量之后，可以搜索最近登记的评估和查看振动度量。</span><span class="sxs-lookup"><span data-stu-id="954fc-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="954fc-111">条件评估是为资产创建的。</span><span class="sxs-lookup"><span data-stu-id="954fc-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="954fc-112">请在执行条件评估过程之前为资产类型设置条件评估模板。</span><span class="sxs-lookup"><span data-stu-id="954fc-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="954fc-113">之所以为条件评估使用模板，是为了避免相似资产的条件数据变更。</span><span class="sxs-lookup"><span data-stu-id="954fc-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="954fc-114">在资产管理中设置和使用条件评估的顺序为：首先设置所需条件评估模板。</span><span class="sxs-lookup"><span data-stu-id="954fc-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="954fc-115">接下来在**资产类型**窗体中将模板与资产类型关联。</span><span class="sxs-lookup"><span data-stu-id="954fc-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="954fc-116">最后可以在**资产**窗体中为资产创建条件评估模板登记。</span><span class="sxs-lookup"><span data-stu-id="954fc-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="954fc-117">创建条件评估模板</span><span class="sxs-lookup"><span data-stu-id="954fc-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="954fc-118">选择**资产管理** > **设置** > **资产类型** > **条件评估**。</span><span class="sxs-lookup"><span data-stu-id="954fc-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="954fc-119">选择**新建**以创建新模板。</span><span class="sxs-lookup"><span data-stu-id="954fc-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="954fc-120">在**模板** 字段中插入模板的 ID。</span><span class="sxs-lookup"><span data-stu-id="954fc-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="954fc-121">在**名称**字段中插入模板的名称。</span><span class="sxs-lookup"><span data-stu-id="954fc-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="954fc-122">在**条件评估行**快速选项卡上，添加条件评估所需行，包括选择相应条件类型和度量单位。</span><span class="sxs-lookup"><span data-stu-id="954fc-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="954fc-123">在**资产类型**快速选项卡上，添加应该使用条件评估模板的资产类型。</span><span class="sxs-lookup"><span data-stu-id="954fc-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="954fc-124">在屏幕顶部**详细信息**组中的**行**和**资产类型**字段中，可以看到与所选条件评估模板关联的评估行和评估类型的数量。</span><span class="sxs-lookup"><span data-stu-id="954fc-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="954fc-125">为资产创建条件评估登记</span><span class="sxs-lookup"><span data-stu-id="954fc-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="954fc-126">选择**资产管理** > **常用** > **资产** > **所有资产**。</span><span class="sxs-lookup"><span data-stu-id="954fc-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="954fc-127">在列表中，选择要为其创建条件评估登记的资产。</span><span class="sxs-lookup"><span data-stu-id="954fc-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="954fc-128">在**常规**选项卡上，单击**条件评估**。</span><span class="sxs-lookup"><span data-stu-id="954fc-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="954fc-129">单击**新建**创建新的登记。</span><span class="sxs-lookup"><span data-stu-id="954fc-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="954fc-130">在**日期**字段中选择条件评估的日期。</span><span class="sxs-lookup"><span data-stu-id="954fc-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="954fc-131">在**工人**字段中选择执行评估登记的工人的姓名。</span><span class="sxs-lookup"><span data-stu-id="954fc-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="954fc-132">在**行**字段中，可以查看为条件评估设置的评估行数量。</span><span class="sxs-lookup"><span data-stu-id="954fc-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="954fc-133">在**模板**字段中选择条件评估的模板。</span><span class="sxs-lookup"><span data-stu-id="954fc-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="954fc-134">将在**名称**字段中自动插入模板的名称，在**条件评估行**快速选项卡上插入关联的登记行。</span><span class="sxs-lookup"><span data-stu-id="954fc-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="954fc-135">可在**注释**快速选项卡上插入与所选条件评估有关的注释。</span><span class="sxs-lookup"><span data-stu-id="954fc-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="954fc-136">在**值**字段中插入每个条件评估行的度量数据。</span><span class="sxs-lookup"><span data-stu-id="954fc-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="954fc-137">可在**条件评估行**快速选项卡 > **注释**字段中插入与所选登记行有关的注释。</span><span class="sxs-lookup"><span data-stu-id="954fc-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="954fc-138">如果添加有关行的注释，将自动选中**注释**复选框。</span><span class="sxs-lookup"><span data-stu-id="954fc-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="954fc-139">为资产创建条件评估登记之后，可以打印条件评估报告。</span><span class="sxs-lookup"><span data-stu-id="954fc-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="954fc-140">也可以为工作订单登记条件评估（**资产管理** > **常用** > **工作订单** > **所有工作订单** > **条件评估**按钮）。</span><span class="sxs-lookup"><span data-stu-id="954fc-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>
