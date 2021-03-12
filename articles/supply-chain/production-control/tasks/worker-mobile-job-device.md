---
title: 使用移动作业设备配置工作人员
description: 本主题介绍如何给工人的用户帐户分配正确的角色，并使工人执行车间登记。
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89b75936ea9c0f25f82175a1871088da8fd74ad6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980923"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="1bc31-103">使用移动作业设备配置工作人员</span><span class="sxs-lookup"><span data-stu-id="1bc31-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1bc31-104">本主题介绍如何给工人的用户帐户分配正确的角色，并使工人执行车间登记。</span><span class="sxs-lookup"><span data-stu-id="1bc31-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="1bc31-105">验证是否为工人分配了特定角色。</span><span class="sxs-lookup"><span data-stu-id="1bc31-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="1bc31-106">对于此示例，配置工人帐户之前，验证是否为用户“SHANNON”分配了机器操作员角色。</span><span class="sxs-lookup"><span data-stu-id="1bc31-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="1bc31-107">转到 **导航窗格 > 模块 > 系统管理 > 用户 > 用户**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="1bc31-108">在快速筛选器中搜索用户。</span><span class="sxs-lookup"><span data-stu-id="1bc31-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="1bc31-109">在这个例子中，输入 `shannon`。</span><span class="sxs-lookup"><span data-stu-id="1bc31-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="1bc31-110">在显示的用户帐户的 **用户 ID** 列中选择链接。</span><span class="sxs-lookup"><span data-stu-id="1bc31-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="1bc31-111">在 **用户的角色** 树中，选择 **角色 > 机器操作员**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="1bc31-112">关闭 **用户详细信息** 和 **用户** 页回到主页。</span><span class="sxs-lookup"><span data-stu-id="1bc31-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="1bc31-113">配置工人帐户</span><span class="sxs-lookup"><span data-stu-id="1bc31-113">Configure worker account</span></span>
1. <span data-ttu-id="1bc31-114">转到 **导航窗格 > 模块 > 人力资源 > 工人 > 工人**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="1bc31-115">在快速筛选器中搜索用户。</span><span class="sxs-lookup"><span data-stu-id="1bc31-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="1bc31-116">在这个例子中，输入 `shannon`。</span><span class="sxs-lookup"><span data-stu-id="1bc31-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="1bc31-117">在显示的用户帐户的 **名称** 列中选择链接。</span><span class="sxs-lookup"><span data-stu-id="1bc31-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="1bc31-118">选择 **时间登记** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="1bc31-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="1bc31-119">选择 **在登记终端上启用**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="1bc31-120">在下列字段中输入或选择值：</span><span class="sxs-lookup"><span data-stu-id="1bc31-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="1bc31-121">**计算组**</span><span class="sxs-lookup"><span data-stu-id="1bc31-121">**Calculation group**</span></span>  
    - <span data-ttu-id="1bc31-122">**默认计算组**</span><span class="sxs-lookup"><span data-stu-id="1bc31-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="1bc31-123">**审核组**</span><span class="sxs-lookup"><span data-stu-id="1bc31-123">**Approval group**</span></span>  
    - <span data-ttu-id="1bc31-124">**标准模板**</span><span class="sxs-lookup"><span data-stu-id="1bc31-124">**Standard profile**</span></span>  
    - <span data-ttu-id="1bc31-125">**模板组**</span><span class="sxs-lookup"><span data-stu-id="1bc31-125">**Profile group**</span></span>  

7. <span data-ttu-id="1bc31-126">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-126">Select **OK**.</span></span>
8. <span data-ttu-id="1bc31-127">选择 **编辑** 为新时期登记的工人输入一个标记编号。</span><span class="sxs-lookup"><span data-stu-id="1bc31-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="1bc31-128">在 **标记 ID** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="1bc31-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="1bc31-129">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-129">Select **Save**.</span></span>
10. <span data-ttu-id="1bc31-130">关闭 **工人详细信息** 和 **工人** 页。</span><span class="sxs-lookup"><span data-stu-id="1bc31-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="1bc31-131">将工人分配到设备组</span><span class="sxs-lookup"><span data-stu-id="1bc31-131">Assign worker to device group</span></span>
1. <span data-ttu-id="1bc31-132">转到 **生产控制 > 设置 > 制造执行 > 为设备配置作业卡**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="1bc31-133">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-133">Select **Add**.</span></span>
3. <span data-ttu-id="1bc31-134">在列表中，选择所需的工人。</span><span class="sxs-lookup"><span data-stu-id="1bc31-134">In the list, select the desired worker.</span></span> <span data-ttu-id="1bc31-135">在这个例子中，选择 **SHANNON**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="1bc31-136">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-136">Select **OK**.</span></span>
5. <span data-ttu-id="1bc31-137">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="1bc31-137">Select **Edit**.</span></span>
6. <span data-ttu-id="1bc31-138">在 **生产单位** 字段，您可以设置工人的默认筛选器。</span><span class="sxs-lookup"><span data-stu-id="1bc31-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="1bc31-139">这将确保在工作人员登录到设备时，只显示所选生产单位的生产作业。</span><span class="sxs-lookup"><span data-stu-id="1bc31-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="1bc31-140">输入所需值。</span><span class="sxs-lookup"><span data-stu-id="1bc31-140">Enter the desired value.</span></span>
7. <span data-ttu-id="1bc31-141">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1bc31-141">Close the page.</span></span>

