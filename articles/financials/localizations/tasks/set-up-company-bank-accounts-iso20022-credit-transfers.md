--- 
title: "设置 ISO20022 贷方转帐的公司银行帐户"
description: "此过程显示如何设置生成付款文件所需的，公司具体的银行帐户信息。"
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="80518-103">设置 ISO20022 贷方转帐的公司银行帐户</span><span class="sxs-lookup"><span data-stu-id="80518-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="80518-104">此过程显示如何设置生成付款文件所需的，公司具体的银行帐户信息。</span><span class="sxs-lookup"><span data-stu-id="80518-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="80518-105">您设置生成 ISO 20022 贷方转帐格式所需的信息，但是根据格式可能需要其他信息，如德国 ID 或分类代码。</span><span class="sxs-lookup"><span data-stu-id="80518-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="80518-106">用于创建此过程的演示数据公司是 DEMF。</span><span class="sxs-lookup"><span data-stu-id="80518-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="80518-107">这是五个用于演示使用电子申报配置的供应商付款流程的流程中的第二个。</span><span class="sxs-lookup"><span data-stu-id="80518-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="80518-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="80518-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="80518-109">设置 BAN 和 SWIFT 代码</span><span class="sxs-lookup"><span data-stu-id="80518-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="80518-110">转到现金和银行管理>银行账号。</span><span class="sxs-lookup"><span data-stu-id="80518-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="80518-111">使用“快速筛选器”以筛选含有 'DEMF OPER' 值的“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="80518-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="80518-112">单击“DEMF OPER”以打开银行帐户详细信息。</span><span class="sxs-lookup"><span data-stu-id="80518-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="80518-113">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="80518-113">Click Edit.</span></span>
5. <span data-ttu-id="80518-114">展开”其他识别“部分。</span><span class="sxs-lookup"><span data-stu-id="80518-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="80518-115">在“IBAN”字段中，键入“DE89370400440532013000”。</span><span class="sxs-lookup"><span data-stu-id="80518-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="80518-116">在“SWIFT 代码”字段中，键入“DEUTDEFF”。</span><span class="sxs-lookup"><span data-stu-id="80518-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="80518-117">请注意，许多付款格式不需要 SWIFT\BIC，但是建议还是为银行帐户登记。</span><span class="sxs-lookup"><span data-stu-id="80518-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="80518-118">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="80518-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="80518-119">为法人实体设置银行帐户</span><span class="sxs-lookup"><span data-stu-id="80518-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="80518-120">转至“组织管理”>“组织”>“法人”。</span><span class="sxs-lookup"><span data-stu-id="80518-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="80518-121">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="80518-121">Click Edit.</span></span>
3. <span data-ttu-id="80518-122">展开“银行帐户信息”部分。</span><span class="sxs-lookup"><span data-stu-id="80518-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="80518-123">在“银行帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="80518-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="80518-124">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="80518-124">Click Save.</span></span>

