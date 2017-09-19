--- 
title: "针对电子申报 (ER) 生成包含申请表数据更新的文档"
description: "若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 1 部分 - 导入配置）”这一过程。"
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aa737abc9273e0068d864416ffb85302468088ed
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="4cfc7-103">针对电子申报 (ER) 生成包含申请表数据更新的文档</span><span class="sxs-lookup"><span data-stu-id="4cfc7-103">Generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4cfc7-104">若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 1 部分：导入配置）”这一过程。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="4cfc7-105">此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="4cfc7-106">在此过程中，将运行已为示例公司 Litware 公司创建的 ER 导入格式配置，以便生成电子单据。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="4cfc7-107">此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="4cfc7-108">可使用 DEMF 数据集完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="4cfc7-109">首先，将 DEMF 公司的国家/地区上下文从 DEU（德国）更改为 BEL（比利时）。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="4cfc7-110">单击“组织管理”>“组织”>“法人”以更新法人 DEMF 的主地址中的国家/地区代码。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="4cfc7-111">重新启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="4cfc7-112">运行导入的 ER 格式</span><span class="sxs-lookup"><span data-stu-id="4cfc7-112">Run imported ER format</span></span>
1. <span data-ttu-id="4cfc7-113">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4cfc7-114">在树中，展开“内部统计(模型)”。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="4cfc7-115">在树中，选择“内部统计(模型)\内部统计(格式)”。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="4cfc7-116">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-116">Click Run.</span></span>
    * <span data-ttu-id="4cfc7-117">运行 ER 格式映射的草稿版本以生成内部统计报表。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="4cfc7-118">在“输入文件名”字段中，键入“intrastat.xml”。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="4cfc7-119">指定文件的名称。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="4cfc7-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-120">Click OK.</span></span>
    * <span data-ttu-id="4cfc7-121">检查生成的 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="4cfc7-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-122">Close the page.</span></span>
8. <span data-ttu-id="4cfc7-123">转到“纳税”>“申报”>“外贸”>“内部统计”。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="4cfc7-124">打开此窗体以查看所生成电子单据中包含的内部统计交易记录。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="4cfc7-125">单击“内部统计存档”。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="4cfc7-126">由于执行的 ER 格式中不包含应用程序数据更新的任何设置，所以尚未归档已完成内部统计报表的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="4cfc7-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-127">Close the page.</span></span>
11. <span data-ttu-id="4cfc7-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4cfc7-128">Close the page.</span></span>

