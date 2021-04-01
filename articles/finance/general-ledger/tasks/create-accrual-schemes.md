---
title: 创建应计方案
description: 本主题说明如何创建应计方案。
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c021f71735e63c270e8f1998d77d4e4abcc5506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236689"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="9ed50-103">创建应计方案</span><span class="sxs-lookup"><span data-stu-id="9ed50-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ed50-104">本主题说明如何创建应计方案。</span><span class="sxs-lookup"><span data-stu-id="9ed50-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="9ed50-105">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="9ed50-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9ed50-106">转到 **导航窗格 > 模块 > 总帐 > 日记帐设置 > 应计方案**。</span><span class="sxs-lookup"><span data-stu-id="9ed50-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="9ed50-107">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9ed50-107">Select **New**.</span></span>
3. <span data-ttu-id="9ed50-108">在 **应计标识** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ed50-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="9ed50-109">在 **应计方案的描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9ed50-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="9ed50-110">在 **借方** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="9ed50-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="9ed50-111">定义的主科目将替换日记帐凭证行的借方主科目，并且还用于根据分类帐的应计交易冲销延期交易。</span><span class="sxs-lookup"><span data-stu-id="9ed50-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="9ed50-112">在 **贷方** 字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="9ed50-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="9ed50-113">定义的主科目将替换日记帐凭证行的贷方主科目，并且还用于根据分类帐的应计交易冲销延期交易。</span><span class="sxs-lookup"><span data-stu-id="9ed50-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="9ed50-114">在 **凭证** 字段中，选择您想要在过帐交易记录时确定的凭证。</span><span class="sxs-lookup"><span data-stu-id="9ed50-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="9ed50-115">在 **描述** 字段中，输入一个值来描述要过帐的交易记录。</span><span class="sxs-lookup"><span data-stu-id="9ed50-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="9ed50-116">在 **期间频率** 字段中，选择交易记录的产生频率。</span><span class="sxs-lookup"><span data-stu-id="9ed50-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="9ed50-117">在 **发生次数(按期间)** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="9ed50-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="9ed50-118">在 **过帐交易记录** 字段中，选择交易记录过帐的时间，如 **每月**。</span><span class="sxs-lookup"><span data-stu-id="9ed50-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]