---
title: 使用 PowerApps 和 Microsoft Flow 扩展 Talent - 示例方案
description: 本主题介绍 Microsoft Dynamics 365 for Talent 的一些使用 Microsoft PowerApps 和 Microsoft Flow 的可扩展性方案示例。
author: negudava
manager: Annbe
ms.date: 03/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0aa3578047b9397682a7039d0dbcc05cc1b167e4
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/12/2019
ms.locfileid: "949912"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="3ed8b-103">使用 PowerApps 和 Microsoft Flow 扩展 Talent - 示例方案</span><span class="sxs-lookup"><span data-stu-id="3ed8b-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="3ed8b-104">本主题介绍 Microsoft Dynamics 365 for Talent 的一些使用 Microsoft PowerApps 和 Microsoft Flow 的可扩展性方案示例。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="3ed8b-105">可以将与各示例关联的解决方案包导入到您的 PowerApps 环境中。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="3ed8b-106">然后可以将这些包用作指南或起点来实施适用于贵组织的方案。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ed8b-107">如果要“照原样”使用本主题中介绍的模板和应用，请务必测试这些模板和应用，以确保其涵盖特定于您的实施的所有方案。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="3ed8b-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="3ed8b-108">Prerequisites</span></span>

- <span data-ttu-id="3ed8b-109">若要导入包，用户必须具有**环境制造者**权限。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="3ed8b-110">若要导出或导入应用，用户必须拥有 PowerApps 计划 2 许可证或 PowerApps 计划 2 试用许可证。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="3ed8b-111">流 – 表连接</span><span class="sxs-lookup"><span data-stu-id="3ed8b-111">Flow – Form Connect</span></span>

<span data-ttu-id="3ed8b-112">**流 – 表连接** 模板可用于从 Microsoft Forms 读取数据并存储到 Common Data Service 实体中。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="3ed8b-113">可扩展此模板，以使其可用于其他方案。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="3ed8b-114">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="3ed8b-114">Here are some examples:</span></span>

- <span data-ttu-id="3ed8b-115">捕获应聘者评估。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="3ed8b-116">捕获课程调查表的结果。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="3ed8b-117">为人力资源 (HR) 管理员编译面试问题库。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="3ed8b-118">捕获应聘者的面试流程评估</span><span class="sxs-lookup"><span data-stu-id="3ed8b-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="3ed8b-119">在 Microsoft Dynamics 365: Attract 中，可以在应聘者门户中显示窗体，而应聘者可以填写详细信息。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="3ed8b-120">也可以将窗体作为活动嵌入到工作模板中。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="3ed8b-121">应聘者提交窗体时，Microsoft Flow 捕获窗体提交，读取数据，然后将其存储到 Common Data Service 实体中。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="3ed8b-122">若要下载**流 – 表连接**模板和自定义实体结构，请转至 Microsoft 下载中心中的[流 – 表连接](https://go.microsoft.com/fwlink/?linkid=2081988)。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="3ed8b-123">启动和提取传递到 Powerapps 的参数</span><span class="sxs-lookup"><span data-stu-id="3ed8b-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="3ed8b-124">**启动和提取传递到 Powerapps 的参数**模板可用作任何特定于 Attract 的 PowerApps 方案的起点。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="3ed8b-125">其中包含 Attract 传递的所有默认参数，如**工作申请**、**应聘者 ID** 和 **工作 ID**。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="3ed8b-126">此模板可用于检索应聘者评估表，这样招聘经理就可以查看应聘者填写的评估。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="3ed8b-127">可在 Attract 中将使用 PowerApps 创建的应用嵌入到工作模板内。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="3ed8b-128">若要下载**启动和提取传递到 Powerapps 的参数**模板和自定义实体结构，请转到 Microsoft 下载中心中的[启动和提取传递到 Powerapps 的参数](https://go.microsoft.com/fwlink/?linkid=2081991)。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="3ed8b-129">与 Office 365 的集成</span><span class="sxs-lookup"><span data-stu-id="3ed8b-129">Integration with Office 365</span></span>

<span data-ttu-id="3ed8b-130">**与 Office 365 的集成**应用可用于从 Microsoft Office 365 为已登录用户提取团队信息。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="3ed8b-131">它在 Talent 中提醒工作人员提取上班打卡和下班打卡详细信息和异常记录。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="3ed8b-132">上班打卡和下班打卡详细信息存储在自定义的 Common Data Service 实体中。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="3ed8b-133">假定这些详细信息是通过集成从第三方系统填写的。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="3ed8b-134">可扩展此应用，以使其可用于其他方案。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="3ed8b-135">例如，可用于显示团队休假信息、日历事件和团队特定的任何事件。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="3ed8b-136">若要下载**与 Office 365 的的集成**应用和自定义实体结构，请转到 Microsoft 下载中心中的[与 Office 365 的集成](https://go.microsoft.com/fwlink/?linkid=2081787)。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="3ed8b-137">流 – 电子邮件通知</span><span class="sxs-lookup"><span data-stu-id="3ed8b-137">Flow – Email Notification</span></span>

<span data-ttu-id="3ed8b-138">**流 – 电子邮件通知**模板可用于电子邮件通知方案。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="3ed8b-139">可用于在招聘流程任何阶段向招聘团队拒绝的应聘者触发通知电子邮件。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="3ed8b-140">可扩展此模板以在整个招聘流程中跟踪对应聘者阶段的更改，以及向招聘团队和应聘者发送通知。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="3ed8b-141">总之，对于 Common Data Service 中存储的实体，可以设置流程以发送有关 Core HR、Attract 或 Dynamics 365 Talent: Onboard 中发生的事件的通知。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="3ed8b-142">若要下载**流 – 电子邮件通知**模板，请转到 Microsoft 下载中心中的[流 – 电子邮件通知](https://go.microsoft.com/fwlink/?linkid=2082103)。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="3ed8b-143">流 – SQL 连接和执行</span><span class="sxs-lookup"><span data-stu-id="3ed8b-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="3ed8b-144">**流 – SQL 连接和执行**模板连接到 Microsoft SQL Server 并让 SQL 查询运行。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="3ed8b-145">尽管此模板设计为读取和更新 SQL 表，但对其进行扩展，以便将其用于其他方案。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="3ed8b-146">例如，可将其用于使用来自 SQL Server 的记录填充 Common Data Service 中的暂存表，以及通过使用来自 SQL Server 的增量推送定期同步暂存表。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="3ed8b-147">若要下载**流 – SQL 连接和执行**模板和自定义实体结构，请转至 Microsoft 下载中心中的[流 – SQL 连接和执行](https://go.microsoft.com/fwlink/?linkid=2081789)。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="3ed8b-148">流 – SharePoint 集成</span><span class="sxs-lookup"><span data-stu-id="3ed8b-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="3ed8b-149">**流 – SharePoint 集成**模板可用于从 Microsoft SharePoint 列表读取数据，将该列表与任何 Common Data Service 实体的字段值进行比较，以及将比较结果以通知电子邮件的形式发送。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="3ed8b-150">组织可能有一组急需的技能。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="3ed8b-151">这些技能可以以 SharePoint 列表的形式存储在 SharePoint 中。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="3ed8b-152">当应聘者申请列出了一组必需技能的任何工作时，如果应聘者的技能与 SharePoint 中存储的技能之间匹配度极高，将发送通知电子邮件。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="3ed8b-153">这样，将更快填充急需职位，因为通知会帮助招聘人员联系应聘者和在整个组织中交叉招聘应聘者。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="3ed8b-154">可扩展此模板，以便其可用于涉及 SharePoint 集成的任何方案。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="3ed8b-155">若要下载**流 – SharePoint 集成**模板，请转到 Microsoft 下载中心中的[流 – SharePoint 集成](https://go.microsoft.com/fwlink/?linkid=2082109)。</span><span class="sxs-lookup"><span data-stu-id="3ed8b-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>



## <a name="additional-resources"></a><span data-ttu-id="3ed8b-156">其他资源</span><span class="sxs-lookup"><span data-stu-id="3ed8b-156">Additional resources</span></span>

[<span data-ttu-id="3ed8b-157">该 Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="3ed8b-157">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="3ed8b-158">在租户与环境之间迁移应用</span><span class="sxs-lookup"><span data-stu-id="3ed8b-158">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
