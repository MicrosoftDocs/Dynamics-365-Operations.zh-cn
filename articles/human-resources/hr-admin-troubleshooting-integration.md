---
title: 与 Finance 集成的常见问题
description: 本文说明在 Human Resources 和 Finance 集成中要同步哪些数据。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b9cfc0964a532cd32dda029419c892fa8ae55e02
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008191"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="32530-103">与 Finance 集成的常见问题</span><span class="sxs-lookup"><span data-stu-id="32530-103">Integration with Finance FAQ</span></span>

<span data-ttu-id="32530-104">此主题回答有关在 Dynamics 365 Human Resources 与 Dynamics 365 Finance 集成时同步的数据的常见问题。</span><span class="sxs-lookup"><span data-stu-id="32530-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="32530-105">所有数据均同步还是只是一些数据实体？</span><span class="sxs-lookup"><span data-stu-id="32530-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="32530-106">将同步一部分数据。</span><span class="sxs-lookup"><span data-stu-id="32530-106">A subset of the data is synchronized.</span></span> <span data-ttu-id="32530-107">有关所有实体的列表，请参阅[与 Dynamics 365 Finance 的集成](hr-admin-integration-finance.md)。</span><span class="sxs-lookup"><span data-stu-id="32530-107">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a><span data-ttu-id="32530-108">为什么我看不到任何数据同步到 Common Data Service？</span><span class="sxs-lookup"><span data-stu-id="32530-108">Why don't I see any data synced to Common Data Service?</span></span>

<span data-ttu-id="32530-109">默认情况下，Common Data Service 集成在不包含提供的演示数据的新环境中处于关闭状态。</span><span class="sxs-lookup"><span data-stu-id="32530-109">By default, the Common Data Service integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="32530-110">默认情况下，在包含演示数据的新环境中将其打开，并且在设置环境后即开始数据同步。</span><span class="sxs-lookup"><span data-stu-id="32530-110">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="32530-111">环境准备好可以同步数据后，可以打开集成。</span><span class="sxs-lookup"><span data-stu-id="32530-111">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="32530-112">有关详细信息，请参阅[配置 Common Data Service 集成](hr-admin-integration-common-data-service.md)。</span><span class="sxs-lookup"><span data-stu-id="32530-112">For more information, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="32530-113">我可以不使用模板创建新映射吗？</span><span class="sxs-lookup"><span data-stu-id="32530-113">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="32530-114">模板是起点。</span><span class="sxs-lookup"><span data-stu-id="32530-114">Templates are the starting point.</span></span> <span data-ttu-id="32530-115">您可以创建自己的模板，但在创建集成项目时始终需要模板。</span><span class="sxs-lookup"><span data-stu-id="32530-115">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="32530-116">有关数据集成器 (DI)、模板和项目的详细信息，请参阅[将数据集成到 Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)。</span><span class="sxs-lookup"><span data-stu-id="32530-116">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="32530-117">我可以映射在 Human Resources 和 Finance 之间转移的财务维度吗？</span><span class="sxs-lookup"><span data-stu-id="32530-117">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="32530-118">Financial dimensions 当前不在 Common Data Service 中，因此不是默认模板的一部分。</span><span class="sxs-lookup"><span data-stu-id="32530-118">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="32530-119">此实体已计划，但当前未确定发布时间。</span><span class="sxs-lookup"><span data-stu-id="32530-119">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="32530-120">对于位于 Finance 但不存在于 Human Resources 中的数据，请使用 Human Resources 中的**配置链接**将两个系统链接在一起。</span><span class="sxs-lookup"><span data-stu-id="32530-120">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![映射财务维度](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="32530-122">在某些情况下，当我导入员工时，他们在 Finance 中成为空闲工作人员。</span><span class="sxs-lookup"><span data-stu-id="32530-122">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="32530-123">为什么？</span><span class="sxs-lookup"><span data-stu-id="32530-123">Why?</span></span>

<span data-ttu-id="32530-124">如果员工在 Human Resources 中没有活动雇用详细信息记录，您可能收到此错误。</span><span class="sxs-lookup"><span data-stu-id="32530-124">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="32530-125">若要解决此问题，请转到**人员管理 \> 员工 \> 雇佣历史记录 \> 日期管理器**，验证是否有活动雇用详细信息记录。</span><span class="sxs-lookup"><span data-stu-id="32530-125">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="32530-126">如果我选择仅映射一部分字段，对非映射字段所做的更改是否会触发同步？</span><span class="sxs-lookup"><span data-stu-id="32530-126">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="32530-127">数据同步按照执行计划进行。</span><span class="sxs-lookup"><span data-stu-id="32530-127">Data sync follows the execution schedule.</span></span> <span data-ttu-id="32530-128">集成将在记录中的任意字段更改时提取该记录，不论字段是否是集成映射的一部分。</span><span class="sxs-lookup"><span data-stu-id="32530-128">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="32530-129">我如何仅发送有效工作人员的更改而不发送已离职的记录？</span><span class="sxs-lookup"><span data-stu-id="32530-129">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="32530-130">使用“高级查询”，您可以在将数据传递到目标前筛选并改造源数据。</span><span class="sxs-lookup"><span data-stu-id="32530-130">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![可用工作人员高级查询](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="32530-132">我可以指定将特定实体的哪些字段发送到 Finance 吗？</span><span class="sxs-lookup"><span data-stu-id="32530-132">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="32530-133">字段可以在集成任务中添加或删除。</span><span class="sxs-lookup"><span data-stu-id="32530-133">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="32530-134">并非 Common Data Service 实体上存在的所有数据字段都从 Human Resources 填充。</span><span class="sxs-lookup"><span data-stu-id="32530-134">Not all data fields that exist on the Common Data Service entity will be populated from Human Resources.</span></span>
<span data-ttu-id="32530-135">附加数据可以通过 Power Apps 填充。</span><span class="sxs-lookup"><span data-stu-id="32530-135">Additional data can be populated via Power Apps.</span></span>

![在集成任务中添加或删除字段](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="32530-137">我将集成设置为批处理作业，但 Human Resources 失去了与目标系统的连接。</span><span class="sxs-lookup"><span data-stu-id="32530-137">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="32530-138">我如何将同一组更改发送到目标系统？</span><span class="sxs-lookup"><span data-stu-id="32530-138">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="32530-139">异常处理不需要特殊设置。</span><span class="sxs-lookup"><span data-stu-id="32530-139">No special setup is required for exception handling.</span></span> <span data-ttu-id="32530-140">数据集成器将自动捕获和报告在源和目标发生的错误，并允许手动重试。</span><span class="sxs-lookup"><span data-stu-id="32530-140">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="32530-141">但是，它不允许手动数据更正。</span><span class="sxs-lookup"><span data-stu-id="32530-141">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="32530-142">如果需要更新数据，这应在源或目标发生。</span><span class="sxs-lookup"><span data-stu-id="32530-142">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="32530-143">我可以设置双向集成吗？</span><span class="sxs-lookup"><span data-stu-id="32530-143">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="32530-144">否，目前集成是单向的（Human Resources 到 Finance and Operations）。</span><span class="sxs-lookup"><span data-stu-id="32530-144">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="32530-145">不过，提供了默认模板将数据从 Human Resources 发送到 Finance。</span><span class="sxs-lookup"><span data-stu-id="32530-145">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="32530-146">我在集成时可以允许删除记录吗？</span><span class="sxs-lookup"><span data-stu-id="32530-146">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="32530-147">否，数据集成器不会捕获已删除的数据传输记录。</span><span class="sxs-lookup"><span data-stu-id="32530-147">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="32530-148">目前仅包括数据创建和更新 (UPSERT)。</span><span class="sxs-lookup"><span data-stu-id="32530-148">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="32530-149">我可以重新运行出错的执行吗？</span><span class="sxs-lookup"><span data-stu-id="32530-149">Can I rerun the errored execution?</span></span> <span data-ttu-id="32530-150">如果可以，是发送完整文件还是仅更改部分？</span><span class="sxs-lookup"><span data-stu-id="32530-150">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="32530-151">数据集成器的首次运行始终是完整运行。</span><span class="sxs-lookup"><span data-stu-id="32530-151">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="32530-152">后续运行基于更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="32530-152">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="32530-153">在错误运行执行时，它会提取运行作用域内的记录并发出 Common Data Service 中的最近更改。</span><span class="sxs-lookup"><span data-stu-id="32530-153">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="32530-154">当我保存项目时，发生错误：“项目存在映射错误”。</span><span class="sxs-lookup"><span data-stu-id="32530-154">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="32530-155">我该做什么？</span><span class="sxs-lookup"><span data-stu-id="32530-155">What do I do?</span></span>

<span data-ttu-id="32530-156">检查您的集成密钥的设置，对设置进行任何所需的更改，然后刷新项目中的实体。</span><span class="sxs-lookup"><span data-stu-id="32530-156">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="32530-157">在使用默认模板时，集成密钥将自动导入。</span><span class="sxs-lookup"><span data-stu-id="32530-157">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="32530-158">在新任务添加到现有模板时，可能发生此问题。</span><span class="sxs-lookup"><span data-stu-id="32530-158">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="32530-159">如果我有 N 个工作人员有雇用关系的法人，我是否需要为每个法人创建映射？</span><span class="sxs-lookup"><span data-stu-id="32530-159">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="32530-160">是，对于 Finance 中的每个法人，您需要在数据集成中有单独的集成项目。</span><span class="sxs-lookup"><span data-stu-id="32530-160">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="32530-161">我需要转移不是 Microsoft 提供的默认模板一部分的数据。</span><span class="sxs-lookup"><span data-stu-id="32530-161">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="32530-162">我可以这样做吗？</span><span class="sxs-lookup"><span data-stu-id="32530-162">Can I do this?</span></span>

<span data-ttu-id="32530-163">可以，字段可以在现有模板中添加或删除。</span><span class="sxs-lookup"><span data-stu-id="32530-163">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="32530-164">模板可以修改成包括其他 Common Data Service 实体中的其他数据。</span><span class="sxs-lookup"><span data-stu-id="32530-164">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="32530-165">实体必须在 Common Data Service 中才能够包含在模板中。</span><span class="sxs-lookup"><span data-stu-id="32530-165">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="32530-166">我只是创建了新的 Finance 和 Human Resources 环境，但发生错误“数据值违反了完整性约束”。</span><span class="sxs-lookup"><span data-stu-id="32530-166">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="32530-167">为什么？</span><span class="sxs-lookup"><span data-stu-id="32530-167">Why?</span></span>

<span data-ttu-id="32530-168">此错误的原因可能包括：</span><span class="sxs-lookup"><span data-stu-id="32530-168">Reasons for this error can include:</span></span>

- <span data-ttu-id="32530-169">数据转移导致源 (Common Data Service) 发生了重复的记录提取。</span><span class="sxs-lookup"><span data-stu-id="32530-169">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="32530-170">数据转移在 Finance and Operations 中必填的字段中包含空值。</span><span class="sxs-lookup"><span data-stu-id="32530-170">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="32530-171">验证 Common Data Service 中的数据以及是否满足 Finance and Operations 的要求。</span><span class="sxs-lookup"><span data-stu-id="32530-171">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="32530-172">如果存在执行错误，并且员工 ID 未同步，我如何找到具有失败员工记录的历史作业？</span><span class="sxs-lookup"><span data-stu-id="32530-172">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="32530-173">数据集成器将在 Finance 中创建多个项目。</span><span class="sxs-lookup"><span data-stu-id="32530-173">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="32530-174">数据集成器任务与 Finance 项目之间的关系是一对一。</span><span class="sxs-lookup"><span data-stu-id="32530-174">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="32530-175">跟踪 Finance 中数据集成器执行历史记录的时间并查找索引 -1 项目。</span><span class="sxs-lookup"><span data-stu-id="32530-175">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="32530-176">如果任务编号在数据集成器中是 9，索引在 Finance 中则是 8。</span><span class="sxs-lookup"><span data-stu-id="32530-176">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="32530-177">从数据集成器捕获任务索引（在本示例中是“9”）。</span><span class="sxs-lookup"><span data-stu-id="32530-177">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![从数据集成器捕获任务索引](media/CaptureTaskIndex.png)

2. <span data-ttu-id="32530-179">跟踪项目的执行时间。</span><span class="sxs-lookup"><span data-stu-id="32530-179">Track the execution time of the project.</span></span>

    ![跟踪项目的执行时间](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="32530-181">在 Finance 中，识别索引 - 1。</span><span class="sxs-lookup"><span data-stu-id="32530-181">In Finance, identify index - 1.</span></span> <span data-ttu-id="32530-182">在此示例中，后缀为“8”的项目和索引“0”项目的执行时间与步骤 2 中的执行时间匹配。</span><span class="sxs-lookup"><span data-stu-id="32530-182">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![标识索引。](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="32530-184">集成 Human Resources 和 Finance 之后，我在 Finance 中看不到我的 Human Resources 数据。</span><span class="sxs-lookup"><span data-stu-id="32530-184">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="32530-185">我该做什么？</span><span class="sxs-lookup"><span data-stu-id="32530-185">What do I do?</span></span>

<span data-ttu-id="32530-186">与 Finance 的集成是一个两步流程。</span><span class="sxs-lookup"><span data-stu-id="32530-186">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="32530-187">首先，验证 Human Resources 数据在 Common Data Service 中已更新并可用。</span><span class="sxs-lookup"><span data-stu-id="32530-187">First, verify that the Human Resources data is updated and available in Common Data Service.</span></span> <span data-ttu-id="32530-188">这是一个接近实时的同步，可以在 Power Apps 中通过查看数据实体中的数据验证。</span><span class="sxs-lookup"><span data-stu-id="32530-188">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data entities.</span></span>

![Common Data Service 中的数据](media/DataInCDS.png)

<span data-ttu-id="32530-190">如果数据未按预期出现在 Common Data Service 中，请验证集成中是否支持该实体。</span><span class="sxs-lookup"><span data-stu-id="32530-190">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="32530-191">若要在 Common Data Service 中包括附加数据，需要 Microsoft 一端进行更改。</span><span class="sxs-lookup"><span data-stu-id="32530-191">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="32530-192">如果实体受支持，且数据在 Common Data Service 中可用，请验证映射在数据集成器中是正确的。</span><span class="sxs-lookup"><span data-stu-id="32530-192">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="32530-193">如果集成器映射看起来正常，则验证数据管理作业是否成功运行。</span><span class="sxs-lookup"><span data-stu-id="32530-193">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="32530-194">错误可能在执行批处理作业时发生。</span><span class="sxs-lookup"><span data-stu-id="32530-194">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="32530-195">有关数据管理的详细信息，请参阅[数据管理](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="32530-195">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="32530-196">我在将员工地址导入 Finance 之后，这些地址不正确。</span><span class="sxs-lookup"><span data-stu-id="32530-196">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="32530-197">我应该怎么做？</span><span class="sxs-lookup"><span data-stu-id="32530-197">What should I do?</span></span>

<span data-ttu-id="32530-198">**位置 ID** 的编号规则在 Human Resources 和 Finance 中使用相同模式。</span><span class="sxs-lookup"><span data-stu-id="32530-198">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="32530-199">编号规则在两端都需要是唯一的，以便在将数据从 Common Data Service 集成到 Finance and Operations 时没有地址冲突。</span><span class="sxs-lookup"><span data-stu-id="32530-199">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="32530-200">在实施 Human Resources 时，请验证编号规则在 Human Resources 和 Finance 中不同。</span><span class="sxs-lookup"><span data-stu-id="32530-200">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="32530-201">验证数据可以在两个系统中维护的情况的所有编号规则是不同的。</span><span class="sxs-lookup"><span data-stu-id="32530-201">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="32530-202">当创建连接集时，我无法在“连接”下拉列表中看到连接。</span><span class="sxs-lookup"><span data-stu-id="32530-202">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="32530-203">我该做什么？</span><span class="sxs-lookup"><span data-stu-id="32530-203">What do I do?</span></span>

<span data-ttu-id="32530-204">请确保在创建连接时，您选择的是 Dynamics 365 Finance 和 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="32530-204">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="32530-205">当同步雇佣时，发生错误“CompanyInfo_FK 不存在”或“未在相关表‘雇佣’中找到字段‘雇佣结束日期’中的值‘12/31/2154 11:59:59 pm’”。我应该怎么做？</span><span class="sxs-lookup"><span data-stu-id="32530-205">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="32530-206">确保您在映射到正确的法人。</span><span class="sxs-lookup"><span data-stu-id="32530-206">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="32530-207">法人同步不是默认模板的一部分，因此，Human Resources 和 Common Data Service 中存在的每个法人也会出现在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="32530-207">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="32530-208">此外，还请确保您为关联的连接集选择了正确的法人。</span><span class="sxs-lookup"><span data-stu-id="32530-208">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="32530-209">在设置我的项目后，Finance 的字段映射似乎是空的。</span><span class="sxs-lookup"><span data-stu-id="32530-209">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="32530-210">我应该怎么做？</span><span class="sxs-lookup"><span data-stu-id="32530-210">What should I do?</span></span>

<span data-ttu-id="32530-211">通过转到**数据管理 \> 框架参数 \> 实体设置 \> 刷新实体列表**刷新 Finance 中的数据实体。</span><span class="sxs-lookup"><span data-stu-id="32530-211">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="32530-212">这应需要两三分钟完成，然后您应该看到这些映射。</span><span class="sxs-lookup"><span data-stu-id="32530-212">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="32530-213">在已创建新项目时，将发生此问题。</span><span class="sxs-lookup"><span data-stu-id="32530-213">This issue occurs when new projects are created.</span></span>

![缺少字段映射](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="32530-215">其他资源</span><span class="sxs-lookup"><span data-stu-id="32530-215">Additional resources</span></span>

- <span data-ttu-id="32530-216">数据集成器 (DI)：</span><span class="sxs-lookup"><span data-stu-id="32530-216">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="32530-217">将数据集成到 Common Data Service</span><span class="sxs-lookup"><span data-stu-id="32530-217">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="32530-218">数据集成器错误管理和故障排除</span><span class="sxs-lookup"><span data-stu-id="32530-218">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="32530-219">响应 Power Apps、Microsoft Power Automate 和 Common Data Service 中系统生成日志的 DSR 请求</span><span class="sxs-lookup"><span data-stu-id="32530-219">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="32530-220">数据管理：</span><span class="sxs-lookup"><span data-stu-id="32530-220">Data Management:</span></span>

  - [<span data-ttu-id="32530-221">数据管理</span><span class="sxs-lookup"><span data-stu-id="32530-221">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
