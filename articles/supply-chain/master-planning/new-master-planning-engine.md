---
title: 主计划的迁移到计划优化
description: 本主题提供有关新的主计划引擎、计划优化的信息，以及有关从现有引擎迁移的信息。
author: ChristianRytt
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: e227cabdd205b7a0c1fe784fc719b538e6ea4443
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907683"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a><span data-ttu-id="8a929-103">主计划的迁移到计划优化</span><span class="sxs-lookup"><span data-stu-id="8a929-103">Migration to Planning Optimization for master planning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a929-104">内置的主计划引擎计划将被废弃（已弃用）。</span><span class="sxs-lookup"><span data-stu-id="8a929-104">The built-in master planning engine is scheduled to be made obsolete (deprecated).</span></span> <span data-ttu-id="8a929-105">它将替换为 Microsoft Dynamics 365 Supply Chain Management 的计划优化加载项。</span><span class="sxs-lookup"><span data-stu-id="8a929-105">It's being replaced by the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8a929-106">本主题提供有关对新部署和现有部署的影响的信息。</span><span class="sxs-lookup"><span data-stu-id="8a929-106">This topic provides information about the impact on new and existing deployments.</span></span> <span data-ttu-id="8a929-107">它包含有关所需操作的信息。</span><span class="sxs-lookup"><span data-stu-id="8a929-107">It includes information about required actions.</span></span>

<span data-ttu-id="8a929-108">计划优化使主计划计算可以在 Supply Chain Management 及其 Azure SQL 数据库之外进行。</span><span class="sxs-lookup"><span data-stu-id="8a929-108">Planning Optimization enables master planning calculations to occur outside Supply Chain Management and its Azure SQL database.</span></span> <span data-ttu-id="8a929-109">与计划优化相关的好处包括在主计划运行期间改进的性能以及对 SQL 数据库的影响最小。</span><span class="sxs-lookup"><span data-stu-id="8a929-109">The benefits that are associated with Planning Optimization include improved performance and minimized impact on the SQL database during master planning runs.</span></span> <span data-ttu-id="8a929-110">因为即使在工作时间内也可以进行快速计划运行，因此计划人员可以立即对需求或参数更改作出反应。</span><span class="sxs-lookup"><span data-stu-id="8a929-110">Because quick planning runs can be done even during office hours, planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="8a929-111">有关计划优化的详细信息，请参阅[计划优化概述](planning-optimization/planning-optimization-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="8a929-111">For more information about Planning Optimization, see [Planning Optimization overview](planning-optimization/planning-optimization-overview.md).</span></span>

## <a name="obsolescence-of-the-existing-master-planning-engine"></a><span data-ttu-id="8a929-112">现有主计划引擎的废弃</span><span class="sxs-lookup"><span data-stu-id="8a929-112">Obsolescence of the existing master planning engine</span></span>

<span data-ttu-id="8a929-113">Microsoft 正在废弃内置的计划引擎，以支持计划优化。</span><span class="sxs-lookup"><span data-stu-id="8a929-113">Microsoft is in the process of making the built-in planning engine obsolete in favor of Planning Optimization.</span></span> <span data-ttu-id="8a929-114">此更改会影响所有云环境。</span><span class="sxs-lookup"><span data-stu-id="8a929-114">This change affects all cloud environments.</span></span> <span data-ttu-id="8a929-115">本地安装不受影响。</span><span class="sxs-lookup"><span data-stu-id="8a929-115">On-premises installations aren't affected.</span></span> <span data-ttu-id="8a929-116">在版本 10.0.16 及更高版本中，如果运行内置主计划而不生成计划的生产订单，您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="8a929-116">In version 10.0.16 and later, you will receive an error message if you run the built-in master planning without generating planned production orders.</span></span> <span data-ttu-id="8a929-117">但是，尽管有错误消息，主计划运行仍将成功完成。</span><span class="sxs-lookup"><span data-stu-id="8a929-117">However, the master planning run will be successfully completed despite the error message.</span></span>

<span data-ttu-id="8a929-118">有关内置计划引擎的废弃的详细信息，请参阅 [Dynamics 365 Supply Chain Management 中的已删除或已弃用功能](../get-started/removed-deprecated-features-scm-updates.md)中的公告。</span><span class="sxs-lookup"><span data-stu-id="8a929-118">For more information about the obsolescence of the built-in planning engine, see the announcements in [Removed or deprecated features in Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).</span></span>

## <a name="migration-messages-and-exceptions"></a><span data-ttu-id="8a929-119">迁移、消息和例外</span><span class="sxs-lookup"><span data-stu-id="8a929-119">Migration, messages, and exceptions</span></span>

<span data-ttu-id="8a929-120">运行内置主计划引擎而不生成计划生产订单的现有环境的所有者将收到一封电子邮件，用于提供有关例外流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="8a929-120">Owners of existing environments who run the built-in master planning engine without generating planned production orders will receive an email that provides details about the exception process.</span></span> <span data-ttu-id="8a929-121">我们建议您与合作伙伴一起评估和计划迁移到计划优化。</span><span class="sxs-lookup"><span data-stu-id="8a929-121">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="8a929-122">如前所述，在版本 10.0.16 及更高版本中，如果运行内置主计划而不生成计划的生产订单，您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="8a929-122">As has been mentioned, you will receive an error message in version 10.0.16 and later if you run the built-in master planning without generating planned production orders.</span></span> <span data-ttu-id="8a929-123">此错误消息包括有关迁移的指南和有关请求例外的说明。</span><span class="sxs-lookup"><span data-stu-id="8a929-123">This error message includes guidance about migration and instructions for requesting an exception.</span></span>

### <a name="new-deployments"></a><span data-ttu-id="8a929-124">新部署</span><span class="sxs-lookup"><span data-stu-id="8a929-124">New deployments</span></span>

<span data-ttu-id="8a929-125">对于云中的所有新部署，应将计划优化视为默认的主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="8a929-125">Planning Optimization should be considered the default master planning engine for all new deployments in the cloud.</span></span> <span data-ttu-id="8a929-126">通常，应该将计划优化用于在主计划期间不生成计划生产订单的所有新部署。</span><span class="sxs-lookup"><span data-stu-id="8a929-126">In general, Planning Optimization should be used for all new deployments that don't generate planned production orders during master planning.</span></span> <span data-ttu-id="8a929-127">如果新部署依赖于计划优化当前不支持的功能，您可以请求例外，以便继续使用内置的主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="8a929-127">If a new deployment depends on functionality that Planning Optimization doesn't currently support, you can request an exception so that you can continue to use the built-in master planning engine.</span></span>

### <a name="existing-deployments"></a><span data-ttu-id="8a929-128">现有部署</span><span class="sxs-lookup"><span data-stu-id="8a929-128">Existing deployments</span></span>

<span data-ttu-id="8a929-129">依赖于主计划的现有基于云的部署的所有者应计划迁移到计划优化。</span><span class="sxs-lookup"><span data-stu-id="8a929-129">Owners of existing cloud-based deployments that depend on master planning should plan to migrate to Planning Optimization.</span></span> <span data-ttu-id="8a929-130">如果您的实施依赖于计划优化当前不支持的功能，您可以请求例外，以便继续使用内置的主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="8a929-130">If your implementation depends on functionality that Planning Optimization doesn't currently support, you can request an exception so that you can continue to use the built-in master planning engine.</span></span>

<span data-ttu-id="8a929-131">对于当前使用将要废弃的主计划流程的环境，Microsoft 将向环境管理员发送电子邮件。该电子邮件将提供有关迁移或请求例外所需操作的信息。</span><span class="sxs-lookup"><span data-stu-id="8a929-131">For environments that currently use master planning processes that are being made obsolete, Microsoft will send an email to the environment admin. This email will provide information about the actions that are required to migrate or to request an exception.</span></span>

## <a name="the-exception-process"></a><span data-ttu-id="8a929-132">例外流程</span><span class="sxs-lookup"><span data-stu-id="8a929-132">The exception process</span></span>

<span data-ttu-id="8a929-133">如果您因为您的业务流程在很大程度上依赖于当前在计划优化中未实现的至少一项功能，而必须继续使用内置的主计划引擎，可以请求例外。</span><span class="sxs-lookup"><span data-stu-id="8a929-133">You can request an exception if you must continue to use the built-in master planning engine because your business processes depends heavily on at least one feature that isn't currently implemented in Planning Optimization.</span></span> <span data-ttu-id="8a929-134">有关可用功能的列表，请参阅[计划优化拟合分析](planning-optimization/planning-optimization-fit-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8a929-134">For a list of available features, see [Planning Optimization fit analysis](planning-optimization/planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="8a929-135">当前，如果您的主计划流程不包括生产（即由主计划生成的计划生产订单）并且您需要版本 10.0.15 以上的内置主计划引擎，则仅与计划优化的例外相关。</span><span class="sxs-lookup"><span data-stu-id="8a929-135">Currently, exceptions for Planning Optimization migration are only relevant if your master planning process doesn't include production (that is, planned production orders that are generated by master planning), and you require the built-in master planning engine beyond version 10.0.15.</span></span>

<span data-ttu-id="8a929-136">在所需的功能变为可用后，Microsoft 将提供一个宽限期，直到例外到期。</span><span class="sxs-lookup"><span data-stu-id="8a929-136">After the required features become available, Microsoft will provide a grace period until the exception expires.</span></span> <span data-ttu-id="8a929-137">当所需的功能变为可用并且宽限期已开始时，将通知环境管理员。</span><span class="sxs-lookup"><span data-stu-id="8a929-137">The environment admin will be informed when the required features have become available and the grace period has started.</span></span>

<span data-ttu-id="8a929-138">以下流程图总结了本主题中提供的信息，以便您可以快速确定是否应请求例外。</span><span class="sxs-lookup"><span data-stu-id="8a929-138">The following flowchart summarizes the information provided in this topic so you can quickly find out whether you should request an exception.</span></span> <span data-ttu-id="8a929-139">如果需要请求例外，请填写并提交[计划优化迁移和例外调查表](https://go.microsoft.com/fwlink/?linkid=2144962)。</span><span class="sxs-lookup"><span data-stu-id="8a929-139">If you do need to request an exception, please fill out and submit the [Planning Optimization migration and exception questionnaire](https://go.microsoft.com/fwlink/?linkid=2144962).</span></span>

<span data-ttu-id="8a929-140">![例外流程图](media/exception-diagram.png "例外流程图")</span><span class="sxs-lookup"><span data-stu-id="8a929-140">![Exception flowchart](media/exception-diagram.png "Exception flowchart")</span></span>

> [!NOTE]
> <span data-ttu-id="8a929-141">您只能针对当前包括或将包括生产环境的租户（而不能仅针对具有沙盒环境的租户）请求例外。</span><span class="sxs-lookup"><span data-stu-id="8a929-141">You can only request an exception for tenants that currently include, or will include, a production environment, not for tenants with sandbox environments only.</span></span> <span data-ttu-id="8a929-142">如果您需要在基础结构即服务 (IaaS) 沙盒环境上禁用计划优化例外错误，请运行在[沙盒环境](#faq-sandbox)中提供的 SQL 查询。</span><span class="sxs-lookup"><span data-stu-id="8a929-142">If you need to disable the Planning Optimization exception error on an infrastructure as a service (IaaS) sandbox environment, run the SQL query provided in [Sandbox environments](#faq-sandbox).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8a929-143">常见问题</span><span class="sxs-lookup"><span data-stu-id="8a929-143">Frequently asked questions</span></span>

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a><span data-ttu-id="8a929-144">沙盒环境</span><span class="sxs-lookup"><span data-stu-id="8a929-144">Sandbox environments</span></span>

<span data-ttu-id="8a929-145">是否可以在我的沙盒环境上使用内置主计划？</span><span class="sxs-lookup"><span data-stu-id="8a929-145">Can I use built-in master planning on my sandbox environment?</span></span> <span data-ttu-id="8a929-146">是否需要例外？</span><span class="sxs-lookup"><span data-stu-id="8a929-146">Do I need an exception?</span></span>

<span data-ttu-id="8a929-147">**回答：** 例外通常与沙盒环境无关，因为计划优化例外错误不会阻止内置主计划引擎成功运行。</span><span class="sxs-lookup"><span data-stu-id="8a929-147">**Answer:** Exceptions aren't normally relevant for sandbox environments because the Planning Optimization exception error doesn't prevent the built-in master planning engine from running successfully.</span></span> <span data-ttu-id="8a929-148">但是，如果错误消息打扰到您，可以通过在您的数据库上运行以下查询来在 IaaS（而非 Service Fabric）沙盒环境上禁用它：</span><span class="sxs-lookup"><span data-stu-id="8a929-148">However, if the error message disturbs you, you can disable it on an IaaS (not Service Fabric) sandbox environment by running the following query on your database:</span></span>

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a><span data-ttu-id="8a929-149">本地环境</span><span class="sxs-lookup"><span data-stu-id="8a929-149">On-premises environments</span></span>

<span data-ttu-id="8a929-150">我的环境是本地的。</span><span class="sxs-lookup"><span data-stu-id="8a929-150">My environment is on-premises.</span></span> <span data-ttu-id="8a929-151">是否需要例外？</span><span class="sxs-lookup"><span data-stu-id="8a929-151">Do I need an exception?</span></span>

<span data-ttu-id="8a929-152">**回答：** 否。</span><span class="sxs-lookup"><span data-stu-id="8a929-152">**Answer:** No.</span></span> <span data-ttu-id="8a929-153">本地环境不需要例外。</span><span class="sxs-lookup"><span data-stu-id="8a929-153">An exception isn't required for on-premises environments.</span></span> <span data-ttu-id="8a929-154">您可以继续使用内置主计划。</span><span class="sxs-lookup"><span data-stu-id="8a929-154">You can continue to use the built-in master planning.</span></span> <span data-ttu-id="8a929-155">如果需要任何操作，您的环境管理员将收到通知。</span><span class="sxs-lookup"><span data-stu-id="8a929-155">Your environment admin will be informed if any action is required.</span></span>

### <a name="production-scenarios"></a><span data-ttu-id="8a929-156">生产方案</span><span class="sxs-lookup"><span data-stu-id="8a929-156">Production scenarios</span></span>

<span data-ttu-id="8a929-157">我们使用计划生产订单，但是我担心升级到版本 10.0.16 时会发生什么。</span><span class="sxs-lookup"><span data-stu-id="8a929-157">We use planned production orders, but I'm concerned about what will happen when we upgrade to version 10.0.16.</span></span> <span data-ttu-id="8a929-158">是否应采取任何操作？</span><span class="sxs-lookup"><span data-stu-id="8a929-158">Should I take any action?</span></span>

<span data-ttu-id="8a929-159">**回答：** 您不必担心。</span><span class="sxs-lookup"><span data-stu-id="8a929-159">**Answer:** You should not be concerned.</span></span> <span data-ttu-id="8a929-160">您可以在版本 10.0.16 中继续使用内置主计划。</span><span class="sxs-lookup"><span data-stu-id="8a929-160">You can continue to use the built-in master planning in version 10.0.16.</span></span> <span data-ttu-id="8a929-161">但是，我们建议您评估是否可以从当前功能开始迁移到计划优化。</span><span class="sxs-lookup"><span data-stu-id="8a929-161">However, we recommend that you evaluate whether migration to Planning Optimization can start with the current functionality.</span></span> <span data-ttu-id="8a929-162">我们还建议您随时了解新功能。</span><span class="sxs-lookup"><span data-stu-id="8a929-162">We also recommend that you remain informed about new functionality.</span></span>

### <a name="email-from-microsoft"></a><span data-ttu-id="8a929-163">来自 Microsoft 的电子邮件</span><span class="sxs-lookup"><span data-stu-id="8a929-163">Email from Microsoft</span></span>

<span data-ttu-id="8a929-164">我们的环境管理员收到了来自 Microsoft 的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="8a929-164">Our environment admin received an email from Microsoft.</span></span> <span data-ttu-id="8a929-165">此电子邮件表明我们应该迁移到计划优化或请求例外。</span><span class="sxs-lookup"><span data-stu-id="8a929-165">This email states that we should migrate to Planning Optimization or request an exception.</span></span> <span data-ttu-id="8a929-166">是否需要采取任何操作？</span><span class="sxs-lookup"><span data-stu-id="8a929-166">Do I need to take any action?</span></span>

<span data-ttu-id="8a929-167">**回答：** 是。</span><span class="sxs-lookup"><span data-stu-id="8a929-167">**Answer:** Yes.</span></span> <span data-ttu-id="8a929-168">除非您遵循电子邮件中的说明，否则您的环境将受影响。</span><span class="sxs-lookup"><span data-stu-id="8a929-168">Your environment will be affected unless you follow the instructions in the email.</span></span> <span data-ttu-id="8a929-169">您可以按指定的日期迁移到计划优化，也可以使用电子邮件中的链接请求例外。</span><span class="sxs-lookup"><span data-stu-id="8a929-169">You can either migrate to Planning Optimization by the date specified or request an exception by using the link in the email.</span></span> <span data-ttu-id="8a929-170">此链接将打开一个调查表。</span><span class="sxs-lookup"><span data-stu-id="8a929-170">This link opens a questionnaire.</span></span> <span data-ttu-id="8a929-171">完成并提交此调查表后，您将通过电子邮件收到回复。</span><span class="sxs-lookup"><span data-stu-id="8a929-171">After you've completed and submitted this questionnaire, you will receive a reply via email.</span></span> <span data-ttu-id="8a929-172">尽管此流程是手动的，但 Microsoft 将尝试在提交调查表后的一周内回复。</span><span class="sxs-lookup"><span data-stu-id="8a929-172">Although this process is manual, Microsoft tries to reply within a week after the questionnaire is submitted.</span></span>

### <a name="error-messages"></a><span data-ttu-id="8a929-173">错误消息</span><span class="sxs-lookup"><span data-stu-id="8a929-173">Error messages</span></span>

<span data-ttu-id="8a929-174">我使用的是版本 10.0.16 或更高版本，并且在运行主计划时收到以下错误消息。</span><span class="sxs-lookup"><span data-stu-id="8a929-174">I'm using version 10.0.16 or later, and I receive the following error message when I run master planning.</span></span> <span data-ttu-id="8a929-175">是否阻止主计划？</span><span class="sxs-lookup"><span data-stu-id="8a929-175">Is master planning blocked?</span></span>

> <span data-ttu-id="8a929-176">您收到此错误消息是因为内置主计划引擎用于计划优化所支持的方案。</span><span class="sxs-lookup"><span data-stu-id="8a929-176">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="8a929-177">您现在应该迁移到计划优化，因为当前的内置主计划已弃用。</span><span class="sxs-lookup"><span data-stu-id="8a929-177">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="8a929-178">请注意，此主计划运行已成功完成。</span><span class="sxs-lookup"><span data-stu-id="8a929-178">Note that this master planning run did complete successfully.</span></span>
>
> <span data-ttu-id="8a929-179">如果您的迁移非常依赖待定功能，可以请求继续使用内置主计划引擎的例外。</span><span class="sxs-lookup"><span data-stu-id="8a929-179">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span>
>
> <span data-ttu-id="8a929-180">请完成以下调查表以开始使用（如果与从迁移到计划优化请求例外相关）。</span><span class="sxs-lookup"><span data-stu-id="8a929-180">Please complete the following questionnaire to get started and if relevant request exception from migration to Planning Optimization.</span></span>

<span data-ttu-id="8a929-181">**回答：** 否，不阻止主计划。</span><span class="sxs-lookup"><span data-stu-id="8a929-181">**Answer:** No, master planning isn't blocked.</span></span> <span data-ttu-id="8a929-182">您的主计划运行已成功完成，可按常规方式使用结果。</span><span class="sxs-lookup"><span data-stu-id="8a929-182">Your master planning run was successfully completed, and you can use the result in the usual way.</span></span> <span data-ttu-id="8a929-183">但是，为了避免在以后的主计划运行期间收到此错误消息，您必须立即迁移到计划优化或使用错误消息中的链接请求例外。</span><span class="sxs-lookup"><span data-stu-id="8a929-183">However, to avoid receiving this error message during future master planning runs, you must either migrate to Planning Optimization immediately or request an exception by using the link in the error message.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
