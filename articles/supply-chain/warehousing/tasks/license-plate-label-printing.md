---
title: 启用牌照标签打印
description: 此主题显示如何在销售领料工作流程中从库存对最后一个物料拣货之后，对串行装运集装箱码 (SSCC) 标签启用自动打印。
author: perlynne
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 545f1c15888bcd0b46e1028f58cbe3a274846c92
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146019"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="dcb64-103">启用牌照标签打印</span><span class="sxs-lookup"><span data-stu-id="dcb64-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcb64-104">此主题显示如何在销售领料工作流程中从库存对最后一个物料拣货之后，对串行装运集装箱码 (SSCC) 标签启用自动打印。</span><span class="sxs-lookup"><span data-stu-id="dcb64-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="dcb64-105">您可以使用演示数据公司 USMF 运行此程序。</span><span class="sxs-lookup"><span data-stu-id="dcb64-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="dcb64-106">如果您使用自己的数据运行，则须为牌照设置一个数序。</span><span class="sxs-lookup"><span data-stu-id="dcb64-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="dcb64-107">在您开始此任务前，需要装配一台标签打印机。</span><span class="sxs-lookup"><span data-stu-id="dcb64-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="dcb64-108">转到“组织管理”>“设置”>“网络打印机”。</span><span class="sxs-lookup"><span data-stu-id="dcb64-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="dcb64-109">在“操作窗格”中，单击“选项”，然后单击“下载文档路由代理安装程序”按钮。</span><span class="sxs-lookup"><span data-stu-id="dcb64-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="dcb64-110">运行此安装程序并确认工作网络打印机设置为“主动”，方可继续该程序。</span><span class="sxs-lookup"><span data-stu-id="dcb64-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="dcb64-111">设置 GS1 公司字头。</span><span class="sxs-lookup"><span data-stu-id="dcb64-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="dcb64-112">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="dcb64-113">在 **GS1 公司前缀**字段中，输入一个 7 位数字的个人 GS1 公司编号。</span><span class="sxs-lookup"><span data-stu-id="dcb64-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="dcb64-114">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-114">Select **Save**.</span></span>
4. <span data-ttu-id="dcb64-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dcb64-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="dcb64-116">设置 SSCC 牌照数序</span><span class="sxs-lookup"><span data-stu-id="dcb64-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="dcb64-117">转到**导航窗格 > 模块 > 组织管理 > 标号规则 > 编号规则**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="dcb64-118">在**区域**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="dcb64-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="dcb64-119">在**参考**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="dcb64-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="dcb64-120">在**公司**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="dcb64-121">展开**分段**部分。</span><span class="sxs-lookup"><span data-stu-id="dcb64-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="dcb64-122">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-122">Select **Edit**.</span></span>
7. <span data-ttu-id="dcb64-123">在**区段**表中，选择第一行</span><span class="sxs-lookup"><span data-stu-id="dcb64-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="dcb64-124">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-124">Select **Remove**.</span></span>
9. <span data-ttu-id="dcb64-125">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-125">Select **Remove**.</span></span>
10. <span data-ttu-id="dcb64-126">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-126">Select **Save**.</span></span>
11. <span data-ttu-id="dcb64-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dcb64-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="dcb64-128">创建文档路径布局</span><span class="sxs-lookup"><span data-stu-id="dcb64-128">Create the document route layout</span></span>
1. <span data-ttu-id="dcb64-129">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 文档路线选择 > 文档路线选择布局**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="dcb64-130">启用 SSCC 布局。</span><span class="sxs-lookup"><span data-stu-id="dcb64-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="dcb64-131">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-131">Select **New**.</span></span>
3. <span data-ttu-id="dcb64-132">在**布局 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="dcb64-133">在**描述**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="dcb64-134">选择**在文本结尾处插入**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="dcb64-135">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-135">Select **Save**.</span></span>
7. <span data-ttu-id="dcb64-136">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dcb64-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="dcb64-137">设置文档路径</span><span class="sxs-lookup"><span data-stu-id="dcb64-137">Set up the document routing</span></span>
1. <span data-ttu-id="dcb64-138">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 文档路线选择 > 文档路线选择**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="dcb64-139">在**工作订单类型**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="dcb64-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="dcb64-140">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-140">Select **New**.</span></span>
4. <span data-ttu-id="dcb64-141">在**仓库**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="dcb64-142">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="dcb64-143">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-143">Select **New**.</span></span>
7. <span data-ttu-id="dcb64-144">在**布局 ID** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="dcb64-145">在**名称**字段中，输入您要使用的打印机名称。</span><span class="sxs-lookup"><span data-stu-id="dcb64-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="dcb64-146">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-146">Select **Save**.</span></span>
10. <span data-ttu-id="dcb64-147">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dcb64-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="dcb64-148">创建移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="dcb64-148">Create mobile device menu</span></span>
1. <span data-ttu-id="dcb64-149">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 移动设备 > 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="dcb64-150">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-150">Select **New**.</span></span>
3. <span data-ttu-id="dcb64-151">在**菜单项名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="dcb64-152">在**标题**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="dcb64-153">在**模式**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="dcb64-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="dcb64-154">在**使用现有工作**字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="dcb64-155">在**生成牌照**字段中选择**是**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="dcb64-156">展开**工作类**部分。</span><span class="sxs-lookup"><span data-stu-id="dcb64-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="dcb64-157">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-157">Select **New**.</span></span>
10. <span data-ttu-id="dcb64-158">在**工作类 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="dcb64-159">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-159">Select **Save**.</span></span>
12. <span data-ttu-id="dcb64-160">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dcb64-160">Close the page.</span></span>
13. <span data-ttu-id="dcb64-161">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 移动设备 > 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="dcb64-162">在树形图中，选择您之前已创建的菜单项。</span><span class="sxs-lookup"><span data-stu-id="dcb64-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="dcb64-163">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-163">Select **Edit**.</span></span>
16. <span data-ttu-id="dcb64-164">选择箭头以将该菜单项添加到菜单中。</span><span class="sxs-lookup"><span data-stu-id="dcb64-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="dcb64-165">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-165">Select **Save**.</span></span>
18. <span data-ttu-id="dcb64-166">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dcb64-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="dcb64-167">更新工作模板</span><span class="sxs-lookup"><span data-stu-id="dcb64-167">Update a work template</span></span>
1. <span data-ttu-id="dcb64-168">转到**导航窗格 > 模块 > 仓库管理 > 设置 > 工作 > 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="dcb64-169">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-169">Select **Edit**.</span></span>
3. <span data-ttu-id="dcb64-170">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-170">Select **New**.</span></span>
4. <span data-ttu-id="dcb64-171">在**工作类型**字段中，选择**打印**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="dcb64-172">在**工作类 ID** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dcb64-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="dcb64-173">选择**上移**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-173">Select **Move up**.</span></span>
7. <span data-ttu-id="dcb64-174">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="dcb64-174">Select **Save**.</span></span>
8. <span data-ttu-id="dcb64-175">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="dcb64-175">Close the page.</span></span>

