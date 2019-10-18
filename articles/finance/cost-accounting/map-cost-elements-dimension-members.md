---
title: 将成本元素维度成员映射到一组常用维度成员
description: 通过将不同的成本元素维度成员映射到一组通用的成本元素维度成员，您可以将数据合并为通用格式进行分析。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: deb9b5aab9cd69270c78d4e1ea0e2a6cac6ac370
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176606"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="0145d-103">将成本元素维度成员映射到一组常用维度成员</span><span class="sxs-lookup"><span data-stu-id="0145d-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0145d-104">通过将不同的成本元素维度成员映射到一组通用的成本元素维度成员，您可以将数据合并为通用格式进行分析。</span><span class="sxs-lookup"><span data-stu-id="0145d-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="0145d-105">如果您是一家全球性公司且遵守法定会计要求，您可能要使用多个会计科目表。</span><span class="sxs-lookup"><span data-stu-id="0145d-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="0145d-106">当您从不同的会计科目表导入成本元素维度成员时，您最后可能会将科目混合。</span><span class="sxs-lookup"><span data-stu-id="0145d-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="0145d-107">但是，这些科目实际上可能具有相同的本质，因此您想使用通用格式对它们进行分析并分摊成本。</span><span class="sxs-lookup"><span data-stu-id="0145d-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="0145d-108">将成本元素维度成员映射到通用格式</span><span class="sxs-lookup"><span data-stu-id="0145d-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="0145d-109">以下示例说明了您作为成本控制员可以如何在成本核算中创建新的成本元素维度，并且将来自美国会计科目表结构和法国会计科目表结构的成本元素维度成员映射到一组通用的成本元素维度成员。</span><span class="sxs-lookup"><span data-stu-id="0145d-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="0145d-110">然后，您可以使用这组通用的成本元素维度成员在成本核算分类帐中对来自两个法人的成本数据进行分析。</span><span class="sxs-lookup"><span data-stu-id="0145d-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="0145d-111">来源：美国会计科目表</span><span class="sxs-lookup"><span data-stu-id="0145d-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="0145d-112">来源：法国会计科目表</span><span class="sxs-lookup"><span data-stu-id="0145d-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="0145d-113">新的成本元素维度成员通用组</span><span class="sxs-lookup"><span data-stu-id="0145d-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="0145d-114">导入来自美国会计科目表的成本元素维度成员</span><span class="sxs-lookup"><span data-stu-id="0145d-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="0145d-115">导入来自法国会计科目表的成本元素维度成员</span><span class="sxs-lookup"><span data-stu-id="0145d-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="0145d-116">将美国和法国成本元素维度成员映射到通用组</span><span class="sxs-lookup"><span data-stu-id="0145d-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="0145d-117">5001：销售</span><span class="sxs-lookup"><span data-stu-id="0145d-117">5001: Sales</span></span>                                                           | <span data-ttu-id="0145d-118">5001：销售和广告</span><span class="sxs-lookup"><span data-stu-id="0145d-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="0145d-119">5000：销售和广告</span><span class="sxs-lookup"><span data-stu-id="0145d-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="0145d-120">5030：广告</span><span class="sxs-lookup"><span data-stu-id="0145d-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="0145d-121">6390：存货采购\*</span><span class="sxs-lookup"><span data-stu-id="0145d-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="0145d-122">7000：清洁费用</span><span class="sxs-lookup"><span data-stu-id="0145d-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="0145d-123">7001：清洁费用</span><span class="sxs-lookup"><span data-stu-id="0145d-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="0145d-124">7001：差旅费用</span><span class="sxs-lookup"><span data-stu-id="0145d-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="0145d-125">7001：差旅费用</span><span class="sxs-lookup"><span data-stu-id="0145d-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="0145d-126">\*存货采购法国成本元素维度成员未映射。</span><span class="sxs-lookup"><span data-stu-id="0145d-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="0145d-127">币种转换</span><span class="sxs-lookup"><span data-stu-id="0145d-127">Currency conversion</span></span>
<span data-ttu-id="0145d-128">您使用的不同会计科目表可以被设置为使用不同币种。</span><span class="sxs-lookup"><span data-stu-id="0145d-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="0145d-129">在这种情况下，请确保指定币种转换，以便按照使用成本元素维度成员所在的成本核算分类帐中的定义，使用正确的币种处理成本数据。</span><span class="sxs-lookup"><span data-stu-id="0145d-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="0145d-130">在前一示例中，如果在成本核算分类帐中使用美元 (USD)，您必须创建从 USD 到欧元 (EUR) 的币种转换，以便为映射的成本元素维度成员处理交易记录。</span><span class="sxs-lookup"><span data-stu-id="0145d-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="0145d-131">在任何时间更新映射</span><span class="sxs-lookup"><span data-stu-id="0145d-131">Update mappings at any time</span></span>
<span data-ttu-id="0145d-132">您可以在任何时间更新成本元素维度的映射定义。</span><span class="sxs-lookup"><span data-stu-id="0145d-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="0145d-133">由于映射不是按日期生效，因此将在您下一次处理成本交易记录或运行成本计算时应用更改。</span><span class="sxs-lookup"><span data-stu-id="0145d-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>



