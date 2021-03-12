---
title: Modern POS (MPOS) 和 Cloud POS 中的演示数据屏幕布局
description: 本主题提供了有关 Dynamics 365 Commerce 中销售点 (POS) 体验的演示数据集包含的屏幕布局信息。
author: josaw1
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: e55db57089c8ea5bd3def25d79d9c65a3165526c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982706"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="1a56c-103">Modern POS (MPOS) 和 Cloud POS 中的演示数据屏幕布局</span><span class="sxs-lookup"><span data-stu-id="1a56c-103">Demo data screen layouts in Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a56c-104">本主题提供了有关 Dynamics 365 Commerce 中销售点 (POS) 体验的演示数据集包含的屏幕布局信息。</span><span class="sxs-lookup"><span data-stu-id="1a56c-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1a56c-105">概览</span><span class="sxs-lookup"><span data-stu-id="1a56c-105">Overview</span></span>

<span data-ttu-id="1a56c-106">包括在 Commerce 演示数据中的示例屏幕布局提供为各个零售段、商店工作人员角色和设备优化的内容。</span><span class="sxs-lookup"><span data-stu-id="1a56c-106">The sample screen layouts that are included with Commerce demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="1a56c-107">一个布局可以包含多个布局大小和按钮网格组合，以在商店工作人员在设备和工作站之间移动时帮助确保覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="1a56c-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="1a56c-108">此主题突出介绍了这些布局之间的区别、它们提供的操作和整体体验。</span><span class="sxs-lookup"><span data-stu-id="1a56c-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![跨设备演示数据布局](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="1a56c-110">屏幕布局 ID 的分类</span><span class="sxs-lookup"><span data-stu-id="1a56c-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="1a56c-111">若要查找屏幕布局，请转到 **Retail 和 Commerce** \> **渠道设置** \> **POS 设置** \> **POS** \> **屏幕布局**。</span><span class="sxs-lookup"><span data-stu-id="1a56c-111">To find screen layouts, go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS** \> **Screen layouts**.</span></span>

![屏幕布局页面](../commerce/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="1a56c-113">屏幕布局 ID 最多可以有 10 个字符。</span><span class="sxs-lookup"><span data-stu-id="1a56c-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="1a56c-114">ID 是一个包括三个信息的字符串，按以下顺序：</span><span class="sxs-lookup"><span data-stu-id="1a56c-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="1a56c-115">公司</span><span class="sxs-lookup"><span data-stu-id="1a56c-115">Company</span></span>
2. <span data-ttu-id="1a56c-116">布局版本</span><span class="sxs-lookup"><span data-stu-id="1a56c-116">Layout version</span></span>
3. <span data-ttu-id="1a56c-117">人员</span><span class="sxs-lookup"><span data-stu-id="1a56c-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="1a56c-118">公司</span><span class="sxs-lookup"><span data-stu-id="1a56c-118">Company</span></span>

| <span data-ttu-id="1a56c-119">字母</span><span class="sxs-lookup"><span data-stu-id="1a56c-119">Letter</span></span> | <span data-ttu-id="1a56c-120">公司</span><span class="sxs-lookup"><span data-stu-id="1a56c-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="1a56c-121">A</span><span class="sxs-lookup"><span data-stu-id="1a56c-121">A</span></span>      | <span data-ttu-id="1a56c-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="1a56c-122">Adventure Works</span></span> |
| <span data-ttu-id="1a56c-123">F</span><span class="sxs-lookup"><span data-stu-id="1a56c-123">F</span></span>      | <span data-ttu-id="1a56c-124">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="1a56c-124">Fabrikam</span></span>        |
| <span data-ttu-id="1a56c-125">C</span><span class="sxs-lookup"><span data-stu-id="1a56c-125">C</span></span>      | <span data-ttu-id="1a56c-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="1a56c-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="1a56c-127">布局版本</span><span class="sxs-lookup"><span data-stu-id="1a56c-127">Layout version</span></span>

| <span data-ttu-id="1a56c-128">版本号</span><span class="sxs-lookup"><span data-stu-id="1a56c-128">Version number</span></span> | <span data-ttu-id="1a56c-129">说明</span><span class="sxs-lookup"><span data-stu-id="1a56c-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a56c-130">3</span><span class="sxs-lookup"><span data-stu-id="1a56c-130">3</span></span>              | <span data-ttu-id="1a56c-131">支持各种设备和纵横比的多个屏幕尺寸的基本版本</span><span class="sxs-lookup"><span data-stu-id="1a56c-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="1a56c-132">3.1</span><span class="sxs-lookup"><span data-stu-id="1a56c-132">3.1</span></span>            | <span data-ttu-id="1a56c-133">具有其他 **建议的产品** 面板支持的基础版本</span><span class="sxs-lookup"><span data-stu-id="1a56c-133">The base version that has additional support for the **Recommended products** panel</span></span>        |
| <span data-ttu-id="1a56c-134">4</span><span class="sxs-lookup"><span data-stu-id="1a56c-134">4</span></span>              | <span data-ttu-id="1a56c-135">扩展 Fabrikam 更新布局的扩展版本</span><span class="sxs-lookup"><span data-stu-id="1a56c-135">The extended version for extended Fabrikam updated layout</span></span>                                  |

### <a name="persona"></a><span data-ttu-id="1a56c-136">人员</span><span class="sxs-lookup"><span data-stu-id="1a56c-136">Persona</span></span>

| <span data-ttu-id="1a56c-137">缩写</span><span class="sxs-lookup"><span data-stu-id="1a56c-137">Abbreviation</span></span> | <span data-ttu-id="1a56c-138">人员</span><span class="sxs-lookup"><span data-stu-id="1a56c-138">Persona</span></span>       | <span data-ttu-id="1a56c-139">内容</span><span class="sxs-lookup"><span data-stu-id="1a56c-139">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="1a56c-140">CSH</span><span class="sxs-lookup"><span data-stu-id="1a56c-140">CSH</span></span>          | <span data-ttu-id="1a56c-141">出纳</span><span class="sxs-lookup"><span data-stu-id="1a56c-141">Cashier</span></span>       | <span data-ttu-id="1a56c-142">出纳布局包括所有与交易相关的操作，如客户订单、退货、折扣、失效和礼品卡。</span><span class="sxs-lookup"><span data-stu-id="1a56c-142">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="1a56c-143">这些布局还包括库存管理的日常任务，如价格检查、库存查找和存货盘点。</span><span class="sxs-lookup"><span data-stu-id="1a56c-143">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="1a56c-144">基本的班次管理还为初始金额、暂停班次和打卡时间提供。</span><span class="sxs-lookup"><span data-stu-id="1a56c-144">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="1a56c-145">MGR</span><span class="sxs-lookup"><span data-stu-id="1a56c-145">MGR</span></span>          | <span data-ttu-id="1a56c-146">商店经理</span><span class="sxs-lookup"><span data-stu-id="1a56c-146">Store Manager</span></span> | <span data-ttu-id="1a56c-147">商店经理布局包括在出纳布局中找到的所有交易相关操作，而且包括税覆盖。</span><span class="sxs-lookup"><span data-stu-id="1a56c-147">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="1a56c-148">这些布局还包括库存管理的日常任务，如价格检查、库存查找和存货盘点。</span><span class="sxs-lookup"><span data-stu-id="1a56c-148">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="1a56c-149">班次管理为开始、暂停和结束班次提供。</span><span class="sxs-lookup"><span data-stu-id="1a56c-149">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="1a56c-150">此外，这些布局还包括输入、删除、钱币清点以及金库投箱和银行投箱的开票人操作。</span><span class="sxs-lookup"><span data-stu-id="1a56c-150">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="1a56c-151">最后，这些布局包括对绩效报表的访问，以及启用要打印的 X 和 Z 报表。</span><span class="sxs-lookup"><span data-stu-id="1a56c-151">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="1a56c-152">STK</span><span class="sxs-lookup"><span data-stu-id="1a56c-152">STK</span></span>          | <span data-ttu-id="1a56c-153">保管员</span><span class="sxs-lookup"><span data-stu-id="1a56c-153">Stock Clerk</span></span>   | <span data-ttu-id="1a56c-154">保管员布局针对库存管理进行了优化。</span><span class="sxs-lookup"><span data-stu-id="1a56c-154">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="1a56c-155">它们包括对价格检查、库存查找、领料和收货、库存盘点和配套件拆卸的日常任务的访问。</span><span class="sxs-lookup"><span data-stu-id="1a56c-155">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="1a56c-156">这些布局还为时钟和暂停班次提供基本班次操作。</span><span class="sxs-lookup"><span data-stu-id="1a56c-156">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="1a56c-157">尽管这些布局主要用于后勤办公室任务，保管员与出纳的交易记录屏幕具有相同的操作。</span><span class="sxs-lookup"><span data-stu-id="1a56c-157">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="1a56c-158">示例布局</span><span class="sxs-lookup"><span data-stu-id="1a56c-158">Example layout</span></span>

<span data-ttu-id="1a56c-159">这是 Fabrikam 公司、布局版本 4 和人员为商店经理的屏幕布局 ID 的示例：</span><span class="sxs-lookup"><span data-stu-id="1a56c-159">Here is an example of a screen layout ID for the Fabrikam company, layout version 4, and the Store Manager persona:</span></span>

<span data-ttu-id="1a56c-160">F4MGR</span><span class="sxs-lookup"><span data-stu-id="1a56c-160">F4MGR</span></span>

<span data-ttu-id="1a56c-161">下图显示 Fabrikam 商店经理的欢迎屏幕的示例。</span><span class="sxs-lookup"><span data-stu-id="1a56c-161">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![Fabrikam 商店经理的欢迎屏幕](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="1a56c-163">布局大小</span><span class="sxs-lookup"><span data-stu-id="1a56c-163">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="1a56c-164">完整型布局与紧凑型布局</span><span class="sxs-lookup"><span data-stu-id="1a56c-164">Full vs. compact layouts</span></span>

<span data-ttu-id="1a56c-165">屏幕布局同时具有完整设备和紧凑设备的配置。</span><span class="sxs-lookup"><span data-stu-id="1a56c-165">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="1a56c-166">因此，用户可以被分配一个屏幕布局，而该屏幕布局支持商店内的多种尺寸和外形。</span><span class="sxs-lookup"><span data-stu-id="1a56c-166">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="1a56c-167">**现代 POS - 完整型** – 通常，完整型布局最适合较大显示器，如台式机显示器或平板电脑。</span><span class="sxs-lookup"><span data-stu-id="1a56c-167">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="1a56c-168">用户可以选择布局包含的元素 UI，指定这些元素的尺寸和位置，并配置它们的详细属性。</span><span class="sxs-lookup"><span data-stu-id="1a56c-168">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="1a56c-169">完整型布局同时支持垂直配置和水平配置。</span><span class="sxs-lookup"><span data-stu-id="1a56c-169">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="1a56c-170">**现代 POS - 紧凑型** - 通常，紧凑型布局最适合手机或小平板电脑。</span><span class="sxs-lookup"><span data-stu-id="1a56c-170">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="1a56c-171">对于紧凑型设备，设计功能受到限制。</span><span class="sxs-lookup"><span data-stu-id="1a56c-171">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="1a56c-172">用户可以为收据窗格和总计窗格配置列和字段。</span><span class="sxs-lookup"><span data-stu-id="1a56c-172">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="1a56c-173">提供的屏幕分辨率</span><span class="sxs-lookup"><span data-stu-id="1a56c-173">Screen resolutions that are provided</span></span>

<span data-ttu-id="1a56c-174">下表显示为典型的屏幕分辨率提供的布局大小。</span><span class="sxs-lookup"><span data-stu-id="1a56c-174">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="1a56c-175">布局类型</span><span class="sxs-lookup"><span data-stu-id="1a56c-175">Layout type</span></span> | <span data-ttu-id="1a56c-176">分辨率</span><span class="sxs-lookup"><span data-stu-id="1a56c-176">Resolution</span></span> | <span data-ttu-id="1a56c-177">纵横比</span><span class="sxs-lookup"><span data-stu-id="1a56c-177">Aspect ratio</span></span> | <span data-ttu-id="1a56c-178">目标显示</span><span class="sxs-lookup"><span data-stu-id="1a56c-178">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="1a56c-179">压缩\*</span><span class="sxs-lookup"><span data-stu-id="1a56c-179">Compact\*</span></span>   | <span data-ttu-id="1a56c-180">480 × 853</span><span class="sxs-lookup"><span data-stu-id="1a56c-180">480 × 853</span></span>  | <span data-ttu-id="1a56c-181">16:9</span><span class="sxs-lookup"><span data-stu-id="1a56c-181">16:9</span></span>         | <span data-ttu-id="1a56c-182">电话</span><span class="sxs-lookup"><span data-stu-id="1a56c-182">Phones</span></span>                  |
| <span data-ttu-id="1a56c-183">完全</span><span class="sxs-lookup"><span data-stu-id="1a56c-183">Full</span></span>        | <span data-ttu-id="1a56c-184">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="1a56c-184">1024 × 768</span></span> | <span data-ttu-id="1a56c-185">4:3</span><span class="sxs-lookup"><span data-stu-id="1a56c-185">4:3</span></span>          | <span data-ttu-id="1a56c-186">平板电脑</span><span class="sxs-lookup"><span data-stu-id="1a56c-186">Tablets</span></span>                 |
| <span data-ttu-id="1a56c-187">完全\*</span><span class="sxs-lookup"><span data-stu-id="1a56c-187">Full\*</span></span>      | <span data-ttu-id="1a56c-188">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="1a56c-188">1280 × 720</span></span> | <span data-ttu-id="1a56c-189">16:9</span><span class="sxs-lookup"><span data-stu-id="1a56c-189">16:9</span></span>         | <span data-ttu-id="1a56c-190">平板电脑</span><span class="sxs-lookup"><span data-stu-id="1a56c-190">Tablets</span></span>                 |
| <span data-ttu-id="1a56c-191">完全</span><span class="sxs-lookup"><span data-stu-id="1a56c-191">Full</span></span>        | <span data-ttu-id="1a56c-192">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="1a56c-192">1366 × 768</span></span> | <span data-ttu-id="1a56c-193">16:9</span><span class="sxs-lookup"><span data-stu-id="1a56c-193">16:9</span></span>         | <span data-ttu-id="1a56c-194">平板电脑，较大屏幕</span><span class="sxs-lookup"><span data-stu-id="1a56c-194">Tablets, larger screens</span></span> |
| <span data-ttu-id="1a56c-195">全尺寸</span><span class="sxs-lookup"><span data-stu-id="1a56c-195">Full</span></span>        | <span data-ttu-id="1a56c-196">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="1a56c-196">1440 × 960</span></span> | <span data-ttu-id="1a56c-197">3:2</span><span class="sxs-lookup"><span data-stu-id="1a56c-197">3:2</span></span>          | <span data-ttu-id="1a56c-198">平板电脑，较大屏幕</span><span class="sxs-lookup"><span data-stu-id="1a56c-198">Tablets, larger screens</span></span> |
| <span data-ttu-id="1a56c-199">全尺寸\*</span><span class="sxs-lookup"><span data-stu-id="1a56c-199">Full\*</span></span>      | <span data-ttu-id="1a56c-200">1536 × 864</span><span class="sxs-lookup"><span data-stu-id="1a56c-200">1536 × 864</span></span> | <span data-ttu-id="1a56c-201">16:9</span><span class="sxs-lookup"><span data-stu-id="1a56c-201">16:9</span></span>         | <span data-ttu-id="1a56c-202">平板电脑，较大屏幕</span><span class="sxs-lookup"><span data-stu-id="1a56c-202">Tablets, larger screens</span></span> |

<span data-ttu-id="1a56c-203">\*这些额外的布局大小仅在 Adventure Works 和 Fabrikam 布局中提供。</span><span class="sxs-lookup"><span data-stu-id="1a56c-203">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>

> [!TIP]
> <span data-ttu-id="1a56c-204">POS 基于与可用于当前应用窗口的屏幕分辨率最接近的大小自动选择布局大小。</span><span class="sxs-lookup"><span data-stu-id="1a56c-204">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="1a56c-205">若要查找当前使用的屏幕布局 ID 和布局分辨率，在 Modern POS (MPOS) 或 Retail Cloud POS (CPOS) 中，打开 **设置** 页，然后在 **会话信息** 部分查找。</span><span class="sxs-lookup"><span data-stu-id="1a56c-205">To find the screen layout ID and layout resolution that are currently used, in Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="1a56c-206">您还可以看到当前应用程序或浏览器框架的实际窗口分辨率。</span><span class="sxs-lookup"><span data-stu-id="1a56c-206">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="1a56c-207">在具有此信息后，可以查找布局内容的源，方法是转到 **渠道设置** \> **POS 设置** \> **POS** \> **屏幕布局**。</span><span class="sxs-lookup"><span data-stu-id="1a56c-207">After you have this information, you can find the source of the layout content by going to **Channel setup** \> **POS setup** \> **POS** \> **Screen layouts**.</span></span>

![Commerce 和 POS 中的屏幕布局和布局分辨率/大小](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="1a56c-209">公司和品牌</span><span class="sxs-lookup"><span data-stu-id="1a56c-209">Companies and brands</span></span>

<span data-ttu-id="1a56c-210">每个虚构的公司面向不同的零售段，包含为公司的市场调整的产品目录。</span><span class="sxs-lookup"><span data-stu-id="1a56c-210">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="1a56c-211">每家公司都具有伴随其产品的独一无二的视觉品牌。</span><span class="sxs-lookup"><span data-stu-id="1a56c-211">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="1a56c-212">品牌元素包括个性色、深色主题或浅色主题，以及提供逼真体验的附带照片。</span><span class="sxs-lookup"><span data-stu-id="1a56c-212">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="1a56c-213">公司细分市场和视觉特征</span><span class="sxs-lookup"><span data-stu-id="1a56c-213">Company segment and visual characteristics</span></span>

| <span data-ttu-id="1a56c-214">公司</span><span class="sxs-lookup"><span data-stu-id="1a56c-214">Company</span></span>         | <span data-ttu-id="1a56c-215">库位</span><span class="sxs-lookup"><span data-stu-id="1a56c-215">Location</span></span> | <span data-ttu-id="1a56c-216">分段</span><span class="sxs-lookup"><span data-stu-id="1a56c-216">Segment</span></span>        | <span data-ttu-id="1a56c-217">个性</span><span class="sxs-lookup"><span data-stu-id="1a56c-217">Accent</span></span> | <span data-ttu-id="1a56c-218">主题</span><span class="sxs-lookup"><span data-stu-id="1a56c-218">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="1a56c-219">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="1a56c-219">Adventure Works</span></span> | <span data-ttu-id="1a56c-220">西雅图</span><span class="sxs-lookup"><span data-stu-id="1a56c-220">Seattle</span></span>  | <span data-ttu-id="1a56c-221">体育用品</span><span class="sxs-lookup"><span data-stu-id="1a56c-221">Sporting Goods</span></span> | <span data-ttu-id="1a56c-222">蓝色</span><span class="sxs-lookup"><span data-stu-id="1a56c-222">Blue</span></span>   | <span data-ttu-id="1a56c-223">深色</span><span class="sxs-lookup"><span data-stu-id="1a56c-223">Dark</span></span>  |
| <span data-ttu-id="1a56c-224">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="1a56c-224">Fabrikam</span></span>        | <span data-ttu-id="1a56c-225">旧金山</span><span class="sxs-lookup"><span data-stu-id="1a56c-225">San Francisco</span></span>  | <span data-ttu-id="1a56c-226">风格</span><span class="sxs-lookup"><span data-stu-id="1a56c-226">Fashion</span></span>        | <span data-ttu-id="1a56c-227">绿色</span><span class="sxs-lookup"><span data-stu-id="1a56c-227">Green</span></span>  | <span data-ttu-id="1a56c-228">浅色</span><span class="sxs-lookup"><span data-stu-id="1a56c-228">Light</span></span> |
| <span data-ttu-id="1a56c-229">Contoso</span><span class="sxs-lookup"><span data-stu-id="1a56c-229">Contoso</span></span>         | <span data-ttu-id="1a56c-230">波士顿</span><span class="sxs-lookup"><span data-stu-id="1a56c-230">Boston</span></span>   | <span data-ttu-id="1a56c-231">电子</span><span class="sxs-lookup"><span data-stu-id="1a56c-231">Electronics</span></span>    | <span data-ttu-id="1a56c-232">红色</span><span class="sxs-lookup"><span data-stu-id="1a56c-232">Red</span></span>    | <span data-ttu-id="1a56c-233">深色</span><span class="sxs-lookup"><span data-stu-id="1a56c-233">Dark</span></span>  |

> [!NOTE]
> <span data-ttu-id="1a56c-234">Adventure Works 和 Fabrikam 为两个旗舰品牌。</span><span class="sxs-lookup"><span data-stu-id="1a56c-234">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="1a56c-235">Contoso 可用，但并不提供所有布局。</span><span class="sxs-lookup"><span data-stu-id="1a56c-235">Contoso is available, but not all layouts have been provided.</span></span>

<span data-ttu-id="1a56c-236">下图显示了三个虚构公司的欢迎页面和交易页面示例。</span><span class="sxs-lookup"><span data-stu-id="1a56c-236">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="1a56c-237">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="1a56c-237">Adventure Works</span></span>

![演示数据：Adventure Works 的欢迎页面](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![演示数据：Adventure Works 的交易页面](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="1a56c-240">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="1a56c-240">Fabrikam</span></span>

![演示数据：Fabrikam 的欢迎页面](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![演示数据：Fabrikam 的交易页面](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="1a56c-243">Contoso</span><span class="sxs-lookup"><span data-stu-id="1a56c-243">Contoso</span></span>

![演示数据：Contoso 的布局](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="1a56c-245">用户登录矩阵</span><span class="sxs-lookup"><span data-stu-id="1a56c-245">User sign in matrix</span></span>

<span data-ttu-id="1a56c-246">已为各个屏幕布局提供了用户。</span><span class="sxs-lookup"><span data-stu-id="1a56c-246">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="1a56c-247">通过使用下表，您应该能够访问任何屏幕。</span><span class="sxs-lookup"><span data-stu-id="1a56c-247">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="1a56c-248">使用相应的操作员 ID 登录。</span><span class="sxs-lookup"><span data-stu-id="1a56c-248">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="1a56c-249">公司</span><span class="sxs-lookup"><span data-stu-id="1a56c-249">Company</span></span>         | <span data-ttu-id="1a56c-250">屏幕布局 ID</span><span class="sxs-lookup"><span data-stu-id="1a56c-250">Screen layout ID</span></span> | <span data-ttu-id="1a56c-251">人员</span><span class="sxs-lookup"><span data-stu-id="1a56c-251">Persona</span></span>       | <span data-ttu-id="1a56c-252">操作员 ID</span><span class="sxs-lookup"><span data-stu-id="1a56c-252">Operator IDs</span></span>           |
|-----------------|------------------|---------------|------------------------|
| <span data-ttu-id="1a56c-253">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="1a56c-253">Adventure Works</span></span> | <span data-ttu-id="1a56c-254">A3MGR</span><span class="sxs-lookup"><span data-stu-id="1a56c-254">A3MGR</span></span>            | <span data-ttu-id="1a56c-255">商店经理</span><span class="sxs-lookup"><span data-stu-id="1a56c-255">Store Manager</span></span> | <span data-ttu-id="1a56c-256">000154、000137、000073</span><span class="sxs-lookup"><span data-stu-id="1a56c-256">000154, 000137, 000073</span></span> |
| <span data-ttu-id="1a56c-257">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="1a56c-257">Adventure Works</span></span> | <span data-ttu-id="1a56c-258">A3CSH</span><span class="sxs-lookup"><span data-stu-id="1a56c-258">A3CSH</span></span>            | <span data-ttu-id="1a56c-259">出纳</span><span class="sxs-lookup"><span data-stu-id="1a56c-259">Cashier</span></span>       | <span data-ttu-id="1a56c-260">000150、000175、000165</span><span class="sxs-lookup"><span data-stu-id="1a56c-260">000150, 000175, 000165</span></span> |
| <span data-ttu-id="1a56c-261">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="1a56c-261">Adventure Works</span></span> | <span data-ttu-id="1a56c-262">A3STK</span><span class="sxs-lookup"><span data-stu-id="1a56c-262">A3STK</span></span>            | <span data-ttu-id="1a56c-263">保管员</span><span class="sxs-lookup"><span data-stu-id="1a56c-263">Stock Clerk</span></span>   | <span data-ttu-id="1a56c-264">000155、000181、000152</span><span class="sxs-lookup"><span data-stu-id="1a56c-264">000155, 000181, 000152</span></span> |
| <span data-ttu-id="1a56c-265">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="1a56c-265">Fabrikam</span></span>        | <span data-ttu-id="1a56c-266">F4MGR</span><span class="sxs-lookup"><span data-stu-id="1a56c-266">F4MGR</span></span>            | <span data-ttu-id="1a56c-267">商店经理</span><span class="sxs-lookup"><span data-stu-id="1a56c-267">Store Manager</span></span> | <span data-ttu-id="1a56c-268">000160、000713</span><span class="sxs-lookup"><span data-stu-id="1a56c-268">000160, 000713</span></span>         |
| <span data-ttu-id="1a56c-269">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="1a56c-269">Fabrikam</span></span>        | <span data-ttu-id="1a56c-270">F3CSH</span><span class="sxs-lookup"><span data-stu-id="1a56c-270">F3CSH</span></span>            | <span data-ttu-id="1a56c-271">出纳</span><span class="sxs-lookup"><span data-stu-id="1a56c-271">Cashier</span></span>       | <span data-ttu-id="1a56c-272">000161、000113、000114</span><span class="sxs-lookup"><span data-stu-id="1a56c-272">000161, 000113, 000114</span></span> |
| <span data-ttu-id="1a56c-273">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="1a56c-273">Fabrikam</span></span>        | <span data-ttu-id="1a56c-274">F3STK</span><span class="sxs-lookup"><span data-stu-id="1a56c-274">F3STK</span></span>            | <span data-ttu-id="1a56c-275">保管员</span><span class="sxs-lookup"><span data-stu-id="1a56c-275">Stock Clerk</span></span>   | <span data-ttu-id="1a56c-276">000164、000112、000123</span><span class="sxs-lookup"><span data-stu-id="1a56c-276">000164, 000112, 000123</span></span> |
| <span data-ttu-id="1a56c-277">Contoso</span><span class="sxs-lookup"><span data-stu-id="1a56c-277">Contoso</span></span>         | <span data-ttu-id="1a56c-278">C3MGR</span><span class="sxs-lookup"><span data-stu-id="1a56c-278">C3MGR</span></span>            | <span data-ttu-id="1a56c-279">商店经理</span><span class="sxs-lookup"><span data-stu-id="1a56c-279">Store Manager</span></span> | <span data-ttu-id="1a56c-280">000100、000111</span><span class="sxs-lookup"><span data-stu-id="1a56c-280">000100, 000111</span></span>         |
| <span data-ttu-id="1a56c-281">Contoso</span><span class="sxs-lookup"><span data-stu-id="1a56c-281">Contoso</span></span>         | <span data-ttu-id="1a56c-282">C3CSH</span><span class="sxs-lookup"><span data-stu-id="1a56c-282">C3CSH</span></span>            | <span data-ttu-id="1a56c-283">出纳</span><span class="sxs-lookup"><span data-stu-id="1a56c-283">Cashier</span></span>       | <span data-ttu-id="1a56c-284">000110、000120</span><span class="sxs-lookup"><span data-stu-id="1a56c-284">000110, 000120</span></span>         |
| <span data-ttu-id="1a56c-285">Contoso</span><span class="sxs-lookup"><span data-stu-id="1a56c-285">Contoso</span></span>         | <span data-ttu-id="1a56c-286">不适用</span><span class="sxs-lookup"><span data-stu-id="1a56c-286">Not applicable</span></span>   | <span data-ttu-id="1a56c-287">保管员</span><span class="sxs-lookup"><span data-stu-id="1a56c-287">Stock Clerk</span></span>   | <span data-ttu-id="1a56c-288">不适用</span><span class="sxs-lookup"><span data-stu-id="1a56c-288">Not applicable</span></span>         |

> [!TIP]
> <span data-ttu-id="1a56c-289">为了达到最佳效果，请在相应的商店位置激活收银机，然后将公司设置为您计划在登录时使用的人员的公司。</span><span class="sxs-lookup"><span data-stu-id="1a56c-289">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="1a56c-290">这样，您可以帮助确保视觉形象和品牌图像与整个体验一致。</span><span class="sxs-lookup"><span data-stu-id="1a56c-290">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="1a56c-291">例如，如果您有兴趣查看出纳的 Fabrikam 布局，则应该在休斯敦商店激活收银机。</span><span class="sxs-lookup"><span data-stu-id="1a56c-291">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->
