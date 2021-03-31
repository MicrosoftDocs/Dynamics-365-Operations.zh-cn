---
title: 设置 ISO20022 直接借记的客户及客户银行帐户
description: 此任务通过设置所需的客户银行帐户和客户直接借记授权以生成客户付款文件（如 ISO20022 直接借记）。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d097caf3ad097e3107708c426ef668c70298c4f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209843"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="fb430-103">设置 ISO20022 直接借记的客户及客户银行帐户</span><span class="sxs-lookup"><span data-stu-id="fb430-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb430-104">此任务通过设置所需的客户银行帐户和客户直接借记授权以生成客户付款文件（如 ISO20022 直接借记）。</span><span class="sxs-lookup"><span data-stu-id="fb430-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="fb430-105">客户或客户银行帐户可能需要此过程中未介绍的更多信息，具体取决于设置的客户付款格式。</span><span class="sxs-lookup"><span data-stu-id="fb430-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="fb430-106">本任务所用的演示数据公司为“DEMF“， 其法定注册国家/地区主地址为”德国“。</span><span class="sxs-lookup"><span data-stu-id="fb430-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="fb430-107">这是五个用于演示使用电子申报配置的客户付款流程的过程中的第四个。</span><span class="sxs-lookup"><span data-stu-id="fb430-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="fb430-108">设置客户银行帐户</span><span class="sxs-lookup"><span data-stu-id="fb430-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="fb430-109">转到“应付帐款”>“客户”>“所有客户”。</span><span class="sxs-lookup"><span data-stu-id="fb430-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="fb430-110">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="fb430-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="fb430-111">例如，在含有“DE-010”值的“帐户”字段中筛选。</span><span class="sxs-lookup"><span data-stu-id="fb430-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="fb430-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="fb430-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fb430-113">在“操作窗格”上，单击“客户”。</span><span class="sxs-lookup"><span data-stu-id="fb430-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="fb430-114">单击“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="fb430-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="fb430-115">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="fb430-115">Click New.</span></span>
7. <span data-ttu-id="fb430-116">在“银行帐户”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fb430-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="fb430-117">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fb430-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="fb430-118">例如，输入“EUR 银行”。</span><span class="sxs-lookup"><span data-stu-id="fb430-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="fb430-119">在“银行组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fb430-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="fb430-120">在“IBAN”字段，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fb430-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="fb430-121">例如，输入“DE36200400000628808808”。</span><span class="sxs-lookup"><span data-stu-id="fb430-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="fb430-122">在“SWIFT 代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="fb430-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="fb430-123">例如，输入 'COBADEFFXXX'。</span><span class="sxs-lookup"><span data-stu-id="fb430-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="fb430-124">请注意，许多付款格式不需要 SWIFT\BIC，但是建议还是为银行帐户登记。</span><span class="sxs-lookup"><span data-stu-id="fb430-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="fb430-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="fb430-125">Click Save.</span></span>
13. <span data-ttu-id="fb430-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="fb430-126">Close the page.</span></span>
14. <span data-ttu-id="fb430-127">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="fb430-127">Click Edit.</span></span>
15. <span data-ttu-id="fb430-128">展开“默认付款”部分。</span><span class="sxs-lookup"><span data-stu-id="fb430-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="fb430-129">在“银行帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fb430-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="fb430-130">添加直接借记授权单</span><span class="sxs-lookup"><span data-stu-id="fb430-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="fb430-131">展开“直接借记授权”部分。</span><span class="sxs-lookup"><span data-stu-id="fb430-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="fb430-132">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="fb430-132">Click Add.</span></span>
3. <span data-ttu-id="fb430-133">在“贷方银行帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fb430-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="fb430-134">例如，选择“DEMF OPER”。</span><span class="sxs-lookup"><span data-stu-id="fb430-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="fb430-135">在“签署日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="fb430-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="fb430-136">单击“是”以确认日期的更新。</span><span class="sxs-lookup"><span data-stu-id="fb430-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="fb430-137">在“输入位置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="fb430-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="fb430-138">在“付款期望值”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="fb430-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="fb430-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="fb430-139">Click OK.</span></span>
9. <span data-ttu-id="fb430-140">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="fb430-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]