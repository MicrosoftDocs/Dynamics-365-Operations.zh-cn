---
title: 管理购买和出售休假策略
description: 您可以在 Dynamics 365 Human Resources 中让员工可以购买和出售休假。
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 491d1654bd219b487f95a1eb328e574114ec1f9f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051369"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="25c41-103">管理购买和出售休假策略</span><span class="sxs-lookup"><span data-stu-id="25c41-103">Manage buy and sell leave policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="25c41-104">您可以通过创建购买和出售休假策略使员工能够购买和出售休假。</span><span class="sxs-lookup"><span data-stu-id="25c41-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="25c41-105">您可以配置这些策略来使用审批工作流、设置最大金额和费率以及设置购买和出售费率。</span><span class="sxs-lookup"><span data-stu-id="25c41-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="25c41-106">让员工可以购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="25c41-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="25c41-107">在 **休假和缺勤参数** 页面上，为 **允许员工购买休假** 和 **允许员工出售休假** 选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="25c41-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="25c41-108">创建购买和出售休假策略</span><span class="sxs-lookup"><span data-stu-id="25c41-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="25c41-109">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="25c41-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="25c41-110">选择 **购买和出售休假策略**。</span><span class="sxs-lookup"><span data-stu-id="25c41-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="25c41-111">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="25c41-111">Select **New**.</span></span>

4. <span data-ttu-id="25c41-112">在 **购买和出售休假策略** 下为策略输入 **名称** 和 **描述**。</span><span class="sxs-lookup"><span data-stu-id="25c41-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="25c41-113">选择 **策略类型**。</span><span class="sxs-lookup"><span data-stu-id="25c41-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="25c41-114">可用策略类型为 **金额** 和 **每周工时**。</span><span class="sxs-lookup"><span data-stu-id="25c41-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="25c41-115">选择 **金额** 为员工可以购买和出售的最大金额输入 **固定金额**。</span><span class="sxs-lookup"><span data-stu-id="25c41-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="25c41-116">如果选择 **每周工时**，在员工的分配工作时间日历中定义的工作时间用于确定策略的最大金额。</span><span class="sxs-lookup"><span data-stu-id="25c41-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="25c41-117">为策略选择 **开始日期** 和 **结束日期**。</span><span class="sxs-lookup"><span data-stu-id="25c41-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="25c41-118">购买和出售休假的请求只能在此时间范围内提交。</span><span class="sxs-lookup"><span data-stu-id="25c41-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="25c41-119">为策略选择一个 **工作流 ID**。</span><span class="sxs-lookup"><span data-stu-id="25c41-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="25c41-120">任何购买和出售请求都将使用此工作流进行审核和审批。</span><span class="sxs-lookup"><span data-stu-id="25c41-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="25c41-121">在 **购买策略** 下，选择 **全职等效** (FTE)，根据在员工职位中定义的 FTE 按比例分配最大金额。</span><span class="sxs-lookup"><span data-stu-id="25c41-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="25c41-122">如果策略类型是 **金额**，请输入 **最大固定金额**。</span><span class="sxs-lookup"><span data-stu-id="25c41-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="25c41-123">选择 **添加** 为员工购买休假添加休假类型。</span><span class="sxs-lookup"><span data-stu-id="25c41-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="25c41-124">您可以向策略添加多个休假类型。</span><span class="sxs-lookup"><span data-stu-id="25c41-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="25c41-125">为休假类型输入 **服务月数**，可以通过不同的服务月数确定员工可以购买的最大金额。</span><span class="sxs-lookup"><span data-stu-id="25c41-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="25c41-126">为休假类型输入 **最大金额**。</span><span class="sxs-lookup"><span data-stu-id="25c41-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="25c41-127">输入员工购买休假所使用的 **费率**。</span><span class="sxs-lookup"><span data-stu-id="25c41-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="25c41-128">（可选）输入用于购买休假的 **收入代码**。</span><span class="sxs-lookup"><span data-stu-id="25c41-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="25c41-129">（可选）设置是否使用 FTE 确定休假类型的最大金额。</span><span class="sxs-lookup"><span data-stu-id="25c41-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="25c41-130">要创建出售策略，请按照 **出售策略** 下的步骤 8 到 14 操作。</span><span class="sxs-lookup"><span data-stu-id="25c41-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="25c41-131">将购买和出售休假策略添加到休假和缺勤计划中</span><span class="sxs-lookup"><span data-stu-id="25c41-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="25c41-132">在 **休假和缺勤** 页面上，选择一个休假和缺勤计划。</span><span class="sxs-lookup"><span data-stu-id="25c41-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="25c41-133">在 **规则** 下，选择 **购买和出售休假策略**。</span><span class="sxs-lookup"><span data-stu-id="25c41-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="25c41-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="25c41-134">See also</span></span>

[<span data-ttu-id="25c41-135">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="25c41-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="25c41-136">配置休假和缺勤类型</span><span class="sxs-lookup"><span data-stu-id="25c41-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="25c41-137">应计休假和缺勤计划</span><span class="sxs-lookup"><span data-stu-id="25c41-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="25c41-138">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="25c41-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]