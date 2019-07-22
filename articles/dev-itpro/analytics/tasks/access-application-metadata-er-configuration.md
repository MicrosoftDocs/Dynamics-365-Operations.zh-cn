---
title: 通过使用 ER 配置访问应用程序元数据
description: 本主题中的步骤介绍 Regulatory Configuration Service (RCS) 用户如何在 Finance and Operations 中通过使用元数据设计新的电子申报 (ER) 模型映射。
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b95b41b27cecd4c71ed7646f329cf5736a01b561
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727021"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="b9261-103">通过使用 ER 配置访问应用程序元数据</span><span class="sxs-lookup"><span data-stu-id="b9261-103">Access application metadata by using ER configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9261-104">以下步骤介绍系统管理员或电子报表开发人员角色的 Regulatory Configuration Service (RCS) 用户如何使用 Dynamics 365 for Finance and Operations 应用程序的元数据设计新的电子报表 (ER) 模型映射。</span><span class="sxs-lookup"><span data-stu-id="b9261-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the metadata of the Dynamics 365 for Finance and Operations application.</span></span> <span data-ttu-id="b9261-105">可访问应用程序元数据，方法是使用其中包含一组示例元数据的 ER 配置访问外贸交易。</span><span class="sxs-lookup"><span data-stu-id="b9261-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="b9261-106">为了完成这些步骤，您必须首先在 RCS 中完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="b9261-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="b9261-107">然后在 Finance and Operations 中完成 [(ER) 在 RCS 中准备要使用的应用程序元数据](prepare-application-metadata-rcs.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="b9261-107">Then, in Finance and Operations, complete the steps in the topic, [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b9261-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="b9261-108">Prerequisites</span></span>
1. <span data-ttu-id="b9261-109">转到**所有工作区** > **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="b9261-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="b9261-110">确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。</span><span class="sxs-lookup"><span data-stu-id="b9261-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="b9261-111">如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="b9261-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="b9261-112">导入元数据配置</span><span class="sxs-lookup"><span data-stu-id="b9261-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="b9261-113">单击**元数据配置**。</span><span class="sxs-lookup"><span data-stu-id="b9261-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="b9261-114">导入包含来自 Finance and Operations 应用程序且为了生成外贸业务所用电子单据而配置的元数据的 ER 元数据配置。</span><span class="sxs-lookup"><span data-stu-id="b9261-114">Import the ER metadata configuration that contains metadata from the Finance and Operations application that is configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="b9261-115">由于已完成了 [(ER) 在 RCS 中准备要使用的应用程序元数据](prepare-application-metadata-rcs.md)过程中的步骤，所以此 ER 元数据配置已导出为 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="b9261-115">This ER metadata configuration has been exported as XML file while the steps in the [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="b9261-116">单击**交换**。</span><span class="sxs-lookup"><span data-stu-id="b9261-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="b9261-117">单击**从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="b9261-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="b9261-118">单击**浏览**并选择“Foreign trade metadata.xml”文件。</span><span class="sxs-lookup"><span data-stu-id="b9261-118">Click **Browse** and select the ‘Foreign trade metadata.xml’ file.</span></span> 
6. <span data-ttu-id="b9261-119">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9261-119">Click **OK**.</span></span> 
7. <span data-ttu-id="b9261-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b9261-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="b9261-121">创建数据模型配置</span><span class="sxs-lookup"><span data-stu-id="b9261-121">Create data model configuration</span></span>
1. <span data-ttu-id="b9261-122">单击**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="b9261-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="b9261-123">单击**创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b9261-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="b9261-124">在**名称**字段中键入“外贸模型”。</span><span class="sxs-lookup"><span data-stu-id="b9261-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="b9261-125">单击**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="b9261-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="b9261-126">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="b9261-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="b9261-127">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="b9261-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="b9261-128">在**名称**字段中，键入“根”。</span><span class="sxs-lookup"><span data-stu-id="b9261-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="b9261-129">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="b9261-129">Click **Add**.</span></span> 
9. <span data-ttu-id="b9261-130">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="b9261-130">Click **New** to open the drop dialog.</span></span> 
10. <span data-ttu-id="b9261-131">在**名称**字段中，键入“交易”。</span><span class="sxs-lookup"><span data-stu-id="b9261-131">In the **Name** field, type 'Transaction'.</span></span> 
11. <span data-ttu-id="b9261-132">在**物料类型**字段中，选择**记录列表**。</span><span class="sxs-lookup"><span data-stu-id="b9261-132">In the **Item type** field, select **Record list**.</span></span> 
12. <span data-ttu-id="b9261-133">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="b9261-133">Click **Add**.</span></span> 
13. <span data-ttu-id="b9261-134">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="b9261-134">Click **New** to open the drop dialog.</span></span> 
14. <span data-ttu-id="b9261-135">在**名称**字段中，键入“商品代码”。</span><span class="sxs-lookup"><span data-stu-id="b9261-135">In the **Name** field, type 'Commodity code'.</span></span> 
15. <span data-ttu-id="b9261-136">在**物料类型**字段中，选择**字符串**。</span><span class="sxs-lookup"><span data-stu-id="b9261-136">In the **Item type** field, select **String**.</span></span> 
16. <span data-ttu-id="b9261-137">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="b9261-137">Click **Add**.</span></span> 
17. <span data-ttu-id="b9261-138">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="b9261-138">Click **New** to open the drop dialog.</span></span> 
18. <span data-ttu-id="b9261-139">在**名称**字段中，键入“开票金额”。</span><span class="sxs-lookup"><span data-stu-id="b9261-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19. <span data-ttu-id="b9261-140">在**物料类型**字段中，选择**实际**。</span><span class="sxs-lookup"><span data-stu-id="b9261-140">In the **Item type** field, select **Real**.</span></span> 
20. <span data-ttu-id="b9261-141">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="b9261-141">Click **Add**.</span></span> 
21. <span data-ttu-id="b9261-142">单击**新建**，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="b9261-142">Click **New** to open the drop dialog.</span></span> 
22. <span data-ttu-id="b9261-143">在**名称**字段中，键入“日期”。</span><span class="sxs-lookup"><span data-stu-id="b9261-143">In the **Name** field, type 'Date'.</span></span> 
23. <span data-ttu-id="b9261-144">在**物料类型**字段中，选择**日期**。</span><span class="sxs-lookup"><span data-stu-id="b9261-144">In the **Item type** field, select **Date**.</span></span> 
24. <span data-ttu-id="b9261-145">单击**添加**。</span><span class="sxs-lookup"><span data-stu-id="b9261-145">Click **Add**.</span></span> 
25. <span data-ttu-id="b9261-146">单击**根引用**。</span><span class="sxs-lookup"><span data-stu-id="b9261-146">Click **Root reference**.</span></span> 
26. <span data-ttu-id="b9261-147">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9261-147">Click **OK**.</span></span> 
27. <span data-ttu-id="b9261-148">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="b9261-148">Click **Save**.</span></span> 
28. <span data-ttu-id="b9261-149">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b9261-149">Close the page.</span></span> 
29. <span data-ttu-id="b9261-150">单击**更改状态**。</span><span class="sxs-lookup"><span data-stu-id="b9261-150">Click **Change status**.</span></span> 
30. <span data-ttu-id="b9261-151">单击**完成**。</span><span class="sxs-lookup"><span data-stu-id="b9261-151">Click **Complete**.</span></span> 
31. <span data-ttu-id="b9261-152">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9261-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="b9261-153">创建模型映射配置</span><span class="sxs-lookup"><span data-stu-id="b9261-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="b9261-154">单击**创建配置**，以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="b9261-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="b9261-155">在**新建**字段中，输入“基于数据模型‘外贸模型’的模型映射”。</span><span class="sxs-lookup"><span data-stu-id="b9261-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="b9261-156">在**名称**字段中键入“外贸映射”。</span><span class="sxs-lookup"><span data-stu-id="b9261-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="b9261-157">单击**创建配置**。</span><span class="sxs-lookup"><span data-stu-id="b9261-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="b9261-158">展开**先决条件**部分。</span><span class="sxs-lookup"><span data-stu-id="b9261-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="b9261-159">单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="b9261-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="b9261-160">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="b9261-160">Click **New**.</span></span> 
8. <span data-ttu-id="b9261-161">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="b9261-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="b9261-162">在**先决条件组件类型**字段中，选择**配置**。</span><span class="sxs-lookup"><span data-stu-id="b9261-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10. <span data-ttu-id="b9261-163">选择**外贸元数据**配置。</span><span class="sxs-lookup"><span data-stu-id="b9261-163">Select **Foreign trade metadata** configuration.</span></span> 
11. <span data-ttu-id="b9261-164">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="b9261-164">Click **Save**.</span></span> 
12. <span data-ttu-id="b9261-165">已添加了对“外贸元数据”配置版本 1 的引用。</span><span class="sxs-lookup"><span data-stu-id="b9261-165">We added the reference to the version 1 of the ‘Foreign trade metadata’ configuration.</span></span> <span data-ttu-id="b9261-166">设计此模型映射时，将提供来自此配置的应用程序元数据。</span><span class="sxs-lookup"><span data-stu-id="b9261-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13. <span data-ttu-id="b9261-167">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b9261-167">Close the page.</span></span> 
14. <span data-ttu-id="b9261-168">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="b9261-168">Click **Designer**.</span></span> 
15. <span data-ttu-id="b9261-169">单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="b9261-169">Click **Designer**.</span></span> 
16. <span data-ttu-id="b9261-170">在树中，选择 **Dynamics 365 for Operations\表记录**。</span><span class="sxs-lookup"><span data-stu-id="b9261-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17. <span data-ttu-id="b9261-171">单击**添加根**。</span><span class="sxs-lookup"><span data-stu-id="b9261-171">Click **Add root**.</span></span> 
18. <span data-ttu-id="b9261-172">在**名称**字段中，键入“内部统计”。</span><span class="sxs-lookup"><span data-stu-id="b9261-172">In the **Name** field, type 'Intrastat'.</span></span> 
19. <span data-ttu-id="b9261-173">选择**内部统计**表记录。</span><span class="sxs-lookup"><span data-stu-id="b9261-173">Select **Intrastat** table records.</span></span> 
20. <span data-ttu-id="b9261-174">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9261-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="b9261-175">仅提供了 2 个表，因为仅向当前正在使用的元数据集添加了 2 个表。</span><span class="sxs-lookup"><span data-stu-id="b9261-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21. <span data-ttu-id="b9261-176">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="b9261-176">Click **Bind**.</span></span> 
22. <span data-ttu-id="b9261-177">在树中，展开**内部统计**。</span><span class="sxs-lookup"><span data-stu-id="b9261-177">In the tree, expand **Intrastat**.</span></span> 
23. <span data-ttu-id="b9261-178">在树中，选择**内部统计\AmountMST**。</span><span class="sxs-lookup"><span data-stu-id="b9261-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24. <span data-ttu-id="b9261-179">在树中，展开**交易 = 内部统计**。</span><span class="sxs-lookup"><span data-stu-id="b9261-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25. <span data-ttu-id="b9261-180">在树中，选择**交易 = 内部统计\开票金额**。</span><span class="sxs-lookup"><span data-stu-id="b9261-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26. <span data-ttu-id="b9261-181">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="b9261-181">Click **Bind**.</span></span> 
27. <span data-ttu-id="b9261-182">在树中，选择**内部统计\TransDate**。</span><span class="sxs-lookup"><span data-stu-id="b9261-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28. <span data-ttu-id="b9261-183">在树中，选择**交易 = 内部统计\日期**。</span><span class="sxs-lookup"><span data-stu-id="b9261-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29. <span data-ttu-id="b9261-184">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="b9261-184">Click **Bind**.</span></span> 
30. <span data-ttu-id="b9261-185">在树中，展开**内部统计\>关系**。</span><span class="sxs-lookup"><span data-stu-id="b9261-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31. <span data-ttu-id="b9261-186">在树中，展开**内部统计\>关系\IntrastatCommodity**。</span><span class="sxs-lookup"><span data-stu-id="b9261-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32. <span data-ttu-id="b9261-187">在树中，选择**内部统计\>关系\IntrastatCommodity\代码**。</span><span class="sxs-lookup"><span data-stu-id="b9261-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33. <span data-ttu-id="b9261-188">在树中，选择**交易 = 内部统计\商品代码**。</span><span class="sxs-lookup"><span data-stu-id="b9261-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34. <span data-ttu-id="b9261-189">单击**绑定**。</span><span class="sxs-lookup"><span data-stu-id="b9261-189">Click **Bind**.</span></span> 
35. <span data-ttu-id="b9261-190">单击**验证**。</span><span class="sxs-lookup"><span data-stu-id="b9261-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="b9261-191">我们已使用来自引用的 ER 元数据配置的应用程序元数据详细信息成功绑定了带有介绍的数据源项的数据模型的元素。</span><span class="sxs-lookup"><span data-stu-id="b9261-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36. <span data-ttu-id="b9261-192">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="b9261-192">Click **Save**.</span></span> 
37. <span data-ttu-id="b9261-193">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b9261-193">Close the page.</span></span> 
38. <span data-ttu-id="b9261-194">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="b9261-194">Close the page.</span></span> 
39. <span data-ttu-id="b9261-195">如果需要扩展现有元数据集，请在 Finance and Operations 中操作。</span><span class="sxs-lookup"><span data-stu-id="b9261-195">When you need to extend the existing set of metadata, you can do it in Finance and Operations.</span></span> <span data-ttu-id="b9261-196">然后就可以从 Finance and Operations 中导出新的 ER 元数据配置已完成版本，导入到 RCS 中，然后更新引用新的所导入元数据配置版本的所配置模型映射配置的必备条件。</span><span class="sxs-lookup"><span data-stu-id="b9261-196">Then you can export the new completed version of ER metadata configuration from Finance and Operation,s import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b9261-197">本地部署的应用程序（此时对 Dynamics 365 for Finance and Operations 使用本地业务数据 (LBD) 或本地部署的部署模型）只能使用这种方法获取有关应用程序元数据的信息。</span><span class="sxs-lookup"><span data-stu-id="b9261-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used for Dynamics 365 for Finance and Operations).</span></span>
        
