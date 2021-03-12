---
title: 过帐定义
description: 本文提供有关过帐定义以及如何定义和关联它们的信息。 对于支持的过帐类型和文档，则可以使用过帐定义而不是过帐模板来分类会计条目中的主科目和财务维度。
author: ShylaThompson
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1da98461d1faf59ad8496dbc5623e97ac88c8a28
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990331"
---
# <a name="posting-definitions"></a><span data-ttu-id="76a11-104">过帐定义</span><span class="sxs-lookup"><span data-stu-id="76a11-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76a11-105">本文提供有关过帐定义以及如何定义和关联它们的信息。</span><span class="sxs-lookup"><span data-stu-id="76a11-105">This article provides information about posting definitions, and how to define and link them.</span></span>
<span data-ttu-id="76a11-106">对于支持的过帐类型和文档，则可以使用过帐定义而不是过帐模板来分类会计条目中的主科目和财务维度。</span><span class="sxs-lookup"><span data-stu-id="76a11-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="76a11-107">您可以在 **交易记录过帐定义** 页上查看支持的文档和过帐类型。</span><span class="sxs-lookup"><span data-stu-id="76a11-107">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="76a11-108">若要开始使用过帐定义，则在 **总帐参数** 页选择 **使用过帐定义** 选项。</span><span class="sxs-lookup"><span data-stu-id="76a11-108">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="76a11-109">即使在您使用过帐定义时，您仍必须为源条目和不支持的过帐类型和文档定义过帐模板。</span><span class="sxs-lookup"><span data-stu-id="76a11-109">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="76a11-110">您必须使用过帐定义以便支持采购订单的预留款核算和采购申请的预留款核算。</span><span class="sxs-lookup"><span data-stu-id="76a11-110">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="76a11-111">定义过帐定义</span><span class="sxs-lookup"><span data-stu-id="76a11-111">Defining posting definitions</span></span>
<span data-ttu-id="76a11-112">使用 **过帐定义** 页可以指定匹配条件并定义应在匹配发生时生成的条目。</span><span class="sxs-lookup"><span data-stu-id="76a11-112">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="76a11-113">匹配条件针对源条目评估为会计分配。</span><span class="sxs-lookup"><span data-stu-id="76a11-113">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="76a11-114">在 **过帐定义** 页中，您还可以分配优先级编号到条目行以控制评估行的订单。</span><span class="sxs-lookup"><span data-stu-id="76a11-114">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="76a11-115">具有最低优先级编号的行首先进行评估。</span><span class="sxs-lookup"><span data-stu-id="76a11-115">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="76a11-116">例如，具有优先级 1 的所有行进行评估，然后是具有优先级 2 的行，依此类推。</span><span class="sxs-lookup"><span data-stu-id="76a11-116">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="76a11-117">当找到匹配时，忽略其他匹配条件。</span><span class="sxs-lookup"><span data-stu-id="76a11-117">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="76a11-118">此外，只有与源交易记录匹配的组中的条件创建生成的条目。</span><span class="sxs-lookup"><span data-stu-id="76a11-118">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="76a11-119">通过使用 **测试过帐定义** 向导您可以验证您的过帐定义。</span><span class="sxs-lookup"><span data-stu-id="76a11-119">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="76a11-120">在您为过帐后定义定义一个示例源条目后，您将看到生成的条目。</span><span class="sxs-lookup"><span data-stu-id="76a11-120">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="76a11-121">您可以与生效日期一起使用过帐定义版本。</span><span class="sxs-lookup"><span data-stu-id="76a11-121">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="76a11-122">例如，您可以创建过帐定义的将来版本过帐到一个新的会计年度的不同会计科目。</span><span class="sxs-lookup"><span data-stu-id="76a11-122">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="76a11-123">使用 **交易记录过帐定义** 页可以分配过帐定义到交易记录类型。</span><span class="sxs-lookup"><span data-stu-id="76a11-123">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="76a11-124">链接过帐定义</span><span class="sxs-lookup"><span data-stu-id="76a11-124">Linking posting definitions</span></span>
<span data-ttu-id="76a11-125">在您创建过帐定义时，您可以从一个过帐定义链接到另一个。</span><span class="sxs-lookup"><span data-stu-id="76a11-125">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="76a11-126">除了当前过帐定义的标准外，然后还考虑您链接到的定义的条件。</span><span class="sxs-lookup"><span data-stu-id="76a11-126">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="76a11-127">此功能帮助您节省时间，因为如果您已输入另一个定义的那些行，您则不必在 **过帐定义** 页的 **条目** 快速选项卡重新输入条件。</span><span class="sxs-lookup"><span data-stu-id="76a11-127">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="76a11-128">在图或表中，包括您可以使用的所有链接。</span><span class="sxs-lookup"><span data-stu-id="76a11-128">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="76a11-129">为避免与当前过帐定义的冲突，请确保您链接的所有过帐定义的行是唯一的。</span><span class="sxs-lookup"><span data-stu-id="76a11-129">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="76a11-130">当您在过帐定义创建链接时，适用以下限制:</span><span class="sxs-lookup"><span data-stu-id="76a11-130">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="76a11-131">指定过帐定义可以链接到另一个过帐定义或从另一个过帐定义链接，但不能同时链接这两者。</span><span class="sxs-lookup"><span data-stu-id="76a11-131">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="76a11-132">但是，过帐定义能与多个过帐定义链接。</span><span class="sxs-lookup"><span data-stu-id="76a11-132">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="76a11-133">您可以设置只在同一个模块中的过帐定义之间的链接。</span><span class="sxs-lookup"><span data-stu-id="76a11-133">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="76a11-134">您可以分配过帐定义到任何交易记录类型，但是，交易记录类型必须作为过帐定义在同一模块。</span><span class="sxs-lookup"><span data-stu-id="76a11-134">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="76a11-135">使用 **交易记录过帐定义** 页可以查看交易记录类型在哪个模块。</span><span class="sxs-lookup"><span data-stu-id="76a11-135">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="76a11-136">有关详细信息，请参阅[过帐定义示例](example-posting-definitions.md)。</span><span class="sxs-lookup"><span data-stu-id="76a11-136">For more information, see [Posting definition examples](example-posting-definitions.md).</span></span> 


