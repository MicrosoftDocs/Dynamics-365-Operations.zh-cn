---
title: "设置法人之间的 HR 参数"
description: "您必须为在公司间共享的记录设置共享参数，例如职位记录。 本文说明如何设置跨法人的人力资源参数。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 90d348f8b8414d6e31092cdd18760375dd283155
ms.contentlocale: zh-cn
ms.lasthandoff: 06/29/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a><span data-ttu-id="bb8d8-104">设置法人之间的 HR 参数</span><span class="sxs-lookup"><span data-stu-id="bb8d8-104">Set up HR parameters across legal entities</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="bb8d8-105">您必须为在公司间共享的记录设置共享参数，例如职位记录。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="bb8d8-106">本文说明如何设置跨法人的人力资源参数。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="bb8d8-107">某些类型的记录（如位置记录）将在公司间共享。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="bb8d8-108">对于这些记录，您必须设置共享的参数。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="bb8d8-109">例如，您使用**“人力资源共享参数”**页设置法人之间的人力资源参数。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="bb8d8-110">在**“人力资源共享参数”**页上，将根据区域的功能将参数分组到相应区域中。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="bb8d8-111">以前发布的功能</span><span class="sxs-lookup"><span data-stu-id="bb8d8-111">Previously released functionality</span></span>
<span data-ttu-id="bb8d8-112">在**“标识”**选项卡上，您必须选择表示页面上列出的标识号的标识类型。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="bb8d8-113">在您可以输入工作的人员的标识信息之前，必须设置标识类型。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="bb8d8-114">有关社会保险号、国家/地区 ID 号、侨民 ID 号和个人 ID 代码的信息保留在**“标识类型”**页上。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="bb8d8-115">要定义新的标识类型或检查现有类型的列表，请单击**人事管理** &gt; **链接选项卡** &gt; **设置** &gt; **标识类型**。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="bb8d8-116">您可以输入简单的代码和描述。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="bb8d8-117">如果您正在使用 Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="bb8d8-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="bb8d8-118">在**“标识”**选项卡上，您必须选择表示页面上列出的标识号的标识类型。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="bb8d8-119">在您可以输入工作的人员的标识信息之前，必须设置标识类型。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="bb8d8-120">有关社会保险号、国家/地区 ID 号、侨民 ID 号和个人 ID 代码的信息保留在**“标识类型”**页上。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="bb8d8-121">要定义新的标识类型或检查现有类型的列表，请单击**人力资源** &gt; **设置** &gt; **标识类型**。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="bb8d8-122">您可以输入简单的代码和描述。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="bb8d8-123">在**“编号规则”**选项卡上，您可以选择用于以下记录的编号规则：人员编号、职位、用户请求 ID、I-9 文档、申请人、讨论、福利 ID 和人事操作（如果此记录类型已启用）。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="bb8d8-124">要维护编号规则引用和代码，请使用**“编号规则”**列表页。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="bb8d8-125">要查找此页，请使用页搜索功能。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="bb8d8-126">在**“职位”**选项卡上，指示新的职位在默认情况下是否可分配：</span><span class="sxs-lookup"><span data-stu-id="bb8d8-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="bb8d8-127">**始终** – 创建新的职位时，可将工作人员分配到这些职位。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="bb8d8-128">在创建职位时，**职位**页的**常规**选项卡上的**可进行分配的日期和时间**将自动设置为创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="bb8d8-129">**从不** – 创建新的职位时，您无法将工作人员分配到这些职位。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="bb8d8-130">如果选择此选项，则您必须在每个新职位可用时打开其**“职位”**页，然后在**“常规”**选项卡上，输入**“可用于分配”**日期以启用工作人员分配。</span><span class="sxs-lookup"><span data-stu-id="bb8d8-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="see-also"></a><span data-ttu-id="bb8d8-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb8d8-131">See also</span></span>
--------

[<span data-ttu-id="bb8d8-132">设置特定于公司的 HR 参数</span><span class="sxs-lookup"><span data-stu-id="bb8d8-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)




