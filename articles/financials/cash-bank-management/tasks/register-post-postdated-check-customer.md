--- 
title: "为客户登记和过帐远期支票"
description: "您可以登记从客户处接收的远期支票的详细信息。"
author: kweekley
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
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1610036815349f625a67d5dd67260114d42fff97
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="4101c-103">为客户登记和过帐远期支票</span><span class="sxs-lookup"><span data-stu-id="4101c-103">Register and post a postdated check for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4101c-104">您可以登记从客户处接收的远期支票的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4101c-104">You can register details of a postdated cheque received from a customer.</span></span> <span data-ttu-id="4101c-105">您还可以过帐该远期发票并生成财务交易记录。</span><span class="sxs-lookup"><span data-stu-id="4101c-105">You can also post the postdated cheque and generate financial transactions.</span></span>   <span data-ttu-id="4101c-106">在您登记和过帐从客户收到的远期支票之前，请完成以下任务：   • 在现金和银行管理页面设置远期支票 • 设置远期支票的付款方式   此过程的角色为出纳员。</span><span class="sxs-lookup"><span data-stu-id="4101c-106">Complete the following tasks before you register and post a postdated cheque received from a customer:   • Set up postdated Cheques in the Cash and bank management page • Set up a method of payment for postdated Cheques   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="4101c-107">该程序适用于 USMF 演示公司。</span><span class="sxs-lookup"><span data-stu-id="4101c-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="4101c-108">转到“应收账款”>“付款”>“付款日记帐”。</span><span class="sxs-lookup"><span data-stu-id="4101c-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="4101c-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="4101c-109">Click New.</span></span>
3. <span data-ttu-id="4101c-110">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4101c-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4101c-111">单击“行”。</span><span class="sxs-lookup"><span data-stu-id="4101c-111">Click Lines.</span></span>
5. <span data-ttu-id="4101c-112">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="4101c-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="4101c-113">在“帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="4101c-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="4101c-114">在“信用”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="4101c-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="4101c-115">输入远期支票中注明的金额。</span><span class="sxs-lookup"><span data-stu-id="4101c-115">Enter the amount specified in the postdated cheque.</span></span>  
8. <span data-ttu-id="4101c-116">单击“付款”选项卡。</span><span class="sxs-lookup"><span data-stu-id="4101c-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="4101c-117">在“付款方式”字段中，输入值。</span><span class="sxs-lookup"><span data-stu-id="4101c-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="4101c-118">选择远期支票的付款方式</span><span class="sxs-lookup"><span data-stu-id="4101c-118">Select the method of payment for the postdated cheque</span></span>  
10. <span data-ttu-id="4101c-119">单击“远期支票”选项卡。</span><span class="sxs-lookup"><span data-stu-id="4101c-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="4101c-120">在“到期日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="4101c-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="4101c-121">输入远期支票到期付款的日期。</span><span class="sxs-lookup"><span data-stu-id="4101c-121">Enter the date when the postdated cheque is due for payment.</span></span>  
12. <span data-ttu-id="4101c-122">在“开证银行分行”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4101c-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="4101c-123">输入远期支票的银行详情。</span><span class="sxs-lookup"><span data-stu-id="4101c-123">Enter the bank details of the postdated cheque.</span></span>  
13. <span data-ttu-id="4101c-124">在“支票号码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4101c-124">In the cheque number field, type a value.</span></span>
14. <span data-ttu-id="4101c-125">在“开证银行名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="4101c-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="4101c-126">输入远期支票的银行详情。</span><span class="sxs-lookup"><span data-stu-id="4101c-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="4101c-127">单击“过帐”。</span><span class="sxs-lookup"><span data-stu-id="4101c-127">Click Post.</span></span>
16. <span data-ttu-id="4101c-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4101c-128">Close the page.</span></span>

