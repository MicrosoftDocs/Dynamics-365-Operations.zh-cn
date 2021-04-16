---
title: 批量创建月日记帐条目
description: 本主题说明如何在记录月租赁费用时批量创建日记帐条目来帮助提高效率。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 664001dd6e9da449dec65750da53d58bd27438b4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816020"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="8657c-103">批量创建月日记帐条目</span><span class="sxs-lookup"><span data-stu-id="8657c-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8657c-104">本主题说明如何在记录月租赁费用时批量创建日记帐条目来帮助提高效率。</span><span class="sxs-lookup"><span data-stu-id="8657c-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="8657c-105">批处理可用于从多个计划创建日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8657c-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="8657c-106">这些日记帐条目可以包括租赁付款、负债摊销、使用权 (ROU) 资产摊销以及执行成本费用。</span><span class="sxs-lookup"><span data-stu-id="8657c-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="8657c-107">您还可以使用批处理来同时对多个租赁进行初始识别，或者同时为多个租赁创建转换调整。</span><span class="sxs-lookup"><span data-stu-id="8657c-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="8657c-108">要设置批处理作业，或处理多个租赁的付款发票、折旧或利息，请转到 **资产租赁 \> 定期 \> 批量创建日记帐**。</span><span class="sxs-lookup"><span data-stu-id="8657c-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="8657c-109">在出现的对话框中，您可以选择用于创建日记帐条目的计划。</span><span class="sxs-lookup"><span data-stu-id="8657c-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="8657c-110">您还可以指定是否应针对特定实体、租赁组或租赁帐簿运行批处理流程。</span><span class="sxs-lookup"><span data-stu-id="8657c-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="8657c-111">后续交易（如负债摊销计划、付款、折旧和费用）将仅在相应租赁的初始确认过帐后才过帐。</span><span class="sxs-lookup"><span data-stu-id="8657c-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="8657c-112">将创建日记帐条目，但是在您选择 **运行** 命令之前，不会过帐这些条目。</span><span class="sxs-lookup"><span data-stu-id="8657c-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]