---
title: Dynamics 365 Talent（2019 年 6 月 11 日）新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f2ee23733d686480cd4323cab952ae12eceaf142
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897572"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-11-2019"></a><span data-ttu-id="84b1b-103">Dynamics 365 Talent（2019 年 6 月 11 日）新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="84b1b-103">What's new or changed in Dynamics 365 Talent (June 11, 2019)</span></span>

<span data-ttu-id="84b1b-104">此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="84b1b-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="84b1b-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="84b1b-105">Changes in Attract</span></span>

### <a name="search-engine-optimization-for-job-posts"></a><span data-ttu-id="84b1b-106">针对工作发布的搜索引擎优化</span><span class="sxs-lookup"><span data-stu-id="84b1b-106">Search engine optimization for job posts</span></span>

<span data-ttu-id="84b1b-107">在 Dynamics 365 Talent: Attract: 管理中心中开启**搜索引擎优化**之后，只要激活并发布新工作或更新现有工作，Attract 都会通知 Google Indexing 应用程序编程接口 (API) 去抓取网页。</span><span class="sxs-lookup"><span data-stu-id="84b1b-107">After you turn on **Search Engine Optimization** in the Dynamics 365 Talent: Attract Admin center, Attract informs the Google Indexing application programming interface (API) to crawl the webpage whenever you activate and post a new job or update an existing job.</span></span> <span data-ttu-id="84b1b-108">这样就会在 Google 和其他搜索引擎的搜索结果中显示该作业。</span><span class="sxs-lookup"><span data-stu-id="84b1b-108">In this way, the job will appear in the search results for Google and other search engines.</span></span>

<span data-ttu-id="84b1b-109">同样，只要取消发布工作，Attract 就会通知 Indexing API，这样取消发布的工作就会不再在搜索结果中显示。</span><span class="sxs-lookup"><span data-stu-id="84b1b-109">Likewise, whenever you unpost a job, Attract informs the Indexing API, so that the unposted job will stop appearing in search results.</span></span>

> [!NOTE]
> <span data-ttu-id="84b1b-110">Web 爬网程序没有为抓取网页或更新搜索结果定义时间范围。</span><span class="sxs-lookup"><span data-stu-id="84b1b-110">Web crawlers don't have a defined timeframe for crawling webpages or updating search results.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="84b1b-111">Attract 中即将推出</span><span class="sxs-lookup"><span data-stu-id="84b1b-111">Coming soon in Attract</span></span>

### <a name="job-approvals-appear-on-the-home-page"></a><span data-ttu-id="84b1b-112">主页中显示工作审核</span><span class="sxs-lookup"><span data-stu-id="84b1b-112">Job approvals appear on the home page</span></span>

<span data-ttu-id="84b1b-113">仪表板的**审核**部分中将显示审核。</span><span class="sxs-lookup"><span data-stu-id="84b1b-113">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="84b1b-114">审核人可以在**已分配给您**（其中显示工作 ID、工作头衔、其他审核人和作业的分配日期）下查看自己的审核。</span><span class="sxs-lookup"><span data-stu-id="84b1b-114">Approvers can review their approvals under **Assigned to you**, which shows the job ID, the job title, other approvers, and the date when the job was assigned.</span></span> <span data-ttu-id="84b1b-115">提交待审核工作的用户可以在**您请求的**（其中显示仍然必须审核提交的工作的审核者）下查看自己的工作。</span><span class="sxs-lookup"><span data-stu-id="84b1b-115">Users who submit a job for approval can review their jobs under **Requested by you**, which shows the approvers who must still approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="84b1b-116">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="84b1b-116">Changes in Onboard</span></span>

<span data-ttu-id="84b1b-117">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="84b1b-117">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="84b1b-118">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="84b1b-118">Changes in Core HR</span></span>

<span data-ttu-id="84b1b-119">本部分中介绍的更改适用于内部版本号 8.1.2337。</span><span class="sxs-lookup"><span data-stu-id="84b1b-119">The changes that are described in this section apply to build number 8.1.2337.</span></span>

### <a name="platform-update-27-for-finance-and-operations"></a><span data-ttu-id="84b1b-120">Finance and Operations 的平台更新 27</span><span class="sxs-lookup"><span data-stu-id="84b1b-120">Platform update 27 for Finance and Operations</span></span>

<span data-ttu-id="84b1b-121">有关 Finance and Operations 的平台更新 27 的更多详细信息，请参阅 [Dynamics 365 Finance and Operations 平台更新 27（2019 年 6 月）的预览功能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27)。</span><span class="sxs-lookup"><span data-stu-id="84b1b-121">For more details about Platform update 27 for Finance and Operations, see [Preview features in Dynamics 365 Finance and Operations platform update 27 (June 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).</span></span>

### <a name="feature-management-workspace-in-talent"></a><span data-ttu-id="84b1b-122">Talent 中的功能管理工作区</span><span class="sxs-lookup"><span data-stu-id="84b1b-122">Feature management workspace in Talent</span></span>

<span data-ttu-id="84b1b-123">可使用**系统管理**中的**功能管理**工作区查看、启用、禁用和计划各版本中提供的功能。</span><span class="sxs-lookup"><span data-stu-id="84b1b-123">The **Feature management** workspace in **System administration** lets you view, enable, disable, and schedule features that have been delivered in each release.</span></span> <span data-ttu-id="84b1b-124">默认情况下，新功能处于关闭状态。</span><span class="sxs-lookup"><span data-stu-id="84b1b-124">By default, new features are turned off.</span></span> <span data-ttu-id="84b1b-125">可使用**功能管理**工作区开启这些功能并查看其文档。</span><span class="sxs-lookup"><span data-stu-id="84b1b-125">You can use the **Feature management** workspace to turn them on and view the documentation for them.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="84b1b-126">Common Data Service 实体对自定义字段的支持</span><span class="sxs-lookup"><span data-stu-id="84b1b-126">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="84b1b-127">颁发机构实体现在支持自定义字段。</span><span class="sxs-lookup"><span data-stu-id="84b1b-127">The Issuing agency entity now supports custom fields.</span></span>

### <a name="new-common-data-service-entities"></a><span data-ttu-id="84b1b-128">新增 Common Data Service 实体</span><span class="sxs-lookup"><span data-stu-id="84b1b-128">New Common Data Service entities</span></span>

<span data-ttu-id="84b1b-129">增加了任务组实体。</span><span class="sxs-lookup"><span data-stu-id="84b1b-129">The Task group entity has been added.</span></span>

## <a name="in-preview"></a><span data-ttu-id="84b1b-130">预览模式</span><span class="sxs-lookup"><span data-stu-id="84b1b-130">In preview</span></span>

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a><span data-ttu-id="84b1b-131">仅在沙盒环境中才会启用预览功能。</span><span class="sxs-lookup"><span data-stu-id="84b1b-131">Preview features will be enabled only in sandbox environments</span></span>

<span data-ttu-id="84b1b-132">有关如何发布更改的详细信息，请参阅[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。</span><span class="sxs-lookup"><span data-stu-id="84b1b-132">For more information about how changes are published, see [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="84b1b-133">配置新的 Talent 实例时，可指示实例类型为“生产”还是“沙盒”。</span><span class="sxs-lookup"><span data-stu-id="84b1b-133">When you provision a new instance of Talent, you can indicate whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="84b1b-134">“沙盒”实例类型可用于提前测试新功能。</span><span class="sxs-lookup"><span data-stu-id="84b1b-134">The Sandbox instance type allows for early testing of new features.</span></span> <span data-ttu-id="84b1b-135">将把所有现有 Talent 实例更新为**生产**实例类型。</span><span class="sxs-lookup"><span data-stu-id="84b1b-135">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="84b1b-136">如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support)以发起更改请求。</span><span class="sxs-lookup"><span data-stu-id="84b1b-136">If you want one of your existing instances to be updated to the **Sandbox** instance type, contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="restrict-the-leave-types-in-time-off-requests"></a><span data-ttu-id="84b1b-137">限制请假中的休假类型</span><span class="sxs-lookup"><span data-stu-id="84b1b-137">Restrict the leave types in time-off requests</span></span>

<span data-ttu-id="84b1b-138">组织可以为员工提供多种休假类型。</span><span class="sxs-lookup"><span data-stu-id="84b1b-138">Organizations can offer many types of leave to employees.</span></span> <span data-ttu-id="84b1b-139">但是，可能不适合员工提交某些休假类型的请假。</span><span class="sxs-lookup"><span data-stu-id="84b1b-139">However, it might not be appropriate for employees to submit time-off requests for some leave types.</span></span> <span data-ttu-id="84b1b-140">可以改用人力资源 (HR) 管理这些休假类型。</span><span class="sxs-lookup"><span data-stu-id="84b1b-140">Those leave types might be managed by Human resources (HR) instead.</span></span> <span data-ttu-id="84b1b-141">在此版本中，可以配置员工可以提交哪些休假类型的请假。</span><span class="sxs-lookup"><span data-stu-id="84b1b-141">In this release, you can configure which leave types employees can submit time-off requests for.</span></span> 

## <a name="coming-soon-in-core-hr"></a><span data-ttu-id="84b1b-142">Core HR 中即将推出</span><span class="sxs-lookup"><span data-stu-id="84b1b-142">Coming soon in Core HR</span></span>

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a><span data-ttu-id="84b1b-143">在经理自助服务中查看有关报表性能的更多信息</span><span class="sxs-lookup"><span data-stu-id="84b1b-143">View extended information about report performance in manager self-service</span></span>

<span data-ttu-id="84b1b-144">经理可通过一个新选项查看直接报表和扩展报表的绩效。</span><span class="sxs-lookup"><span data-stu-id="84b1b-144">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="84b1b-145">现在，职能经理可以分配和更新绩效目标和颁发新审核。</span><span class="sxs-lookup"><span data-stu-id="84b1b-145">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="84b1b-146">此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。</span><span class="sxs-lookup"><span data-stu-id="84b1b-146">In addition, direct managers and their employees can maintain and update performance journals to help guarantee that the performance review process goes smoothly.</span></span> <span data-ttu-id="84b1b-147">实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。</span><span class="sxs-lookup"><span data-stu-id="84b1b-147">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="84b1b-148">打印绩效复查</span><span class="sxs-lookup"><span data-stu-id="84b1b-148">Print performance reviews</span></span>

<span data-ttu-id="84b1b-149">员工、经理和 HR 可以打印员工的绩效复查。</span><span class="sxs-lookup"><span data-stu-id="84b1b-149">Employees, managers, and HR will be able to print an employee's performance review.</span></span>
