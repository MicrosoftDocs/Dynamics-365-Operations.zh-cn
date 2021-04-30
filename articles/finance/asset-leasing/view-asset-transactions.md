---
title: 查看负债、资产和费用交易
description: 本主题说明如何查看租赁资产的交易。 这些交易包括已过帐的租赁负债交易和执行费用交易。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 55b8019db6abdb3bd5ecdb6eadc4f7443f2bf071
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881630"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="9d24e-104">查看负债、资产和费用交易</span><span class="sxs-lookup"><span data-stu-id="9d24e-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d24e-105">本主题说明如何查看租赁资产的交易。</span><span class="sxs-lookup"><span data-stu-id="9d24e-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="9d24e-106">这些交易包括已过帐的租赁负债交易和执行费用交易。</span><span class="sxs-lookup"><span data-stu-id="9d24e-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="9d24e-107">多种报表中都使用负债和使用权 (ROU) 资产的帐面价值。</span><span class="sxs-lookup"><span data-stu-id="9d24e-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="9d24e-108">还用于计算调整值。</span><span class="sxs-lookup"><span data-stu-id="9d24e-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="9d24e-109">负债交易记录</span><span class="sxs-lookup"><span data-stu-id="9d24e-109">Liability transactions</span></span>

<span data-ttu-id="9d24e-110">要查看租赁负债交易，请在 **租赁摘要** 页上选择一个租赁，然后选择 **帐簿** 打开租赁记录的附加帐簿。</span><span class="sxs-lookup"><span data-stu-id="9d24e-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="9d24e-111">过帐初始确认、发票或利息日记帐之后，选择 **负债交易**。</span><span class="sxs-lookup"><span data-stu-id="9d24e-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="9d24e-112">**负债交易** 页显示增加或减少租赁负债的交易。</span><span class="sxs-lookup"><span data-stu-id="9d24e-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="9d24e-113">此页面上的负数表示标准应用程序中的信用证交易。</span><span class="sxs-lookup"><span data-stu-id="9d24e-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="9d24e-114">任何应计利息均显示为负值，并增加总租赁负债。</span><span class="sxs-lookup"><span data-stu-id="9d24e-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="9d24e-115">任何租赁调整均显示为正值或负值，具体取决于租赁帐簿的性质和影响。</span><span class="sxs-lookup"><span data-stu-id="9d24e-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="9d24e-116">所选租赁的租赁负债的当前总净额显示在页面的左下方。</span><span class="sxs-lookup"><span data-stu-id="9d24e-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="9d24e-117">资产交易记录</span><span class="sxs-lookup"><span data-stu-id="9d24e-117">Asset transactions</span></span>

<span data-ttu-id="9d24e-118">要查看租赁资产交易，请在 **租赁摘要** 页上选择一个租赁，然后选择 **帐簿** 打开租赁记录的附加租赁帐簿。</span><span class="sxs-lookup"><span data-stu-id="9d24e-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="9d24e-119">然后选择 **租赁交易**。</span><span class="sxs-lookup"><span data-stu-id="9d24e-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="9d24e-120">**资产交易** 页面显示增加或减少租赁资产和累计折旧科目的交易。</span><span class="sxs-lookup"><span data-stu-id="9d24e-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="9d24e-121">借项显示为正数，贷项显示为负数，正如 **负债交易** 页上。</span><span class="sxs-lookup"><span data-stu-id="9d24e-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="9d24e-122">过帐的初始确认和下一个累计折旧在页面的左下方显示为资产余额。</span><span class="sxs-lookup"><span data-stu-id="9d24e-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="9d24e-123">费用交易</span><span class="sxs-lookup"><span data-stu-id="9d24e-123">Expenses transactions</span></span>

<span data-ttu-id="9d24e-124">要查看租赁费用交易，请在 **租赁摘要** 页上选择一个租赁，然后选择 **帐簿** 打开租赁记录的附加租赁帐簿。</span><span class="sxs-lookup"><span data-stu-id="9d24e-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="9d24e-125">然后选择 **费用交易**。</span><span class="sxs-lookup"><span data-stu-id="9d24e-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="9d24e-126">**费用交易** 页显示已针对租赁过帐的所有费用，例如利息费用、折旧费用和任何执行成本。</span><span class="sxs-lookup"><span data-stu-id="9d24e-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
