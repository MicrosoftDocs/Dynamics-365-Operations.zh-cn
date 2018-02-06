--- 
title: "使用移动作业设备配置工作人员"
description: "该过程向您显示如何给工作人员的用户帐户分配正确的角色，并使工作人员执行车间登记。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: f9de2f79c68fead5ede714ff05bba97118874aad
ms.contentlocale: zh-cn
ms.lasthandoff: 02/06/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="6a604-103">使用移动作业设备配置工作人员</span><span class="sxs-lookup"><span data-stu-id="6a604-103">Configure a worker using the mobile job device</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a604-104">该过程向您显示如何给工作人员的用户帐户分配正确的角色，并使工作人员执行车间登记。</span><span class="sxs-lookup"><span data-stu-id="6a604-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="6a604-105">将角色分配给用户帐户</span><span class="sxs-lookup"><span data-stu-id="6a604-105">Assign roles to user account</span></span>
1. <span data-ttu-id="6a604-106">转到“系统管理”>“用户”>“用户”。</span><span class="sxs-lookup"><span data-stu-id="6a604-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="6a604-107">使用“快速筛选器”以筛选用户帐户与机器操作员角色关联的工作人员姓名。</span><span class="sxs-lookup"><span data-stu-id="6a604-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="6a604-108">在示例数据中，名称应为“Shannon”。</span><span class="sxs-lookup"><span data-stu-id="6a604-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="6a604-109">突出显示用户帐户记录。</span><span class="sxs-lookup"><span data-stu-id="6a604-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="6a604-110">在此列表中，单击在所选行的“名称”链接以查看用户帐户的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6a604-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="6a604-111">在树形图中，请选择“角色\机器操作员”。</span><span class="sxs-lookup"><span data-stu-id="6a604-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="6a604-112">关闭用户帐户详细信息页。</span><span class="sxs-lookup"><span data-stu-id="6a604-112">Close the user account details page.</span></span>
7. <span data-ttu-id="6a604-113">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6a604-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="6a604-114">配置工作人员帐户。</span><span class="sxs-lookup"><span data-stu-id="6a604-114">Configure worker account.</span></span>
1. <span data-ttu-id="6a604-115">转到“人力资源”>“工作人员”>“工作人员”。</span><span class="sxs-lookup"><span data-stu-id="6a604-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="6a604-116">使用“快速筛选器”以筛选用户帐户与机器操作员角色关联的工作人员姓名。</span><span class="sxs-lookup"><span data-stu-id="6a604-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="6a604-117">在示例数据中，名称应为“Shannon”。</span><span class="sxs-lookup"><span data-stu-id="6a604-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="6a604-118">突出显示用户帐户记录。</span><span class="sxs-lookup"><span data-stu-id="6a604-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="6a604-119">在此列表中，单击在所选行的“名称”链接以查看用户帐户的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6a604-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="6a604-120">单击“雇用”选项卡。</span><span class="sxs-lookup"><span data-stu-id="6a604-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="6a604-121">展开“时间登记”快速选项卡并单击“激活登记终端”。</span><span class="sxs-lookup"><span data-stu-id="6a604-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="6a604-122">单击“激活登记终端”。</span><span class="sxs-lookup"><span data-stu-id="6a604-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="6a604-123">在“计算组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6a604-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="6a604-124">在“默认计算组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6a604-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="6a604-125">在“批准组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6a604-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="6a604-126">在“标准模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6a604-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="6a604-127">在“模板组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6a604-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="6a604-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6a604-128">Click OK.</span></span>
14. <span data-ttu-id="6a604-129">单击“编辑”为新时期登记的工作人员输入一个标记编号。</span><span class="sxs-lookup"><span data-stu-id="6a604-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="6a604-130">在“标记 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6a604-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="6a604-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6a604-131">Click Save.</span></span>
17. <span data-ttu-id="6a604-132">使用“保存记录”快捷方式。</span><span class="sxs-lookup"><span data-stu-id="6a604-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="6a604-133">关闭工作人员详细信息页</span><span class="sxs-lookup"><span data-stu-id="6a604-133">Close the worker details page.</span></span>
19. <span data-ttu-id="6a604-134">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6a604-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="6a604-135">将工作人员分配到设备组。</span><span class="sxs-lookup"><span data-stu-id="6a604-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="6a604-136">转到“生产控制”>“设置”>“制造执行”>“为设备配置作业卡”。</span><span class="sxs-lookup"><span data-stu-id="6a604-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="6a604-137">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="6a604-137">Click Add.</span></span>
3. <span data-ttu-id="6a604-138">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="6a604-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6a604-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="6a604-139">Click OK.</span></span>
5. <span data-ttu-id="6a604-140">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="6a604-140">Click Edit.</span></span>
6. <span data-ttu-id="6a604-141">在“生产单位”字段，您可以设置工作人员的默认筛选器。</span><span class="sxs-lookup"><span data-stu-id="6a604-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="6a604-142">这将确保在工作人员登录到设备时，只显示所选生产单位的生产作业。</span><span class="sxs-lookup"><span data-stu-id="6a604-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="6a604-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6a604-143">Close the page.</span></span>

