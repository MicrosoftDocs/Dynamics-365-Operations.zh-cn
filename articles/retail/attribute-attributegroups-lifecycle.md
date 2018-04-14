---
title: "Finance and Operations 中各种零售实体的属性、属性组及其关联"
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ad524e8d585da2140f3cdae17e3a1a2832ada3f0
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="attributes-attribute-groups-and-their-associations-with-various-retail-entities-in-finance-and-operations"></a><span data-ttu-id="0ff3b-102">Finance and Operations 中各种零售实体的属性、属性组及其关联</span><span class="sxs-lookup"><span data-stu-id="0ff3b-102">Attributes, attribute groups, and their associations with various Retail entities in Finance and Operations</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="0ff3b-103">可通过*属性*和用户定义的字段（**如内存大小**、**硬盘容量**、**符合能源之星的要求**等）进一步描述产品及其特征。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-103">*Attributes* provide a way to further describe a product and its characteristics through user-defined fields (such as **Memory size**, **Hard disk capacity**, **Is Energy star compliant**, and so on).</span></span> <span data-ttu-id="0ff3b-104">在 Microsoft Dynamics 365 for Finance and Operations 中，可以将属性与各种零售实体（如产品类别和零售通道）关联，并且可以为属性设置默认值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-104">In Microsoft Dynamics 365 for Finance and Operations, attributes can be associated with various Retail entities, such as product categories and retail channels, and default values can be set for them.</span></span> <span data-ttu-id="0ff3b-105">当产品与产品类别或销售渠道关联时，产品将继承属性及默认值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-105">Products then inherit the attributes and the default values when they are associated with the product categories or retail channels.</span></span> <span data-ttu-id="0ff3b-106">默认值可在单个产品级别、在零售渠道级别或在零售目录中覆盖。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-106">The default values can be overridden at the individual product level, at the retail channel level, or in a retail catalog.</span></span>
 
<span data-ttu-id="0ff3b-107">例如，电视机产品通常具有以下属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-107">For example, a typical television product might have the following attributes.</span></span>

| <span data-ttu-id="0ff3b-108">类别</span><span class="sxs-lookup"><span data-stu-id="0ff3b-108">Category</span></span>   | <span data-ttu-id="0ff3b-109">属性</span><span class="sxs-lookup"><span data-stu-id="0ff3b-109">Attribute</span></span>                | <span data-ttu-id="0ff3b-110">允许的值</span><span class="sxs-lookup"><span data-stu-id="0ff3b-110">Permissible values</span></span>          | <span data-ttu-id="0ff3b-111">默认值</span><span class="sxs-lookup"><span data-stu-id="0ff3b-111">Default value</span></span> |
|------------|--------------------------|-----------------------------|---------------|
| <span data-ttu-id="0ff3b-112">电视和视频</span><span class="sxs-lookup"><span data-stu-id="0ff3b-112">TV & Video</span></span> | <span data-ttu-id="0ff3b-113">品牌</span><span class="sxs-lookup"><span data-stu-id="0ff3b-113">Brand</span></span>                    | <span data-ttu-id="0ff3b-114">任何有效的品牌值</span><span class="sxs-lookup"><span data-stu-id="0ff3b-114">Any valid brand value</span></span>       | <span data-ttu-id="0ff3b-115">None</span><span class="sxs-lookup"><span data-stu-id="0ff3b-115">None</span></span>          |
| <span data-ttu-id="0ff3b-116">电视</span><span class="sxs-lookup"><span data-stu-id="0ff3b-116">TV</span></span>         | <span data-ttu-id="0ff3b-117">屏幕尺寸</span><span class="sxs-lookup"><span data-stu-id="0ff3b-117">Screen Size</span></span>              | <span data-ttu-id="0ff3b-118">20–80 英寸</span><span class="sxs-lookup"><span data-stu-id="0ff3b-118">20–80 inches</span></span>                | <span data-ttu-id="0ff3b-119">None</span><span class="sxs-lookup"><span data-stu-id="0ff3b-119">None</span></span>          |
|            | <span data-ttu-id="0ff3b-120">垂直行业解决方案</span><span class="sxs-lookup"><span data-stu-id="0ff3b-120">Vertical Resolution</span></span>      | <span data-ttu-id="0ff3b-121">480i、720p、1080i 或 1080p</span><span class="sxs-lookup"><span data-stu-id="0ff3b-121">480i, 720p, 1080i, or 1080p</span></span> | <span data-ttu-id="0ff3b-122">1080p</span><span class="sxs-lookup"><span data-stu-id="0ff3b-122">1080p</span></span>         |
|            | <span data-ttu-id="0ff3b-123">屏幕刷新率</span><span class="sxs-lookup"><span data-stu-id="0ff3b-123">Screen Refresh Rate</span></span>      | <span data-ttu-id="0ff3b-124">60hz、120hz 或 240hz</span><span class="sxs-lookup"><span data-stu-id="0ff3b-124">60hz, 120hz, or 240hz</span></span>       | <span data-ttu-id="0ff3b-125">60hz</span><span class="sxs-lookup"><span data-stu-id="0ff3b-125">60hz</span></span>          |
|            | <span data-ttu-id="0ff3b-126">HDMI 输入</span><span class="sxs-lookup"><span data-stu-id="0ff3b-126">HDMI Inputs</span></span>              | <span data-ttu-id="0ff3b-127">0–10</span><span class="sxs-lookup"><span data-stu-id="0ff3b-127">0–10</span></span>                        | <span data-ttu-id="0ff3b-128">3</span><span class="sxs-lookup"><span data-stu-id="0ff3b-128">3</span></span>             |
|            | <span data-ttu-id="0ff3b-129">DVI 输入</span><span class="sxs-lookup"><span data-stu-id="0ff3b-129">DVI Inputs</span></span>               | <span data-ttu-id="0ff3b-130">0–10</span><span class="sxs-lookup"><span data-stu-id="0ff3b-130">0–10</span></span>                        | <span data-ttu-id="0ff3b-131">1</span><span class="sxs-lookup"><span data-stu-id="0ff3b-131">1</span></span>             |
|            | <span data-ttu-id="0ff3b-132">复合输入</span><span class="sxs-lookup"><span data-stu-id="0ff3b-132">Composite Inputs</span></span>         | <span data-ttu-id="0ff3b-133">0–10</span><span class="sxs-lookup"><span data-stu-id="0ff3b-133">0–10</span></span>                        | <span data-ttu-id="0ff3b-134">2</span><span class="sxs-lookup"><span data-stu-id="0ff3b-134">2</span></span>             |
|            | <span data-ttu-id="0ff3b-135">组件输入</span><span class="sxs-lookup"><span data-stu-id="0ff3b-135">Component Inputs</span></span>         | <span data-ttu-id="0ff3b-136">0–10</span><span class="sxs-lookup"><span data-stu-id="0ff3b-136">0–10</span></span>                        | <span data-ttu-id="0ff3b-137">1</span><span class="sxs-lookup"><span data-stu-id="0ff3b-137">1</span></span>             |
| <span data-ttu-id="0ff3b-138">LCD</span><span class="sxs-lookup"><span data-stu-id="0ff3b-138">LCD</span></span>        | <span data-ttu-id="0ff3b-139">3D 已就绪</span><span class="sxs-lookup"><span data-stu-id="0ff3b-139">3D Ready</span></span>                 | <span data-ttu-id="0ff3b-140">是或否</span><span class="sxs-lookup"><span data-stu-id="0ff3b-140">Yes or No</span></span>                   | <span data-ttu-id="0ff3b-141">是</span><span class="sxs-lookup"><span data-stu-id="0ff3b-141">Yes</span></span>           |
|            | <span data-ttu-id="0ff3b-142">3D 已启用</span><span class="sxs-lookup"><span data-stu-id="0ff3b-142">3D Enabled</span></span>               | <span data-ttu-id="0ff3b-143">是或否</span><span class="sxs-lookup"><span data-stu-id="0ff3b-143">Yes or No</span></span>                   | <span data-ttu-id="0ff3b-144">无</span><span class="sxs-lookup"><span data-stu-id="0ff3b-144">No</span></span>            |
| <span data-ttu-id="0ff3b-145">等离子</span><span class="sxs-lookup"><span data-stu-id="0ff3b-145">Plasma</span></span>     | <span data-ttu-id="0ff3b-146">最低工作温度</span><span class="sxs-lookup"><span data-stu-id="0ff3b-146">Operating Temp From</span></span>      | <span data-ttu-id="0ff3b-147">32–110 度</span><span class="sxs-lookup"><span data-stu-id="0ff3b-147">32–110 degrees</span></span>              | <span data-ttu-id="0ff3b-148">32</span><span class="sxs-lookup"><span data-stu-id="0ff3b-148">32</span></span>            |
|            | <span data-ttu-id="0ff3b-149">最高工作温度</span><span class="sxs-lookup"><span data-stu-id="0ff3b-149">Operating Temp To</span></span>        | <span data-ttu-id="0ff3b-150">32–110 度</span><span class="sxs-lookup"><span data-stu-id="0ff3b-150">32–110 degrees</span></span>              | <span data-ttu-id="0ff3b-151">100</span><span class="sxs-lookup"><span data-stu-id="0ff3b-151">100</span></span>           |
| <span data-ttu-id="0ff3b-152">投影</span><span class="sxs-lookup"><span data-stu-id="0ff3b-152">Projection</span></span> | <span data-ttu-id="0ff3b-153">投影管保修</span><span class="sxs-lookup"><span data-stu-id="0ff3b-153">Projection Tube Warranty</span></span> | <span data-ttu-id="0ff3b-154">6、12 或 18 个月</span><span class="sxs-lookup"><span data-stu-id="0ff3b-154">6, 12, or 18 months</span></span>         | <span data-ttu-id="0ff3b-155">12</span><span class="sxs-lookup"><span data-stu-id="0ff3b-155">12</span></span>            |
|            | <span data-ttu-id="0ff3b-156">投影管数</span><span class="sxs-lookup"><span data-stu-id="0ff3b-156"># of Projection Tubes</span></span>    | <span data-ttu-id="0ff3b-157">1–5</span><span class="sxs-lookup"><span data-stu-id="0ff3b-157">1–5</span></span>                         | <span data-ttu-id="0ff3b-158">3</span><span class="sxs-lookup"><span data-stu-id="0ff3b-158">3</span></span>             |

## <a name="attributes-and-attribute-types"></a><span data-ttu-id="0ff3b-159">属性和属性类型</span><span class="sxs-lookup"><span data-stu-id="0ff3b-159">Attributes and attribute types</span></span>

<span data-ttu-id="0ff3b-160">属性基于*属性类型*。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-160">Attributes are based on *attribute types*.</span></span> <span data-ttu-id="0ff3b-161">特性类型标识可为特定于特性输入数据的类型。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-161">The attribute type identifies the type of data that can be entered for a specific attribute.</span></span> <span data-ttu-id="0ff3b-162">Finance and Operations 目前支持以下属性类型：</span><span class="sxs-lookup"><span data-stu-id="0ff3b-162">Finance and Operations currently supports the following attribute types:</span></span>

- <span data-ttu-id="0ff3b-163">**货币** - 此类型支持货币值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-163">**Currency** – This type supports a currency value.</span></span> <span data-ttu-id="0ff3b-164">它可以受约束（即，它可以支持某个值范围），也可以保持开放。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-164">It can be bounded (that is, it can support a range of values), or it can be left open.</span></span>
- <span data-ttu-id="0ff3b-165">**日期时间** - 此类型支持日期和时间值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-165">**DateTime** – This type supports a date and time value.</span></span> <span data-ttu-id="0ff3b-166">它可以有范围，也可以保持开放。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-166">It can be bounded or left open.</span></span>
- <span data-ttu-id="0ff3b-167">**小数** - 此类型支持包括小数位的数字值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-167">**Decimal** – This type supports a numerical value that includes decimal places.</span></span> <span data-ttu-id="0ff3b-168">它还支持度量单位。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-168">It also supports a unit of measure.</span></span> <span data-ttu-id="0ff3b-169">它可以有范围，也可以保持开放。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-169">It can be bounded or left open.</span></span>
- <span data-ttu-id="0ff3b-170">**整数** - 此类型支持数字值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-170">**Integer** – This type supports a numerical value.</span></span> <span data-ttu-id="0ff3b-171">它还支持度量单位。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-171">It also supports a unit of measure.</span></span> <span data-ttu-id="0ff3b-172">它可以有范围，也可以保持开放。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-172">It can be bounded or left open.</span></span>
- <span data-ttu-id="0ff3b-173">**文本** - 此类型支持文本值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-173">**Text** – This type supports a text value.</span></span> <span data-ttu-id="0ff3b-174">它还支持预定义的一组可能值（即*枚举*）。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-174">It also supports a predefined set of possible values (that is, an *enumeration*).</span></span>
- <span data-ttu-id="0ff3b-175">**布尔** - 此类型支持二进制值（**true** 或 **false**）。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-175">**Boolean** – This type supports a binary value (**true** or **false**).</span></span>
- <span data-ttu-id="0ff3b-176">**引用** - 此类型引用其他属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-176">**Reference** – This type references other attributes.</span></span>

### <a name="set-up-attribute-types-in-finance-and-operations"></a><span data-ttu-id="0ff3b-177">在 Finance and Operations 中设置属性类型</span><span class="sxs-lookup"><span data-stu-id="0ff3b-177">Set up attribute types in Finance and Operations</span></span>

1. <span data-ttu-id="0ff3b-178">以零售促销经理的身份登录 Finance and Operations 后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-178">Sign in to the Finance and Operations back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="0ff3b-179">转到**产品信息管理** &gt; **设置** &gt; **类别和属性** &gt; **属性类型**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-179">Go to **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attribute types**.</span></span>
3. <span data-ttu-id="0ff3b-180">创建**文本**类型的两个属性类型，将**固定列表**选项设置为**是**，然后添加一列值：</span><span class="sxs-lookup"><span data-stu-id="0ff3b-180">Create two attribute types of the **Text** type, set the **Fixed list** option to **Yes**, and then add a list of values:</span></span>

    - <span data-ttu-id="0ff3b-181">将一个属性类型命名为**镜片形状**，然后添加以下值：**椭圆形**、**方形**和**三角形**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-181">Name one attribute type **Lens shape**, and add the following values: **Oval**, **Square**, and **Rectangle**.</span></span>
    - <span data-ttu-id="0ff3b-182">将另一个属性类型命名为**太阳镜品牌**，然后添加以下值：**Ray ban**、**Aviator** 和 **Oakley**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-182">Name the other attribute type **Sunglass brand**, and add the following values: **Ray ban**, **Aviator**, and **Oakley**.</span></span>

![属性类型](media/AttributeType.png)

### <a name="set-up-an-attribute-in-finance-and-operations"></a><span data-ttu-id="0ff3b-184">在 Finance and Operations 中设置属性</span><span class="sxs-lookup"><span data-stu-id="0ff3b-184">Set up an attribute in Finance and Operations</span></span>

1. <span data-ttu-id="0ff3b-185">以零售促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-185">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="0ff3b-186">转到**产品信息管理** &gt; **设置** &gt; **类别和属性** &gt; **属性**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-186">Go to **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attributes**.</span></span>
3. <span data-ttu-id="0ff3b-187">创建名为**镜片**的属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-187">Create an attribute that is named **Lens**.</span></span>
4. <span data-ttu-id="0ff3b-188">将**属性类型**字段设置为**镜片形状**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-188">Set the **Attribute type** field to **Lens shape**.</span></span>

![属性](media/Attribute.png)

## <a name="attribute-metadata"></a><span data-ttu-id="0ff3b-190">属性元数据</span><span class="sxs-lookup"><span data-stu-id="0ff3b-190">Attribute metadata</span></span>

<span data-ttu-id="0ff3b-191">*属性元数据*用于选择选项来指定各产品的属性的行为。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-191">*Attribute metadata* lets you select options to specify how the attributes for each product should behave.</span></span> <span data-ttu-id="0ff3b-192">例如，您可指定是否要求属性，它们是否可用于搜索，和他们是否可用作筛选器。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-192">For example, you can specify whether attributes are required, whether they can be used for searches, and whether they can be used as a filter.</span></span>

<span data-ttu-id="0ff3b-193">对于零售产品，可在渠道级别覆盖属性元数据设置。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-193">For retail products, the attribute metadata settings can be overridden at the channel level.</span></span> <span data-ttu-id="0ff3b-194">此主题后文将介绍此功能。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-194">This capability will be discussed later in this topic.</span></span>

<span data-ttu-id="0ff3b-195">您可能已经注意到，**属性**页中包含与属性元数据有关的选项。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-195">As you might notice, the **Attributes** page includes options that are related to attribute metadata.</span></span> <span data-ttu-id="0ff3b-196">在 **POS 属性元数据**下，一个名称为**可细化**的选项影响属性值在零售点 (POS) 中的行为或系统处理这些属性值的方式。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-196">Under **Attribute metadata for POS**, one option that is named **"Can be refined"** affects the behavior of the attribute values in the retail point of sale (POS) or the way that the system handles those attribute values.</span></span> <span data-ttu-id="0ff3b-197">只有可将其**可细化**选项设置为**是**的属性才会显示以供细化或在零售 POS 中筛选产品。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-197">Only attributes for which you may set the **"Can be refined"** option to **"Yes"**, will show up for refinement or filtering of products in the retail POS.</span></span>

<span data-ttu-id="0ff3b-198">下面是**属性**页中显示的其余属性元数据选项：</span><span class="sxs-lookup"><span data-stu-id="0ff3b-198">Here are the remaining attribute metadata options on the **Attributes** page:</span></span>

- <span data-ttu-id="0ff3b-199">可搜索</span><span class="sxs-lookup"><span data-stu-id="0ff3b-199">Searchable</span></span>
- <span data-ttu-id="0ff3b-200">可检索</span><span class="sxs-lookup"><span data-stu-id="0ff3b-200">Retrievable</span></span>
- <span data-ttu-id="0ff3b-201">可查询</span><span class="sxs-lookup"><span data-stu-id="0ff3b-201">Can be queried</span></span>
- <span data-ttu-id="0ff3b-202">可排序</span><span class="sxs-lookup"><span data-stu-id="0ff3b-202">Sortable</span></span>
- <span data-ttu-id="0ff3b-203">允许多个值</span><span class="sxs-lookup"><span data-stu-id="0ff3b-203">Allow multiple values</span></span>
- <span data-ttu-id="0ff3b-204">忽略大小写和格式</span><span class="sxs-lookup"><span data-stu-id="0ff3b-204">Ignore case and format</span></span>
- <span data-ttu-id="0ff3b-205">完成匹配</span><span class="sxs-lookup"><span data-stu-id="0ff3b-205">Complete match</span></span>

<span data-ttu-id="0ff3b-206">这些选项最初用于改进联机店面的搜索功能。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-206">These options were originally intended to improve the search functionality for the online storefront.</span></span> <span data-ttu-id="0ff3b-207">尽管 Finance and Operations 中不包含现成的联机店面，却的确包含电子商务发布软件开发包 (SDK)。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-207">Although Finance and Operations doesn't include the online storefront out of the box, it does include the eCommerce Publishing Software Development Kit (SDK).</span></span> <span data-ttu-id="0ff3b-208">客户可使用此 SDK 将产品放入所选搜索索引中。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-208">Customers can use this SDK to put products into a search index of their choice.</span></span> <span data-ttu-id="0ff3b-209">尽管导入了产品数据，客户仍然应该可以区分可搜索数据、可查询的数据等。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-209">Although the product data is imported, customers should still be able to distinguish searchable data, data that can be queried, and so on.</span></span> <span data-ttu-id="0ff3b-210">这样他们就可以构建最佳索引以确保仅为*他们认为*应该建立索引的属性建立索引。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-210">In that way, they can build an optimal index to make sure that they index only attributes that, *in their opinion*, should be indexed.</span></span>

<span data-ttu-id="0ff3b-211">有关其余这些选项的用途信息，请参阅 [SharePoint 2013 中的搜索架构概述](https://technet.microsoft.com/en-us/library/jj219669.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-211">For information about the purpose of these remaining options, see [Overview of the search schema in SharePoint Server 2013](https://technet.microsoft.com/en-us/library/jj219669.aspx).</span></span>

## <a name="filter-settings-for-attributes"></a><span data-ttu-id="0ff3b-212">属性的筛选设置</span><span class="sxs-lookup"><span data-stu-id="0ff3b-212">Filter settings for attributes</span></span>

<span data-ttu-id="0ff3b-213">可通过属性的筛选器设置定义属性的筛选器如何在零售 POS 中显示。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-213">Filter settings for attributes let you define how the filters for attributes are shown in the retail POS.</span></span> <span data-ttu-id="0ff3b-214">若要访问属性的筛选器设置，请在 Finance and Operations 中的**属性**页面上选择属性，然后在操作窗格中选择**筛选器设置**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-214">To access the filter settings for an attribute, on the **Attributes** page in Finance and Operations, select the attribute, and then, on the Action Pane, select **Filter settings**.</span></span>

<span data-ttu-id="0ff3b-215">**筛选器显示首选项**页面中包含以下字段：</span><span class="sxs-lookup"><span data-stu-id="0ff3b-215">The **Filter display preferences** page includes the following fields:</span></span>

- <span data-ttu-id="0ff3b-216">**名称** - 默认情况下，此字段设置为属性的名称。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-216">**Name** – By default, this field is set to the name of the attribute.</span></span> <span data-ttu-id="0ff3b-217">然而，您可以更改值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-217">However, you can change the value.</span></span>
- <span data-ttu-id="0ff3b-218">**显示选项** - 以下选项可用：</span><span class="sxs-lookup"><span data-stu-id="0ff3b-218">**Display option** – The following options are available:</span></span>

    - <span data-ttu-id="0ff3b-219">**单一值** - 此选项可用于以下属性类型：**布尔**、**货币**、**小数**、**整数**和**文本**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-219">**Single value** – This option is available for the following attribute types: **Boolean**, **Currency**, **Decimal**, **Integer**, and **Text**.</span></span> <span data-ttu-id="0ff3b-220">此选项支持在客户端中为这些属性选择单个值来进行细化。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-220">This option enables single value selection for these attributes in the client for refinement.</span></span>
    - <span data-ttu-id="0ff3b-221">**多个值** - 此选项可用于以下属性类型：**货币**、**小数**、**整数**和**文本**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-221">**Multi value** – This option is available for the following attribute types: **Currency**, **Decimal**, **Integer**, and **Text**.</span></span> <span data-ttu-id="0ff3b-222">此选项支持在客户端中为该属性选择多个值来进行细化。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-222">This option enables multi-value selection for this attribute in the client for refinement.</span></span>

- <span data-ttu-id="0ff3b-223">**显示控制** - 以下选项可用：</span><span class="sxs-lookup"><span data-stu-id="0ff3b-223">**Display control** – The following options are available:</span></span>

    - <span data-ttu-id="0ff3b-224">**列表** - 此选项可用于所有属性类型。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-224">**List** – This option is available for the all attribute types.</span></span>
    - <span data-ttu-id="0ff3b-225">**范围** - 此选项可用于以下属性类型：**货币**、**小数**和**整数**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-225">**Range** – This option is available for the following attribute types: **Currency**, **Decimal**, and **Integer**.</span></span> 
    - <span data-ttu-id="0ff3b-226">**滑块** - 此选项可用于以下属性类型：**货币**、**小数**和**整数**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-226">**Slider** – This option is available for the following attribute types: **Currency**, **Decimal**, and **Integer**.</span></span>
    - <span data-ttu-id="0ff3b-227">**带有滑块的滚动条** - 此选项可用于以下属性类型：**货币**、**小数**和**整数**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-227">**Slider with bars** – This option is available for the following attribute types: **Currency**, **Decimal**, and **Integer**.</span></span>

- <span data-ttu-id="0ff3b-228">**阈值** - 如果选择了**范围**作为显示控制类型，则需要此设置。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-228">**Threshold value** – This setting is required if you selected **Range** as the display control type.</span></span> <span data-ttu-id="0ff3b-229">可将分号 (;) 用作分隔符来定义值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-229">You can define values by using a semicolon (;) as a delimiter.</span></span>

    <span data-ttu-id="0ff3b-230">例如，对于**包容量**这样的筛选器，阈值可以为 **10; 20; 50; 100; 200; 500; 1000; 5000**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-230">For example, for the filter like **Bag Volume**, a threshold value can be **10; 20; 50; 100; 200; 500; 1000; 5000**.</span></span> <span data-ttu-id="0ff3b-231">在此情况下，零售 POS 将显示以下范围。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-231">In this case, the retail POS will show the following ranges.</span></span> <span data-ttu-id="0ff3b-232">所有在结果集中无任何产品的范围都将灰显。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-232">Any ranges that don't have any products in the result set will appear dimmed.</span></span>

    - <span data-ttu-id="0ff3b-233">小于 10</span><span class="sxs-lookup"><span data-stu-id="0ff3b-233">Less than 10</span></span>
    - <span data-ttu-id="0ff3b-234">10 - 20</span><span class="sxs-lookup"><span data-stu-id="0ff3b-234">10 – 20</span></span>
    - <span data-ttu-id="0ff3b-235">20 - 50</span><span class="sxs-lookup"><span data-stu-id="0ff3b-235">20 – 50</span></span>
    - <span data-ttu-id="0ff3b-236">50 - 100</span><span class="sxs-lookup"><span data-stu-id="0ff3b-236">50 – 100</span></span>
    - <span data-ttu-id="0ff3b-237">100 - 200</span><span class="sxs-lookup"><span data-stu-id="0ff3b-237">100 – 200</span></span>
    - <span data-ttu-id="0ff3b-238">200 - 500</span><span class="sxs-lookup"><span data-stu-id="0ff3b-238">200 – 500</span></span>
    - <span data-ttu-id="0ff3b-239">500 次或更多</span><span class="sxs-lookup"><span data-stu-id="0ff3b-239">500 or more</span></span>

![属性筛选器设置](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a><span data-ttu-id="0ff3b-241">属性组</span><span class="sxs-lookup"><span data-stu-id="0ff3b-241">Attribute groups</span></span>

<span data-ttu-id="0ff3b-242">定义属性之后，可将其分配给属性组。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-242">After attributes have been defined, they can be assigned to attribute groups.</span></span> <span data-ttu-id="0ff3b-243">*属性组*用于对产品中的一个组件或子组件的单个属性进行分组。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-243">An *attribute group* is used to group the individual attributes for a component or subcomponent in a product configuration model.</span></span> <span data-ttu-id="0ff3b-244">一个属性可以包含在多个属性组中。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-244">An attribute can be included in more than one attribute group.</span></span> <span data-ttu-id="0ff3b-245">属性组可帮助用户配置产品，因为可将多种选择安排到特定上下文中。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-245">Attribute groups can help users configure products, because the various selections are arranged in a specific context.</span></span> <span data-ttu-id="0ff3b-246">可将属性组分配给零售类别或零售渠道。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-246">Attribute groups can be assigned to retail categories or retail channels.</span></span>

<span data-ttu-id="0ff3b-247">您还可以为属性组中包含的属性设置默认值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-247">You can also set default values for attributes that are included in an attribute group.</span></span> <span data-ttu-id="0ff3b-248">例如，向属性组添加颜色属性，然后选择**蓝色**作为默认属性值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-248">For example, you add an attribute for color to an attribute group and select **Blue** as the default attribute value.</span></span> <span data-ttu-id="0ff3b-249">在此情况下，向零售产品添加包含颜色为其属性之一的属性组时，**蓝色**将显示为该产品的默认颜色。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-249">In this case, when the attribute group is added to a retail product that includes color as one of its attributes, **Blue** appears as the default color for that product.</span></span>

![属性组](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a><span data-ttu-id="0ff3b-251">创建属性组</span><span class="sxs-lookup"><span data-stu-id="0ff3b-251">Create an attribute group</span></span>

1. <span data-ttu-id="0ff3b-252">以零售促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-252">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="0ff3b-253">转到**产品信息管理** &gt; **设置** &gt; **类别和属性** &gt; **属性组**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-253">Go to **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attribute groups**.</span></span>
3. <span data-ttu-id="0ff3b-254">创建一个名称为**时尚太阳镜**的属性组。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-254">Create an attribute group that is named **Fashion Sunglasses**.</span></span>
4. <span data-ttu-id="0ff3b-255">添加以下属性：**镜片形状** 和**太阳镜品牌**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-255">Add the following attributes: **Lens shape** and **Sunglass brand**.</span></span>

### <a name="assign-attribute-groups-to-retail-categories"></a><span data-ttu-id="0ff3b-256">将属性组分配到零售类别</span><span class="sxs-lookup"><span data-stu-id="0ff3b-256">Assign attribute groups to retail categories</span></span>

<span data-ttu-id="0ff3b-257">可将一个或多个属性组与以下类型的零售类别层次结构中的类别节点关联：零售产品层次结构、渠道导航类别层次结构和补充产品类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-257">One or more attribute groups can be associated with category nodes in the following types of retail category hierarchies: Retail product hierarchy, Channel navigation category hierarchy, and Supplemental product category hierarchy.</span></span> <span data-ttu-id="0ff3b-258">然后，为产品分类时，这些产品将继承属性组中包含的属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-258">Then, when products are categorized, they inherit the attributes that are included in the attribute groups.</span></span>

![零售产品层次结构 - 产品属性组](media/AGRetailProdHierarchy.PNG)

<span data-ttu-id="0ff3b-260">按照以下步骤将属性组分配给零售产品层次结构中的类别。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-260">Follow these steps to assign attribute groups to categories in the Retail product hierarchy.</span></span>

1. <span data-ttu-id="0ff3b-261">以零售促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-261">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="0ff3b-262">转至**零售** &gt; **类别和产品管理** &gt; **零售产品层次结构**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-262">Go to **Retail** &gt; **Category and product management** &gt; **Retail product hierarchy**.</span></span>
3. <span data-ttu-id="0ff3b-263">选择**时尚导航层次结构**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-263">Select **Fashion navigation hierarchy**.</span></span>
4. <span data-ttu-id="0ff3b-264">在**男装**下，选择**裤子**类别，然后在**产品属性组**快速选项卡中，添加一个名称为**男士皮带**的属性组。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-264">Under **Menswear**, select the **Pants** category, and then, on the **Product attribute groups** FastTab, add an attribute group that is named **Men's belt**.</span></span>
5. <span data-ttu-id="0ff3b-265">选择**时尚太阳镜**类别，然后通过选择**查看属性**验证**时尚太阳镜**属性组中的新属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-265">Select the **Fashion sunglasses** category, and verify the new attributes in the **Fashion Sunglasses** attribute group by selecting **View attributes**.</span></span>

    <span data-ttu-id="0ff3b-266">该属性组应显示新的**镜片形状**和**太阳镜品牌**属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-266">The attribute group should show the new **Lens shape** and **Sunglass brand** attributes.</span></span>

6. <span data-ttu-id="0ff3b-267">在**男装**下，选择**裤子**类别，然后通过选择**查看属性**验证**男士皮带**属性组的属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-267">Under **Menswear**, select the **Pants** category, and verify the attributes for the **Men's belt** attribute group by selecting **View attributes**.</span></span>

    <span data-ttu-id="0ff3b-268">该属性组应显示**男士皮带品牌**、**皮带材质**和**皮带尺寸**属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-268">The attribute group should show the **Men's belt brand**, **Belt fabric**, and **Belt size** attributes.</span></span>

> [!NOTE]
> <span data-ttu-id="0ff3b-269">此过程也可用于为渠道导航类别层次结构和补充产品类别层次结构中的列表分配属性组。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-269">This procedure can also be used to assign attribute groups to categories in the Channel navigation category hierarchy and the Supplemental product category hierarchy.</span></span> <span data-ttu-id="0ff3b-270">在步骤 2 中，请使用以下导航路径：</span><span class="sxs-lookup"><span data-stu-id="0ff3b-270">In step 2, use the following navigation paths:</span></span>
>
> - <span data-ttu-id="0ff3b-271">**零售** &gt; **类别和产品管理** &gt; **渠道导航类别**</span><span class="sxs-lookup"><span data-stu-id="0ff3b-271">**Retail** &gt; **Category and product management** &gt; **Channel navigation categories**</span></span>
> - <span data-ttu-id="0ff3b-272">**零售** &gt; **类别和产品管理** &gt; **补充产品类别**</span><span class="sxs-lookup"><span data-stu-id="0ff3b-272">**Retail** &gt; **Category and product management** &gt; **Supplemental product categories**</span></span>

### <a name="assign-attribute-groups-to-retail-stores"></a><span data-ttu-id="0ff3b-273">将属性组分配到零售商店</span><span class="sxs-lookup"><span data-stu-id="0ff3b-273">Assign attribute groups to retail stores</span></span>

<span data-ttu-id="0ff3b-274">一个或多个属性组可与零售商店层次结构中的一个或多个零售商店关联。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-274">One or more attribute groups can be associated with one or more retail stores in the retail store hierarchy.</span></span> <span data-ttu-id="0ff3b-275">然后，为特定零售商店丰富产品后，这些产品将继承属性组中包含的属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-275">Then, when products are enriched for specific retail stores, they inherit the attributes that are included in the attribute groups.</span></span>

1. <span data-ttu-id="0ff3b-276">以零售促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-276">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="0ff3b-277">转至**零售** &gt; **渠道设置** &gt; **渠道类别和产品属性**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-277">Go to **Retail** &gt; **Channel setup** &gt; **Channel categories and product attributes**.</span></span>
3. <span data-ttu-id="0ff3b-278">为休斯顿渠道分配属性组：</span><span class="sxs-lookup"><span data-stu-id="0ff3b-278">Assign attribute groups to the Houston channel:</span></span>

    1. <span data-ttu-id="0ff3b-279">选择**休斯顿**渠道。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-279">Select the **Houston** channel.</span></span>
    2. <span data-ttu-id="0ff3b-280">在**属性组**快速选项卡中，选择**添加**，然后在**名称**字段中，选择 **SharePointProvisionedProductAttributeGroup**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-280">On the **Attribute group** FastTab, select **Add**, and then, in the **Name** field, select **SharePointProvisionedProductAttributeGroup**.</span></span>
    3. <span data-ttu-id="0ff3b-281">再次选择**添加**，然后在**名称**字段中选择**男士皮带**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-281">Select **Add** again, and then, in the **Name** field, select **Men's belt**.</span></span>
    4. <span data-ttu-id="0ff3b-282">再次选择**添加**，然后在**名称**字段中选择**时尚太阳镜**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-282">Select **Add** again, and then, in the **Name** field, select **Fashion Sunglasses**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0ff3b-283">可通过一个选项指定该渠道应继承其在层次结构中的父渠道的属性组。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-283">An option lets you specify that this channel should inherit the attribute groups from its parent channel in the hierarchy.</span></span> <span data-ttu-id="0ff3b-284">如果将**继承**选项设置为**是**，子渠道将继承其所有属性组和这些属性组中的所有属性。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-284">If you set the **Inherit** option to **Yes**, the child channel node inherits all the attribute groups and all the attributes in those attribute groups.</span></span>

4. <span data-ttu-id="0ff3b-285">请启用这些属性，以便其在休斯顿渠道中可用：</span><span class="sxs-lookup"><span data-stu-id="0ff3b-285">Enable the attributes so that they are available in the Houston channel:</span></span>

    1. <span data-ttu-id="0ff3b-286">在操作窗格上，选择**设置属性元数据**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-286">On the Action Pane, select **Set attribute metadata**.</span></span>
    2. <span data-ttu-id="0ff3b-287">选择**时尚**类别节点，然后在**渠道产品属性**快速选项卡上，为每个属性选择**包括属性**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-287">Select the **Fashion** category node, and then, on the **Channel product attributes** FastTab, select **Include attribute** for each attribute.</span></span>
    3. <span data-ttu-id="0ff3b-288">选择**时尚配件**类别节点，选择**时尚太阳镜**类别，然后在**渠道产品属性**快速选项卡上，为每个属性选择**包括属性**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-288">Select the **Fashion Accessories** category node, select the **Fashion Sunglasses** category, and then, on the **Channel product attributes** FastTab, select **Include attribute** for each attribute.</span></span>
    4. <span data-ttu-id="0ff3b-289">选择**安装**类别节点，选择**裤子**类别，然后在**渠道产品属性**快速选项卡上，为每个属性选择**包括属性**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-289">Select the **Menswear** category node, select the **Pants** category, and then, on the **Channel product attributes** FastTab, select **Include attribute** for each attribute.</span></span>

![渠道类别和产品属性 - 属性组](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a><span data-ttu-id="0ff3b-291">覆盖属性值</span><span class="sxs-lookup"><span data-stu-id="0ff3b-291">Overriding attribute values</span></span>

<span data-ttu-id="0ff3b-292">单个产品的默认属性值可在产品级别覆盖。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-292">The default values of attributes can be overridden for individual products at the product level.</span></span> <span data-ttu-id="0ff3b-293">也可以覆盖针对特定零售渠道的特定目录中的单个产品的默认值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-293">Default values can also be overridden for individual products in specific catalogs that are targeted at specific retail channels.</span></span>

### <a name="override-the-attribute-values-of-an-individual-product"></a><span data-ttu-id="0ff3b-294">覆盖单个产品的属性值</span><span class="sxs-lookup"><span data-stu-id="0ff3b-294">Override the attribute values of an individual product</span></span>

1. <span data-ttu-id="0ff3b-295">以零售促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-295">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="0ff3b-296">转至**零售** &gt; **类别和产品管理** &gt; **已发布的产品(按类别)**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-296">Go to **Retail** &gt; **Category and product management** &gt; **Released products by category**.</span></span>
3. <span data-ttu-id="0ff3b-297">选择**时尚** &gt; **时尚配件** &gt; **时尚太阳镜**类别节点。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-297">Select the **Fashion** &gt; **Fashion Accessories** &gt; **Fashion Sunglasses** category node.</span></span>
4. <span data-ttu-id="0ff3b-298">在网格中选择所需产品。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-298">Select the required product in the grid.</span></span> <span data-ttu-id="0ff3b-299">然后，在操作窗格中**产品**选项卡上的**设置**组中，选择**产品属性**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-299">Then, on the Action Pane, on the **Product** tab, in the **Set up** group, select **Product attributes**.</span></span>
5. <span data-ttu-id="0ff3b-300">在左窗格中选择一个属性，然后在右窗格中更新其值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-300">Select an attribute in the left pane, and then update its value in the right pane.</span></span>

![产品详细信息页面 - 产品属性组](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a><span data-ttu-id="0ff3b-302">覆盖目录中的产品的属性值</span><span class="sxs-lookup"><span data-stu-id="0ff3b-302">Override the attribute values of products in a catalog</span></span>

1. <span data-ttu-id="0ff3b-303">以零售促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-303">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="0ff3b-304">转至**零售** &gt; **目录管理** &gt; **所有目录**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-304">Go to **Retail** &gt; **Catalog management** &gt; **All catalogs**.</span></span>
3. <span data-ttu-id="0ff3b-305">选择 **Fabrikam Base Catalog** 目录。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-305">Select the **Fabrikam Base Catalog** catalog.</span></span>
4. <span data-ttu-id="0ff3b-306">选择**时尚** &gt; **时尚配件** &gt; **时尚太阳镜**类别节点。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-306">Select the **Fashion** &gt; **Fashion Accessories** &gt; **Fashion Sunglasses** category node.</span></span>
5. <span data-ttu-id="0ff3b-307">在**产品**快速选项卡中，选择所需产品，然后选择产品网格上方的**属性**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-307">On the **Products** FastTab, select the required product, and then select **Attributes** above the product grid.</span></span>
6. <span data-ttu-id="0ff3b-308">在以下快速选项卡上，更新所需属性的值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-308">On the following FastTabs, update the values of the required attributes:</span></span>

   - <span data-ttu-id="0ff3b-309">共享的产品媒体</span><span class="sxs-lookup"><span data-stu-id="0ff3b-309">Shared product media</span></span>
   - <span data-ttu-id="0ff3b-310">共享产品属性</span><span class="sxs-lookup"><span data-stu-id="0ff3b-310">Shared product attributes</span></span>
   - <span data-ttu-id="0ff3b-311">通道媒体</span><span class="sxs-lookup"><span data-stu-id="0ff3b-311">Channel media</span></span>
   - <span data-ttu-id="0ff3b-312">渠道产品属性</span><span class="sxs-lookup"><span data-stu-id="0ff3b-312">Channel product attributes</span></span>

     > [!NOTE]
     > <span data-ttu-id="0ff3b-313">如果在 Finance and Operations 中创建共享产品介质和共享产品属性，它们将应用于所有零售产品。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-313">If shared product media and shared product attributes are created in Finance and Operations, they apply to all the retail products.</span></span>

![目录产品属性组](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a><span data-ttu-id="0ff3b-315">覆盖渠道中的产品的属性值</span><span class="sxs-lookup"><span data-stu-id="0ff3b-315">Override the attribute values of products in a channel</span></span>

1. <span data-ttu-id="0ff3b-316">以零售促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-316">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="0ff3b-317">转至**零售** &gt; **渠道设置** &gt; **渠道类别和产品属性**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-317">Go to **Retail** &gt; **Channel setup** &gt; **Channel categories and product attributes**.</span></span>
3. <span data-ttu-id="0ff3b-318">选择**休斯顿**渠道。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-318">Select the **Houston** channel.</span></span>
4. <span data-ttu-id="0ff3b-319">在**产品**快速选项卡中，选择所需产品，然后选择产品网格上方的**属性**。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-319">On the **Products** FastTab, select the required product, and then select **Attributes** above the product grid.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ff3b-320">如果无可用产品，请添加产品，方法是在**产品**快速选项卡上选择**添加**，然后在**添加产品**对话框中选择所需产品。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-320">If no products are available, add products by selecting **Add** on the **Products** FastTab and then selecting the required products in the **Add products** dialog box.</span></span>

5. <span data-ttu-id="0ff3b-321">在以下快速选项卡上，更新所需属性的值。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-321">On the following FastTabs, update the values of the required attributes:</span></span>

   - <span data-ttu-id="0ff3b-322">共享的产品媒体</span><span class="sxs-lookup"><span data-stu-id="0ff3b-322">Shared product media</span></span>
   - <span data-ttu-id="0ff3b-323">共享产品属性</span><span class="sxs-lookup"><span data-stu-id="0ff3b-323">Shared product attributes</span></span>
   - <span data-ttu-id="0ff3b-324">通道媒体</span><span class="sxs-lookup"><span data-stu-id="0ff3b-324">Channel media</span></span>
   - <span data-ttu-id="0ff3b-325">渠道产品属性</span><span class="sxs-lookup"><span data-stu-id="0ff3b-325">Channel product attributes</span></span>

     > [!NOTE]
     > <span data-ttu-id="0ff3b-326">如果在 Finance and Operations 中创建共享产品介质和共享产品属性，它们将应用于所有零售产品。</span><span class="sxs-lookup"><span data-stu-id="0ff3b-326">If shared product media and shared product attributes are created in Finance and Operations, they apply to all the retail products.</span></span>

