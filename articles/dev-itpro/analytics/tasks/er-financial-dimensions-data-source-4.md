--- 
title: "运行使用财务维度作为数据源的报表"
description: "以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。"
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 47ba48461a1c502a93df416d1acac1e85a841079
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source"></a><span data-ttu-id="fe1fa-103">运行使用财务维度作为数据源的报表</span><span class="sxs-lookup"><span data-stu-id="fe1fa-103">Run a report that uses financial dimensions as a data source</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe1fa-104">以下步骤说明指定为系统管理员或电子申报开发人员角色的用户可以如何配置电子申报 (ER) 模型，以便将财务维度用作 ER 报表的数据源。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="fe1fa-105">这些步骤可以在 DEMF 公司执行。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="fe1fa-106">若要完成这些步骤，则必须首先完成“ER 将财务维度用作数据源（第 3 部分：设计报表）”过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="fe1fa-107">还必须在“电子申报参数”页面中配置默认单据类型。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="fe1fa-108">下载和导入任何 ER 配置时也设置默认单据类型。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="fe1fa-109">运行报表</span><span class="sxs-lookup"><span data-stu-id="fe1fa-109">Run report</span></span>
1. <span data-ttu-id="fe1fa-110">转到“组织管理”>“电子申报”>“配置”。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fe1fa-111">在树中，展开“财务维度示例模型”。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="fe1fa-112">在树中，选择“财务维度示例模型\分类日记帐报表”。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="fe1fa-113">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-113">Click Run.</span></span>
5. <span data-ttu-id="fe1fa-114">在“维度名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="fe1fa-115">若要选择当前公司中的所有维度，请输入以下内容：BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="fe1fa-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="fe1fa-116">扩展“要包括的记录”部分。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="fe1fa-117">单击“筛选器”。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-117">Click Filter.</span></span>
8. <span data-ttu-id="fe1fa-118">选择“分类日记帐”表和“日记帐批号”字段的行。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="fe1fa-119">在“标准”字段中，键入“00057”。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="fe1fa-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-120">Click OK.</span></span>
11. <span data-ttu-id="fe1fa-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-121">Click OK.</span></span>
    * <span data-ttu-id="fe1fa-122">检查生成的输出。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-122">Review the generated output.</span></span> <span data-ttu-id="fe1fa-123">请注意，设置的相应维度中的财务维度表示所选批次的每个交易。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="fe1fa-124">运行此报表并选择不同维度，以便了解该报表不依赖所选维度数量或为此 Dynamics 365 for Finance and Operations 实例配置的维度数量。</span><span class="sxs-lookup"><span data-stu-id="fe1fa-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


