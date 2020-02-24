---
title: 创建覆盖范围选项
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008168"
---
# <a name="create-coverage-options"></a><span data-ttu-id="684e5-102">创建覆盖范围选项</span><span class="sxs-lookup"><span data-stu-id="684e5-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="684e5-103">Microsoft Dynamics 365 Human Resources 中的覆盖范围选项是供参与者在福利计划或项目中选择的覆盖范围级别，例如医疗计划的“仅限员工”，或人寿保险计划的“2x 薪金”。</span><span class="sxs-lookup"><span data-stu-id="684e5-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="684e5-104">定义后，覆盖范围选项可以重复使用，您可以将一个选项与一个或多个计划相关联。</span><span class="sxs-lookup"><span data-stu-id="684e5-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="684e5-105">定义覆盖范围选项后，将覆盖范围选项附加到福利计划类型中。</span><span class="sxs-lookup"><span data-stu-id="684e5-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="684e5-106">然后计划类型将与福利计划或项目关联。</span><span class="sxs-lookup"><span data-stu-id="684e5-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="684e5-107">与计划类型相关联的覆盖范围选项可用于使用该计划类型创建的所有计划。</span><span class="sxs-lookup"><span data-stu-id="684e5-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="684e5-108">在**福利管理**工作区中，在**设置**下，选择**覆盖范围选项**。</span><span class="sxs-lookup"><span data-stu-id="684e5-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="684e5-109">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="684e5-109">Select **New**.</span></span>

3. <span data-ttu-id="684e5-110">为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="684e5-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="684e5-111">字段</span><span class="sxs-lookup"><span data-stu-id="684e5-111">Field</span></span> | <span data-ttu-id="684e5-112">说明</span><span class="sxs-lookup"><span data-stu-id="684e5-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="684e5-113">**覆盖范围选项**</span><span class="sxs-lookup"><span data-stu-id="684e5-113">**Coverage option**</span></span> | <span data-ttu-id="684e5-114">唯一的覆盖范围选项名称。</span><span class="sxs-lookup"><span data-stu-id="684e5-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="684e5-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="684e5-115">**Description**</span></span> | <span data-ttu-id="684e5-116">覆盖范围选项的描述。</span><span class="sxs-lookup"><span data-stu-id="684e5-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="684e5-117">**覆盖范围代码**</span><span class="sxs-lookup"><span data-stu-id="684e5-117">**Coverage code**</span></span> | <span data-ttu-id="684e5-118">覆盖范围代码为每个合格的已覆盖人员类型分配最小和最大金额。</span><span class="sxs-lookup"><span data-stu-id="684e5-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="684e5-119">覆盖范围代码指示某计划类型覆盖哪些人员以及允许的覆盖范围金额。</span><span class="sxs-lookup"><span data-stu-id="684e5-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="684e5-120">您可以用美元金额或百分比表示覆盖范围金额。</span><span class="sxs-lookup"><span data-stu-id="684e5-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="684e5-121">例如:</span><span class="sxs-lookup"><span data-stu-id="684e5-121">For example:</span></span></br></br><span data-ttu-id="684e5-122">- **Emp+1** – 要取得资格，员工必须选择一个依赖方（如果选择了多个，将不再具有资格）。</span><span class="sxs-lookup"><span data-stu-id="684e5-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="684e5-123">- **Emp+家庭** – 要取得资格，员工必须至少选择两个依赖方。</span><span class="sxs-lookup"><span data-stu-id="684e5-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="684e5-124">**最大数**</span><span class="sxs-lookup"><span data-stu-id="684e5-124">**Maximum number**</span></span> | <span data-ttu-id="684e5-125">最大依赖方数。</span><span class="sxs-lookup"><span data-stu-id="684e5-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="684e5-126">**状态**</span><span class="sxs-lookup"><span data-stu-id="684e5-126">**Status**</span></span> | <span data-ttu-id="684e5-127">覆盖范围选项的状态。</span><span class="sxs-lookup"><span data-stu-id="684e5-127">The status of the coverage option.</span></span> <span data-ttu-id="684e5-128">如果覆盖范围选项的状态设置为“无效”，则不能在计划类型上选择该覆盖范围选项。</span><span class="sxs-lookup"><span data-stu-id="684e5-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="684e5-129">**百分比**</span><span class="sxs-lookup"><span data-stu-id="684e5-129">**Percent**</span></span> | <span data-ttu-id="684e5-130">百分比金额。</span><span class="sxs-lookup"><span data-stu-id="684e5-130">The percent amount.</span></span> <span data-ttu-id="684e5-131">仅当在“覆盖范围代码”字段中选择了“% x 薪金”时，此字段才有效。</span><span class="sxs-lookup"><span data-stu-id="684e5-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="684e5-132">**除数**</span><span class="sxs-lookup"><span data-stu-id="684e5-132">**Divisor**</span></span> | <span data-ttu-id="684e5-133">选择覆盖范围代码 % x 薪金时要在计算中使用的除数。</span><span class="sxs-lookup"><span data-stu-id="684e5-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="684e5-134">**最小百分比**</span><span class="sxs-lookup"><span data-stu-id="684e5-134">**Percent minimum**</span></span> | <span data-ttu-id="684e5-135">选择百分比覆盖范围代码时的最小百分比。</span><span class="sxs-lookup"><span data-stu-id="684e5-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="684e5-136">**最大百分比**</span><span class="sxs-lookup"><span data-stu-id="684e5-136">**Percent maximum**</span></span> | <span data-ttu-id="684e5-137">选择百分比覆盖范围代码时的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="684e5-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="684e5-138">在**个人联系人资格选项**下，将合适的个人联系人资格选项附加到每个覆盖范围选项中。</span><span class="sxs-lookup"><span data-stu-id="684e5-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="684e5-139">在**自助服务**下，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="684e5-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="684e5-140">字段</span><span class="sxs-lookup"><span data-stu-id="684e5-140">Field</span></span> | <span data-ttu-id="684e5-141">说明</span><span class="sxs-lookup"><span data-stu-id="684e5-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="684e5-142">**允许员工缴纳金额**</span><span class="sxs-lookup"><span data-stu-id="684e5-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="684e5-143">指定是否允许员工在选择福利时在福利自助服务上修改缴纳金额。</span><span class="sxs-lookup"><span data-stu-id="684e5-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="684e5-144">如果选中此复选框，系统将根据员工在福利自助服务中输入的缴纳金额来计算福利计划参数。</span><span class="sxs-lookup"><span data-stu-id="684e5-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="684e5-145">**允许员工覆盖范围金额**</span><span class="sxs-lookup"><span data-stu-id="684e5-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="684e5-146">指定是否允许员工在选择福利时在福利自助服务上修改覆盖范围金额。</span><span class="sxs-lookup"><span data-stu-id="684e5-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="684e5-147">如果选中此复选框，系统将根据员工在福利自助服务中输入的覆盖范围金额来计算福利计划参数。</span><span class="sxs-lookup"><span data-stu-id="684e5-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="684e5-148">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="684e5-148">Select **Save**.</span></span> 
