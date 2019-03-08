---
title: 手动输入申请人和申请表数据
description: 此过程显示如何手动维护申请人及其申请表的信息。
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60b3d155826d234744c9805b18edf0226e237ed3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "364526"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="7ab98-103">手动输入申请人和申请表数据</span><span class="sxs-lookup"><span data-stu-id="7ab98-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ab98-104">此过程显示如何手动维护申请人及其申请表的信息。</span><span class="sxs-lookup"><span data-stu-id="7ab98-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="7ab98-105">您可以输入和维护个人信息、面试日期和时间、推荐人、能力和申请人的住宿请求。</span><span class="sxs-lookup"><span data-stu-id="7ab98-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="7ab98-106">您还可以更新申请人的工作申请状态，以及写信或发送电子邮件与申请人沟通。</span><span class="sxs-lookup"><span data-stu-id="7ab98-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="7ab98-107">在您创建申请人记录时，在全球通讯簿中创建该申请人的人员记录。</span><span class="sxs-lookup"><span data-stu-id="7ab98-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="7ab98-108">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="7ab98-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="7ab98-109">创建新的申请人记录</span><span class="sxs-lookup"><span data-stu-id="7ab98-109">Create a new applicant record</span></span>
1. <span data-ttu-id="7ab98-110">转到“人力资源”>“招聘”>“申请人”>“申请人”。</span><span class="sxs-lookup"><span data-stu-id="7ab98-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="7ab98-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7ab98-111">Click New.</span></span>
3. <span data-ttu-id="7ab98-112">在“名字”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7ab98-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="7ab98-113">在“姓氏”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7ab98-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="7ab98-114">可以输入申请人的其他信息（如有）。</span><span class="sxs-lookup"><span data-stu-id="7ab98-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="7ab98-115">例如，可包含申请人的最高学历、当前职务或前雇主等信息。</span><span class="sxs-lookup"><span data-stu-id="7ab98-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="7ab98-116">切换“联系信息”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="7ab98-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="7ab98-117">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="7ab98-117">Click Add.</span></span>
7. <span data-ttu-id="7ab98-118">在“描述”字段中，键入“通信电子邮件”。</span><span class="sxs-lookup"><span data-stu-id="7ab98-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="7ab98-119">在“类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="7ab98-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="7ab98-120">在“联系电话/地址”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7ab98-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="7ab98-121">此电子邮件地址将用于生成与申请人通信的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="7ab98-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="7ab98-122">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="7ab98-122">Click Add.</span></span>
11. <span data-ttu-id="7ab98-123">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7ab98-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="7ab98-124">在“联系电话/地址”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7ab98-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="7ab98-125">申请人个人信息。</span><span class="sxs-lookup"><span data-stu-id="7ab98-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="7ab98-126">如果需要，可以输入申请人的其他个人信息。</span><span class="sxs-lookup"><span data-stu-id="7ab98-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="7ab98-127">例如，这可能包括出生日期、种族血统、性别或婚姻状况。</span><span class="sxs-lookup"><span data-stu-id="7ab98-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="7ab98-128">在操作窗格上，单击“能力”。</span><span class="sxs-lookup"><span data-stu-id="7ab98-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="7ab98-129">您可以输入申请人的能力资料，包括其技能、专业经验、教育程度、测试或证书。</span><span class="sxs-lookup"><span data-stu-id="7ab98-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="7ab98-130">此信息可用于反应申请人是否具有与公司数据定义的工作相关的技能。</span><span class="sxs-lookup"><span data-stu-id="7ab98-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="7ab98-131">为申请人创建申请表。</span><span class="sxs-lookup"><span data-stu-id="7ab98-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="7ab98-132">单击“申请表”。</span><span class="sxs-lookup"><span data-stu-id="7ab98-132">Click Applications.</span></span>
2. <span data-ttu-id="7ab98-133">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7ab98-133">Click New.</span></span>
3. <span data-ttu-id="7ab98-134">在“招聘项目”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="7ab98-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7ab98-135">选择招聘项目，将申请人与该招聘项目中包含的特定开放职位关联起来。</span><span class="sxs-lookup"><span data-stu-id="7ab98-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="7ab98-136">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="7ab98-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7ab98-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7ab98-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7ab98-138">默认情况下，工作和部门基于所选的招聘项目。</span><span class="sxs-lookup"><span data-stu-id="7ab98-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="7ab98-139">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7ab98-139">Click Save.</span></span>
    * <span data-ttu-id="7ab98-140">在保存申请表后，您可以添加文档附件，包括申请人的经验、所获奖项和求职信。</span><span class="sxs-lookup"><span data-stu-id="7ab98-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

