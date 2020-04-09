---
title: 设置 ISO20022 直接借记的公司银行帐户
description: 此任务通过设置所需的特定于公司的银行帐户信息以生成客户付款文件。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 652d8aa8f78d9a12ee390d23904f2c94d9bcf684
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144851"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="a842e-103">设置 ISO20022 直接借记的公司银行帐户</span><span class="sxs-lookup"><span data-stu-id="a842e-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a842e-104">此任务通过设置所需的特定于公司的银行帐户信息以生成客户付款文件。</span><span class="sxs-lookup"><span data-stu-id="a842e-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="a842e-105">此过程以 ISO 20022 直接借记格式为例。</span><span class="sxs-lookup"><span data-stu-id="a842e-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="a842e-106">其他格式可能需要更多设置信息，如公司 ID 或分类代码。</span><span class="sxs-lookup"><span data-stu-id="a842e-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="a842e-107">用于创建此任务的演示数据公司是 DEMF。</span><span class="sxs-lookup"><span data-stu-id="a842e-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="a842e-108">这是五个用于演示使用电子申报配置的客户付款流程的过程中的第二个。</span><span class="sxs-lookup"><span data-stu-id="a842e-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="a842e-109">设置 IBAN 和 SWIFT 代码</span><span class="sxs-lookup"><span data-stu-id="a842e-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="a842e-110">转到现金和银行管理>银行账号。</span><span class="sxs-lookup"><span data-stu-id="a842e-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="a842e-111">使用“快速筛选器”以筛选含有 'DEMF OPER' 值的“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="a842e-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="a842e-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a842e-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a842e-113">例如：单击“DEMF OPER”以打开银行帐户详细信息。</span><span class="sxs-lookup"><span data-stu-id="a842e-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="a842e-114">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="a842e-114">Click Edit.</span></span>
5. <span data-ttu-id="a842e-115">展开或折叠”其他识别“部分。</span><span class="sxs-lookup"><span data-stu-id="a842e-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="a842e-116">在“IBAN”字段，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a842e-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="a842e-117">例如，输入“DE89370400440532013000”。</span><span class="sxs-lookup"><span data-stu-id="a842e-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="a842e-118">在“SWIFT 代码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a842e-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="a842e-119">例如，输入“DEUTDEFF”。</span><span class="sxs-lookup"><span data-stu-id="a842e-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="a842e-120">请注意，许多付款格式不需要 SWIFT\BIC，但是建议还是为银行帐户登记。</span><span class="sxs-lookup"><span data-stu-id="a842e-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="a842e-121">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a842e-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="a842e-122">为法人实体设置银行帐户</span><span class="sxs-lookup"><span data-stu-id="a842e-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="a842e-123">转至“组织管理”>“组织”>“法人”。</span><span class="sxs-lookup"><span data-stu-id="a842e-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="a842e-124">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="a842e-124">Click Edit.</span></span>
3. <span data-ttu-id="a842e-125">展开或折叠“银行帐户信息”部分。</span><span class="sxs-lookup"><span data-stu-id="a842e-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="a842e-126">在“银行帐户”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a842e-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a842e-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a842e-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a842e-128">例如：选择“DEMF OPER”银行帐户。</span><span class="sxs-lookup"><span data-stu-id="a842e-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="a842e-129">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a842e-129">Click Save.</span></span>

