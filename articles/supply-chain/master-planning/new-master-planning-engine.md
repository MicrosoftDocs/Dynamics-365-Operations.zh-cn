---
title: 主计划的迁移到计划优化
description: 本主题提供有关新的主计划引擎、计划优化的信息，以及有关从现有引擎迁移的信息。
author: ChristianRytt
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: 94e5668da45c524ed9ab9eef10b40d0fb5336a65
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645988"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a><span data-ttu-id="6c3d2-103">主计划的迁移到计划优化</span><span class="sxs-lookup"><span data-stu-id="6c3d2-103">Migration to Planning Optimization for master planning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c3d2-104">内置的主计划引擎计划将被废弃（已弃用）。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-104">The built-in master planning engine is scheduled to be made obsolete (deprecated).</span></span> <span data-ttu-id="6c3d2-105">它将替换为 Microsoft Dynamics 365 Supply Chain Management 的计划优化加载项。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-105">It's being replaced by the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6c3d2-106">本主题提供有关对新部署和现有部署的影响的信息。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-106">This topic provides information about the impact on new and existing deployments.</span></span> <span data-ttu-id="6c3d2-107">它包含有关所需操作的信息。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-107">It includes information about required actions.</span></span>

<span data-ttu-id="6c3d2-108">计划优化使主计划计算可以在 Supply Chain Management 及其 Azure SQL 数据库之外进行。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-108">Planning Optimization enables master planning calculations to occur outside Supply Chain Management and its Azure SQL database.</span></span> <span data-ttu-id="6c3d2-109">与计划优化相关的好处包括在主计划运行期间改进的性能以及对 SQL 数据库的影响最小。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-109">The benefits that are associated with Planning Optimization include improved performance and minimized impact on the SQL database during master planning runs.</span></span> <span data-ttu-id="6c3d2-110">因为即使在工作时间内也可以进行快速计划运行，因此计划人员可以立即对需求或参数更改作出反应。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-110">Because quick planning runs can be done even during office hours, planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="6c3d2-111">有关计划优化的详细信息，请参阅[计划优化概述](planning-optimization/planning-optimization-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-111">For more information about Planning Optimization, see [Planning Optimization overview](planning-optimization/planning-optimization-overview.md).</span></span>

## <a name="obsolescence-of-the-existing-master-planning-engine"></a><span data-ttu-id="6c3d2-112">现有主计划引擎的废弃</span><span class="sxs-lookup"><span data-stu-id="6c3d2-112">Obsolescence of the existing master planning engine</span></span>

<span data-ttu-id="6c3d2-113">Microsoft 正在废弃内置的计划引擎，以支持计划优化。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-113">Microsoft is in the process of making the built-in planning engine obsolete in favor of Planning Optimization.</span></span> <span data-ttu-id="6c3d2-114">此更改会影响所有云环境。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-114">This change affects all cloud environments.</span></span> <span data-ttu-id="6c3d2-115">本地安装不受影响。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-115">On-premises installations aren't affected.</span></span> <span data-ttu-id="6c3d2-116">在版本 10.0.16 及更高版本中，如果运行内置主计划而不生成计划的生产订单，您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-116">In version 10.0.16 and later, you will receive an error message if you run the built-in master planning without generating planned production orders.</span></span> <span data-ttu-id="6c3d2-117">但是，尽管有错误消息，主计划运行仍将成功完成。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-117">However, the master planning run will be successfully completed despite the error message.</span></span>

<span data-ttu-id="6c3d2-118">有关内置计划引擎的废弃的详细信息，请参阅 [Dynamics 365 Supply Chain Management 中的已删除或已弃用功能](../get-started/removed-deprecated-features-scm-updates.md)中的公告。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-118">For more information about the obsolescence of the built-in planning engine, see the announcements in [Removed or deprecated features in Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).</span></span>

## <a name="migration-messages-and-exceptions"></a><span data-ttu-id="6c3d2-119">迁移、消息和例外</span><span class="sxs-lookup"><span data-stu-id="6c3d2-119">Migration, messages, and exceptions</span></span>

<span data-ttu-id="6c3d2-120">运行内置主计划引擎而不生成计划生产订单的现有环境的所有者将收到一封电子邮件，用于提供有关例外流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-120">Owners of existing environments who run the built-in master planning engine without generating planned production orders will receive an email that provides details about the exception process.</span></span> <span data-ttu-id="6c3d2-121">我们建议您与合作伙伴一起评估和计划迁移到计划优化。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-121">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="6c3d2-122">如前所述，在版本 10.0.16 及更高版本中，如果运行内置主计划而不生成计划的生产订单，您将收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-122">As has been mentioned, you will receive an error message in version 10.0.16 and later if you run the built-in master planning without generating planned production orders.</span></span> <span data-ttu-id="6c3d2-123">此错误消息包括有关迁移的指南和有关请求例外的说明。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-123">This error message includes guidance about migration and instructions for requesting an exception.</span></span>

### <a name="new-deployments"></a><span data-ttu-id="6c3d2-124">新部署</span><span class="sxs-lookup"><span data-stu-id="6c3d2-124">New deployments</span></span>

<span data-ttu-id="6c3d2-125">对于云中的所有新部署，应将计划优化视为默认的主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-125">Planning Optimization should be considered the default master planning engine for all new deployments in the cloud.</span></span> <span data-ttu-id="6c3d2-126">通常，应该将计划优化用于在主计划期间不生成计划生产订单的所有新部署。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-126">In general, Planning Optimization should be used for all new deployments that don't generate planned production orders during master planning.</span></span> <span data-ttu-id="6c3d2-127">如果新部署依赖于计划优化当前不支持的功能，您可以请求例外，以便继续使用内置的主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-127">If a new deployment depends on functionality that Planning Optimization doesn't currently support, you can request an exception so that you can continue to use the built-in master planning engine.</span></span>

### <a name="existing-deployments"></a><span data-ttu-id="6c3d2-128">现有部署</span><span class="sxs-lookup"><span data-stu-id="6c3d2-128">Existing deployments</span></span>

<span data-ttu-id="6c3d2-129">依赖于主计划的现有基于云的部署的所有者应计划迁移到计划优化。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-129">Owners of existing cloud-based deployments that depend on master planning should plan to migrate to Planning Optimization.</span></span> <span data-ttu-id="6c3d2-130">如果您的实施依赖于计划优化当前不支持的功能，您可以请求例外，以便继续使用内置的主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-130">If your implementation depends on functionality that Planning Optimization doesn't currently support, you can request an exception so that you can continue to use the built-in master planning engine.</span></span>

<span data-ttu-id="6c3d2-131">对于当前使用将要废弃的主计划流程的环境，Microsoft 将向环境管理员发送电子邮件。该电子邮件将提供有关迁移或请求例外所需操作的信息。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-131">For environments that currently use master planning processes that are being made obsolete, Microsoft will send an email to the environment admin. This email will provide information about the actions that are required to migrate or to request an exception.</span></span>

## <a name="the-exception-process"></a><span data-ttu-id="6c3d2-132">例外流程</span><span class="sxs-lookup"><span data-stu-id="6c3d2-132">The exception process</span></span>

<span data-ttu-id="6c3d2-133">如果您因为您的业务流程在很大程度上依赖于当前在计划优化中未实现的至少一项功能，而必须继续使用内置的主计划引擎，可以请求例外。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-133">You can request an exception if you must continue to use the built-in master planning engine because your business processes depends heavily on at least one feature that isn't currently implemented in Planning Optimization.</span></span> <span data-ttu-id="6c3d2-134">有关可用功能的列表，请参阅[计划优化拟合分析](planning-optimization/planning-optimization-fit-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-134">For a list of available features, see [Planning Optimization fit analysis](planning-optimization/planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="6c3d2-135">当前，如果您的主计划流程不包括生产（即由主计划生成的计划生产订单）并且您需要版本 10.0.15 以上的内置主计划引擎，则仅与计划优化的例外相关。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-135">Currently, exceptions for Planning Optimization migration are only relevant if your master planning process doesn't include production (that is, planned production orders that are generated by master planning), and you require the built-in master planning engine beyond version 10.0.15.</span></span>

<span data-ttu-id="6c3d2-136">在所需的功能变为可用后，Microsoft 将提供一个宽限期，直到例外到期。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-136">After the required features become available, Microsoft will provide a grace period until the exception expires.</span></span> <span data-ttu-id="6c3d2-137">当所需的功能变为可用并且宽限期已开始时，将通知环境管理员。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-137">The environment admin will be informed when the required features have become available and the grace period has started.</span></span>

> [!NOTE]
> <span data-ttu-id="6c3d2-138">您只能针对生产环境（而非沙盒环境）请求一个例外。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-138">You can only request an exception for production environments, not for sandbox environments.</span></span> <span data-ttu-id="6c3d2-139">如果您需要在基础结构即服务 (IaaS) 沙盒环境上禁用计划优化例外错误，请运行在[沙盒环境](#faq-sandbox)中提供的 SQL 查询。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-139">If you need to disable the Planning Optimization exception error on an infrastructure as a service (IaaS) sandbox environment, run the SQL query provided in [Sandbox environments](#faq-sandbox).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6c3d2-140">常见问题</span><span class="sxs-lookup"><span data-stu-id="6c3d2-140">Frequently asked questions</span></span>

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a><span data-ttu-id="6c3d2-141">沙盒环境</span><span class="sxs-lookup"><span data-stu-id="6c3d2-141">Sandbox environments</span></span>

<span data-ttu-id="6c3d2-142">是否可以在我的沙盒环境上使用内置主计划？</span><span class="sxs-lookup"><span data-stu-id="6c3d2-142">Can I use built-in master planning on my sandbox environment?</span></span> <span data-ttu-id="6c3d2-143">是否需要例外？</span><span class="sxs-lookup"><span data-stu-id="6c3d2-143">Do I need an exception?</span></span>

<span data-ttu-id="6c3d2-144">**回答：** 例外通常与沙盒环境无关，因为计划优化例外错误不会阻止内置主计划引擎成功运行。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-144">**Answer:** Exceptions aren't normally relevant for sandbox environments because the Planning Optimization exception error doesn't prevent the built-in master planning engine from running successfully.</span></span> <span data-ttu-id="6c3d2-145">但是，如果错误消息打扰到您，可以通过在您的数据库上运行以下查询来在 IaaS（而非 Service Fabric）沙盒环境上禁用它：</span><span class="sxs-lookup"><span data-stu-id="6c3d2-145">However, if the error message disturbs you, you can disable it on an IaaS (not Service Fabric) sandbox environment by running the following query on your database:</span></span>

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a><span data-ttu-id="6c3d2-146">本地环境</span><span class="sxs-lookup"><span data-stu-id="6c3d2-146">On-premises environments</span></span>

<span data-ttu-id="6c3d2-147">我的环境是本地的。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-147">My environment is on-premises.</span></span> <span data-ttu-id="6c3d2-148">是否需要例外？</span><span class="sxs-lookup"><span data-stu-id="6c3d2-148">Do I need an exception?</span></span>

<span data-ttu-id="6c3d2-149">**回答：** 否。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-149">**Answer:** No.</span></span> <span data-ttu-id="6c3d2-150">本地环境不需要例外。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-150">An exception isn't required for on-premises environments.</span></span> <span data-ttu-id="6c3d2-151">您可以继续使用内置主计划。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-151">You can continue to use the built-in master planning.</span></span> <span data-ttu-id="6c3d2-152">如果需要任何操作，您的环境管理员将收到通知。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-152">Your environment admin will be informed if any action is required.</span></span>

### <a name="production-scenarios"></a><span data-ttu-id="6c3d2-153">生产方案</span><span class="sxs-lookup"><span data-stu-id="6c3d2-153">Production scenarios</span></span>

<span data-ttu-id="6c3d2-154">我们使用计划生产订单，但是我担心升级到版本 10.0.16 时会发生什么。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-154">We use planned production orders, but I'm concerned about what will happen when we upgrade to version 10.0.16.</span></span> <span data-ttu-id="6c3d2-155">是否应采取任何操作？</span><span class="sxs-lookup"><span data-stu-id="6c3d2-155">Should I take any action?</span></span>

<span data-ttu-id="6c3d2-156">**回答：** 您不必担心。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-156">**Answer:** You should not be concerned.</span></span> <span data-ttu-id="6c3d2-157">您可以在版本 10.0.16 中继续使用内置主计划。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-157">You can continue to use the built-in master planning in version 10.0.16.</span></span> <span data-ttu-id="6c3d2-158">但是，我们建议您评估是否可以从当前功能开始迁移到计划优化。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-158">However, we recommend that you evaluate whether migration to Planning Optimization can start with the current functionality.</span></span> <span data-ttu-id="6c3d2-159">我们还建议您随时了解新功能。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-159">We also recommend that you remain informed about new functionality.</span></span>

### <a name="email-from-microsoft"></a><span data-ttu-id="6c3d2-160">来自 Microsoft 的电子邮件</span><span class="sxs-lookup"><span data-stu-id="6c3d2-160">Email from Microsoft</span></span>

<span data-ttu-id="6c3d2-161">我们的环境管理员收到了来自 Microsoft 的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-161">Our environment admin received an email from Microsoft.</span></span> <span data-ttu-id="6c3d2-162">此电子邮件表明我们应该迁移到计划优化或请求例外。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-162">This email states that we should migrate to Planning Optimization or request an exception.</span></span> <span data-ttu-id="6c3d2-163">是否需要采取任何操作？</span><span class="sxs-lookup"><span data-stu-id="6c3d2-163">Do I need to take any action?</span></span>

<span data-ttu-id="6c3d2-164">**回答：** 是。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-164">**Answer:** Yes.</span></span> <span data-ttu-id="6c3d2-165">除非您遵循电子邮件中的说明，否则您的环境将受影响。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-165">Your environment will be affected unless you follow the instructions in the email.</span></span> <span data-ttu-id="6c3d2-166">您可以按指定的日期迁移到计划优化，也可以使用电子邮件中的链接请求例外。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-166">You can either migrate to Planning Optimization by the date specified or request an exception by using the link in the email.</span></span> <span data-ttu-id="6c3d2-167">此链接将打开一个调查表。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-167">This link opens a questionnaire.</span></span> <span data-ttu-id="6c3d2-168">完成并提交此调查表后，您将通过电子邮件收到回复。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-168">After you've completed and submitted this questionnaire, you will receive a reply via email.</span></span> <span data-ttu-id="6c3d2-169">尽管此流程是手动的，但 Microsoft 将尝试在提交调查表后的一周内回复。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-169">Although this process is manual, Microsoft tries to reply within a week after the questionnaire is submitted.</span></span>

### <a name="error-messages"></a><span data-ttu-id="6c3d2-170">错误消息</span><span class="sxs-lookup"><span data-stu-id="6c3d2-170">Error messages</span></span>

<span data-ttu-id="6c3d2-171">我使用的是版本 10.0.16 或更高版本，并且在运行主计划时收到以下错误消息。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-171">I'm using version 10.0.16 or later, and I receive the following error message when I run master planning.</span></span> <span data-ttu-id="6c3d2-172">是否阻止主计划？</span><span class="sxs-lookup"><span data-stu-id="6c3d2-172">Is master planning blocked?</span></span>

> <span data-ttu-id="6c3d2-173">您收到此错误消息是因为内置主计划引擎用于计划优化所支持的方案。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-173">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="6c3d2-174">您现在应该迁移到计划优化，因为当前的内置主计划已弃用。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-174">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="6c3d2-175">请注意，此主计划运行已成功完成。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-175">Note that this master planning run did complete successfully.</span></span>
>
> <span data-ttu-id="6c3d2-176">如果您的迁移非常依赖待定功能，可以请求继续使用内置主计划引擎的例外。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-176">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span>
>
> <span data-ttu-id="6c3d2-177">请完成以下调查表以开始使用（如果与从迁移到计划优化请求例外相关）。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-177">Please complete the following questionnaire to get started and if relevant request exception from migration to Planning Optimization.</span></span>

<span data-ttu-id="6c3d2-178">**回答：** 否，不阻止主计划。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-178">**Answer:** No, master planning isn't blocked.</span></span> <span data-ttu-id="6c3d2-179">您的主计划运行已成功完成，可按常规方式使用结果。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-179">Your master planning run was successfully completed, and you can use the result in the usual way.</span></span> <span data-ttu-id="6c3d2-180">但是，为了避免在以后的主计划运行期间收到此错误消息，您必须立即迁移到计划优化或使用错误消息中的链接请求例外。</span><span class="sxs-lookup"><span data-stu-id="6c3d2-180">However, to avoid receiving this error message during future master planning runs, you must either migrate to Planning Optimization immediately or request an exception by using the link in the error message.</span></span>
