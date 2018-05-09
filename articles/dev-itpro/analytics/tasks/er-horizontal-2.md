--- 
title: "运行使用可水平扩展的范围在 Excel 报表中动态添加列的格式"
description: "下列步骤介绍指定为系统管理员或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便将报表生成为 OPENXML 工作表 (Excel) 文件格式，在这种文件中，可以根据可水平扩展的范围动态创建所需列。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5c4538bd9f8c71108e7ec8fd9da2c2b914d76f13
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a><span data-ttu-id="9f691-103">运行使用可水平扩展的范围在 Excel 报表中动态添加列的格式</span><span class="sxs-lookup"><span data-stu-id="9f691-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f691-104">下列步骤介绍指定为系统管理员或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便将报表生成为 OPENXML 工作表 (Excel) 文件格式，在这种文件中，可以根据可水平扩展的范围动态创建所需列。</span><span class="sxs-lookup"><span data-stu-id="9f691-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="9f691-105">这些步骤可以在 DEMF 公司执行。</span><span class="sxs-lookup"><span data-stu-id="9f691-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="9f691-106">必须首先完成“ER 使用可水平扩展的范围在 Excel 报表中动态添加列（第 1 部分：设计格式）”过程中的步骤，才能完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="9f691-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="9f691-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="9f691-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="9f691-108">查找创建的格式</span><span class="sxs-lookup"><span data-stu-id="9f691-108">Find created format</span></span>
1. <span data-ttu-id="9f691-109">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="9f691-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9f691-110">在树中，展开“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="9f691-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="9f691-111">在树中，选择“财务维度示例模型\包含可水平扩展范围的示例报表”。</span><span class="sxs-lookup"><span data-stu-id="9f691-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="9f691-112">执行格式以创建 Excel 输出</span><span class="sxs-lookup"><span data-stu-id="9f691-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="9f691-113">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="9f691-113">Click Run.</span></span>
2. <span data-ttu-id="9f691-114">在“维度名称”字段中，键入“BusinessUnit;CostCenter;Department”。</span><span class="sxs-lookup"><span data-stu-id="9f691-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="9f691-115">在“维度名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9f691-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="9f691-116">若要选择当前公司的所有维度，请输入以下内容：BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="9f691-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="9f691-117">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="9f691-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="9f691-118">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="9f691-118">Click Filter.</span></span>
5. <span data-ttu-id="9f691-119">选择“分类日记帐”表和“日记帐批号”字段的行。</span><span class="sxs-lookup"><span data-stu-id="9f691-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="9f691-120">在“条件”字段中，键入“00057..00058”。</span><span class="sxs-lookup"><span data-stu-id="9f691-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="9f691-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="9f691-121">00057..00058</span></span>  
7. <span data-ttu-id="9f691-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9f691-122">Click OK.</span></span>
8. <span data-ttu-id="9f691-123">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9f691-123">Click OK.</span></span>
    * <span data-ttu-id="9f691-124">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="9f691-124">Review the generated output.</span></span> <span data-ttu-id="9f691-125">请注意，新创建的 Excel 文件中包含为财务维度选择的相同数量的列。</span><span class="sxs-lookup"><span data-stu-id="9f691-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="9f691-126">这些列中的报表标题表示财务维度的名称。</span><span class="sxs-lookup"><span data-stu-id="9f691-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="9f691-127">这些列中的交易行表示财务维度的名称。</span><span class="sxs-lookup"><span data-stu-id="9f691-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="9f691-128">运行此报表并选择不同维度，以便了解该报表不依赖所选维度数量或为此 Dynamics 365 for Finance and Operations 实例配置的维度数量。</span><span class="sxs-lookup"><span data-stu-id="9f691-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


