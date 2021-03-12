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
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f189d1ed5b0917c9975587accc2275556ceb8143
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968746"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="a0e91-103">平衡单位间核算的日记帐</span><span class="sxs-lookup"><span data-stu-id="a0e91-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0e91-104">本文显示当在分类帐页中选择平衡财务维度时日记帐如何自动平衡。</span><span class="sxs-lookup"><span data-stu-id="a0e91-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="a0e91-105">如果在财务维度值的级别处的科目分录不平衡，则附加的科目分录将自动创建以平衡日记帐。</span><span class="sxs-lookup"><span data-stu-id="a0e91-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="a0e91-106">这些科目分录使用 **自动交易记录帐户** 页上的 **单位间 - 借方** 和 **单位间 - 贷方** 过帐类型来确定主科目。</span><span class="sxs-lookup"><span data-stu-id="a0e91-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="a0e91-107">例如，业务单位，是会计科目的二级细分，被选择作为平衡财务维度，以下会计分录即将创建。</span><span class="sxs-lookup"><span data-stu-id="a0e91-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="a0e91-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="a0e91-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="a0e91-109">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="a0e91-109">100.00 DR</span></span> |
| <span data-ttu-id="a0e91-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="a0e91-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="a0e91-111">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="a0e91-111">100.00 DR</span></span> |
| <span data-ttu-id="a0e91-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="a0e91-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="a0e91-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="a0e91-113">200.00 CR</span></span> |

<span data-ttu-id="a0e91-114">在这种情况下，以下余额确定：</span><span class="sxs-lookup"><span data-stu-id="a0e91-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="a0e91-115">对于业务单位 MSP = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="a0e91-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="a0e91-116">对于业务单位 NY = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="a0e91-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="a0e91-117">因此，以下会计分录将自动创建，以在财务维度值级别平衡日记帐。</span><span class="sxs-lookup"><span data-stu-id="a0e91-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="a0e91-118">（单位间借方）– MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="a0e91-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="a0e91-119">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="a0e91-119">100.00 DR</span></span> |
| <span data-ttu-id="a0e91-120">（单位间贷方）– NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="a0e91-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="a0e91-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="a0e91-121">100.00 CR</span></span> |





