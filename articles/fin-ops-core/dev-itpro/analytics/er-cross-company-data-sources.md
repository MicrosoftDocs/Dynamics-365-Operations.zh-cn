---
title: 电子设备 (ER) 中的公司间数据源
description: 本主题介绍如何在电子申报 (ER) 中使用公司间数据源。
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1a5c05b65c9022220056947471e95b703d923dc5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680822"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a><span data-ttu-id="3378f-103">电子设备 (ER) 中的公司间数据源</span><span class="sxs-lookup"><span data-stu-id="3378f-103">Cross-company data sources in Electronic reporting (ER)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3378f-104">可以设计电子申报 (ER) 格式以生成各种格式的传出单据。</span><span class="sxs-lookup"><span data-stu-id="3378f-104">You can design Electronic reporting (ER) formats to generate outgoing documents in various formats.</span></span> <span data-ttu-id="3378f-105">生成单据时，ER 格式调用在相应 ER 模型映射中配置的数据源。</span><span class="sxs-lookup"><span data-stu-id="3378f-105">When a document is generated, an ER format calls data sources that were configured in a corresponding ER model mapping.</span></span> <span data-ttu-id="3378f-106">若要配置对申请表的访问以检索记录，可使用 **表记录** 类型的 ER 数据源。</span><span class="sxs-lookup"><span data-stu-id="3378f-106">To configure access to application tables for record retrieval, you can use ER data sources of the **Table records** type.</span></span> <span data-ttu-id="3378f-107">访问表为共享表（即表中的数据在保存时不带公司标识符）时，此数据源将返回所有记录。</span><span class="sxs-lookup"><span data-stu-id="3378f-107">When the accessing table is a shared table (that is, a table where data is saved without a company identifier), this data source returns all records.</span></span> <span data-ttu-id="3378f-108">访问表为依赖于公司的表（即表中的数据按公司保存）时，此数据源仅返回已为当前公司保存的记录（即，运行 ER 格式的公司环境）。</span><span class="sxs-lookup"><span data-stu-id="3378f-108">When the accessing table is a company-dependent table (that is, a table where data is saved per company), this data source returns only the records that have been saved for the current company (that is, the company context that the ER format is running under).</span></span>

<span data-ttu-id="3378f-109">现在可将模型映射中类型为 **表记录** 的每个数据源标记为公司间。</span><span class="sxs-lookup"><span data-stu-id="3378f-109">Every data source of the **Table records** type in a model mapping can be now marked as a cross-company data source.</span></span> <span data-ttu-id="3378f-110">因此，可使用类型为 **表记录** 的数据源访问申请表中的公司间数据。</span><span class="sxs-lookup"><span data-stu-id="3378f-110">Therefore, you can use data sources of the **Table records** type to access cross-company data in application tables.</span></span>

<span data-ttu-id="3378f-111">如果将一个数据源标记为公司间数据源，则将发生行为：</span><span class="sxs-lookup"><span data-stu-id="3378f-111">If you mark a data source as cross-company, the following behavior occurs:</span></span>

- <span data-ttu-id="3378f-112">对于引用除 CompanyInfo 外的任何共享表的数据源，该数据源将返回所引用表中的全部记录。</span><span class="sxs-lookup"><span data-stu-id="3378f-112">For a data source that refers to any shared table except CompanyInfo, the data source returns all records that exist in the referenced table.</span></span> 
- <span data-ttu-id="3378f-113">对于引用 CompanyInfo 表的数据源，即使 CompanyInfo 是共享表，该数据源仍然返回包含定义的范围中一家公司的标识符的记录。</span><span class="sxs-lookup"><span data-stu-id="3378f-113">For a data source that refers to the CompanyInfo table, even though CompanyInfo is a shared table, the data source returns the records that contain the identifier of a company from the defined scope.</span></span>
- <span data-ttu-id="3378f-114">对于任何依赖于公司的表，该数据源返回包含定义的范围中一家公司的标识符的所引用表的记录。</span><span class="sxs-lookup"><span data-stu-id="3378f-114">For any company-dependent table, the data source returns the records of the referenced table that contain the identifier of a company from the defined scope.</span></span>

<span data-ttu-id="3378f-115">在系统查询对话框中，如果为标记为公司间的任何数据源开启了 **要求查询** 选项，则可在 **公司范围** 选项卡中手动选择要包括的一家或多家公司。</span><span class="sxs-lookup"><span data-stu-id="3378f-115">In the system query dialog box, when the **Ask for query** option is turned on for any data source that is marked as cross-company, you can manually select one or more companies to include on the **Company range** tab.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3378f-116">与其他筛选器不同，公司筛选器标记为在您运行 ER 格式时为查询最后使用的值。</span><span class="sxs-lookup"><span data-stu-id="3378f-116">Like other filters, the company filter is persisted as a last-used value for queries when you run an ER format.</span></span> <span data-ttu-id="3378f-117">如果更改数据源的公司间值，将不自动更改该筛选器。</span><span class="sxs-lookup"><span data-stu-id="3378f-117">The filter isn't automatically changed if you change the cross-company value for a data source.</span></span> <span data-ttu-id="3378f-118">若要为另一个数据源使用其他公司间值，请删除相应的用户特定选择。</span><span class="sxs-lookup"><span data-stu-id="3378f-118">To use a different cross-company value for another data source, delete the corresponding user-specific selection.</span></span>

<span data-ttu-id="3378f-119">对于标记为公司间的每个数据源，可通过在 ER 表达式中使用 **FILTER** 和 **WHERE** 函数选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="3378f-119">For every data source that is marked as cross-company, you can select the records that you want by using the **FILTER** and **WHERE** functions in ER expressions.</span></span> <span data-ttu-id="3378f-120">**dataAreaID** 字段也可以用作公司标识符。</span><span class="sxs-lookup"><span data-stu-id="3378f-120">The **dataAreaID** field can also be used as a company identifier.</span></span> <span data-ttu-id="3378f-121">现在如果使用 **FILTER** 函数，则将 **dataAreaID** 字段限制为以下类型的条件：</span><span class="sxs-lookup"><span data-stu-id="3378f-121">Currently, the **dataAreaID** field is limited to the following types of conditions when the **FILTER** function is used:</span></span>

- <span data-ttu-id="3378f-122">仅支持只有一个 **dataAreaID** 字段的条件。</span><span class="sxs-lookup"><span data-stu-id="3378f-122">Only conditions that have a single **dataAreaID** field comparison are supported.</span></span>
- <span data-ttu-id="3378f-123">仅允许具有的表达式不依赖于记录列表项的比较。</span><span class="sxs-lookup"><span data-stu-id="3378f-123">Only comparisons that have expressions that don't depend on records list items are allowed.</span></span>

<span data-ttu-id="3378f-124">因此，以下表达式有效。</span><span class="sxs-lookup"><span data-stu-id="3378f-124">Therefore, the following expression is valid.</span></span>

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

<span data-ttu-id="3378f-125">默认情况下，范围包括当前申请表的所有公司。</span><span class="sxs-lookup"><span data-stu-id="3378f-125">By default, the scope includes all companies of the current application.</span></span> <span data-ttu-id="3378f-126">但是可以进行限制。</span><span class="sxs-lookup"><span data-stu-id="3378f-126">However, it can be restricted.</span></span> <span data-ttu-id="3378f-127">要对单个 ER 格式限制公司间数据访问的范围，请为该格式分配特定组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="3378f-127">To restrict the scope of cross-company data access for a single ER format, assign a specific organization hierarchy to the format.</span></span> <span data-ttu-id="3378f-128">如果为 ER 格式定义层次结构，则仅返回所分配层次结构中存在的法人的记录，即使该格式调用公司间数据源也不例外。</span><span class="sxs-lookup"><span data-stu-id="3378f-128">When a hierarchy is defined for an ER format, only records for legal entities that are presented in the assigned hierarchy are returned, even though the format calls cross-company data sources.</span></span> <span data-ttu-id="3378f-129">如果为 ER 格式定义了对不再存在的层次结构的引用，将应用默认范围，并且该格式将调用公司间数据源。</span><span class="sxs-lookup"><span data-stu-id="3378f-129">When a reference to a hierarchy that no longer exists is defined for an ER format, the default scope is applied, and the format calls cross-company data sources.</span></span> <span data-ttu-id="3378f-130">在此情况下，将返回所有申请公司的记录。</span><span class="sxs-lookup"><span data-stu-id="3378f-130">In this situation, records for all application companies are returned.</span></span>

<span data-ttu-id="3378f-131">请注意，如果为分配给单个 ER 格式的组织层次结构开启 **使用草稿** 选项 ，将使用该层次结构的草稿版本中的法人识别公司间数据源的范围。</span><span class="sxs-lookup"><span data-stu-id="3378f-131">Note that when the **Use draft** option is turned on for the assigned to a single ER format organization hierarchy, the legal entities from the draft version of this hierarchy will be used to identify the scope for cross-company data sources.</span></span> <span data-ttu-id="3378f-132">如果不存在草稿版本，则为其使用该组织层次结构的最近发布版本中的法人。</span><span class="sxs-lookup"><span data-stu-id="3378f-132">If the draft version does not exist, the legal entities from the last published version of this organization hierarchy will be used for this.</span></span>

<span data-ttu-id="3378f-133">请注意，如果为分配给单个 ER 格式的组织层次结构关闭 **使用草稿** 选项 ，将使用该组织层次结构的最近发布版本中的法人识别公司间数据源的范围。</span><span class="sxs-lookup"><span data-stu-id="3378f-133">Note that when the **Use draft** option is turned off for the assigned to a single ER format organization hierarchy, the legal entities from the last published version of this organization hierarchy will be used to identify the scope for cross-company data sources.</span></span> <span data-ttu-id="3378f-134">ER 框架中不支持组织层次结构的日期有效性。</span><span class="sxs-lookup"><span data-stu-id="3378f-134">Date effectiveness of organization hierarchies is not supported yet in the ER framework.</span></span>

<span data-ttu-id="3378f-135">可在可从 ER 工作区访问的特定页中将该层次结构分配给某个格式，或通过使用 **组织管理 -\> 电子申报 -\> 格式的法人筛选器** 菜单项分配。</span><span class="sxs-lookup"><span data-stu-id="3378f-135">The hierarchy can be assigned to a format in a specific page that can be accessed from the ER workspace or by using the **Organization administration \> Electronic reporting \> Legal entity filter for formats** menu item.</span></span> <span data-ttu-id="3378f-136">若要访问该页，必须为用户授予 **维护格式的法人筛选器** 权限 (ERMaintainFormatMappingLegalEntityFilters)。</span><span class="sxs-lookup"><span data-stu-id="3378f-136">To access the page, the **Maintain legal entity filters for format** privilege (ERMaintainFormatMappingLegalEntityFilters) must be granted to a user.</span></span> <span data-ttu-id="3378f-137">除了用户可以在系统查询对话框中手动指定的限制，还将应用格式的基于层次结构的法人的范围限制。</span><span class="sxs-lookup"><span data-stu-id="3378f-137">The scope restriction of hierarchy-based legal entities for the format is applied in addition to the restriction that the user can manually specify in the system query dialog box.</span></span> <span data-ttu-id="3378f-138">运行格式时，将使用这些限制的重合部分。</span><span class="sxs-lookup"><span data-stu-id="3378f-138">The intersection of these restrictions is used when the format is run.</span></span>

<span data-ttu-id="3378f-139">若要了解此功能的详细信息，请播放任务指南 **ER 以公司间模式访问依赖于公司的表的记录**，该任务指南属于 7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程，可从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载。</span><span class="sxs-lookup"><span data-stu-id="3378f-139">To learn more about this feature, play the task guide, **ER Access records of company dependent tables in cross-company mode**, which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process, and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="3378f-140">此任务指南将引导您完成配置 ER 模型映射和 ER 格式以便以公司间模式访问申请表这一过程。</span><span class="sxs-lookup"><span data-stu-id="3378f-140">This task guide walks you through the process of configuring an ER model mapping and ER format to access application tables in cross-company mode.</span></span>

<span data-ttu-id="3378f-141">请下载以下文件以完成本任务指南：</span><span class="sxs-lookup"><span data-stu-id="3378f-141">Download the following files to complete the task guide:</span></span>

- [<span data-ttu-id="3378f-142">ER 模型配置 - CrossCompanyDataAccessModel.xml</span><span class="sxs-lookup"><span data-stu-id="3378f-142">ER model configuration - CrossCompanyDataAccessModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="3378f-143">ER 格式配置 - CrossCompanyDataAccessFormat.xml</span><span class="sxs-lookup"><span data-stu-id="3378f-143">ER format configuration - CrossCompanyDataAccessFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
