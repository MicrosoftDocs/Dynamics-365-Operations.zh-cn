---
title: 每个日记帐的帐簿数
description: 本主题描述通过批处理作业创建固定资产购置或折旧建议时，日记帐与资产帐簿之间的关系。 您可以定义各项购置和折旧所包括的最大帐簿数。
author: moaamer
ms.date: 11/19/2020
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
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e948b4353d0216f1e09019a98319e343bd535861
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822025"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="5ba61-104">每个日记帐的帐簿数</span><span class="sxs-lookup"><span data-stu-id="5ba61-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ba61-105">本主题描述通过批处理作业创建固定资产购置或折旧建议时，日记帐与资产帐簿之间的关系。</span><span class="sxs-lookup"><span data-stu-id="5ba61-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="5ba61-106">您可以使用 **固定资产参数** 页面（**固定资产 \> 设置 \> 固定资产参数**）中 **常规** 选项卡上的 **每个日记帐的帐簿数** 部分中的字段定义各项购置和折旧要包含的帐簿的数量。</span><span class="sxs-lookup"><span data-stu-id="5ba61-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="5ba61-107">这些字段使您可以分配每本购置日记帐和折旧日记帐的资产帐簿的数量。</span><span class="sxs-lookup"><span data-stu-id="5ba61-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="5ba61-108">对于购置方案，默认值为至少 10,000 本帐簿。</span><span class="sxs-lookup"><span data-stu-id="5ba61-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="5ba61-109">对于折旧方案，默认值为至少 2,000 本帐簿。</span><span class="sxs-lookup"><span data-stu-id="5ba61-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="5ba61-110">例如，如果有 4,000 项固定资产，并且每项资产与两本帐簿关联，则一本帐簿将过帐到当前层，另一本帐簿则过帐到税层。</span><span class="sxs-lookup"><span data-stu-id="5ba61-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="5ba61-111">如果通过批处理购置 4,000 项固定资产，则创建一项固定资产购置日记帐的批处理作业将包含 4,000 个资产帐簿。</span><span class="sxs-lookup"><span data-stu-id="5ba61-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="5ba61-112">将继续使用创建的日记帐，直到完成批处理作业。</span><span class="sxs-lookup"><span data-stu-id="5ba61-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="5ba61-113">每个日记帐的最大帐簿数量中不包含衍生帐簿。</span><span class="sxs-lookup"><span data-stu-id="5ba61-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="5ba61-114">您可以使用批处理对同一组所购置资产运行折旧。</span><span class="sxs-lookup"><span data-stu-id="5ba61-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="5ba61-115">例如，批处理作业创建两个折旧日记帐，每个折旧日记帐由 2,000 本资产帐簿组成。</span><span class="sxs-lookup"><span data-stu-id="5ba61-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="5ba61-116">第一个日记帐将包含与固定资产关联的帐簿，这些帐簿的编号为 1 到 2,000。</span><span class="sxs-lookup"><span data-stu-id="5ba61-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="5ba61-117">然后，第二个日记帐将包含与固定资产关联的帐簿，这些帐簿的编号为 2,001 到 4,000。</span><span class="sxs-lookup"><span data-stu-id="5ba61-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="5ba61-118">批处理作业不包括已结帐簿。</span><span class="sxs-lookup"><span data-stu-id="5ba61-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="5ba61-119">例如，在一个折旧批处理作业中，前 2,000 本帐簿中有 10 本已结。</span><span class="sxs-lookup"><span data-stu-id="5ba61-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="5ba61-120">在此示例中，第一个日记帐将包含与固定资产关联的帐簿，这些帐簿的编号为 1 到 2,011。</span><span class="sxs-lookup"><span data-stu-id="5ba61-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="5ba61-121">然后，第二个日记帐将包含与固定资产关联的帐簿，这些帐簿的编号为 2,012 到 4,000。</span><span class="sxs-lookup"><span data-stu-id="5ba61-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

> [!NOTE]
> <span data-ttu-id="5ba61-122">如果您具有包含不同分隔符（例如 – 或 /）的固定资产 ID，并且在批处理作业中创建了固定资产交易，则必须针对每种类型的分隔符运行单独的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="5ba61-122">If you have fixed asset IDs with different separators (such as – or /), and you create fixed asset transactions in batch jobs, you must run a separate batch job for each type of separator.</span></span> <span data-ttu-id="5ba61-123">系统无法在同一批处理作业中处理不同的分隔符。</span><span class="sxs-lookup"><span data-stu-id="5ba61-123">The system can't process different separators within the same batch job.</span></span>

<span data-ttu-id="5ba61-124">如果同一日记帐中不存在重复的资产 ID，则将限制帐簿的数量。</span><span class="sxs-lookup"><span data-stu-id="5ba61-124">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="5ba61-125">但是，如果资产 ID 与帐簿 ID 相同，则可以超出每个日记帐的帐簿数，以将资产 ID 保留在同一日记帐中。</span><span class="sxs-lookup"><span data-stu-id="5ba61-125">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="5ba61-126">例如，有 5,001 个固定资产 ID，每个固定资产 ID 与三本帐簿关联，而每本资产帐簿过帐到同一个过帐层。</span><span class="sxs-lookup"><span data-stu-id="5ba61-126">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="5ba61-127">您连续三个月运行折旧，但不汇总。</span><span class="sxs-lookup"><span data-stu-id="5ba61-127">You run depreciation for three consecutive months, without summarizing.</span></span>  <span data-ttu-id="5ba61-128">折旧日记帐将通过批处理作业创建，并且系统将创建七个日记帐，这些日记帐具有 667 个固定资产 ID，每个固定资产 ID 包含三本帐簿。</span><span class="sxs-lookup"><span data-stu-id="5ba61-128">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="5ba61-129">结果将为 2,001 本帐簿。</span><span class="sxs-lookup"><span data-stu-id="5ba61-129">The result will be 2,001 books.</span></span> <span data-ttu-id="5ba61-130">因此，在三个月内，将有 6003 个日记帐行在同一日记帐中维护相同的资产 ID。</span><span class="sxs-lookup"><span data-stu-id="5ba61-130">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="5ba61-131">系统还将创建一个日记帐，其中有 332 个固定资产 ID，每个固定资产 ID 三本帐簿。</span><span class="sxs-lookup"><span data-stu-id="5ba61-131">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="5ba61-132">在三个月内，将有 2988 行。</span><span class="sxs-lookup"><span data-stu-id="5ba61-132">In three months, there will be 2,988 lines.</span></span>

> [!NOTE] 
> <span data-ttu-id="5ba61-133">如果在创建折旧方案时启用了 **汇总折旧** 参数，**每个日记帐的帐簿数 - 折旧方案** 字段中的值将无效。</span><span class="sxs-lookup"><span data-stu-id="5ba61-133">If the **Summarize depreciation** parameter is turned on when you're creating a depreciation proposal, then the value in the **Number of books per journal - Depreciation proposal** field has no effect.</span></span> <span data-ttu-id="5ba61-134">在这种情况下，每个日记帐的帐簿数为 6000，这是内部定义的限制。</span><span class="sxs-lookup"><span data-stu-id="5ba61-134">In this case number of books per journal is 6000, which is the internal defined limit.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
