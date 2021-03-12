---
title: 管理属性和属性组
description: 此主题介绍如何使用属性通过用户定义的字段介绍产品及其特征。
author: ashishmsft
manager: AnnBe
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategoryAttribute, EcoResProductEntityAttributeTableFieldAssociation, EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResAttributeType, EcoResAttributeValue, EcoResCategoryAttributeGroup, EcoResCategoryFriendlyName
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: 70e2b52dd140660fe98c6ff07248a033ba4bd635
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979965"
---
# <a name="manage-attributes-and-attribute-groups"></a><span data-ttu-id="865d1-103">管理属性和属性组</span><span class="sxs-lookup"><span data-stu-id="865d1-103">Manage attributes and attribute groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="865d1-104">可通过 *属性* 和用户定义的字段（**如内存大小**、**硬盘容量**、**符合能源之星的要求** 等）进一步描述产品及其特征。</span><span class="sxs-lookup"><span data-stu-id="865d1-104">*Attributes* provide a way to further describe a product and its characteristics through user-defined fields (such as **Memory size**, **Hard disk capacity**, **Is Energy star compliant**, and so on).</span></span> <span data-ttu-id="865d1-105">可以将属性与各种 Commerce 实体（如产品类别和通道）关联，并且可以为属性设置默认值。</span><span class="sxs-lookup"><span data-stu-id="865d1-105">Attributes can be associated with various Commerce entities, such as product categories and channels, and default values can be set for them.</span></span> <span data-ttu-id="865d1-106">当产品与产品类别或渠道关联时，产品将继承属性及默认值。</span><span class="sxs-lookup"><span data-stu-id="865d1-106">Products then inherit the attributes and the default values when they are associated with the product categories or channels.</span></span> <span data-ttu-id="865d1-107">默认值可在单个产品级别、在渠道级别或在目录中被覆盖。</span><span class="sxs-lookup"><span data-stu-id="865d1-107">The default values can be overridden at the individual product level, at the channel level, or in a catalog.</span></span>


<span data-ttu-id="865d1-108">例如，电视机产品通常具有以下属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-108">For example, a typical television product might have the following attributes.</span></span>

| <span data-ttu-id="865d1-109">类别</span><span class="sxs-lookup"><span data-stu-id="865d1-109">Category</span></span>   | <span data-ttu-id="865d1-110">属性</span><span class="sxs-lookup"><span data-stu-id="865d1-110">Attribute</span></span>                | <span data-ttu-id="865d1-111">允许的值</span><span class="sxs-lookup"><span data-stu-id="865d1-111">Permissible values</span></span>          | <span data-ttu-id="865d1-112">默认值</span><span class="sxs-lookup"><span data-stu-id="865d1-112">Default value</span></span> |
|------------|--------------------------|-----------------------------|---------------|
| <span data-ttu-id="865d1-113">电视和视频</span><span class="sxs-lookup"><span data-stu-id="865d1-113">TV & Video</span></span> | <span data-ttu-id="865d1-114">品牌</span><span class="sxs-lookup"><span data-stu-id="865d1-114">Brand</span></span>                    | <span data-ttu-id="865d1-115">任何有效的品牌值</span><span class="sxs-lookup"><span data-stu-id="865d1-115">Any valid brand value</span></span>       | <span data-ttu-id="865d1-116">None</span><span class="sxs-lookup"><span data-stu-id="865d1-116">None</span></span>          |
| <span data-ttu-id="865d1-117">电视</span><span class="sxs-lookup"><span data-stu-id="865d1-117">TV</span></span>         | <span data-ttu-id="865d1-118">屏幕尺寸</span><span class="sxs-lookup"><span data-stu-id="865d1-118">Screen Size</span></span>              | <span data-ttu-id="865d1-119">20–80 英寸</span><span class="sxs-lookup"><span data-stu-id="865d1-119">20–80 inches</span></span>                | <span data-ttu-id="865d1-120">None</span><span class="sxs-lookup"><span data-stu-id="865d1-120">None</span></span>          |
|            | <span data-ttu-id="865d1-121">垂直行业解决方案</span><span class="sxs-lookup"><span data-stu-id="865d1-121">Vertical Resolution</span></span>      | <span data-ttu-id="865d1-122">480i、720p、1080i 或 1080p</span><span class="sxs-lookup"><span data-stu-id="865d1-122">480i, 720p, 1080i, or 1080p</span></span> | <span data-ttu-id="865d1-123">1080p</span><span class="sxs-lookup"><span data-stu-id="865d1-123">1080p</span></span>         |
|            | <span data-ttu-id="865d1-124">屏幕刷新率</span><span class="sxs-lookup"><span data-stu-id="865d1-124">Screen Refresh Rate</span></span>      | <span data-ttu-id="865d1-125">60hz、120hz 或 240hz</span><span class="sxs-lookup"><span data-stu-id="865d1-125">60hz, 120hz, or 240hz</span></span>       | <span data-ttu-id="865d1-126">60hz</span><span class="sxs-lookup"><span data-stu-id="865d1-126">60hz</span></span>          |
|            | <span data-ttu-id="865d1-127">HDMI 输入</span><span class="sxs-lookup"><span data-stu-id="865d1-127">HDMI Inputs</span></span>              | <span data-ttu-id="865d1-128">0–10</span><span class="sxs-lookup"><span data-stu-id="865d1-128">0–10</span></span>                        | <span data-ttu-id="865d1-129">3</span><span class="sxs-lookup"><span data-stu-id="865d1-129">3</span></span>             |
|            | <span data-ttu-id="865d1-130">DVI 输入</span><span class="sxs-lookup"><span data-stu-id="865d1-130">DVI Inputs</span></span>               | <span data-ttu-id="865d1-131">0–10</span><span class="sxs-lookup"><span data-stu-id="865d1-131">0–10</span></span>                        | <span data-ttu-id="865d1-132">1</span><span class="sxs-lookup"><span data-stu-id="865d1-132">1</span></span>             |
|            | <span data-ttu-id="865d1-133">复合输入</span><span class="sxs-lookup"><span data-stu-id="865d1-133">Composite Inputs</span></span>         | <span data-ttu-id="865d1-134">0–10</span><span class="sxs-lookup"><span data-stu-id="865d1-134">0–10</span></span>                        | <span data-ttu-id="865d1-135">2</span><span class="sxs-lookup"><span data-stu-id="865d1-135">2</span></span>             |
|            | <span data-ttu-id="865d1-136">组件输入</span><span class="sxs-lookup"><span data-stu-id="865d1-136">Component Inputs</span></span>         | <span data-ttu-id="865d1-137">0–10</span><span class="sxs-lookup"><span data-stu-id="865d1-137">0–10</span></span>                        | <span data-ttu-id="865d1-138">1</span><span class="sxs-lookup"><span data-stu-id="865d1-138">1</span></span>             |
| <span data-ttu-id="865d1-139">LCD</span><span class="sxs-lookup"><span data-stu-id="865d1-139">LCD</span></span>        | <span data-ttu-id="865d1-140">3D 已就绪</span><span class="sxs-lookup"><span data-stu-id="865d1-140">3D Ready</span></span>                 | <span data-ttu-id="865d1-141">是或否</span><span class="sxs-lookup"><span data-stu-id="865d1-141">Yes or No</span></span>                   | <span data-ttu-id="865d1-142">是</span><span class="sxs-lookup"><span data-stu-id="865d1-142">Yes</span></span>           |
|            | <span data-ttu-id="865d1-143">3D 已启用</span><span class="sxs-lookup"><span data-stu-id="865d1-143">3D Enabled</span></span>               | <span data-ttu-id="865d1-144">是或否</span><span class="sxs-lookup"><span data-stu-id="865d1-144">Yes or No</span></span>                   | <span data-ttu-id="865d1-145">无</span><span class="sxs-lookup"><span data-stu-id="865d1-145">No</span></span>            |
| <span data-ttu-id="865d1-146">等离子</span><span class="sxs-lookup"><span data-stu-id="865d1-146">Plasma</span></span>     | <span data-ttu-id="865d1-147">最低工作温度</span><span class="sxs-lookup"><span data-stu-id="865d1-147">Operating Temp From</span></span>      | <span data-ttu-id="865d1-148">32–110 度</span><span class="sxs-lookup"><span data-stu-id="865d1-148">32–110 degrees</span></span>              | <span data-ttu-id="865d1-149">32</span><span class="sxs-lookup"><span data-stu-id="865d1-149">32</span></span>            |
|            | <span data-ttu-id="865d1-150">最高工作温度</span><span class="sxs-lookup"><span data-stu-id="865d1-150">Operating Temp To</span></span>        | <span data-ttu-id="865d1-151">32–110 度</span><span class="sxs-lookup"><span data-stu-id="865d1-151">32–110 degrees</span></span>              | <span data-ttu-id="865d1-152">100</span><span class="sxs-lookup"><span data-stu-id="865d1-152">100</span></span>           |
| <span data-ttu-id="865d1-153">投影</span><span class="sxs-lookup"><span data-stu-id="865d1-153">Projection</span></span> | <span data-ttu-id="865d1-154">投影管保修</span><span class="sxs-lookup"><span data-stu-id="865d1-154">Projection Tube Warranty</span></span> | <span data-ttu-id="865d1-155">6、12 或 18 个月</span><span class="sxs-lookup"><span data-stu-id="865d1-155">6, 12, or 18 months</span></span>         | <span data-ttu-id="865d1-156">12</span><span class="sxs-lookup"><span data-stu-id="865d1-156">12</span></span>            |
|            | <span data-ttu-id="865d1-157">投影管 \#</span><span class="sxs-lookup"><span data-stu-id="865d1-157">\# of Projection Tubes</span></span>   | <span data-ttu-id="865d1-158">1–5</span><span class="sxs-lookup"><span data-stu-id="865d1-158">1–5</span></span>                         | <span data-ttu-id="865d1-159">3</span><span class="sxs-lookup"><span data-stu-id="865d1-159">3</span></span>             |

## <a name="attributes-and-attribute-types"></a><span data-ttu-id="865d1-160">属性和属性类型</span><span class="sxs-lookup"><span data-stu-id="865d1-160">Attributes and attribute types</span></span>

<span data-ttu-id="865d1-161">属性基于 *属性类型*。</span><span class="sxs-lookup"><span data-stu-id="865d1-161">Attributes are based on *attribute types*.</span></span> <span data-ttu-id="865d1-162">特性类型标识可为特定于特性输入数据的类型。</span><span class="sxs-lookup"><span data-stu-id="865d1-162">The attribute type identifies the type of data that can be entered for a specific attribute.</span></span> <span data-ttu-id="865d1-163">支持以下属性类型：</span><span class="sxs-lookup"><span data-stu-id="865d1-163">The following attribute types are supported:</span></span>

- <span data-ttu-id="865d1-164">**货币** - 此类型支持货币值。</span><span class="sxs-lookup"><span data-stu-id="865d1-164">**Currency** – This type supports a currency value.</span></span> <span data-ttu-id="865d1-165">它可以受约束（即，它可以支持某个值范围），也可以保持开放。</span><span class="sxs-lookup"><span data-stu-id="865d1-165">It can be bounded (that is, it can support a range of values), or it can be left open.</span></span>
- <span data-ttu-id="865d1-166">**日期时间** - 此类型支持日期和时间值。</span><span class="sxs-lookup"><span data-stu-id="865d1-166">**DateTime** – This type supports a date and time value.</span></span> <span data-ttu-id="865d1-167">它可以有范围，也可以保持开放。</span><span class="sxs-lookup"><span data-stu-id="865d1-167">It can be bounded or left open.</span></span>
- <span data-ttu-id="865d1-168">**小数** - 此类型支持包括小数位的数字值。</span><span class="sxs-lookup"><span data-stu-id="865d1-168">**Decimal** – This type supports a numerical value that includes decimal places.</span></span> <span data-ttu-id="865d1-169">它还支持度量单位。</span><span class="sxs-lookup"><span data-stu-id="865d1-169">It also supports a unit of measure.</span></span> <span data-ttu-id="865d1-170">它可以有范围，也可以保持开放。</span><span class="sxs-lookup"><span data-stu-id="865d1-170">It can be bounded or left open.</span></span>
- <span data-ttu-id="865d1-171">**整数** - 此类型支持数字值。</span><span class="sxs-lookup"><span data-stu-id="865d1-171">**Integer** – This type supports a numerical value.</span></span> <span data-ttu-id="865d1-172">它还支持度量单位。</span><span class="sxs-lookup"><span data-stu-id="865d1-172">It also supports a unit of measure.</span></span> <span data-ttu-id="865d1-173">它可以有范围，也可以保持开放。</span><span class="sxs-lookup"><span data-stu-id="865d1-173">It can be bounded or left open.</span></span>
- <span data-ttu-id="865d1-174">**文本** - 此类型支持文本值。</span><span class="sxs-lookup"><span data-stu-id="865d1-174">**Text** – This type supports a text value.</span></span> <span data-ttu-id="865d1-175">它还支持预定义的一组可能值（即 *枚举*）。</span><span class="sxs-lookup"><span data-stu-id="865d1-175">It also supports a predefined set of possible values (that is, an *enumeration*).</span></span>
- <span data-ttu-id="865d1-176">**布尔** - 此类型支持二进制值（**true** 或 **false**）。</span><span class="sxs-lookup"><span data-stu-id="865d1-176">**Boolean** – This type supports a binary value (**true** or **false**).</span></span>
- <span data-ttu-id="865d1-177">**引用** - 此类型引用其他属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-177">**Reference** – This type references other attributes.</span></span>

### <a name="set-up-attribute-types"></a><span data-ttu-id="865d1-178">设置属性类型</span><span class="sxs-lookup"><span data-stu-id="865d1-178">Set up attribute types</span></span>

1. <span data-ttu-id="865d1-179">以促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="865d1-179">Sign in to the back-office client as a merchandising manager.</span></span>
2. <span data-ttu-id="865d1-180">转到 **产品信息管理** &gt; **设置** &gt; **类别和属性** &gt; **属性类型**。</span><span class="sxs-lookup"><span data-stu-id="865d1-180">Go to **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attribute types**.</span></span>
3. <span data-ttu-id="865d1-181">创建 **文本** 类型的两个属性类型，将 **固定列表** 选项设置为 **是**，然后添加一列值：</span><span class="sxs-lookup"><span data-stu-id="865d1-181">Create two attribute types of the **Text** type, set the **Fixed list** option to **Yes**, and then add a list of values:</span></span>

    - <span data-ttu-id="865d1-182">将一个属性类型命名为 **镜片形状**，然后添加以下值：**椭圆形**、**方形** 和 **三角形**。</span><span class="sxs-lookup"><span data-stu-id="865d1-182">Name one attribute type **Lens shape**, and add the following values: **Oval**, **Square**, and **Rectangle**.</span></span>
    - <span data-ttu-id="865d1-183">将另一个属性类型命名为 **太阳镜品牌**，然后添加以下值：**Ray ban**、**Aviator** 和 **Oakley**。</span><span class="sxs-lookup"><span data-stu-id="865d1-183">Name the other attribute type **Sunglass brand**, and add the following values: **Ray ban**, **Aviator**, and **Oakley**.</span></span>

![属性类型](media/AttributeType.png)

### <a name="set-up-an-attribute"></a><span data-ttu-id="865d1-185">设置属性</span><span class="sxs-lookup"><span data-stu-id="865d1-185">Set up an attribute</span></span>

1. <span data-ttu-id="865d1-186">以促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="865d1-186">Sign in to the back-office client as a merchandising manager.</span></span>
2. <span data-ttu-id="865d1-187">转到 **产品信息管理** &gt; **设置** &gt; **类别和属性** &gt; **属性**。</span><span class="sxs-lookup"><span data-stu-id="865d1-187">Go to **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attributes**.</span></span>
3. <span data-ttu-id="865d1-188">创建名为 **镜片** 的属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-188">Create an attribute that is named **Lens**.</span></span>
4. <span data-ttu-id="865d1-189">将 **属性类型** 字段设置为 **镜片形状**。</span><span class="sxs-lookup"><span data-stu-id="865d1-189">Set the **Attribute type** field to **Lens shape**.</span></span>

![属性](media/Attribute.png)

## <a name="attribute-metadata"></a><span data-ttu-id="865d1-191">属性元数据</span><span class="sxs-lookup"><span data-stu-id="865d1-191">Attribute metadata</span></span>

<span data-ttu-id="865d1-192">*属性元数据* 用于选择选项来指定各产品的属性的行为。</span><span class="sxs-lookup"><span data-stu-id="865d1-192">*Attribute metadata* lets you select options to specify how the attributes for each product should behave.</span></span> <span data-ttu-id="865d1-193">例如，您可指定是否要求属性，它们是否可用于搜索，和他们是否可用作筛选器。</span><span class="sxs-lookup"><span data-stu-id="865d1-193">For example, you can specify whether attributes are required, whether they can be used for searches, and whether they can be used as a filter.</span></span>

<span data-ttu-id="865d1-194">对于产品，可在渠道级别覆盖属性元数据设置。</span><span class="sxs-lookup"><span data-stu-id="865d1-194">For products, the attribute metadata settings can be overridden at the channel level.</span></span> <span data-ttu-id="865d1-195">此主题后文将介绍此功能。</span><span class="sxs-lookup"><span data-stu-id="865d1-195">This capability will be discussed later in this topic.</span></span>

<span data-ttu-id="865d1-196">您可能已经注意到，**属性** 页中包含与属性元数据有关的选项。</span><span class="sxs-lookup"><span data-stu-id="865d1-196">As you might notice, the **Attributes** page includes options that are related to attribute metadata.</span></span> <span data-ttu-id="865d1-197">在 **POS 属性元数据** 下，一个名称为 **可细化** 的选项影响属性值在零售点 (POS) 中的行为或系统处理这些属性值的方式。</span><span class="sxs-lookup"><span data-stu-id="865d1-197">Under **Attribute metadata for POS**, one option that is named **Can be refined** affects the behavior of the attribute values in the point of sale (POS) or the way that the system handles those attribute values.</span></span> <span data-ttu-id="865d1-198">只有可将其 **可细化** 选项设置为 **是** 的属性才会显示以供细化或在 POS 中筛选产品。</span><span class="sxs-lookup"><span data-stu-id="865d1-198">Only attributes for which you may set the **Can be refined** option to **Yes**, will show up for refinement or filtering of products in the POS.</span></span>

<span data-ttu-id="865d1-199">下面是 **属性** 页中显示的其余属性元数据选项：</span><span class="sxs-lookup"><span data-stu-id="865d1-199">Here are the remaining attribute metadata options on the **Attributes** page:</span></span>

- <span data-ttu-id="865d1-200">可搜索</span><span class="sxs-lookup"><span data-stu-id="865d1-200">Searchable</span></span>
- <span data-ttu-id="865d1-201">可检索</span><span class="sxs-lookup"><span data-stu-id="865d1-201">Retrievable</span></span>
- <span data-ttu-id="865d1-202">可查询</span><span class="sxs-lookup"><span data-stu-id="865d1-202">Can be queried</span></span>
- <span data-ttu-id="865d1-203">可排序</span><span class="sxs-lookup"><span data-stu-id="865d1-203">Sortable</span></span>
- <span data-ttu-id="865d1-204">允许多个值</span><span class="sxs-lookup"><span data-stu-id="865d1-204">Allow multiple values</span></span>
- <span data-ttu-id="865d1-205">忽略大小写和格式</span><span class="sxs-lookup"><span data-stu-id="865d1-205">Ignore case and format</span></span>
- <span data-ttu-id="865d1-206">完成匹配</span><span class="sxs-lookup"><span data-stu-id="865d1-206">Complete match</span></span>

<span data-ttu-id="865d1-207">这些选项最初用于改进联机店面的搜索功能。</span><span class="sxs-lookup"><span data-stu-id="865d1-207">These options were originally intended to improve the search functionality for the online storefront.</span></span> <span data-ttu-id="865d1-208">尽管 Commerce 中不包含现成的联机店面，却的确包含电子商务发布软件开发包 (SDK)。</span><span class="sxs-lookup"><span data-stu-id="865d1-208">Although Commerce doesn't include the online storefront out of the box, it does include the eCommerce Publishing Software Development Kit (SDK).</span></span> <span data-ttu-id="865d1-209">客户可使用此 SDK 将产品放入所选搜索索引中。</span><span class="sxs-lookup"><span data-stu-id="865d1-209">Customers can use this SDK to put products into a search index of their choice.</span></span> <span data-ttu-id="865d1-210">尽管导入了产品数据，客户仍然应该可以区分可搜索数据、可查询的数据等。</span><span class="sxs-lookup"><span data-stu-id="865d1-210">Although the product data is imported, customers should still be able to distinguish searchable data, data that can be queried, and so on.</span></span> <span data-ttu-id="865d1-211">这样他们就可以构建最佳索引以确保仅为 *他们认为* 应该建立索引的属性建立索引。</span><span class="sxs-lookup"><span data-stu-id="865d1-211">In that way, they can build an optimal index to make sure that they index only attributes that, *in their opinion*, should be indexed.</span></span>

<span data-ttu-id="865d1-212">有关其余这些选项的用途信息，请参阅 [SharePoint Server 2013 中的搜索架构概述](https://technet.microsoft.com/library/jj219669.aspx)。</span><span class="sxs-lookup"><span data-stu-id="865d1-212">For information about the purpose of these remaining options, see [Overview of the search schema in SharePoint Server 2013](https://technet.microsoft.com/library/jj219669.aspx).</span></span>

## <a name="filter-settings-for-attributes"></a><span data-ttu-id="865d1-213">属性的筛选设置</span><span class="sxs-lookup"><span data-stu-id="865d1-213">Filter settings for attributes</span></span>

<span data-ttu-id="865d1-214">可通过属性的筛选器设置定义属性的筛选器如何在 POS 中显示。</span><span class="sxs-lookup"><span data-stu-id="865d1-214">Filter settings for attributes let you define how the filters for attributes are shown in the POS.</span></span> <span data-ttu-id="865d1-215">若要访问属性的筛选器设置，请在的 **属性** 页面上选择属性，然后在操作窗格中选择 **筛选器设置**。</span><span class="sxs-lookup"><span data-stu-id="865d1-215">To access the filter settings for an attribute, on the **Attributes** page, select the attribute, and then, on the Action Pane, select **Filter settings**.</span></span>

<span data-ttu-id="865d1-216">**筛选器显示首选项** 页面中包含以下字段：</span><span class="sxs-lookup"><span data-stu-id="865d1-216">The **Filter display preferences** page includes the following fields:</span></span>

- <span data-ttu-id="865d1-217">**名称** - 默认情况下，此字段设置为属性的名称。</span><span class="sxs-lookup"><span data-stu-id="865d1-217">**Name** – By default, this field is set to the name of the attribute.</span></span> <span data-ttu-id="865d1-218">然而，您可以更改值。</span><span class="sxs-lookup"><span data-stu-id="865d1-218">However, you can change the value.</span></span>
- <span data-ttu-id="865d1-219">**显示选项** - 以下选项可用：</span><span class="sxs-lookup"><span data-stu-id="865d1-219">**Display option** – The following options are available:</span></span>

    - <span data-ttu-id="865d1-220">**单一值** - 此选项可用于以下属性类型：**布尔**、**货币**、**小数**、**整数** 和 **文本**。</span><span class="sxs-lookup"><span data-stu-id="865d1-220">**Single value** – This option is available for the following attribute types: **Boolean**, **Currency**, **Decimal**, **Integer**, and **Text**.</span></span> <span data-ttu-id="865d1-221">此选项支持在客户端中为这些属性选择单个值来进行细化。</span><span class="sxs-lookup"><span data-stu-id="865d1-221">This option enables single value selection for these attributes in the client for refinement.</span></span>
    - <span data-ttu-id="865d1-222">**多个值** - 此选项可用于以下属性类型：**货币**、**小数**、**整数** 和 **文本**。</span><span class="sxs-lookup"><span data-stu-id="865d1-222">**Multi value** – This option is available for the following attribute types: **Currency**, **Decimal**, **Integer**, and **Text**.</span></span> <span data-ttu-id="865d1-223">此选项支持在客户端中为该属性选择多个值来进行细化。</span><span class="sxs-lookup"><span data-stu-id="865d1-223">This option enables multi-value selection for this attribute in the client for refinement.</span></span>

- <span data-ttu-id="865d1-224">**显示控制** - 以下选项可用：</span><span class="sxs-lookup"><span data-stu-id="865d1-224">**Display control** – The following options are available:</span></span>

    - <span data-ttu-id="865d1-225">**列表** - 此选项可用于所有属性类型。</span><span class="sxs-lookup"><span data-stu-id="865d1-225">**List** – This option is available for the all attribute types.</span></span>
    - <span data-ttu-id="865d1-226">**范围** - 此选项可用于以下属性类型：**货币**、**小数** 和 **整数**。</span><span class="sxs-lookup"><span data-stu-id="865d1-226">**Range** – This option is available for the following attribute types: **Currency**, **Decimal**, and **Integer**.</span></span>
    - <span data-ttu-id="865d1-227">**滑块** - 此选项可用于以下属性类型：**货币**、**小数** 和 **整数**。</span><span class="sxs-lookup"><span data-stu-id="865d1-227">**Slider** – This option is available for the following attribute types: **Currency**, **Decimal**, and **Integer**.</span></span>
    - <span data-ttu-id="865d1-228">**带有滑块的滚动条** - 此选项可用于以下属性类型：**货币**、**小数** 和 **整数**。</span><span class="sxs-lookup"><span data-stu-id="865d1-228">**Slider with bars** – This option is available for the following attribute types: **Currency**, **Decimal**, and **Integer**.</span></span>

- <span data-ttu-id="865d1-229">**阈值** - 如果选择了 **范围** 作为显示控制类型，则需要此设置。</span><span class="sxs-lookup"><span data-stu-id="865d1-229">**Threshold value** – This setting is required if you selected **Range** as the display control type.</span></span> <span data-ttu-id="865d1-230">可将分号 (;) 用作分隔符来定义值。</span><span class="sxs-lookup"><span data-stu-id="865d1-230">You can define values by using a semicolon (;) as a delimiter.</span></span>

    <span data-ttu-id="865d1-231">例如，对于 **包容量** 这样的筛选器，阈值可以为 **10; 20; 50; 100; 200; 500; 1000; 5000**。</span><span class="sxs-lookup"><span data-stu-id="865d1-231">For example, for the filter like **Bag Volume**, a threshold value can be **10; 20; 50; 100; 200; 500; 1000; 5000**.</span></span> <span data-ttu-id="865d1-232">在此情况下，POS 将显示以下范围。</span><span class="sxs-lookup"><span data-stu-id="865d1-232">In this case, the POS will show the following ranges.</span></span> <span data-ttu-id="865d1-233">所有在结果集中无任何产品的范围都将灰显。</span><span class="sxs-lookup"><span data-stu-id="865d1-233">Any ranges that don't have any products in the result set will appear dimmed.</span></span>

    - <span data-ttu-id="865d1-234">小于 10</span><span class="sxs-lookup"><span data-stu-id="865d1-234">Less than 10</span></span>
    - <span data-ttu-id="865d1-235">10 - 20</span><span class="sxs-lookup"><span data-stu-id="865d1-235">10 – 20</span></span>
    - <span data-ttu-id="865d1-236">20 - 50</span><span class="sxs-lookup"><span data-stu-id="865d1-236">20 – 50</span></span>
    - <span data-ttu-id="865d1-237">50 - 100</span><span class="sxs-lookup"><span data-stu-id="865d1-237">50 – 100</span></span>
    - <span data-ttu-id="865d1-238">100 - 200</span><span class="sxs-lookup"><span data-stu-id="865d1-238">100 – 200</span></span>
    - <span data-ttu-id="865d1-239">200 - 500</span><span class="sxs-lookup"><span data-stu-id="865d1-239">200 – 500</span></span>
    - <span data-ttu-id="865d1-240">500 次或更多</span><span class="sxs-lookup"><span data-stu-id="865d1-240">500 or more</span></span>

![属性筛选器设置](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a><span data-ttu-id="865d1-242">属性组</span><span class="sxs-lookup"><span data-stu-id="865d1-242">Attribute groups</span></span>

<span data-ttu-id="865d1-243">定义属性之后，可将其分配给属性组。</span><span class="sxs-lookup"><span data-stu-id="865d1-243">After attributes have been defined, they can be assigned to attribute groups.</span></span> <span data-ttu-id="865d1-244">*属性组* 用于对产品中的一个组件或子组件的单个属性进行分组。</span><span class="sxs-lookup"><span data-stu-id="865d1-244">An *attribute group* is used to group the individual attributes for a component or subcomponent in a product configuration model.</span></span> <span data-ttu-id="865d1-245">一个属性可以包含在多个属性组中。</span><span class="sxs-lookup"><span data-stu-id="865d1-245">An attribute can be included in more than one attribute group.</span></span> <span data-ttu-id="865d1-246">属性组可帮助用户配置产品，因为可将多种选择安排到特定上下文中。</span><span class="sxs-lookup"><span data-stu-id="865d1-246">Attribute groups can help users configure products, because the various selections are arranged in a specific context.</span></span> <span data-ttu-id="865d1-247">可将属性组分配给类别或渠道。</span><span class="sxs-lookup"><span data-stu-id="865d1-247">Attribute groups can be assigned to categories or channels.</span></span>

<span data-ttu-id="865d1-248">您还可以为属性组中包含的属性设置默认值。</span><span class="sxs-lookup"><span data-stu-id="865d1-248">You can also set default values for attributes that are included in an attribute group.</span></span> <span data-ttu-id="865d1-249">例如，向属性组添加颜色属性，然后选择 **蓝色** 作为默认属性值。</span><span class="sxs-lookup"><span data-stu-id="865d1-249">For example, you add an attribute for color to an attribute group and select **Blue** as the default attribute value.</span></span> <span data-ttu-id="865d1-250">在此情况下，向产品添加包含颜色为其属性之一的属性组时，**蓝色** 将显示为该产品的默认颜色。</span><span class="sxs-lookup"><span data-stu-id="865d1-250">In this case, when the attribute group is added to a product that includes color as one of its attributes, **Blue** appears as the default color for that product.</span></span>

![属性组](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a><span data-ttu-id="865d1-252">创建属性组</span><span class="sxs-lookup"><span data-stu-id="865d1-252">Create an attribute group</span></span>

1. <span data-ttu-id="865d1-253">以促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="865d1-253">Sign in to the back-office client as a merchandising manager.</span></span>
2. <span data-ttu-id="865d1-254">转到 **产品信息管理** &gt; **设置** &gt; **类别和属性** &gt; **属性组**。</span><span class="sxs-lookup"><span data-stu-id="865d1-254">Go to **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attribute groups**.</span></span>
3. <span data-ttu-id="865d1-255">创建一个名称为 **时尚太阳镜** 的属性组。</span><span class="sxs-lookup"><span data-stu-id="865d1-255">Create an attribute group that is named **Fashion Sunglasses**.</span></span>
4. <span data-ttu-id="865d1-256">添加以下属性：**镜片形状** 和 **太阳镜品牌**。</span><span class="sxs-lookup"><span data-stu-id="865d1-256">Add the following attributes: **Lens shape** and **Sunglass brand**.</span></span>

### <a name="assign-attribute-groups-to-categories"></a><span data-ttu-id="865d1-257">将属性组分配到类别</span><span class="sxs-lookup"><span data-stu-id="865d1-257">Assign attribute groups to categories</span></span>

<span data-ttu-id="865d1-258">可将一个或多个属性组与以下类型的类别层次结构中的类别节点关联：Commerce 产品层次结构、渠道导航类别层次结构和补充产品类别层次结构。</span><span class="sxs-lookup"><span data-stu-id="865d1-258">One or more attribute groups can be associated with category nodes in the following types of category hierarchies: Commerce product hierarchy, Channel navigation category hierarchy, and Supplemental product category hierarchy.</span></span> <span data-ttu-id="865d1-259">然后，为产品分类时，这些产品将继承属性组中包含的属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-259">Then, when products are categorized, they inherit the attributes that are included in the attribute groups.</span></span>

![产品层次结构 - 产品属性组](media/AGRetailProdHierarchy.PNG)

<span data-ttu-id="865d1-261">按照以下步骤将属性组分配给 Commerce 产品层次结构中的类别。</span><span class="sxs-lookup"><span data-stu-id="865d1-261">Follow these steps to assign attribute groups to categories in the Commerce product hierarchy.</span></span>

1. <span data-ttu-id="865d1-262">以促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="865d1-262">Sign in to the back-office client as a merchandising manager.</span></span>
2. <span data-ttu-id="865d1-263">转至 **Retail 和 Commerce** &gt; **类别和产品管理** &gt; **Commerce 产品层次结构**。</span><span class="sxs-lookup"><span data-stu-id="865d1-263">Go to **Retail and Commerce** &gt; **Category and product management** &gt; **Commerce product hierarchy**.</span></span>
3. <span data-ttu-id="865d1-264">选择 **时尚导航层次结构**。</span><span class="sxs-lookup"><span data-stu-id="865d1-264">Select **Fashion navigation hierarchy**.</span></span>
4. <span data-ttu-id="865d1-265">在 **男装** 下，选择 **裤子** 类别，然后在 **产品属性组** 快速选项卡中，添加一个名称为 **男士皮带** 的属性组。</span><span class="sxs-lookup"><span data-stu-id="865d1-265">Under **Menswear**, select the **Pants** category, and then, on the **Product attribute groups** FastTab, add an attribute group that is named **Men's belt**.</span></span>
5. <span data-ttu-id="865d1-266">选择 **时尚太阳镜** 类别，然后通过选择 **查看属性** 验证 **时尚太阳镜** 属性组中的新属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-266">Select the **Fashion sunglasses** category, and verify the new attributes in the **Fashion Sunglasses** attribute group by selecting **View attributes**.</span></span>

    <span data-ttu-id="865d1-267">该属性组应显示新的 **镜片形状** 和 **太阳镜品牌** 属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-267">The attribute group should show the new **Lens shape** and **Sunglass brand** attributes.</span></span>

6. <span data-ttu-id="865d1-268">在 **男装** 下，选择 **裤子** 类别，然后通过选择 **查看属性** 验证 **男士皮带** 属性组的属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-268">Under **Menswear**, select the **Pants** category, and verify the attributes for the **Men's belt** attribute group by selecting **View attributes**.</span></span>

    <span data-ttu-id="865d1-269">该属性组应显示 **男士皮带品牌**、**皮带材质** 和 **皮带尺寸** 属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-269">The attribute group should show the **Men's belt brand**, **Belt fabric**, and **Belt size** attributes.</span></span>

> [!NOTE]
> <span data-ttu-id="865d1-270">此过程也可用于为渠道导航类别层次结构和补充产品类别层次结构中的列表分配属性组。</span><span class="sxs-lookup"><span data-stu-id="865d1-270">This procedure can also be used to assign attribute groups to categories in the Channel navigation category hierarchy and the Supplemental product category hierarchy.</span></span> <span data-ttu-id="865d1-271">在步骤 2 中，请使用以下导航路径：</span><span class="sxs-lookup"><span data-stu-id="865d1-271">In step 2, use the following navigation paths:</span></span>
>
> - <span data-ttu-id="865d1-272">Retail 和 Commerce &gt; 类别和产品管理 &gt; 渠道导航类别</span><span class="sxs-lookup"><span data-stu-id="865d1-272">Retail and Commerce &gt; Category and product management &gt; Channel navigation categories</span></span>
> - <span data-ttu-id="865d1-273">Retail 和 Commerce &gt; 类别和产品管理 &gt; 补充产品类别</span><span class="sxs-lookup"><span data-stu-id="865d1-273">Retail and Commerce &gt; Category and product management &gt; Supplemental product categories</span></span>

### <a name="assign-attribute-groups-to-stores"></a><span data-ttu-id="865d1-274">将属性组分配到商店</span><span class="sxs-lookup"><span data-stu-id="865d1-274">Assign attribute groups to stores</span></span>

<span data-ttu-id="865d1-275">一个或多个属性组可与商店层次结构中的一个或多个商店关联。</span><span class="sxs-lookup"><span data-stu-id="865d1-275">One or more attribute groups can be associated with one or more stores in the store hierarchy.</span></span> <span data-ttu-id="865d1-276">然后，为特定商店丰富产品后，这些产品将继承属性组中包含的属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-276">Then, when products are enriched for specific stores, they inherit the attributes that are included in the attribute groups.</span></span>

1. <span data-ttu-id="865d1-277">以促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="865d1-277">Sign in to the back-office client as a merchandising manager.</span></span>
2. <span data-ttu-id="865d1-278">转到 **Retail 和 Commerce** &gt; **渠道设置** &gt; **渠道类别和产品属性**。</span><span class="sxs-lookup"><span data-stu-id="865d1-278">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **Channel categories and product attributes**.</span></span>
3. <span data-ttu-id="865d1-279">为休斯顿渠道分配属性组：</span><span class="sxs-lookup"><span data-stu-id="865d1-279">Assign attribute groups to the Houston channel:</span></span>

    1. <span data-ttu-id="865d1-280">选择 **休斯顿** 渠道。</span><span class="sxs-lookup"><span data-stu-id="865d1-280">Select the **Houston** channel.</span></span>
    2. <span data-ttu-id="865d1-281">在 **属性组** 快速选项卡中，选择 **添加**，然后在 **名称** 字段中，选择 **SharePointProvisionedProductAttributeGroup**。</span><span class="sxs-lookup"><span data-stu-id="865d1-281">On the **Attribute group** FastTab, select **Add**, and then, in the **Name** field, select **SharePointProvisionedProductAttributeGroup**.</span></span>
    3. <span data-ttu-id="865d1-282">再次选择 **添加**，然后在 **名称** 字段中选择 **男士皮带**。</span><span class="sxs-lookup"><span data-stu-id="865d1-282">Select **Add** again, and then, in the **Name** field, select **Men's belt**.</span></span>
    4. <span data-ttu-id="865d1-283">再次选择 **添加**，然后在 **名称** 字段中选择 **时尚太阳镜**。</span><span class="sxs-lookup"><span data-stu-id="865d1-283">Select **Add** again, and then, in the **Name** field, select **Fashion Sunglasses**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="865d1-284">可通过一个选项指定该渠道应继承其在层次结构中的父渠道的属性组。</span><span class="sxs-lookup"><span data-stu-id="865d1-284">An option lets you specify that this channel should inherit the attribute groups from its parent channel in the hierarchy.</span></span> <span data-ttu-id="865d1-285">如果将 **继承** 选项设置为 **是**，子渠道将继承其所有属性组和这些属性组中的所有属性。</span><span class="sxs-lookup"><span data-stu-id="865d1-285">If you set the **Inherit** option to **Yes**, the child channel node inherits all the attribute groups and all the attributes in those attribute groups.</span></span>

4. <span data-ttu-id="865d1-286">请启用这些属性，以便其在休斯顿渠道中可用：</span><span class="sxs-lookup"><span data-stu-id="865d1-286">Enable the attributes so that they are available in the Houston channel:</span></span>

    1. <span data-ttu-id="865d1-287">在操作窗格上，选择 **设置属性元数据**。</span><span class="sxs-lookup"><span data-stu-id="865d1-287">On the Action Pane, select **Set attribute metadata**.</span></span>
    2. <span data-ttu-id="865d1-288">选择 **时尚** 类别节点，然后在 **渠道产品属性** 快速选项卡上，为每个属性选择 **包括属性**。</span><span class="sxs-lookup"><span data-stu-id="865d1-288">Select the **Fashion** category node, and then, on the **Channel product attributes** FastTab, select **Include attribute** for each attribute.</span></span>
    3. <span data-ttu-id="865d1-289">选择 **时尚配件** 类别节点，选择 **时尚太阳镜** 类别，然后在 **渠道产品属性** 快速选项卡上，为每个属性选择 **包括属性**。</span><span class="sxs-lookup"><span data-stu-id="865d1-289">Select the **Fashion Accessories** category node, select the **Fashion Sunglasses** category, and then, on the **Channel product attributes** FastTab, select **Include attribute** for each attribute.</span></span>
    4. <span data-ttu-id="865d1-290">选择 **安装** 类别节点，选择 **裤子** 类别，然后在 **渠道产品属性** 快速选项卡上，为每个属性选择 **包括属性**。</span><span class="sxs-lookup"><span data-stu-id="865d1-290">Select the **Menswear** category node, select the **Pants** category, and then, on the **Channel product attributes** FastTab, select **Include attribute** for each attribute.</span></span>

![渠道类别和产品属性 - 属性组](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a><span data-ttu-id="865d1-292">覆盖属性值</span><span class="sxs-lookup"><span data-stu-id="865d1-292">Overriding attribute values</span></span>

<span data-ttu-id="865d1-293">单个产品的默认属性值可在产品级别覆盖。</span><span class="sxs-lookup"><span data-stu-id="865d1-293">The default values of attributes can be overridden for individual products at the product level.</span></span> <span data-ttu-id="865d1-294">也可以覆盖针对特定渠道的特定目录中的单个产品的默认值。</span><span class="sxs-lookup"><span data-stu-id="865d1-294">Default values can also be overridden for individual products in specific catalogs that are targeted at specific channels.</span></span>

### <a name="override-the-attribute-values-of-an-individual-product"></a><span data-ttu-id="865d1-295">覆盖单个产品的属性值</span><span class="sxs-lookup"><span data-stu-id="865d1-295">Override the attribute values of an individual product</span></span>

1. <span data-ttu-id="865d1-296">以促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="865d1-296">Sign in to the back-office client as a merchandising manager.</span></span>
2. <span data-ttu-id="865d1-297">转至 **Retail 和 Commerce** &gt; **类别和产品管理** &gt; **已发布的产品(按类别)**。</span><span class="sxs-lookup"><span data-stu-id="865d1-297">Go to **Retail and Commerce** &gt; **Category and product management** &gt; **Released products by category**.</span></span>
3. <span data-ttu-id="865d1-298">选择 **时尚** &gt; **时尚配件** &gt; **时尚太阳镜** 类别节点。</span><span class="sxs-lookup"><span data-stu-id="865d1-298">Select the **Fashion** &gt; **Fashion Accessories** &gt; **Fashion Sunglasses** category node.</span></span>
4. <span data-ttu-id="865d1-299">在网格中选择所需产品。</span><span class="sxs-lookup"><span data-stu-id="865d1-299">Select the required product in the grid.</span></span> <span data-ttu-id="865d1-300">然后，在操作窗格中 **产品** 选项卡上的 **设置** 组中，选择 **产品属性**。</span><span class="sxs-lookup"><span data-stu-id="865d1-300">Then, on the Action Pane, on the **Product** tab, in the **Set up** group, select **Product attributes**.</span></span>
5. <span data-ttu-id="865d1-301">在左窗格中选择一个属性，然后在右窗格中更新其值。</span><span class="sxs-lookup"><span data-stu-id="865d1-301">Select an attribute in the left pane, and then update its value in the right pane.</span></span>

![产品详细信息页面 - 产品属性组](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a><span data-ttu-id="865d1-303">覆盖目录中的产品的属性值</span><span class="sxs-lookup"><span data-stu-id="865d1-303">Override the attribute values of products in a catalog</span></span>

1. <span data-ttu-id="865d1-304">以促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="865d1-304">Sign in to the back-office client as a merchandising manager.</span></span>
2. <span data-ttu-id="865d1-305">转至 **Retail 和 Commerce** &gt; **目录管理** &gt; **所有目录**。</span><span class="sxs-lookup"><span data-stu-id="865d1-305">Go to **Retail and Commerce** &gt; **Catalog management** &gt; **All catalogs**.</span></span>
3. <span data-ttu-id="865d1-306">选择 **Fabrikam Base Catalog** 目录。</span><span class="sxs-lookup"><span data-stu-id="865d1-306">Select the **Fabrikam Base Catalog** catalog.</span></span>
4. <span data-ttu-id="865d1-307">选择 **时尚** &gt; **时尚配件** &gt; **时尚太阳镜** 类别节点。</span><span class="sxs-lookup"><span data-stu-id="865d1-307">Select the **Fashion** &gt; **Fashion Accessories** &gt; **Fashion Sunglasses** category node.</span></span>
5. <span data-ttu-id="865d1-308">在 **产品** 快速选项卡中，选择所需产品，然后选择产品网格上方的 **属性**。</span><span class="sxs-lookup"><span data-stu-id="865d1-308">On the **Products** FastTab, select the required product, and then select **Attributes** above the product grid.</span></span>
6. <span data-ttu-id="865d1-309">在以下快速选项卡上，更新所需属性的值。</span><span class="sxs-lookup"><span data-stu-id="865d1-309">On the following FastTabs, update the values of the required attributes:</span></span>

    - <span data-ttu-id="865d1-310">共享的产品媒体</span><span class="sxs-lookup"><span data-stu-id="865d1-310">Shared product media</span></span>
    - <span data-ttu-id="865d1-311">共享产品属性</span><span class="sxs-lookup"><span data-stu-id="865d1-311">Shared product attributes</span></span>
    - <span data-ttu-id="865d1-312">通道媒体</span><span class="sxs-lookup"><span data-stu-id="865d1-312">Channel media</span></span>
    - <span data-ttu-id="865d1-313">渠道产品属性</span><span class="sxs-lookup"><span data-stu-id="865d1-313">Channel product attributes</span></span>

    > [!NOTE]
    > <span data-ttu-id="865d1-314">如果创建共享产品介质和共享产品属性，它们将应用于所有产品。</span><span class="sxs-lookup"><span data-stu-id="865d1-314">If shared product media and shared product attributes are created, they apply to all the products.</span></span>

![目录产品属性组](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a><span data-ttu-id="865d1-316">覆盖渠道中的产品的属性值</span><span class="sxs-lookup"><span data-stu-id="865d1-316">Override the attribute values of products in a channel</span></span>

1. <span data-ttu-id="865d1-317">以促销经理的身份登录后端办公客户端。</span><span class="sxs-lookup"><span data-stu-id="865d1-317">Sign in to the back-office client as a merchandising manager.</span></span>
2. <span data-ttu-id="865d1-318">转到 **Retail 和 Commerce** &gt; **渠道设置** &gt; **渠道类别和产品属性**。</span><span class="sxs-lookup"><span data-stu-id="865d1-318">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **Channel categories and product attributes**.</span></span>
3. <span data-ttu-id="865d1-319">选择 **休斯顿** 渠道。</span><span class="sxs-lookup"><span data-stu-id="865d1-319">Select the **Houston** channel.</span></span>
4. <span data-ttu-id="865d1-320">在 **产品** 快速选项卡中，选择所需产品，然后选择产品网格上方的 **属性**。</span><span class="sxs-lookup"><span data-stu-id="865d1-320">On the **Products** FastTab, select the required product, and then select **Attributes** above the product grid.</span></span>

    > [!NOTE]
    > <span data-ttu-id="865d1-321">如果无可用产品，请添加产品，方法是在 **产品** 快速选项卡上选择 **添加**，然后在 **添加产品** 对话框中选择所需产品。</span><span class="sxs-lookup"><span data-stu-id="865d1-321">If no products are available, add products by selecting **Add** on the **Products** FastTab and then selecting the required products in the **Add products** dialog box.</span></span>

5. <span data-ttu-id="865d1-322">在以下快速选项卡上，更新所需属性的值。</span><span class="sxs-lookup"><span data-stu-id="865d1-322">On the following FastTabs, update the values of the required attributes:</span></span>

    - <span data-ttu-id="865d1-323">共享的产品媒体</span><span class="sxs-lookup"><span data-stu-id="865d1-323">Shared product media</span></span>
    - <span data-ttu-id="865d1-324">共享产品属性</span><span class="sxs-lookup"><span data-stu-id="865d1-324">Shared product attributes</span></span>
    - <span data-ttu-id="865d1-325">通道媒体</span><span class="sxs-lookup"><span data-stu-id="865d1-325">Channel media</span></span>
    - <span data-ttu-id="865d1-326">渠道产品属性</span><span class="sxs-lookup"><span data-stu-id="865d1-326">Channel product attributes</span></span>

    > [!NOTE]
    > <span data-ttu-id="865d1-327">如果创建共享产品介质和共享产品属性，它们将应用于所有产品。</span><span class="sxs-lookup"><span data-stu-id="865d1-327">If shared product media and shared product attributes are created, they apply to all the products.</span></span>
