---
title: 结算会计科目之间的交易记录
description: 该过程显示如何结算会计科目间的交易和取消分类帐结算。
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144666"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="e85db-103">结算会计科目之间的交易记录</span><span class="sxs-lookup"><span data-stu-id="e85db-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e85db-104">该过程显示如何结算会计科目间的交易和取消分类帐结算。</span><span class="sxs-lookup"><span data-stu-id="e85db-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="e85db-105">此过程使用演示数据公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="e85db-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="e85db-106">结算会计科目之间的交易记录</span><span class="sxs-lookup"><span data-stu-id="e85db-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="e85db-107">转到“总帐”>“定期任务”>“分类帐结算”。</span><span class="sxs-lookup"><span data-stu-id="e85db-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="e85db-108">在列表中，找到您要结算的交易记录。</span><span class="sxs-lookup"><span data-stu-id="e85db-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="e85db-109">余额必须为零。</span><span class="sxs-lookup"><span data-stu-id="e85db-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="e85db-110">单击“包括”。</span><span class="sxs-lookup"><span data-stu-id="e85db-110">Click Include.</span></span>
4. <span data-ttu-id="e85db-111">单击“接受”。</span><span class="sxs-lookup"><span data-stu-id="e85db-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="e85db-112">取消分类帐结算</span><span class="sxs-lookup"><span data-stu-id="e85db-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="e85db-113">转到“总帐”>“查询和报表”>“试算平衡表”。</span><span class="sxs-lookup"><span data-stu-id="e85db-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="e85db-114">单击“参数”以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="e85db-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="e85db-115">单击“更新”。</span><span class="sxs-lookup"><span data-stu-id="e85db-115">Click Update.</span></span>
4. <span data-ttu-id="e85db-116">在列表中，找到您已结算交易记录的科目。</span><span class="sxs-lookup"><span data-stu-id="e85db-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="e85db-117">单击“所有交易记录”。</span><span class="sxs-lookup"><span data-stu-id="e85db-117">Click All transactions.</span></span>
6. <span data-ttu-id="e85db-118">使用筛选器轻松查找列表中的交易记录。</span><span class="sxs-lookup"><span data-stu-id="e85db-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="e85db-119">单击“分类帐结算”。</span><span class="sxs-lookup"><span data-stu-id="e85db-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="e85db-120">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="e85db-120">In the list, mark the selected row.</span></span>

