---
title: 内部公司支出
description: 由在组织中的一个法人雇佣的工作人员可能在同一组织执行其他法人的工作。 在此情况下，您可以使用内部公司费用功能来将工作人员的费用分配到执行该工作的法人。
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390876"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="37bac-104">内部公司支出</span><span class="sxs-lookup"><span data-stu-id="37bac-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37bac-105">由在组织中的一个法人雇佣的工作人员可能在同一组织执行其他法人的工作。</span><span class="sxs-lookup"><span data-stu-id="37bac-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="37bac-106">在此情况下，您可以使用内部公司费用功能来将工作人员的费用分配到执行该工作的法人。</span><span class="sxs-lookup"><span data-stu-id="37bac-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="37bac-107">雇用该工作人员的法人称为借出方法人。</span><span class="sxs-lookup"><span data-stu-id="37bac-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="37bac-108">工作人员产生费用的法人称为“借款法人”。</span><span class="sxs-lookup"><span data-stu-id="37bac-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="37bac-109">在工作人员可以为不同的法人执行工作的创建和提交费用之前，必须在借出法人中的**费用管理参数**页选择**允许内部公司支出行**选项。</span><span class="sxs-lookup"><span data-stu-id="37bac-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="37bac-110">内部公司费用的税金过帐</span><span class="sxs-lookup"><span data-stu-id="37bac-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37bac-111">如果要在费用报表中使用与借出方（源）法人而不是借入方（目标）法人 关联的税组，需要在设置总帐销售税时配置此设置。</span><span class="sxs-lookup"><span data-stu-id="37bac-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="37bac-112">如果总帐参数**内部公司税金过帐的法人**设置为**源**，并且**应用应用销售税纳税规则**设置为**否**时，将使用借出方法人的税务组合。</span><span class="sxs-lookup"><span data-stu-id="37bac-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="37bac-113">如果同一个参数设置为**目标**，将使用借入方法人的税务组合。</span><span class="sxs-lookup"><span data-stu-id="37bac-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="37bac-114">对于美国的法人来说，如果此参数设置为**源**，则还必须在新的**分类帐过帐组**页中配置**应收销售税**字段。</span><span class="sxs-lookup"><span data-stu-id="37bac-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="37bac-115">成本核算引擎将把此字段中的信息用于与税务有关的成本核算条目。</span><span class="sxs-lookup"><span data-stu-id="37bac-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="37bac-116">无论是否有项目，此行为对过帐的费用行都一致。</span><span class="sxs-lookup"><span data-stu-id="37bac-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
