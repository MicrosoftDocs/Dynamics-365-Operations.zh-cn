---
title: 过帐支出报表
description: 本主题说明如何将支出报表过帐到总帐。
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176593"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="9f402-103">过帐支出报表</span><span class="sxs-lookup"><span data-stu-id="9f402-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f402-104">在支出报表已审核和转移到总帐后，可以将其过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="9f402-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="9f402-105">在您过帐支出报表时，将标识适用于增值税 (VAT) 回收的费用。</span><span class="sxs-lookup"><span data-stu-id="9f402-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="9f402-106">验证和回收增值税付款的任务被分配给负责验证支出报表的员工。</span><span class="sxs-lookup"><span data-stu-id="9f402-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="9f402-107">如果应向雇佣该员工的公司以外的其它公司收取支出报表中的费用， 您必须验证是哪个公司欠这笔费用，以及这笔费用应付给哪个公司。</span><span class="sxs-lookup"><span data-stu-id="9f402-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="9f402-108">例如，提交支出报表的员工为 DAT 工作，但是费用应向 DIR 公司收取。</span><span class="sxs-lookup"><span data-stu-id="9f402-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="9f402-109">在这种情况下，DAT 是费用的应收公司，DIR 是费用的应付公司。</span><span class="sxs-lookup"><span data-stu-id="9f402-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="9f402-110">在验证这些日志行后，可以将支出行过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="9f402-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="9f402-111">若要过帐支出报表，请在**已审核的支出报表**页面中选择支出报表，然后在操作窗格中选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="9f402-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="9f402-112">也可以一次性过帐列表中的所有支出报表。</span><span class="sxs-lookup"><span data-stu-id="9f402-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="9f402-113">选择所有支出报表，然后选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="9f402-113">Select all the expense reports, and then select **Post**.</span></span>
