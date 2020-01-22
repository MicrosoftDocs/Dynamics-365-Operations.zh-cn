---
title: Dynamics 365 Talent 的新增功能或更改（2019 年 7 月 30 日）
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 07/30/2019
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 96937d48e0d1003adbc5f7fedc89b2686ace01cd
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899016"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-30-2019"></a><span data-ttu-id="3f782-103">Dynamics 365 Talent 的新增功能或更改（2019 年 7 月 30 日）</span><span class="sxs-lookup"><span data-stu-id="3f782-103">What's new or changed in Dynamics 365 Talent (July 30, 2019)</span></span>

<span data-ttu-id="3f782-104">此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="3f782-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="3f782-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="3f782-105">Changes in Attract</span></span>
<span data-ttu-id="3f782-106">本版本中包含 Dynamics 365 Talent: Attract 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="3f782-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="3f782-107">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="3f782-107">Changes in Onboard</span></span>
<span data-ttu-id="3f782-108">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="3f782-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="3f782-109">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="3f782-109">Changes in Core HR</span></span>
<span data-ttu-id="3f782-110">本部分中的更改适用于内部版本号 8.1.2409。</span><span class="sxs-lookup"><span data-stu-id="3f782-110">Changes described in this section apply to build number 8.1.2409.</span></span>


### <a name="region-support-for-canada-and-southeast-asia"></a><span data-ttu-id="3f782-111">加拿大和东南亚的地区支持</span><span class="sxs-lookup"><span data-stu-id="3f782-111">Region support for Canada and Southeast Asia</span></span>

<span data-ttu-id="3f782-112">我们很高兴地宣布，加拿大和东南亚地区将于 2019 年 8 月 1 日推出 Talent。</span><span class="sxs-lookup"><span data-stu-id="3f782-112">We are pleased to announce that Canada and Southeast Asia regions will be available for Talent on August 1, 2019.</span></span> <span data-ttu-id="3f782-113">通过此更改，您可以在加拿大和亚洲地区创建环境，并且所有 Talent 数据将仅在这些位置内维护。</span><span class="sxs-lookup"><span data-stu-id="3f782-113">With this change, you can create environments in the Canadian and Asian regions, and all Talent data will be maintained solely within those locations.</span></span> <span data-ttu-id="3f782-114">您可以通过在“新建环境”对话框中选择位置来在这些新地区创建环境，并使用该环境在 LCS 中配置 Talent，如[配置 Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) 中所述。</span><span class="sxs-lookup"><span data-stu-id="3f782-114">You can create an environment in these new regions by selecting the location in the New Environment dialog and use that environment to provision Talent in LCS as described in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="3f782-115">不支持将现有项目的数据从其他地区迁移到加拿大和亚洲地区。</span><span class="sxs-lookup"><span data-stu-id="3f782-115">Data migration of existing projects from other regions to the Canadian and Asian regions is not supported.</span></span> <span data-ttu-id="3f782-116">仅新项目可以配置到这些新的支持地区。</span><span class="sxs-lookup"><span data-stu-id="3f782-116">Only new projects can be provisioned to these new supported regions.</span></span>

### <a name="new-active-positions-list-page"></a><span data-ttu-id="3f782-117">新的有效职位列表页</span><span class="sxs-lookup"><span data-stu-id="3f782-117">New Active positions list page</span></span>

<span data-ttu-id="3f782-118">基于位置的列表的选项现在包括：**所有职位**、**有效职位**、**空缺职位**和**无效职位**。</span><span class="sxs-lookup"><span data-stu-id="3f782-118">The options for position-based lists now include: **All positions**, **Active positions**, **Open positions**, and **Inactive positions**.</span></span> <span data-ttu-id="3f782-119">新的**有效职位**列表页面仅显示截至当前日期的有效位置（空缺或已填补）。</span><span class="sxs-lookup"><span data-stu-id="3f782-119">The new **Active positions** list page displays only those positions, open or filled, that are active as of the current date.</span></span> 

### <a name="allow-course-participants-to-be-added-to-open-courses"></a><span data-ttu-id="3f782-120">允许课程参与者被添加到开设的课程</span><span class="sxs-lookup"><span data-stu-id="3f782-120">Allow course participants to be added to open courses</span></span>

<span data-ttu-id="3f782-121">本周的更改更正了仅直接下属可以注册开设的课程的问题。</span><span class="sxs-lookup"><span data-stu-id="3f782-121">This week's changes correct an issue where only direct reports can be registered for open courses.</span></span>

### <a name="fte-analysis-displaying-incorrect-fte-number"></a><span data-ttu-id="3f782-122">FTE 分析显示不正确的 FTE 编号</span><span class="sxs-lookup"><span data-stu-id="3f782-122">FTE Analysis displaying incorrect FTE number</span></span>

<span data-ttu-id="3f782-123">**FTE 分析**已在**人事管理**的**分析**选项卡中得到更正。</span><span class="sxs-lookup"><span data-stu-id="3f782-123">**FTE analysis** has been corrected on the **Analytics** tab for **Personnel management**.</span></span>

### <a name="final-comments-label-translation"></a><span data-ttu-id="3f782-124">最终注释标签翻译</span><span class="sxs-lookup"><span data-stu-id="3f782-124">Final comments label translation</span></span>

<span data-ttu-id="3f782-125">**最终注释**标签现在在审核窗体中翻译。</span><span class="sxs-lookup"><span data-stu-id="3f782-125">The **Final comments** label is now translated in the review form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="3f782-126">预览模式</span><span class="sxs-lookup"><span data-stu-id="3f782-126">In preview</span></span>

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a><span data-ttu-id="3f782-127">只有沙盒实例中才会启用预览功能</span><span class="sxs-lookup"><span data-stu-id="3f782-127">Preview features are enabled only in sandbox instances</span></span>

<span data-ttu-id="3f782-128">配置新的 Talent 实例时，可指定实例类型为**生产**还是**沙盒**。</span><span class="sxs-lookup"><span data-stu-id="3f782-128">When you provision a new instance of Talent, you can specify whether the instance type is **Production** or **Sandbox**.</span></span> <span data-ttu-id="3f782-129">**沙盒**类型的实例可用于提前测试新功能。</span><span class="sxs-lookup"><span data-stu-id="3f782-129">Instances of the **Sandbox** type allow for early testing of new features.</span></span> <span data-ttu-id="3f782-130">将把所有现有 Talent 实例更新为**生产**实例类型。</span><span class="sxs-lookup"><span data-stu-id="3f782-130">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="3f782-131">如果需要将现有实例之一更新为**沙盒**实例类型，请联系[支持](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support)以发起更改请求。</span><span class="sxs-lookup"><span data-stu-id="3f782-131">If you want one of your existing instances to be updated to the **Sandbox** instance type, contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

<span data-ttu-id="3f782-132">有关如何发布更改的详细信息，请参阅[配置 Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。</span><span class="sxs-lookup"><span data-stu-id="3f782-132">For more information about how changes are published, see [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

### <a name="view-extended-information-for-performance-in-manager-self-service"></a><span data-ttu-id="3f782-133">在经理自助服务中查看绩效的更多信息</span><span class="sxs-lookup"><span data-stu-id="3f782-133">View extended information for performance in manager self-service</span></span>

<span data-ttu-id="3f782-134">经理可通过一个新选项查看直接报表和扩展报表的绩效。</span><span class="sxs-lookup"><span data-stu-id="3f782-134">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="3f782-135">现在，职能经理可以分配和更新绩效目标和颁发新审核。</span><span class="sxs-lookup"><span data-stu-id="3f782-135">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="3f782-136">此外，直属经理及其员工可维护和更新绩效日记帐，以帮助确保绩效复查流程顺利进行。</span><span class="sxs-lookup"><span data-stu-id="3f782-136">In addition, direct managers and their employees can maintain and update performance journals to help ensure that the performance review process goes smoothly.</span></span> <span data-ttu-id="3f782-137">实施此更改后，除了直接报表，经理还可以查看和维护与其扩展报表的绩效有关的信息。</span><span class="sxs-lookup"><span data-stu-id="3f782-137">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>
