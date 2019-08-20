---
title: 平衡单位间核算的日记帐
description: 本文显示当在分类帐页中选择平衡财务维度时日记帐如何自动平衡。
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e84d96b5467b38e07a9ed31f142c27b638289284
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839345"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="70907-103">平衡单位间核算的日记帐</span><span class="sxs-lookup"><span data-stu-id="70907-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70907-104">本文显示当在分类帐页中选择平衡财务维度时日记帐如何自动平衡。</span><span class="sxs-lookup"><span data-stu-id="70907-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="70907-105">如果在财务维度值的级别处的科目分录不平衡，则附加的科目分录将自动创建以平衡日记帐。</span><span class="sxs-lookup"><span data-stu-id="70907-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="70907-106">这些科目分录使用**自动交易记录帐户**页上的**单位间 - 借方**和**单位间 - 贷方**过帐类型来确定主科目。</span><span class="sxs-lookup"><span data-stu-id="70907-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="70907-107">例如，业务单位，是会计科目的二级细分，被选择作为平衡财务维度，以下会计分录即将创建。</span><span class="sxs-lookup"><span data-stu-id="70907-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="70907-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="70907-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="70907-109">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="70907-109">100.00 DR</span></span> |
| <span data-ttu-id="70907-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="70907-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="70907-111">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="70907-111">100.00 DR</span></span> |
| <span data-ttu-id="70907-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="70907-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="70907-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="70907-113">200.00 CR</span></span> |

<span data-ttu-id="70907-114">在这种情况下，以下余额确定：</span><span class="sxs-lookup"><span data-stu-id="70907-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="70907-115">对于业务单位 MSP = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="70907-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="70907-116">对于业务单位 NY = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="70907-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="70907-117">因此，以下会计分录将自动创建，以在财务维度值级别平衡日记帐。</span><span class="sxs-lookup"><span data-stu-id="70907-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="70907-118">（单位间借方）– MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="70907-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="70907-119">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="70907-119">100.00 DR</span></span> |
| <span data-ttu-id="70907-120">（单位间贷方）– NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="70907-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="70907-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="70907-121">100.00 CR</span></span> |





