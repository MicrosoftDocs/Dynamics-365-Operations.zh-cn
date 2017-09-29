--- 
title: "创建应计方案"
description: "此任务指南介绍创建应计架构的步骤。"
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 324be23a1e26de0d05c7cf6a61567f7260d0c390
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="60da0-103">创建应计方案</span><span class="sxs-lookup"><span data-stu-id="60da0-103">Create accrual schemes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60da0-104">此任务指南介绍创建应计架构的步骤。</span><span class="sxs-lookup"><span data-stu-id="60da0-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="60da0-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="60da0-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="60da0-106">转到“总帐”>“日记帐设置”>“应计架构”。</span><span class="sxs-lookup"><span data-stu-id="60da0-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="60da0-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="60da0-107">Click New.</span></span>
3. <span data-ttu-id="60da0-108">在“应计标识”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="60da0-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="60da0-109">在“应计架构的描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="60da0-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="60da0-110">在“借方”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="60da0-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="60da0-111">定义的主科目将替换日记帐凭证行的借方主科目，并且还用于根据分类帐的应计交易冲销延期交易。</span><span class="sxs-lookup"><span data-stu-id="60da0-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="60da0-112">在“贷方”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="60da0-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="60da0-113">定义的主科目将替换日记帐凭证行的贷方主科目，并且还用于根据分类帐的应计交易冲销延期交易。</span><span class="sxs-lookup"><span data-stu-id="60da0-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="60da0-114">在“凭证”字段中，选择您想要在过帐交易记录时确定的凭证。</span><span class="sxs-lookup"><span data-stu-id="60da0-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="60da0-115">在“描述”字段中，输入一个值来描述要过帐的交易记录。</span><span class="sxs-lookup"><span data-stu-id="60da0-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="60da0-116">在“期间频率”字段中，选择交易记录的产生频率。</span><span class="sxs-lookup"><span data-stu-id="60da0-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="60da0-117">在“发生次数(按期间)”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="60da0-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="60da0-118">在“过帐交易记录”字段中，选择交易记录过帐的时间，如每月。</span><span class="sxs-lookup"><span data-stu-id="60da0-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


