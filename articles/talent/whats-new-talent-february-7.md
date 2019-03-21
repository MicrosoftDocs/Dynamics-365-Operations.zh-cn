---
title: Dynamics 365 for Talent（2019 年 2 月 7 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 23386d04fac5a41682d3ced448ce07e6729def3c
ms.sourcegitcommit: b3b21795f36e5852ffe18200d6fe0b93363b1cbd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2019
ms.locfileid: "377723"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-7-2019"></a><span data-ttu-id="1cf99-103">Dynamics 365 for Talent（2019 年 2 月 7 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="1cf99-103">What's new or changed in Dynamics 365 for Talent (February 7, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1cf99-104">此主题介绍了 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="1cf99-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="1cf99-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="1cf99-105">Changes in Attract</span></span>

### <a name="interview-scheduling-enhancements"></a><span data-ttu-id="1cf99-106">面试计划增强</span><span class="sxs-lookup"><span data-stu-id="1cf99-106">Interview scheduling enhancements</span></span>
<span data-ttu-id="1cf99-107">端对端面试计划体验已改进。</span><span class="sxs-lookup"><span data-stu-id="1cf99-107">Improvements have been made to the end-to-end interview scheduling experience.</span></span> <span data-ttu-id="1cf99-108">现在可查看内部应聘者的日历可用日期，并可以使用内部应聘者的日历来获取计划建议。</span><span class="sxs-lookup"><span data-stu-id="1cf99-108">You can now see the calendar availability of an internal candidate and use the internal candidate’s calendar for schedule recommendations.</span></span> <span data-ttu-id="1cf99-109">有关详细信息，请参阅[面试计划和反馈](interview-scheduling-feedback.md)。</span><span class="sxs-lookup"><span data-stu-id="1cf99-109">For more information, see [Interview scheduling and feedback](interview-scheduling-feedback.md).</span></span>

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a><span data-ttu-id="1cf99-110">工作发布到 LinkedIn – 已解决了公司不匹配问题</span><span class="sxs-lookup"><span data-stu-id="1cf99-110">Job posting to LinkedIn – company mismatch issue fixed</span></span>
<span data-ttu-id="1cf99-111">已解决了从 Attract 发布到LinkedIn 的工作在错误的公司名下显示这一问题。</span><span class="sxs-lookup"><span data-stu-id="1cf99-111">An issue has been fixed where jobs posted to LinkedIn from Attract were appearing under the wrong company name.</span></span> <span data-ttu-id="1cf99-112">有关详细信息，请参阅[在 Attract 中创建、审核和发布工作](creating-jobs-attract.md)。</span><span class="sxs-lookup"><span data-stu-id="1cf99-112">For more information, see [Create, approve, and post jobs in Attract](creating-jobs-attract.md).</span></span>

### <a name="career-site-url-displayed-in-admin-settings"></a><span data-ttu-id="1cf99-113">求职站点 URL 在“管理员设置”中显示</span><span class="sxs-lookup"><span data-stu-id="1cf99-113">Career site URL displayed in Admin settings</span></span>
<span data-ttu-id="1cf99-114">求职站点主页 URL 现在在**求职站点管理**下的**管理员设置**中显示。</span><span class="sxs-lookup"><span data-stu-id="1cf99-114">The career site home page URL is now displayed in **Admin Settings** under **Career Site management**.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="1cf99-115">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="1cf99-115">Changes in Core HR</span></span>

<span data-ttu-id="1cf99-116">**内部版本 8.1.2134**</span><span class="sxs-lookup"><span data-stu-id="1cf99-116">**Build 8.1.2134**</span></span>

### <a name="multiple-compensation-levels-supported-on-jobs"></a><span data-ttu-id="1cf99-117">工作支持多个薪酬级别</span><span class="sxs-lookup"><span data-stu-id="1cf99-117">Multiple compensation levels supported on jobs</span></span>
<span data-ttu-id="1cf99-118">可通过此更改为某个工作定义多个薪酬级别，从而在使用该工作时支持计划之间可能不同的员工固定薪酬范围。</span><span class="sxs-lookup"><span data-stu-id="1cf99-118">This change allows for more than one compensation level to be defined on a job, enabling employee fixed compensation ranges which may differ between plans when using the same job.</span></span> 

<span data-ttu-id="1cf99-119">例如:</span><span class="sxs-lookup"><span data-stu-id="1cf99-119">For example:</span></span>    
<span data-ttu-id="1cf99-120">*工作* - 客户经理*关联的薪酬级别：* B1 和 B2 - 每个级别都有一个定义的值范围。</span><span class="sxs-lookup"><span data-stu-id="1cf99-120">*Job* - Account Manager *Associated compensation levels:* B1 and B2 - Each level has a defined range of values.</span></span> <span data-ttu-id="1cf99-121">B1 = 最低为 50,000，中等为 60,000，最高为 75,000，B2 = 最低为 65,000，中等为 74,000，最高为 85,000。</span><span class="sxs-lookup"><span data-stu-id="1cf99-121">B1 = Min 50,000, Mid 60,000, Max 75,000 and B2 = Min 65,000, Mid 74,000, Max 85,000.</span></span> <span data-ttu-id="1cf99-122">根据定义的资格规则为员工创建固定薪酬时，每个固定计划现在可指向同一个工作和该工作的不同级别。</span><span class="sxs-lookup"><span data-stu-id="1cf99-122">When creating fixed compensation for employees, based on the eligibility rules defined, each fixed plan can now point to the same job and to different levels on the job.</span></span> <span data-ttu-id="1cf99-123">这样就可以在不同区域/国家或地区中定义计划，并且计划可指向不含重复工作但范围不同的同一个工作，以考虑这些差异。</span><span class="sxs-lookup"><span data-stu-id="1cf99-123">This allows for plans to be defined in different regions/companies and point to the same job but different ranges without duplicating jobs to account for these differences.</span></span>

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a><span data-ttu-id="1cf99-124">已向员工固定薪酬实体添加了薪酬级别字段。</span><span class="sxs-lookup"><span data-stu-id="1cf99-124">Compensation level field has been added to the Employee fixed compensation entity</span></span> 
<span data-ttu-id="1cf99-125">通过此更新，已将员工固定薪酬实体更新为包含**薪酬级别**字段。</span><span class="sxs-lookup"><span data-stu-id="1cf99-125">With this update, the employee fixed compensation entity has been updated to include the **Compensation level** field.</span></span> <span data-ttu-id="1cf99-126">通过添加此项功能，可以更轻松地更新员工固定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="1cf99-126">This addition makes it easier to update employee fixed compensation plans.</span></span> 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a><span data-ttu-id="1cf99-127">更新和新建职位时更新工作系列</span><span class="sxs-lookup"><span data-stu-id="1cf99-127">Update Job family when updating and creating new positions</span></span>
<span data-ttu-id="1cf99-128">更改某项职位的工作时，**工作系列**现在默认基于所选工作。</span><span class="sxs-lookup"><span data-stu-id="1cf99-128">When changing the job on a position, **Job family** will now default based on the job selected.</span></span>

### <a name="performance-improvements-when-rendering-workspaces"></a><span data-ttu-id="1cf99-129">呈现工作区方面的性能改进</span><span class="sxs-lookup"><span data-stu-id="1cf99-129">Performance improvements when rendering workspaces</span></span>
<span data-ttu-id="1cf99-130">仅当访问这些页面时，才加载工作区中的分析选项卡。</span><span class="sxs-lookup"><span data-stu-id="1cf99-130">Analytics tabs on workspaces will now load only when accessing those pages.</span></span> <span data-ttu-id="1cf99-131">首次呈现页面时，将在页面的左上角显示一个指示器。</span><span class="sxs-lookup"><span data-stu-id="1cf99-131">An indicator will display during the initial rendering of the page in the upper-left corner of the page.</span></span>
