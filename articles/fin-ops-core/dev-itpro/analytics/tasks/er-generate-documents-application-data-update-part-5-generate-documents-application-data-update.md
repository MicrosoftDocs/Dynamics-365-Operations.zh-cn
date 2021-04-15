---
title: 生成包含应用程序数据的单据
description: 若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 4 部分 - 修改格式）”这一过程。
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2591f5b32417dd7517f76fc237d2337af64b3f61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745027"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="42f55-103">生成包含应用程序数据的单据</span><span class="sxs-lookup"><span data-stu-id="42f55-103">Generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42f55-104">若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 4 部分：修改格式）”这一过程。</span><span class="sxs-lookup"><span data-stu-id="42f55-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 4: Modify format)".</span></span>



<span data-ttu-id="42f55-105">此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据和更新应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="42f55-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="42f55-106">在此过程中，将执行 ER 格式配置以生成内部统计报表，并更新应用程序数据以存档报告流程的详细信息。</span><span class="sxs-lookup"><span data-stu-id="42f55-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="42f55-107">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="42f55-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="42f55-108">可使用 DEMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="42f55-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="42f55-109">首先，确保 DEMF 公司的国家/地区上下文为 BEL（比利时）。</span><span class="sxs-lookup"><span data-stu-id="42f55-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="42f55-110">设置外贸参数</span><span class="sxs-lookup"><span data-stu-id="42f55-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="42f55-111">转到缴税>设置 >外贸>外贸参数。</span><span class="sxs-lookup"><span data-stu-id="42f55-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="42f55-112">单击“数序”选项卡。</span><span class="sxs-lookup"><span data-stu-id="42f55-112">Click the Number sequences tab.</span></span>

    <span data-ttu-id="42f55-113">存档内部统计报告流程的详细信息时，需要标识所创建各存档的记录。</span><span class="sxs-lookup"><span data-stu-id="42f55-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="42f55-114">必须为其配置特殊编号规则。</span><span class="sxs-lookup"><span data-stu-id="42f55-114">A special number sequence must be configured for that.</span></span>  

3. <span data-ttu-id="42f55-115">选择“内部统计存档标识”参考。</span><span class="sxs-lookup"><span data-stu-id="42f55-115">Select the 'Intrastat archive ID' reference.</span></span>
4. <span data-ttu-id="42f55-116">在“编号规则代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="42f55-116">In the Number sequence code field, type a value.</span></span>

    <span data-ttu-id="42f55-117">在“编号规则代码”字段中，输入或选择值“Fore_2”。</span><span class="sxs-lookup"><span data-stu-id="42f55-117">In the 'Number sequence code' field, enter or select the value 'Fore_2'.</span></span>  

5. <span data-ttu-id="42f55-118">对编号规则代码执行 ResolveChanges。</span><span class="sxs-lookup"><span data-stu-id="42f55-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="42f55-119">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="42f55-119">Click Save.</span></span>
7. <span data-ttu-id="42f55-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="42f55-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="42f55-121">运行修改后的 ER 格式</span><span class="sxs-lookup"><span data-stu-id="42f55-121">Run modified ER format</span></span>
1. <span data-ttu-id="42f55-122">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="42f55-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="42f55-123">在树中，展开“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="42f55-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="42f55-124">在树中，选择“内部统计(模型)\内部统计(格式)”。</span><span class="sxs-lookup"><span data-stu-id="42f55-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="42f55-125">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="42f55-125">Click Run.</span></span>
5. <span data-ttu-id="42f55-126">在“输入文件名”字段中，键入“intrastat2.xml”。</span><span class="sxs-lookup"><span data-stu-id="42f55-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
6. <span data-ttu-id="42f55-127">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="42f55-127">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="42f55-128">检查 ER 格式执行结果</span><span class="sxs-lookup"><span data-stu-id="42f55-128">Review ER format execution's results</span></span>
<span data-ttu-id="42f55-129">检查生成的 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="42f55-129">Review the generated XML file.</span></span>  
1. <span data-ttu-id="42f55-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="42f55-130">Close the page.</span></span>
2. <span data-ttu-id="42f55-131">转到“纳税”>“申报”>“外贸”>“内部统计”。</span><span class="sxs-lookup"><span data-stu-id="42f55-131">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>

    <span data-ttu-id="42f55-132">打开此窗体（其中包含已包括的内部统计交易记录）以查看所生成电子单据。</span><span class="sxs-lookup"><span data-stu-id="42f55-132">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  

3. <span data-ttu-id="42f55-133">单击“内部统计存档”。</span><span class="sxs-lookup"><span data-stu-id="42f55-133">Click Intrastat archive.</span></span>

    <span data-ttu-id="42f55-134">由于执行的 ER 格式中现在包含应用程序数据更新的任何设置，所以已归档已完成内部统计报告的详细信息。</span><span class="sxs-lookup"><span data-stu-id="42f55-134">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="42f55-135">在此窗体中，可以查看创建的存档的标题记录。</span><span class="sxs-lookup"><span data-stu-id="42f55-135">In this form, you can see the header record of the created archive.</span></span>  

4. <span data-ttu-id="42f55-136">单击“详细信息”。</span><span class="sxs-lookup"><span data-stu-id="42f55-136">Click Details.</span></span>

    <span data-ttu-id="42f55-137">在此窗体中，可以查看创建的存档的详细信息。</span><span class="sxs-lookup"><span data-stu-id="42f55-137">In this form, you can see the details for the created archive.</span></span>  

5. <span data-ttu-id="42f55-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="42f55-138">Close the page.</span></span>
6. <span data-ttu-id="42f55-139">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="42f55-139">Close the page.</span></span>
7. <span data-ttu-id="42f55-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="42f55-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]