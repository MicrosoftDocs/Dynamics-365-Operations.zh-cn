---
title: ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 2 部分 - 运行格式）
description: 本主题介绍如何配置电子报告 (ER) 格式以将报表生成为 OPENXML 工作表 (Excel) 文件。 （第 2 部分）
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a62bad6ca241a2372a72e312ec5a707008a5fc09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744979"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="998d7-104">ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 2 部分 - 运行格式）</span><span class="sxs-lookup"><span data-stu-id="998d7-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="998d7-105">下列步骤介绍指定为系统管理员或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便将报表生成为 OPENXML 工作表 (Excel) 文件格式，在这种文件中，可以根据可水平扩展的范围动态创建所需列。</span><span class="sxs-lookup"><span data-stu-id="998d7-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="998d7-106">这些步骤可以在 DEMF 公司执行。</span><span class="sxs-lookup"><span data-stu-id="998d7-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="998d7-107">必须首先完成“ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 1 部分：设计格式）”过程中的步骤，才能完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="998d7-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="998d7-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="998d7-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="998d7-109">查找创建的格式</span><span class="sxs-lookup"><span data-stu-id="998d7-109">Find created format</span></span>
1. <span data-ttu-id="998d7-110">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="998d7-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="998d7-111">在树中，展开“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="998d7-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="998d7-112">在树中，选择“财务维度示例模型\包含可水平扩展范围的示例报表”。</span><span class="sxs-lookup"><span data-stu-id="998d7-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="998d7-113">执行格式以创建 Excel 输出</span><span class="sxs-lookup"><span data-stu-id="998d7-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="998d7-114">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="998d7-114">Click Run.</span></span>
2. <span data-ttu-id="998d7-115">在“维度名称”字段中，键入“BusinessUnit;CostCenter;Department”。</span><span class="sxs-lookup"><span data-stu-id="998d7-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="998d7-116">在“维度名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="998d7-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="998d7-117">若要选择当前公司的所有维度，请输入以下内容：BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="998d7-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="998d7-118">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="998d7-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="998d7-119">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="998d7-119">Click Filter.</span></span>
5. <span data-ttu-id="998d7-120">选择“分类日记帐”表和“日记帐批号”字段的行。</span><span class="sxs-lookup"><span data-stu-id="998d7-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="998d7-121">在“条件”字段中，键入“00057..00058”。</span><span class="sxs-lookup"><span data-stu-id="998d7-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="998d7-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="998d7-122">00057..00058</span></span>  
7. <span data-ttu-id="998d7-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="998d7-123">Click OK.</span></span>
8. <span data-ttu-id="998d7-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="998d7-124">Click OK.</span></span>
    * <span data-ttu-id="998d7-125">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="998d7-125">Review the generated output.</span></span> <span data-ttu-id="998d7-126">请注意，新创建的 Excel 文件中包含为财务维度选择的相同数量的列。</span><span class="sxs-lookup"><span data-stu-id="998d7-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="998d7-127">这些列中的报表标题表示财务维度的名称。</span><span class="sxs-lookup"><span data-stu-id="998d7-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="998d7-128">这些列中的交易行表示财务维度的名称。</span><span class="sxs-lookup"><span data-stu-id="998d7-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="998d7-129">运行此报表并选择不同维度，以便了解该报表不依赖所选维度数量或为此实例配置的维度数量。</span><span class="sxs-lookup"><span data-stu-id="998d7-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]