---
title: 简化的员工条目和导航
description: Dynamics 365 for Talent 中的工作人员的数据输入已得到增强，允许所有员工（过去、现在或将来）快速输入。 已更新简化/整合的导航模型，可以快速查找相关信息并查看和进行任何必要的更新。
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: be0253ffc4396f36050ef02c51a20d378e44473d
ms.sourcegitcommit: 4176c333ce3f88c5c68e95bd47e5791d32365dd2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "1918187"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="c511f-104">简化的员工条目和导航</span><span class="sxs-lookup"><span data-stu-id="c511f-104">Streamlined employee entry and navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c511f-105">Dynamics 365 for Talent 允许高效输入员工和雇用数据。</span><span class="sxs-lookup"><span data-stu-id="c511f-105">Dynamics 365 for Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="c511f-106">您可以快速更新过去、现在和将来员工和合同工的工作历史信息。</span><span class="sxs-lookup"><span data-stu-id="c511f-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="c511f-107">您还可以启用简化的导航体验，来快速查找相关信息并进行必要的更改。</span><span class="sxs-lookup"><span data-stu-id="c511f-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="c511f-108">此功能现在可在沙盒环境中使用。</span><span class="sxs-lookup"><span data-stu-id="c511f-108">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="c511f-109">要打开此功能，请导航至**系统管理 > 链接 > 设置 > 系统参数 > 预览功能**。</span><span class="sxs-lookup"><span data-stu-id="c511f-109">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="c511f-110">选择**增强的工作人员窗体和导航**。</span><span class="sxs-lookup"><span data-stu-id="c511f-110">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="c511f-111">这将为所有用户启用这些更改。</span><span class="sxs-lookup"><span data-stu-id="c511f-111">This will enable these changes for all users.</span></span> <span data-ttu-id="c511f-112">您可以随时关闭此选项。</span><span class="sxs-lookup"><span data-stu-id="c511f-112">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="c511f-113">视图选项</span><span class="sxs-lookup"><span data-stu-id="c511f-113">View options</span></span>

<span data-ttu-id="c511f-114">您可以使用工作人员窗体上的**查看选项**从单个列表中选择员工和合同工的任意组合。</span><span class="sxs-lookup"><span data-stu-id="c511f-114">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="c511f-115">通过这些选项，您可以跨法人查看工作人员或查看您当前登录的法人的工作人员。</span><span class="sxs-lookup"><span data-stu-id="c511f-115">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="c511f-116">您还可以查看有效、待定和离职的工作人员，您可以根据工作人员的类型（员工或合同工）限定结果。</span><span class="sxs-lookup"><span data-stu-id="c511f-116">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="c511f-117">如果启用了高级安全性，您将只能看到您有权访问的法人的员工和合同工。</span><span class="sxs-lookup"><span data-stu-id="c511f-117">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="c511f-118">列表视图中的列会根据您的选择而更改。</span><span class="sxs-lookup"><span data-stu-id="c511f-118">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="c511f-119">例如，在查看离职员工时，终止雇用日期和原因代码将显示为列表中的其他列。</span><span class="sxs-lookup"><span data-stu-id="c511f-119">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="c511f-120">[![视图选项](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="c511f-120">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="c511f-121">导航和横幅</span><span class="sxs-lookup"><span data-stu-id="c511f-121">Navigation and banner</span></span>

<span data-ttu-id="c511f-122">横幅显示每个工人的关键信息。</span><span class="sxs-lookup"><span data-stu-id="c511f-122">A banner displays key information for each worker.</span></span> <span data-ttu-id="c511f-123">有效工作人员的横幅显示以下字段：</span><span class="sxs-lookup"><span data-stu-id="c511f-123">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="c511f-124">**称谓**</span><span class="sxs-lookup"><span data-stu-id="c511f-124">**Title**</span></span>
- <span data-ttu-id="c511f-125">**部门**</span><span class="sxs-lookup"><span data-stu-id="c511f-125">**Department**</span></span>
- <span data-ttu-id="c511f-126">**职位类型**</span><span class="sxs-lookup"><span data-stu-id="c511f-126">**Position type**</span></span>
- <span data-ttu-id="c511f-127">**工作人员类型**</span><span class="sxs-lookup"><span data-stu-id="c511f-127">**Worker type**</span></span>
- <span data-ttu-id="c511f-128">**经理**</span><span class="sxs-lookup"><span data-stu-id="c511f-128">**Manager**</span></span>
- <span data-ttu-id="c511f-129">**法人**</span><span class="sxs-lookup"><span data-stu-id="c511f-129">**Legal entity**</span></span>

<span data-ttu-id="c511f-130">离职工作人员的横幅显示以下字段：</span><span class="sxs-lookup"><span data-stu-id="c511f-130">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="c511f-131">**离职日期**</span><span class="sxs-lookup"><span data-stu-id="c511f-131">**Exited date**</span></span>
- <span data-ttu-id="c511f-132">**原因**</span><span class="sxs-lookup"><span data-stu-id="c511f-132">**Reason**</span></span>

<span data-ttu-id="c511f-133">待定员工的横幅显示以下字段：</span><span class="sxs-lookup"><span data-stu-id="c511f-133">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="c511f-134">**称谓**</span><span class="sxs-lookup"><span data-stu-id="c511f-134">**Title**</span></span>
- <span data-ttu-id="c511f-135">**部门**</span><span class="sxs-lookup"><span data-stu-id="c511f-135">**Department**</span></span>
- <span data-ttu-id="c511f-136">**职位类型**</span><span class="sxs-lookup"><span data-stu-id="c511f-136">**Position type**</span></span>
- <span data-ttu-id="c511f-137">**经理**</span><span class="sxs-lookup"><span data-stu-id="c511f-137">**Manager**</span></span>
- <span data-ttu-id="c511f-138">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="c511f-138">**Starting date**</span></span>
- <span data-ttu-id="c511f-139">**法人**</span><span class="sxs-lookup"><span data-stu-id="c511f-139">**Legal entity**</span></span>

<span data-ttu-id="c511f-140">工作人员页面的操作窗格已重新安排，以包含更少的选项。</span><span class="sxs-lookup"><span data-stu-id="c511f-140">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="c511f-141">信息现在按以下类别管理：</span><span class="sxs-lookup"><span data-stu-id="c511f-141">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="c511f-142">工作</span><span class="sxs-lookup"><span data-stu-id="c511f-142">Work</span></span>
- <span data-ttu-id="c511f-143">人员</span><span class="sxs-lookup"><span data-stu-id="c511f-143">Person</span></span>
- <span data-ttu-id="c511f-144">离开</span><span class="sxs-lookup"><span data-stu-id="c511f-144">Leave</span></span>
- <span data-ttu-id="c511f-145">薪酬</span><span class="sxs-lookup"><span data-stu-id="c511f-145">Compensation</span></span>
- <span data-ttu-id="c511f-146">福利</span><span class="sxs-lookup"><span data-stu-id="c511f-146">Benefits</span></span>
- <span data-ttu-id="c511f-147">合规性</span><span class="sxs-lookup"><span data-stu-id="c511f-147">Compliance</span></span>

<span data-ttu-id="c511f-148">此外，主工作人员页面上的新**链接**选项卡为用户提供了访问工作人员所有相关信息的中心位置。</span><span class="sxs-lookup"><span data-stu-id="c511f-148">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="c511f-149">由于这些更改，信息可能会出现在您习惯的不同位置。</span><span class="sxs-lookup"><span data-stu-id="c511f-149">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="c511f-150">例如，先前显示在工作人员窗体上的工资单信息现在显示在**薪酬 > 工资单**下的操作窗格中，而**个人信息**选项卡现在具有**更多信息**按钮，可以隐藏不经常访问的字段。</span><span class="sxs-lookup"><span data-stu-id="c511f-150">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="c511f-151">[![横幅](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="c511f-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="c511f-152">工作历史记录</span><span class="sxs-lookup"><span data-stu-id="c511f-152">Work history</span></span>

<span data-ttu-id="c511f-153">**工作历史记录**选项卡显示所有法人的工作历史记录，可供离职、有效和待定的员工和合同工使用。</span><span class="sxs-lookup"><span data-stu-id="c511f-153">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="c511f-154">您现在可以立即查看您有权访问的法人的所有工作历史记录。</span><span class="sxs-lookup"><span data-stu-id="c511f-154">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="c511f-155">此外，您还可以编辑每个工作历史记录条目的信息，而无需更改数据上下文。</span><span class="sxs-lookup"><span data-stu-id="c511f-155">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="c511f-156">您可以直接在页面上更新所有信息。</span><span class="sxs-lookup"><span data-stu-id="c511f-156">You can update all information directly on the page.</span></span> 

<span data-ttu-id="c511f-157">[![工作历史记录](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="c511f-157">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="c511f-158">职位历史记录</span><span class="sxs-lookup"><span data-stu-id="c511f-158">Position history</span></span>

<span data-ttu-id="c511f-159">主工作人员页面上的**职位**选项卡提供了组织内所有职位的完整视图，包括过去、现在和所有将来的分配。</span><span class="sxs-lookup"><span data-stu-id="c511f-159">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="c511f-160">您仍然可以在操作窗格中直接导航到工作人员的职位历史记录。</span><span class="sxs-lookup"><span data-stu-id="c511f-160">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="c511f-161">[![职位](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="c511f-161">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

