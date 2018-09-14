--- 
title: "创建供应商银行帐户"
description: "此过程演示如何为供应商创建银行帐户。"
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: deb3587667ac13b95617ec219995bfef931df00c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="cd97c-103">创建供应商银行帐户</span><span class="sxs-lookup"><span data-stu-id="cd97c-103">Create a vendor bank account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd97c-104">此过程演示如何为供应商创建银行帐户。</span><span class="sxs-lookup"><span data-stu-id="cd97c-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="cd97c-105">您可以在演示数据公司 USMF 中使用此过程。</span><span class="sxs-lookup"><span data-stu-id="cd97c-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="cd97c-106">转到“采购”>“供应商”>“所有供应商”。</span><span class="sxs-lookup"><span data-stu-id="cd97c-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="cd97c-107">选择要为其创建银行帐户的供应商，然后单击“供应商帐户 ID”中的链接。</span><span class="sxs-lookup"><span data-stu-id="cd97c-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="cd97c-108">在“操作窗格”上，单击“供应商”。</span><span class="sxs-lookup"><span data-stu-id="cd97c-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="cd97c-109">单击“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="cd97c-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="cd97c-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cd97c-110">Click New.</span></span>
6. <span data-ttu-id="cd97c-111">在“银行帐户”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="cd97c-112">此 ID 将用于识别供应商记录中的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="cd97c-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="cd97c-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="cd97c-114">在“银行组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="cd97c-115">在“银行代号类型”字段中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="cd97c-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="cd97c-116">这是用于国际支付的银行代号的类型。</span><span class="sxs-lookup"><span data-stu-id="cd97c-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="cd97c-117">在“银行帐号”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="cd97c-118">在“SWIFT 代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="cd97c-119">在“IBAN”字段，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="cd97c-120">IBAN 编号的格式必须正确。</span><span class="sxs-lookup"><span data-stu-id="cd97c-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="cd97c-121">例如，您可以使用 DE89370400440532013000。</span><span class="sxs-lookup"><span data-stu-id="cd97c-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="cd97c-122">如果已到达生效日期，但尚未超过到期日期，则银行帐户的状态为“有效”。</span><span class="sxs-lookup"><span data-stu-id="cd97c-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="cd97c-123">如果“生效日期”和“到期日期”字段均为空白，则也是处于“有效”状态。</span><span class="sxs-lookup"><span data-stu-id="cd97c-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="cd97c-124">如果“生效日期”和“到期日期”字段中的日期均为未来日期，则不可使用电子付款。</span><span class="sxs-lookup"><span data-stu-id="cd97c-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="cd97c-125">可使用其他付款类型，且银行帐户有效。</span><span class="sxs-lookup"><span data-stu-id="cd97c-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="cd97c-126">展开“设置”部分。</span><span class="sxs-lookup"><span data-stu-id="cd97c-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="cd97c-127">在“文本代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="cd97c-128">此字段指定接收方的银行对账单上显示的代码。</span><span class="sxs-lookup"><span data-stu-id="cd97c-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="cd97c-129">在“发送给银行的消息”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="cd97c-130">在“汇率参考”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="cd97c-131">这是任何远期汇率或定期汇率的参考编号。</span><span class="sxs-lookup"><span data-stu-id="cd97c-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="cd97c-132">在“货币”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="cd97c-133">当发布预验证时，此部分提供其状态（待定或已审核）的概述。</span><span class="sxs-lookup"><span data-stu-id="cd97c-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="cd97c-134">展开“地址”部分。</span><span class="sxs-lookup"><span data-stu-id="cd97c-134">Expand the Address section.</span></span>
19. <span data-ttu-id="cd97c-135">展开“预验证”部分。</span><span class="sxs-lookup"><span data-stu-id="cd97c-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="cd97c-136">展开“联系信息”部分。</span><span class="sxs-lookup"><span data-stu-id="cd97c-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="cd97c-137">在“电话”字段，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="cd97c-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="cd97c-138">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="cd97c-138">Close the page.</span></span>
23. <span data-ttu-id="cd97c-139">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="cd97c-139">Click Edit.</span></span>
24. <span data-ttu-id="cd97c-140">展开付款窗口。</span><span class="sxs-lookup"><span data-stu-id="cd97c-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="cd97c-141">在“银行帐户”字段中，选择您刚才创建的帐户。</span><span class="sxs-lookup"><span data-stu-id="cd97c-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="cd97c-142">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cd97c-142">Click Save.</span></span>
    * <span data-ttu-id="cd97c-143">地址可以从银行组继承（如果已指定），也可以在此处添加。</span><span class="sxs-lookup"><span data-stu-id="cd97c-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  


