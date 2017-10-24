---
title: "设置特定于公司的 HR 参数"
description: "某些人力资源 (HR) 参数的设置在公司间共享，而其他参数设置是特定于公司的。 本文说明如何设置特定于公司的人力资源参数。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c280b5ae3b8fc208759ec486db0a1015a9c24633
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-company-specific-hr-parameters"></a><span data-ttu-id="6dd4e-104">设置特定于公司的 HR 参数</span><span class="sxs-lookup"><span data-stu-id="6dd4e-104">Set up company-specific HR parameters</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="6dd4e-105">某些人力资源 (HR) 参数的设置在公司间共享，而其他参数设置是特定于公司的。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-105">The settings of some Human resources (HR) parameters are shared across companies, whereas the settings of other parameters are company-specific.</span></span> <span data-ttu-id="6dd4e-106">本文说明如何设置特定于公司的人力资源参数。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-106">This article explains how to set up company-specific HR parameters.</span></span>

<span data-ttu-id="6dd4e-107">提供了两个页面来设置人力资源 (HR) 参数。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-107">Two pages are used to set Human resources (HR) parameters.</span></span> <span data-ttu-id="6dd4e-108">对于跨公司共享的参数，您可使用**“人力资源共享参数”**页。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-108">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="6dd4e-109">对于特定于公司的参数（换句话说，这些设置将应用于单个公司），您可使用**“人力资源参数”**页。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-109">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span> <span data-ttu-id="6dd4e-110">在**“人力资源参数”**页上，设置在 6 个选项卡之间分配：</span><span class="sxs-lookup"><span data-stu-id="6dd4e-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

-   <span data-ttu-id="6dd4e-111">常规</span><span class="sxs-lookup"><span data-stu-id="6dd4e-111">General</span></span>
-   <span data-ttu-id="6dd4e-112">招聘 - 不包括在 Dynamics 365 for Talent 中</span><span class="sxs-lookup"><span data-stu-id="6dd4e-112">Recruitment - this is not included in Dynamics 365 for Talent</span></span>
-   <span data-ttu-id="6dd4e-113">薪酬</span><span class="sxs-lookup"><span data-stu-id="6dd4e-113">Compensation</span></span>
-   <span data-ttu-id="6dd4e-114">编号规则</span><span class="sxs-lookup"><span data-stu-id="6dd4e-114">Number sequences</span></span>
-   <span data-ttu-id="6dd4e-115">家庭医疗休假法 (FMLA)</span><span class="sxs-lookup"><span data-stu-id="6dd4e-115">Family and Medical Leave Act (FMLA)</span></span>
-   <span data-ttu-id="6dd4e-116">员工自助服务</span><span class="sxs-lookup"><span data-stu-id="6dd4e-116">Employee self-service</span></span>

<span data-ttu-id="6dd4e-117">每个选项卡均包含与单个公司有关的信息。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-117">Each tab contains information that pertains to a single company.</span></span> <span data-ttu-id="6dd4e-118">**“常规”**选项卡上的设置定义有关缺勤、伤害和疾病以及新的雇用的信息的外观。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-118">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="6dd4e-119">此选项卡上的设置还定义在您工作时显示的某些默认条目。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-119">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="6dd4e-120">具体而言，可使用此选项卡选择要应用于未结缺勤事务的颜色、指定要用于报表的样式表，启用培训课程和缺勤登记之间的集成，以及选择用于控制此集成的缺勤代码。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-120">Specifically, this tab lets you select a color to apply to open absence transactions, specify the style sheet to use for reports, enable the integration between training courses and absence registration, and select the absence code that is used to control this integration.</span></span> <span data-ttu-id="6dd4e-121">您还可以指示伤害和疾病案例事件的保留时长，并指定在雇用新工作人员时显示的默认标识号。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-121">You can also indicate how long injury and illness case incidents should be kept, and specify the default identification number that is shown when a new worker is hired.</span></span> 

<span data-ttu-id="6dd4e-122">**“招聘”**选项卡上的设置定义用于自动发送到申请人的通信的文档类型，以及用于主动提供的申请（不针对特定招聘项目的申请）的招聘项目。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-122">The settings on the **Recruitment** tab define the document types that are used for correspondence that is automatically sent to applicants, and the recruitment project that is used for unsolicited applications (applications that aren't for a specific recruitment project).</span></span> <span data-ttu-id="6dd4e-123">为招聘项目帐龄定义的期间确定包含在**“招聘管理”**工作区中的**“帐龄项目”**磁贴上的招聘项目。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-123">The period that is defined for the recruitment project aging determines the recruitment projects that are included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="6dd4e-124">为申请截止日期警告定义的期间用于显示接近其在**“招聘”**工作区中的**“接近申请截止日期”**磁贴上的申请截止日期的招聘项目。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-124">The period that is defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span> 

<span data-ttu-id="6dd4e-125">**薪酬**选项卡上的设置定义用户是否必须确认是希望保存固定薪酬计划的信息还是可变薪酬计划的信息。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-125">The settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="6dd4e-126">如果您选中**启用保存验证**复选框，则只要用户关闭与薪酬相关的页面，他们就会收到一条消息，询问是否需要保存记录。薪酬管理中的某些页面不允许用户删除信息。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-126">If you select the **Enable save validation** check box, any time that users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="6dd4e-127">薪酬管理中的某些页面不允许用户删除信息。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-127">Some pages in compensation management don't let users delete information.</span></span> <span data-ttu-id="6dd4e-128">因此，通过提示用户验证是否要保存信息，您也许能够限制可保存但稍后无法删除的信息量。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-128">Therefore, by prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="6dd4e-129">如果清除**“启用保存验证”**复选框，则始终将立即保存记录（可能在用户准备就绪之前）。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-129">If the **Enable save validation** check box is cleared, records are always saved immediately, possibly before the user is ready.</span></span> <span data-ttu-id="6dd4e-130">如果您使用绩效管理，则也可使用**“薪酬”**选项卡来选择要使用的评级模型，而不是选择在对绩效进行评级时分配给薪酬计划的模型。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-130">If you're using performance management, the **Compensation** tab also lets you select a rating model to use instead of the model that is assigned to compensation plans when performance is rated.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="6dd4e-131">以前发布的功能</span><span class="sxs-lookup"><span data-stu-id="6dd4e-131">Previously released functionality</span></span>
<span data-ttu-id="6dd4e-132">**“编号规则”**选项卡上的设置确定用于自动将 ID 分配到人力资源中的项目（例如，申请、缺勤登记、薪酬流程结果、案例编号、课程和课程安排）的顺序。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-132">The settings on the **Number sequence** tab determine the sequences that are used to automatically assign IDs to items in Human resources, such as applications, absence registrations, compensation process results, case numbers, courses, and course agendas.</span></span> <span data-ttu-id="6dd4e-133">要维护编号规则引用和代码，可使用**编号规则**列表页（单击**组织管理** &gt; **编号规则** &gt; **编号规则**）。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-133">To maintain number sequence references and codes, use the **Number sequences** list page (click **Organization administration** &gt; **Number sequences** &gt; **Number sequences**).</span></span>

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="6dd4e-134">如果您正在使用 Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="6dd4e-134">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="6dd4e-135">**“编号规则”**选项卡上的设置确定用于自动将 ID 分配到人力资源中的项目（例如，申请、缺勤登记、薪酬流程结果、案例编号、课程和课程安排）的顺序。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-135">The settings on the **Number sequence** tab determine the sequences that are used to automatically assign IDs to items in Human resources, such as applications, absence registrations, compensation process results, case numbers, courses, and course agendas.</span></span> <span data-ttu-id="6dd4e-136">要维护编号规则引用和代码，可使用**编号规则**列表页（单击**系统管理** &gt; **链接选项卡** &gt; **编号规则** &gt; **编号规则**）。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-136">To maintain number sequence references and codes, use the **Number sequences** list page (click **System administration** &gt; **Links tab** &gt; **Number sequences** &gt; **Number sequences**).</span></span> 

<span data-ttu-id="6dd4e-137">**“FMLA”**选项卡上的设置定义员工为获得享受 FMLA 权益的资格而必须工作的小时数、获得资格所需的雇用时长以及用于确定雇用时长的雇用开始日期。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-137">The settings on the **FMLA** tab define how many hours an employee must work in order to be eligible for FMLA benefits, the length of employment that is required for eligibility, and the employment start date that is used to determine the length of employment.</span></span> <span data-ttu-id="6dd4e-138">此类设置还定义员工有资格获得的 FMLA 小时数以及用于计算员工已使用的 FMLA 小时数的 FMLA 假期日历。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-138">The settings also define the number of FMLA hours that employees are entitled to and the FMLA leave calendar that is used to calculate how many FMLA hours employees have used.</span></span> <span data-ttu-id="6dd4e-139">**“FMLA”**选项卡仅对位于美国的公司可用。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-139">The **FMLA** tab is available only to companies in the United States.</span></span> 

<span data-ttu-id="6dd4e-140">**注意：**工作的小时数不能超过 1,250，雇用时长不能超过 12 个月。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-140">**Note:** The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="6dd4e-141">这些最大值符合美国的联邦法律。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-141">These maximum values are in accordance with federal law in the United States.</span></span> <span data-ttu-id="6dd4e-142">最后，**“员工自助服务”**选项卡确定经理可代表其员工输入的信息。</span><span class="sxs-lookup"><span data-stu-id="6dd4e-142">Finally, the settings on the **Employee self-service** tab determine the information that a manager can enter on behalf of his or her employees.</span></span>

<a name="see-also"></a><span data-ttu-id="6dd4e-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="6dd4e-143">See also</span></span>
--------

[<span data-ttu-id="6dd4e-144">设置法人之间的 HR 参数</span><span class="sxs-lookup"><span data-stu-id="6dd4e-144">Set up HR parameters across legal entities</span></span>](set-up-hr-parameters-across-legal-entities.md)



