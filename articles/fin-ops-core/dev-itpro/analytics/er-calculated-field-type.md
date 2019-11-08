---
title: 支持对计算字段类型的 ER 数据源执行参数化调用
description: 此主题提供有关如何对 ER 数据源使用计算字段类型的信息。
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550076"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="8d32f-103">支持对计算字段类型的 ER 数据源执行参数化调用</span><span class="sxs-lookup"><span data-stu-id="8d32f-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d32f-104">此主题介绍如何使用**计算字段**类型设计电子申报 (ER) 数据源。</span><span class="sxs-lookup"><span data-stu-id="8d32f-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="8d32f-105">此数据库中可以包含一个 ER 表达式，其在执行时由调用此数据源的绑定中配置的参数自变量的值控制。</span><span class="sxs-lookup"><span data-stu-id="8d32f-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="8d32f-106">通过配置此类数据源的参数化调用，可以在大量绑定中重复使用一个数据源，从而减少必须在 ER 模型映射或 ER 格式中配置的数据源的总数。</span><span class="sxs-lookup"><span data-stu-id="8d32f-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="8d32f-107">还可以简化配置的 ER 组件，从而降低维护成本和其他使用者的使用成本。</span><span class="sxs-lookup"><span data-stu-id="8d32f-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d32f-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="8d32f-108">Prerequisites</span></span>
<span data-ttu-id="8d32f-109">要完成本主题中的示例，您必须具有以下访问权限：</span><span class="sxs-lookup"><span data-stu-id="8d32f-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="8d32f-110">访问以下角色之一：</span><span class="sxs-lookup"><span data-stu-id="8d32f-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="8d32f-111">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="8d32f-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="8d32f-112">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="8d32f-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="8d32f-113">系统管理员</span><span class="sxs-lookup"><span data-stu-id="8d32f-113">System administrator</span></span>

- <span data-ttu-id="8d32f-114">对于下列角色之一，访问已为与 Finance and Operations 相同的租户配置的 Regulatory Configuration Services (RCS)：</span><span class="sxs-lookup"><span data-stu-id="8d32f-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="8d32f-115">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="8d32f-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="8d32f-116">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="8d32f-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="8d32f-117">系统管理员</span><span class="sxs-lookup"><span data-stu-id="8d32f-117">System administrator</span></span>

<span data-ttu-id="8d32f-118">从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载压缩文件**支持对计算字段类型的 ER 数据源执行参数化调用**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="8d32f-119">其中包含必须提取并存储到本地的以下 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="8d32f-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="8d32f-120">**内容**</span><span class="sxs-lookup"><span data-stu-id="8d32f-120">**Content**</span></span>                           | <span data-ttu-id="8d32f-121">**文件名**</span><span class="sxs-lookup"><span data-stu-id="8d32f-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8d32f-122">示例 ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="8d32f-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="8d32f-123">用于了解参数化调用的模型.版本.1.xml</span><span class="sxs-lookup"><span data-stu-id="8d32f-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="8d32f-124">示例 ER 元数据配置</span><span class="sxs-lookup"><span data-stu-id="8d32f-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="8d32f-125">用于了解参数化调用的元数据.版本.1.xml</span><span class="sxs-lookup"><span data-stu-id="8d32f-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="8d32f-126">示例 ER 模型映射配置</span><span class="sxs-lookup"><span data-stu-id="8d32f-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="8d32f-127">用于了解参数化调用的映射.版本.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="8d32f-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="8d32f-128">示例 ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="8d32f-128">Sample ER format configuration</span></span>        | <span data-ttu-id="8d32f-129">用于了解参数化调用的格式.版本.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="8d32f-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="8d32f-130">登录您的 RCS 实例</span><span class="sxs-lookup"><span data-stu-id="8d32f-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="8d32f-131">在此示例中，将为示例公司 Litware 公司创建一个配置。首先必须在 RCS 中完成[创建一个配置提供程序，并标记其为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程中的步骤：</span><span class="sxs-lookup"><span data-stu-id="8d32f-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="8d32f-132">在默认仪表板中，选择**电子申报**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="8d32f-133">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="8d32f-134">按照以下顺序将下载的配置导入到 RCS 中：数据模型、元数据、模型映射、格式。</span><span class="sxs-lookup"><span data-stu-id="8d32f-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="8d32f-135">为每个 ER 配置完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="8d32f-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="8d32f-136">选择**交换**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="8d32f-137">选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="8d32f-138">选择**浏览**，然后选择 XML 格式的所需 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="8d32f-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="8d32f-139">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="8d32f-140">查看提供的 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="8d32f-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="8d32f-141">查看模型映射</span><span class="sxs-lookup"><span data-stu-id="8d32f-141">Review model mapping</span></span>

1. <span data-ttu-id="8d32f-142">在配置树中，展开**用于了解参数化调用的模型**项的内容。</span><span class="sxs-lookup"><span data-stu-id="8d32f-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="8d32f-143">选择**用于了解参数化调用的映射**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="8d32f-144">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-144">Select **Designer**.</span></span>
4. <span data-ttu-id="8d32f-145">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="8d32f-146">此 ER 模型映射用于执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8d32f-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="8d32f-147">提取 **TaxTable** 表中的税码（**税**数据源）的列表。</span><span class="sxs-lookup"><span data-stu-id="8d32f-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="8d32f-148">提取 **TaxTrans** 表中的税务交易记录（**交易记录**数据源）的列表：</span><span class="sxs-lookup"><span data-stu-id="8d32f-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="8d32f-149">按税码为提取的交易记录（**组**数据源）列表分组。</span><span class="sxs-lookup"><span data-stu-id="8d32f-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="8d32f-150">按税码计算分组的交易记录的以下聚合值：</span><span class="sxs-lookup"><span data-stu-id="8d32f-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="8d32f-151">税金基数值的和。</span><span class="sxs-lookup"><span data-stu-id="8d32f-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="8d32f-152">税金值的和。</span><span class="sxs-lookup"><span data-stu-id="8d32f-152">Sum of tax values.</span></span>
        - <span data-ttu-id="8d32f-153">采用的税率的最小值。</span><span class="sxs-lookup"><span data-stu-id="8d32f-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="8d32f-154">此配置中的模型映射实施为此模型创建并在 Finance and Operations 中执行的任何 ER 格式的基本数据模型。</span><span class="sxs-lookup"><span data-stu-id="8d32f-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="8d32f-155">结果，**Tax**和 **Gr** 数据源的内容将对抽象数据源之类 ER 格式公开。</span><span class="sxs-lookup"><span data-stu-id="8d32f-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![其中显示“税”和“组”数据源的模型映射设计器页面](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="8d32f-157">关闭**模型映射设计器**页。</span><span class="sxs-lookup"><span data-stu-id="8d32f-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="8d32f-158">关闭**模型映射**页。</span><span class="sxs-lookup"><span data-stu-id="8d32f-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="8d32f-159">查看格式</span><span class="sxs-lookup"><span data-stu-id="8d32f-159">Review format</span></span>

1. <span data-ttu-id="8d32f-160">在配置树中，展开**用于了解参数化调用的模型**项的内容。</span><span class="sxs-lookup"><span data-stu-id="8d32f-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="8d32f-161">选择**用于了解参数化调用的格式**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="8d32f-162">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-162">Select **Designer**.</span></span> <span data-ttu-id="8d32f-163">此 ER 格式用于执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8d32f-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="8d32f-164">生成 XML 格式的报税单。</span><span class="sxs-lookup"><span data-stu-id="8d32f-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="8d32f-165">在报税单中提供以下征税级别：正常、减税、免税。</span><span class="sxs-lookup"><span data-stu-id="8d32f-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="8d32f-166">在每个征税级别提供多项详细信息，从而每个级别包含不同数量的详细信息。</span><span class="sxs-lookup"><span data-stu-id="8d32f-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![“格式设计器”页面](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="8d32f-168">选择**映射**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="8d32f-169">展开**模型**、**数据**和**摘要**项。</span><span class="sxs-lookup"><span data-stu-id="8d32f-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="8d32f-170">计算字段**模型.数据.摘要.级别**中包含表达式，用于将征税级别（**正常**、**减税**、**免税**或**其他**）的代码作为可在运行时从**模型.数据.摘要**数据源检索的任何税码的文本值返回。</span><span class="sxs-lookup"><span data-stu-id="8d32f-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![其中显示“用于了解参数化调用的数据模型”模型的详细信息的格式设计器页面](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="8d32f-172">展开**模型**.**数据2** 项。</span><span class="sxs-lookup"><span data-stu-id="8d32f-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="8d32f-173">展开**模型**.**数据2.摘要2** 项。</span><span class="sxs-lookup"><span data-stu-id="8d32f-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="8d32f-174">配置**模型**.**数据2.摘要2** 数据源是为了按（**模型.数据.摘要.级别**计算字段返回的）征税级别为**模型.数据.摘要**数据源交易记录详细信息分组和计算聚合。</span><span class="sxs-lookup"><span data-stu-id="8d32f-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![其中显示“模型.数据2.摘要2”数据源的详细信息的格式设计器页面](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="8d32f-176">查看计算字段**模型**.**数据2.级别1**、**模型**.**数据2.级别2** 和**模型**.**数据2.级别3**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="8d32f-177">这些计算字段用于筛选**模型**.**数据2.摘要2** 记录列表和仅返回表示特定征税级别的记录。</span><span class="sxs-lookup"><span data-stu-id="8d32f-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="8d32f-178">关闭**格式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="8d32f-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="8d32f-179">创建派生格式</span><span class="sxs-lookup"><span data-stu-id="8d32f-179">Create a derived format</span></span>
<span data-ttu-id="8d32f-180">可通过添加一个计算字段来筛选所需征税级别，而不是使用现有三个字段，改进提供的格式：**模型**.**数据2.级别1**、**模型**.**数据2.级别2** 和**模型**.**数据2.级别3**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="8d32f-181">可以在将调用这个新计算字段的位置中指定所需征税级别。</span><span class="sxs-lookup"><span data-stu-id="8d32f-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="8d32f-182">在配置树中，展开**用于了解参数化调用的模型**项的内容。</span><span class="sxs-lookup"><span data-stu-id="8d32f-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="8d32f-183">选择**用于了解参数化调用的格式**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="8d32f-184">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="8d32f-185">选择**从以下名称派生: 用于了解参数化调用的格式, Microsoft**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="8d32f-186">在**名称**字段中，输入**用于了解参数化调用的格式(自定义)**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="8d32f-187">选择**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="8d32f-188">配置用于返回记录列表的参数化计算字段</span><span class="sxs-lookup"><span data-stu-id="8d32f-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="8d32f-189">开始添加新的计算字段</span><span class="sxs-lookup"><span data-stu-id="8d32f-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="8d32f-190">选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-190">Select **Designer**.</span></span>
2. <span data-ttu-id="8d32f-191">选择**展开/折叠**以展开所有格式项。</span><span class="sxs-lookup"><span data-stu-id="8d32f-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="8d32f-192">选择**映射**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="8d32f-193">展开**模型**项。</span><span class="sxs-lookup"><span data-stu-id="8d32f-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="8d32f-194">选择**模型.数据2** 项。</span><span class="sxs-lookup"><span data-stu-id="8d32f-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="8d32f-195">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-195">Select **Add**.</span></span>
7. <span data-ttu-id="8d32f-196">选择**函数\\计算字段**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="8d32f-197">在**名称**字段中，输入**级别**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="8d32f-198">选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="8d32f-199">定义用于添加计算字段的参数</span><span class="sxs-lookup"><span data-stu-id="8d32f-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="8d32f-200">选择**参数**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="8d32f-201">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-201">Select **New**.</span></span>
3. <span data-ttu-id="8d32f-202">在**名称**字段中，输入**征税级别**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="8d32f-203">在**类型**字段中，选择**字符串**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="8d32f-204">只有原始数据类型才能用于指定参数的自变量类型。</span><span class="sxs-lookup"><span data-stu-id="8d32f-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="8d32f-205">因此，**记录列表**、**记录**和**枚举**类型不能用于此用途。</span><span class="sxs-lookup"><span data-stu-id="8d32f-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="8d32f-206">为一个计算字段最多可以指定 8 个参数。</span><span class="sxs-lookup"><span data-stu-id="8d32f-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![参数数据源列表](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="8d32f-208">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-208">Select **OK**.</span></span>

<span data-ttu-id="8d32f-209">可以通过添加此参数来指定调用此计算字段所需条件。</span><span class="sxs-lookup"><span data-stu-id="8d32f-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="8d32f-210">调用此计算字段时，需要将**征税级别**参数的自变量指定为**字符串**格式的值。</span><span class="sxs-lookup"><span data-stu-id="8d32f-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="8d32f-211">请确保仅为容器中包含的计算字段（**记录列表**、**记录**或**容器**）定义参数。</span><span class="sxs-lookup"><span data-stu-id="8d32f-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="8d32f-212">将在此计算字段的数据源列表中提供配置的参数。</span><span class="sxs-lookup"><span data-stu-id="8d32f-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="8d32f-213">可通过选择**添加数据源**向配置的表达式添加参数。</span><span class="sxs-lookup"><span data-stu-id="8d32f-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![数据源字段](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="8d32f-215">定义用于添加计算字段的表达式</span><span class="sxs-lookup"><span data-stu-id="8d32f-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="8d32f-216">在**公式**字段中，输入：</span><span class="sxs-lookup"><span data-stu-id="8d32f-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="8d32f-217">**WHERE(\@.摘要2, \@.摘要2.分组.级别 =**</span><span class="sxs-lookup"><span data-stu-id="8d32f-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="8d32f-218">在数据源列表中选择**征税级别**参数。</span><span class="sxs-lookup"><span data-stu-id="8d32f-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="8d32f-219">选择**添加数据源**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="8d32f-220">在**公式**字段中，设置如下表达式：</span><span class="sxs-lookup"><span data-stu-id="8d32f-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="8d32f-221">**WHERE(\@.摘要2, \@.摘要2.分组.级别 = '征税级别')**</span><span class="sxs-lookup"><span data-stu-id="8d32f-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="8d32f-222">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-222">Select **Save**.</span></span>

    ![数据源字段信息](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="8d32f-224">关闭**公式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="8d32f-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="8d32f-225">完成添加新的计算字段</span><span class="sxs-lookup"><span data-stu-id="8d32f-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="8d32f-226">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-226">Select **OK**.</span></span>

<span data-ttu-id="8d32f-227">在**格式设计器**页面中，配置的参数化计算字段**级别**需要一个**字符串**自变量。</span><span class="sxs-lookup"><span data-stu-id="8d32f-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![展开的计算字段级别列表](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="8d32f-229">对绑定格式元素使用配置的计算字段</span><span class="sxs-lookup"><span data-stu-id="8d32f-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="8d32f-230">选择**模型.数据2.级别**以选择配置的计算字段。</span><span class="sxs-lookup"><span data-stu-id="8d32f-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="8d32f-231">选择**报.税.正常**格式元素。</span><span class="sxs-lookup"><span data-stu-id="8d32f-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="8d32f-232">选择**绑定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-232">Select **Bind**.</span></span>
4. <span data-ttu-id="8d32f-233">选择**是**以确认在所选格式元素的所有嵌套格式元素中，将当前使用的数据源**级别1** 替换为新数据源**级别**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="8d32f-234">应用的绑定已构建为参数化计算字段的一个调用。</span><span class="sxs-lookup"><span data-stu-id="8d32f-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="8d32f-235">在以下情况下，绑定格式元素的名称默认用作参数化计算字段的自变量：</span><span class="sxs-lookup"><span data-stu-id="8d32f-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="8d32f-236">计算字段配置为使用单个参数。</span><span class="sxs-lookup"><span data-stu-id="8d32f-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="8d32f-237">此参数的数据类型定义为**字符串**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="8d32f-238">如果绑定格式元素的名称为空，则在应用的绑定中使用此元素的数据源名称。</span><span class="sxs-lookup"><span data-stu-id="8d32f-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="8d32f-239">选择**报.税.减税**格式元素。</span><span class="sxs-lookup"><span data-stu-id="8d32f-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="8d32f-240">选择**绑定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-240">Select **Bind**.</span></span>
7. <span data-ttu-id="8d32f-241">选择**是**以确认在所选格式元素下的所有嵌套格式元素中，将当前使用的数据源**级别2** 替换为新数据源**级别**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="8d32f-242">选择**报.税.免税**格式元素。</span><span class="sxs-lookup"><span data-stu-id="8d32f-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="8d32f-243">选择**绑定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-243">Select **Bind**.</span></span>
10. <span data-ttu-id="8d32f-244">选择**是**以确认在所选格式元素下的所有嵌套格式元素中，将当前使用的数据源**级别3** 替换为新数据源**级别**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="8d32f-245">为表示征税级别的 XML 元素指定参数化计算字段的自变量时（例如，**模型.数据2.级别("减税")** 作为文本值），则无需对嵌套的 XML 属性执行z相同操作 — 其绑定将自动继承在父级别（**模型.数据2.级别.聚合.基数**，而不是**模型.数据2.级别("减税").聚合.基数**）定义的自变量的值。</span><span class="sxs-lookup"><span data-stu-id="8d32f-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="8d32f-246">不支持重复调用任何参数化计算字段。</span><span class="sxs-lookup"><span data-stu-id="8d32f-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="8d32f-247">您在选择的绑定中，可以选择 **编辑配方**和更改将参数化的计算字段的应用由默认参数。</span><span class="sxs-lookup"><span data-stu-id="8d32f-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="8d32f-248">如果缺少此自变量，可能导致运行时出错 — 在验证当前格式时通知用户此类情况。</span><span class="sxs-lookup"><span data-stu-id="8d32f-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![验证警告通知](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="8d32f-250">配置参数化计算字段以返回记录</span><span class="sxs-lookup"><span data-stu-id="8d32f-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="8d32f-251">如果参数化计算字段返回记录，您需要支持将此记录的单个字段绑定到格式元素。</span><span class="sxs-lookup"><span data-stu-id="8d32f-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="8d32f-252">在此类情况下，不存在包含用于调用参数化计算字段的自变量的值的父绑定 — 必须在单个记录的字段的绑定中定义该值。</span><span class="sxs-lookup"><span data-stu-id="8d32f-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="8d32f-253">开始添加新的计算字段</span><span class="sxs-lookup"><span data-stu-id="8d32f-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="8d32f-254">选择**模型.数据2** 项。</span><span class="sxs-lookup"><span data-stu-id="8d32f-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="8d32f-255">选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-255">Select **Add**.</span></span>
3. <span data-ttu-id="8d32f-256">选择**函数\\计算字段**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="8d32f-257">在**名称**字段中，输入**级别记录**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="8d32f-258">选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="8d32f-259">定义用于添加计算字段的参数</span><span class="sxs-lookup"><span data-stu-id="8d32f-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="8d32f-260">选择**参数**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="8d32f-261">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-261">Select **New**.</span></span>
3. <span data-ttu-id="8d32f-262">在**名称**字段中，输入**征税级别**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="8d32f-263">在**类型**字段中，选择**字符串**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="8d32f-264">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="8d32f-265">定义用于添加计算字段的表达式</span><span class="sxs-lookup"><span data-stu-id="8d32f-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="8d32f-266">在**公式**字段中，输入以下内容：</span><span class="sxs-lookup"><span data-stu-id="8d32f-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="8d32f-267">**FIRSTORNULL(\@.级别(**</span><span class="sxs-lookup"><span data-stu-id="8d32f-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="8d32f-268">选择**征税级别**参数。</span><span class="sxs-lookup"><span data-stu-id="8d32f-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="8d32f-269">选择**添加数据源**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="8d32f-270">在**公式**字段中，将 **'征税级别'))** 追加到在步骤 1 中输入的内容后，以便将表达式设置为：</span><span class="sxs-lookup"><span data-stu-id="8d32f-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="8d32f-271">**FIRSTORNULL(\@.级别('征税级别'))**</span><span class="sxs-lookup"><span data-stu-id="8d32f-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="8d32f-272">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-272">Select **Save**.</span></span>
6. <span data-ttu-id="8d32f-273">关闭**公式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="8d32f-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="8d32f-274">完成添加新的计算字段</span><span class="sxs-lookup"><span data-stu-id="8d32f-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="8d32f-275">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="8d32f-276">使用配置的计算字段绑定公式元素</span><span class="sxs-lookup"><span data-stu-id="8d32f-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="8d32f-277">展开**模型.数据2.级别记录**以选择配置的计算字段。</span><span class="sxs-lookup"><span data-stu-id="8d32f-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="8d32f-278">展开配置的计算字段的**模型.数据2.级别记录.聚合**容器。</span><span class="sxs-lookup"><span data-stu-id="8d32f-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="8d32f-279">选择**模型.数据2.级别记录.聚合.基数**字段。</span><span class="sxs-lookup"><span data-stu-id="8d32f-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="8d32f-280">选择**报.税.免税**格式元素。</span><span class="sxs-lookup"><span data-stu-id="8d32f-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="8d32f-281">选择**取消绑定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="8d32f-282">选择**报.税.免税.基数**格式元素。</span><span class="sxs-lookup"><span data-stu-id="8d32f-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="8d32f-283">选择**绑定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-283">Select **Bind**.</span></span>
8. <span data-ttu-id="8d32f-284">选择**编辑公式**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="8d32f-285">将表达式更改为**模型.数据2.级别记录("免税").聚合.基数**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![更新后的表达式](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="8d32f-287">删除不使用的计算字段</span><span class="sxs-lookup"><span data-stu-id="8d32f-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="8d32f-288">选择**模型.数据2.级别1**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="8d32f-289">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-289">Select **Delete**.</span></span>
3. <span data-ttu-id="8d32f-290">选择**模型.数据2.级别2**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="8d32f-291">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-291">Select **Delete**.</span></span>
5. <span data-ttu-id="8d32f-292">选择**模型.数据2.级别3**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="8d32f-293">选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-293">Select **Delete**.</span></span>
7. <span data-ttu-id="8d32f-294">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="8d32f-295">您在格式绑定中多次重复使用了同一个计算字段**模型.数据2.级别**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="8d32f-296">使用和维护单个计算字段而不是对多个相似字段执行此操作容易得多。</span><span class="sxs-lookup"><span data-stu-id="8d32f-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="8d32f-297">关闭**格式设计器**页。</span><span class="sxs-lookup"><span data-stu-id="8d32f-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="8d32f-298">完成调整后的派生格式版本</span><span class="sxs-lookup"><span data-stu-id="8d32f-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="8d32f-299">在**版本**快速选项卡中，选择**更改状态**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="8d32f-300">选择**完成**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="8d32f-301">导出完成的派生格式版本</span><span class="sxs-lookup"><span data-stu-id="8d32f-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="8d32f-302">在配置树中选择**用于了解参数化调用的格式(自定义)** 格式。</span><span class="sxs-lookup"><span data-stu-id="8d32f-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="8d32f-303">在**版本**快速选项卡中，选择已完成版本 1.1.1。</span><span class="sxs-lookup"><span data-stu-id="8d32f-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="8d32f-304">选择**交换**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="8d32f-305">选择**导出为 XML 文件**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="8d32f-306">将下载的配置以 XML 格式存储在本地。</span><span class="sxs-lookup"><span data-stu-id="8d32f-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="8d32f-307">测试 ER 格式</span><span class="sxs-lookup"><span data-stu-id="8d32f-307">Test ER formats</span></span> 
<span data-ttu-id="8d32f-308">可运行初始 ER 格式和改进的 ER 格式以确保配置的参数化计算字段正确工作。</span><span class="sxs-lookup"><span data-stu-id="8d32f-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="8d32f-309">导入 ER 配置</span><span class="sxs-lookup"><span data-stu-id="8d32f-309">Import ER configurations</span></span>
<span data-ttu-id="8d32f-310">可通过使用 **RCS** 类型的 ER 存储库从 RCS 导入已审查的配置。</span><span class="sxs-lookup"><span data-stu-id="8d32f-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="8d32f-311">如果已经执行了[从 Regulatory Configuration Service 导入电子申报配置](rcs-download-configurations.md)主题中的步骤，请使用配置的 ER 存储库将本主题前文讨论的配置导入到您的环境中。</span><span class="sxs-lookup"><span data-stu-id="8d32f-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="8d32f-312">否则，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="8d32f-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="8d32f-313">选择 **DEMF** 公司，然后在默认仪表板中选择**电子申报**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="8d32f-314">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="8d32f-315">按照以下顺序从 Microsoft 下载中心导入配置：数据模型、元数据、模型映射、格式。</span><span class="sxs-lookup"><span data-stu-id="8d32f-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="8d32f-316">为每个 ER 配置完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="8d32f-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="8d32f-317">选择**交换**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="8d32f-318">选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="8d32f-319">选择**浏览**以选择 XML 格式的所需 ER 配置。</span><span class="sxs-lookup"><span data-stu-id="8d32f-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="8d32f-320">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-320">Select **OK**.</span></span>

4. <span data-ttu-id="8d32f-321">导入从 RCS 导出的**用于了解参数化调用的格式(自定义)** 格式的已完成版本 1.1.1：</span><span class="sxs-lookup"><span data-stu-id="8d32f-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="8d32f-322">选择**交换**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="8d32f-323">选择**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="8d32f-324">选择**浏览**以选择本地存储的 XML 格式的**用于了解参数化调用的格式(自定义)** 文件。</span><span class="sxs-lookup"><span data-stu-id="8d32f-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="8d32f-325">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="8d32f-326">运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="8d32f-326">Run ER formats</span></span>

1. <span data-ttu-id="8d32f-327">在配置树中，展开**用于了解参数化调用的模型**项的内容。</span><span class="sxs-lookup"><span data-stu-id="8d32f-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="8d32f-328">选择**用于了解参数化调用的格式**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="8d32f-329">在最上面的功能区中选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="8d32f-330">保存本地生成的输出。</span><span class="sxs-lookup"><span data-stu-id="8d32f-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="8d32f-331">选择**用于了解参数化调用的格式(自定义)** 项。</span><span class="sxs-lookup"><span data-stu-id="8d32f-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="8d32f-332">在最上面的功能区中选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="8d32f-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="8d32f-333">将生成的输出保存到本地。</span><span class="sxs-lookup"><span data-stu-id="8d32f-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="8d32f-334">比较生成的输出的内容。</span><span class="sxs-lookup"><span data-stu-id="8d32f-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d32f-335">其他资源</span><span class="sxs-lookup"><span data-stu-id="8d32f-335">Additional resources</span></span>
[<span data-ttu-id="8d32f-336">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="8d32f-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
