--- 
title: "设置增值税主管机构"
description: "销售税主管机构是收缴需要申报和缴纳的销售税的实体。"
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f75ee28343161026a73dd889b345d65ecc345884
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="592af-103">设置增值税主管机构</span><span class="sxs-lookup"><span data-stu-id="592af-103">Set up sales tax authorities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="592af-104">销售税主管机构是收缴需要申报和缴纳的销售税的实体。</span><span class="sxs-lookup"><span data-stu-id="592af-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="592af-105">您可以直接向销售税主管机构支付销售税，也可以通过为销售税主管机构创建的供应商帐户支付。</span><span class="sxs-lookup"><span data-stu-id="592af-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="592af-106">如果您这样做，公司可以使用其日常付款程序及时向增值税主管机构付款。</span><span class="sxs-lookup"><span data-stu-id="592af-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="592af-107">如果您没有将增值税主管机构设置为供应商，则某个人必须在相应的到期日期时准备向增值税主管机构手动付款。</span><span class="sxs-lookup"><span data-stu-id="592af-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="592af-108">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="592af-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="592af-109">转到“纳税”>“间接税”>“销售税”>“销售税主管机构”。</span><span class="sxs-lookup"><span data-stu-id="592af-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="592af-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="592af-110">Click New.</span></span>
3. <span data-ttu-id="592af-111">在“主管机构”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="592af-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="592af-112">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="592af-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="592af-113">在“供应商帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="592af-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="592af-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="592af-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="592af-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="592af-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="592af-116">为您的国家/地区选择报表版式（如果有）。</span><span class="sxs-lookup"><span data-stu-id="592af-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="592af-117">如果报表版式不对应于销售税主管机构的要求，请使用默认版式。</span><span class="sxs-lookup"><span data-stu-id="592af-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="592af-118">在舍入表格和“舍入”字段中输入数字，以指定支付的总税额如何舍入。</span><span class="sxs-lookup"><span data-stu-id="592af-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="592af-119">所有舍入差额将过帐到总帐中设置的自动交易记录的帐户。</span><span class="sxs-lookup"><span data-stu-id="592af-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="592af-120">在“舍入”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="592af-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="592af-121">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="592af-121">Click Save.</span></span>

