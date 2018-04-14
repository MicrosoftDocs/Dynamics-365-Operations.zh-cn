--- 
title: "定义呼叫中心渠道和渠道属性"
description: "此程序会逐步演示如何新建零售渠道和定义渠道属性。"
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bfccbaab5b4d0b4d84d1bf344521b22b7a5e6efc
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="define-call-center-channel-and-channel-attributes"></a><span data-ttu-id="12a2e-103">定义呼叫中心渠道和渠道属性</span><span class="sxs-lookup"><span data-stu-id="12a2e-103">Define call center channel and channel attributes</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="12a2e-104">此程序会逐步演示如何新建零售渠道和定义渠道属性。</span><span class="sxs-lookup"><span data-stu-id="12a2e-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="12a2e-105">创建此任务的演示数据公司是 USRT。</span><span class="sxs-lookup"><span data-stu-id="12a2e-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="12a2e-106">此程序是专为零售 IT 角色设计的。</span><span class="sxs-lookup"><span data-stu-id="12a2e-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="12a2e-107">创建新的商店</span><span class="sxs-lookup"><span data-stu-id="12a2e-107">Create new store</span></span>
1. <span data-ttu-id="12a2e-108">转到所有工作区 > 渠道部署。</span><span class="sxs-lookup"><span data-stu-id="12a2e-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="12a2e-109">单击“新建渠道”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-109">Click New channel.</span></span>
3. <span data-ttu-id="12a2e-110">单击“商店”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-110">Click Store.</span></span>
4. <span data-ttu-id="12a2e-111">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="12a2e-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="12a2e-112">在“商店编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="12a2e-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="12a2e-113">在“仓库”字段，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="12a2e-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12a2e-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="12a2e-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="12a2e-116">在“商店时区”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="12a2e-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="12a2e-117">在“渠道配置文件”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="12a2e-118">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="12a2e-119">在“语言”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="12a2e-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12a2e-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="12a2e-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="12a2e-122">在“销售税组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="12a2e-123">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12a2e-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="12a2e-124">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="12a2e-125">在“客户通讯簿”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="12a2e-126">选择用于将客户链接到此商店的通讯簿。</span><span class="sxs-lookup"><span data-stu-id="12a2e-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="12a2e-127">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12a2e-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="12a2e-128">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="12a2e-129">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-129">Click Select.</span></span>
22. <span data-ttu-id="12a2e-130">在“员工通讯簿”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="12a2e-131">选择用于将出纳链接到此商店的通讯簿。</span><span class="sxs-lookup"><span data-stu-id="12a2e-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="12a2e-132">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12a2e-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="12a2e-133">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="12a2e-134">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-134">Click Select.</span></span>
26. <span data-ttu-id="12a2e-135">在“默认客户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="12a2e-136">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="12a2e-137">展开或折叠“屏幕布局”部分。</span><span class="sxs-lookup"><span data-stu-id="12a2e-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="12a2e-138">在“屏幕布局 ID”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="12a2e-139">选择此商店的默认 POS 屏幕布局。</span><span class="sxs-lookup"><span data-stu-id="12a2e-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="12a2e-140">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12a2e-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="12a2e-141">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="12a2e-142">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="12a2e-143">单击“渠道属性”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="12a2e-144">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-144">Click New.</span></span>
35. <span data-ttu-id="12a2e-145">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="12a2e-146">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12a2e-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="12a2e-147">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="12a2e-148">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-148">Click Save.</span></span>
39. <span data-ttu-id="12a2e-149">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12a2e-149">Close the page.</span></span>
40. <span data-ttu-id="12a2e-150">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="12a2e-151">单击“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-151">Click Payment methods.</span></span>
42. <span data-ttu-id="12a2e-152">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-152">Click New.</span></span>
43. <span data-ttu-id="12a2e-153">在“支付方式”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="12a2e-154">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="12a2e-155">展开或折叠“过帐”部分。</span><span class="sxs-lookup"><span data-stu-id="12a2e-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="12a2e-156">在“科目编号”字段中，指定所需的值。</span><span class="sxs-lookup"><span data-stu-id="12a2e-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="12a2e-157">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-157">Click Save.</span></span>
48. <span data-ttu-id="12a2e-158">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12a2e-158">Close the page.</span></span>
49. <span data-ttu-id="12a2e-159">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="12a2e-160">单击“现金清点”，</span><span class="sxs-lookup"><span data-stu-id="12a2e-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="12a2e-161">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-161">Click New.</span></span>
52. <span data-ttu-id="12a2e-162">在“交易记录币种金额”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="12a2e-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="12a2e-163">在“货币”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="12a2e-164">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12a2e-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="12a2e-165">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="12a2e-166">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-166">Click Save.</span></span>
57. <span data-ttu-id="12a2e-167">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12a2e-167">Close the page.</span></span>
58. <span data-ttu-id="12a2e-168">单击“操作窗格”上的“设置”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="12a2e-169">单击“商店定位符组分配”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="12a2e-170">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-170">Click New.</span></span>
61. <span data-ttu-id="12a2e-171">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="12a2e-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="12a2e-172">在“定位器组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="12a2e-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="12a2e-173">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="12a2e-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="12a2e-174">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="12a2e-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="12a2e-175">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="12a2e-175">Click Save.</span></span>
66. <span data-ttu-id="12a2e-176">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="12a2e-176">Close the page.</span></span>


