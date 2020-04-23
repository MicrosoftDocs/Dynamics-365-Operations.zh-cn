---
title: 启用牌照标签打印
description: 此主题显示如何在销售领料工作流程中从库存对最后一个物料拣货之后，对串行装运集装箱码 (SSCC) 标签启用自动打印。
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 484a1465dd41429fe201de18aac55f118a483cab
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217003"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="72da5-103">启用牌照标签打印</span><span class="sxs-lookup"><span data-stu-id="72da5-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72da5-104">此主题显示如何在销售领料工作流程中从库存对最后一个物料拣货之后，对串行装运集装箱码 (SSCC) 标签启用自动打印。</span><span class="sxs-lookup"><span data-stu-id="72da5-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="72da5-105">您可以使用演示数据公司 USMF 运行此程序。</span><span class="sxs-lookup"><span data-stu-id="72da5-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="72da5-106">如果您使用自己的数据运行，则须为牌照设置一个数序。</span><span class="sxs-lookup"><span data-stu-id="72da5-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="72da5-107">在您开始此任务前，需要装配一台标签打印机。</span><span class="sxs-lookup"><span data-stu-id="72da5-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="72da5-108">转到“组织管理”>“设置”>“网络打印机”。</span><span class="sxs-lookup"><span data-stu-id="72da5-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="72da5-109">在“操作窗格”中，单击“选项”，然后单击“下载文档路由代理安装程序”按钮。</span><span class="sxs-lookup"><span data-stu-id="72da5-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="72da5-110">运行此安装程序并确认工作网络打印机设置为“主动”，方可继续该程序。</span><span class="sxs-lookup"><span data-stu-id="72da5-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="72da5-111">设置 GS1 公司字头。</span><span class="sxs-lookup"><span data-stu-id="72da5-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="72da5-112">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="72da5-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="72da5-113">在 **GS1 公司前缀**字段中，输入一个 7 位数字的个人 GS1 公司编号。</span><span class="sxs-lookup"><span data-stu-id="72da5-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="72da5-114">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="72da5-114">Select **Save**.</span></span>
4. <span data-ttu-id="72da5-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="72da5-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="72da5-116">设置 SSCC 牌照数序</span><span class="sxs-lookup"><span data-stu-id="72da5-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="72da5-117">转到**导航窗格 > 模块 > 组织管理 > 标号规则 > 编号规则**。</span><span class="sxs-lookup"><span data-stu-id="72da5-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="72da5-118">在**区域**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="72da5-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="72da5-119">在**参考**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="72da5-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="72da5-120">在**公司**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="72da5-121">展开**分段**部分。</span><span class="sxs-lookup"><span data-stu-id="72da5-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="72da5-122">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="72da5-122">Select **Edit**.</span></span>
7. <span data-ttu-id="72da5-123">在**区段**表中，选择第一行</span><span class="sxs-lookup"><span data-stu-id="72da5-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="72da5-124">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="72da5-124">Select **Remove**.</span></span>
9. <span data-ttu-id="72da5-125">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="72da5-125">Select **Remove**.</span></span>
10. <span data-ttu-id="72da5-126">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="72da5-126">Select **Save**.</span></span>
11. <span data-ttu-id="72da5-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="72da5-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="72da5-128">创建文档路径布局</span><span class="sxs-lookup"><span data-stu-id="72da5-128">Create the document route layout</span></span>
1. <span data-ttu-id="72da5-129">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 文档路线选择 > 文档路线选择布局**。</span><span class="sxs-lookup"><span data-stu-id="72da5-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="72da5-130">启用 SSCC 布局。</span><span class="sxs-lookup"><span data-stu-id="72da5-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="72da5-131">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="72da5-131">Select **New**.</span></span>
3. <span data-ttu-id="72da5-132">在**布局 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="72da5-133">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="72da5-134">选择**在文本结尾处插入**。</span><span class="sxs-lookup"><span data-stu-id="72da5-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="72da5-135">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="72da5-135">Select **Save**.</span></span>
7. <span data-ttu-id="72da5-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="72da5-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="72da5-137">设置文档路径</span><span class="sxs-lookup"><span data-stu-id="72da5-137">Set up the document routing</span></span>
1. <span data-ttu-id="72da5-138">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 文档路线选择 > 文档路线选择**。</span><span class="sxs-lookup"><span data-stu-id="72da5-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="72da5-139">在**工作订单类型**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="72da5-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="72da5-140">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="72da5-140">Select **New**.</span></span>
4. <span data-ttu-id="72da5-141">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="72da5-142">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="72da5-143">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="72da5-143">Select **New**.</span></span>
7. <span data-ttu-id="72da5-144">在**布局 ID** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="72da5-145">在**名称**字段中，输入您要使用的打印机名称。</span><span class="sxs-lookup"><span data-stu-id="72da5-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="72da5-146">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="72da5-146">Select **Save**.</span></span>
10. <span data-ttu-id="72da5-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="72da5-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="72da5-148">创建移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="72da5-148">Create mobile device menu</span></span>
1. <span data-ttu-id="72da5-149">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 移动设备 > 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="72da5-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="72da5-150">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="72da5-150">Select **New**.</span></span>
3. <span data-ttu-id="72da5-151">在**菜单项名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="72da5-152">在**标题**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="72da5-153">在**模式**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="72da5-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="72da5-154">在**使用现有工作**字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="72da5-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="72da5-155">在**生成牌照**字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="72da5-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="72da5-156">展开**工作类**部分。</span><span class="sxs-lookup"><span data-stu-id="72da5-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="72da5-157">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="72da5-157">Select **New**.</span></span>
10. <span data-ttu-id="72da5-158">在**工作类 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="72da5-159">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="72da5-159">Select **Save**.</span></span>
12. <span data-ttu-id="72da5-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="72da5-160">Close the page.</span></span>
13. <span data-ttu-id="72da5-161">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 移动设备 > 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="72da5-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="72da5-162">在树形图中，选择您之前已创建的菜单项。</span><span class="sxs-lookup"><span data-stu-id="72da5-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="72da5-163">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="72da5-163">Select **Edit**.</span></span>
16. <span data-ttu-id="72da5-164">选择箭头以将该菜单项添加到菜单中。</span><span class="sxs-lookup"><span data-stu-id="72da5-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="72da5-165">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="72da5-165">Select **Save**.</span></span>
18. <span data-ttu-id="72da5-166">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="72da5-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="72da5-167">更新工作模板</span><span class="sxs-lookup"><span data-stu-id="72da5-167">Update a work template</span></span>
1. <span data-ttu-id="72da5-168">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 工作 > 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="72da5-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="72da5-169">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="72da5-169">Select **Edit**.</span></span>
3. <span data-ttu-id="72da5-170">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="72da5-170">Select **New**.</span></span>
4. <span data-ttu-id="72da5-171">在**工作类型**字段中，选择**打印**。</span><span class="sxs-lookup"><span data-stu-id="72da5-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="72da5-172">在**工作类 ID** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="72da5-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="72da5-173">选择**上移**。</span><span class="sxs-lookup"><span data-stu-id="72da5-173">Select **Move up**.</span></span>
7. <span data-ttu-id="72da5-174">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="72da5-174">Select **Save**.</span></span>
8. <span data-ttu-id="72da5-175">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="72da5-175">Close the page.</span></span>

