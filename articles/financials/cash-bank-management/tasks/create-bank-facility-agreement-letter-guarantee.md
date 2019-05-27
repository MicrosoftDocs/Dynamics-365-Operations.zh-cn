---
title: 创建保函的银行信贷协议
description: 此任务可以创建一个银行融资协议，以便处理保函。
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04ee7b1483f3b8a7cda7fce5439586f0a2979e51
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566171"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="d2df3-103">创建保函的银行信贷协议</span><span class="sxs-lookup"><span data-stu-id="d2df3-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2df3-104">此任务可以创建一个银行融资协议，以便处理保函。</span><span class="sxs-lookup"><span data-stu-id="d2df3-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="d2df3-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="d2df3-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="d2df3-106">创建银行信贷协议</span><span class="sxs-lookup"><span data-stu-id="d2df3-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="d2df3-107">转到“现金和银行管理”>“保函”>“银行融资协议”。</span><span class="sxs-lookup"><span data-stu-id="d2df3-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="d2df3-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d2df3-108">Click New.</span></span>
3. <span data-ttu-id="d2df3-109">在“协议编号”字段中，输入交易的银行协议编号。</span><span class="sxs-lookup"><span data-stu-id="d2df3-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="d2df3-110">在“银行帐户”字段中，选择开放保函适用的银行帐号。</span><span class="sxs-lookup"><span data-stu-id="d2df3-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="d2df3-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d2df3-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d2df3-112">在“开始日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="d2df3-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="d2df3-113">在“结束日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="d2df3-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="d2df3-114">切换“概况”部分的扩展。</span><span class="sxs-lookup"><span data-stu-id="d2df3-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="d2df3-115">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="d2df3-115">Click Add line.</span></span>
10. <span data-ttu-id="d2df3-116">在“融资类型”字段中，单击下拉键打开查询。</span><span class="sxs-lookup"><span data-stu-id="d2df3-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d2df3-117">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="d2df3-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="d2df3-118">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="d2df3-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="d2df3-119">在“限值”字段中，输入与银行协商的金额。</span><span class="sxs-lookup"><span data-stu-id="d2df3-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="d2df3-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d2df3-120">Click Save.</span></span>
15. <span data-ttu-id="d2df3-121">切换“保函”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="d2df3-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="d2df3-122">在“计算方法”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="d2df3-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="d2df3-123">根据需要输入“现金保证金”、“发货佣金”、“展开佣金”、“增值佣金”或“降值佣金”的计算方法和百分比详情。</span><span class="sxs-lookup"><span data-stu-id="d2df3-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="d2df3-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d2df3-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="d2df3-125">展开银行融资协议</span><span class="sxs-lookup"><span data-stu-id="d2df3-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="d2df3-126">单击“扩展”打开垂直对话框。</span><span class="sxs-lookup"><span data-stu-id="d2df3-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="d2df3-127">在“新协议数目”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d2df3-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="d2df3-128">在“结束日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="d2df3-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="d2df3-129">单击“扩展”。</span><span class="sxs-lookup"><span data-stu-id="d2df3-129">Click Extend.</span></span>
5. <span data-ttu-id="d2df3-130">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d2df3-130">Click Save.</span></span>
6. <span data-ttu-id="d2df3-131">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d2df3-131">Close the page.</span></span>

