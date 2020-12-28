---
title: 重新分类租赁负债的短期部分
description: 本主题说明如何创建月度日记帐条目以将部分租赁负债重新分类为短期租赁。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440947"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="35f05-103">重新分类租赁负债的短期部分</span><span class="sxs-lookup"><span data-stu-id="35f05-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35f05-104">本主题说明如何创建月度日记帐条目以将部分租赁负债重新分类为短期租赁。</span><span class="sxs-lookup"><span data-stu-id="35f05-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="35f05-105">当在批处理过程中选择的计划是 **短期租赁负债重新分类** 时，将创建日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="35f05-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="35f05-106">该条目用于在当月的最后一天过帐租赁负债的当前部分。</span><span class="sxs-lookup"><span data-stu-id="35f05-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="35f05-107">同时，从下个月的第一天开始过帐冲销条目。</span><span class="sxs-lookup"><span data-stu-id="35f05-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="35f05-108">负债摊销计划中将显示租赁负债的短期部分。</span><span class="sxs-lookup"><span data-stu-id="35f05-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="35f05-109">过帐日记帐条目过帐后，**已创建的负债重分类日记帐** 列变为可用，并且也在计划中填写了日记帐 ID。</span><span class="sxs-lookup"><span data-stu-id="35f05-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="35f05-110">要创建并过帐短期负债重新分类日记帐条目，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="35f05-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="35f05-111">转到 **资产租赁 \> 定期 \> 批量日记帐创建**。</span><span class="sxs-lookup"><span data-stu-id="35f05-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="35f05-112">在 **批量日记帐创建** 对话框的 **选择计划** 字段中，选择 **短期租赁负债重新分类**。</span><span class="sxs-lookup"><span data-stu-id="35f05-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="35f05-113">在 **租赁组** 字段中，选择租赁组。</span><span class="sxs-lookup"><span data-stu-id="35f05-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="35f05-114">或者，在 **帐簿** 字段中，选择帐簿 ID。</span><span class="sxs-lookup"><span data-stu-id="35f05-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="35f05-115">打开 **过帐** 参数。</span><span class="sxs-lookup"><span data-stu-id="35f05-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="35f05-116">或者，如果应创建但不过帐条目，请关闭此参数。</span><span class="sxs-lookup"><span data-stu-id="35f05-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="35f05-117">打开 **过帐前预览** 参数以在条目过帐之前进行查看。</span><span class="sxs-lookup"><span data-stu-id="35f05-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="35f05-118">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="35f05-118">Select **OK**.</span></span>
