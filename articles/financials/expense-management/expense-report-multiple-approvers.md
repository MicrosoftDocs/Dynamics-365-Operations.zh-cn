---
title: "支出报表和多个审核人"
description: "此主题介绍需要多人审核的支出报表。"
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 0f7592c580a21040c8b630885939ceaab3855c2c
ms.contentlocale: zh-cn
ms.lasthandoff: 03/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="30c51-103">支出报表和多个审核人</span><span class="sxs-lookup"><span data-stu-id="30c51-103">Expense reports and multiple approvers</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="30c51-104">根据您组织的支出审核策略，可能需要多人审核由员工提交的支出报表。</span><span class="sxs-lookup"><span data-stu-id="30c51-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="30c51-105">在您设置支出报表审核的工作流程时，可以添加包括一个或多个支出报表审核人的任务或步骤的工作流元素。</span><span class="sxs-lookup"><span data-stu-id="30c51-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="30c51-106">例如，您可能需要所有支出报表首先由提交报表的员工经理审核，然后由应付帐款协调员进行审核。</span><span class="sxs-lookup"><span data-stu-id="30c51-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="30c51-107">如果您决定需要多个支出报表审核人，您可以添加在以下任何方法中的工作流元素：</span><span class="sxs-lookup"><span data-stu-id="30c51-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="30c51-108">添加包含一个步骤的一个审核元素。</span><span class="sxs-lookup"><span data-stu-id="30c51-108">Add one approval element that has one step.</span></span> <span data-ttu-id="30c51-109">例如，该步骤可能要求将支出报表分配给用户组，并且由 50% 的用户组成员进行审核。</span><span class="sxs-lookup"><span data-stu-id="30c51-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="30c51-110">添加包含多个步骤的一个审核元素。</span><span class="sxs-lookup"><span data-stu-id="30c51-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="30c51-111">例如，审核元素可能包含以下步骤：</span><span class="sxs-lookup"><span data-stu-id="30c51-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="30c51-112">由提交支出报表的员工经理审核。</span><span class="sxs-lookup"><span data-stu-id="30c51-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="30c51-113">应付帐款职员验证收据和支出报表物料。</span><span class="sxs-lookup"><span data-stu-id="30c51-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="30c51-114">由预算所有者审核支出报表。</span><span class="sxs-lookup"><span data-stu-id="30c51-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="30c51-115">添加多个审核元素，每个审核元素中包含一个步骤。</span><span class="sxs-lookup"><span data-stu-id="30c51-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="30c51-116">例如，您可以为下面的每个步骤添加一个单独的审核元素：</span><span class="sxs-lookup"><span data-stu-id="30c51-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="30c51-117">员工经理审核支出报表。</span><span class="sxs-lookup"><span data-stu-id="30c51-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="30c51-118">由预算所有者审核支出报表。</span><span class="sxs-lookup"><span data-stu-id="30c51-118">The budget owner approves the expense report.</span></span>

