---
title: 配置键和数据实体
description: 此主题介绍配置键和数据实体之间的关系。
author: Sunil-Garg
manager: AnnBe
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: b951c1da298689ea82f8c0abb868bea7c8c22487
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182063"
---
# <a name="configuration-keys-and-data-entities"></a><span data-ttu-id="80f41-103">Configuration Key 和数据实体</span><span class="sxs-lookup"><span data-stu-id="80f41-103">Configuration keys and data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80f41-104">使用数据实体导入或导出数据之前，建议首先确定配置键对要使用的数据实体的影响。</span><span class="sxs-lookup"><span data-stu-id="80f41-104">Before you use data entities to import or export data, we recommended that you first determine the impact of configuration keys on the data entities that you are planning to use.</span></span>

<span data-ttu-id="80f41-105">若要了解有关配置键的详细信息，请参阅[许可证代码和配置键报告](../sysadmin/license-codes-configuration-keys-report.md)。</span><span class="sxs-lookup"><span data-stu-id="80f41-105">To learn more about configuration keys, see the [License codes and configuration keys report](../sysadmin/license-codes-configuration-keys-report.md).</span></span>

### <a name="configuration-key-assignments"></a><span data-ttu-id="80f41-106">指定配置键</span><span class="sxs-lookup"><span data-stu-id="80f41-106">Configuration key assignments</span></span>
<span data-ttu-id="80f41-107">可以为下面的一种或全部项目指定配置键。</span><span class="sxs-lookup"><span data-stu-id="80f41-107">Configuration keys can be assigned to one or all of the following artifacts.</span></span>

- <span data-ttu-id="80f41-108">数据实体</span><span class="sxs-lookup"><span data-stu-id="80f41-108">Data entities</span></span>
- <span data-ttu-id="80f41-109">用作数据源的表</span><span class="sxs-lookup"><span data-stu-id="80f41-109">Tables used as data sources</span></span>
- <span data-ttu-id="80f41-110">表字段</span><span class="sxs-lookup"><span data-stu-id="80f41-110">Table fields</span></span>
- <span data-ttu-id="80f41-111">数据实体字段</span><span class="sxs-lookup"><span data-stu-id="80f41-111">Data entity fields</span></span>

<span data-ttu-id="80f41-112">下表汇总介绍构成对象的不同项目的配置键值如何更改对象的预期行为。</span><span class="sxs-lookup"><span data-stu-id="80f41-112">The following table summarizes how configuration key values on the different artifacts that underlie an object change the expected behavior of the object.</span></span>

| <span data-ttu-id="80f41-113">数据实体的配置键设置</span><span class="sxs-lookup"><span data-stu-id="80f41-113">Configuration key setting on data entity</span></span> | <span data-ttu-id="80f41-114">表的配置键设置</span><span class="sxs-lookup"><span data-stu-id="80f41-114">Configuration key setting on table</span></span> | <span data-ttu-id="80f41-115">表字段的配置键设置</span><span class="sxs-lookup"><span data-stu-id="80f41-115">Configuration key setting on table field</span></span> | <span data-ttu-id="80f41-116">数据实体字段的配置键设置</span><span class="sxs-lookup"><span data-stu-id="80f41-116">Configuration key on data entity field</span></span> | <span data-ttu-id="80f41-117">预期行为</span><span class="sxs-lookup"><span data-stu-id="80f41-117">Expected behavior</span></span> |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| <span data-ttu-id="80f41-118">已禁用</span><span class="sxs-lookup"><span data-stu-id="80f41-118">Disabled</span></span>                                | <span data-ttu-id="80f41-119">不评估</span><span class="sxs-lookup"><span data-stu-id="80f41-119">Not evaluated</span></span>                      | <span data-ttu-id="80f41-120">不评估</span><span class="sxs-lookup"><span data-stu-id="80f41-120">Not evaluated</span></span>                            | <span data-ttu-id="80f41-121">不评估</span><span class="sxs-lookup"><span data-stu-id="80f41-121">Not evaluated</span></span>                          | <span data-ttu-id="80f41-122">如果禁用数据实体的配置键，数据实体将不起作用。</span><span class="sxs-lookup"><span data-stu-id="80f41-122">If the configuration key for the data entity is disabled, the data entity will not be functional.</span></span> <span data-ttu-id="80f41-123">启用还是禁用基础表和字段中的配置键无关紧要。</span><span class="sxs-lookup"><span data-stu-id="80f41-123">It does not matter whether the configuration keys in the underlying tables and fields are enabled or disabled.</span></span> |
| <span data-ttu-id="80f41-124">已启用</span><span class="sxs-lookup"><span data-stu-id="80f41-124">Enabled</span></span>                                 | <span data-ttu-id="80f41-125">已禁用</span><span class="sxs-lookup"><span data-stu-id="80f41-125">Disabled</span></span>                           | <span data-ttu-id="80f41-126">不评估</span><span class="sxs-lookup"><span data-stu-id="80f41-126">Not evaluated</span></span>                            | <span data-ttu-id="80f41-127">不评估</span><span class="sxs-lookup"><span data-stu-id="80f41-127">Not evaluated</span></span>                          | <span data-ttu-id="80f41-128">如果启用数据实体的配置键，数据管理框架将检查各个基础表中的配置键。</span><span class="sxs-lookup"><span data-stu-id="80f41-128">If the configuration key for a data entity is enabled, the data management framework checks the configuration key on each of the underlying tables.</span></span> <span data-ttu-id="80f41-129">如果禁用表的配置键，该表在数据实体中将不可用于功能性使用。</span><span class="sxs-lookup"><span data-stu-id="80f41-129">If the configuration key for a table is disabled, that table will not be available in the data entity for functional use.</span></span> <span data-ttu-id="80f41-130">如果禁用表的配置键，将不评估表和数据实体配置键设置。</span><span class="sxs-lookup"><span data-stu-id="80f41-130">If a table's configuration key is disabled, the table and data entity configuration key settings are not evaluated.</span></span> <span data-ttu-id="80f41-131">如果实体中的主表已禁用其配置键，系统将视为已禁用实体的配置键。</span><span class="sxs-lookup"><span data-stu-id="80f41-131">If the primary table in the entity has its configuration key disabled, then the system will act as though the entity's configuration key were disabled.</span></span> |
| <span data-ttu-id="80f41-132">已启用</span><span class="sxs-lookup"><span data-stu-id="80f41-132">Enabled</span></span>                                 | <span data-ttu-id="80f41-133">已启用</span><span class="sxs-lookup"><span data-stu-id="80f41-133">Enabled</span></span>                            | <span data-ttu-id="80f41-134">已禁用</span><span class="sxs-lookup"><span data-stu-id="80f41-134">Disabled</span></span>                                 | <span data-ttu-id="80f41-135">不评估</span><span class="sxs-lookup"><span data-stu-id="80f41-135">Not evaluated</span></span>                          | <span data-ttu-id="80f41-136">如果启用数据实体的配置键，并且启用基础表配置键，数据管理框架将检查表中字段的配置键。</span><span class="sxs-lookup"><span data-stu-id="80f41-136">If the configuration key for a data entity is enabled, and the underlying tables configuration keys are enabled, the data management framework will check the configuration key on of the fields in the tables.</span></span> <span data-ttu-id="80f41-137">如果禁用字段的配置键，即使响应数据实体字段已启用了配置键，该字段在数据实体中也不可用于功能性使用。</span><span class="sxs-lookup"><span data-stu-id="80f41-137">If the configuration key for a field is disabled, that field will not be available in the data entity for functional use even if the corresponding data entity field has the configuration key enabled.</span></span> |
| <span data-ttu-id="80f41-138">已启用</span><span class="sxs-lookup"><span data-stu-id="80f41-138">Enabled</span></span>                                 | <span data-ttu-id="80f41-139">已启用</span><span class="sxs-lookup"><span data-stu-id="80f41-139">Enabled</span></span>                            | <span data-ttu-id="80f41-140">已启用</span><span class="sxs-lookup"><span data-stu-id="80f41-140">Enabled</span></span>                                  | <span data-ttu-id="80f41-141">已禁用</span><span class="sxs-lookup"><span data-stu-id="80f41-141">Disabled</span></span>                               | <span data-ttu-id="80f41-142">如果在其他所有级别中启用配置键，但是未启用实体字段配置键，该字段在数据实体中将不可用。</span><span class="sxs-lookup"><span data-stu-id="80f41-142">If the configuration key is enabled at all other levels, but the entity field configuration key is not enabled, then the field will not be available for use in the data entity.</span></span> |

> [!NOTE]
> <span data-ttu-id="80f41-143">如果一个实体将另一个实体用作数据源，将以递归方式应用上述语义。</span><span class="sxs-lookup"><span data-stu-id="80f41-143">If an entity has another entity as a data source then, the above semantics are applied in a recursive manner.</span></span>

### <a name="entity-list-refresh"></a><span data-ttu-id="80f41-144">刷新实体列表</span><span class="sxs-lookup"><span data-stu-id="80f41-144">Entity list refresh</span></span>
<span data-ttu-id="80f41-145">刷新实体列表时，数据管理框架构建配置键元数据供运行时使用。</span><span class="sxs-lookup"><span data-stu-id="80f41-145">When the entity list is refreshed, the data management framework builds the configuration key metadata for runtime use.</span></span> <span data-ttu-id="80f41-146">此元数据使用上面介绍的逻辑构建。</span><span class="sxs-lookup"><span data-stu-id="80f41-146">This metadata is built using the logic described above.</span></span> <span data-ttu-id="80f41-147">我们强烈建议先等待实体列表刷新完毕，再使用数据管理框架中的作业和实体。</span><span class="sxs-lookup"><span data-stu-id="80f41-147">We strongly recommend that you wait for the entity list refresh to complete before using jobs and entities in the data management framework.</span></span> <span data-ttu-id="80f41-148">如果不等待，配置键元数据可能不是最新的，从而导致意外结果。</span><span class="sxs-lookup"><span data-stu-id="80f41-148">If you don't wait, the configuration key metadata may not be up to date and could result in unexpected outcomes.</span></span> <span data-ttu-id="80f41-149">刷新实体列表时，实体列表页面中将显示以下消息。</span><span class="sxs-lookup"><span data-stu-id="80f41-149">When the entity list is being refreshed, the following message is shown in the entity list page.</span></span>

![刷新实体列表](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a><span data-ttu-id="80f41-151">数据实体列表页面</span><span class="sxs-lookup"><span data-stu-id="80f41-151">Data entity list page</span></span>
<span data-ttu-id="80f41-152">“数据管理”工作区中的数据实体列表页面显示实体的配置键设置。</span><span class="sxs-lookup"><span data-stu-id="80f41-152">The data entity list page in the Data management workspace shows the configuration key settings for the entities.</span></span> <span data-ttu-id="80f41-153">请从该页面开始了解配置键对数据实体的影响。</span><span class="sxs-lookup"><span data-stu-id="80f41-153">Start from this page to understand the impact from configuration keys on the data entity.</span></span>

<span data-ttu-id="80f41-154">此信息使用实体刷新期间构建的元数据显示。</span><span class="sxs-lookup"><span data-stu-id="80f41-154">This information is shown using the metadata that is built during entity refresh.</span></span> <span data-ttu-id="80f41-155">配置键列显示与数据实体关联的配置键的名称。</span><span class="sxs-lookup"><span data-stu-id="80f41-155">The configuration key column shows the name of the configuration key that is associated with the data entity.</span></span> <span data-ttu-id="80f41-156">如果此列为空，说明没有配置键与数据实体关联。</span><span class="sxs-lookup"><span data-stu-id="80f41-156">If this column is blank it means that there is no configuration key associated with the data entity.</span></span> <span data-ttu-id="80f41-157">配置键状态列显示配置键的状态。</span><span class="sxs-lookup"><span data-stu-id="80f41-157">The configuration key status column shows the state of the configuration key.</span></span> <span data-ttu-id="80f41-158">如果它有选中标记，说明已启用该键。</span><span class="sxs-lookup"><span data-stu-id="80f41-158">If it has a checkmark, it means the key is enabled.</span></span> <span data-ttu-id="80f41-159">如果为空，说明已禁用该键或没有关联的键。</span><span class="sxs-lookup"><span data-stu-id="80f41-159">If it is blank, it means either the key is disabled or there is no key associated.</span></span>

![实体列表页面](./media/Data_entity_list_page.png)

### <a name="target-fields"></a><span data-ttu-id="80f41-161">目标字段</span><span class="sxs-lookup"><span data-stu-id="80f41-161">Target fields</span></span>
<span data-ttu-id="80f41-162">下一步是钻取到数据实体中以查看配置键对表和字段的影响。</span><span class="sxs-lookup"><span data-stu-id="80f41-162">The next step is to drill into the data entity to view the impact of configuration keys on tables and fields.</span></span> <span data-ttu-id="80f41-163">数据实体的目标字段窗体显示数据实体中的相关表和字段的配置键和键状态信息。</span><span class="sxs-lookup"><span data-stu-id="80f41-163">The target fields form for a data entity shows configuration key and the key status information for the related tables and fields in the data entity.</span></span> <span data-ttu-id="80f41-164">如果数据实体本身已禁用其配置键，将显示一条警告消息，说明无论实体的配置键为哪种状态，该实体的目标字段窗体中的表和字段都将不可用。</span><span class="sxs-lookup"><span data-stu-id="80f41-164">If the data entity itself has its configuration key disabled, a warning message is shown informing that the tables and fields in the target fields form for this entity will not be available at all regardless of their configuration key status.</span></span>

![目标字段](./media/Target_fields_1.png)

### <a name="child-entities"></a><span data-ttu-id="80f41-166">子实体</span><span class="sxs-lookup"><span data-stu-id="80f41-166">Child entities</span></span> 
<span data-ttu-id="80f41-167">某些实体将其他实体用作数据库，或为复合数据实体：将在子实体窗体中显示这些实体的配置键信息。</span><span class="sxs-lookup"><span data-stu-id="80f41-167">Certain entities have other entities as data sources, or are composite data entities: configuration key information for these entities is shown in the Child entities form.</span></span> <span data-ttu-id="80f41-168">此窗体的使用方法类似上面介绍的实体列表页面。</span><span class="sxs-lookup"><span data-stu-id="80f41-168">Use this form in the similar way to the entities list page described above.</span></span> <span data-ttu-id="80f41-169">子实体的目标字段窗体的行为也类似上面介绍的行为。</span><span class="sxs-lookup"><span data-stu-id="80f41-169">The target fields form for the child entity also behaves like what is described above.</span></span>

![目标字段](./media/Target_fields_2.png)

### <a name="using-data-entities"></a><span data-ttu-id="80f41-171">使用数据实体</span><span class="sxs-lookup"><span data-stu-id="80f41-171">Using data entities</span></span>
<span data-ttu-id="80f41-172">了解了配置键对要使用的数据实体的全部影响（如果有）之后，现在可继续使用数据实体，方法是将其添加到数据项目。</span><span class="sxs-lookup"><span data-stu-id="80f41-172">After understanding the full impact, if any, of configuration keys on the data entities that you would like to use, you can now proceed to using the data entities by adding them to data projects.</span></span> 

### <a name="run-time-validations-for-configuration-keys"></a><span data-ttu-id="80f41-173">配置键的运行时验证</span><span class="sxs-lookup"><span data-stu-id="80f41-173">Run time validations for configuration keys</span></span>
<span data-ttu-id="80f41-174">以下用例下将使用实体列表刷新期间构建的配置键元数据执行运行时验证。</span><span class="sxs-lookup"><span data-stu-id="80f41-174">Using the configuration key metadata built during entity refresh list, run time validations are performed in the following use cases.</span></span>

- <span data-ttu-id="80f41-175">向作业添加了数据实体时</span><span class="sxs-lookup"><span data-stu-id="80f41-175">When a data entity is added to a job</span></span>
- <span data-ttu-id="80f41-176">用户在实体列表中单击“验证”时</span><span class="sxs-lookup"><span data-stu-id="80f41-176">When user clicks 'validate' on the entity list</span></span>
- <span data-ttu-id="80f41-177">用户将包加载到数据项目中时</span><span class="sxs-lookup"><span data-stu-id="80f41-177">When the user loads a data package into a data project</span></span>
- <span data-ttu-id="80f41-178">用户将模板加载到数据项目中时</span><span class="sxs-lookup"><span data-stu-id="80f41-178">When the user loads a template into a data project</span></span>
- <span data-ttu-id="80f41-179">加载现有数据项目时</span><span class="sxs-lookup"><span data-stu-id="80f41-179">When an existing data project is loaded</span></span>
- <span data-ttu-id="80f41-180">将模板加载到数据项目中时</span><span class="sxs-lookup"><span data-stu-id="80f41-180">When a template is loaded into a data project</span></span>
- <span data-ttu-id="80f41-181">执行导出/导入作业前（批处理、非批处理、重复执行、OData）</span><span class="sxs-lookup"><span data-stu-id="80f41-181">Before the export/import job is executed (batch, non-batch, recurring, OData)</span></span>
- <span data-ttu-id="80f41-182">用户生成映射时</span><span class="sxs-lookup"><span data-stu-id="80f41-182">When the user generates mapping</span></span>
- <span data-ttu-id="80f41-183">用户在映射 UI 中映射字段时</span><span class="sxs-lookup"><span data-stu-id="80f41-183">When the user maps fields in the mapping UI</span></span>
- <span data-ttu-id="80f41-184">用户仅添加“可导入字段”时</span><span class="sxs-lookup"><span data-stu-id="80f41-184">When the user adds only 'importable fields'</span></span>

### <a name="managing-configuration-key-changes"></a><span data-ttu-id="80f41-185">管理配置键更改</span><span class="sxs-lookup"><span data-stu-id="80f41-185">Managing configuration key changes</span></span>
<span data-ttu-id="80f41-186">只要在实体、表或字段级别更新配置键，都必须刷新数据管理框架中的实体列表。</span><span class="sxs-lookup"><span data-stu-id="80f41-186">Anytime that you update configuration keys at the entity, table or field level, the entity list in the data management framework must be refreshed.</span></span> <span data-ttu-id="80f41-187">此流程确保该框架拾取最新的配置键设置。</span><span class="sxs-lookup"><span data-stu-id="80f41-187">This process ensures that the framework picks up the latest configuration key settings.</span></span> <span data-ttu-id="80f41-188">刷新实体列表前，实体列表页面中将显示以下警告。</span><span class="sxs-lookup"><span data-stu-id="80f41-188">Until the entity list is refreshed, the following warning will be shown in the entity list page.</span></span> <span data-ttu-id="80f41-189">刷新实体列表之后，更新后的配置键更改将立即生效。</span><span class="sxs-lookup"><span data-stu-id="80f41-189">The updated configuration key changes will take effect immediately after the entity list is refreshed.</span></span> <span data-ttu-id="80f41-190">建议在配置键更改生效后，验证现有数据对象和作业，以确保其功能正常。</span><span class="sxs-lookup"><span data-stu-id="80f41-190">We recommend that you validate existing data projects and jobs to make sure that they function as expected after the configuration keys changes are put in effect.</span></span>

![目标字段](./media/Target_fields_3.png)
