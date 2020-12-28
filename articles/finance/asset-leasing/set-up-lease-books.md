---
title: 设置租赁帐簿
description: 本主题描述了租赁帐簿中维护的信息。 租赁帐簿中包含确定租赁在系统中的会计方式的会计政策。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440952"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="434e2-104">设置租赁帐簿</span><span class="sxs-lookup"><span data-stu-id="434e2-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="434e2-105">租赁帐簿中包含确定租赁在系统中的会计方式的会计政策。</span><span class="sxs-lookup"><span data-stu-id="434e2-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="434e2-106">除了基于现金的记帐之外，资产租赁还支持以下准则：</span><span class="sxs-lookup"><span data-stu-id="434e2-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="434e2-107">美国通用会计制度 (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="434e2-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="434e2-108">会计准则编纂专题 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="434e2-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="434e2-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="434e2-109">ASC 840</span></span>
- <span data-ttu-id="434e2-110">国际财务报告准则 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="434e2-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="434e2-111">国际会计标准 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="434e2-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="434e2-112">要创建租赁帐簿，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="434e2-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="434e2-113">转到 **资产租赁 \> 设置 \> 租赁帐簿**。</span><span class="sxs-lookup"><span data-stu-id="434e2-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="434e2-114">选择 **新建** 添加帐簿。</span><span class="sxs-lookup"><span data-stu-id="434e2-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="434e2-115">设置以下字段。</span><span class="sxs-lookup"><span data-stu-id="434e2-115">Set the following fields.</span></span>

    | <span data-ttu-id="434e2-116">姓名</span><span class="sxs-lookup"><span data-stu-id="434e2-116">Name</span></span>                                     | <span data-ttu-id="434e2-117">说明</span><span class="sxs-lookup"><span data-stu-id="434e2-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="434e2-118">过帐层</span><span class="sxs-lookup"><span data-stu-id="434e2-118">Posting layer</span></span>                            | <span data-ttu-id="434e2-119">选择要使用的过帐层。</span><span class="sxs-lookup"><span data-stu-id="434e2-119">Select the posting layer to use.</span></span> <span data-ttu-id="434e2-120">为租赁附加的每本帐簿都是为特定过帐层设置的。</span><span class="sxs-lookup"><span data-stu-id="434e2-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="434e2-121">每个过帐层都有不同的过帐目的。</span><span class="sxs-lookup"><span data-stu-id="434e2-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="434e2-122">租赁类型</span><span class="sxs-lookup"><span data-stu-id="434e2-122">Lease type</span></span>                               | <span data-ttu-id="434e2-123">选择是自动将租赁分类，还是应将其预定义为金融租赁或经营性租赁。</span><span class="sxs-lookup"><span data-stu-id="434e2-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="434e2-124">会计框架</span><span class="sxs-lookup"><span data-stu-id="434e2-124">Accounting framework</span></span>                     | <span data-ttu-id="434e2-125">选择与帐簿关联的框架。</span><span class="sxs-lookup"><span data-stu-id="434e2-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="434e2-126">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="434e2-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="434e2-127">如果将租赁类型设置为 **自动**，并且资产使用年限中的租赁期大于或等于此字段中输入的百分比，则系统将租赁分类为金融租赁。</span><span class="sxs-lookup"><span data-stu-id="434e2-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="434e2-128">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="434e2-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="434e2-129">输入一个整数以定义将确定租赁类型的阈值。</span><span class="sxs-lookup"><span data-stu-id="434e2-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="434e2-130">如果将来的最低租赁付款额的现值大于帐簿设置中用户定义的值，并且如果帐簿的租赁分类设置为自动，则系统会将租赁分类为金融租赁。</span><span class="sxs-lookup"><span data-stu-id="434e2-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="434e2-131">短期阈值</span><span class="sxs-lookup"><span data-stu-id="434e2-131">Short-term threshold</span></span>                     | <span data-ttu-id="434e2-132">输入用作短期租赁阈值的月数。</span><span class="sxs-lookup"><span data-stu-id="434e2-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="434e2-133">如果租赁期小于或等于您在此处输入的月数，则系统会将租赁归类为短期租赁，并采用延期租金处理。</span><span class="sxs-lookup"><span data-stu-id="434e2-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="434e2-134">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="434e2-134">Low value threshold</span></span>                      | <span data-ttu-id="434e2-135">输入用作低价值租赁的阈值的金额。</span><span class="sxs-lookup"><span data-stu-id="434e2-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="434e2-136">如果资产的公平价值小于或等于您在此处输入的值，则系统会将租赁归类为低价值租赁，并采用延期租金处理。</span><span class="sxs-lookup"><span data-stu-id="434e2-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="434e2-137">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="434e2-137">Pay to vendor</span></span>                            | <span data-ttu-id="434e2-138">将此选项设置为 **是**，以便允许将租赁付款作为发票过帐到每个租赁中指定的供应商科目。</span><span class="sxs-lookup"><span data-stu-id="434e2-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="434e2-139">过帐租赁付款后，将贷记供应商科目。</span><span class="sxs-lookup"><span data-stu-id="434e2-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="434e2-140">如果此选项设置为 **否**，将改为贷记 **租赁过帐参数** 页上的 **租赁付款** 过帐类型指定的科目。</span><span class="sxs-lookup"><span data-stu-id="434e2-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
