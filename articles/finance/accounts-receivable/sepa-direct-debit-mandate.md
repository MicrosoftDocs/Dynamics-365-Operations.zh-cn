---
title: 设置 SEPA 直接借记授权单
description: 在客户将已经签署的授权授予债权人的情况下，单一欧元支付区 (SEPA) 直接借记允许债权人从客户的银行帐户中筹集资金。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6ee3861e967246e79b072aaa69f2be02db9231b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995485"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="30462-103">设置 SEPA 直接借记授权单</span><span class="sxs-lookup"><span data-stu-id="30462-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30462-104">在客户将已经签署的授权授予债权人的情况下，单一欧元支付区 (SEPA) 直接借记允许债权人从客户的银行帐户中筹集资金。</span><span class="sxs-lookup"><span data-stu-id="30462-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="30462-105">客户签署的授权允许债权人收取付款，并指示客户方银行支付该收款。</span><span class="sxs-lookup"><span data-stu-id="30462-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="30462-106">此主题的组织是为了显示 SEPA 直接借记授权单的设置流程。</span><span class="sxs-lookup"><span data-stu-id="30462-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="30462-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="30462-107">Prerequisites</span></span>
<span data-ttu-id="30462-108">下表显示必须先就绪然后才能开始的先决条件。</span><span class="sxs-lookup"><span data-stu-id="30462-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="30462-109">类别</span><span class="sxs-lookup"><span data-stu-id="30462-109">Category</span></span>       | <span data-ttu-id="30462-110">先决条件</span><span class="sxs-lookup"><span data-stu-id="30462-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30462-111">国家/地区</span><span class="sxs-lookup"><span data-stu-id="30462-111">Country/region</span></span> | <span data-ttu-id="30462-112">法人的主要地址必须在以下国家/地区：奥地利、比利时、德国、西班牙、法国、意大利或荷兰。</span><span class="sxs-lookup"><span data-stu-id="30462-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="30462-113">为直接借记授权设置编号规则。每个直接借记授权必须具有一个独有的编号。</span><span class="sxs-lookup"><span data-stu-id="30462-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="30462-114">使用 **编号规则** 页创建直接借记授权的编号规则。</span><span class="sxs-lookup"><span data-stu-id="30462-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="30462-115">使用该标识符在 **应收帐款参数** 页中将编号规则分配给直接借记授权系统。</span><span class="sxs-lookup"><span data-stu-id="30462-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="30462-116">为直接借记授权设置应收帐款参数。使用 **应收帐款参数** 页可以设置直接借记授权的参数。</span><span class="sxs-lookup"><span data-stu-id="30462-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="30462-117">若要设置参数，请在 **直接借记** 选项卡上，根据需要更改默认参数。</span><span class="sxs-lookup"><span data-stu-id="30462-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="30462-118">然后，在 **编号规则** 选项卡上，用您早先设置的更新编号规则 **直接借记授权单 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="30462-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="30462-119">设置直接借记授权的付款方式。您必须按照付款方式的以下附加步骤进行操作：</span><span class="sxs-lookup"><span data-stu-id="30462-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="30462-120">您将使用此付款方式查询发票以生成直接借记付款。</span><span class="sxs-lookup"><span data-stu-id="30462-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="30462-121">使用 **付款方式** 页可设置付款方式。</span><span class="sxs-lookup"><span data-stu-id="30462-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="30462-122">若要设置直接借记授权的付款方式，您必须按照付款方式的以下附加步骤进行操作：</span><span class="sxs-lookup"><span data-stu-id="30462-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="30462-123">在 **付款类型** 字段中，选择 **电子支付**。</span><span class="sxs-lookup"><span data-stu-id="30462-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="30462-124">选项：如果您希望您的每位客户具有多个授权，请在 **期间** 字段中选择 **发票**。</span><span class="sxs-lookup"><span data-stu-id="30462-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="30462-125">将会为每张发票创建单独的付款，而每笔付款使用的都是为发票指定的授权。</span><span class="sxs-lookup"><span data-stu-id="30462-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="30462-126">通过使用直接借记授权单，选择 **需要授权单** 选项创建付款。</span><span class="sxs-lookup"><span data-stu-id="30462-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="30462-127">只有当您在 **付款类型** 字段中选择 **电子支付** 时，**需要授权单** 才可用。</span><span class="sxs-lookup"><span data-stu-id="30462-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="30462-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="30462-128">Additional resources</span></span>

[<span data-ttu-id="30462-129">SEPA 直接借记概览</span><span class="sxs-lookup"><span data-stu-id="30462-129">SEPA direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="30462-130">为客户创建直接借记授权单</span><span class="sxs-lookup"><span data-stu-id="30462-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 

