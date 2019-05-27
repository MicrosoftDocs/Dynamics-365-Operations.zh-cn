---
title: 启用牌照标签打印
description: 销售领料工作流程的最后一项工作是库存拣货，此程序适用于在此之后的串行装运集装箱码 (SSCC) 标签的自动打印。
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d906ca9f5a6536870fa0c322a0792ed5672c25e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558095"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="8b99c-103">启用牌照标签打印</span><span class="sxs-lookup"><span data-stu-id="8b99c-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b99c-104">销售领料工作流程的最后一项工作是库存拣货，此程序适用于在此之后的串行装运集装箱码 (SSCC) 标签的自动打印。</span><span class="sxs-lookup"><span data-stu-id="8b99c-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="8b99c-105">您可以使用演示数据公司 USMF 运行此程序。</span><span class="sxs-lookup"><span data-stu-id="8b99c-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="8b99c-106">如果您使用自己的数据运行，则须为牌照设置一个数序。</span><span class="sxs-lookup"><span data-stu-id="8b99c-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="8b99c-107">在您开始此任务前，需要装配一台标签打印机。</span><span class="sxs-lookup"><span data-stu-id="8b99c-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="8b99c-108">转到“组织管理”>“设置”>“网络打印机”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="8b99c-109">在“操作窗格”中，单击“选项”，然后单击“下载文档路由代理安装程序”按钮。</span><span class="sxs-lookup"><span data-stu-id="8b99c-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="8b99c-110">运行此安装程序并确认工作网络打印机设置为“主动”，方可继续该程序。</span><span class="sxs-lookup"><span data-stu-id="8b99c-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="8b99c-111">设置 GS1 公司字头。</span><span class="sxs-lookup"><span data-stu-id="8b99c-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="8b99c-112">转到“仓库管理”>“设置”>“仓库管理参数”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="8b99c-113">在 GS1 公司的字头字段中，输入一个 7 位数字的个人 GS1 公司编号。</span><span class="sxs-lookup"><span data-stu-id="8b99c-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="8b99c-114">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-114">Click Save.</span></span>
4. <span data-ttu-id="8b99c-115">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b99c-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="8b99c-116">设置 SSCC 牌照数序</span><span class="sxs-lookup"><span data-stu-id="8b99c-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="8b99c-117">转到“组织管理”>“标号规则”>“编号规则”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="8b99c-118">在“区域”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="8b99c-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="8b99c-119">在“参考”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="8b99c-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="8b99c-120">在“公司”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="8b99c-121">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8b99c-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8b99c-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8b99c-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8b99c-123">展开“分段”部分。</span><span class="sxs-lookup"><span data-stu-id="8b99c-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="8b99c-124">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-124">Click Edit.</span></span>
9. <span data-ttu-id="8b99c-125">在“区段”表中，选择第一行</span><span class="sxs-lookup"><span data-stu-id="8b99c-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="8b99c-126">单击“移除”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-126">Click Remove.</span></span>
11. <span data-ttu-id="8b99c-127">单击“移除”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-127">Click Remove.</span></span>
12. <span data-ttu-id="8b99c-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-128">Click Save.</span></span>
13. <span data-ttu-id="8b99c-129">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b99c-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="8b99c-130">创建文档路径布局</span><span class="sxs-lookup"><span data-stu-id="8b99c-130">Create the document route layout</span></span>
1. <span data-ttu-id="8b99c-131">转到“仓库管理”>“设置”>“设置”>“文档路径布局”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="8b99c-132">启用 SSCC 布局。</span><span class="sxs-lookup"><span data-stu-id="8b99c-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="8b99c-133">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-133">Click New.</span></span>
3. <span data-ttu-id="8b99c-134">在“布局 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="8b99c-135">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8b99c-136">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="8b99c-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="8b99c-137">单击文本结尾处的“插入”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="8b99c-138">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-138">Click Save.</span></span>
8. <span data-ttu-id="8b99c-139">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b99c-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="8b99c-140">设置文档路径</span><span class="sxs-lookup"><span data-stu-id="8b99c-140">Set up the document routing</span></span>
1. <span data-ttu-id="8b99c-141">转到“仓库管理”>“设置”>“文档路径”>“文档路径”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="8b99c-142">在“工作订单类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="8b99c-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="8b99c-143">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-143">Click New.</span></span>
4. <span data-ttu-id="8b99c-144">在“仓库”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="8b99c-145">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="8b99c-146">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-146">Click New.</span></span>
7. <span data-ttu-id="8b99c-147">在“布局 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="8b99c-148">在“名称”字段中，输入您要使用的打印机名称。</span><span class="sxs-lookup"><span data-stu-id="8b99c-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="8b99c-149">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-149">Click Save.</span></span>
10. <span data-ttu-id="8b99c-150">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b99c-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="8b99c-151">创建移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="8b99c-151">Create mobile device menu</span></span>
1. <span data-ttu-id="8b99c-152">转到“仓库管理”>“设置”>“移动设备”>“移动设备菜单项”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="8b99c-153">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-153">Click New.</span></span>
3. <span data-ttu-id="8b99c-154">在“菜单项名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="8b99c-155">在“标题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="8b99c-156">在“模式”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="8b99c-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="8b99c-157">在“使用现有工作”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="8b99c-158">在“生成牌照”字段中选择”是“。</span><span class="sxs-lookup"><span data-stu-id="8b99c-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="8b99c-159">展开“工作类”部分。</span><span class="sxs-lookup"><span data-stu-id="8b99c-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="8b99c-160">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-160">Click New.</span></span>
10. <span data-ttu-id="8b99c-161">在“工作类 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="8b99c-162">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-162">Click Save.</span></span>
12. <span data-ttu-id="8b99c-163">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b99c-163">Close the page.</span></span>
13. <span data-ttu-id="8b99c-164">转到“仓库管理”>“设置”>“设置”>“移动设备菜单”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="8b99c-165">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="8b99c-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="8b99c-166">在此树上，选择“在树上，选择之前创建的菜单项”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="8b99c-167">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-167">Click Edit.</span></span>
17. <span data-ttu-id="8b99c-168">单击箭头在此菜单中添加菜单项。</span><span class="sxs-lookup"><span data-stu-id="8b99c-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="8b99c-169">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-169">Click Save.</span></span>
19. <span data-ttu-id="8b99c-170">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b99c-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="8b99c-171">更新工作模板</span><span class="sxs-lookup"><span data-stu-id="8b99c-171">Update a work template</span></span>
1. <span data-ttu-id="8b99c-172">转到“仓库管理”>“设置”>“工作”>“工作模板”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="8b99c-173">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="8b99c-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8b99c-174">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-174">Click Edit.</span></span>
4. <span data-ttu-id="8b99c-175">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-175">Click New.</span></span>
5. <span data-ttu-id="8b99c-176">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="8b99c-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8b99c-177">在“工作类型”字段中，选择“打印”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="8b99c-178">在“工作类 ID”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="8b99c-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="8b99c-179">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="8b99c-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8b99c-180">单击“上移”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-180">Click Move up.</span></span>
10. <span data-ttu-id="8b99c-181">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="8b99c-181">Click Save.</span></span>
11. <span data-ttu-id="8b99c-182">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="8b99c-182">Close the page.</span></span>

