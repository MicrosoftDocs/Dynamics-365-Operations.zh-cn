---
title: "MPOS/CPOS 中的演示数据屏幕布局"
description: "本主题提供了有关 Microsoft Dynamics 365 for Retail 中销售点 (POS) 体验的演示数据集包含的屏幕布局信息。"
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.search.scope: Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 563c89c75e2136294f8f841bec094c2aeb85d580
ms.openlocfilehash: b758b48230e8d9fabdccbe267a6ad6b9e74af0ff
ms.contentlocale: zh-cn
ms.lasthandoff: 10/17/2017

---

# <a name="demo-data-screen-layouts-in-mposcpos"></a><span data-ttu-id="3690f-103">MPOS/CPOS 中的演示数据屏幕布局</span><span class="sxs-lookup"><span data-stu-id="3690f-103">Demo data screen layouts in MPOS/CPOS</span></span>

<span data-ttu-id="3690f-104">本主题提供了有关 Microsoft Dynamics 365 for Retail 中销售点 (POS) 体验的演示数据集包含的屏幕布局信息。</span><span class="sxs-lookup"><span data-stu-id="3690f-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="3690f-105">概览</span><span class="sxs-lookup"><span data-stu-id="3690f-105">Overview</span></span>

<span data-ttu-id="3690f-106">包括在 Retail 演示数据中的示例屏幕布局提供为各个零售段、商店工作人员角色和设备优化的内容。</span><span class="sxs-lookup"><span data-stu-id="3690f-106">The sample screen layouts that are included with Retail demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="3690f-107">一个布局可以包含多个布局大小和按钮网格组合，以在商店工作人员在设备和工作站之间移动时帮助确保覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="3690f-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="3690f-108">此主题突出介绍了这些布局之间的区别、它们提供的操作和整体体验。</span><span class="sxs-lookup"><span data-stu-id="3690f-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![跨设备演示数据布局](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="3690f-110">屏幕布局 ID 的分类</span><span class="sxs-lookup"><span data-stu-id="3690f-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="3690f-111">若要查找 Retail 中的屏幕布局，请转到 **Retail** > **渠道设置** > **POS 设置** > **POS** > **屏幕布局**。</span><span class="sxs-lookup"><span data-stu-id="3690f-111">To find screen layouts in Retail, go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>

![Retail 中的屏幕布局页面](../retail/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="3690f-113">屏幕布局 ID 最多可以有 10 个字符。</span><span class="sxs-lookup"><span data-stu-id="3690f-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="3690f-114">ID 是一个包括三个信息的字符串，按以下顺序：</span><span class="sxs-lookup"><span data-stu-id="3690f-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="3690f-115">公司</span><span class="sxs-lookup"><span data-stu-id="3690f-115">Company</span></span>
2. <span data-ttu-id="3690f-116">布局版本</span><span class="sxs-lookup"><span data-stu-id="3690f-116">Layout version</span></span>
3. <span data-ttu-id="3690f-117">人员</span><span class="sxs-lookup"><span data-stu-id="3690f-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="3690f-118">公司</span><span class="sxs-lookup"><span data-stu-id="3690f-118">Company</span></span>

| <span data-ttu-id="3690f-119">字母</span><span class="sxs-lookup"><span data-stu-id="3690f-119">Letter</span></span> | <span data-ttu-id="3690f-120">公司</span><span class="sxs-lookup"><span data-stu-id="3690f-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="3690f-121">A</span><span class="sxs-lookup"><span data-stu-id="3690f-121">A</span></span>      | <span data-ttu-id="3690f-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="3690f-122">Adventure Works</span></span> |
| <span data-ttu-id="3690f-123">F</span><span class="sxs-lookup"><span data-stu-id="3690f-123">F</span></span>      | <span data-ttu-id="3690f-124">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="3690f-124">Fabrikam</span></span>        |
| <span data-ttu-id="3690f-125">C</span><span class="sxs-lookup"><span data-stu-id="3690f-125">C</span></span>      | <span data-ttu-id="3690f-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="3690f-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="3690f-127">布局版本</span><span class="sxs-lookup"><span data-stu-id="3690f-127">Layout version</span></span>

| <span data-ttu-id="3690f-128">版本号</span><span class="sxs-lookup"><span data-stu-id="3690f-128">Version number</span></span> | <span data-ttu-id="3690f-129">说明</span><span class="sxs-lookup"><span data-stu-id="3690f-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3690f-130">3</span><span class="sxs-lookup"><span data-stu-id="3690f-130">3</span></span>              | <span data-ttu-id="3690f-131">支持各种设备和纵横比的多个屏幕尺寸的基本版本</span><span class="sxs-lookup"><span data-stu-id="3690f-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="3690f-132">3.1</span><span class="sxs-lookup"><span data-stu-id="3690f-132">3.1</span></span>            | <span data-ttu-id="3690f-133">具有其他**建议的产品**面板支持的基础版本</span><span class="sxs-lookup"><span data-stu-id="3690f-133">The base version that has additional support for the **Recommended products** panel</span></span>        |

### <a name="persona"></a><span data-ttu-id="3690f-134">人员</span><span class="sxs-lookup"><span data-stu-id="3690f-134">Persona</span></span>

| <span data-ttu-id="3690f-135">缩写</span><span class="sxs-lookup"><span data-stu-id="3690f-135">Abbreviation</span></span> | <span data-ttu-id="3690f-136">人员</span><span class="sxs-lookup"><span data-stu-id="3690f-136">Persona</span></span>       | <span data-ttu-id="3690f-137">内容</span><span class="sxs-lookup"><span data-stu-id="3690f-137">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="3690f-138">CSH</span><span class="sxs-lookup"><span data-stu-id="3690f-138">CSH</span></span>          | <span data-ttu-id="3690f-139">出纳</span><span class="sxs-lookup"><span data-stu-id="3690f-139">Cashier</span></span>       | <span data-ttu-id="3690f-140">出纳布局包括所有与交易相关的操作，如客户订单、退货、折扣、失效和礼品卡。</span><span class="sxs-lookup"><span data-stu-id="3690f-140">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="3690f-141">这些布局还包括库存管理的日常任务，如价格检查、库存查找和存货盘点。</span><span class="sxs-lookup"><span data-stu-id="3690f-141">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="3690f-142">基本的班次管理还为初始金额、暂停班次和打卡时间提供。</span><span class="sxs-lookup"><span data-stu-id="3690f-142">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="3690f-143">MGR</span><span class="sxs-lookup"><span data-stu-id="3690f-143">MGR</span></span>          | <span data-ttu-id="3690f-144">商店经理</span><span class="sxs-lookup"><span data-stu-id="3690f-144">Store Manager</span></span> | <span data-ttu-id="3690f-145">商店经理布局包括在出纳布局中找到的所有交易相关操作，而且包括税覆盖。</span><span class="sxs-lookup"><span data-stu-id="3690f-145">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="3690f-146">这些布局还包括库存管理的日常任务，如价格检查、库存查找和存货盘点。</span><span class="sxs-lookup"><span data-stu-id="3690f-146">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="3690f-147">班次管理为开始、暂停和结束班次提供。</span><span class="sxs-lookup"><span data-stu-id="3690f-147">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="3690f-148">此外，这些布局还包括输入、删除、钱币清点以及金库投箱和银行投箱的开票人操作。</span><span class="sxs-lookup"><span data-stu-id="3690f-148">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="3690f-149">最后，这些布局包括对绩效报表的访问，以及启用要打印的 X 和 Z 报表。</span><span class="sxs-lookup"><span data-stu-id="3690f-149">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="3690f-150">STK</span><span class="sxs-lookup"><span data-stu-id="3690f-150">STK</span></span>          | <span data-ttu-id="3690f-151">保管员</span><span class="sxs-lookup"><span data-stu-id="3690f-151">Stock Clerk</span></span>   | <span data-ttu-id="3690f-152">保管员布局针对库存管理进行了优化。</span><span class="sxs-lookup"><span data-stu-id="3690f-152">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="3690f-153">它们包括对价格检查、库存查找、领料和收货、库存盘点和配套件拆卸的日常任务的访问。</span><span class="sxs-lookup"><span data-stu-id="3690f-153">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="3690f-154">这些布局还为时钟和暂停班次提供基本班次操作。</span><span class="sxs-lookup"><span data-stu-id="3690f-154">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="3690f-155">尽管这些布局主要用于后勤办公室任务，保管员与出纳的交易记录屏幕具有相同的操作。</span><span class="sxs-lookup"><span data-stu-id="3690f-155">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="3690f-156">示例布局</span><span class="sxs-lookup"><span data-stu-id="3690f-156">Example layout</span></span>

<span data-ttu-id="3690f-157">这是 Fabrikam 公司、布局版本 3 和人员为商店经理的屏幕布局 ID 的示例：</span><span class="sxs-lookup"><span data-stu-id="3690f-157">Here is an example of a screen layout ID for the Fabrikam company, layout version 3, and the Store Manager persona:</span></span>

<span data-ttu-id="3690f-158">F3MGR</span><span class="sxs-lookup"><span data-stu-id="3690f-158">F3MGR</span></span>

<span data-ttu-id="3690f-159">下图显示 Fabrikam 商店经理的欢迎屏幕的示例。</span><span class="sxs-lookup"><span data-stu-id="3690f-159">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![Fabrikam 商店经理的欢迎屏幕](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="3690f-161">布局大小</span><span class="sxs-lookup"><span data-stu-id="3690f-161">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="3690f-162">完整型布局与紧凑型布局</span><span class="sxs-lookup"><span data-stu-id="3690f-162">Full vs. compact layouts</span></span>

<span data-ttu-id="3690f-163">屏幕布局同时具有完整设备和紧凑设备的配置。</span><span class="sxs-lookup"><span data-stu-id="3690f-163">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="3690f-164">因此，用户可以被分配一个屏幕布局，而该屏幕布局支持商店内的多种尺寸和外形。</span><span class="sxs-lookup"><span data-stu-id="3690f-164">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="3690f-165">**现代 POS - 完整型** – 通常，完整型布局最适合较大显示器，如台式机显示器或平板电脑。</span><span class="sxs-lookup"><span data-stu-id="3690f-165">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="3690f-166">用户可以选择布局包含的元素 UI，指定这些元素的尺寸和位置，并配置它们的详细属性。</span><span class="sxs-lookup"><span data-stu-id="3690f-166">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="3690f-167">完整型布局同时支持垂直配置和水平配置。</span><span class="sxs-lookup"><span data-stu-id="3690f-167">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="3690f-168">**现代 POS - 紧凑型** - 通常，紧凑型布局最适合手机或小平板电脑。</span><span class="sxs-lookup"><span data-stu-id="3690f-168">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="3690f-169">对于紧凑型设备，设计功能受到限制。</span><span class="sxs-lookup"><span data-stu-id="3690f-169">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="3690f-170">用户可以为收据窗格和总计窗格配置列和字段。</span><span class="sxs-lookup"><span data-stu-id="3690f-170">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="3690f-171">提供的屏幕分辨率</span><span class="sxs-lookup"><span data-stu-id="3690f-171">Screen resolutions that are provided</span></span>

<span data-ttu-id="3690f-172">下表显示为典型的屏幕分辨率提供的布局大小。</span><span class="sxs-lookup"><span data-stu-id="3690f-172">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="3690f-173">布局类型</span><span class="sxs-lookup"><span data-stu-id="3690f-173">Layout type</span></span> | <span data-ttu-id="3690f-174">分辨率</span><span class="sxs-lookup"><span data-stu-id="3690f-174">Resolution</span></span> | <span data-ttu-id="3690f-175">纵横比</span><span class="sxs-lookup"><span data-stu-id="3690f-175">Aspect ratio</span></span> | <span data-ttu-id="3690f-176">目标显示</span><span class="sxs-lookup"><span data-stu-id="3690f-176">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="3690f-177">压缩\*</span><span class="sxs-lookup"><span data-stu-id="3690f-177">Compact\*</span></span>   | <span data-ttu-id="3690f-178">480 × 853</span><span class="sxs-lookup"><span data-stu-id="3690f-178">480 × 853</span></span>  | <span data-ttu-id="3690f-179">16:9</span><span class="sxs-lookup"><span data-stu-id="3690f-179">16:9</span></span>         | <span data-ttu-id="3690f-180">电话</span><span class="sxs-lookup"><span data-stu-id="3690f-180">Phones</span></span>                  |
| <span data-ttu-id="3690f-181">完全</span><span class="sxs-lookup"><span data-stu-id="3690f-181">Full</span></span>        | <span data-ttu-id="3690f-182">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="3690f-182">1024 × 768</span></span> | <span data-ttu-id="3690f-183">4:3</span><span class="sxs-lookup"><span data-stu-id="3690f-183">4:3</span></span>          | <span data-ttu-id="3690f-184">平板电脑</span><span class="sxs-lookup"><span data-stu-id="3690f-184">Tablets</span></span>                 |
| <span data-ttu-id="3690f-185">完全\*</span><span class="sxs-lookup"><span data-stu-id="3690f-185">Full\*</span></span>      | <span data-ttu-id="3690f-186">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="3690f-186">1280 × 720</span></span> | <span data-ttu-id="3690f-187">16:9</span><span class="sxs-lookup"><span data-stu-id="3690f-187">16:9</span></span>         | <span data-ttu-id="3690f-188">平板电脑</span><span class="sxs-lookup"><span data-stu-id="3690f-188">Tablets</span></span>                 |
| <span data-ttu-id="3690f-189">完全</span><span class="sxs-lookup"><span data-stu-id="3690f-189">Full</span></span>        | <span data-ttu-id="3690f-190">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="3690f-190">1366 × 768</span></span> | <span data-ttu-id="3690f-191">16:9</span><span class="sxs-lookup"><span data-stu-id="3690f-191">16:9</span></span>         | <span data-ttu-id="3690f-192">平板电脑，较大屏幕</span><span class="sxs-lookup"><span data-stu-id="3690f-192">Tablets, larger screens</span></span> |
| <span data-ttu-id="3690f-193">完全</span><span class="sxs-lookup"><span data-stu-id="3690f-193">Full</span></span>        | <span data-ttu-id="3690f-194">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="3690f-194">1440 × 960</span></span> | <span data-ttu-id="3690f-195">3:2</span><span class="sxs-lookup"><span data-stu-id="3690f-195">3:2</span></span>          | <span data-ttu-id="3690f-196">平板电脑，较大屏幕</span><span class="sxs-lookup"><span data-stu-id="3690f-196">Tablets, larger screens</span></span> |

<span data-ttu-id="3690f-197">\*这些额外的布局大小仅在 Adventure Works 和 Fabrikam 布局中提供。</span><span class="sxs-lookup"><span data-stu-id="3690f-197">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>


>[!TIP]
> <span data-ttu-id="3690f-198">POS 基于与可用于当前应用窗口的屏幕分辨率最接近的大小自动选择布局大小。</span><span class="sxs-lookup"><span data-stu-id="3690f-198">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="3690f-199">若要查找当前使用的屏幕布局 ID 和布局分辨率，在 Retail Modern POS (MPOS) 或 Retail Cloud POS 中，打开**设置**页，然后在**会话信息**部分查找。</span><span class="sxs-lookup"><span data-stu-id="3690f-199">To find the screen layout ID and layout resolution that are currently used, in Retail Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="3690f-200">您还可以看到当前应用程序或浏览器框架的实际窗口分辨率。</span><span class="sxs-lookup"><span data-stu-id="3690f-200">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="3690f-201">在具有此信息后，可以查找 Retail 中布局内容的源，方法是转到**渠道设置** > **POS 设置** > **POS** > **屏幕布局**。</span><span class="sxs-lookup"><span data-stu-id="3690f-201">After you have this information, you can find the source of the layout content in Retail by going to **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>


![Retail 和 POS 中的屏幕布局和布局分辨率/大小](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="3690f-203">公司和品牌</span><span class="sxs-lookup"><span data-stu-id="3690f-203">Companies and brands</span></span>

<span data-ttu-id="3690f-204">每个虚构的公司面向不同的零售段，包含为公司的市场调整的产品目录。</span><span class="sxs-lookup"><span data-stu-id="3690f-204">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="3690f-205">每家公司都具有伴随其产品的独一无二的视觉品牌。</span><span class="sxs-lookup"><span data-stu-id="3690f-205">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="3690f-206">品牌元素包括个性色、深色主题或浅色主题，以及提供逼真体验的附带照片。</span><span class="sxs-lookup"><span data-stu-id="3690f-206">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="3690f-207">公司细分市场和视觉特征</span><span class="sxs-lookup"><span data-stu-id="3690f-207">Company segment and visual characteristics</span></span>

| <span data-ttu-id="3690f-208">公司</span><span class="sxs-lookup"><span data-stu-id="3690f-208">Company</span></span>         | <span data-ttu-id="3690f-209">库位</span><span class="sxs-lookup"><span data-stu-id="3690f-209">Location</span></span> | <span data-ttu-id="3690f-210">分段</span><span class="sxs-lookup"><span data-stu-id="3690f-210">Segment</span></span>        | <span data-ttu-id="3690f-211">个性</span><span class="sxs-lookup"><span data-stu-id="3690f-211">Accent</span></span> | <span data-ttu-id="3690f-212">主题</span><span class="sxs-lookup"><span data-stu-id="3690f-212">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="3690f-213">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="3690f-213">Adventure Works</span></span> | <span data-ttu-id="3690f-214">西雅图</span><span class="sxs-lookup"><span data-stu-id="3690f-214">Seattle</span></span>  | <span data-ttu-id="3690f-215">体育用品</span><span class="sxs-lookup"><span data-stu-id="3690f-215">Sporting Goods</span></span> | <span data-ttu-id="3690f-216">蓝色</span><span class="sxs-lookup"><span data-stu-id="3690f-216">Blue</span></span>   | <span data-ttu-id="3690f-217">深色</span><span class="sxs-lookup"><span data-stu-id="3690f-217">Dark</span></span>  |
| <span data-ttu-id="3690f-218">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="3690f-218">Fabrikam</span></span>        | <span data-ttu-id="3690f-219">休斯敦</span><span class="sxs-lookup"><span data-stu-id="3690f-219">Houston</span></span>  | <span data-ttu-id="3690f-220">风格</span><span class="sxs-lookup"><span data-stu-id="3690f-220">Fashion</span></span>        | <span data-ttu-id="3690f-221">绿色</span><span class="sxs-lookup"><span data-stu-id="3690f-221">Green</span></span>  | <span data-ttu-id="3690f-222">浅</span><span class="sxs-lookup"><span data-stu-id="3690f-222">Light</span></span> |
| <span data-ttu-id="3690f-223">Contoso</span><span class="sxs-lookup"><span data-stu-id="3690f-223">Contoso</span></span>         | <span data-ttu-id="3690f-224">波士顿</span><span class="sxs-lookup"><span data-stu-id="3690f-224">Boston</span></span>   | <span data-ttu-id="3690f-225">电子</span><span class="sxs-lookup"><span data-stu-id="3690f-225">Electronics</span></span>    | <span data-ttu-id="3690f-226">红色</span><span class="sxs-lookup"><span data-stu-id="3690f-226">Red</span></span>    | <span data-ttu-id="3690f-227">深色</span><span class="sxs-lookup"><span data-stu-id="3690f-227">Dark</span></span>  |


>[!NOTE]
> <span data-ttu-id="3690f-228">Adventure Works 和 Fabrikam 为两个旗舰品牌。</span><span class="sxs-lookup"><span data-stu-id="3690f-228">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="3690f-229">Contoso 可用，但并不提供所有布局。</span><span class="sxs-lookup"><span data-stu-id="3690f-229">Contoso is available, but not all layouts have been provided.</span></span>


<span data-ttu-id="3690f-230">下图显示了三个虚构公司的欢迎页面和交易页面示例。</span><span class="sxs-lookup"><span data-stu-id="3690f-230">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="3690f-231">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="3690f-231">Adventure Works</span></span>

![演示数据：Adventure Works 的欢迎页面](../retail/media/demo-screen-layouts-fig-4-1a.png)

![演示数据：Adventure Works 的交易页面](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="3690f-234">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="3690f-234">Fabrikam</span></span>

![演示数据：Fabrikam 的欢迎页面](../retail/media/demo-screen-layouts-fig-4-2a.png)

![演示数据：Fabrikam 的交易页面](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="3690f-237">Contoso</span><span class="sxs-lookup"><span data-stu-id="3690f-237">Contoso</span></span>

![演示数据：Contoso 的布局](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="3690f-239">用户登录矩阵</span><span class="sxs-lookup"><span data-stu-id="3690f-239">User sign in matrix</span></span>

<span data-ttu-id="3690f-240">已为各个屏幕布局提供了用户。</span><span class="sxs-lookup"><span data-stu-id="3690f-240">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="3690f-241">通过使用下表，您应该能够访问任何屏幕。</span><span class="sxs-lookup"><span data-stu-id="3690f-241">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="3690f-242">使用相应的操作员 ID 登录。</span><span class="sxs-lookup"><span data-stu-id="3690f-242">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="3690f-243">公司</span><span class="sxs-lookup"><span data-stu-id="3690f-243">Company</span></span>         | <span data-ttu-id="3690f-244">屏幕布局 ID</span><span class="sxs-lookup"><span data-stu-id="3690f-244">Screen layout ID</span></span> | <span data-ttu-id="3690f-245">人员</span><span class="sxs-lookup"><span data-stu-id="3690f-245">Persona</span></span>          | <span data-ttu-id="3690f-246">操作员 ID</span><span class="sxs-lookup"><span data-stu-id="3690f-246">Operator IDs</span></span>           |
|-----------------|------------------|---------------   |------------------------|
| <span data-ttu-id="3690f-247">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="3690f-247">Adventure Works</span></span> | <span data-ttu-id="3690f-248">A3MGR</span><span class="sxs-lookup"><span data-stu-id="3690f-248">A3MGR</span></span>            | <span data-ttu-id="3690f-249">商店经理</span><span class="sxs-lookup"><span data-stu-id="3690f-249">Store Manager</span></span>    | <span data-ttu-id="3690f-250">000154、000137、000073</span><span class="sxs-lookup"><span data-stu-id="3690f-250">000154, 000137, 000073</span></span> |
| <span data-ttu-id="3690f-251">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="3690f-251">Adventure Works</span></span> | <span data-ttu-id="3690f-252">A3CSH</span><span class="sxs-lookup"><span data-stu-id="3690f-252">A3CSH</span></span>            | <span data-ttu-id="3690f-253">出纳</span><span class="sxs-lookup"><span data-stu-id="3690f-253">Cashier</span></span>          | <span data-ttu-id="3690f-254">000150、000175、000165</span><span class="sxs-lookup"><span data-stu-id="3690f-254">000150, 000175, 000165</span></span> |
| <span data-ttu-id="3690f-255">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="3690f-255">Adventure Works</span></span> | <span data-ttu-id="3690f-256">A3STK</span><span class="sxs-lookup"><span data-stu-id="3690f-256">A3STK</span></span>            | <span data-ttu-id="3690f-257">保管员</span><span class="sxs-lookup"><span data-stu-id="3690f-257">Stock Clerk</span></span>      | <span data-ttu-id="3690f-258">000155、000181、000152</span><span class="sxs-lookup"><span data-stu-id="3690f-258">000155, 000181, 000152</span></span> |
| <span data-ttu-id="3690f-259">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="3690f-259">Fabrikam</span></span>        | <span data-ttu-id="3690f-260">F3MGR</span><span class="sxs-lookup"><span data-stu-id="3690f-260">F3MGR</span></span>            | <span data-ttu-id="3690f-261">商店经理</span><span class="sxs-lookup"><span data-stu-id="3690f-261">Store Manager</span></span>    | <span data-ttu-id="3690f-262">000160、000168、000163</span><span class="sxs-lookup"><span data-stu-id="3690f-262">000160, 000168, 000163</span></span> |
| <span data-ttu-id="3690f-263">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="3690f-263">Fabrikam</span></span>        | <span data-ttu-id="3690f-264">F3CSH</span><span class="sxs-lookup"><span data-stu-id="3690f-264">F3CSH</span></span>            | <span data-ttu-id="3690f-265">出纳</span><span class="sxs-lookup"><span data-stu-id="3690f-265">Cashier</span></span>          | <span data-ttu-id="3690f-266">000161、000113、000114</span><span class="sxs-lookup"><span data-stu-id="3690f-266">000161, 000113, 000114</span></span> |
| <span data-ttu-id="3690f-267">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="3690f-267">Fabrikam</span></span>        | <span data-ttu-id="3690f-268">F3STK</span><span class="sxs-lookup"><span data-stu-id="3690f-268">F3STK</span></span>            | <span data-ttu-id="3690f-269">保管员</span><span class="sxs-lookup"><span data-stu-id="3690f-269">Stock Clerk</span></span>      | <span data-ttu-id="3690f-270">000164、000112、000123</span><span class="sxs-lookup"><span data-stu-id="3690f-270">000164, 000112, 000123</span></span> |
| <span data-ttu-id="3690f-271">Contoso</span><span class="sxs-lookup"><span data-stu-id="3690f-271">Contoso</span></span>         | <span data-ttu-id="3690f-272">C3MGR</span><span class="sxs-lookup"><span data-stu-id="3690f-272">C3MGR</span></span>            | <span data-ttu-id="3690f-273">商店经理</span><span class="sxs-lookup"><span data-stu-id="3690f-273">Store Manager</span></span>    | <span data-ttu-id="3690f-274">000100、000111</span><span class="sxs-lookup"><span data-stu-id="3690f-274">000100, 000111</span></span>         |
| <span data-ttu-id="3690f-275">Contoso</span><span class="sxs-lookup"><span data-stu-id="3690f-275">Contoso</span></span>         | <span data-ttu-id="3690f-276">C3CSH</span><span class="sxs-lookup"><span data-stu-id="3690f-276">C3CSH</span></span>            | <span data-ttu-id="3690f-277">出纳</span><span class="sxs-lookup"><span data-stu-id="3690f-277">Cashier</span></span>          | <span data-ttu-id="3690f-278">000110、000120</span><span class="sxs-lookup"><span data-stu-id="3690f-278">000110, 000120</span></span>         |
| <span data-ttu-id="3690f-279">Contoso</span><span class="sxs-lookup"><span data-stu-id="3690f-279">Contoso</span></span>         | <span data-ttu-id="3690f-280">不适用</span><span class="sxs-lookup"><span data-stu-id="3690f-280">Not applicable</span></span>   | <span data-ttu-id="3690f-281">保管员</span><span class="sxs-lookup"><span data-stu-id="3690f-281">Stock Clerk</span></span>      | <span data-ttu-id="3690f-282">不适用</span><span class="sxs-lookup"><span data-stu-id="3690f-282">Not applicable</span></span>         |


>[!TIP]
> <span data-ttu-id="3690f-283">为了达到最佳效果，请在相应的商店位置激活收银机，然后将公司设置为您计划在登录时使用的人员的公司。</span><span class="sxs-lookup"><span data-stu-id="3690f-283">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="3690f-284">这样，您可以帮助确保视觉形象和品牌图像与整个体验一致。</span><span class="sxs-lookup"><span data-stu-id="3690f-284">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="3690f-285">例如，如果您有兴趣查看出纳的 Fabrikam 布局，则应该在休斯敦商店激活收银机。</span><span class="sxs-lookup"><span data-stu-id="3690f-285">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->
